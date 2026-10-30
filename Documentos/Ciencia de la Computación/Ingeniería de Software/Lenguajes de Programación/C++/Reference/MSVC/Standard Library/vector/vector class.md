# `vector` class
The C++ Standard Library vector class is a class template for sequence containers.

`vector` is a dynamic array, offering a powerful and flexible way to manage collections of elements.
## Key features
### Dynamic size
Unlike regular arrays, `std::vector` can grow or shrink as needed during runtime. You don't need to specify a fixed size upfront.
### Contiguous storage
Elements in a `vector` are stored in contiguous memory locations, just like a regular array. This provides excellent performance for accessing elements by index (random access).
### Automatic memory management
`vector` handles memory allocation and deallocation automatically. When you add or remove elements, it manages the underlying memory for you.
### Bounds checking (in Debug Mode)
Many implementations provide bounds checking in debug builds, which helps catch errors where you try to access elements outside the valid range of the vector.
### Part of the STL
`vector` is a standard container, meaning it's readily available in any C++ environment that conforms to the standard.