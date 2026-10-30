# Maximum Problem
## ¿Cuál es el problema?
Dado un conjunto o lista de números, encontrar el elemento de mayor valor.
## Código
### Pseudocódigo
```
function maximum(numbers: List<integer>): integer
	if nums.empty return 0
	if nums.size == 1 return numbers[0]
	
	max: integer = numbers[0]
	
	for i in range(1, numbers.size)
		actual: integer = numbers[i]
		
		if actual > max
			max = actual
```
## Ejemplos
### Ejemplo 1
Entrada: `[8, 3, 2, 14, 1]`
Salida: `14`
