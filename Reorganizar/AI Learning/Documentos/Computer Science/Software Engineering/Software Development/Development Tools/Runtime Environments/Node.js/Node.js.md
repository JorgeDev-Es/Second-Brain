# Node.js
Node.js is a JavaScript runtime environment that executes JavaScript code outside of a web browser.
It's built on Chrome's V8 JavaScript engine, which is known for its performance.
## Introduction to Node.js
Node.js is an open-source and cross-platform JavaScript runtime environment.

Node.js runs the V8 JavaScript engine, the core of Google Chrome, outside of the browser.

A Node.js app runs in a single process, without creating a new thread for every request. Node.js provides a set of asynchronous I/O primitives in its standard library that prevent JavaScript code from blocking and generally, libraries in Node.js are written using non-blocking paradigms, making blocking behavior the exception rather than the norm.

When Node.js performs an I/O operation, like reading from network, accessing a database or the filesystem, instead of blocking the thread and wasting CPU cycles waiting, Node.js will resume the operations when the response comes back.

This allows to Node.js to handle thousands of concurrent connections with a single server without introducing the burden of managing thread concurrency, which could be a significant source of bugs.

Node.js fue creado por Ryan Dahl en 2009 con el objetivo de construir un entorno de ejecución JavaScript del lado del servidor basado en un modelo de eventos asíncronos y no bloqueantes.
La creación de Node.js se basa en una combinación de tecnologías clave, incluidas V8, C++ y libuv, entre otras

La API de HTTP en Node.js realmente utiliza C++ under the hood. Cuando Node.js maneja solicitudes HTTP, internamente utiliza la librería de C++ para interactuar con el sistema operativo y manejar las conexiones de red.