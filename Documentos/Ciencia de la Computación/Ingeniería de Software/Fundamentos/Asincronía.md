# Asincronía
## Mejores prácticas
### Evitar efectos secundarios
Aun que no todos los efectos secundarios son malos, pero deben ser intencionales.
❌
```JavaScript
let selectedFile

async function selectFile(path) {
	selectedFile = await readFile(path)
}

await selectFile()
```
✅
```JavaScript
let selectedFile

async function selectFile(path) {
	return await readFile(path)
}

selectedFile = await selectFile(path)
```