1
```cli
pnpm create vite@latest
```
2
electron - vanilla
3
```
pnpm add -D solid-js vite-plugin-solid
```
4
Create `index.tsx`
```typescript
// index.tsx

/* @refresh reload */

import { render } from "solid-js/web"

import "@master/css"

import "./index.css"

  

import router from "./router.tsx"

  

const root = document.getElementById("root")

  

render(router, root!)
```