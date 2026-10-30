# Breath of the Wild
## Descripción
La decompilación de The Legend of Zelda: Breath of the Wild (1.5.0).
## Framework y motor
Breath of the Wild es un videojuego lanzado en marzo del 2017 para la Wii U y la Switch. Comparte mucho código con juegos first-party contemporaneos de Nintendo, como Splatoon 2 y Super Mario Odyssey, destacando las librerías [[Documentación/Decompilación/Nintendo Switch/sead/sead|sead]] y NintendoWare.

Breath of the Wild es el primer juego principal de Nintendo en usar XLink (EffectLink y SoundLink) como un sistema para hacer código puente y efectos gráficos o de sonido de manera máß sencilla, y marca tambien el primer uso significante de flujos de evento (mediante la librería EventFlow o evfl).
### Motor
Breath of the Wild usa un motor completamente personalizado, el cuál es conocido como KingSystem. Parece ser escrito desde cero debido a que no comparte nada importante de juegos previos de Zelda o Nintendo. No usa LunchPack o el motor SMO.
### Físicas
El juego se apoya en el motor de físicas Havok para físicas ragdoll, colisiones (Physics2012), navegación (NavMesh), y modelado de ropa. Breath of the Wild no usa la librería KCL de Nintendo.
## Arquitectura
### Código
BotW está escrito en C++ sin casi código ensamblador escrito a mano y sin uso de la librería estándar de C++. Las estructuras estándar como strings o associative maps son implementados en la librería [[Documentación/Decompilación/Nintendo Switch/sead/sead|sead]]. No se usa Standard RTTI, en su lugar el juego se mantiene en la implementación propia de RTTI de la librería [[Documentación/Decompilación/Nintendo Switch/sead/sead|sead]].

El código base parece ser compilado con altos niveles de optimización habilitados para los lanzamientos de Wii U y Switch. A partir de la versión 1.6.0 de Switch, el juego es compilado adicionalmente con LTO habilitado, que resulta en cantidades masivas de código basura.
El juego es dividido en muchos componentes y hace uso pesado de managers, los cuales son singletons que son generalmente responsables re una tarea específica (PlacementMgr para posicionamiento de actores, EventMgr para eventos in-game, etc.). La gran mayoría de managers son dynamically allocated, no almacenados en BSS.
En total, existen 130 subsistemas.
## Sitio web oficial
El sitio web oficial es https://botw.link/.
El repositorio oficial es https://github.com/zeldaret/botw.
## Referencias
https://botw.link/
https://github.com/zeldaret/botw
https://zeldamods.org/wiki/Overview#Framework_and_engine