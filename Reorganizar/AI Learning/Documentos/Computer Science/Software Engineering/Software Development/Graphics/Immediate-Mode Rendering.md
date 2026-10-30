- **Definición básica**:
    - Es un enfoque de renderizado donde el programa **envía directamente los comandos de dibujo a la GPU en cada frame**.
    - No existe una "escena" almacenada en el motor gráfico; el programador debe redibujar todo cada vez que se refresca la pantalla.
- **Contraste con Retained-Mode**:
    - En _retained mode_, se guarda un **árbol de objetos o escena** (ejemplo: un canvas con formas o un motor 3D con nodos).
    - En _immediate mode_, la responsabilidad es del programador: si quieres que un objeto siga viéndose, debes volver a llamarlo en cada frame.
- **Características principales**:
    - **Simplicidad conceptual**: se parece a "pintar" cada vez desde cero.
    - **Menor sobrecarga estructural**: no hay necesidad de un grafo de escena complejo.
    - **Gran flexibilidad**: el programador tiene control directo de qué se dibuja y cuándo.
    - **Menos eficiencia en escenas grandes**: como todo se recalcula cada frame, manejar muchos objetos puede ser costoso.
- **Ejemplos en la práctica**:
    - **APIs clásicas**: OpenGL antiguo (`glBegin/glEnd`), DirectX 7.
    - **Frameworks modernos**: Dear ImGui (interfaz inmediata para UI), raylib en 2D/3D.
    - **Contraste**: motores como Unity o Qt usan modos retenidos.
- **Casos de uso habituales**:
    
    - Interfaces gráficas rápidas y temporales (ej. herramientas de debug).
        
    - Prototipos donde se prefiere sencillez a rendimiento.
        
    - Escenarios donde el control preciso frame a frame es más importante que la eficiencia estructural.