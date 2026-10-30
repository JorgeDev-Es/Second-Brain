# Observer Pattern
## Behavioral design pattern
Observer pattern primarily focuses on how objects interact with each other and how responsibilities are distributed among them.
## Combine Observer Pattern with Adapter Pattern
The common scenario for combining these two patterns is when you have:
1. A subject that expects so communicate with objects that implement its `Observer` interface.
2. An existing class (the Adaptee) that you want to be notified by the Subject, but it doesn't implement the `Observer` interface. It has its own, different method signature for receiving notifications.
## Observer Pattern vs Callback
A callback is essentially a function that's passed as an argument to another function, to be executed later.

The callbacks are useful when:
- **Single Subscriber:** When there's only one specific piece of code that needs to react to an event or result.
- **Simple, Direct Reaction:** When the reaction is straightforward and tightly coupled to the initial operation.
- **Asynchronous Operations:** Very common in JavaScript for handling the result of an async task (e.g., fetching data, file operations).
- **One-off Events:** For events that happen once or don't require a persistent subscription model.
### Limitations of callbacks
Callbacks has some limitations, and it's there where Observer shines.
- **Tight Coupling:** The `SomeUtility` class (or `MusicScanner` in your original code) directly knows about and calls the specific callback function. If you want a _second_ part of your application to also react to `doSomething` finishing, you'd have to modify `doSomething` to call _another_ callback, or restructure it to accept an array of callbacks, which starts to resemble the Observer pattern anyway.
    
- **Scalability Issues:** As the number of things that need to react grows, managing multiple callbacks becomes messy.
    
- **Lack of Flexibility for New Reactions:** Adding a new reaction means modifying the original function.
    
- **No Unsubscription:** Callbacks typically don't offer a built-in way to "unsubscribe" once registered.

## When do you need