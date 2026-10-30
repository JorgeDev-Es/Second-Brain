# For Loop
## `for...in`
`for...in` is used to iterate over items in a collection that implements the `IntoIterator` trait. This trait defines a way to create an iterator from a collection. Iterators are responsible for producing a sequence of values.
### Basic syntax
```Rust
for item in collection {

}
```
### How it works
- When a `for...in` loop starts, the `into_iter()` method of the `IntoIterator` trait is called on the `collection`. This method consumes the collection (or borrows it, depending on the type and how you're using it) and returns an iterator.
- The iterator then produces a sequence of items.
- In each iteration of the loop, the `next()` method of the iterator is called. This method returns an `Option<Item>`, where `Item` is the type of the elements in the collection.
    - If `next()` returns `Some(value)`, the `value` is assigned to the `item` variable, and the code inside the loop body is executed.
    - If `next()` returns `None`, it signifies that the iterator has reached the end of the sequence, and the loop terminates.
## Looping with a counter
## Iterating with index and value
## Iterating in reverse
## Iterating over the keys and values of a `HashMap`
## Iterating over the Elements of a `HashSet`