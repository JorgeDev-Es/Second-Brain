# Naming Conventions
## General principles
### Clarity and conciseness
The name should clearly indicate the variable's purpose. Avoid overly short or cryptic names, but also avoid excessively long names. Strive for a balance that conveys meaning efficiently.
### Descriptive names
En lugar de nombres como `x` o `n`, usar nombres como `counter`, `userName`, etcetera. El nombra debe reflejar el dato que almacena la variable.
### Consistency
Stick to a chosen naming convention throughout your project. Mixing different styles can make the code harder to read.
### Avoid abbreviations
While tempting to shorten names, avoid abbreviations unless they are widely understood within the context of your project.
`userAccountBalance` is generally better than `usrAcctBal`.
### Meaningful names for booleans
Use prefixes like `is`, `has`, `can`, or `should` for boolean variables to clearly indicate their purpose.
`isValid`, `hasItems`, `canEdit`.
## Language specific conventions
Most of programming languages may have their own recommended conventions.
### `snake_case`
Words are separated by underscores and are all lowercase.
This is common in languages like Python, Ruby, and C++.
### `camelCase`
The first word starts with a lowercase letter, and subsequent words are capitalized.
### `kebab-case`
Similar to [[#`snake_case`]], but hyphens are used as separators. Less common for variable names but sometimes used in URLs or filenames.