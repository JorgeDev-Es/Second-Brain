# Framework Vue
## Reactividad
Al enviar datos entre procesos de Vue cumpliendo con la serialización de objetos, es necesario usar ciertas funciones.

Al enviar valores creados con `ref()`, es necesario usar `toValue()` o `unRef()`.
Al enviar valores creados con `reactive()`
Usar `toRaw()` y `cloneDeep`