# Es Palíndromo
## Problema
Dado un string, verificar si es palindromo
## Posibles soluciones
### Dividir el array
Dividir el array en dos partes dependiendo si es par o impar a la mitad, y comparar la primera mitad con la segunda mitad en reversa.

**Problemas**:
Necesitas determinar si es par o impar.
Necesitas hacer reverse a un string.
Uso de memoria innecesario al crear nuevos arrays (tanto para hacer reverse como para verificar si son iguales).
```TypeScript
function isEven(num: number) {
  return num % 2 === 0;
}

function reverseString(str: string): string {
  const output: string[] = [];
  for (const letter of str) {
    output.unshift(letter);
  }

  return output.join("");
}

function isPalindrome(str: string): boolean {
  const start = 0;
  const end = str.length;
  const middle = isEven(str.length) ? str.length / 2 : str.length / 2 + 1;

  console.log(reverseString(str.slice(start, middle)));
  console.log(str.slice(middle - 1, end));

  return reverseString(str.slice(start, middle)) === str.slice(middle - 1, end);
}
```
### Verificar start y end
Asignar `start` y `end`, comparar el carácter de inicio con el carácter del final, y mientras no se encuentre una comparación invalida, sumar al start y restar al end hasta que start sea mayor a end (se han verificado todos los caracteres)
```TypeScript
function isPalindrome(str: string): boolean {
  let start = 0;
  let end = str.length - 1;

  while (start < end) {
    if (str[start] !== str[end]) {
      return false;
    }
    start++;
    end--;
  }

  return true;
}

```