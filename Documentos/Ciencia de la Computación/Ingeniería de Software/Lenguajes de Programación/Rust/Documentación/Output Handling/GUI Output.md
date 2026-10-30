# GUI Output
Rust doesn't have a built-in, standard GUI framework like how web browsers natively understand and render HTML, CSS and JavaScript.

Instead, you use external libraries (crates) specifically designed for GUI development. These libraries are written using Rust's core features (functions, enums, structs, `impl`, traits, macros, etc.), but they provide higher-level abstractions and components that make GUI development possible.

For example, using `iced` crate you are not directly writing code to draw pixels or handle raw window messages. Instead, you are using the API provided by the `iced` library, which is built using Rust's core features like:
- `struct`: To define your application's state (`Example` holds the `radius`).
- `enum`: To represent messages or events that the UI generates (`Message::RadiusChanged`).
- `impl`To define the behavior and logic of your application, including how to handle messages (`update`) and how to construct the user interface based on the current state (`view`).
- Functions and methods from the crate's module: Like `column!`, `slider`, `text`, `center`, `.padding()`, `.spacing()`, etc., which are the building blocks and layout tools provided by the `iced` library.
In Rust with a GUI crate, you define all these aspects (state, event handling, UI structure, and appearance/layout) within your Rust code using the crate's API, 