# Browser Window
It creates a new Browser Window with native properties as set by the `options`.

```typescript
const window = new BrowserWindow(options?: Electron.BrowserWindowConstructorOptions): BrowserWindow
```
## Parametros
### `options` (opcional)
`options` es un parámetro opcional con un tipo de dato `Electron.BrowserWindowConstructorOptions`, la cual define las opciones configurables al crear una nueva ventana del navegador, como las herramientas del desarrollador, si se permite la integracion de Node.js, etc.
```
options?: Electron.BrowserWindowConstructorOptions
```

## Returns
Retorna una instancia de la clase BrowserWindow.
## Resources
https://www.electronjs.org/docs/latest/api/browser-window#class-browserwindow-extends-basewindow