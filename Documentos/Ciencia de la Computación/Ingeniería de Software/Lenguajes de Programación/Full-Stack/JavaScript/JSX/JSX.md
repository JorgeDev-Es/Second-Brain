# JSX
## ¿Qué es JSX?
JSX, siglas de JavaScript XML, es una extensión de JavaScript que permite la creación de árboles DOM usando una sintaxis similar a XML.

Herramientas como Babel, Vite, etc., convierten el código JSX en código JavaScript que el navegador puede entender.
```JavaScript
// JSX
const elemento = (
  <div className="saludo">
    <h1>Hola Mundo</h1>
    <p>Aprendiendo React</p>
  </div>
);
```

```JavaScript
// JavaScript
const elemento = React.createElement(
  "div",
  { className: "saludo" },
  React.createElement("h1", null, "Hola Mundo"),
  React.createElement("p", null, "Aprendiendo React")
);
```
## Referencias
https://es.wikipedia.org/wiki/JSX_(JavaScript)