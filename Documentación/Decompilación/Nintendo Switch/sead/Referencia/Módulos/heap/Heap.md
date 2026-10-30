# `sead::Heap`
`sead/include/heap/seadHeap.h`
Hereda de: [[Documentación/Decompilación/Nintendo Switch/sead/Referencia/Módulos/heap/IDisposer|IDisposer]], INamable, hostio::reflexible.
`sead::Heap` es la clase base abstracta del sistema de gestión de memoria de sead: define la interfaz común de asignación/liberación (`tryAlloc`, `free`, `freeAll`, `adjust`) y organiza la memoria en un árbol jerárquico de heaps con soporte de thread-safety y limpieza automática de objetos.
## ¿Qué es?
Es una clase abstracta pura (una interfaz) que hereda de `IDisposer`, `INamable` y `hostio::Reflexible`. No se instancia directamente: las implementaciones concretas son `ExpHeap` (asignador general con fragmentación, con modos `FirstFit`/`BestFit`) y `FrameHeap` (asignador lineal).

No implementa cómo se asigna la memoria por sí misma, sino que obliga a todas las clases hijas a implementar su propia versión de `tryAlloc`.
## ¿Para qué sirve?

### 1. Asignación de memoria

La interfaz principal son `tryAlloc(size, alignment)` y `free(ptr)`, más una envoltura `alloc()` que hace assert si falla . También soporta `tryRealloc`, `resizeFront`/`resizeBack` y consultas como `getFreeSize()` / `getMaxAllocatableSize()`.
### 2. Jerarquía de heaps
Cada heap tiene `mParent`, una lista `mChildren` y un rango `[mStart, mStart+mSize)` seadHeap.h:110-113 . La raíz es un `ExpHeap` creado sobre el `Arena` por `HeapMgr::createRootHeap_()` seadHeapMgr.cpp:47-51 . `findContainHeap_` permite saber qué heap posee un puntero seadHeap.h:84 .
### 3. Destrucción automática de objetos (`IDisposer`)
Los objetos creados en un heap se registran en `mDisposerList` vía `appendDisposer_`, de modo que al destruir el heap se llama a sus destructores automáticamente .
### 4. Thread-safety y dirección de asignación
Cada heap contiene un `CriticalSection` (`mCS`) activable con `enableLock`, y una dirección `Forward`/`Reverse` que controla si las asignaciones crecen desde el inicio o el final del bloque.
## Ejemplo
`StringBuilderBase::createImpl_` muestra el patrón típico: si no pasas un heap, usa `HeapMgr::instance()->getCurrentHeap()` (el heap actual del thread), asigna con `heap->alloc(...)` y construye el objeto con placement new seadStringBuilder.cpp:42-50 . A su vez, `TaskMgr::finalize` destruye los heaps por tarea vía `heap->destroy()` seadTaskMgr.cpp:128-137 .
## Notes
- `Heap` también integra depuración: flags `cEnableWarning`, `cEnableDebugFillSystem/User` y volcado YAML con `dumpTreeYAML` seadHeap.h:32-33 seadHeap.h:69-71 .
- El operador `new` global usa el "current heap" por thread gestionado por `HeapMgr`, y `ScopedCurrentHeapSetter` permite cambiarlo temporalmente seadHeapMgr.h:56 seadHeapMgr.h:96-105 .