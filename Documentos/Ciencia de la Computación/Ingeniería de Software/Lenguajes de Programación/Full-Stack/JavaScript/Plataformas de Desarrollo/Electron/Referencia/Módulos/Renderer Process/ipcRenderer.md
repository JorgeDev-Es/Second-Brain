# Módulo `ipcRenderer` de Electron.js
EL módulo `ipcRenderer` es un `EventEmitter`.
## Métodos
### `invoke()`
Envía un mensaje al proceso principal mediante un `channel` y espera un resultado de manera asíncrona.

El proceso principal debería escuchar el `channel` con `ipcMain.handle()`.

Envía y recibe un único resultado asíncrono.
### `on(channel, listener)`
#### Descripción
El método `ipcRenderer.on()` escucha un `channel`, cuando un nuevo mensaje llega, se ejecutara la función `listener(event, args...)`.
Escucha múltiples mensajes de manera asíncrona.
#### Parámetros
-  `channel`
-  `listener(event, ...args)`. Función a ejecutar
	- `event`
	- `...args`

### `send()`
Envía un mensaje asíncrono al proceso principal mediante un `canal`.

## Referencias
https://www.electronjs.org/docs/latest/api/ipc-renderer