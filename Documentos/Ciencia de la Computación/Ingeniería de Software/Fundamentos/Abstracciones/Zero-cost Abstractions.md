# Zero-Cost Abstractions
## Lenguajes que no son zero-cost abstractions
La mayoría de los lenguajes de alto nivel (Java, Python, C#, JavaScript, etcétera) introducen abstracciones con costes adicionales inevitables.
- **Java / C#:**
    - La máquina virtual (JVM o CLR) impone un modelo de ejecución con recolección de basura, llamadas dinámicas y _just-in-time compilation_.
    - Aunque el JIT puede optimizar mucho, existe siempre cierta sobrecarga que no estaría presente en un equivalente escrito en C o ensamblador.
- **Python / JavaScript:**
    - La interpretación dinámica y la tipificación en tiempo de ejecución hacen que operaciones simples (como una suma o un acceso a lista) requieran comprobaciones adicionales, muy alejadas del coste real en hardware.
- **Lenguajes puramente funcionales (Haskell, OCaml, etc.):**
    - Muchas abstracciones de alto nivel (monadas, inmutabilidad estricta, recursión, _lazy evaluation_) implican estructuras auxiliares en memoria y evaluaciones diferidas que no pueden eliminarse por completo.
## Lenguajes que **sí se acercan a zero-cost abstractions**

- **C++:** diseñado con esa filosofía desde los años 80.
- **Rust:** adoptó el mismo principio como uno de sus pilares, pero con mayor seguridad en memoria y concurrencia.
- **Ada / Zig:** también siguen una línea similar, aunque con menor popularidad.
## 📌 Implicaciones principales
1. **Control total sobre el coste de ejecución**
    - Cada abstracción puede evaluarse casi como si se hubiera escrito a mano en bajo nivel.
    - Se posibilita la escritura de código de alto nivel sin sacrificar rendimiento.
2. **Ausencia de sobrecarga oculta**
    - No existen mecanismos automáticos como _garbage collection_ o comprobaciones dinámicas que introduzcan costes invisibles al programador.
    - Todo coste en tiempo y memoria puede rastrearse al código escrito.
3. **Mayor responsabilidad del programador**
    - La gestión de recursos, memoria, concurrencia y seguridad depende directamente de las decisiones del desarrollador.
    - El riesgo de errores (fugas de memoria, _use-after-free_, _data races_) aumenta si no se usan correctamente las herramientas del lenguaje.
## 📌 Beneficios de este modelo
- **Máxima eficiencia:**  
    El código puede alcanzar un rendimiento cercano al ensamblador o C puro.
- **Escalabilidad hacia sistemas críticos:**  
    Es ideal para sistemas embebidos, videojuegos, motores gráficos, simulaciones, tiempo real y aplicaciones con recursos limitados.
- **Flexibilidad:**  
    El programador puede elegir entre escribir en un estilo muy abstracto (con STL, plantillas, lambdas) o en estilo cercano al hardware.
- **Previsibilidad:**  
    El coste de una operación se infiere con facilidad, algo fundamental en entornos donde el rendimiento es determinante.
## 📌 Costes y riesgos de este modelo
- **Curva de aprendizaje pronunciada:**  
    Se exige mayor conocimiento del hardware, compilador y modelo de memoria.
- **Mayor propensión a errores críticos:**  
    Una abstracción mal usada (ejemplo: punteros crudos sin RAII) puede provocar fallos graves.
- **Mantenimiento más complejo:**  
    El código con optimizaciones de bajo nivel tiende a ser menos legible y más difícil de mantener en proyectos grandes.
- **Falta de seguridad por defecto (en C++):**  
    A diferencia de Rust, C++ no garantiza memoria y concurrencia seguras, dejando toda la responsabilidad al programador.