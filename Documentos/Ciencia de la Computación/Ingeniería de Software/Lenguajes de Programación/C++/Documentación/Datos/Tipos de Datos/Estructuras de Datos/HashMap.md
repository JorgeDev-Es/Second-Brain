# Estructura de Datos `HashMap` en C++
La implementación de Hash map en la librería estándar de C++ es [[Documentos/Ciencia de la Computación/Ingeniería de Software/Lenguajes de Programación/C++/Reference/Standard Library/unordered_map/unordered_map|unordered_map]].

## Características
## Ventajas y desventajas de Hash Map
### Ventajas
#### Velocidad
Acceso, inserción y eliminación más rápidos.
### Desventajas
### Orden de elementos no garantizado
`std::unordered_map` no garantiza el orden de las claves, por lo que el orden de iteración es desconocido.

Sacrifica el orden de los elementos para lograr una velocidad O(1), ya que elementos ordenados por clave tienen una velocidad O(log n).

```C++
#include <unordered_map>
```

## Operaciones
### Inserción
#### `unordered_map.insert({key, value})`

## Recursos
### Referencias
https://cppbyexample.com/hash_map.html