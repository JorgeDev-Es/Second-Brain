# Codificación de Caracteres en C\#
.NET usa UTF-16 internamente, sin embargo, el estándar actual es UTF-8.
Debido a que .NET oculta los detalles de la codificación interna, la mayoría del tiempo no se percibe la diferencia en la codificación de caracteres.
```C#
string text = "avocado";

int size = System.Text.Encoding.Unicode.GetBytes(text).Length;

Console.WriteLine(size); // Output> 14
```

```C#
string text = "avocado🥑";

int size = System.Text.Encoding.Unicode.GetBytes(text).Length;

Console.WriteLine(size); // Output> 18
```