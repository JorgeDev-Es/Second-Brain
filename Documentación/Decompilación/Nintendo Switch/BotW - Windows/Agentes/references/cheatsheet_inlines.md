# Decompilation Cheatsheet & Patrones Inline (zeldaret/botw)

Guía de referencia rápida para reconocer funciones inline en el pseudocódigo de IDA/Ghidra y solucionar diferencias de generación de código (codegen) con Clang 4.0.1 en AArch64.

---

## 1. Patrones Inline de `sead`

### `sead::SafeString` y Constructores Implícitos
Cuando veas una estructura en la pila inicializada con la `vtable` de `sead::SafeStringBase` y un puntero a literal de cadena:
```c
// Pseudocódigo IDA/Ghidra:
vtable = &sead::SafeStringBase<char>::vtable;
cstr = "Enemy_Assassin_Junior";
```
Equivale en C++ a pasar un literal directamente a un parámetro `const sead::SafeString&` o declarar:
```cpp
sead::SafeString str = "Enemy_Assassin_Junior";
```

### `sead::SafeString::isEmpty()`
```c
// Pseudocódigo:
str.vptr->assureTerminationImpl_(&str);
if (*str.mStringTop == sead::SafeStringBase::cNullChar) { ... }
```
Reemplazar por:
```cpp
if (str.isEmpty()) { ... }
```

### `sead::SafeString::isEqual` / `operator==`
```c
// Pseudocódigo:
enemy->vptr->assureTermination(enemy);
v15 = enemy->mStringTop;
if (v15 == "Enemy_Assassin_Junior") { ... }
// seguido de un bucle do-while comparando byte por byte hasta cNullChar o 0x80000
```
Reemplazar por:
```cpp
if (enemy == "Enemy_Assassin_Junior") {
    // ...
}
```

### `sead::SafeString::calcLength()`
Un bucle que suma de 3 en 3 (`str_length += 3LL`), verifica `cNullChar` en offsets `+0`, `+1`, `+2` y tiene un límite de seguridad de `0x80000`:
```cpp
s32 len = str.calcLength();
```

### `sead::BufferedSafeString::copy` / `FixedSafeString`
Cuando un `FixedSafeString<N>` establece su `vptr`, asigna `mBufferSize = N`, llama a `assureTerminationImpl_` y ejecuta un bucle de copia con límite `mBufferSize - 1`:
```cpp
sead::FixedSafeString<64> name(other_string);
// o bien:
name.copy(other_string);
```

### `sead::makeScopedLock` (`sead::CriticalSection`)
Si una función llama a `sead::CriticalSection::lock(&cs)` al inicio de un bloque y `sead::CriticalSection::unlock(&cs)` al salir (incluyendo múltiples puntos de retorno):
```cpp
{
    auto lock = sead::makeScopedLock(mCS);
    // código protegido...
}
```

### `sead::Buffer<T>::operator[]` y `get`
El acceso en modo seguro o ciertas funciones de `sead::Buffer` comprueban límites (`if (this->mSize <= idx)` y devuelven `&mBuffer[0]` o `nullptr`):
```cpp
// Si devuelve referencia con fallback al primer elemento:
auto& item = mBuffer[idx];
// Si devuelve puntero con fallback a nullptr cuando idx < 0 || idx >= mSize:
auto* item = mBuffer.get(idx);
```

### `sead::Buffer<T>::allocBufferAssert` / `tryAllocBuffer`
Cuando veas una multiplicación `sizeof(T) * count + 8` (para el header de arreglo si `T` tiene destructor) o `operator new[](size, heap, alignment, std::nothrow)` seguida de un bucle inicializando cada elemento:
```cpp
mBuffer.allocBufferAssert(count, heap);
// o si comprueba el retorno booleano:
if (!mBuffer.tryAllocBuffer(count, heap))
    return false;
```

### `sead::DynamicCast<Derived*>` (SEAD RTTI)
Patrón clásico en el pseudocódigo:
```c
x = __ldar(&guard_var);
if ((x & 1) == 0 && __cxa_guard_acquire(&guard_var)) {
    // inicialización estática de RuntimeTypeInfo
    __cxa_guard_release(&guard_var);
}
if (ptr && ptr->checkDerivedRuntimeTypeInfo(ptr, &Derived::sRuntimeTypeInfo)) { ... }
```
Reemplazar todo el bloque por:
```cpp
if (auto* derived = sead::DynamicCast<Derived>(ptr)) {
    // usar derived...
}
```

### Placement `new` con `sead::Heap`
```c
// Pseudocódigo:
void* ptr = operator new(sizeof(SomeClass), heap, 8u, &std::nothrow);
if (ptr) SomeClass::SomeClass(ptr);
```
Reemplazar por:
```cpp
auto* ptr = new (heap, std::nothrow) SomeClass();
// Si no pasa std::nothrow:
auto* ptr = new (heap) SomeClass();
```

### Matemáticas (`sead::Mathf`)
- Instrucción `fmin` en AArch64 -> `sead::Mathf::maxClamp(val, max_val)` (o `val < max_val ? val : max_val`).
- Instrucción `fminnm` en AArch64 -> `sead::Mathf::min(a, b)`.
- Instrucción `fmax` en AArch64 -> `sead::Mathf::minClamp(val, min_val)`.
- Instrucción `fmaxnm` en AArch64 -> `sead::Mathf::max(a, b)`.

---

## 2. Resolución de Mismatches en AArch64 (Clang 4.0.1)

### Orden Incorrecto de Bloques Básicos (Branching)
1. **Invierte condicionales:** Cambia `if (a) { X } else { Y }` por `if (!a) { Y } else { X }`.
2. **Reordena condiciones lógicas:** Si las lecturas de memoria son independientes, prueba cambiar `if (a && b)` o `if (x || y)`.
3. **Ternarios vs `if/else`:** Aunque Clang suele normalizarlos, con objetos complejos o referencias puede cambiar el registro asignado.
4. **Funciones inline auxiliares:** Si una expresión compleja desordena los registros de toda la función, extráela a una pequeña función privada/estática `inline`. El asignador de registros de LLVM trata los valores de retorno de funciones inlined de forma ligeramente distinta a las variables locales directas.

### Diferencias en Bucles (`Loops`)
1. **Tipos de índice (`s32` vs `u32`):** En arquitecturas de 64 bits (AArch64), usar `s32` (con signo) obliga al compilador a veces a emitir instrucciones de extensión de signo (`sxtw`) al indexar arreglos, mientras que `u32` o `size_t` no, o viceversa. También afecta el desenrollado de bucles (*loop unrolling*).
2. **Condición de parada (`<` vs `!=`):** Prueba primero `<`. Si el límite no es constante en tiempo de compilación y el ensamblador usa `B.NE` sin comprobación inicial de `<`, prueba `!=`.
3. **Range-based `for` vs Iteradores explícitos:**
   - Estándar preferido: `for (auto& item : container)`
   - Si el iterador final se recalcula en cada vuelta: `for (auto it = container.begin(); it != container.end(); ++it)`
   - Algoritmos STL (común en `EventFlow` y algunos managers): `std::for_each`, `std::any_of`, `std::all_of`.

### Diferencias Menores (Banderas e Instrucciones)
- **Signedness en comparaciones de enteros:**
  - `B.HI` / `B.HS` / `B.LO` / `B.LS` -> Comparación **unsigned** (`u32`, `u64`).
  - `B.GT` / `B.GE` / `B.LT` / `B.LE` -> Comparación **signed** (`s32`, `s64`).
- **Punteros vs `uintptr_t`:** Comparar o restar punteros directamente no siempre genera el mismo IR en Clang 4.0.1 que hacer cast a `uintptr_t`.
- **Inicialización de estructuras:** En constructores, prefiere usar inicializadores por defecto en la declaración de la clase (`u32 mFlags = 0;`) en lugar de asignarlos en el cuerpo del constructor.
