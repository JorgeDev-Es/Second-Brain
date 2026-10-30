# UI Software Architecture
UI Architecture se refiere a la manera en que se organiza, diseña y conecta la interfaz gráfica de una aplicación con el resto del sistema. No se trata solo de "cómo se ve", sino de cómo se estructura y comunica la UI con la lógica y los datos.
## Objetivos
## Principales capas
### Presentación (View)
Debe ser lo más "dummy" posible: solo recibe eventos y los muestra.
## Eventos Directos (`onClick()`, `onChange()`, etc.)

Bueno para prototipos o cosas simples.
Puede volverse difícil de mantener si pones mucha lógica.
## Controladores o funciones
## Patrones de Arquitectura
Separan la lógica de UI (vista) de la lógica de negocio (modelo).
Te obliga a pensar más en estructuras, pero la recompensa es mayor claridad.
## State management
En lugar de reaccionar solo a eventos, manejas el estado de la aplicación y haces que la UI reaccione a ese estado.
## Reactive Programming
### Component-Based UI Design
Organizar la UI en componentes reutilizables.