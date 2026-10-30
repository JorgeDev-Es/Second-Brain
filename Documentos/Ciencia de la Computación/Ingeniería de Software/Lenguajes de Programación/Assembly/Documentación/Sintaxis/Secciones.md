# Secciones
En un programa de ensamblador, un programa se divide en tres secciones: La sección **data**, la sección **bss** y la sección **text**.
## Sección **Data**
La sección **data** es usada para declarar datos iniciales o constantes. Estos datos no cambian durante el tiempo de ejecución. Puedes declarar varios valores constantes, nombres de archivos, tamaños de buffer, etc., en esta sección.
La sintaxis para declarar la sección **data** es:
```Assembly
section.data
```
## Sección **bss**
La sección **bss** es usada para declarar variables. La sintaxis para declarar la sección **bss** es:
```Assembly
section.bss
```
## Sección **text**
La sección **text** es usada para almacenar el código actual. Esta sección debe empezar con la declaración `global _start`, que le dice al kernel donde empieza la ejecución del programa.

La sintaxis para declarar la sección **text** es:
```Assembly
section.text
global .start
_start:
```
## Referencias
https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm