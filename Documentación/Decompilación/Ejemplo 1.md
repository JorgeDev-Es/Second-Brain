```
my_function:
11db2e8:    mov     x8, x0
11db2ec:    ldr     w9, [x8, #0x520]
11db2f0:    tbz     w9, #0x5, 11db304
11db2f4:    ldr     x0, [x8, #0x4d0]
11db2f8:    cbz     x0, 11db304
11db2fc:    mov     x1, x8
11db300:    b       d3c5e0
11db304:    mov     x0, xzr
11db308:    ret
f5a24c:     ret 
```
## Variables
### `x0`
`x0` contiene el primer argumento pasado a la función (a menudo un puntero o un objeto (`this`)
### `x8`
`x8` es un registro temporal/scratch que se usa para no perder ese puntero original.