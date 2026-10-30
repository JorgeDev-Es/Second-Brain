- **Definición básica**:
    
    - Es un enfoque donde el sistema gráfico **mantiene un grafo de escena u objetos persistentes en memoria**.
        
    - El programador describe los elementos (formas, modelos, UI) y sus propiedades, y el motor se encarga de redibujarlos automáticamente en cada frame.
        
- **Contraste con Immediate-Mode**:
    
    - En _immediate mode_, el programador debe redibujar manualmente todo en cada frame.
        
    - En _retained mode_, el motor guarda la información de los objetos y los renderiza según corresponda, sin que el programador tenga que volver a emitir todos los comandos cada vez.
        
- **Características principales**:
    
    - **Estructura jerárquica**: normalmente se organiza en un _scene graph_ (árbol de nodos con transformaciones y objetos).
        
    - **Persistencia**: una vez se agrega un objeto a la escena, se sigue dibujando hasta que se cambie o elimine.
        
    - **Automatización**: el motor gestiona optimizaciones (occlusion culling, batching, sorting).
        
    - **Menor control directo**: el programador confía en que el motor administre cuándo y cómo dibujar.
        
- **Ejemplos en la práctica**:
    
    - **Motores de videojuegos**: Unity, Unreal Engine, Godot.
        
    - **Frameworks de UI**: WPF, JavaFX, Qt (Widgets y QML).
        
    - **APIs gráficas modernas**: Scene graphs en Vulkan/DirectX 12 a través de librerías de más alto nivel.
        
- **Casos de uso habituales**:
    
    - Aplicaciones con **escenas complejas y persistentes**, donde mantener manualmente todos los elementos sería poco eficiente.
        
    - **Interfaces gráficas interactivas** que requieren que los objetos permanezcan en pantalla hasta ser modificados.
        
    - **Videojuegos y simulaciones** donde la organización jerárquica de objetos facilita animaciones, cámaras y físicas.