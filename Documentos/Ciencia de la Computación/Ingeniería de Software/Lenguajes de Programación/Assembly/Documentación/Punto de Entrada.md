
```C
int main() {
    return 0;
}
```

```armasm
main:
        sub     sp, sp, #0x10      # Reserva un bloque de 16 bytes
        mov     w0, wzr            # Mueve un 0 para el retorno de la función.
        str     wzr, [sp, #12]     # Guarda la variable de retorno (modo Debug)
        add     sp, sp, #16        # Libera el stack
        ret                        # Retorna con el valor cargado en w0
```