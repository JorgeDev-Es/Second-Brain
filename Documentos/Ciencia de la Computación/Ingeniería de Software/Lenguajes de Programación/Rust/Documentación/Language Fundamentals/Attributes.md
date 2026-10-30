# Attributes
Attributes are a form of metadata that you can apply to code items (like functions, structs, modules, crates, etc.) using `#[...]` or `#[...]`. They provide instructions or information to the compiler, linting tools, build scripts, or other aspects of the Rust ecosystem.

`#[attribute]` applies to the item that immediately follows the attribute (e.g., a struct, a function).

`#[attribute]` applies to the item that contains the attribute, typically used at the crate or module level )e.g., the whole crate or a specific module).

`#[attribute]` for outer attributes and `#![attribute]` for inner attributes.