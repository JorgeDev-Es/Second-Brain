- **Composición en Windows App SDK**:
    
    - Es la tecnología que maneja el **renderizado eficiente de elementos visuales** en aplicaciones modernas de Windows.
        
    - Funciona como un motor gráfico independiente que se encarga de **dibujar, animar y componer** visuales en pantalla.
        
    - Permite efectos avanzados (blur, sombras, transformaciones 2D/3D, animaciones fluidas) sin bloquear el hilo principal de la UI.
        
- **Visual Layer**:
    
    - Es la **API de bajo nivel** que expone la composición a los desarrolladores.
        
    - Proporciona un modelo basado en un **árbol de visuales** (_visual tree_), similar a un _scene graph_.
        
    - Cada _Visual_ representa un objeto en pantalla (rectángulos, imágenes, efectos, contenedores) y puede tener hijos.
        
- **Elementos clave del Visual Layer**:
    
    - **Visual**: unidad básica de dibujo, con propiedades de tamaño, posición, opacidad, transformaciones.
        
    - **ContainerVisual**: un _Visual_ que puede contener otros _Visuals_, formando jerarquías.
        
    - **SpriteVisual**: un _Visual_ especializado en mostrar un rectángulo con color sólido, imágenes o efectos.
        
    - **CompositionTarget**: punto de conexión entre la aplicación y el motor de composición.
        
    - **Compositor**: objeto raíz que se usa para crear _Visuals_, animaciones y efectos.
        
- **Ventajas de usar el Visual Layer**:
    
    - **Rendimiento**: muchas animaciones y efectos se ejecutan directamente en la GPU, sin pasar por el hilo de la UI.
        
    - **Flexibilidad**: se pueden crear interfaces y efectos más sofisticados que con controles estándar.
        
    - **Separación de responsabilidades**: la UI (XAML o WinUI) maneja la lógica de interacción, y la composición maneja el renderizado optimizado.
        
- **Ejemplos de uso**:
    
    - Crear animaciones de desplazamiento fluidas en listas.
        
    - Agregar desenfoques acrílicos y sombras suaves en elementos de la UI.
        
    - Integrar contenido 2D/3D con efectos visuales en tiempo real.