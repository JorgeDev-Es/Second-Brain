# Bifurcación Condicional
```Assembly
main:
    sub     sp, sp, #0x10          // 1. Reserva 16 bytes en la pila
    str     wzr, [sp, #12]         // 2. Inicializa la ranura de retorno [sp, #12] en 0 por defecto
    mov     w8, #0x9               // 3. Calcula 3 * 3 = 9
    str     w8, [sp, #8]           // 4. Guarda a = 9 en la ranura [sp, #8]
    ldr     w8, [sp, #8]           // 5. Vuelve a leer 'a' desde la pila (típico de modo Debug)
    subs    w8, w8, #0x4           // 6. Resta 4 a 'w8' y actualiza las banderas de condición
    b.gt    7ec <main+0x2c>        // 7. Si a > 4, salta al bloque del 'else/return 0'
    b       7e0 <main+0x20>        // 8. Si no, salta al bloque del 'if'

// --- Rama if (a <= 4) ---
    mov     w8, #0x1               // Prepara el valor 1
    str     w8, [sp, #12]          // Guarda 1 en la ranura de retorno de la pila
    b       7f4 <main+0x34>        // Salta a la salida común

// --- Rama else (continúa con return 0) ---
    str     wzr, [sp, #12]         // Guarda 0 (wzr) en la ranura de retorno de la pila
    b       7f4 <main+0x34>        // Salta a la salida común

// --- Salida unificada (main+0x34) ---
    ldr     w0, [sp, #12]          // Carga el valor final decidido (0 o 1) en w0
    add     sp, sp, #0x10          // Libera la pila
    ret                            // Retorna con el valor cargado en w0
```