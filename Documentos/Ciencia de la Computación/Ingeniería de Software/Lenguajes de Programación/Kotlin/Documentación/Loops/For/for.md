# `for` loop in Kotlin
The `for` loop 
```Kotlin
// Code example
for (i in 1..5) {
	println(i)
}
```

```Kotlin
// Using `withIndex` library function (more idiomatic)
for ((index, value) in fruits.withIndex()) {
	println("Item at $index is $value")
}
```