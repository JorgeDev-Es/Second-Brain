# Windows Application Entry Point
```C++
int WINAPI wWinMain(
	HINSTANCE hInstance,
	HINSTANCE hPrevInstance,
	PWSTR pCmdLine,
	int nCmdShow
)
```

## Parameters
`hInstance` es el *handle* a una instancia o el *handle* a un módulo.
El sistema operativo usa este valor para identificar
`hPrevInstance` es obsoleto. Se usaba en Windows 16-bit, pero ahora es siempre cero.
`pCmdLine` contiene los argumentos de línea de comandos cómo un string Unicode.
`nCmdShow` es un flag que indica si la ventana de la aplicación principal es minimizada, maximizada, o mostrada normalmente.
## Referencias
https://learn.microsoft.com/en-us/windows/win32/learnwin32/winmain--the-application-entry-point