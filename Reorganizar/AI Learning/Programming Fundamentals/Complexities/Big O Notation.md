# Big O Notation
Big O Notation is a way to describe the performance or complexity of an algorithm by analyzing how the runtime or space requirement grow as the input size (n) increases.
## Complejidad de Tiempo Constante O(1)
El tiempo de ejecución es constante y no depende del tamaño de la entrada. No importa si estas procesando 10 elementos o 10 millones; el tiempo será el mismo.

**Ejemplos**
- Acceder a un elemento en un array por su índice.
```Typescript
const element = array [5]
```
## Complejidad de Tiempo Lineal
El tiempo de ejecución crece linealmente con el tamaño de la entrada. Si duplicas el número de elementos, el tiempo de ejecución aproximadamente también se duplica.

**Ejemplos**
- Recorrer todos los elementos de un array.
### Diferencia entre la complejidad de tiempo lineal y
La diferencia principal entre una notación O(n) y O(n²) radica en cómo se recorren y procesan los elementos del array.
En la notación O(n²), por cada elemento del array tienes que recorrer nuevamente todo el arreglo para verificar los elementos hasta encontrar el valor.
En la notación
Por lo que mientras en una notación O(n²) recorres los elementos restantes por cada iteración, en la notación O(n²) recorres los elementos ya vistos por cada iteración, por lo que solo recorres el array una sola vez.
## Complejidad de Tiempo

## Ejemplos
### Adding spaces to a String
**Problem**
You are given a 0-indexed string s and a 0-indexed integer array spaces that describes the indices in the original string where spaces will be added. Each space should be inserted before the character at the given index.
**O(m * n) inefficient solution**
```TypeScript
function addSpaces(
  s: string,
  spaces: number[]
): string {
  const sArray = s.split("")
  
  spaces.sort((a, b) => b - a)

  for (const index of spaces) {
    sArray.splice(index, 0, " ")
  }
  
  return sArray.join("")
}
```

Esta solución, aunque resuelve el problema correctamente, tiene un problema grave de eficiencia que hace que la complejidad O(m * n) se acerque a O(n²) en el peor de los casos.
Esto se debe a que `Array.splice` tiene una complejidad lineal O(n) debid\o al movimiento 


Debido al uso de for...of, la función tiene que recorrer todo el array por cada índice del array de `spaces`, lo cuál en casos simples puede no haber problema, al momento de pasar arrays extremadamente largos con una cantidad de índices significativos la función puede tardar más tiempo del necesario.
**O(n log m) efficient solution**