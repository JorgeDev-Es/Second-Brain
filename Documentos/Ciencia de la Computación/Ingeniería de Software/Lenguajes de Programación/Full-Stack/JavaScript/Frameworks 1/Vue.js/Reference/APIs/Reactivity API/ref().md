# `ref()`
Takes an inner value and returns a reactive and mutable ref object. The ref object has a single property `.value` that points to the inner value.

If an object is assigned as a ref's value, the object is made deeply reactive by the reactive method.