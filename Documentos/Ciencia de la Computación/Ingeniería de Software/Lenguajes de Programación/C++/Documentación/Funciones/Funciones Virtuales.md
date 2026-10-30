# Funciones virtuales
## Tipos de funciones virtuales
### Función virtual normal
#### Definición
```C++
virtual void myFunc() {
	// Implementation...
}
```
### Función virtual pura

#### Definición
Se declara con `virtual`, no tiene implementación y termina con `= 0`
```c++
virtual void* tryAlloc(size_t size, s32 alignment) = 0;
```