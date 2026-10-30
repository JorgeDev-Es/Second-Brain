# Método `GetContext()` de la Web API `HTMLCanvasElement`
## Descripción
El método `HTMLCanvasElement.getContext()` retorna un contexto de dibujo en el lienzo, o `null` si el identificador del contexto no esta soportado.
## Sintaxis
```TS
canvas.getContext(contextType, contextAttributes)
```
## Ejemplos
### Ejemplo básico
```TS
const canvas = document.getElementByID("canvas")
const ctx = canvas.getContext("2d")
```
## Referencias
https://developer.mozilla.org/es/docs/Web/API/HTMLCanvasElement/getContext