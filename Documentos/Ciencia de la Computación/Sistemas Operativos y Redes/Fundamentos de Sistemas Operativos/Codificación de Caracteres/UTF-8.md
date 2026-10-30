## UTF-8
## ¿Qué es UTF-8?
UTF-8

UTF-8 stands for Unicode Transformation Format - 8 bits.
## Lenguajes de programación
Los lenguajes de programación usan UTF-8 como el estándar, incluso para leer el código fuente.
E incluso si el lenguaje de programación puede leer otra codificación de caracteres para crear cadenas de caracteres internas, lo único que hara es decodificarlas a UTF-8 para poder trabajar con strings.
## Tamaño en bytes variables
Por ejemplo, al usar Rust para detectar la cantidad de bytes utilizadas en un string, notamos que solo usara 1 byte por cada caracter ASCII
```Rust
let word: &'static str = "Avocado";

print("{}", word.len()); // Output> 7
```

Pero al agregar un emoji, en lugar de usar 8 bytes, usa 11:
```Rust
let word: &'static str = "Avocado🥑";

print("{}", word.len()); // Output> 10
```
## Referencias
https://en.wikipedia.org/wiki/UTF-8
https://www.youtube.com/watch?v=vpSkBV5vydg