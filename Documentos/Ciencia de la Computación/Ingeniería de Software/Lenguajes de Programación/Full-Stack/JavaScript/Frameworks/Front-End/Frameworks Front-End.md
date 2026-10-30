# Frameworks Front-End de JavaScript
## ¿Qué es un framework de JavaScript?
En proyectos pequeños, el rendimiento entre los frameworks front-end es extremadamente similar.
### JavaScript Vanilla vs Frameworks Front-End
Usar JavaScript Vanilla ofrece control total, sin embargo, ese control total viene con la advertencia de que debes ser tú el que haga todo, el DOM, el enrutado, el estado, etc.
## ¿Qué se busca resolver con un framework Front-End?
### ¿Cómo funciona internamente?
Una de las principales características de un framework de JavaScript es abstraer la manipulación del DOM

#### Ejemplos
##### Creación de un elemento y añadirlo a la aplicación
JavaScript
```JavaScript
const element = document.getElementById('app');
const p = document.createElement('p');
p.textContent = 'Hola desde VanillaJS';
element.appendChild(p);
```
JSX
```JSX
function App() {
  return (
    <div>
      <p>Hola desde JSX en React</p>
    </div>
  );
}
```
##### Crear un botón y añadir un evento
```JavaScript
const btn = document.createElement('button');
btn.textContent = 'Click me';
btn.addEventListener('click', () => alert('Clicked!'));
document.body.appendChild(btn);
```
JSX
```JSX
function Button() {
  return <button onClick={() => alert('Clicked!')}>Click me</button>;
}
```
##### Estado
JavaScript
JSX
```JSX
function Counter() {
  const [count, setCount] = React.useState(0);
  return <button onClick={() => setCount(count + 1)}>{count}</button>;
}
```
### Rendimiento
React 19, el cuál es un framework que se considera "lento" debido a su evolución, realiza alrededor de 52 mil operaciones por segundo, no es necesario preocuparte por el rendimiento si el proyecto no realiza tantas operaciones, por lo que no tienes porque preocuparte por cuál framework elegir por rendimiento, sino por el cuál te sientas más cómodo usando.

Los benchmarks de frameworks front-end suelen enfocarse en las operaciones de actualización de DOM, debido a que estos frameworks se crearon con el propósito de reducir la cantidad de actualizaciones del DOM debido a lo pesadas que son. Una aplicación normal realiza alrededor de decenas o cientos de cambios por segundo, no miles. Por ello, incluso el framework más "lento" es más que suficiente en la mayoría de los casos.
### Minificación
Los frameworks front-end suelen realizar un proceso de compilación, pero no una compilación nativa donde se genera código máquina, sino que todos los archivos .js, .ts, .vue, .jsx, .css, etc., se convierten en unos pocos archivos para reducir los ficheros de código final, reducir el tempo de carga, aumentar la seguridad del código fuente, optimizar los assets, etc.
También se puede conocer como empaquetado o minificación.
## ¿Qué arquitecturas de diseño utilizan?
### Programación declarativa
### Component-Based Architecture
### Virtual DOM y Reconcilización
### Unidirectional Data Flow
### Hooks y composición sobre herencia
### Patrón de estado global
## ¿Cómo es el proceso de compilación de los frameworks front-end?
## Referencias
https://dev.to/hamzakhan/javascript-framework-showdown-react-vs-vue-vs-solidjs-in-2025-hpc
https://lab.wallarm.com/what/que-es-la-minificacion-y-por-que-es-necesaria/?lang=es