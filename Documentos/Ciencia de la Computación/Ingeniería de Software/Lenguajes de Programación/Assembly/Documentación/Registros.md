# Registros
## ¿Qué son los registros?
Los registros son componentes del procesador que almacenan datos y direcciones.

Al contrario de las variables, los registros son un conjunto límitado de registros físicos (`eax`, `ebx`, `ecx`, etc.) y se reutilizan para almacenar valores a lo largo del programa. Para conservar más datos de los caben en los registros, se pueden almacenar en memoria, usando etiquetas como nombres simbólicos.

Algunos registros tienen funciones especiales por la arquitectura utilizada o por convenciones.

En un procesador x86_64, el tamaño de un registro es de 64 bits (8 bytes)
Los registros son casillas de almacenamiento microscópicas ubicadas dentro de procesador. A diferencia de la memoria RAM o el SSD, la CPU solo puede realizar operaciones aritméticas y de control de flujo con datos que estén cargados en sus registros.

En el estándar oficial de 64 bits de ARM (AAPCS64), el procesador tiene 31 registros generales divididos por función y reglas de uso.

La cantidad de registros dependen de la arquitectura objetivo.
## ¿Por qué existen los registros?
La gran mayoría de las operaciones del procesador involucran el procesamiento de datos. Sin embargo, la lectura y almacenamiento de datos en la memoria relentiza al procesador, al requerir procesos complicados.
Para acelerar las operaciones del procesador, el procesador incluye algunas ubicaciones de almacenamiento de memoria internas, llamadas **registros**.
Los registros almacenan datos para ser procesados sin tener que acceder a la memoria.
## Cargar datos en registros
### Inmediato
Cuando cargas un valor constante directamente en un registro (por ejemplo, el número `3`). ese dato viaja incrustado dentro de los propios bits de la instrucción binaria. A este tipo de valores se les denomina **valores inmediatos** (**immediate values**) porque la CPU no necesita consultar la memoria RAM ni el bus de datos para obtener el número, sino que al decodificar la propia instrucción en código máquina, el dato ya está ahí.
### Registro a registro
### Desde memoria (RAM/Variables)
## Tipos de registros
Los registros son agrupados en tres categorías:
- Registros generales
- Registros de control
- Registros segmentados
Los registros generales son generalmente divididos en los siguientes grupos:
- Registros de datos
- Registros de punteros
- Registros de índice
## Registros de propósito general
Los registros de próposito general son 8, pero solo puedes usar 6.
## Registros generales
Cada casilla física mide 64 bits, pero tiene usa `x` si accede a los 64 bits completos y `w` si accede únicamente a los 32 bits inferiores de esa misma casilla.

| Registros                 | Rol estándar         | ¿Para qué sirve?                                                                                                                     |
| ------------------------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `x0` - `x7` (`w0` - `w7`) | Argumentos y retorno | Al llamar a una función, los primeros 8 parámetros se cargan en `x0` - `x7`. Al regresar, el valor devuelto se entrega en `x0`/`w0`. |

## Stack Pointer
## Link Register
## Word Zero Register
Está cableado a cero a nivel de silicio.
##  Program Counter (PC)
El procesador posee un registro especializado llamado Contador de Programa o apuntador de instrucciones (`PC` en ARM y `IP`/`EIP` en x86).
La dirección de memoria a la que apunta el PC se trata exclusivamente como código/instrucción.
## Ciclo de instrucciones
Fetch
Decode
Execute
## Registro de Instrucción (IR)
## Referencias
https://www.tutorialspoint.com/assembly_programming/assembly_introduction.htm
https://www.tutorialspoint.com/assembly_programming/assembly_registers.htm