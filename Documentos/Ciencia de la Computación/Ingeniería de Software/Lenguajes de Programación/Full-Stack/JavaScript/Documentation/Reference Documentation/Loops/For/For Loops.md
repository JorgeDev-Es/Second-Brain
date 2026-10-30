## `for()` y `for...of`
El bucle `for` tradicional es versátil y se utiliza para iterar sobre índices.
```TypeScript
for (let i = 0; i < array.length; i++) {
	console.log(i)
con
}
```
## `for...of` y `for...in`
## Índices independientes o índices auxiliares
Crear índices independientes en lugar de modificar `i` directamente es una práctica común en programación cuando se presentan escenarios donde es necesario mantener el control sobre múltiples elementos iterados simultáneamnete o cuando modificar `i` podría causar problemas de lógica o errores difíciles de depurar.
**Iteración simultánea de múltiples estructuras**
Si necesitas recorrer dos estructuras de datos (como un array y otro array relacionado), un índice independiente permite gestionar ambas iteraciones sin afectar el flujo principal.
```JavaScript
const arr1 = [1, 2, 3]; const arr2 = [10, 20, 30]; // Usando índices independientes
let j = 0;
for (let i = 0; i < arr1.length; i++) { 
	console.log(arr1[i], arr2[j]);
	j++;
	// Avanzamos en el segundo array
}
```
Si modificaras **`i`** para manejar ambas estructuras, el bucle podría volverse confuso o provocar inconsistencias.
**Iteraciones condicionales dentro de un bucle**
Cuando tienes lógica condicional que depende de un segundo índice o contador. Alterar **`i`** directamente dentro del bucle principal puede provocar saltos no deseados, mientras que un índice independiente asegura un control más claro.
```JavaScript
const str = "abcdef";
const indices = [1, 3, 5];
let j = 0;
let result = '';

for (let i = 0; i < str.length; i++) {
  if (j < indices.length && i === indices[j]) {
    result += '-';
    j++; // Solo avanzamos este índice cuando se cumple la condición
  }
  result += str[i];
}
console.log(result); // a-bc-de-f

```
Alterar **`i`** directamente en este caso podría causar errores de salto en la cadena original.
**Procesos que requieren mantener el índice original**
En algunas situaciones, necesitas iterar una estructura pero también usar el valor original de **`i`** en algún cálculo o lógica más adelante. Crear un índice independiente te permite manipularlo sin perder el valor original.
**Evitar problemas de legibilidad y depuración**
Modificar **`i`** directamente en bucles largos puede hacer que el flujo lógico sea difícil de seguir y más propenso a errores. Usar un índice independiente mejora la **legibilidad** y hace que el código sea más intuitivo.
```JavaScript
for (let i = 0; i < array.length; i++) {
  if (condicion) {
    i--; // Modificamos i
  }
  // Es difícil saber cómo se comportará el bucle
}

```
```JavaScript
let auxIndex = 0;
for (let i = 0; i < array.length; i++) {
  if (condicion) {
    auxIndex++;
  }
}

```

**Cuando hay una relación directa entre elementos**
Si trabajas con una estructura de datos secundaria que está relacionada con el bucle principal (como un array de índices o posiciones específicas), un índice independiente asegura que avances en la estructura secundaria en paralelo con la iteración.
```JavaScript
const values = [5, 10, 15, 20];
const skip = [1, 3];
let skipIndex = 0;

for (let i = 0; i < values.length; i++) {
  if (skipIndex < skip.length && i === skip[skipIndex]) {
    skipIndex++; // Solo avanzamos este índice cuando coincide
    continue;    // Saltamos este elemento
  }
  console.log(values[i]);
}

```
**Evitar efectos secundarios inesperados**
Cuando el bucle se encuentra en un entorno complejo, como anidaciones o funciones de callback, modificar **`i`** puede causar efectos secundarios inesperados. Usar un índice independiente reduce este riesgo.

Crear índices independientes suele hacer que el código sea más **fácil de entender**, **más confiable** y **menos propenso a errores**. Aunque puede parecer redundante en algunos casos, el beneficio de claridad y control a menudo supera cualquier inconveniente.