---
name: botw-decomp
description: Guia y asistente experto para contribuir al proyecto de decompilacion de The Legend of Zelda Breath of the Wild (zeldaret/botw, uking Switch 1.5.0). Activalo cuando el usuario mencione botw decomp, uking, zeldaret/botw, igualar ensamblador AArch64 con Clang 4.0.1, des-inlinear funciones de sead/ksys/agl/Havok, analizar pseudocodigo de IDA/Ghidra de BotW, usar diff.py, tools/check o data/uking_functions.csv.
---
# BotW Decomp

Asistente especializado en ingeniería inversa y decompilación *matching* de C++ para el proyecto **The Legend of Zelda: Breath of the Wild Decompilation (`zeldaret/botw`)**.
## Tecnologías
Sistema operativo: Ubuntu 26.04.1 LTS (WSL)
Arquitectura del sistema operativo: x86_64
Editor de código: Antigravity IDE (WSL 2 Remote)
Extensiones: clangd, CMake Tools, CMake IntelliSense, Python
Lenguajes de programación: Assembly (Aarch64), C++ 17 y Python3
Versión de CMake: 4.2.3
Versión de Clang/Clang++: 4.0.1
Versión de Ghidra: 12.1.4
Extensiones de Ghidra: Ghidra MCP, SwitchLoader
Arquitectura destino del proyecto: Aarch64 (Nintendo Switch)
## GhidraMCP
Para ejecutar el MCP se usa `ghidra-mcp`.
## When to Use

- Traducir pseudocódigo de Ghidra (`main.nso.h`, `main.nso.c`) a código C++17 limpio y equivalente al original de Nintendo Switch.
- Identificar y des-inlinear (*uninline*) funciones comunes de las librerías `sead`, `ksys` (KingSystem), `gsys`, `agl`, `xlink2` y `Havok`.
- Diagnosticar y resolver diferencias de código ensamblador AArch64 (*mismatches* de registro, orden de bloques básicos, banderas de comparación) usando `./diff.py`.
- Configurar el entorno de compilación, registrar símbolos en `data/uking_functions.csv` y validar con `tools/check`.

## Recursos de la Skill

Consulta los archivos de referencia incluidos en esta skill según la necesidad:

- `references/cheatsheet_inlines.md`: Patrones detallados de funciones inline de `sead`, `ksys` y `Havok`, además de estrategias de resolución de *mismatches* en AArch64.
- `references/uking_structures.md`: Referencia de estructuras clave del motor (`ksys::act::Actor`, `ksys::act::BaseProc`, `ksys::gdt::GameData`, `ksys::phys`, `sead` y `Havok`) y sus layouts de memoria.

## Flujo de Trabajo Estándar (Step-by-Step)

1. Compila el proyecto con Ninja y verifica que el estado base sea limpio:
   ```bash
   ninja -C build
   tools/check
   ```

### 2. Selección y Análisis de la Función
1. Abre el MCP de Ghidra y localiza la función o clase a decompilar (en `src/KingSystem/` o `src/Game/`).
2. Consulta `references/uking_structures.md` o los encabezados del repositorio para verificar los tipos de datos exactos, offsets de miembros y herencia (`vtable`).
3. Antes de escribir C++, identifica qué partes del pseudocódigo son artefactos del compilador o funciones inline:
   - Bucles manuales de longitud o comparación de strings suelen ser métodos inline de `sead::SafeString`.
   - Llamadas a `_cxa_guard_acquire` con comprobación de RTTI corresponden a `sead::DynamicCast<T*>()`.
   - Asignaciones con `operator new` seguidas de constructor corresponden a `new (heap) SomeClass` o `sead::Buffer::allocBuffer`.
   - Revisa `references/cheatsheet_inlines.md` para ver la tabla de conversión completa.

### 3. Implementación en C++17 (Guía de Estilo de `zeldaret/botw`)
- **Código C++ natural:** No traduzcas el pseudocódigo de C literalmente línea por línea ni uses aritmética de punteros cruda (`*(int*)((char*)this + 0x14)`). Define los miembros en el `struct`/`class` y accede a ellos normalmente.
- **Nombres de miembros:** Usa el prefijo `m` para variables miembro (`mFlags`, `mActorParam`), `s` para estáticas (`sInstance`) y `c` para constantes.
- **Punteros y tipos:** Usa `nullptr` en lugar de `NULL` o `0LL`. Usa los tipos base de `sead` (`u8`, `u16`, `u32`, `u64`, `s8`, `s16`, `s32`, `s64`, `f32`, `f64`).
- **Inicialización en cabecera:** Inicializa los miembros por defecto directamente en la definición de la clase/estructura en el `.h` para que el constructor generado coincida con el original.

### 4. Registro del Símbolo Mangled
1. Compila con `ninja -C build`.
2. Obtén el nombre *mangled* de la función recién implementada:
   ```bash
   tools/print_decomp_symbols.py -a | grep NombreDeClase::nombreFuncion
   ```
3. Abre `data/uking_functions.csv`, busca la dirección hexadecimal de la función (ej. `0x00000071010c0d60`) y añade el símbolo *mangled* en la última columna:
   ```csv
   0x00000071010c0d60,sub_71010C0D60,136,_ZN4ksys4util13TaskQueueBaseD1Ev
   ```

### 5. Comparación de Ensamblador y Matching
1. Ejecuta `diff.py` para comparar el ensamblador original (izquierda) con el generado por Clang 4.0.1 (derecha):
   ```bash
   ./diff.py --source _ZN4ksys4util13TaskQueueBaseD1Ev
   ```
   - Agrega `-mw3` para recompilar automáticamente al guardar cambios en el archivo fuente.
   - Agrega `--inlines` si necesitas inspeccionar llamadas inline complejas.
2. Ignora diferencias de reubicación de direcciones en pares `adrp` + `ldr` o instrucciones `b` / `bl`.
3. Si hay diferencias de código (*mismatches*), aplica las técnicas de `references/cheatsheet_inlines.md` (invertir condicionales, revisar signedness `u32` vs `s32`, cambiar entre `for (auto& x : arr)` e iteradores explícitos, o usar `sead::Mathf`).

### 6. Cierre y Formateo
1. Si la función coincide al 100%, deja el nombre *mangled* limpio en `data/uking_functions.csv`.
2. Si queda una diferencia menor (ej. un *regalloc* o reordenamiento mínimo), añade un comentario `// NON_MATCHING: explicación` sobre la función y coloca un `?` al final del símbolo en `data/uking_functions.csv`. Si la diferencia es grande, usa `!`.
3. Formatea el código con `clang-format` y ejecuta `tools/check` antes de crear el commit.

## Gotchas

- **No escribas bucles manuales para `sead::SafeString`:** Casi todos los bucles raros que avanzan de 3 en 3 bytes o comprueban `0x80000` e invocan `assureTerminationImpl_` son llamadas inline a `calcLength()`, `isEqual()`, `operator==` o `include()`.
- **Cuidado con `fmin` vs `fminnm` en AArch64:** En el pseudocódigo ambos aparecen como `fminf`, pero en ensamblador `fmin` proviene de `sead::Mathf::maxClamp` (o ternario `x < y ? x : y`) y `fminnm` proviene de `sead::Mathf::min` (`std::min`).
- **Comparaciones en punto flotante y NaN:** En AArch64, `x > 5.0f` y `!(x <= 5.0f)` generan saltos condicionales distintos debido al manejo de `NaN`. Si una rama parece invertida, invierte la condición del `if`.
