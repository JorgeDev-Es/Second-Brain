# `Window` Class
Represents the window of the current Application.
- **Contenedor raíz**:
    
    - Es el objeto que representa **una ventana nativa de la aplicación**.
        
    - Es el **marco** donde se muestra todo el contenido visual (páginas, controles, layouts).
        
- **Parte del sistema de ventanas**:
    
    - Corresponde a una **ventana de nivel superior** de la aplicación (con barra de título, bordes, botones de minimizar/maximizar/cerrar).
        
    - Se integra con el sistema operativo (alt+tab, administración de ventanas, snapping en escritorio).
        
- **Punto de conexión con la UI**:
    
    - Tiene la propiedad `Content`, donde se asigna un **elemento raíz de XAML** (ej. un `Frame` o una `Page`).
        
    - Es el objeto que la aplicación muestra llamando a `window.Activate()`.
        
- **Gestiona ciclo de vida visual**:
    
    - Se crea en el `OnLaunched` de la clase `Application`.
        
    - Puede haber **múltiples ventanas** en la misma app (útil en apps de escritorio multitarea).
        

---

### ❌ Qué **no es** un `Window` en WinUI 3

- **No es un control XAML**:
    
    - A diferencia de `Grid`, `StackPanel`, `Page`, etc., **no forma parte del árbol visual XAML**.
        
    - No se coloca dentro de otro control ni se anida como layout.
        
- **No es la aplicación completa**:
    
    - La clase `Application` (en `Microsoft.UI.Xaml.Application`) administra el **ciclo de vida global** de la app, pero un `Window` es solo una de sus posibles superficies visuales.
        
- **No es un proceso separado**:
    
    - Todas las ventanas de la app comparten el mismo proceso y recursos.
        
    - No equivale a ejecutar otra instancia de la app.
        
- **No maneja navegación interna**:
    
    - La navegación entre páginas o vistas se hace con un `Frame` dentro del `Window.Content`.
        
    - El `Window` solo hospeda el contenido, no controla la navegación directamente.