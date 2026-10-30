## Good practices
### **Single Responsibility Principle (SRP)**

- **Practice:** Each function should do one thing, and do it well.
- **Why it's good:** Makes functions easier to understand, test, and maintain. If a function tries to do too many things, it becomes complex and brittle.
- **Example:**
    - **Bad:** A `processOrder` function that validates input, calculates total, saves to database, and sends email.
    - **Good:** Separate functions like `validateOrder`, `calculateOrderTotal`, `saveOrderToDatabase`, `sendOrderConfirmationEmail`, and then an orchestrator function `processOrder` that calls these smaller ones.

### 2. **Descriptive Naming**

- **Practice:** Function names should clearly describe what the function _does_ (usually a verb phrase), and parameter names should clearly describe their purpose.
- **Why it's good:** Improves readability and understanding without needing to read the function body.
- **Examples:**
    - `calculateAverage` instead of `avg` or `processData`.
    - `getUserProfile(userId: string)` instead of `get(id: string)`.

### 3. **Type Safety (TypeScript Specific)**

- **Practice:** Always explicitly declare parameter types and function return types. Avoid `any` whenever possible.
- **Why it's good:** TypeScript's static type checking catches errors at compile time, preventing many runtime bugs. It also acts as self-documentation.
- **Example:**
    
    TypeScript
    
    ```
    // Bad (missing return type, implicit 'any' possible if not careful)
    function calculateTotal(items, discount) { /* ... */ }
    
    // Good
    function calculateTotal(items: { price: number; quantity: number }[], discount: number): number { /* ... */ }
    ```
    

### 4. **Handle Edge Cases Gracefully**

- **Practice:** Anticipate unusual or extreme inputs and ensure the function behaves predictably.
- **Why it's good:** Prevents runtime errors and makes your code robust. Common edge cases include:
    - Empty arrays/collections (`[]`)
    - Null or undefined values (`null`, `undefined`)
    - Zero (`0`)
    - Negative numbers (if applicable)
    - Empty strings (`""`)
- **Example (from your original code):**
    
    TypeScript
    
    ```
    function getAverage(scores: number[]): number {
        if (scores.length === 0) {
            return 0; // or throw new Error("Cannot calculate average of an empty array.");
        }
        // ... rest of the logic
    }
    ```
    

### 5. **Validate Inputs**

- **Practice:** If a function expects inputs in a specific format or within a certain range, validate them at the beginning of the function.
- **Why it's good:** Prevents invalid data from propagating through your system, leading to harder-to-debug issues later. Can use `if` checks or guard clauses.
- **Example:**
    
    TypeScript
    
    ```
    function setTemperature(temp: number): void {
        if (temp < -273.15) { // Absolute zero
            throw new Error("Temperature cannot be below absolute zero.");
        }
        // ... set temperature
    }
    
    function processUserId(id: string): void {
        if (!id || id.trim() === '') {
            throw new Error("User ID cannot be empty.");
        }
        // ...
    }
    ```
    

### 6. **Consistent Return Values**

- **Practice:** A function should always return the expected type, even in error or edge cases. If it returns nothing, declare `void`.
- **Why it's good:** Consumers of your function know exactly what to expect, reducing boilerplate error checking for valid results.
- **Example:** If a function can't find a user, return `null` or `undefined` (and document it), rather than sometimes throwing an error and sometimes returning an object.

### 7. **Avoid Side Effects (Prefer Pure Functions)**

- **Practice:** Ideally, functions should be "pure":
    - Given the same inputs, they always return the same output.
    - They don't cause any observable side effects (e.g., modifying global variables, logging to console, making network requests, changing external state).
- **Why it's good:** Pure functions are easier to test, debug, and reason about. They lead to more predictable and robust code. While not all functions can be pure, strive for it where possible.
- **Example:**
    - **Impure:** `function addProduct(product: Product): void { products.push(product); }` (modifies `products` array outside its scope)
    - **Pure:** `function createNewArrayWithProduct(products: Product[], newProduct: Product): Product[] { return [...products, newProduct]; }` (returns a new array, doesn't modify the original)

### 8. **Parameter Order and Limit**

- **Practice:**
    - Place required parameters before optional ones.
    - Limit the number of parameters (ideally 0-3). If a function needs many parameters, consider grouping them into an object.
- **Why it's good:** Improves readability and makes function calls less error-prone. Object parameters are more flexible for future changes.
- **Example:**
    
    TypeScript
    
    ```
    // Bad
    function createUser(name: string, age: number, email: string, isActive: boolean, role: string, department: string): User { /* ... */ }
    
    // Good
    interface UserOptions {
        name: string;
        age: number;
        email: string;
        isActive?: boolean; // Optional
        role?: string;
        department?: string;
    }
    function createUser(options: UserOptions): User { /* ... */ }
    ```
    

### 9. **Use Constants and Enums**

- **Practice:** Avoid "magic strings" or "magic numbers" in your function logic. Define constants or use enums for fixed values.
- **Why it's good:** Improves readability, makes code easier to modify (change constant in one place), and reduces typos.
- **Example:**
    
    TypeScript
    
    ```
    // Bad
    function processStatus(status: string): void {
        if (status === "pending") { /* ... */ }
    }
    
    // Good
    enum OrderStatus {
        Pending = "pending",
        Shipped = "shipped",
        Delivered = "delivered",
        Cancelled = "cancelled"
    }
    function processStatus(status: OrderStatus): void {
        if (status === OrderStatus.Pending) { /* ... */ }
    }
    ```
    

### 10. **Comments and Documentation (JSDoc)**

- **Practice:** Use JSDoc comments to explain what a function does, its parameters, return values, and any side effects or important considerations.
- **Why it's good:** Essential for team collaboration and for your future self. Tools can generate documentation from JSDoc comments.
- **Example:**
    
    TypeScript
    
    ```
    /**
     * Retrieves a user by their ID from the database.
     * @param userId The unique identifier of the user.
     * @returns A Promise that resolves to the User object, or null if not found.
     * @throws {Error} If there's a database connection issue.
     */
    async function getUserById(userId: string): Promise<User | null> { /* ... */ }
    ```
    

### 11. **Error Handling Strategy**

- **Practice:** Decide on a consistent strategy for handling errors (e.g., throwing exceptions, returning `null`/`undefined`, returning `Result` objects).
- **Why it's good:** Makes your error handling predictable and easier for calling code to implement.
- **Example:**
    - **Throwing errors:** For truly exceptional, unrecoverable situations.
    - **Returning `null`/`undefined`:** For expected "not found" or "no result" scenarios.
    - **Returning `Result` objects:** For more explicit error reporting (e.g., `{ success: boolean, data?: T, error?: Error }`).

### 12. **Early Exit / Guard Clauses**

- **Practice:** Handle error conditions or edge cases at the beginning of the function using `if` statements that return early or throw errors.
- **Why it's good:** Reduces nesting, improves readability, and keeps the main logic path clear.
- **Example:**
    
    TypeScript
    
    ```
    function processData(data: any[]): void {
        if (!data || data.length === 0) {
            console.warn("No data to process.");
            return; // Early exit
        }
        // ... main processing logic here (not nested)
    }
    ```
    

### 13. **Immutability (Preferring `const`)**

- **Practice:** Use `const` for variables whose values don't change. When modifying data structures (like arrays or objects), prefer creating new ones rather than mutating existing ones.
- **Why it's good:** Reduces unexpected side effects, makes code easier to reason about, and simplifies debugging.
- **Example:**
    
    TypeScript
    
    ```
    // Bad (modifies original array)
    function addToArray(arr: number[], value: number): void {
        arr.push(value);
    }
    
    // Good (creates a new array)
    function createNewArrayWithAddedValue(arr: number[], value: number): number[] {
        return [...arr, value];
    }
    ```
Creating effective and maintainable functions is a cornerstone of good programming. In TypeScript, types aren't just a safety net; they're a powerful tool that enhances design principles like the **Single Responsibility Principle (SRP)**.

### How Types Support the Single Responsibility Principle

**Yes, types absolutely support SRP!** Here's how:

1. **Clear Purpose Definition:** By explicitly defining a function's **inputs (parameters)** and **outputs (return type)** with specific types, you're creating a clear "contract" for what that function does. If your function is typed to take an `Order` and return a `number` (the total), it clearly signals that its job is to _calculate the order total_. Should you find yourself needing to add parameters or logic for "sending an email" to this same function, the type system will subtly (or not so subtly!) tell you that you're adding responsibilities beyond its original, clear contract.
    
2. **Action Restriction:** Types constrain what you can do _inside_ the function. If a parameter is a `ReadOnlyArray<string>`, TypeScript won't let you modify that array, nudging you towards returning a new array if transformation is needed. This promotes **pure functions** and prevents unintended side effects.
    
3. **Custom Types and Interfaces:** Defining interfaces (`interface User { id: string; name: string; }`) creates structured data. If your function works with a `User` type, it's less likely to accidentally manipulate `Order` data, as the types guide you. This promotes **cohesion** and separation of concerns.
    
4. **Early Infraction Detection:** TypeScript's compiler acts as your first line of defense. If you try to make a function do something outside its typed contract, the compiler will flag it immediately, before runtime, pushing you to refactor and split responsibilities earlier.
    

In essence, types force you to be **explicit** about a function's role, naturally guiding you toward functions with clear, well-defined, and singular responsibilities.

---

## The Right Steps to Create Good Functions

Here's a logical sequence for building robust and well-designed functions, heavily supported by TypeScript:

### 1. Define Responsibility and Contract (Inputs & Outputs)

- **Ask yourself:** "What _single thing_ should this function do?"
    
- **Identify Inputs (Parameters):** What data does it need? What are their types? Are any optional?
    
    - **TypeScript's Role:** Explicitly declare parameters with their types (`paramName: Type`).
- **Identify Output (Return Type):** What result does it produce? What's its type? Does it return `void` (nothing) if its purpose is a side effect?
    
    - **TypeScript's Role:** Explicitly declare the return type (`): ReturnType {`).
    
    _Example:_
    
    TypeScript
    
    ```
    function calculateTotalPrice(items: Product[], taxRate: number): number {
        // ... logic goes here
    }
    ```
    

### 2. Implement Function Body (Core Logic)

- **Write the Core Logic:** This is where the function performs its single responsibility.
- **Use `const` and Intermediate Types:** Declare variables with `const` for immutability and let TypeScript infer types, or explicitly declare them for clarity.
- **TypeScript's Role:** The compiler guides you if you try to use non-existent properties or assign incorrect types, and ensures your return value matches the declared `ReturnType`.

### 3. Handle Edge Cases and Validations

- **Identify Edge Cases:** Think about unusual or extreme inputs (empty arrays, `null`/`undefined` values, zero, negative numbers, empty strings, etc.).
    
- **Implement Validations (Guard Clauses):** Add checks at the _beginning_ of the function. If inputs are invalid or an edge case applies, decide whether to:
    
    - **Throw an Error:** For truly exceptional, unrecoverable situations.
    - **Return a Default Value:** For predictable behavior in a "not ideal" but valid scenario (e.g., `0` for an empty array's average).
    - **Return `null`/`undefined`:** To signify "not found" or "not applicable."
- **TypeScript's Role:** While TypeScript ensures type correctness, it can't validate _values_ (e.g., a positive number). This is where runtime logic is crucial. However, by declaring return types like `User | null`, TypeScript forces consuming code to handle possible `null` values.
    
    _Example:_
    
    TypeScript
    
    ```
    function getAverage(scores: number[]): number {
        if (scores.length === 0) { // Handles the empty array edge case
            return 0;
        }
        // ... rest of the logic
    }
    ```
    

### 4. Documentation and Comments

- **Add JSDoc:** Essential for explaining the function's purpose, parameters, return values, side effects, or crucial considerations.
- **Complex Logic Comments:** Use comments to explain _why_ a complex piece of logic exists, not just _what_ it does.
- **TypeScript's Role:** IDEs leverage JSDoc for auto-completion and pop-up descriptions.

### 5. Refactor and Test

- **Review SRP:** Is the function still doing only one thing? If not, split it.
- **Simplify:** Can the logic be more concise (e.g., using array methods)?
- **Unit Tests:** Write tests for normal cases and all identified edge cases.
- **TypeScript's Role:** Refactoring is much safer with TypeScript, as the compiler helps prevent breaking changes due to type mismatches.

---

### When to Comment on Edge Cases?

The goal is **self-documenting code**. Clear variable names, logical control flow, and good modularity often make code obvious. However, for **edge cases and validations**, the need for comments is nuanced:

- **Simple, Obvious Validations:** Often require no comments. An `if (array.length === 0)` check is usually clear enough on its own.
- **Complex or Non-Obvious Validations:** **Yes, consider a comment.** If the condition is intricate, involves specific domain rules, or prevents a non-obvious problem, a comment explaining the _why_ or the _problem prevented_ adds significant value.
- **Specific Error Handling Decisions:** When you choose to throw an error rather than return a value, or if the error message itself is key, a comment explaining the _intention_ or _impact_ can be helpful.
## Recommended Logical Order for Functions

Think of your function as a small, efficient machine. For it to work flawlessly, it needs to ensure it's receiving valid input, then perform its core task, and finally deliver the expected result. This logical flow helps create robust, readable, and maintainable code.

Here's the recommended order:

### 1. Validations and Edge Cases (Guard Clauses)

This is the **first and most critical step**. Before your function attempts any core operations, it must confirm that its inputs are valid and that it's in a state to operate correctly.

- **What to do:**
    - **Verify parameters:** Are they present? Are their values acceptable (e.g., non-negative, within a valid range)? (TypeScript handles types, but not values).
    - **Handle error conditions:** Are there situations that prevent the function from fulfilling its purpose (e.g., division by zero, empty arrays, insufficient permissions)?
    - **"Early Exits":** If an error or common edge case is met, the function should **exit immediately**. This could involve returning a default value (like `0`, `[]`, or `null`) or throwing an error.
- **Why it's important:** Ensures **robustness** by preventing runtime errors, keeps the main logic clean by handling "bad" conditions upfront, and improves **efficiency** by avoiding unnecessary computations.

---

### 2. Data Preparation (Optional)

Sometimes, the main logic needs data in a specific format or requires some preliminary transformations.

- **What to do:**
    - Perform **light transformations** like type conversions, string reformatting, filtering irrelevant elements, or sorting arrays.
    - **Initialize variables** that will be used in the core logic.
- **Why it's important:** **Simplifies the core logic** by providing it with ready-to-use data, making that section more focused and readable.

---

### 3. Core Function Logic

This is where your function performs the primary task it was designed for. It's the "heart" of your function.

- **What to do:**
    - Implement the **central algorithm**.
    - Perform calculations.
    - Manipulate data structures.
    - Call any necessary helper functions (if your main function delegates smaller sub-tasks).
- **Why it's important:** This section should embody the function's **single responsibility**. If it becomes too large or complex, it's a strong indicator that the function might be doing too much and needs to be broken down.

---

### 4. Result Construction and Return

Finally, the function assembles and delivers the value it promised in its return type.

- **What to do:**
    - Format the **final output**.
    - Create new objects or arrays if the function is "pure" (meaning it doesn't modify input data).
    - Return the calculated value or the operation's outcome.
- **Why it's important:** Fulfills the function's **contract** and ensures the output is always in the expected format for the calling code.