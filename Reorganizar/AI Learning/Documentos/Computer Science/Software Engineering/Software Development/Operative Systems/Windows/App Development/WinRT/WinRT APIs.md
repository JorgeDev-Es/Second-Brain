- **Definición básica**:
    
    - **WinRT (Windows Runtime)** es un entorno de ejecución y un conjunto de APIs modernas introducidas con Windows 8.
        
    - Proporciona una plataforma orientada a objetos, basada en componentes, diseñada para aplicaciones universales (_UWP_) y ahora usada también en **Windows App SDK**.
        
- **Características principales**:
    
    - **Lenguaje-agnóstica**: las APIs de WinRT pueden ser usadas desde C++, C#, VB.NET, y JavaScript, gracias a un sistema de _metadata_ común (ECMA-335).
        
    - **Componentes COM modernos**: se basa en COM (Component Object Model), pero con sintaxis y proyección más amigable.
        
    - **Consistencia en namespaces**: organiza APIs en espacios de nombres tipo `Windows.*` (ej. `Windows.UI.Composition`, `Windows.Devices.Geolocation`).
        
- **Modelo de programación**:
    
    - **Objetos de Windows Runtime**: exponen métodos, propiedades y eventos como clases normales en cada lenguaje soportado.
        
    - **Async-first**: muchas operaciones (I/O, red, archivos, UI) se exponen de forma asíncrona mediante _async/await_.
        
    - **Proyecciones de lenguaje**: cada lenguaje accede a WinRT como si fuera código nativo de ese entorno.
        
- **Ejemplos de APIs WinRT**:
    
    - **Windows.UI.Composition** → motor de composición visual (animaciones, efectos).
        
    - **Windows.Devices.Sensors** → acceso a sensores como acelerómetro o giroscopio.
        
    - **Windows.Storage** → manejo de archivos y carpetas con permisos seguros.
        
    - **Windows.Media** → reproducción de audio/video, captura de cámara.
        
- **Relación con otras plataformas**:
    
    - **UWP**: usaba WinRT como base principal.
        
    - **WinUI 3 / Windows App SDK**: reutiliza muchas APIs WinRT, pero en un modelo de empaquetado más flexible (Win32 + modernas).
        
    - **Interoperabilidad**: WinRT puede ser consumido desde aplicaciones de escritorio tradicionales (Win32/.NET) usando _projections_.
        
- **Ventajas de WinRT**:
    
    - Permite acceso unificado y seguro a funcionalidades modernas del sistema.
        
    - Facilita desarrollo multiplataforma dentro del ecosistema Windows.
        
    - Reduce la complejidad de usar directamente COM o Win32 nativo.