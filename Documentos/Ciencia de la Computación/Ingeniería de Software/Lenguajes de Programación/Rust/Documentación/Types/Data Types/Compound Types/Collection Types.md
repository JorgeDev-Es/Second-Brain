# Collection Types
## Arrays and vectors
Arrays and vectors are used to store sequences of data, but they have differences in how they are managed:
- `Array`s:
	- **Fixed Size**: An array has a fixed size, which is determined at compile time. This size is part of the array's type signature.
	- **Stack Allocation:** Arrays are typically allocated on the stack (though very large arrays might be moved to the heap by the compiler depending on context and optimization).
	- **Type:** The size `N` is part of the type `[T; N]`. An array of size 5 is a different type from an array of size 6.
	- **Performance:** Generally very efficient for access and iteration because their size is known and data is contiguous, often on the stack. No runtime overhead for resizing.
	- **Flexibility:** Less flexible for scenarios where the number of elements isn't known beforehand or changes during program execution.
- `Vector`s:
	- **Growable Size:** A `Vec<T>` (short for "vector") is a dynamic, growable array type. Its size can change at runtime; you can push elements onto it or pop them off.
	- **Heap Allocation:** Vectors allocate their data on the heap. They store a pointer to the data, their current length, and their capacity on the stack.
	- **Type:** The type `Vec<T>` does _not_ include the size. A `Vec<i32>` can hold zero, five, or a million `i32`s.
	- **Flexibility:** Much more flexible than arrays for dynamic collections of data.
	- **Performance:** Accessing elements is still O(1) (constant time), but pushing elements may sometimes require reallocation (copying data to a larger area on the heap), which has performance costs. There's also a small overhead for heap allocation compared to stack allocation.