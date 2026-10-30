## Dato inmediato (Constante o literal)
```C
// C
int a = 32;

// Assembly
mov eax, 42
```
## Copiar registro a registro (Asignación entre variables locales)
```C
// C
int a = 10;
int b = a;

// Assembly
mov ebx, ecx
```
## Cargar desde memoria (Lectura de RAM)
```C
// C
int global_val = 100;

void foo() {
	int x = global_val;
}

// Assembly
mov eax, [global_val]
```