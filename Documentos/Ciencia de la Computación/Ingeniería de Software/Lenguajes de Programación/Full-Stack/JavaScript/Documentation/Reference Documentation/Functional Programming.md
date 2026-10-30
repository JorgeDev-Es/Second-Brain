# Functional Programming in JavaScript

## Why functional programming?
- Improved code clarity. Pure functions and immutability make code easier to understand and reason about.
- Easier testing. Pure functions are simple to test because they have no side effects.
- Concurrency. Immutable data makes it easier to write concurrent code, as you don't have to worry about race conditions.
- Maintainability. Functional code tends to be more modular and easier to mantain.
### Pure functions
```JavaScript
// Pure function
function add(a, b) {
	return a + b
}

// Impure function (has side effect)
let total = 0
function addToTotal(value) {
	total += value
	return total
}
```
### Immutability
Data should not be modified after it's created. Instead, you create new data with the desired changes.
```JavaScript
// Immutable update using spread syntax
const originalArray = [1, 2, 3]
const newArray = [...originalArray, 4] // Creates a new array

//Mutable update
originalArray.push(4)
```
### First-class functions
Functions can be treated like any other variable. You can pass them as arguments to other functions, return them from functions, and assign them to variables.
```JavaScript
function multiplyBy(factor) {
	return function(number) {
		return number * factor
	}
}

const double = multiplyBy(2)
console.log(double(5)) // $> 10
```
### Higher-order functions
Functions that operate on other functions, either by taking them as arguments or returning them. Common examples include `map`, `filter`, and `reduce`.
```JavaScript
const numbers = [1, 2, 3, 4, 5]

// Using map to transform each element.
const doubledNumbers = number.map(number => number * 2)

// Using filter to select elements based on a condition.
const evenNumbers = numbers.filter(number => number % 2 === 0)

// Using reduce to combine all elements into one value.
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0)
```