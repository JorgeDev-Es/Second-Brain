# Archivos
## Lectura de archivos
### `File.ReadAllLines()`
## Formatos de saltos de línea
C# está diseñado para manejar automáticamente los diferentes formatos de salto de línea:
- **`\n`** (LF, Unix/Linux)
- **`\r\n`** (CRLF, Windows)
- **`\r`** (CR, Mac Clásico)
Por lo que `StreamReader.ReadLine()` siempre devuelve una cadena limpia.