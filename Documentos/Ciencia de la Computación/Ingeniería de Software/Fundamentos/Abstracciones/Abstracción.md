# Abstracción
Una abstracción es una manera de **ocultar detalles de implementación y ofrecer una interfaz más simple o más expresiva** para resolver un problema.

- Una **función** que encapsula una secuencia de instrucciones.
- Una **clase** que modela un concepto del mundo real.
- Una **plantilla genérica** que evita escribir código duplicado para distintos tipos.
- Una **biblioteca estándar (STL)** que abstrae estructuras de datos y algoritmos comunes.

La abstracción busca ocultar la complejidad para trabajar de manera más **eficiente**.

Generalmente, la abstracción tiene un coste de rendimiento, sea grande o sea pequeño, a beneficio de simplificar el desarrollo y el coste mental.
En lenguajes de alto nivel (Python, Java, etc.), esas abstracciones suelen implicar sobrecostes inevitables en memoria o tiempo de ejecución.
## ¿Para qué se usa una abstracción?
Sin abstracciones, estás enfocado en el "cómo", con abstracciones, te enfocas en el "qué".
## Ventajas y desventajas
Si estas usando C, no estas usando Assembly y sus ventajas. Si estas usando JavaScript, no estas usando C y sus ventajas. Si estas usando Vue, no estas usando JavaScript Vanilla y sus ventajas.
### Ventajas
- Reduce la carga cognitiva
- Reutilización
- Mayor seguridad
- Mantenibilidad
- Escalabilidad
### Desventajas
- Overhead de rendimiento
- Consumo de recursos
- Latencia

En C++ la filosofía es diferente: **si la abstracción no es usada, no cuesta nada; y si es usada, cuesta lo mismo que el equivalente en bajo nivel.**
## Embellecimiento
## Código generico
## ¿Cómo saber que abstracción elegir?
No hay tecnologías sin desventajas.
Enfocate en el objetivo y no en la herramienta.
"Necesito una aplicación web básica", entonces cualquier framework web que elijas es la correcta.
"Necesito una aplicación nativa, con un alto rendimiento y control directo del hardware", entonces C o Assembly son las herramientas correctas.