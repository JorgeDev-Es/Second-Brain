# Función `toRaw()` de Composition API de Vue
## Descripción
Devuelve el objeto original, sin procesar, a partir de un proxy creado por Vue.
## Detalles
`toRaw()` puede retornar el objeto original desde proxies creados por `reactive()`, `readonly()`, `shallowReactive()` o `shallowReadonly`. Es una via de escape que puede ser usado para leer temporalmente sin incurrir en el overhead de acceso/seguimiento del proxy o escribir sin provocar cambios.
No es recomendado para mantener una referencia persistente al objeto original. Usarse con precaución.