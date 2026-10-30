```Python
def printListNode(list_node: ListNode):  
    actual_list = list_node  
    
    while actual_list.next is not None:  
        print(actual_list.val)  
        actual_list = actual_list.next  
    
    print(actual_list.val)
```
# Problemas
### Variable naming
#### `actual_list`
```Python
actual_list = list_node
```
❌ `actual_list`
✅ `current`
- `current` es un termino no ambiguo que le dice a cualquier desarrollador lo que la variable representa de manera exacta, en este ejemplo, el node que estás **actualmente** inspeccionando.
- En el inglés, *Current* se refiere a algo que esta pasando en el tiempo presente mientras que *Actual* se refiere a algo que es real o cierto y es usado para contrastar.


### Lógica
#### `while current.next is not None`

```Python
    while current.next is not None:  
        print(current.val)  
        current = current.next  
    
    print(current.val)
```
❌ `while current.next is not None`
- Lista de un solo node. A list with only one node will immediately fail the loop condition, as its `next` pointer is `None`. The code will then need to handle this single node separately.
- **Empty List**: If the list is empty (the head is `None`), calling `current.next` will raise an `AttributeError`, causing your program to crash. This approach is not safe for all possible inputs.
✅ `while current is not None`
- Maneja los nodes automáticamente. El loop continua mientras `current` apunte a un node válido. Se detiene naturalmente cuando `current` se vuelve `None` después de procesar el último node, así que no necesitas agregar código extra para manejar el final de la lista.
- Lista de un solo node. El loop se ejecuta una ves, procesa el node y entonces termina.
- Lista vacía. Si `current` comienza cómo `None`, la condición `current is not None` is inmediatamente `False`, y el loop simplemente se ignora. No se genera el error `AttributeError` al intentar acceder a `current_list.val`.

## 