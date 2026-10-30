# `HTTP`
The `HTTP` module c

This module can be imported via `import * as http from 'node:http`

The HTTP interfaces in Node.js are designed to support many features of the protocol which have been traditionally difficult to use. In particular, large, possibly chunk-encoded, messages. The interface is careful to never buffer entire requests or responses, so the user is able to stream data.

In order to support the full spectrum of possible HTTP applications, the Node.js HTTP API is very low level. It deals with stream handling and message parsing only. It parses a message into headers and body but it does not parse the actual headers or the body.

La API de HTTP en Node.js realmente utiliza C++ under the hood. Cuando Node.js maneja solicitudes HTTP, internamente utiliza la librería de C++ para interactuar con el sistema operativo y manejar las conexiones de red.