# User Interfaces in Programming Fundamentals
Las interfaces de usuario son los medios mediante los cuales las personas interactúan con los programas. En programación, suelen dividirse en dos grandes categorías:
1. Command Line Interface (CLI).
2. Graphic User Interface (GUI)

Los lenguajes de programación no suelen incluir herramientas gráficas integradas, ya que las GUI dependen de interacciones específicas con el sistema operativo y sus APIs gráficas.
Las GUI no solo se ven diferentes según el contexto, sino que también funcionan de manera diferente debido a cómo están diseñadas y las tecnologías subyacentes que la soportan.
Por ejemplo, en los videojuegos los botones generalmente utilizan zonas de detección dentro del juego para registrar si el cursor o el dedo del jugador está sobre el botón, mientras que en el sistema operativo son gestionados por la API gráficas y se manejan a través de funciones asociadas a los botones.
Además, existen alternativas intermedias que ofrecen un equilibrio entre personalización y facilidad de uso, sin las limitaciones de los sistemas operativos ni la complejidad extrema de un motor gráfico, como las herramientas de UI de un navegador o las herraminetas de un framework multiplataforma como QT.

QT ofrece un motor gráfico basado en OpenGL/Vulkan que se encargan de mostrar la UI, sobrepasando las limitaciones de desarrollas interfaces con las APIs gráficas del sistema operativo.

Existen múltiples opciones, donde puedes desarrollar una UI consistente al sistema operativo donde el usuario del mismo se sienta familiar o una UI con diseño personalizable donde el usuario sienta que esta utilizando una aplicación propia de lo que esta utilizando.
Esto ya que las limitaciones de las APIs gráficas del sistema operativo no permitirían crear UI de programas como VS Code, Steam, etcétera; sin parecer que son parte de Windows, de Linux o de Android.

Hay que aprender cuando una UI deba ser consistente con los estilos y patrones nativos del sistema operativo, por ejemplo, en aplicaciones que funcionen solo con ese sistema operativo y que ofrezcan herramientas centradas para el sistema operativo, como puede ser un calendario, un reloj, una aplicación de ajustes, etcétera. Y cuando una

Las interfaces de usuario (UI) son fundamentales para que los programas sean más accesibles y utilizables por personas que no están familiarizadas con la terminal o las líneas de comando.
## 
Rendering a UI on any operating system ultimately requires interacting with a graphics API.
For example, the Windows API uses a combination of technologies to render windows, leveraging the power of DirectX and the Desktop Window Manager (DWM).
1. **Window Creation:** When you create a window using the Win32 API functions (like `CreateWindowEx`), the system allocates resources for the window and registers it with the DWM.
    
2. **Content Rendering:** Your application is responsible for rendering the content of the window. This can be done using various methods:
    
    - **GDI (Graphics Device Interface):** An older 2D graphics API. While still supported, it's less performant than newer options.
    - **Direct2D:** A modern 2D graphics API built on top of DirectX. It's hardware-accelerated and provides a more efficient way to render 2D content within a window.
    - **Direct3D:** For more complex 3D graphics or high-performance 2D graphics, applications can use Direct3D directly.
    - **Other UI Frameworks:** If you're using a UI framework like WPF or WinUI, the framework handles the rendering using Direct2D or Direct3D under the hood.
3. **DWM Composition:** Once your application has rendered the window content (into a DirectX surface or other compatible format), the DWM takes over. It composites the content of all windows on the desktop, applying effects like transparency, shadows, and animations. This composition is done using Direct3D.
    
4. **Presentation:** The final composed desktop image is then presented to the display by the DWM.
The Win32 API provides the mechanisms for creating and managing windows, while the actual rendering is done by your application (using GDI, Direct2D, Direct3D, or a UI framework) and then composited and presented by the DWM using Direct3D. DirectX plays a crucial role in the modern Windows rendering pipeline, even for seemingly simple window rendering.
## Que sí y que no
Everything has its way, its advantages and disadvantages; you can't do everything at the same time. Choosing a technology or paradigm involves making trade-offs based on your priorities- be it performance, development, speed, control, maintainability, or ease of use.
