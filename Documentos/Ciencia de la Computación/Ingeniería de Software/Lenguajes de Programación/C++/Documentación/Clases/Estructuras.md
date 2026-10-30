# Estructuras
## ¿En qué se diferencia una estructura de una clase?
La única diferencia entre una clase y una estructura es que todos los miembros y la herencia de `struct` son `public` por defecto, mientras que en `class` son `private` por defecto.
Ambos pueden tener métodos, constructores, destructores, operadores sobrecargados, modificadores de acceso explícitos, herencia, etcétera.
```C++
struct MiStruct {
    int x;
    int y;
};

class MiClase {
public: // Al poner public, es 100% idéntica al struct
    int x;
    int y;
};
```