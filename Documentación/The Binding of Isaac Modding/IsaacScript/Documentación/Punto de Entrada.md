
```js
// This is the entry point for the TypeScriptToLua bundler, which is set in the "tsconfig.json"  
// file. All this file does is immediately execute the "mod()" function in the "mod.ts" file. (We  
// don't want to point the TypeScriptToLua bundler at the "mod.ts" file directly, because this can  
// cause bugs relating to the temporal dead zone.)  
  
import { main } from "./mod"  
  
main()  
  
// Do not add any code to this file! Edit the "mod.ts" file instead.
```