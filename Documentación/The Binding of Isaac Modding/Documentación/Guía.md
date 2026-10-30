# Guía de Reglas Incompatibles y Omitidas de IsaacScript en Oxlint

Al migrar la configuración base de **`eslint-config-isaacscript`** a **Oxlint** para mods de *The Binding of Isaac* (desarrollados con TypeScript-to-Lua / TSTL), varias reglas originales de ESLint no pueden ejecutarse o fueron omitidas en `oxlint.config.ts`.

Este documento detalla cada una de estas reglas, si son **Type-Aware** o **Sintácticas no implementadas**, su criticidad real dentro del motor del juego y **qué debes verificar manualmente** en tu código para evitar bugs, desincronizaciones o crasheos.

---

## Comparativa: Reglas Originales vs. Estado en Oxlint

| Regla Original | ¿Está en `oxlint.config.ts`? | Motivo de Incompatibilidad / Omisión | Criticidad en Isaac |
| :--- | :--- | :--- | :--- |
| `isaacscript/no-invalid-default-map` | ❌ Omitida | **Type-Aware** (`getParserServices` falla en `jsPlugins`) | 🔴 **Crítica** |
| `isaacscript/no-throw` | ❌ Omitida | **Type-Aware** (Falla en `jsPlugins`) | 🔴 **Crítica** |
| `@typescript-eslint/naming-convention` | ❌ Omitida | **Type-Aware** / Muy compleja para Oxlint AST | 🟡 **Media** (Convención / DX) |
| `@typescript-eslint/no-base-to-string` | ❌ Omitida | **Type-Aware** (Oxlint no soporta `ignoredTypeNames`) | 🟡 **Media** (Depuración / Logs) |
| `@typescript-eslint/no-unsafe-unary-minus` | ❌ Omitida | **Type-Aware** (`off` en ESLint por tipos `int`) | 🟢 **Baja** (Informativa) |
| `@typescript-eslint/require-array-sort-compare` | ❌ Omitida | **Type-Aware** (`off` en ESLint por `table.sort`) | 🟢 **Baja** (Informativa) |
| `complete/consistent-enum-values` | ❌ Omitida | Regla de `eslint-plugin-complete` (`off` en ESLint) | 🟢 **Baja** |
| `complete/no-number-enums` | ❌ Omitida | Regla de `eslint-plugin-complete` (`off` en ESLint) | 🟢 **Baja** |
| `complete/sort-objects` | ❌ Omitida | Regla de `eslint-plugin-complete` (`off` en ESLint) | 🟢 **Baja** |
| `import-x/no-extraneous-dependencies` (archivos config) | ❌ Omitida | Bloque `overrides` de archivos de configuración | 🟢 **Baja** (Solo build tooling) |
| `import-x/no-relative-packages` (archivos config) | ❌ Omitida | Monorepos / archivos de config | 🟢 **Baja** (Solo build tooling) |
| Reglas de formateo de estilo (`semi`, etc.) | ❌ Omitida | Omitidas en Oxlint por diseño; delegadas a **Oxfmt** (`oxfmt.config.ts`) | 🟢 **Baja** (Estilo / DX) |

---

## 1. Reglas Críticas que Debes Verificar Manualmente

### 1.1 `isaacscript/no-invalid-default-map`
* **Tipo:** Type-Aware (Verifica si el valor por defecto es una referencia o un primitivo).
* **Por qué es crítica:** En JavaScript y Lua, los objetos y arreglos se pasan por referencia. Si inicializas un `DefaultMap` pasando un array u objeto (`new DefaultMap([])`), **todas las claves del mapa compartirán la misma instancia en memoria**. Si agregas un item al jugador 0, el jugador 1 también lo recibirá mágicamente.
* **Qué verificar manualmente:**
  ```typescript
  // ❌ ERROR GRAVE: Ambos jugadores alteran la misma lista en Lua
  const inventory = new DefaultMap<PlayerIndex, ItemType[]>([]);

  // ✅ CORRECTO: Usar una función fábrica constructora
  const inventory = new DefaultMap<PlayerIndex, ItemType[]>(() => []);
  ```
  > **Regla de oro:** En `new DefaultMap(...)`, solo pasa valores literales si son primitivos (`0`, `false`, `""`). Para cualquier estructura (`[]`, `{}`, `new Set()`), pasa siempre una función flecha `() => ...`.

---

### 1.2 `isaacscript/no-throw`
* **Tipo:** Type-Aware / Control de flujo.
* **Por qué es crítica:** The Binding of Isaac corre sobre una VM de **Lua 5.3**. Cuando TypeScript-to-Lua transpila un `throw new Error(...)`, genera una llamada nativa a `error()`. A diferencia de Node.js o el navegador, la API de Isaac no maneja excepciones no capturadas de forma elegante: **el frame loop se rompe, la partida se congela o el juego se cierra al escritorio**.
* **Qué verificar manualmente:**
  ```typescript
  // ❌ NUNCA USES THROW EN MODS DE ISAAC
  if (!player) {
    throw new Error("Jugador no encontrado");
  }

  // ✅ CORRECTO: Retorno defensivo y reporte en logs
  if (!player) {
    Isaac.DebugString("[MI-MOD] Jugador no encontrado");
    return;
  }
  ```

---

### 1.3 `@typescript-eslint/naming-convention`
* **Tipo:** Sintáctica / Type-Aware.
* **Por qué importa:** En IsaacScript se personalizó esta regla con un propósito clave: **permitir que los miembros de Enums usen `UPPER_CASE`** y las variables acepten `camelCase`, `PascalCase` y `UPPER_CASE`.
* **Razón técnica:** La API interna del juego en C++/Lua expone constantes en mayúsculas sostenidas (`CollectibleType.COLLECTIBLE_SAD_ONION`, `EntityType.ENTITY_TEAR`). ESLint estándar marcaría error al usar mayúsculas en TypeScript convencional.
* **Qué verificar manualmente:**
  - Al definir enums para tu mod, mantén la convención de Isaac usando mayúsculas:
    ```typescript
    export enum CustomCustomFlag {
      FLAG_BURNING = 1 << 0,
      FLAG_POISON = 1 << 1,
    }
    ```
  - Si en el futuro activas un linter de nombres estricto, no permitas que renombre tus enums a `PascalCase` si interactúan con tablas del juego.

---

### 1.4 `@typescript-eslint/no-base-to-string`
* **Tipo:** Type-Aware.
* **Por qué importa:** Evita interpolar accidentalmente objetos complejos dentro de strings (ej. `` `Jugador: ${player}` ``), lo cual en Lua se traduce en cadenas inútiles como `"table: 0x01a8f9b0"`.
* **Excepción de Isaac:** En la config original se añadía `{ ignoredTypeNames: ["Vector"] }` porque la clase `Vector` de Isaac cuenta con un metamétodo `__tostring` en C++ que imprime limpiamente sus coordenadas `(X, Y)`.
* **Qué verificar manualmente:**
  - No imprimas entidades o tablas directamente: imprime sus propiedades (`${player.Index}`, `${entity.Type}`).
  - `Vector` es el único objeto de Isaac seguro para interpolar directamente en strings.

---

## 2. Reglas que estaban en `"off"` en ESLint (¿Afecta haberlas omitido?)

En la configuración original de IsaacScript, varias reglas estaban deshabilitadas (`"off"`) porque entraban en conflicto con TypeScript-to-Lua o la API de Isaac. 

Al haberlas quitado de `oxlint.config.ts`, **debes tener en cuenta por qué estaban apagadas**:

1. **`@typescript-eslint/no-unsafe-unary-minus` (Estaba en `off`):**
   * *Motivo:* El tipo `int` de IsaacScript a veces daba falsos positivos con el signo negativo (ej. `-1 as int`). En Oxlint no causa problemas a menos que actives una regla que lo prohíba.
2. **`@typescript-eslint/require-array-sort-compare` (Estaba en `off`):**
   * *Motivo:* En JavaScript `[10, 2].sort()` ordena alfabéticamente dando `[10, 2]`. Pero en IsaacScript, TSTL lo compila a la función `table.sort` de Lua, la cual compara números correctamente. Por tanto, no necesitas pasar obligatoriamente `(a, b) => a - b` al ordenar números.
3. **`complete/consistent-enum-values` y `complete/no-number-enums` (Estaban en `off`):**
   * *Motivo:* La API de Isaac **requiere enums numéricos** (IDs de items, entidades, callbacks). Esas reglas intentaban forzar enums de strings, por lo que debían estar apagadas.
4. **`complete/sort-objects` (Estaba en `off`):**
   * *Motivo:* El objeto global `v` (donde se guarda la partida/save data del mod) debe mantener un orden semántico y no alfabético forzado.

---

## 3. Bloque de archivos de configuración (`overrides: ["eslint.config.*"]`)

La configuración original incluía reglas de `import-x` para los propios archivos `eslint.config.*`:
* `import-x/no-extraneous-dependencies`: Permitía importar paquetes de desarrollo en los configs.
* `import-x/no-relative-packages`: Permitía imports relativos entre paquetes en monorepos.

**En Oxlint:** No es necesario replicar esto en tu mod, ya que estas reglas solo aplicaban a la infraestructura de compilación de paquetes de IsaacScript y no al código que se ejecuta en el juego.

---

## 4. Reglas de Estilo y Formateo Omitidas en Oxlint (Delegación a Oxfmt)

En las configuraciones tradicionales basadas en ESLint (`eslint-config-isaacscript`), varias reglas de estilo visual (como el uso o ausencia de punto y coma, espaciado, comillas) estaban integradas en el linter o se apoyaban en plugins como Prettier.

En el ecosistema moderno de Oxc, **Oxlint omite intencionalmente todas las reglas de formateo** por filosofía de diseño, con el objetivo de enfocarse de forma ultrarrápida en la corrección lógica y el análisis estático. Las tareas de estilo se delegan al formateador oficial **Oxfmt**.

Para los proyectos de modding de *The Binding of Isaac* con IsaacScript, la convención estándar es prescindir de puntos y comas (`semi: false`). Esta directriz se define en el archivo de configuración del formateador `oxfmt.config.ts`:

```typescript
import { defineConfig } from "oxfmt"

export default defineConfig({
  semi: false,
})
```

### ¿Por qué no se configuran estas reglas en `oxlint.config.ts`?
* **Separación estricta de responsabilidades:**
  * **Oxlint:** Se encarga exclusivamente de atrapar bugs, desincronizaciones y problemas estructurales en el código.
  * **Oxfmt:** Se encarga de aplicar el diseño visual y estilo (como `semi: false`) de manera instantánea y sin fricción.
* **Cero conflictos:** Al omitir reglas estilísticas en Oxlint, se evitan discrepancias o colisiones entre el linter y el formateador, garantizando un flujo de trabajo óptimo para el mod.

---

## 5. Checklist Rápido para Desarrollar Mods con Oxlint

Antes de compilar y probar tu mod en el juego (`pnpm build` / `isaacscript monitor`), haz esta rápida inspección mental:

- [ ] **Sin `throw`:** ¿Hay algún `throw` en callbacks o funciones del mod? Reemplázalo por `return`.
- [ ] **`DefaultMap` con fábrica:** ¿Todos los `new DefaultMap` con arrays/objetos usan `() => []` o `() => ({})`?
- [ ] **Enums en mayúsculas:** ¿Tus enumeradores siguen el formato `UPPER_CASE` acorde a la API de Isaac?
- [ ] **Interpolación de strings:** ¿Estás convirtiendo objetos complejos a strings sin extraer sus propiedades (salvo `Vector`)?
