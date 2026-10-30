## Inicialización `new`
La manera más rápida
```JavaScript
let arr = [83, 93, 27, 29, 2828]

arr = []
```
## `length = 0`
~6% más lento que `arr = []`
```JavaScript
arr.length = 0
```
## `splice()`
~8% más lento que `arr = []`
```JavaScript
testArray.splice(0, testArray.length);
```
## `pop()`
~26% más lento que `arr = []`
```JavaScript
while (testArray.length > 0) {
  testArray.pop();
}
```
## `shift()`
~88% más lento que `arr = []`
```JavaScript
while (testArray.length > 0) {
  testArray.shift();
}
```