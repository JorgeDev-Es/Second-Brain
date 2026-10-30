# Función `unref()` de Composition API de Vue.js
## Descripción
La función `unref()` devuelve el valor interno si el argumento es un `ref`, de otra manera retorna el argumento en si mismo.
Es una función syntactic sugar para `val = isRef(val) ? val.value : val`.
## Ejemplos
```TypeScript
function useRef(x: number | Ref<number>) {
	const unwrapped = unref(x)
}
```
## Referencias
https://vuejs.org/api/reactivity-utilities.html#unref