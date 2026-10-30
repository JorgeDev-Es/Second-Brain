# Arquitectura Hexagonal
## ¿Qué es la Arquitectura Hexagonal?
La arquitectura hexagonal, también conocida como arquitectura de puertos y adaptadores, es una arquitectura de software.
Se basa en la idea de aislar la lógica central de las preocupaciones externas, por medio de la separación de la aplicación en componentes débilmente aislados.
![[Archivos Adjuntos/Pasted image 20260113185838.png]]
## Elementos de la Arquitectura Hexagonal
### Dominio
Dominio
El dominio puede encontrarse con nombres como `core` (para aplicaciones no empresariales) o `lib` (Para librerías o utilidades puras).
### Casos de uso
Los casos de uso pueden encontrarse con el nombre de `application`.
### Infrastructure
### Entidades
## Invertir las dependencias
Generalmente, la clave para implementar la Arquitectura Hexagonal es invertir las dependencias.
## ¿Dónde se puede usar el patrón hexagonal?
La Arquitectura Hexagonal es un patrón agnóstico. Se puede implementar en prácticamente cualquier lenguaje que soporte [[Documentos/Ciencia de la Computación/Ingeniería de Software/Fundamentos/Interfaces|interfaces]], [[Documentos/Ciencia de la Computación/Ingeniería de Software/Fundamentos/Datos/Tipos de Datos/Tipos Abstractos|tipos abstractos]] o [[Documentos/Ciencia de la Computación/Ingeniería de Software/Fundamentos/Polimorfismo|polimorfismo]].
## Casos de uso
La arquitectura hexagonal destaca cuando se necesita integrar múltiples tecnologías sin que estas contaminen tu lógica central.
Los casos de uso típicos suelen ser aplicaciones web escalables, microservicios, sistemas bancarios y empresariales, aplicaciones de escritorio, servicios en la nube, ciencia de datos, APIs, sistemas de alta concurrencia, herramientas de infraestructura, etc.
## ¿Cuál es su límite y su punto de sobreingeniería?
### Scripts sencillos
### Prototipados rápidos
### Aplicaciones básicas
## Implementación
## Separación
En la arquitectura hexagonal, la separación no es solo conceptual o lógica, sino que se manifiesta físicamente en la estructura de carpetas del proyecto.
## Ejemplos
### Ejemplo básico
Se define un puerto (la interfaz) definiendo lo que se quiere hacer, no como.
```TypeScript
// domain/ports/StoragePort.js
interface StoragePort {
save: (filename: string, content: string) => Promise<void>
}
```
## Referencias
https://thepowertech.es/blog/que-es-arquitectura-hexagonal-en-programacion