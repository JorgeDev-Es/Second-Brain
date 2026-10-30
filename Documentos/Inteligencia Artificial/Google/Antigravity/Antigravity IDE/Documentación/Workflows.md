# Skills de Antigravity IDE
## ¿Qué son los workflows?
Workflows son secuencias de pasos e instrucciones predefinidas que guían a los agentes de inteligencia artificial para realizar tareas específicas de manera controlada y estructurada.
## Características
- Formato y límite. Se guardan como archivos Markdown con un título, una descripción y pasos detallados, con un límite de hasta 12 000 caracteres por archivo.
- Alcance. pueden ser globales o específicos de un espacio de trabajo.
- Independencia de pila tecnológica. Muchos workflows comunitarios están diseñados para detectar automáticamente tu framework, estilo y patrones de proyecto en lugar de forzar una tecnología específica.
- Activación. A diferencia de las reglas (rules) que suelen estar siempre activas, los flujos de trabajo se ejecutan bajo demanda cuando se les invoca.
Globales: `~/.gemini/config/workflows`
Workspace: `.agents/workflows/`