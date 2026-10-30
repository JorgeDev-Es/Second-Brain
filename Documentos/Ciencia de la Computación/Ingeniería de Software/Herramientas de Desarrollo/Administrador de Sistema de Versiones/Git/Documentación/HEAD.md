# HEAD en Git
## ¿Qué es el HEAD en Git?
En Git, el HEAD es una referencia al commit más reciente en la rama actual.

Ejemplo:
Usamos `git log` para obtener el historial de commits:
```Powershell
$> git log
commit d5b336b700d55703e06972e870c86616ead5c0b8 (HEAD -> master)
Author: Dev
Date:   Tue Nov 25 14:31:18 2025 -0600

    Empty project
```

Usamos `Get-Content` para conocer el contenido de HEAD:
```PowerShell
$> Get-Content -Path ".\.git\HEAD"
ref: refs/heads/master
```
HEAD devuelve el archivo al que hace referencia, así que usamos `Get-Content` nuevamente para ver el contenido del archivo `master`:
```PowerShell
$> Get-Content -Path ".\.git\refs\heads\master"
d5b336b700d55703e06972e870c86616ead5c0b8
```
El contenido del master es el SSH del commit más reciente
## Referencias
https://www.geeksforgeeks.org/git/git-head/