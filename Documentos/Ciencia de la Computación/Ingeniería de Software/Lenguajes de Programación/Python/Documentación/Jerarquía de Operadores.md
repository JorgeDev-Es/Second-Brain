# Jerarquía de Operadores en Python
## Ejemplo 1
$$5 - \frac{2}{4}\times\frac{3}{5}= 4.7$$

```Python
equation1 = 5 - ((2 / 4) * (3 / 5))
equation2 = 5 - (2 / 4) * (3 / 5)
equation3 = 5 - 2 / 4 * 3 / 5

print(equation1) # Output> 4.7
print(equation2) # Output> 4.7
print(equation3) # Output> 4.7
```
### Ejemplo 2
$$\frac{4-5}{3+5\times6}= -0.0303...$$
```Python
equation1 = (4 - 5) / (3 + (5 * 6))
print(equation1) #✅ Output> -0.0303...

equation2 = (4 - 5) / (3 + 5 * 6)
print(equation2) #✅ Output> -0.0303...

equation3 = 4 - 5 / (3 + 5 * 6)
print(equation3) #❌ Output> 3.8484...

equation4 = (4 - 5) / 3 + 5 * 6
print(equation3) #❌ Output> 29.6666...

equation5 = 4 - 5 / 3 + 5 * 6
print(equation3) #❌ Output> 32.3333...
```