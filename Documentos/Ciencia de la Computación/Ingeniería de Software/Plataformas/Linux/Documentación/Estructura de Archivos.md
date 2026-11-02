# Estructura de Archivos en Linux
La estruct
## Directorio Raíz `/`
El directorio raíz contiene todos los archivos y directorios en Linux. Toda ruta absoluta de cualquier archivo o directorio se basa en la raíz (`/home/user/documents`, `usr/share`, etc.)
## Binarios `/bin`
El directorio `bin` contiene todos los archivos ejecutables de muchos comandos básicos de Linux, como ls, cp, cd, etc.
La mayoría de los programas en formato binario estan aquí y son accesibles para todos los usuarios del sistema Linux.
## Archivos de dispositivos `/dev`
El directorio `/dev` solo contiene archivos especiales,  incluidos los relativos a los dispositivos. Son archivos virtuales, no están físicamente en el disco.
Por ejemplo:
- `/dev/null` Puede ser enviado para destruir cualquier archivo o cadena.
- `/dev/zero`: Contiene una secuencia infinita de 0s.
- `/dev/random`: Contiene una secuencia infinita de valores aleatorios.
## Archivos de configuración `/etc`
El directorio `/etc` contiene los archivos de configuración principales del sistema, utilizados principalemente por el administrador y los servicios, como el arrchivo de contraseñas y los archivos de red.

Si se necesita hacer cambios en la configuración del sistema.
## Binarios de usuario y datos de programa
El directorio `/usr` contiene todos los archivos ejecutables, las bibliotecas, el código fuente de la mayoría de los programas del sistema. La mayoría de los archivos que contiene son de sólo lectura para el usuario normal.
- `/usr/bin` contiene los comandos básicos del usuario.
- `/usr/sbin` contiene comandos adicionales para el administrador.
- `/usr/lib` contiene las bibliotecas del sistema.
- `/usr/share` contiene la documentación o común a todas las bibliotecas, por ejemplo `usr/share/man` contiene el texto de la página man.
## Datos personales del usuario `/home`
El directorio `/home` contiene los directorios personales de los usuarios. El directorio personal contiene los datos del usuario y los archivos de configuración específicos del usuario.
## Bibliotecas compartidas `/lib`
El directorio `/lib` contienen bibliotecas que pueden ser utilizados por los binarios ejecutables. El directorio `/lib` contiene las bibliotecas que necesitan los binarios de los directorios `/bin` y `/sbin`.
Las bibliotecas que necesitan los binarios en /usr/bin y /usr/sbin se encuentran en el directorio /usr/lib.
## Binarios del sistema `/sbin`
El directorio `/sbin` contiene binarios que solo pueden ser ejecutados por root o un usuario sudo.
## Archivos temporales
El directorio `/tmp` contiene archivos temporales. Todos los datos en `/tmp` se borran al reiniciar el dispositivo.
### Archivos de datos variables `/var`
El directorio `/var` contiene la información en tiempo de ejecución de los programas, como el registro del sistema, el seguimiento de los usuarios, la caché y otros archivos que los programas del sistema crean y gestionan.
## Archivos de arranque `/boot`
El directorio `/boot` contiene los archivos del kernel y la imagen de arranque, además de LILO y Grub. Suele ser recomendable que el directorio resida en una partición al principio del disco.
## Archivos de los procesos y del núcleo
El directorio `/proc` contiene la información sobre los procesos que se están ejecutando y los parámetros del kernel. El contenido del directorio `/proc` es utilizado por una serie de herramientas para obtener información del sistema en tiempo de ejecución.
## Software opcional `/opt`
## Punto de montaje para medios extraíbles `/media`
## Montar directorio `/mnt`
## Datos de servicio `/srv`