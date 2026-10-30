# Interfaz de Línea de Comandos de IsaacScript
## Descripción
Interfaz de línea de comandos para administrar mods de The Binding of Isaac en TypeScript.
## Uso
```Powershell
isaacscript <command> [options]
```
## Comandos
### `nuke`
Elimina y reinstala las dependencias en el proyecto actual.
### `publish`
`isaacscript publish` actualiza la versión y publica una nueva versión.
### `monitor`
`isaacscript monitor` actualiza las dependencias npm en el proyecto actual.

Opciones:

| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--skip-project-checks`\|--skip-project-checks]] |
| ------------------------------------------------------------------------------------------------------------------------ |

### `update`
### `check`
### `copy`
### `init`
Opciones:

| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`-y, --yes`\|-y, --yes]]                                               |
| ---------------------------------------------------------------------------------------------------------------------------------------------- |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--use-current-directory`\|--use-current-directory]]                   |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--custom-directory <directory>`\|--custom-directory <directory>]]     |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`-m, --mods-directory <directory>`\|-m, --mods-directory <directory>]] |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`-s, --save-slot <slot>`\|-s, --save-slot <slot>]]                     |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--vscode`\|--vscode]]                                                 |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--npm`\|--npm]]                                                       |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--yarn`\|--yarn]]                                                     |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--pnpm`\|--pnpm]]                                                     |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--skip-git`\|--skip-git]]                                             |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`--skip-install`\|--skip-install]]                                     |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`-f, --force-name`\|-f, --force-name]]                                 |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`-d, --dev`\|-d, --dev]]                                               |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`-v, --verbose`\|-v, --verbose]]                                       |
| [[Documentación/The Binding of Isaac Modding/IsaacScript/Referencia/CLI#`-h, --help`\|-h, --help]]                                             |

## Opciones
### Opciones globales
#### `-h`
#### `-v`
### Opciones específicas
#### `--skip-project-checks`
#### `-y, --yes`
Responde "sí" a cada opción del diálogo, similar a como funciona "npm init --yes". (por defecto: false)
#### `--use-current-directory`
Usa el directorio actual como raíz para el proyecto. (por defecto: false)
#### `--custom-directory <directory>`
El directorio en el que se creará el proyecto (en lugar del directorio de trabajo actual).
#### `-m, --mods-directory <directory>`
El directorio donde se encuentran los mods de Isaac en tu sistema.
#### `-s, --save-slot <slot>`
La ranura de guardado en el juego que usas para probar el mod. (por defecto: 1)
#### `--vscode`
Abre el proyecto en VSCode después de la inicialización. (por defecto: false)
#### `--npm`
Usa npm como gestor de paquetes. (por defecto: false)
#### `--yarn`
Usa Yarn como gestor de paquetes. (por defecto: false)
#### `--pnpm`
Usa pnpm como gestor de paquetes. (por defecto: false)
#### `--skip-git`
No inicializa Git. (por defecto: false)
#### `--skip-install`
No instala automáticamente las dependencias después de inicializar el proyecto. (por defecto: false)
#### `-f, --force-name`
Permite nombres de proyecto que normalmente no son válidos (por defecto: false)
#### `-d, --dev`
Enlaza el mod resultante con la versión local de desarrollo de isaacscript-common. (por defecto: false)
#### `-v, --verbose`
Habilita la salida detallada (verbose). (por defecto: false)
#### `-h, --help`
Muestra la lista de opciones para este comando.

## Referencias
https://github.com/IsaacScript/isaacscript/tree/main/packages/isaacscript-cli/src/commands