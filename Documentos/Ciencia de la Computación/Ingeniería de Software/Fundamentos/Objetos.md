# Objetos en Programación
## ¿Qué es un objeto en programación?
Un objeto es una entidad que encapsula datos (propiedades o atributos) y comportamientos (métodos o funciones, representando entidades del mundo real o conceptos abstractos.
## Conceptos abstractos
Los objetos que representan conceptos abstractos no representan "cosas", sino responsabilidades.
## ¿Una clase es un objeto?
No, una clase es una manera de crear objetos con una estructura y comportamiento predefinido.
```JavaScript
const book = {
	title: "Atomic Habits",
	author: "James Clear",
	editorial: "Avery",
	date: {
		day: 16,
		month: 10,
		year: 2018
	},
	open() {},
	close() {},
	read() {}
}
```

```JavaScript
const Person = {
	firstName: "James",
	secondName: "Clear",
	age: 32,
	genre: "male",
	eat() {},
	sleep() {},
	think() {},
	work() {}
}
```
## ¿Para que sirven los objetos?
