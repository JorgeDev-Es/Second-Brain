# Variables in Kotlin
```Kotlin
// This code must reside within an executable context.
val num = 5

var customers = 8
println(customers) // $> 8
```
## `val`
`val` is used to declare **read-only variables**.
## `var`
`var` is used to declare **mutable variables**.

---
Variables can be declared outside the `main()` function at the beginning of your program. Variables declared in this way are said to be declared at **top level**.

Es altamente recomendable declarar todas las variables as **read-only (`val`)** by default. Declare mutable variables (var) only if necessary.