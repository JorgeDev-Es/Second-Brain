# Software Engineering Principles
## Software Design Principles
Software design principles
### DRY (Don't Repeat Yourself)
No repetir código o lógica innecesariamente.
Avoid code duplication by abstracting common logic into reusable components. This reduces errors and makes maintenance easier.
### KISS (Keep It Simple, Stupid)
Strive for simplicity in design and avoid unnecessary complexity. Simpler code is easier to understand, debug, and mantain
### YAGNI (You Ain't Gonna Need It)
Avoid implementing features or functionality until they are actually needed.
This prevents wasted effort and keeps the codebase leaner.
### Don't Reinvent The Wheel
Encourages using existing solutions and tools instead of creating new ones from scratch.
It emphasizes leveraging pre-built libraries, frameworks, and readily available code or components when they can fulfill the project's requirements.
**Saves time and resources**. Building something from ground up takes significant time and effort. Utilizing existing solutions drastically reduces development time, allowing developers to focus on more critical aspects of the project.

For example, if you need a sort algorithm, you should use built-in functions in the programming language (como `sort()` en Python o `std::sort` en C++) en lugar de implementar tu propio algoritmo desde cero.
### Code Reuse Principle