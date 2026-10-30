# Types
In Rust, the way you define data structures and associate behavior with them is different from traditional obfect-oriented languages that use the concept of "objects" that bundle data and methods together directly within the instance.
Data structures
You define your custom data types primarily using `struct`s (for grouped data) or `enum`s (for variants). These define the shape of your data.
```Rust
struct Circle {
    radius: f64,
}
```
Behavior (Methods)
You define methods associated with a type using an `impl` block. The `impl` block is separate from the `struct` definition and adds functions (methods) that operate on instances of that type.
```Rust
impl Circle {
    // A method that operates on a Circle instance
    fn area(&self) -> f64 {
        std::f64::consts::PI * self.radius * self.radius
    }

    // A constructor-like function (often called an 'associated function')
    fn new(radius: f64) -> Circle {
        Circle { radius }
    }
}
```