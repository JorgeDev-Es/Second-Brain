# Proceso de Construcción de JavaScript
JavaScript es un lenguaje interpretado, lo que significa que no es necesario un proceso de compilación/construcción para ser ejecutado en un entorno de ejecución. Sin embargo, en el desarrollo moderno, se utiliza un proceso de construcción para transformar un código fuente, sea en JavaScript, TypeScript, JSX, TSX, etc., para generar un código final optimizado, compatible, mantenible, legible, etcétera.

La razón por la que un proceso de construcción puede variar.
Solo usar TypeScript ya requiere un proceso de construcción.
## Entorno de ejecución
En un entorno de ejecución, se ejecutan los archivos que el entorno de ejecución entiende de manera nativa, esto no incluye archivos `.jsx`, `.vue`, `.ts` (aunque existen entornos de ejecución que si lo entienden, como Bun o Deno), etc., sino que es una herramienta de construcción externa quien los entiende y los traspila para que el entorno de ejecución pueda ejecutarlos
## Herramientas de construcción externas
Las herramientas de construcción externas convierten código son la que se encargan de traspilar, minificar, agrupar, empaquetar, etc., código para que un entorno de ejecución pueda ejecutar.