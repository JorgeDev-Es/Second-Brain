# sead
## ¿Qué es sead?
sead, siglas de Standard EAD Library, es un framework y librería base en C++ desarrollado internamente por Nintendo (originalmente por su división EAD y posteriormente EPD) como una capa de abstracción para su entorno de desarrollo de videojuegos. Proporciona una interfaz unificada a través de diferentes generaciones de hardware y sistemas operativos.

Proporciona estructuras de datos básicas como lo son strings, tree maps y otros componentes esenciales (threads, critical sections, file IO, etc.).
## Propósito
La librería fue diseñada para reemplazar o complementar la STL (Librería Estándar) de C++ con alternativas enfocadas en videojuegos y altamente eficientes en el uso de memoria.

En el desarrollo de consolas con presupuestos estrictos de memoria y tiempo de cuadro, la STL (`std::vector`, `std::string`, `std::function`, `dynamic_cast`, etc.) presenta problemas que sead resuelve:
- **Evita asignaciones dinámicas implícitas**. Evita que elementos como cadenas de texto o functores llamen a `operator new` en el heap global tras bambalinas, previniendo la fragmentación de memoria incontrolable y la contención de bloqueo entre hilos.
- **Control total sobre el Heap de destino**. Intercepta todas las llamadas a `new` y `delete` para redirigirlas a su propio sistema de memoria jerárquico (`sead::Heap`, `ExpHeap` `FrameHeap`), permitiendo especificar en qué heap exacto alojar cada recurso o usar buffers fijos en la pila.
- **Sin excepciones ni RTTI nativo de C++**. Está diseñada desde cero para funcionar sin excepciones (`-fno-exceptions`) y cuenta con su propio sistema ligero de identificación de tipos en tiempo de ejecución (`SEAD_RTTI_BASE` / `sead::RuntimeTypeInfo`) para evitar la sobrecarga de `dynamic_cast`.
## Plataformas y videojuegos
sead abstrae los SDKs específicos de cada consola en una API consistente para que la lógica del juego sea independiente de la plataforma:
- `ctr`. Nintendo 3DS.
- `cafe`. Wii U (Cafe SDK).
- `nin`/`nx`. Nintendo Switch y plataformas modernas soportadas por Nintendo SDK (`nnSdk`).
Debido a que la librería evoluciona con cada lanzamiento importante, utiliza la macro `SEAD_VERSION` para ajustar características y diseños binarios según el juego objetivo.
- _The Legend of Zelda: Breath of the Wild_ (`SEAD_VERSION_BOTW`).
- _Super Mario Odyssey_ (`SEAD_VERSION_SMO`).
- _Splatoon 3_ (`SEAD_VERSION_SPL3`).
- _The Legend of Zelda: Tears of the Kingdom_ (`SEAD_VERSION_TOTK`).
- _Super Mario Bros. Wonder_ (`SEAD_VERSION_SMBW`).
- _Super Mario Maker 2_ (`SEAD_VERSION_SMM2`).
## Arquitectura y módulos principales
En la arquitectura de software de un juego de Nintendo, se ubica justo por encima del SDK del sistema (`NintendoSDK`/`nnheaders`) y sirve como cimiento sobre el cual se construye el motor propio del juego (como `ksys`/KingSystem) y la lógica específica del título (`uking).
Está dividida en 21 módulos principales.
## Referencias
https://github.com/open-ead/sead
https://botw.link/cheatsheet/common-inline-functions/sead