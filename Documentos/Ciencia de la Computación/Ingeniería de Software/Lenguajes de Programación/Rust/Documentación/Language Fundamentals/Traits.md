# Traits in Rust
Traits are a fundamental concept that allow for polymorphism.
They define a set of methods that can be implemented by different types. When a type implements a trait, it's promising to provide the functionality defined by that trait.

They are similar in concept to interfaces in other languages, though with some distinct differences (like the ability to implement a trait for a type even if you didn't define either the trait or the type, known as the "orphan rule" for external types)/