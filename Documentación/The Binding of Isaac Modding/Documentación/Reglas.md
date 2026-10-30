# Reglas de Linter con Valor Real en Modding para The Binding of Isaac

En el desarrollo de mods para *The Binding of Isaac: Repentance* mediante TypeScript e IsaacScript (compilados a Lua con TypeScript-to-Lua / TSTL), las herramientas de análisis estático (como ESLint y Oxlint) contienen cientos de reglas. 

Esta nota documenta **únicamente las reglas que tienen un valor funcional real dentro del motor del juego y su entorno de ejecución**. Se omiten deliberadamente las reglas genéricas de "calidad de código" o estilo (como `prefer-const`, `no-unused-vars`, `eqeqeq`, etc.), ya que su propósito es cosmético o de higiene general en JavaScript/TypeScript y no influyen en el comportamiento interno del juego.

---

## ¿Por qué ciertas reglas tienen valor crítico en Isaac?

El entorno de modding de Isaac presenta restricciones técnicas muy específicas:
1. **Máquina Virtual de Lua 5.3:** El código transpilado corre sobre un runtime de Lua embebido en el ejecutable en C++ del juego.
2. **Ciclo síncrono por fotograma (Frame Loop):** La lógica del juego corre a 30 actualizaciones por segundo (ticks) y el renderizado a 60 FPS, sin tolerancia a excepciones no controladas.
3. **Paso por referencia y metamétodos de C++:** Las entidades, vectores y tablas de persistencia interactúan directamente con punteros de C++ expuestos a Lua.
4. **Persistencia mediante Save Data (`v`):** La partida guarda datos estructurados en disco mediante serialización de tablas.

Cualquier regla de linter relevante debe responder a una de estas realidades técnicas.

---

## 1. Prevención de Crashes y Congelamiento del Frame Loop

### `isaacscript/no-throw`
* **Estado:** Activada (o verificada manualmente en Oxlint).
* **Impacto en Isaac:** 🔴 **Crítico (Crash to Desktop / Desincronización del bucle de eventos)**.
* **Causa técnica:** En JavaScript/Node.js, una excepción puede capturarse en un bloque global. Sin embargo, TSTL transpila `throw new Error(...)` a una llamada nativa a `error()` de Lua. Cuando un callback de Isaac (`MC_POST_UPDATE`, `MC_ENTITY_TAKE_DMG`, etc.) ejecuta `error()`, el motor del juego no se recupera: **la partida se congela de inmediato, los demás callbacks dejan de ejecutarse o el juego se cierra directamente al escritorio (CTD)**.
* **Solución aplicada:** Prohibir el uso de `throw`. En su lugar, se utilizan retornos defensivos anticipados (`return`) y advertencias en el registro de depuración del juego:
  ```typescript
  // ❌ Peligro de cierre del juego
  if (!player) {
    throw new Error("Player not found")
  }

  // ✅ Correcto en Isaac
  if (!player) {
    Isaac.DebugString("[MI-MOD ERROR] Player not found")
    return
  }
  ```

---

### `no-floating-promises` / Prohibición de Asincronía (`async` / `await`)
* **Estado:** Activada.
* **Impacto en Isaac:** 🔴 **Crítico (Pérdida de sincronización con los frames del juego)**.
* **Causa técnica:** El motor de The Binding of Isaac opera en un bucle completamente síncrono. La máquina virtual de Lua del juego **carece de un Event Loop** (no existen `setTimeout`, `setImmediate` ni microtareas). Usar promesas o funciones `async` genera código que no se reanuda en el frame correspondiente, perdiendo el determinismo de la partida y provocando que las entidades queden en estados corruptos o desfasados.
* **Solución aplicada:** Toda la lógica de temporizadores en un mod debe calcularse explícitamente contando frames en el callback `MC_POST_UPDATE` (ej. mediante contadores de ticks o `Game():GetFrameCount()`).

---

## 2. Integridad de Memoria y Manejo de Tablas

### `isaacscript/no-invalid-default-map`
* **Estado:** Activada (o verificada manualmente en Oxlint).
* **Impacto en Isaac:** 🔴 **Crítico (Corrupción de datos cruzados entre entidades/jugadores)**.
* **Causa técnica:** `DefaultMap` es la estructura de IsaacScript utilizada comúnmente para asociar datos por jugador (`PlayerIndex`), entidad o habitación. En Lua y JavaScript, los objetos y listas se pasan por referencia. Si se inicializa un `DefaultMap` pasando un array u objeto directo (`new DefaultMap([])`), **todas las claves del mapa apuntarán exactamente a la misma tabla en la memoria de Lua**. Si el Jugador 0 recibe un item en su lista, el Jugador 1 también lo recibirá automáticamente.
* **Solución aplicada:** Exigir siempre una función fábrica para cualquier valor que no sea un primitivo:
  ```typescript
  // ❌ Error: Todas las entidades comparten el mismo array en Lua
  const entityCooldowns = new DefaultMap<PtrHash, number[]>([])

  // ✅ Correcto: Cada entidad obtiene su propia instancia independiente
  const entityCooldowns = new DefaultMap<PtrHash, number[]>(() => [])
  ```

---

### `no-delete-expression` (en arreglos numéricos)
* **Estado:** Activada.
* **Impacto en Isaac:** 🟡 **Alto (Corrupción de longitud de tablas y corte de bucles `ipairs`)**.
* **Causa técnica:** En Lua, los arreglos se representan como tablas con claves numéricas secuenciales del 1 a N. El operador `delete arr[index]` de TypeScript se transpila en Lua como `arr[index] = nil`. En Lua, insertar un `nil` en medio de una tabla secuencial crea un "hueco" (*sparse table*), lo que rompe el operador de longitud `#arr` y provoca que bucles nativos como `ipairs` se interrumpan antes de tiempo, dejando de actualizar o renderizar proyectiles o enemigos activos.
* **Solución aplicada:** Prohibir `delete` en colecciones numéricas; utilizar métodos mutadores que reorganicen los índices de la tabla (como `table.remove` o `.splice()`).

---

## 3. Compatibilidad con la API en C++/Lua de Isaac

### `@typescript-eslint/no-base-to-string` (con excepción para `Vector`)
* **Estado:** Activada con excepción `{ ignoredTypeNames: ["Vector"] }`.
* **Impacto en Isaac:** 🟡 **Medio (Depuración ilegible y errores en HUD/logs)**.
* **Causa técnica:** En Lua, convertir una tabla o userdata a string (por ejemplo, `` `Player: ${player}` ``) produce el puntero de memoria opaco de la tabla (ej. `"table: 0x01a8f9b0"`), lo cual ensucia los logs y rompe cualquier renderizado de texto en pantalla con la fuente del juego.
* **La excepción específica de Isaac:** La clase nativa `Vector` de Isaac cuenta con una sobrecarga del metamétodo `__tostring` implementada en la capa de C++, por lo que `Vector(1, 2)` sí imprime limpiamente `(1, 2)`. La regla debe permitir esta excepción y prohibir interpolar directamente entidades o tablas sin acceder a sus propiedades explícitas (`player.Index`, `entity.Type`).

---

### `@typescript-eslint/naming-convention` (Adaptada al motor de Isaac)
* **Estado:** Configurada especialmente para permitir `UPPER_CASE`.
* **Impacto en Isaac:** 🟡 **Medio (Interoperabilidad con las constantes del juego)**.
* **Causa técnica:** La API en C++/Lua de The Binding of Isaac define todas las enumeraciones y tipos en mayúsculas sostenidas (`CollectibleType.COLLECTIBLE_BRIMSTONE`, `EntityType.ENTITY_TEAR`, `ModCallbacks.MC_POST_UPDATE`, `SoundEffect.SOUND_1UP`). Si se aplicara la convención estándar de TypeScript (`PascalCase` para miembros de enums), causaría constantes errores de tipado o forzaría nombres inconsistentes con la documentación oficial del juego.

---

### `complete/no-number-enums` y `complete/consistent-enum-values`
* **Estado:** Desactivadas (`"off"`).
* **Impacto en Isaac:** 🔴 **Crítico (Rompería la llamada a funciones nativas en C++)**.
* **Causa técnica:** En TypeScript estándar se suele desaconsejar el uso de enums numéricos en favor de uniones de strings. No obstante, **el motor de Isaac en C++ trabaja internamente con IDs numéricos enteros** para registrar callbacks, invocar entidades y asignar coleccionables. Activar estas reglas impediría el uso de enums numéricos indispensables para la API de Isaac.

---

### `no-bitwise-operators`
* **Estado:** Desactivada (`"off"`).
* **Impacto en Isaac:** 🔴 **Crítico (Imposibilidad de leer y alterar máscaras de bits del juego)**.
* **Causa técnica:** Isaac gestiona el estado y las propiedades de las entidades mediante máscaras de bits (*bitmasks*):
  * `TearFlags` (efectos de lágrimas como veneno, fuego, rebote, espectral).
  * `DamageFlag` (tipos de daño como autodestrucción, fuego, penetración).
  * `EntityFlag` y `CacheFlag` (recalculo de estadísticas y estados de entidad).
  Prohibir operadores a nivel de bits (`&`, `|`, `~`, `<<`) impediría consultar o combinar flags requeridas para la mecánica básica de cualquier mod.

---

### `@typescript-eslint/no-unsafe-unary-minus`
* **Estado:** Desactivada (`"off"`).
* **Impacto en Isaac:** 🟢 **Bajo / DX (Falsos positivos con el tipo `int` de IsaacScript)**.
* **Causa técnica:** IsaacScript define tipos nominales para representar enteros (`int`) que se ajustan al rendimiento de Lua 5.3 y C++. Esta regla de ESLint emite falsos positivos al negar enteros (como `-1 as int` o invertir coordenadas de velocidades en proyectiles), por lo que debe mantenerse apagada.

---

### `@typescript-eslint/require-array-sort-compare`
* **Estado:** Desactivada (`"off"`).
* **Impacto en Isaac:** 🟢 **Bajo / DX (Comportamiento nativo de `table.sort` en Lua)**.
* **Causa técnica:** En JavaScript, `[10, 2].sort()` ordena por texto dando `[10, 2]`. Sin embargo, TypeScript-to-Lua compila `.sort()` directamente a la función nativa `table.sort()` de Lua, la cual compara números por valor nativo de forma automática. No es necesario imponer una función de ordenamiento manual en arrays numéricos.

---

## 4. Persistencia y Save Data (`v`)

### `complete/sort-objects`
* **Estado:** Desactivada (`"off"`).
* **Impacto en Isaac:** 🟡 **Medio (Estructura determinista de los datos de guardado)**.
* **Causa técnica:** En los proyectos con IsaacScript, la persistencia se centraliza en el objeto global `v`, el cual se serializa en el archivo `save.dat` del mod (usando `json.encode` o `Isaac.SaveModData`). Este objeto requiere una organización jerárquica y semántica (por ejemplo, número de versión de guardado primero, seguido de estados de la run y configuración). Forzar un orden alfabético automático desorganiza la estructura lógica y puede dificultar migraciones seguras entre versiones del mod.

---

## Tabla Resumen de Reglas con Valor en Isaac

| Regla | Configuración | Justificación en el Motor de Isaac |
| :--- | :--- | :--- |
| `isaacscript/no-throw` | **Obligatoria** | Evita que una excepción no capturada en Lua cierre el juego (Crash to Desktop). |
| `no-floating-promises` | **Obligatoria** | La VM de Lua de Isaac no tiene Event Loop; previene desincronización de frames. |
| `isaacscript/no-invalid-default-map` | **Obligatoria** | Evita que jugadores o entidades compartan la misma referencia de array/objeto en memoria. |
| `no-delete-expression` (arrays) | **Obligatoria** | Evita tablas con huecos (`nil`) que rompen el operador `#` e interrupciones en `ipairs`. |
| `@typescript-eslint/no-base-to-string` | **Obligatoria (con excepción)** | Evita imprimir `"table: 0x..."`; permite únicamente `Vector` (con `__tostring` en C++). |
| `@typescript-eslint/naming-convention` | **Adaptada (`UPPER_CASE`)** | Permite interactuar con enums y constantes nativas de la API del juego. |
| `complete/no-number-enums` | **Desactivada (`off`)** | La API de Isaac en C++ exige identificadores numéricos enteros. |
| `complete/consistent-enum-values` | **Desactivada (`off`)** | Permite los enums numéricos requeridos por el motor. |
| `no-bitwise-operators` | **Desactivada (`off`)** | Indispensable para manipular máscaras de bits (`TearFlags`, `DamageFlag`, `EntityFlag`). |
| `@typescript-eslint/no-unsafe-unary-minus` | **Desactivada (`off`)** | Evita falsos positivos con el tipo `int` propio de IsaacScript. |
| `@typescript-eslint/require-array-sort-compare` | **Desactivada (`off`)** | TSTL compila a `table.sort()` de Lua que compara números nativamente. |
| `complete/sort-objects` | **Desactivada (`off`)** | Respeta el orden semántico del esquema de guardado del mod (`save.dat` / `v`). |

---

## Relación con la Guía de Migración
Para consultar las reglas que no son soportadas en Oxlint y deben verificarse manualmente durante el desarrollo, revisa la [[Documentación/The Binding of Isaac Modding/Documentación/Guía|Guía de Reglas Incompatibles y Omitidas en Oxlint]].
