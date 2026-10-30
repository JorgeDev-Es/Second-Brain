# JavaScript Modules
Un **módulo de JavaScript** es cualquier archivo que:
- Usa la sintaxis `import` o `export`
- O está explícitamente tratado como módulo por el entorno (por ejemplo, en HTML con

## Características clave de los módulos
- **Scope propio**: Las variables definidas en un módulo no contaminan el scope global.
- **Importación/exportación**: Puedes compartir funciones, objetos, clases, etc., entre archivos usando `export` y `import`.
- **Modo estricto**: Los módulos siempre se ejecutan en `"use strict"` automáticamente.
- **Evaluación diferida**: Se cargan de forma asíncrona en navegadores modernos.
- **`import.meta`**: Solo está disponible dentro de módulos, y proporciona metainformación sobre el módulo actual (como su URL).