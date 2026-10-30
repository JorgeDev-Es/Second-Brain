# Assembler
Assembler no es un lenguaje de programación en el sentido tradicional como Python o Java. Más bien, es una representación simbólica del código máquina, que es el lenguaje que entiende directamente el procesador.
**¿Qué significa esto?**

- **Código máquina:** Son secuencias de 0s y 1s que instruyen al procesador sobre qué operaciones realizar. Es muy difícil de leer y escribir para los humanos.
- **Ensamblador:** Utiliza mnemónicos (abreviaturas) para representar las instrucciones del código máquina, lo que lo hace más legible. Por ejemplo, en lugar de una secuencia binaria, se puede escribir "ADD" para indicar una suma.
**La relación entre ensamblador, arquitectura y sistema operativo**

Como bien dices, el ensamblador está intrínsecamente ligado a la arquitectura del procesador y, en cierta medida, al sistema operativo.

- **Arquitectura:** Cada arquitectura (x86, x86_64, ARM, etc.) tiene su propio conjunto de instrucciones y registros. Por lo tanto, el código ensamblador escrito para una arquitectura no funcionará en otra.
- **Sistema operativo:** El sistema operativo también influye, ya que proporciona las interfaces y convenciones para acceder a los recursos del sistema (memoria, dispositivos, etc.). Aunque el ensamblador en sí no depende directamente del sistema operativo, la forma en que se interactúa con el sistema puede variar.

**Ejemplos**

- No es lo mismo programar en ensamblador para Windows con x86_64 que para Linux con x86. Las instrucciones básicas pueden ser similares, pero la forma de acceder a la memoria, manejar interrupciones y realizar llamadas al sistema será diferente.
- Programar en ensamblador para MacOS con ARM implica un conjunto de instrucciones y registros completamente distintos a los de x86.