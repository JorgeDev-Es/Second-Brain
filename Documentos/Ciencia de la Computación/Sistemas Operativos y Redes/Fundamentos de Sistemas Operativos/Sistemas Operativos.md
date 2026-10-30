# Operating Systems (OS)
Un sistema operativo es un [[Documentos/Ciencia de la Computación/Sistemas Operativos y Redes/Fundamentos de Sistemas Operativos/System Software|software de sistema]] que administra el hardware de la computadora y los recursos del software.
También proporciona servicios compartidos para programas de computadora.
## Características
## Components
### Kernel
### Program execution
### Interrupts
### Software interrupt
### Signal
### Hardware interrupt
### Input/output
### Interrupt-driven I/O
### Direct memory access
### Memory Management
### Virtual memory
### Concurrency
### File system
### Security
### User interface
## Compatibilidad e incompatibilidad
El sistema operativo tiene la tarea de definir que es y que no es compatible, estableciendo reglas y abstracciones.

Un sistema operativo Linux no puede ejecutar programas de Windows, no porque el hardware sea incapaz de hacerlo, sino porque el sistema operativo no los reconoce como compatibles.

### ¿Donde nace la incompatibilidad?
#### Application Binary Interface
#### Syscalls
#### Executing Environment and dependencies
#### Security models and permisos
## ¿Qué es y qué no es un sistema operativo?
### ¿Qué es?
### ¿Qué no es?
## ¿Qué ofrece un sistema operativo?
Un sistema operativo ofrece la abstracción, la gestión de recursos y un aislamiento o protección.
### Abstracción
Un programa no necesita como funciona el sistema de archivos o el medio.

La CPU del sistema no sabe que es un proceso, la CPU ejecuta instrucciones de manera lineal, sino que todo ello son abstracciones del sistema operativo para organizar el uso de la CPU y otros recursos.
## Intermediario entre el hardware y el software
Las aplicaciones no interactua directamente con los dispositivos de entrada y salida, sino que el sistema operativo se encarga de manejarlos mediante eventos.

- Los dispositivos (mouse, teclado, etcétera) generan interrupciones de hardware.
- El **kernel** la captura y la traduce en un evento.
- El **subsistema gráfico** (como `win32k.sys`) determina qué ventana tiene el foco o está bajo el cursor.
- El sistema envía un **mensaje** al programa correspondiente, como `WM_LBUTTONDOWN`.
- El programa recibe ese mensaje en su **procedimiento de ventana (**`WndProc`**)** y decide qué hacer.
## Recursos
### Referencias
https://en.wikipedia.org/wiki/Operating_system