```Assembly
section	.text
   global main     ;Debe ser declarado para el linker (ld)
	
main:	            ; Le dice al linker el punto de entrada del programa
   mov	edx,len     ; Tamaño del mensaje
   mov	ecx,msg     ; Mensaje a escribir
   mov	ebx,1       ; file descriptor (stdout)
   mov	eax,4       ; Número del system call (sys_write)
   int	0x80        ; Call kernel
	
   mov	eax,1       ; Número del system call (sys_exit)
   int	0x80        ; Call kernel

section	.data
msg db 'Hello, world', 0xa  ; string que se va a imprimir
len equ $ - msg     ; Tamaño del string
```