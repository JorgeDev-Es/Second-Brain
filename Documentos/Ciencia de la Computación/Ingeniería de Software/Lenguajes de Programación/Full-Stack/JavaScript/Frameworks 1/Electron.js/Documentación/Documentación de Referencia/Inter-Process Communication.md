# Inter-Process Comunication
Inter-process communication (IPC) is a key part of building feature-rich desktop applications in Electron. Because the main and renderer processes have different responsibilities in Electron's process model, IPC is the only way to perform many common tasks, such as calling a native API from your UI or triggering changes in your web contents from native menus.
## IPC channels
n Electron, processes communicate by passing messages through developer-defined "channels" with the [[Documentos/Computer Science/Software Engineering/Software Development/Programming Languages/Full-Stack/JavaScript/Frameworks/Electron.js/Reference/APIs/Main Process Modules/ipcMain/ipcMain|ipcMain]] and [[Documentos/Computer Science/Software Engineering/Software Development/Programming Languages/Full-Stack/JavaScript/Frameworks/Electron.js/Reference/APIs/Renderer Process Modules/ipcRenderer/ipcRenderer|ipcRenderer]] modules.
## Sending messages
It's possible to send messages from the main process to the renderer process.
When sending a message, the event name is the `channel`.
To reply to a synchronous message, you need to set `event.returnValue`.
To send an asynchronous message back to the sender, you can use `event.reply(...)`. This helper method will automatically handle messages coming from frames that aren't the main frame (e.g. iframes) whereas `event.sender.send(...)` will always send to the main frame.
## `ipcMain.handle` and `ipcMain.on`
`ipcMain.handle` and `ipcMain.on` are the primary methods for handling inter-process communications.
## ipcMain.on
[[[Documentos/Computer Science/Software Engineering/Software Development/Programming Languages/Full-Stack/JavaScript/Frameworks/Electron.js/Reference/APIs/Main Process Modules/ipcMain/ipcMain|ipcMain.on]]] is used for asynchronous communication where a response isn't immediately expected.

## Resources
https://www.electronjs.org/docs/latest/tutorial/ipc