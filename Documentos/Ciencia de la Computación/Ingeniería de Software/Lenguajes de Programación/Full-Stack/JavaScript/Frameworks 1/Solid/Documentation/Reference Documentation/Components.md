# Components
Components are functions that accept a props object and return JSX elements including native DOM elements and other components.

```TypeScript
// MyComponent.tsx
export default function MyComponent(props) {
return <div>Hello {props.name}</div>
}
```

```TypeScript
// App.tsx

export default function App () {
	return (
		<>
			<MyComponent name="Solid">
		</>
	)
}
```

Components are lightweight in that they are not stateful themselves and have no instances. Instead, they serve as factory functions for DOM elements and reactive primitives.