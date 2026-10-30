# Listas en Python
## ¿Qué son las listas en Python?
Las listas de Python son una estructura de datos integrada en el lenguaje usados para almacenar una colección de objetos.

```Python
a = [1, 2, 3, 4, 5]
```
## Constructor
La función [[Documentos/Ciencia de la Computación/Ingeniería de Software/Lenguajes de Programación/Python/Referencia/Núcleo del Lenguaje/Funciones/list()|list()]] es usado para crear nuevas listas de objetos. Es usado principalmente para instanciar una lista vacia o para convertir un objeto iterable en una lista mutable estándar.
```Python
# Crear una lista vacia
empty_list = list()

print(empty_list) # Output> []

# Conversión de string
chars = list("Python") # Output> ['P', 'y', 't', 'h', 'o', 'n']

# Conversión de tupla
numbers = list((1, 2, 3)) # Output> [1, 2, 3]

# Dictionary conversion (extracts keys by default)
dict_keys = list({'a': 1, 'b': 2}) # Output> ['a', 'b']
```