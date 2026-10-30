# OxLint
## ¿Qué es OxLint?
OxLint es un linter para JavaScript y TypeScript construido en el stack de Oxc.
## Instalación
La instalación recomendada se encuentra en el sitio web oficial https://oxc.rs/docs/guide/usage/linter/quickstart.html#install.
## Guía rápida
Tras haber instalado `oxlint` como una dependencia de desarrollo, agregas los comandos necesarios al `package.json`
```json
{
  "scripts": {
    "lint": "oxlint",
    "lint:fix": "oxlint --fix"
  }
}
```
## Referencias
https://oxc.rs/docs/guide/usage/linter