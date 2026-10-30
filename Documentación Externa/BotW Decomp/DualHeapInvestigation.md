# Resumen de Hallazgos Técnicos de la Investigación (DualHeapInvestigation)

Este documento recopila todos los hallazgos técnicos, arquitectónicos y de entorno descubiertos durante la sesión de trabajo que no corresponden exclusivamente a la lógica interna de `DualHeap`.

---

## 1. Entorno de Decompilación: GhidraMCP sobre WSL2

Durante la verificación del entorno se descubrió la arquitectura exacta de conexión con Ghidra:

* **Topología:** Ghidra (v12.1.4 con extensión GhidraMCP y SwitchLoader) corre de forma nativa en el host Windows (`D:\Decomps\botw`, PID 4948), analizando `main.uncompressed.nso`.
* **Comunicación Inter-Procesos:** Debido a que corre en Windows, los sockets Unix de `/tmp` no están compartidos con WSL2. Sin embargo, el servidor HTTP de GhidraMCP expone su API en el puerto `8089`. Gracias al *localhost forwarding* nativo de WSL2, es completamente accesible desde Linux mediante peticiones HTTP estándar a `http://127.0.0.1:8089`.
* **Endpoints y Restricciones:**
  - Consulta de metadatos: `/mcp/instance_info`.
  - Descompilación on-demand: `/decompile_function?address=0x...&program=main.uncompressed.nso`.
  - Modificación de prototipos: `/set_function_prototype`. Para funciones AArch64 libres o estáticas se debe especificar la convención `"__cdecl"`.
  - **Peculiaridad de tipos:** El parser C de Ghidra en esta versión no resuelve el typedef `size_t` en prototipos; debe usarse `ulong` (o `unsigned long`) para evitar errores de sintaxis.

---

## 2. El Toolchain y la Trampa de `CMAKE_BUILD_TYPE`

Al comparar inicialmente el código ensamblador con `tools/check`, se observó un desfase masivo: el compilador generaba decenas de instrucciones de guardado en stack (`stur`/`ldur`) innecesarias.

* **Causa descubierta:** El workspace estaba configurado en `CMAKE_BUILD_TYPE=Debug`.
* **Efecto de la optimización:** El archivo `toolchain/ToolchainNX64.cmake` inyecta las banderas de optimización `-O3 -g` exclusivamente en las variables `CMAKE_CXX_FLAGS_RELEASE` y `CMAKE_CXX_FLAGS_RELWITHDEBINFO`. Al estar en `Debug`, Clang 4.0.1 compilaba sin optimización (`-O0`).
* **Solución aplicada:** Reconfigurar con `cmake -B build -DCMAKE_BUILD_TYPE=Release`. Inmediatamente la generación de código pasó a optimizar registros volátiles (`w22`, `w23`, `x24`, etc.) y desenrollar/inlinear según el estándar de Nintendo.

---

## 3. Funcionamiento Interno de `sead::Heap` y `sead::ExpHeap`

A partir de la descompilación de las funciones base de `sead` (`0x7100b04604`, `0x7100b053a8`, `0x7100b05ef4`), se identificaron detalles internos clave:

### A. Estructura y Vtable de `sead::Heap`
Los offsets y llamadas virtuales descubiertos en AArch64:
- `vptr[2]` (`+0x10`): Comprobación de RTTI (`checkDerivedRuntimeTypeInfo`).
- `vptr[6]` (`+0x30`): Método virtual `tryAlloc(size, alignment)`.
- `vptr[0x10]` (`+0x80`): Método virtual `getMaxAllocatableSize(alignment)`.
- `vptr[0x1a]` (`+0xd0`): Registro de heap subordinado `pushBackChild_(Heap* child)`.
- Campo `+0x90`: Almacena la dirección del heap (`mDirection`), donde `1 = cHeapDirection_Forward` y `-1 = cHeapDirection_Reverse`.

### B. Estructura de `sead::MemBlock` (Gestor de Bloques Libres)
- Un `sead::MemBlock` ocupa exactamente **32 bytes (`0x20`)**:
  - `mListNode` (`0x10` bytes): punteros `prev` y `next`.
  - `mHeapCheckTag` (`0x02` bytes): etiqueta mágica de validación de integridad.
  - `mOffset` (`0x02` bytes): offset de alineación.
  - `mSize` (`0x08` bytes): tamaño neto del bloque libre.
- La función interna `sead::ExpHeap::pushToFreeList_` (`0x7100b05ef4`) es la encargada de registrar estos bloques libres en la lista enlazada del heap.

---

## 4. El Mecanismo de `DualFrameHeap` y `EmergencyHeap`

Al analizar la función `FUN_71010bdfb4` (`DualHeapOrDualFrameHeap::tryAllocFromFrameHeapOrEmergency`), se descubrieron componentes clave del subsistema de tolerancia a fallos:

1. **`DualFrameHeap`:**
   - Variante análoga a `DualHeap`, pero derivada de `sead::FrameHeap` en lugar de `sead::ExpHeap`.
   - Tiene su puntero de heap secundario en el offset `0xf0` y un acumulador de bytes asignados en `0xf8`.
2. **Detección de `EmergencyHeap`:**
   - El motor comprueba dinámicamente si el nombre del heap en `*(char**)(heap + 0x28)` coincide exactamente con la cadena literal `"EmergencyHeap"`.
   - Si la asignación estándar falla y se detecta que el heap de respaldo es `EmergencyHeap`, el juego invoca una rutina especial del sistema de actores (`FUN_7100fd266c`) para notificar o mitigar la escasez crítica de memoria antes de registrar el consumo de emergencia.

---

## 5. Dinámica de Consumo de Tokens en Agentes VS Code / Gemini API

A raíz de la consulta sobre el costo incurrido durante los primeros turnos de chat, se desglosó el funcionamiento del protocolo de agentes:

* **Inyección de Schemas JSON:** Las extensiones instaladas (CMake Tools, C/C++ Tools, Pylance, Playwright) registran docenas de herramientas con descripciones extensas. Solo el contexto estático inicial de herramientas y directivas pesa entre 15.000 y 25.000 tokens en cada petición.
* **Bucle Autónomo de Herramientas:** Cada acción que el agente decide ejecutar en terminal o archivo (`read_file`, `curl`, `ninja`, `check`) cuenta como una interacción independiente contra la API. Por tanto, una sola instrucción de usuario puede generar fácilmente 8 a 10 viajes ida y vuelta acumulando el historial completo.
* **Caché de Contexto:** Cuando no hay *prompt caching* activo entre turnos consecutivos con salidas extensas de comandos, el volumen total de tokens facturados puede multiplicarse rápidamente, explicando por qué una conversación aparentemente corta puede procesar cientos de miles de tokens de entrada.
