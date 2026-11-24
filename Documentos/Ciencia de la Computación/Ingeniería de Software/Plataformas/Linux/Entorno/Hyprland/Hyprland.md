# Hyprland
## Qué es Hyprland?
Hyprland es un compositor de Wayland dinámico en mosaico escrito en C++.
Toma las superficies gráficas que le entregan las aplicaciones vía Wayland, las organiza automáticamente en pantalla, les aplica efectos visuales y gestiona los atajos de teclado.

Hyprland permite configurar reglas de ventanas, animaciones y comportamientos en un archivo de texto plano que se recarga instantáneamente sin cerrar tus aplicaciones.

Utiliza OpenGL ES directamente sobre KMS/DRM (Kernel Mode Setting/Direct Rendering Manager).

## Características
### Hot-Reload
Se configura mediante archivos de texto plano analizados por su propio parser (`hyprlang`). Cualquier cambio en el archivo dispara una recarga instantánea de estado en memoria sin reiniciar la sesión gráfica ni cerrar procesos hijos.
### Sistemas de plugins en C++
Ofrece una API nativa que permite compilar bibliotecas compartidas (`.so`) cargables en tiempo de ejecución (`hyprpm`), exponiendo hooks directos a las funciones internas del compositor para modificar el comportamiento del renderizador, crear nuevos layouts o añadir decoraciones de ventana personalizadas.
## Ecosistema
Hyprland funciona como un ecosistema modular compuesto por el binario del compositor, utilidades CLI de control
### `Hyprland`
### `hyprctl`
### Hyprland Plugin Manager(`hyprpm`)
### Librerías compartidas cargadas en memoria
### Procesos de integración y compatibilidad