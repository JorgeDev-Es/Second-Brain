# `type` keyword in TypeScript

The `type` keyword in TypeScript is used to create **type aliases**. A type alias is a new name for an existing type. This doesn't create a new, distinct type; it simply provides an alternative name for a type. You can use type aliases to define:

1. **Primitive types:** Give a more descriptive name to basic types like `string`, `number`, `boolean`.
    
    TypeScript
    
    ```
    type Username = string;
    let myUsername: Username = "TypeScriptDev";
    ```
    
2. **Object types:** Define the shape of an object. This is one of the most common and powerful uses, especially for complex object structures.
    
    TypeScript
    
    ```
    type Point = {
      x: number;
      y: number;
    };
    
    function printCoordinates(pt: Point) {
      console.log(`The coordinates are (${pt.x}, ${pt.y})`);
    }
    
    printCoordinates({ x: 10, y: 20 });
    ```
    
3. **Union types:** Combine multiple types, indicating that a variable can be one of several types.
    
    TypeScript
    
    ```
    type ID = number | string;
    
    function printID(id: ID) {
      console.log(`My ID is: ${id}`);
    }
    
    printID(101);
    printID("abc-123");
    ```
    
4. **Intersection types:** Combine multiple types, indicating that a variable must have all the properties of all combined types.
    
    TypeScript
    
    ```
    type Draggable = {
      drag: () => void;
    };
    
    type Resizable = {
      resize: () => void;
    };
    
    type UIElement = Draggable & Resizable;
    
    const button: UIElement = {
      drag: () => console.log("Dragging..."),
      resize: () => console.log("Resizing..."),
    };
    ```
    
5. **Tuple types:** Define an array with a fixed number of elements where each element has a known type.
    
    TypeScript
    
    ```
    type RGBColor = [number, number, number];
    
    const red: RGBColor = [255, 0, 0];
    ```
    
6. **Function types:** Describe the signature of a function.
    
    TypeScript
    
    ```
    type GreeterFunction = (name: string) => string;
    
    const greet: GreeterFunction = (name) => `Hello, ${name}!`;
    console.log(greet("Alice"));
    ```
    
7. **Generic types:** Create type aliases that can work with different types by using type parameters.
    
    TypeScript
    
    ```
    type Pair<T, U> = [T, U];
    
    const stringAndNumber: Pair<string, number> = ["hello", 123];
    ```
    

**Key Characteristics of `type` aliases:**

- **No new type creation:** As mentioned, `type` aliases don't create new types; they just provide new names for existing ones. This means they cannot be implemented or extended by classes or interfaces.
- **Cannot be `implements` or `extends`:** Unlike `interface`, a `type` alias cannot be used in `implements` or `extends` clauses.
- **Can represent any type:** You can alias primitive types, union types, intersection types, tuple types, and even other type aliases.
- **Useful for complex types:** They help make complex type signatures more readable and reusable by giving them a simple name.
- **Recursive types:** Type aliases can refer to themselves, which is useful for representing tree-like data structures.
    
    TypeScript
    
    ```
    type LinkedList<T> = T & { next: LinkedList<T> | null };
    
    // Example usage (simplified)
    const node1: LinkedList<number> = { value: 1, next: null };
    const node2: LinkedList<number> = { value: 2, next: node1 };
    ```
    

**When to use `type` vs. `interface`:**

While there's often overlap, here's a general guideline:

- **Use `interface` for defining the shape of objects, especially when you expect them to be extended or implemented by classes.** Interfaces are better for "contract" definitions.
- **Use `type` for anything else.** This includes primitive aliases, union types, intersection types, tuples, and function signatures. `type` is more flexible for non-object type definitions.