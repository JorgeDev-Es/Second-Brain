# Objeto global `app` del Módulo del Proceso Principal de Electron
## Descripción
En Electron.js, el objeto `app` es el módulo fundamental del proceso principal encargado de controlar el ciclo de vida completo de la aplicación. Actúa como el orquestador central que emite eventos críticos, como `ready`, `window-all-closed`, `will-quit`, etc.
Además de gestinar el estado operativo, proporciona una interfaz robusta para configurar comportamientos del sistema, como establecer el nombre de la aplicación, gestionar el inicio automático, definir protocolos personalizados y acceder a rutas de directorios específicos del sistema operativo, etc.
## Responsabilidades
### Control del ciclo de vida
Maneja la inicialización, ejecución y el cierre ordenado del software.
### Eventos del sistema
Escucha sucesos como el enfoque de la aplicación, cambios en la red o solicitudes de apertura de archivos.
### Configuración
Permite ajustar parámetros de hardware (GPU), certificados de seguridad y políticas de sandbox.
### Instancia única
Facilita la lógica para asegurar que solo una instancia de la aplicación se esté ejecutando a la vez.
## Métodos
## Propiedades
## Eventos

## Casos de uso
### Cerrar la app
Cerrar la aplicación cuando todas las ventanas son cerradas, excepto en MacOS. En MacOS, es normal para las aplicaciones y su barra de menú mantenerse activas hasta que el usuario las cierra explícitamente con `Cmd + Q`.
```JavaScript
app.on('window-all-closed', () => {  
    if (process.platform !== 'darwin') {  
        app.quit()  
        win = null  
    }  
})
```
### Activar la aplicación en OS X
En OS X, es normal recrear una ventana en la aplicación cuándo el ícono del dock es cliqueado y no hay más ventanas abiertas.
```JavaScript
app.on('activate', () => {  
    // On OS X it's common to re-create a window in the app when the  
    // dock icon is clicked and there are no other windows open.    if (BrowserWindow.getAllWindows().length === 0) {  
        createWindow()  
    }  
})
```
## Referencias
https://www.electronjs.org/docs/latest/api/app