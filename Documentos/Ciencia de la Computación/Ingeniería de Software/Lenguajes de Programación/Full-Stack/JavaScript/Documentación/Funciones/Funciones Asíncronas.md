# Funciones Asíncronas
## ¿Qué son las funciones asíncronas?
Las funciones asíncronas **siempre retornan un `Promise`**. Si el valor de retorno de una función asíncrona no es explícitamente una promesa, sera envuelta en una promesa. Por ejemplo:
```JavaScript
async function foo() {
	return 1
}
```
realmente retorna:
```JavaScript
function foo() {
	return Promise.resolve(1)
}
```
## Referencias
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function