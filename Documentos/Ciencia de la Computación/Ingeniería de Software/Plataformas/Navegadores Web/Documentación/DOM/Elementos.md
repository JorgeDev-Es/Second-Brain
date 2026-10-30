# Elementos del DOM
## ¿Qué son los elementos del DOM?
Un elemento del DOM es la 

## Operaciones de los elementos DOM
### Seleccionar elementos
`getElementById()` selecciona un elemento por su ID.
`getElementsByName()` selecciona múltiples elementos por su nombre.
`getElementsByTagName()` selecciona múltiples elementos por su nombre de etiqueta.
`getElementsByClassName()` selecciona múltiples elementos por uno o más nombres de clases.
`querySelector()` selecciona elementos por su selector CSS.

`querySelector` vs `getElementBy...`
### Recorrer elementos
### Manipular elementos
`createElement()`
`appendChild()`
`textContent`
`innerHTML`
### Trabajando con atributos
### Manipulando los estilos de los elementos
### Trabajando con eventos
## Comportamiento interno de los elementos DOM
Un elemento HTML puede existir pero no mostrarse.

```JS
const button = document.createElement("button")

button.addEventListener("click", () => console.log("You clicked the button"))

button.click()
```
## Referencias
https://www.javascripttutorial.net/javascript-dom/