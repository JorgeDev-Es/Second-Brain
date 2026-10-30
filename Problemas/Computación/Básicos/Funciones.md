# Funciones
## Hola mundo
### ¿Cuál es el problema?
Declarar una función llamada `greet` que reciba como parámetro un nombre y muestre el mensaje `"Hello, <nombre>`.
#### Ejemplo
Entrada: `Chistopher`
Salida: `Hello, Christopher`
## Máximo de dos números
### ¿Cuál es el problema?
Declara una función llamada `max` que reciba como parámetros dos enteros y devuelva el número mayor
### Ejemplos
#### Ejemplo 1
Entrada: `3` y `5`
Salida: `5`
#### Ejemplo 2
Entrada: `-6` y `5`
Salida: `5`
## Máximo de dos números sin signo (Valido para algunos lenguajes)
### ¿Cuál es el problema?
Declarar una función llamada `max` que reciba como parámetros dos números enteros sin signo y devuelva el número mayor
## Mínimo y máximo de dos números
### ¿Cuál es el problema?
Declarar una función llamada `minMax` que reciba como parámetros dos números enteros y retorne un objeto que devuelva cuál es el número mayor o menor `{min: number, max: number}`
### Ejemplos
Entrada: `5` y `10`
Salida: `{min: 5, max: 10}`
### Implementaciones
#### C++
```C++
class MinMax {  
public:  
    int min;  
    int max;  
};  
  
MinMax minMax(const int first, const int second) {  
    MinMax min_max{};  
  
    min_max.min = first > second ? second : first;  
    min_max.max = first > second ? first : second;  
  
    return min_max;  
}  
  
int main() {  
    MinMax myMinMax = minMax(rand(), rand());  
  
    print("min: {}\nmax: {}", myMinMax.min, myMinMax.max);  
  
    return 0;  
}
```