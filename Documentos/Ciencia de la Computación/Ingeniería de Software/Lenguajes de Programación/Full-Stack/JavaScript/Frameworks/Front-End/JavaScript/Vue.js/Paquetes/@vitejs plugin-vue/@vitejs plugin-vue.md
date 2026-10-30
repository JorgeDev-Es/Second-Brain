# `@vitejs/plugin-vue`
El paquete `@vitejs/plugin-vue` proporciona soporte para SFC (Single File Components) de Vue 3 dentro de un proyecto de Vite.

```TypeScript
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'

export default defineConfig({
	plugins: [
		vue()
	]
})
```