# Bucles
## Bucle range-based

```
numbers: List<integer> = [3, 4, 1, 2, 4]

for num in numbers:
	print(number)
```
### C++
un bucle range-based
```C++
for (int number : numbers) {
	cout << num << endl;
}
```

## Bucle con índice
```
numbers: List<integer> = [3, 4, 1, 2, 4]

for i in range(numbers.size):
	print(numbers[i] + ", ") // Output> 3, 4, 1, 2, 4
```

### C++
```C++
for (int i = 0; i < numbers.size(); i++) {
	cout << numbers[i] << ", ";
}
```

```
numbers: List<integer> = [3, 4, 1, 2, 4]

for i in range(start: 1, stop: numbers.size)
	print(numbers[i] + ", ") // Output> 4, 1, 2, 4

for i in range(1, numbers.size)
	print(numbers[i] + ", ") // Output> 4, 1, 2, 4
```

```C++
for (int i = 1; i < numbers.size()) {
	cout << numbers[i] << ", ";
}
```

```
numbers: List<integer> = [3, 4, 1, 2, 4]

for i in range(end: numbers.size, step: 2)
	print(numbers[i] + ", ") // Output> 3, 1, 4
```