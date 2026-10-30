# Funciones en Assembly
## Reservar memoria
A nivel de hardware, no existe el concepto de "scope" automático por defecto como si lo hacen en lenguajes de alto nivel.
En un programa, todas las funciones de un hilo comparten el mismo bloque continuo de memoria llamado stack y el mismo stack pointer (`sp` o `rsp`).
Espacio para variables locales
Al incrementar la cantidad de variables locales, se debe incrementar la cantidad de espacio reservado:
```
// C
int main() {
    int a = 0;
    int b = 1;
    int c = 2;
    return 0;
}

// Assembly
main:
        sub     sp, sp, #16
        //...
```
3 variables de 4 bytes requieren 12 bytes de memoria, por lo que se reservan solo 16 bytes (`#16`) de memoria.
```
// C
int main() {
    int a = 0;
    int b = 1;
    int c = 2;
    int d = 3;
    return 0;
}

// Assembly
main:
        sub     sp, sp, #32
```
4 variables de 4 bytes necesita 16 bytes, por lo que se reservan 32 bytes (`#32`) de memoria.
### Preservación de registros y dirección de retorno