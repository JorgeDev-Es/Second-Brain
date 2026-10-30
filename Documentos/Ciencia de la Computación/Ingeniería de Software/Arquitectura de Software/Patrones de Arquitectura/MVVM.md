# Arquitectura MVVM
## ¿Qué es la arquitectura MVVM?
MVVM es un patrón de arquitectura para aplicaciones UI que separa la interfaz de usuario de la lógica y los datos.

Hay tres componentes fundamentales: el modelo, la vista, y la vista del modelo.
![[Archivos Adjuntos/Pasted image 20250819200105.png]]
## Beneficios
- La vista del modelo actua como un adaptador para las clases del modelo y previene hacer cambios grandes al código del modelo.
- Los desarrolladores pueden crear tests unitarios para la vista del modelo y del modelo, sin usar la vista.
## ¿Dónde se utiliza la arquitectura MVVM?
### Referencias
https://keepcoding.io/blog/que-es-el-patron-de-arquitectura-mvvm/