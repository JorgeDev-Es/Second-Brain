# Matrices
## ¿Qué es una matriz?
Una matriz es un arreglo
## Definición formal
Una matriz es un tensor de rango 2.
## Operaciones con matrices
### Suma de matrices
Al realizar una suma de matrices, las dimensiones deben ser iguales.
$$\begin{bmatrix}a_{11},&a_{12},& \dotsc & a_{1n} \\ \vdots &\ddots& \ddots &\vdots \\ a_{m1}, & \dotsc & \dotsc & a_{mn} \end{bmatrix}$$

Sumar $A + 0 = A$
Multiplicar una matriz por un escalar$0A = 0$
### Multiplicaciones
#### Multiplicación por escalar
#### Multiplicación por vector
### Multiplicación de matrices
## Aplicaciones
### Propagación en redes neuronales
## Representación matricial de un sistema de ecuaciones lineales
### Forma matricial de un sistema de ecuaciones homogéneo
Dado $Ax=b$, sí $b=0$, entonces es un sistema homogéneo $Ax=0$
### Forma matricial de un sistema de ecuaciones no homogéneo
Dado $Ax=b$, sí $b\ne0$, entonces es un sistema no homogéneo.
Si cualquier elemento de $b$ no es 0, se considera un sistema no homogéneo.
$$\begin{bmatrix}0\\\vdots\\b_j\\\vdots\\0\\\end{bmatrix}$$
Sí $b_j\ne0$