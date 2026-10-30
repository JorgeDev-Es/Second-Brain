# Variables
## Variable bindings
When you use the `let` keyword to introduce a name and associate it with a value, you are creating a **variable binding**.
Rust uses the term "binding" to emphasize that the name is bound to a specific value (and its associated type, ownership, and mutability) within a certain scope.
In many other languages, this would simply be called declaring and initializing a variable.

## `const`
3. Type annotation: When declaring a `const`, you must explicitly specify its type. For `let`, the compiler can often infer the type (though you can provide explicit annotations if you wish).
## `let`, `const` and `mut`
In Rust, variables are declared using the `let` keyword. By default, bindings created with let are immutable. This means that once a value is assigned to a variable declared  with just `let`, you cannot reassign a different value to it.
```Rust
let x = 5;
println!("The value of x is: {}, x");

/* !!! */ x = 10; // $> error[E0384]: cannot assign twice to immutable variable 'x'.
```

`const` is used for values that are fixed and known at compile time. They are typically used for hardcoded values that won't change throughout the program's execution, often representing fundamental constants or configuration values.
## Shadowing
