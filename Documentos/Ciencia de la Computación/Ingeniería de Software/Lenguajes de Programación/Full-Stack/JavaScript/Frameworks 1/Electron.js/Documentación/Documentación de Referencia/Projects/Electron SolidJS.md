```PowerShell
pnpm create vite@latest
```

```PowerShell
pnpm add -D solid-js vite-plugin-solid
```

```TypeScript
// vite.config.ts
import solid from 'vite-plugin-solid'

export default defineConfig({
	plugins: [
		...,
		solid()
	]
})
```