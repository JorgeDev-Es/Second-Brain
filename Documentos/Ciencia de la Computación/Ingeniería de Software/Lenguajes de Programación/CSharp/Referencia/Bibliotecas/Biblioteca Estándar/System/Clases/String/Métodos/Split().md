# Método `Split()`  de la clase `String`
## Descripción del método
Divide una cadena de caracteres en una lista de subcadenas en base a un delimitador específico.
## Sobrecargas
### `Split(String, StringSplitOptions)`
Divide una cadena de caracteres en subcadenas en base a la cadena de caracteres separadora.
```C#
public string[] Split(string? separator, StringSplitOptions options = System.StringSplitOptions.None);
```

## Detalles
### Espacio en blanco como delimitador por defecto
Al usar `Split()` con `null`, arrays vacíos u omitiendo argumentos por completo, el método `Split()` usa los separadores de espacio en blanco por defecto.