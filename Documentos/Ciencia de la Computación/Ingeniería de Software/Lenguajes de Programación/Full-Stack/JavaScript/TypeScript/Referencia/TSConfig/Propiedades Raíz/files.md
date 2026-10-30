# Opción `files` de TSConfig
## Descripción
Específica una lista de archivos para incluir en el programa. Ocurrirá un error si cualquiera de estos archivos no puede ser encontrado.

Es util cuando tienes un pequeño número de archivos y no necesitas usar un glob para referencias múltiples archivos. Si esto es lo que necesitas, usa `include`

```JSON
{
	"files": [
		"core.ts",
	    "sys.ts",
	    "types.ts",
	    "scanner.ts",
	    "parser.ts",
	    "utilities.ts",
	    "binder.ts",
	    "checker.ts",
	    "tsc.ts"
	    ]
}
```