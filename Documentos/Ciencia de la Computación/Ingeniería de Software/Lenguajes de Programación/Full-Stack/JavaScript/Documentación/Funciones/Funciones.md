# Funciones en JavaScript
## Funciones regulares vs funciones flecha
### Contexto
En JavaScript, las funciones regulares y las funciones flechas funcionan con un contexto diferente.
En funciones como `window.requestAnimationFrame`, `setTimeout`, etc., el entorno de ejecución invoca el callback directamente (sin contexto de objeto), por lo que `this` apunta a `window` (o `undefined` en modo estricto) independientemente de la clase origen.
```JavaScript
class Person {
	age = 23
	
	showAge() {
		console.log(this.age)
	}
}
```
`Person.showAge()` es una función regular.
Al ejecutar `showAge()` en el ámbito global se devuelve el valor de la propiedad:
```JavaScript
const person = new Person()
person.showAge() // Output> 23
```
Pero al ejecutarlo como un callback en la función `setTimeout()`, la función devuelve `undefined`:
```JavaScript
setTimeout(person.showAge, 100) // Output> undefined
```
Si se imprime `this`,  se devuelve `window`.
Pero al convertir `Person.showAge` a una función flecha o ejecutarlo dentro de una, el problema se resuelve:
```JavaScript
// Conversión de funcíon regular a función flecha
class Person {
	age = 23
	
	showAge = () => {
		console.log(this.age)
	}
}

const person = new Person();

setTimeout(person.showAge, 100) // Output> 23
```

```JavaScript
// Ejecución dentro de un arrow function
setTimeout(() => { person.showAge() }, 100) // Output> 23
```


## Funciones vs Callbacks
```TypeScript
class CanvasRenderer {
  #canvas: HTMLCanvasElement
  #ctx: CanvasRenderingContext2D

  constructor(
    canvas: HTMLCanvasElement,
    ctx: CanvasRenderingContext2D
  ) {
    this.#ctx = ctx
    this.#canvas = canvas
  }

  loop() {
    console.log(this.#ctx) 
  }

  run() {
    window.requestAnimationFrame(this.loop)
  }
}
```
Al ejecutar `window.requestAnimationFrame(this.loop)`, recibimos un error debido a que `this.#ctx` es `null`.
```JavaScript
loop() {
    console.log(this.#ctx) // ❌ Error>  Uncaught TypeError: Cannot read properties of undefined (reading '#ctx')
  }
```
Error que se soluciona al cambiar `loop()` a callback:
```JavaScript
loop = () => {
    console.log(this.#ctx) // ✅
  }
```

```JavaScript

```