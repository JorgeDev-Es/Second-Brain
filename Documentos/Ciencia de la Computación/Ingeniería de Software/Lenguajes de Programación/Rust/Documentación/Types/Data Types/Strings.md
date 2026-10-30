# Strings Data Type in Rust
In Rust, there are primarily two ways to represent sequences of characters (text):
- String Literals (`&str`)
- `String` Type
## String Literals
String literals are immutable references to string data that is hardcoded directly into your program.
They have a fixed size known at compile time.
They are very efficient because they don't require heap memory allocation.
## `String` type
The `String` type is a data type that owns the string data, which is stored on the heap (dynamic memory).
It is mutable, meaning you can modify its contents (add, remove, replace characters).
It has a dynamic size and can grow or shrink at runtime.
It is created from a string literal using methods like `String::from()` or `.to_string()`.