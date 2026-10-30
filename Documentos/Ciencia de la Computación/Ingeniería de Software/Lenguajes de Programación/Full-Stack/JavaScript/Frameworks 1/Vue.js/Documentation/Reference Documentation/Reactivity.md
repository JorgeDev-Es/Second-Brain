# Reactivity in Vue.js
`ref()`creates a reactive reference. Under the hood, the object is wrapped in a `RefImpl` object which has a `.value` property.
## Using `ref()` with objects
Using `ref()` with objects in Vue.js allows you to create a reactive reference to any

`ref()` no hace que todas las propiedades de un objeto sean reactivas automaticamente. `ref()` se refiere únicamente al valor interno que envuelve (accesible a través de `.value`), pero no realiza un seguimiento reactivo de los cambios en propiedades anidadas de objetos o arrays. Es decir, `ref()` es reactivo en el nivel "superficial" (shallow reactivity), no en el nivel "profundo" (deep reactivity).

### **¿Qué significa esto?**

1. **Si el valor de una `ref()` es un primitivo** (como `number`, `string`, `boolean`):
    
    - La reactividad funciona perfectamente, ya que `ref()` rastrea cambios directos al `.value`.
    
```JavaScript
const count = ref(0);
count.value = 1; // Reactivo ✅
```
**Si el valor de una `ref()` es un objeto o array**:

- La reactividad está vinculada a la referencia del objeto/array (si lo reemplazas por completo, se detecta el cambio).
    
- **Pero los cambios en propiedades internas del objeto o elementos del array no son reactivos** a menos que uses `reactive()` o métodos especiales.
```JavaScript
const user = ref({ name: 'Alice', age: 30 });

// Reactivo ✅ (reemplazo completo)
user.value = { name: 'Bob', age: 25 };

// No reactivo ❌ (cambio en propiedad interna)
user.value.age = 26; // Vue no rastreará este cambio automáticamente.
```