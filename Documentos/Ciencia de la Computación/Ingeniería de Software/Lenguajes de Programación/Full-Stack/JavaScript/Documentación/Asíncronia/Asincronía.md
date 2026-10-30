# Asincronía en JavaScript
La programación asíncrona es una técnica que permite a un programa ejecutar tareas potencialmente pesadas y seguir siendo responsivo a otros eventos mientras esas tareas se ejecutan, en lugar de esperar que esas tareas terminen.

Muchas APIs proporcionadas por los entornos de ejecución pueden potencialmente tardar un largo tiempo, por lo que, son asíncronas. Por ejemplo:
- Realizar solicitudes HTTP.
- Acceder a la cámara o micrófono del usuario.
- Solicitar al usuario seleccionar archivos.
## ¿Todas las funciones asíncronas necesitar un `await`?
No
## Asincronía versión Callback vs Asincronía versión Promise
Las promises tienen un ligero overhead de memoria inicial debido a la creación del objeto `Promise` y gestionar el estado de la microtarea. Sin embargo, 
- Seguridad
- Mantenibilidad
- Depuración

## Referencias
https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Async_JS/Introducing