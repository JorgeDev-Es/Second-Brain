# Reduced Instruction Set Architecture
- Las operaciones aritméticas solo ocurren entre registros, y el acceso a memoria se hace únicamente mediante instrucciones dedicadas de carga y guardado.

EL valor que devuelve una función al terminar siempre se guarda en el registro w0 (o x0).

Nació bajo la idea de que la mayoría de los programas solo utilizan un subconjunto pequeño de instrucciones simples. Simplificar las instrucciones permitia ejecutarlas en un único ciclo de reloj y diseñar procesadores con pipelines mucho más rápidas y predecibles.