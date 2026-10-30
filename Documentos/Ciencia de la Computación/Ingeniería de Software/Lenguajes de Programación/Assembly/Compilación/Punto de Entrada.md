# Punto de Entrada
```C++
// C or C++
int main() {
    return 0;
}
```

```Assembly
main:
 sub    sp, sp, #0x10     `Reserva 16 bytes para variables locales.`
 mov    w0, wzr           
 str    wzr, [sp, #12]
 add    sp, sp, #0x10
 ret
```

### `sub    sp, sp, #0x10`
La instrucción decrementa el Stack Pointer (`sp`) en 16 bytes (en hexadecimal). En las arquitecturas modernas, el stack crece hacia abajo.