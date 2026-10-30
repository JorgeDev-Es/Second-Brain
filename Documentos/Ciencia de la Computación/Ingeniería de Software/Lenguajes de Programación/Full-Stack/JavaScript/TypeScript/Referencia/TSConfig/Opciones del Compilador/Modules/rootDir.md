
# Opción `rootDir` de TSConfig
## Descripción
Cuando TypeScript compila archivos, mantiene la misma structura de archivos en el directorio de salida tal como existe en el directorio de entrada

```dirtree

- MyProject
	- tsconfig.json
	- core
		- a.ts
		- b.ts
		- /sub
		  - c.ts
		- types.d.ts
```

