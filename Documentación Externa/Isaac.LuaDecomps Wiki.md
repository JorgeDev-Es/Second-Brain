# Isaac.LuaDecomps

Index your code with Devin
Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Overview

Relevant source files

- [Engine/Components/Image.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Components/Image.lua)
- [Engine/Interface/Shader.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/Shader.lua)
- [Isaac/Components/Manager/OptionsComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua)
- [Isaac/Core/Manager/Static.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Manager/Static.lua)
- [Isaac/Enums.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Enums.lua)
- [Isaac/Global.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua)
- [Isaac/Interface/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/AchievementOverlay.lua)
- [Isaac/Linker/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/AchievementOverlay.lua)
- [Isaac/Linker/Cutscene.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua)
- [Isaac/\_OLD/AchievementOverlay/Component.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua)
- [LICENSE](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LICENSE)
- [main.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/main.lua)

`Isaac.LuaDecomps` is a comprehensive Lua re-expression (decompilation) of the engine internals for _The Binding of Isaac: Repentance_. Its primary goal is to map out, structure, and document the binary behavior, memory layouts, and runtime logic of the native game engine by translating reverse-engineered structures into readable Lua code annotated with EmmyLua types.

The project serves as both an archival study of the game's architecture and a foundational framework for advanced modding, engine research, and tooling.

Sources: [LICENSE1-24](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LICENSE#L1-L24), [Isaac/Global.lua1-46](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L46)

* * *

## Repository Layout

The codebase is organized into distinct top-level directories that separate low-level engine primitives from high-level game rules, legacy artifacts, and IDE type definitions.

```

Root Directory

Engine/ - Low-level subsystems

General/ - Math, ANM2, Utilities

Isaac/ - Game specific mechanics & state

LuaEngine/ - Callback dispatch & binding

_EmmyLua/ - IDE type stubs

_Legacy/ & Isaac/_OLD/ - Historical iterations

Engine.Image (Engine/Components/Image.lua)

Interface.Engine.Shader (Engine/Interface/Shader.lua)

Isaac.Global (Isaac/Global.lua)

Enums (Isaac/Enums.lua)

Interface.Cutscene (Isaac/Linker/Cutscene.lua)
```

_Figure 1: High-level architectural map of repository layout and core modules._

- **`Engine/`**: Houses low-level engine abstractions such as graphics management, shaders, file input/output, and base component definitions like `Engine.Image` [Engine/Components/Image.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Components/Image.lua#L1-L52) and `Interface.Engine.Shader` [Engine/Interface/Shader.lua1-5](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/Shader.lua#L1-L5)
- **`General/`**: Contains shared utility libraries including ANM2 sprite rendering logic, vector math helpers, XML parsers, and custom data structures.
- **`Isaac/`**: The core domain package containing game state managers, entities, weapons, rooms, world generation, and global definitions like `Isaac.Global` [Isaac/Global.lua1-46](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L46) and `Enums` [Isaac/Enums.lua1-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Enums.lua#L1-L13)
- **`LuaEngine/`**: Manages the Lua execution environment, mod entry points, and callback routing systems.
- **`_EmmyLua/`**: Provides comprehensive type annotations and IDE hinting stubs (e.g., ffi, OpenGL, containers).
- **`_Legacy/` and `Isaac/_OLD/`**: Preserves previous decompilation iterations and obsolete file structures for historical reference.

Sources: [Isaac/Global.lua1-46](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L46), `[Isaac/Enums.lua:1-13]`, `[Engine/Components/Image.lua:1-52]`, `[Engine/Interface/Shader.lua:1-5]`, [Isaac/Linker/Cutscene.lua1-10](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua#L1-L10)

* * *

## 1.1 Architectural Layers: Interface, Linker, Component, Core, Content

The codebase enforces a rigorous five-layer convention across nearly all game subsystems (`Interface`, `Linker`, `Component`, `Core`, and `Content`). This separation decouples raw memory representation from stub definitions, binding layers, execution logic, and mod-facing or actor-specific behavior.

- **Interface**: Declares public namespaces, function signatures, and class types.
- **Linker**: Connects interface stubs to concrete implementations and binding tables (e.g., `Interface.Cutscene` bindings) [Isaac/Linker/Cutscene.lua1-51](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua#L1-L51)
- **Component**: Defines memory-offset structs mirroring native C++ structures (e.g., `Component.Options` offsets) [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52)
- **Core**: Implements the real underlying game logic and update routines.
- **Content**: Holds per-actor behaviors, specialized item interactions, and entity-specific scripts.

For details, see [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content).

Sources: [Isaac/Linker/Cutscene.lua1-51](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua#L1-L51), [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52), [Isaac/Interface/AchievementOverlay.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/AchievementOverlay.lua#L1-L2)

* * *

## 1.2 Conventions: Context, Globals and Memory Offsets

To successfully represent native engine structures in Lua, the project adopts strict naming and architectural conventions:

- **Context (`ctx`)**: Manager and game state context objects are threaded through subsystem calls to maintain execution state.
- **Globals**: Global states and root managers are exposed via tables like `Isaac.Global` [Isaac/Global.lua1-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L13) and engine-level equivalents.
- **Memory Offsets**: Component fields are annotated with precise hexadecimal byte offsets derived from reverse-engineering the native binary, as seen in `Component.Options` (`m_musicVolume : 0x18`, `m_sfxVolume : 0x1c`, etc.) [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52)
- **Naming Prefixes**: Native member variables utilize the `m_` prefix (`m_path`, `m_gamma`) [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52) while unknown or ambiguous fields are marked with `_qqq`.

For details, see [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets).

Sources: [Isaac/Global.lua1-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L13), [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52)

* * *

## 1.3 Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)

The repository retains older structural experiments to aid researchers in tracing how current architectures evolved.

- **`_Legacy/`**: A sprawling 354-file directory covering earlier iterations of Actor, Admin, Entity, Game, Mechanics, Menu, and Weapon systems.
- **`Isaac/_OLD/`**: Superseded decompilation attempts for specific modules (e.g., legacy achievement overlay components) [Isaac/\_OLD/AchievementOverlay/Component.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua#L1-L2)

Developers can mine these directories to cross-reference ambiguous native function calls or examine alternative approaches to complex engine subsystems.

For details, see [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)).

Sources: [Isaac/\_OLD/AchievementOverlay/Component.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua#L1-L2)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps#overview)
- [Repository Layout](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps#repository-layout)
- [1.1 Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps#11-architectural-layers-interface-linker-component-core-content)
- [1.2 Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps#12-conventions-context-globals-and-memory-offsets)
- [1.3 Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps#13-legacy-and-deprecated-trees-_legacy-isaac_old)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 1 Overview

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Overview

Relevant source files

- [Engine/Components/Image.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Components/Image.lua)
- [Engine/Interface/Shader.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/Shader.lua)
- [Isaac/Components/Manager/OptionsComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua)
- [Isaac/Core/Manager/Static.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Manager/Static.lua)
- [Isaac/Enums.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Enums.lua)
- [Isaac/Global.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua)
- [Isaac/Interface/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/AchievementOverlay.lua)
- [Isaac/Linker/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/AchievementOverlay.lua)
- [Isaac/Linker/Cutscene.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua)
- [Isaac/\_OLD/AchievementOverlay/Component.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua)
- [LICENSE](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LICENSE)
- [main.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/main.lua)

`Isaac.LuaDecomps` is a comprehensive Lua re-expression (decompilation) of the engine internals for _The Binding of Isaac: Repentance_. Its primary goal is to map out, structure, and document the binary behavior, memory layouts, and runtime logic of the native game engine by translating reverse-engineered structures into readable Lua code annotated with EmmyLua types.

The project serves as both an archival study of the game's architecture and a foundational framework for advanced modding, engine research, and tooling.

Sources: [LICENSE1-24](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LICENSE#L1-L24), [Isaac/Global.lua1-46](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L46)

* * *

## Repository Layout

The codebase is organized into distinct top-level directories that separate low-level engine primitives from high-level game rules, legacy artifacts, and IDE type definitions.

```

Root Directory

Engine/ - Low-level subsystems

General/ - Math, ANM2, Utilities

Isaac/ - Game specific mechanics & state

LuaEngine/ - Callback dispatch & binding

_EmmyLua/ - IDE type stubs

_Legacy/ & Isaac/_OLD/ - Historical iterations

Engine.Image (Engine/Components/Image.lua)

Interface.Engine.Shader (Engine/Interface/Shader.lua)

Isaac.Global (Isaac/Global.lua)

Enums (Isaac/Enums.lua)

Interface.Cutscene (Isaac/Linker/Cutscene.lua)
```

_Figure 1: High-level architectural map of repository layout and core modules._

- **`Engine/`**: Houses low-level engine abstractions such as graphics management, shaders, file input/output, and base component definitions like `Engine.Image` [Engine/Components/Image.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Components/Image.lua#L1-L52) and `Interface.Engine.Shader` [Engine/Interface/Shader.lua1-5](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/Shader.lua#L1-L5)
- **`General/`**: Contains shared utility libraries including ANM2 sprite rendering logic, vector math helpers, XML parsers, and custom data structures.
- **`Isaac/`**: The core domain package containing game state managers, entities, weapons, rooms, world generation, and global definitions like `Isaac.Global` [Isaac/Global.lua1-46](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L46) and `Enums` [Isaac/Enums.lua1-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Enums.lua#L1-L13)
- **`LuaEngine/`**: Manages the Lua execution environment, mod entry points, and callback routing systems.
- **`_EmmyLua/`**: Provides comprehensive type annotations and IDE hinting stubs (e.g., ffi, OpenGL, containers).
- **`_Legacy/` and `Isaac/_OLD/`**: Preserves previous decompilation iterations and obsolete file structures for historical reference.

Sources: [Isaac/Global.lua1-46](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L46), `[Isaac/Enums.lua:1-13]`, `[Engine/Components/Image.lua:1-52]`, `[Engine/Interface/Shader.lua:1-5]`, [Isaac/Linker/Cutscene.lua1-10](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua#L1-L10)

* * *

## 1.1 Architectural Layers: Interface, Linker, Component, Core, Content

The codebase enforces a rigorous five-layer convention across nearly all game subsystems (`Interface`, `Linker`, `Component`, `Core`, and `Content`). This separation decouples raw memory representation from stub definitions, binding layers, execution logic, and mod-facing or actor-specific behavior.

- **Interface**: Declares public namespaces, function signatures, and class types.
- **Linker**: Connects interface stubs to concrete implementations and binding tables (e.g., `Interface.Cutscene` bindings) [Isaac/Linker/Cutscene.lua1-51](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua#L1-L51)
- **Component**: Defines memory-offset structs mirroring native C++ structures (e.g., `Component.Options` offsets) [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52)
- **Core**: Implements the real underlying game logic and update routines.
- **Content**: Holds per-actor behaviors, specialized item interactions, and entity-specific scripts.

For details, see [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content).

Sources: [Isaac/Linker/Cutscene.lua1-51](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua#L1-L51), [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52), [Isaac/Interface/AchievementOverlay.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/AchievementOverlay.lua#L1-L2)

* * *

## 1.2 Conventions: Context, Globals and Memory Offsets

To successfully represent native engine structures in Lua, the project adopts strict naming and architectural conventions:

- **Context (`ctx`)**: Manager and game state context objects are threaded through subsystem calls to maintain execution state.
- **Globals**: Global states and root managers are exposed via tables like `Isaac.Global` [Isaac/Global.lua1-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L13) and engine-level equivalents.
- **Memory Offsets**: Component fields are annotated with precise hexadecimal byte offsets derived from reverse-engineering the native binary, as seen in `Component.Options` (`m_musicVolume : 0x18`, `m_sfxVolume : 0x1c`, etc.) [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52)
- **Naming Prefixes**: Native member variables utilize the `m_` prefix (`m_path`, `m_gamma`) [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52) while unknown or ambiguous fields are marked with `_qqq`.

For details, see [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets).

Sources: [Isaac/Global.lua1-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L13), [Isaac/Components/Manager/OptionsComponent.lua1-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua#L1-L52)

* * *

## 1.3 Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)

The repository retains older structural experiments to aid researchers in tracing how current architectures evolved.

- **`_Legacy/`**: A sprawling 354-file directory covering earlier iterations of Actor, Admin, Entity, Game, Mechanics, Menu, and Weapon systems.
- **`Isaac/_OLD/`**: Superseded decompilation attempts for specific modules (e.g., legacy achievement overlay components) [Isaac/\_OLD/AchievementOverlay/Component.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua#L1-L2)

Developers can mine these directories to cross-reference ambiguous native function calls or examine alternative approaches to complex engine subsystems.

For details, see [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)).

Sources: [Isaac/\_OLD/AchievementOverlay/Component.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua#L1-L2)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview#overview)
- [Repository Layout](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview#repository-layout)
- [1.1 Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview#11-architectural-layers-interface-linker-component-core-content)
- [1.2 Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview#12-conventions-context-globals-and-memory-offsets)
- [1.3 Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview#13-legacy-and-deprecated-trees-_legacy-isaac_old)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 1.1 Architectural Layers: Interface Linker Component Core Content

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Architectural Layers: Interface, Linker, Component, Core, Content

Relevant source files

- [Isaac/Components/Entity/EntityComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua)
- [Isaac/Components/Entity/EntityPtrComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityPtrComponent.lua)
- [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)
- [Isaac/Interface/Entity\_NPC.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Entity_NPC.lua)
- [Isaac/Interface/ItemPool.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/ItemPool.lua)
- [Isaac/Interface/NPC\_Pathfinder.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/NPC_Pathfinder.lua)
- [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)
- [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)
- [Isaac/Linker/Game.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Game.lua)
- [Isaac/Linker/NPC\_Pathfinder.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/NPC_Pathfinder.lua)
- [Isaac/Utils/LootList.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua)

## Purpose and Scope

This page details the five-layer architectural convention used across the codebase to re-express the engine internals of _The Binding of Isaac: Repentance_. By separating definitions, memory layouts, stub bindings, core logic, and content behaviors into distinct namespaces (`Isaac/Interface`, `Isaac/Linker`, `Isaac/Components`, `Isaac/Core`, and `Isaac/Content`), the decompilation maintains a strict modular boundary that mimics low-level engine structures while providing a navigable Lua environment.

* * *

## 1\. Interface Layer (`Isaac/Interface/`)

The **Interface** layer defines the public-facing API surface, namespace declarations, and LuaCATS type annotations. Files in this directory typically contain minimal or empty table declarations that establish type contracts for external tooling and IDE auto-completion, serving as the foundational contract for engine classes [Isaac/Interface/ItemPool.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/ItemPool.lua#L1-L2) [Isaac/Interface/Entity\_NPC.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Entity_NPC.lua#L1-L2) and [Isaac/Interface/NPC\_Pathfinder.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/NPC_Pathfinder.lua#L1-L2)

Sources:

- `Isaac/Interface/ItemPool.lua:1-2`
- `Isaac/Interface/Entity_NPC.lua:1-2`
- `Isaac/Interface/NPC_Pathfinder.lua:1-2`

* * *

## 2\. Linker Layer (`Isaac/Linker/`)

The **Linker** layer acts as the binding and stub bridge between interfaces, memory components, and core processing logic. Linker files (such as `Isaac/Linker/Entity.lua`, `Isaac/Linker/Entity_Pickup.lua`, and `Isaac/Linker/Game.lua`) define stub tables (`Stub`) that map method signatures to component instances and route execution to specific core modules [Isaac/Linker/Entity.lua13-237](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua#L13-L237) [Isaac/Linker/Entity\_Pickup.lua12-209](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua#L12-L209) [Isaac/Linker/Game.lua8-240](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Game.lua#L8-L240) and [Isaac/Linker/NPC\_Pathfinder.lua4-118](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/NPC_Pathfinder.lua#L4-L118)

```
Component Layer

Linker Layer

Interface Layer

Isaac/Interface/Entity.lua

Isaac/Interface/Entity_Pickup.lua

Isaac/Linker/Entity.lua

Isaac/Linker/Entity_Pickup.lua

Isaac/Components/Entity/EntityComponent.lua

Isaac/Components/Entity/PickupComponent.lua
```

Sources:

- `Isaac/Linker/Entity.lua:13-237`
- `Isaac/Linker/Entity_Pickup.lua:12-209`
- `Isaac/Linker/Game.lua:8-240`
- `Isaac/Linker/NPC_Pathfinder.lua:4-118`

* * *

## 3\. Component Layer (`Isaac/Components/`)

The **Component** layer models the C++ memory layout of engine objects. Structs defined here utilize explicit hexadecimal memory-offset annotations corresponding to engine field positions (e.g., `m_priceANM2 : 0x360`, `m_charge : 0x474`) [Isaac/Components/Entity/PickupComponent.lua1-32](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua#L1-L32) and pointer abstractions like `Component.EntityPtr` [Isaac/Components/Entity/EntityPtrComponent.lua1-10](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityPtrComponent.lua#L1-L10)

Components also define factory functions (such as `New()`) to initialize memory-mapped tables with default values and bind virtual functions to their respective linkers [Isaac/Components/Entity/PickupComponent.lua33-92](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua#L33-L92) and [Isaac/Components/Entity/EntityComponent.lua1-129](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L1-L129)

Sources:

- `Isaac/Components/Entity/PickupComponent.lua:1-100`
- `Isaac/Components/Entity/EntityComponent.lua:1-129`
- `Isaac/Components/Entity/EntityPtrComponent.lua:1-10`

* * *

## 4\. Core Layer (`Isaac/Core/`)

The **Core** layer implements the real procedural logic, update loops, sub-systems, and state machines of the game engine. Core modules are consumed directly by the Linker layer to perform heavy calculations, physics checks, chest logic, shop routines, and game state transitions [Isaac/Linker/Entity\_Pickup.lua4-10](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua#L4-L10) and [Isaac/Linker/Game.lua4-7](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Game.lua#L4-L7) Utilities such as `Isaac/Utils/LootList.lua` interface with core spawn routines to manage drop tables and entity instantiation [Isaac/Utils/LootList.lua1-60](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua#L1-L60)

```
Utils Layer

Core Layer

Linker Layer

Isaac/Linker/Game.lua

Isaac/Linker/Entity_Pickup.lua

Isaac/Core/Game/Start.lua

Isaac/Core/Game/Render.lua

Isaac/Core/Pickup/Chest.lua

Isaac/Core/Pickup/ShopItem.lua

Isaac/Utils/LootList.lua
```

Sources:

- `Isaac/Linker/Entity_Pickup.lua:4-10`
- `Isaac/Linker/Game.lua:4-7`
- `Isaac/Utils/LootList.lua:1-60`

* * *

## 5\. Content Layer (`Isaac/Content/`)

The **Content** layer contains per-actor configurations, mod-like behavior scripts, and specific enemy/boss definitions. While the Core layer provides the generic engine mechanics (e.g., how pickups or entities update), the Content layer provides the specific data definitions and localized behavior trees that bring individual entities and items to life.

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content#architectural-layers-interface-linker-component-core-content)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content#purpose-and-scope)
- [1\. Interface Layer (\`Isaac/Interface/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content#1-interface-layer-isaacinterface)
- [2\. Linker Layer (\`Isaac/Linker/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content#2-linker-layer-isaaclinker)
- [3\. Component Layer (\`Isaac/Components/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content#3-component-layer-isaaccomponents)
- [4\. Core Layer (\`Isaac/Core/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content#4-core-layer-isaaccore)
- [5\. Content Layer (\`Isaac/Content/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content#5-content-layer-isaaccontent)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 1.3 Legacy And Deprecated Trees (_Legacy Isaac_Old)

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)

Relevant source files

- [General/Sprite.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Sprite.lua)
- [Isaac/Components/Weapon/WeaponBone.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Weapon/WeaponBone.lua)
- [Isaac/Content/Weapon/Bone/BoneFire.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Weapon/Bone/BoneFire.lua)
- [Isaac/\_OLD/ANM2/Render.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/ANM2/Render.lua)
- [Isaac/\_OLD/Backdrop/Component.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/Backdrop/Component.lua)
- [Isaac/\_OLD/PersistentGameData/Progress.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/PersistentGameData/Progress.lua)
- [Isaac/\_OLD/RoomConfig/Utils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/RoomConfig/Utils.lua)

## Purpose and Scope

This page documents the structural layout and utility of the historical, non-active codebase directories: the 354-file `_Legacy` tree and `Isaac/_OLD`. These directories contain earlier iterations of engine re-expressions, legacy component layouts, experimental rendering pipelines, and partial game logic implementations. Although superseded by the current architectural layout (`Isaac/`, `Engine/`, `General/`), these trees serve as a vital reference repository for cross-referencing undocumented memory offsets, math helpers, stage calculation logic, and early staging variants.

Sources: `Isaac/_OLD/ANM2/Render.lua:1-200()`, `Isaac/_OLD/Backdrop/Component.lua:1-40()`, `Isaac/_OLD/RoomConfig/Utils.lua:1-131()`, `Isaac/_OLD/PersistentGameData/Progress.lua:1-106()`

* * *

## Architecture of Legacy Trees

The historical trees are partitioned into broad sub-packages that predate the current Interface/Linker/Component/Core/Content layering convention. The `_Legacy` root contains modular directories such as `Actor/`, `Admin/`, `Entity/`, `Game/`, `Mechanics/`, `Menu/`, `Weapon/`, and nested `_Legacy/` sub-folders. Similarly, `Isaac/_OLD/` preserves early prototypes for subsystems like backdrop configuration, ANM2 geometry rendering, and persistent game data progress tracking.

```

Root Repository

_Legacy Tree

Isaac/_OLD Tree

Actor/

Admin/

Entity/

Game/

Mechanics/

Menu/

Weapon/

ANM2/Render.lua

Backdrop/Component.lua

RoomConfig/Utils.lua

PersistentGameData/Progress.lua
```

Sources: `Isaac/_OLD/ANM2/Render.lua:1-200()`, `Isaac/_OLD/Backdrop/Component.lua:1-40()`, `Isaac/_OLD/RoomConfig/Utils.lua:1-131()`, `Isaac/_OLD/PersistentGameData/Progress.lua:1-106()`

* * *

## Subsystem Implementations in Legacy Code

### Rendering and ANM2 Transformations (`Isaac/_OLD/ANM2/`)

Early graphics computations resided in `Isaac/_OLD/ANM2/Render.lua`, implementing transformation matrices and vertex source/destination calculations before animation logic was refactored into `General/` and `Isaac/Render`. Functions such as `GetSourceQuad` and `GetDestQuad` handle screen scaling, rotation pivots, and flip flags using raw frame component metrics \[Isaac/\_OLD/ANM2/Render.lua:24-189()\].

```

ANMCorePipeline

GetSourceQuad(frame, layerState, anm2)

GetDestQuad(myContext, position, frame, layerState, anm2)

GraphicsQuad.CreateSourceQuad

GraphicsQuad.Scale & RotateDegrees
```

Sources: `Isaac/_OLD/ANM2/Render.lua:12-189()`

### Backdrop and Room Configuration Utilities (`Isaac/_OLD/Backdrop/`, `Isaac/_OLD/RoomConfig/`)

The backdrop component layout (`Component.Backdrop`) defines raw memory offset annotations for images and sprite entries, mapping backdrops to specific surface structures (`Engine.Image`) and entity tracking flags \[Isaac/\_OLD/Backdrop/Component.lua:1-19()\]. Room configuration helpers in `Isaac/_OLD/RoomConfig/Utils.lua` provide stage translation routines via `GetStageID`, mapping level stages and alternate path variations (`StageType.STAGETYPE_REPENTANCE`) to internal `StbType` enums \[Isaac/\_OLD/RoomConfig/Utils.lua:15-76()\].

Sources: `Isaac/_OLD/Backdrop/Component.lua:1-19()`, `Isaac/_OLD/RoomConfig/Utils.lua:15-76()`

### Persistent Game Data and Unlocks (`Isaac/_OLD/PersistentGameData/`)

Save state logic and achievement unlinking are preserved in `Isaac/_OLD/PersistentGameData/Progress.lua`. Functions like `Unlocked` evaluate active achievements against game state conditions and debug parameters, while `AddStageCompleted` manages completion tallies for unlocking specific entities and items (e.g., tracking `LevelStage.STAGE1_2` milestones to unlock `Achievement.STEVEN`) \[Isaac/\_OLD/PersistentGameData/Progress.lua:17-91()\].

Sources: `Isaac/_OLD/PersistentGameData/Progress.lua:17-91()`

* * *

## Mining Guidelines for Reference

When encountering unmapped functions, unknown constants (`_qqq`), or legacy behavioral parity checks in the active `Isaac/` codebase, developers can query the `_Legacy` and `Isaac/_OLD` trees for historical context using the following heuristics:

1. **Memory Layout Comparison:** Check legacy component files (e.g., `Isaac/_OLD/Backdrop/Component.lua`) when structural offsets in newer component files mismatch or contain padding gaps (`_qqq` markers).
2. **Algorithm Reconstruction:** Use older math and procedural generation helpers (such as `Isaac/_OLD/RoomConfig/Utils.lua`) to reconstruct mathematical transformations or stage index lookups that were compressed or refactored into native bindings.
3. **Vanilla Parity Verification:** Compare legacy event loops against current `Isaac/Core/` and `Isaac/Content/` implementations to verify state transition orders and fallback parameters.

Sources: `Isaac/_OLD/Backdrop/Component.lua:1-40()`, `Isaac/_OLD/RoomConfig/Utils.lua:1-131()`, `Isaac/_OLD/PersistentGameData/Progress.lua:1-106()`

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#legacy-and-deprecated-trees-_legacy-isaac_old)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#purpose-and-scope)
- [Architecture of Legacy Trees](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#architecture-of-legacy-trees)
- [Subsystem Implementations in Legacy Code](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#subsystem-implementations-in-legacy-code)
- [Rendering and ANM2 Transformations (\`Isaac/\_OLD/ANM2/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#rendering-and-anm2-transformations-isaac_oldanm2)
- [Backdrop and Room Configuration Utilities (\`Isaac/\_OLD/Backdrop/\`, \`Isaac/\_OLD/RoomConfig/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#backdrop-and-room-configuration-utilities-isaac_oldbackdrop-isaac_oldroomconfig)
- [Persistent Game Data and Unlocks (\`Isaac/\_OLD/PersistentGameData/\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#persistent-game-data-and-unlocks-isaac_oldpersistentgamedata)
- [Mining Guidelines for Reference](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old)#mining-guidelines-for-reference)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 1.2 Conventions: Context Globals And Memory Offsets

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Conventions: Context, Globals and Memory Offsets

Relevant source files

- [Engine/Global.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Global.lua)
- [General/Context.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Context.lua)
- [Isaac/Core/Slot/SlotCollision.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotCollision.lua)
- [Isaac/Core/Slot/SlotDamage.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotDamage.lua)
- [Isaac/Core/Slot/SlotInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua)
- [Isaac/Core/Slot/SlotMisc.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotMisc.lua)
- [Isaac/Core/Slot/SlotRender.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotRender.lua)
- [Isaac/Core/Slot/SlotUpdate.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotUpdate.lua)
- [Isaac/Global.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua)
- [Isaac/Linker/GenericPrompt.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GenericPrompt.lua)
- [Isaac/Linker/HUD.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/HUD.lua)
- [Isaac/Linker/PersistentGameData.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua)

## Purpose and Scope

This page documents the fundamental architectural conventions used throughout the `Isaac.LuaDecomps` codebase. It details how execution state is threaded via `Context.Common`, how global singletons are partitioned between game logic (`Isaac/Global.lua`) and low-level engine facilities (`Engine/Global.lua`), how C++ memory layouts are mirrored using `m_` prefixes in component files, and the conventions used for unidentified parameters and fields (`_qqq` markers and `param_` placeholders).

Sources: `General/Context.lua:1-4` [General/Context.lua1-3](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Context.lua#L1-L3)`Isaac/Global.lua:1-45` [Isaac/Global.lua1-45](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L45)`Engine/Global.lua:1-16` [Engine/Global.lua1-16](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Global.lua#L1-L16)

* * *

## 1\. Context Threading (`Context.Common`)

Every significant core execution routine, gameplay update, collision handler, and entity operation in the codebase receives a context object—conventionally named `ctx`—whose type is `Context.Common`. Defined in `General/Context.lua`, this structure holds references to the two primary top-level managers of the game loop:

- `manager`: A `Component.Manager` instance handling system setups, transitions, and application state.
- `game`: A `Component.Game` instance handling active run states, rooms, levels, and entity management.

By passing `ctx` explicitly through every call, core functions avoid relying on global state pollution, mirroring how execution context pointers are passed through C++ member functions in the original engine binary.

For example, slot initialization, state updates, and explosion drops all thread `ctx` down to interface and content layers:

- `Init(slot, ctx, entityType, variant, subType, seed)` in `Isaac/Core/Slot/SlotInit.lua:9-15` [Isaac/Core/Slot/SlotInit.lua9-15](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua#L9-L15)
- `Update(slot, ctx)` in `Isaac/Core/Slot/SlotUpdate.lua:24-25` [Isaac/Core/Slot/SlotUpdate.lua24-25](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotUpdate.lua#L24-L25)
- `CreateDropsFromExplosion(slot, ctx)` in `Isaac/Core/Slot/SlotMisc.lua:113-117` [Isaac/Core/Slot/SlotMisc.lua113-117](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotMisc.lua#L113-L117)

### Diagram: Context Threading Data Flow

```
Subsystem Core Functions

Context Structure

Execution Entry

Passes ctx

ctx

ctx

ctx

EngineGameLoop

Context.Common (General/Context.lua)

manager: Component.Manager

game: Component.Game

SlotInit.Init (Isaac/Core/Slot/SlotInit.lua)

SlotUpdate.Update (Isaac/Core/Slot/SlotUpdate.lua)

SlotMisc.CreateDropsFromExplosion (Isaac/Core/Slot/SlotMisc.lua)
```

Sources: `General/Context.lua:1-4` [General/Context.lua1-3](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Context.lua#L1-L3)`Isaac/Core/Slot/SlotInit.lua:9-15` [Isaac/Core/Slot/SlotInit.lua9-15](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua#L9-L15)`Isaac/Core/Slot/SlotUpdate.lua:24-25` [Isaac/Core/Slot/SlotUpdate.lua24-25](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotUpdate.lua#L24-L25)`Isaac/Core/Slot/SlotMisc.lua:113-117` [Isaac/Core/Slot/SlotMisc.lua113-117](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotMisc.lua#L113-L117)

* * *

## 2\. Global State Containers: `Isaac.Global` and `Engine.Global`

Global state is split cleanly between Isaac-specific subsystems and low-level engine services.

### `Isaac/Global.lua`

`Isaac.Global` manages top-level game state pointers, display scaling metrics, and global shader references [Isaac/Global.lua4-45](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L4-L45):

- `Global.Manager`: Active `Component.Manager` reference.
- `Global.MenuManager`: Active `Component.MenuManager` reference.
- `Global.Game`: Active `Component.Game` reference.
- Screen dimensions (`WIDTH`, `HEIGHT`, `RENDER_WIDTH`, `RENDER_HEIGHT`, `POINTSCALE`, etc.).
- `Global.Shaders`: An array lookup table containing pre-allocated shader instances keyed by `Renderer.ShaderType` (e.g., `SHADER_COLOR_OFFSET`, `SHADER_PIXELATION`, `SHADER_BLOOM`, `SHADER_HQ4X`, `SHADER_OLDTV`) [Isaac/Global.lua23-44](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L23-L44)

### `Engine/Global.lua`

`Engine.Global` provides access to core engine subsystems independent of gameplay logic [Engine/Global.lua1-16](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Global.lua#L1-L16):

- `Global.FileManager`: `Engine.FileManager` for asset loading.
- `Global.GraphicsManager`: `Engine.GraphicsManager` for rendering primitives and screen targets.
- `Global.ShapeRenderer`: `Engine.ShapeRenderer` for debug and primitive drawing.
- `Global.ImageManager`: `Engine.ImageManager` for texture handling.

Sources: `Isaac/Global.lua:1-45` [Isaac/Global.lua1-45](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Global.lua#L1-L45)`Engine/Global.lua:1-16` [Engine/Global.lua1-16](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Global.lua#L1-L16)

* * *

## 3\. Component Memory Offsets and Naming (`m_`)

Component tables represent the decompiled memory layouts of C++ structures from the game binary.

- **The `m_` Prefix**: Any field prefixed with `m_` (e.g., `slot.m_state`, `slot.m_position`, `slot.m_sprite`, `slot.m_config`) corresponds directly to a member variable located at a fixed hexadecimal offset within the underlying C++ class instance.
- **Component Initialization**: During `Init` and update routines, these fields are accessed and mutated directly rather than through getter/setter abstractions, reflecting direct memory manipulation in the native engine. For example, slot states, timers, flags, and vectors are assigned directly to `m_` fields [Isaac/Core/Slot/SlotInit.lua20-41](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua#L20-L41):

```
local myConfig = slot.m_config
if myConfig then
    local mySprite = slot.m_sprite
    mySprite:Load(myConfig.anm2Path, true)
    mySprite:Play(mySprite:GetDefaultAnimation(), false)
end

slot.m_targetPosition = Vector(0, 0)
slot.m_positionOffset = Vector(0, 0)
slot.m_sizeMulti = Vector(1, 1)
slot.m_donationValue = 0
slot.m_triggerTimer = 0
slot.m_state = SlotState.IDLE
```

### Diagram: Component Memory Layout Mapping (`m_` Fields)

```
Memory Offsets (C++ Binary Mirror)

Code Entity Space

Natural Language Space

Entity Slot Component Instance

Component.Entity.Slot (Struct)

m_state (+Offset 0x64)

m_position (+Offset 0x80)

m_sprite (+Offset 0xB8)

m_config (+Offset 0xF0)
```

Sources: `Isaac/Core/Slot/SlotInit.lua:20-41` [Isaac/Core/Slot/SlotInit.lua20-41](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua#L20-L41)`Isaac/Core/Slot/SlotUpdate.lua:30-51` [Isaac/Core/Slot/SlotUpdate.lua30-51](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotUpdate.lua#L30-L51)

* * *

## 4\. Unknown Markers (`_qqq` and `param_`)

During the decompilation process, reverse-engineering binary functions often yields parameters and fields whose exact semantic purpose, type, or name cannot be immediately determined. The codebase uses standardized conventions to mark these unknowns:

- **`_qqq` Suffix**: Used for unknown parameters, flags, or local variables whose role is currently ambiguous (e.g., `unused_qqq` in `Isaac/Linker/HUD.lua:63` [Isaac/Linker/HUD.lua60-65](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/HUD.lua#L60-L65)).
- **`param_N` Placeholders**: Used in Stub function signatures within linker files when argument names could not be recovered from debug symbols (e.g., `param_1`, `param_2`, `param_3` in `Isaac/Linker/PersistentGameData.lua:10-15` [Isaac/Linker/PersistentGameData.lua10-15](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua#L10-L15) and `Isaac/Linker/GenericPrompt.lua:41-47` [Isaac/Linker/GenericPrompt.lua41-47](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GenericPrompt.lua#L41-L47)).

These markers serve as signposts for future contributors to investigate during binary comparisons and refactoring passes.

Sources: `Isaac/Linker/HUD.lua:60-65` [Isaac/Linker/HUD.lua60-65](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/HUD.lua#L60-L65)`Isaac/Linker/PersistentGameData.lua:10-15` [Isaac/Linker/PersistentGameData.lua10-15](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua#L10-L15)`Isaac/Linker/GenericPrompt.lua:41-47` [Isaac/Linker/GenericPrompt.lua41-47](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GenericPrompt.lua#L41-L47)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#conventions-context-globals-and-memory-offsets)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#purpose-and-scope)
- [1\. Context Threading (\`Context.Common\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#1-context-threading-contextcommon)
- [Diagram: Context Threading Data Flow](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#diagram-context-threading-data-flow)
- [2\. Global State Containers: \`Isaac.Global\` and \`Engine.Global\`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#2-global-state-containers-isaacglobal-and-engineglobal)
- [\`Isaac/Global.lua\`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#isaacgloballua)
- [\`Engine/Global.lua\`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#enginegloballua)
- [3\. Component Memory Offsets and Naming (\`m\_\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#3-component-memory-offsets-and-naming-m_)
- [Diagram: Component Memory Layout Mapping (\`m\_\` Fields)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#diagram-component-memory-layout-mapping-m_-fields)
- [4\. Unknown Markers (\`\_qqq\` and \`param\_\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets#4-unknown-markers-_qqq-and-param_)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 2.1 Base Entity Entityptr And Entity Lists

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Base Entity, EntityPtr and Entity Lists

Relevant source files

- [Isaac/Components/Config/EntityConfigComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/EntityConfigComponent.lua)
- [Isaac/Components/Entity/EntityComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua)
- [Isaac/Components/Entity/EntityPtrComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityPtrComponent.lua)
- [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)
- [Isaac/Components/Player/TearParams.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Player/TearParams.lua)
- [Isaac/Interface/EntityConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/EntityConfig.lua)
- [Isaac/Interface/Entity\_NPC.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Entity_NPC.lua)
- [Isaac/Interface/NPC\_Pathfinder.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/NPC_Pathfinder.lua)
- [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)
- [Isaac/Linker/EntityConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/EntityConfig.lua)
- [Isaac/Linker/EntityList.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/EntityList.lua)
- [Isaac/Linker/Entity\_Laser.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Laser.lua)
- [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)
- [Isaac/Linker/NPC\_Pathfinder.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/NPC_Pathfinder.lua)
- [Isaac/Utils/LootList.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua)

This leaf page details the foundational entity model in `Isaac.LuaDecomps`. It covers the core memory layout of `Component.Entity`, entity reference handles (`Component.EntityPtr`), global entity lists, spatial/type partitioning, and the underlying plumbing for status effects, collisions, and damage calculation.

* * *

## 1\. Base Entity Memory Layout and Interface

Every entity in the engine inherits from or conforms to the base entity structure defined in `Component.Entity` [Isaac/Components/Entity/EntityComponent.lua26-129](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L26-L129) This structure maps directly to the C++ memory layout of the game engine, annotating fields with precise hexadecimal offsets.

Virtual function hooks—such as `Init`, `Update`, `Render`, `TakeDamage`, `Remove`, and `HandleCollision`—are declared as function signatures within the component and populated during entity creation [Isaac/Components/Entity/EntityComponent.lua1-24](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L1-L24)

Interface stubs in `Isaac.Linker.Entity` (`Isaac/Linker/Entity.lua`) provide Lua-accessible wrappers for querying and mutating entity properties like position, velocity, flags, and type identification [Isaac/Linker/Entity.lua1-237](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua#L1-L237)

```
Delegates to

Core Fields

Core Fields

Virtual Table

Wraps Reference

Interface.EntityStub

Component.Entity

m_position : 0x294

m_velocity : 0x2b8

Init / Update / TakeDamage

EntityPtrComponent
```

Sources: `Isaac/Components/Entity/EntityComponent.lua:1-129`, `Isaac/Linker/Entity.lua:1-237`, `Isaac/Components/Entity/EntityPtrComponent.lua:1-9`

* * *

## 2\. Entity Pointers and References (`EntityPtr`)

Because entities are frequently created, destroyed, or reallocated across frames, direct Lua references to `Component.Entity` tables can quickly become stale or point to recycled memory slots. To solve this, the engine uses `Component.EntityPtr` [Isaac/Components/Entity/EntityPtrComponent.lua1-9](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityPtrComponent.lua#L1-L9)

An `EntityPtr` wraps an optional entity reference (`ref = Component.Entity?`) and is utilized extensively throughout component layouts where weak or managed cross-entity references are required—such as pickup ghosts (`m_pickupGhost_qqq`), unkown entity references (`m_unkEntRef3_qqq`), and magnetized pulling targets (`m_magnetizedPullingEffect`) [Isaac/Components/Entity/PickupComponent.lua21-22](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua#L21-L22) [Isaac/Components/Entity/EntityComponent.lua108](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L108-L108)

Sources: `Isaac/Components/Entity/EntityPtrComponent.lua:1-9`, `Isaac/Components/Entity/PickupComponent.lua:21-22`, `Isaac/Components/Entity/EntityComponent.lua:108-108`

* * *

## 3\. Entity Lists, Partitions and Management

Entities within a room or active game session are organized through entity list managers (`Isaac/Linker/EntityList.lua`).

The entity management subsystem maintains categorized lists and partitions (such as players, tears, projectiles, familiars, pickups, slots, and NPCs) to optimize iteration order during game loops, physics updates, and rendering phases. Partitions allow systems to query subsets of entities efficiently without iterating over the entire global entity pool.

```
Manages

Partitions

Partitions

Partitions

Partitions

GameEngineManager

EntityList.lua

Players

NPCs / Enemies

Pickups

Projectiles / Tears
```

Sources: `Isaac/Linker/EntityList.lua:1-1`

* * *

## 4\. Status Effects, Collision, and Damage Plumbing

### Status Effects

Status effects are tracked via dedicated countdown timers and state flags embedded directly inside the `Component.Entity` layout from offset `0x208` to `0x25c` [Isaac/Components/Entity/EntityComponent.lua85-106](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L85-L106) Key tracking fields include:

- `m_damageCountdown` (`0x20c`) [Isaac/Components/Entity/EntityComponent.lua86](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L86-L86)
- `m_freezeCountdown` (`0x210`) [Isaac/Components/Entity/EntityComponent.lua87](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L87-L87)
- `m_poisonCountdown` (`0x214`) [Isaac/Components/Entity/EntityComponent.lua88](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L88-L88)
- `m_slowingCountdown` (`0x218`) [Isaac/Components/Entity/EntityComponent.lua89](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L89-L89)
- `m_charmedCountdown` (`0x21c`) [Isaac/Components/Entity/EntityComponent.lua90](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L90-L90)
- `m_confusionCountdown` (`0x220`) [Isaac/Components/Entity/EntityComponent.lua91](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L91-L91)
- `m_fearCountdown` (`0x228`) [Isaac/Components/Entity/EntityComponent.lua93](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L93-L93)
- `m_burnCountdown` (`0x22c`) [Isaac/Components/Entity/EntityComponent.lua94](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L94-L94)

### Damage Plumbing

Damage ingestion flows through the `TakeDamage` virtual function hook [Isaac/Components/Entity/EntityComponent.lua8](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L8-L8) Damage events populate history buffers (`m_damage_entries` at `0x8`) and accumulate totals in `m_damage_damageTaken` (`0x14`) and `m_damage_flagsTaken` (`0x18`) [Isaac/Components/Entity/EntityComponent.lua52-54](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L52-L54)

### Collision Plumbing

Collision resolution relies on collision classes and geometry definitions stored in the entity structure:

- `m_gridCollisionClass` (`0x17c`) and `m_entityCollisionClass` (`0x180`) [Isaac/Components/Entity/EntityComponent.lua75-76](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L75-L76)
- `HandleCollision` virtual function hook (`0x22`) managing collider interactions [Isaac/Components/Entity/EntityComponent.lua22](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L22-L22)

```
Triggers

Logs Entry

Accumulates

Triggers

Evaluates

IncomingDamageEvent

Entity.TakeDamage

m_damage_entries : 0x8

m_damage_damageTaken : 0x14

PhysicsCollision

Entity.HandleCollision

m_entityCollisionClass : 0x180
```

Sources: `Isaac/Components/Entity/EntityComponent.lua:8-22`, `Isaac/Components/Entity/EntityComponent.lua:52-54`, `Isaac/Components/Entity/EntityComponent.lua:75-106`

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#base-entity-entityptr-and-entity-lists)
- [1\. Base Entity Memory Layout and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#1-base-entity-memory-layout-and-interface)
- [2\. Entity Pointers and References (\`EntityPtr\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#2-entity-pointers-and-references-entityptr)
- [3\. Entity Lists, Partitions and Management](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#3-entity-lists-partitions-and-management)
- [4\. Status Effects, Collision, and Damage Plumbing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#4-status-effects-collision-and-damage-plumbing)
- [Status Effects](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#status-effects)
- [Damage Plumbing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#damage-plumbing)
- [Collision Plumbing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists#collision-plumbing)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 2 Entity System

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Entity System

Relevant source files

- [Isaac/Components/Entity/EntityComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua)
- [Isaac/Components/Entity/EntityPtrComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityPtrComponent.lua)
- [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)
- [Isaac/Interface/Entity\_NPC.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Entity_NPC.lua)
- [Isaac/Interface/NPC\_Pathfinder.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/NPC_Pathfinder.lua)
- [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)
- [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)
- [Isaac/Linker/NPC\_Pathfinder.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/NPC_Pathfinder.lua)
- [Isaac/Utils/LootList.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua)

The Entity System forms the core architectural model for all dynamic game objects in `Isaac.LuaDecomps`. It defines a multi-layered structure combining Lua interfaces (`Isaac/Interface/`), function linkers (`Isaac/Linker/`), and explicit memory-offset component definitions (`Isaac/Components/Entity/`) that mirror the underlying engine's memory layout.

```

Isaac/Linker/Entity.lua

Interface.Entity

Isaac/Components/Entity/EntityRefComponent.lua

Isaac/Core/Entity/Data.lua

Isaac/Linker/Entity_Pickup.lua

Isaac/Components/Entity/PickupComponent.lua

Isaac/Core/Pickup/Global.lua
```

Sources: [`Isaac/Linker/Entity.lua:1-12`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Linker/Entity_Pickup.lua:1-11`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Components/Entity/EntityRefComponent.lua:1-9`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Components/Entity/PickupComponent.lua:1-40`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

* * *

## 2.1. Base Entity, EntityPtr and Entity Lists

The base entity layer establishes the foundational properties, virtual method tables, and status effect fields shared by every entity in the game. `Component.Entity` defines memory offsets ranging from collision classes and velocities to status effect countdowns (`m_freezeCountdown`, `m_poisonCountdown`, etc.) [Isaac/Components/Entity/EntityComponent.lua1-129](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityComponent.lua#L1-L129) Entity pointers (`Component.EntityPtr`) wrap weak or strong references to entities safely [Isaac/Components/Entity/EntityPtrComponent.lua1-9](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/EntityPtrComponent.lua#L1-L9)

The linker layer (`Isaac/Linker/Entity.lua`) provides stubs for type checking, position queries, flag manipulation, and casting helpers such as `Stub.ToPickup()` and `Stub.ToNPC()` [Isaac/Linker/Entity.lua1-237](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua#L1-L237)

For details, see [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists).

Sources: [`Isaac/Components/Entity/EntityComponent.lua:1-129`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Components/Entity/EntityPtrComponent.lua:1-9`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Linker/Entity.lua:1-237`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

* * *

## 2.2. Player Entity

The player entity subsystem manages Isaac and co-op characters via `Interface.EntityPlayer`. It controls complex states including health pools, inventory, active/passive items, costumes, input mapping, damage calculation, and pocket items.

For details, see [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity).

Sources: [`Isaac/Linker/Entity.lua:1-237`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

* * *

## 2.3. Pickups

```

Isaac/Linker/Entity_Pickup.lua

Isaac/Components/Entity/PickupComponent.lua

m_priceANM2, m_charge, m_timeout, m_state

Isaac/Utils/LootList.lua

IGame.Spawn()
```

Sources: [`Isaac/Linker/Entity_Pickup.lua:1-88`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Components/Entity/PickupComponent.lua:1-32`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Utils/LootList.lua:1-57`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

The pickup subsystem handles collectible items, trinkets, chests, coins, hearts, and shop interactions. Defined by `Component.Entity.Pickup`, it tracks pickup-specific attributes like shop prices (`m_price`), options indices (`m_optionsPickupIndex`), timers, and alternate pedestal states [Isaac/Components/Entity/PickupComponent.lua1-32](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua#L1-L32) Utilities like `Utils.LootList` manage entry collections and deterministic spawning via `LootList.Spawn` [Isaac/Utils/LootList.lua1-57](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua#L1-L57)

For details, see [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups).

Sources: [`Isaac/Linker/Entity_Pickup.lua:1-88`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Components/Entity/PickupComponent.lua:1-32`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Utils/LootList.lua:1-57`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

* * *

## 2.4. NPCs and Pathfinding

NPCs and enemies are structured around `Interface.Entity_NPC` [Isaac/Interface/Entity\_NPC.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Entity_NPC.lua#L1-L2) and associated component data. Navigation is handled by the pathfinding module (`Interface.Npc.Pathfinder`), which supplies methods for grid-based path calculation (`FindGridPath`), target evasion (`EvadeTarget`), and random movement behaviors [Isaac/Interface/NPC\_Pathfinder.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/NPC_Pathfinder.lua#L1-L2)

For details, see [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding).

Sources: [`Isaac/Interface/Entity_NPC.lua:1-2`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system), [`Isaac/Interface/NPC_Pathfinder.lua:1-118`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

* * *

## 2.5. Slots, Beggars and Machines

Stationary entities such as slot machines, blood donation machines, beggars, and shell games are categorized under the slot system. They implement custom lifecycle hooks managing initialization, updates, damage response, and coin insertion mechanics.

For details, see [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines).

Sources: [`Isaac/Linker/Entity.lua:203-208`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

* * *

## 2.6. Familiars and Custom Actor Hooks

Familiars, custom NPCs, and special pickups rely on linker dispatch tables and behavior registries. These bridge core engine events with Lua-defined custom actor logic.

For details, see [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks).

Sources: [`Isaac/Linker/Entity.lua:203-216`](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system#entity-system)
- [2.1. Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system#21-base-entity-entityptr-and-entity-lists)
- [2.2. Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system#22-player-entity)
- [2.3. Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system#23-pickups)
- [2.4. NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system#24-npcs-and-pathfinding)
- [2.5. Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system#25-slots-beggars-and-machines)
- [2.6. Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system#26-familiars-and-custom-actor-hooks)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 2.2 Player Entity

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Player Entity

Relevant source files

- [Isaac/Components/Player/TemporaryEffectsComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Player/TemporaryEffectsComponent.lua)
- [Isaac/Interface/Ambush.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Ambush.lua)
- [Isaac/Interface/Custom/ActorNpc.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Custom/ActorNpc.lua)
- [Isaac/Interface/Custom/ActorPickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Custom/ActorPickup.lua)
- [Isaac/Interface/Custom/RoomMechanics.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/Custom/RoomMechanics.lua)
- [Isaac/Interface/ProceduralItemInventory.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/ProceduralItemInventory.lua)
- [Isaac/Interface/ScoreSheet.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/ScoreSheet.lua)
- [Isaac/Linker/Ambush.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Ambush.lua)
- [Isaac/Linker/Entity\_Player.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua)
- [Isaac/Linker/PlayerManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua)
- [Isaac/Linker/ProceduralItemManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ProceduralItemManager.lua)
- [Isaac/Linker/Seeds.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua)
- [Isaac/Linker/Weapon.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Weapon.lua)
- [Isaac/StateSetup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/StateSetup.lua)

The Player Entity system is responsible for managing the state, behavior, controls, inventory, and lifecycle of all players in The Binding of Isaac: Repentance. Defined primarily through stub interfaces and component bindings in `Isaac/Linker/Entity_Player.lua` [Isaac/Linker/Entity\_Player.lua1-212](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L1-L212) the player subsystem interacts closely with world generation, game loops, item pools, and input managers.

This page serves as a high-level parent overview of the player architecture. For deep dives into specific item interactions and player behavior hooks, see [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions).

* * *

## Architecture and Subsystems

The player model splits responsibilities across several core managers and component definitions. The primary interface `Interface.EntityPlayer` provides access to state queries (such as `Stub.GetPlayerType`, `Stub.GetFireDirection`, and `Stub.GetEffects`) [Isaac/Linker/Entity\_Player.lua30-70](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L30-L70) as well as complex item invocation handlers (such as `Stub.UseActiveItem`, `Stub.use_red_key`, and `Stub.AddWisp`) [Isaac/Linker/Entity\_Player.lua146-192](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L146-L192)

```
Coordinates

Tracks

Manages Array

Uses

Queries

Manager Component

PlayerManager

Game Instance

Interface.EntityPlayer

Component.TemporaryEffects

Interface.Seeds
```

_Sources: [Isaac/Linker/Entity\_Player.lua1-212](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L1-L212) [Isaac/Linker/PlayerManager.lua1-50](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua#L1-L50) [Isaac/Linker/Seeds.lua1-35](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua#L1-L35)_

* * *

## Health Pools, Inventory, and Pocket Items

Players maintain complex health states (red hearts, soul hearts, black hearts, bone hearts, and golden hearts) managed via core update loops. Inventory systems track active items across multiple slots, passive items, trinkets, and cards/pills stored in pocket items.

Query functions like `Stub.GetActiveItem`, `Stub.GetActiveCharge`, and `Stub.GetActiveItemSlot` allow the engine to inspect and manipulate player inventory state [Isaac/Linker/Entity\_Player.lua85-113](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L85-L113) Temporary or status-based modifiers are tracked via `Component.TemporaryEffects`, which maps active item effects and temporary stat boosts directly to the player instance [Isaac/Components/Player/TemporaryEffectsComponent.lua1-11](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Player/TemporaryEffectsComponent.lua#L1-L11)

Sources: [Isaac/Linker/Entity\_Player.lua65-115](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L65-L115) [Isaac/Components/Player/TemporaryEffectsComponent.lua1-11](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Player/TemporaryEffectsComponent.lua#L1-L11)

* * *

## Costumes, Input Control, and Animation

The player entity handles vector-based aiming (`Stub.GetAimDirection`), firing directions (`Stub.GetFireDirection`), and movement states (`Stub.GetMovementDirection`) [Isaac/Linker/Entity\_Player.lua30-85](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L30-L85) Input enabling and disabling are regulated via `Stub.SetControlsEnabled` and `Stub.AreControlsEnabled` [Isaac/Linker/Entity\_Player.lua100-132](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L100-L132)

Costumes and body animations synchronize with weapon firing and item usage. Weapon-specific animations are driven through linkages defined in item states, while extra animations can be halted using helper routines like `Stub.StopExtraAnimation` [Isaac/Linker/Entity\_Player.lua108](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L108-L108)

Sources: [Isaac/Linker/Entity\_Player.lua30-135](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Player.lua#L30-L135)

* * *

## Player Manager

Multiplayer, co-op babies, and global player lookups are orchestrated by `Component.PlayerManager` and its linker interface `Isaac/Linker/PlayerManager.lua` [Isaac/Linker/PlayerManager.lua1-50](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua#L1-L50)

The Player Manager handles spawning co-op players (`Stub.SpawnCoPlayer`, `Stub.SpawnCoPlayerBaby`) [Isaac/Linker/PlayerManager.lua50-56](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua#L50-L56) checking group inventories (`Stub.AnyoneHasCollectible`, `Stub.AnyoneHasTrinket`) [Isaac/Linker/PlayerManager.lua20-32](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua#L20-L32) and tracking item ownership across all active characters (`Stub.FirstCollectibleOwner`, `Stub.RandomCollectibleOwner`) [Isaac/Linker/PlayerManager.lua150-165](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua#L150-L165)

```
GetPlayer

GetPlayer

AnyoneHasCollectible

SpawnCoPlayerBaby

PlayerManager

Entity.Player 1

Entity.Player 2

Item Pools

Co-op Babies
```

_Sources: [Isaac/Linker/PlayerManager.lua1-190](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua#L1-L190)_

* * *

## Seeds and RNG

Player generation, initial stats, and run properties are tied heavily to seed management handled via `Isaac/Linker/Seeds.lua` [Isaac/Linker/Seeds.lua1-111](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua#L1-L111)

The seeds component coordinates player initialization seeds (`Stub.GetPlayerInitSeed`), stage-specific seed generation (`Stub.GetStageSeed`), seed effect validation (`Stub.CanAddSeedEffect`), and banned combo checks (`Stub.IsSeedComboBanned`) [Isaac/Linker/Seeds.lua15-70](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua#L15-L70)

Sources: [Isaac/Linker/Seeds.lua1-111](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua#L1-L111)

* * *

## Child Pages

For detailed documentation on specific player behavior hooks and item-actor interactions, refer to the child page:

- **[Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)** — Covers item-specific player behavior hooks, custom player effects, and item block modules under `Isaac/Linker/Custom/PlayerEffects` and `Isaac/Core/Player/Events`.

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity#player-entity)
- [Architecture and Subsystems](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity#architecture-and-subsystems)
- [Health Pools, Inventory, and Pocket Items](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity#health-pools-inventory-and-pocket-items)
- [Costumes, Input Control, and Animation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity#costumes-input-control-and-animation)
- [Player Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity#player-manager)
- [Seeds and RNG](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity#seeds-and-rng)
- [Child Pages](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity#child-pages)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 2.2.1 Player Effects And Item Interactions

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Player Effects and Item Interactions

Relevant source files

- [Isaac/Content/PlayerEffects/Interactions.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua)
- [Isaac/Content/PlayerEffects/ItemBlock.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua)
- [Isaac/Core/Pickup/Collision.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/Collision.lua)
- [Isaac/Core/Pickup/ShopItem.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/ShopItem.lua)
- [Isaac/Core/Player/Events.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Player/Events.lua)
- [Isaac/Linker/Custom/GameEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/GameEffects.lua)
- [Isaac/Linker/Custom/PlayerEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/PlayerEffects.lua)
- [Isaac/Linker/Custom/RoomMechanics.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/RoomMechanics.lua)

## Purpose and Scope

This page details the implementation of item-specific player behavior hooks, inventory interactions, item blocking mechanics, and player-related event triggers. It covers the linker tables in `Isaac/Linker/Custom/PlayerEffects.lua`, the modular content scripts under `Isaac/Content/PlayerEffects/` (`Interactions.lua`, `ItemBlock.lua`), and player event hooks in `Isaac/Core/Player/Events.lua`.

* * *

## 1\. Linker Architecture and Submodule Routing

The `Isaac/Linker/Custom/PlayerEffects.lua` file acts as a central registry that binds interface declarations to specific implementation modules under `Isaac/Content/PlayerEffects/`. It aggregates disparate content mechanics—such as shop behaviors, loot modifiers, redemption mechanics, and item blocking—into a unified `Interface.PlayerEffects` table.

```

Interface.PlayerEffects

Isaac/Linker/Custom/PlayerEffects.lua

Isaac/Content/PlayerEffects/Shop.lua

Isaac/Content/PlayerEffects/Interactions.lua

Isaac/Content/PlayerEffects/ItemBlock.lua

Isaac/Content/PlayerEffects/WispAdd.lua

Isaac/Content/PlayerEffects/LootModifiers.lua

Isaac/Content/PlayerEffects/Redemption.lua
```

_Sources: [Isaac/Linker/Custom/PlayerEffects.lua1-26](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/PlayerEffects.lua#L1-L26)_

* * *

## 2\. Item and Card Blocking Logic

The `Isaac/Content/PlayerEffects/ItemBlock.lua` module governs conditional restrictions on whether specific items or cards can spawn or be collected based on player types, inventory tags, and active effects.

### Key Functions

- `NoKeeperBlock(playerManager, item)`: Prevents items tagged with `ItemConfig.TAG_NO_KEEPER` from appearing when any player is Keeper or Tainted Keeper [Isaac/Content/PlayerEffects/ItemBlock.lua13-18](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua#L13-L18)
- `NoLostBrBlock(playerManager, ctx, item)`: Checks birthright restrictions for The Lost [Isaac/Content/PlayerEffects/ItemBlock.lua24-28](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua#L24-L28)
- `LostB_BlockItem(playerManager, ctx, item)`: Evaluates quality thresholds and deterministic RNG checks using start seeds to block low-quality non-offensive items for Tainted Lost [Isaac/Content/PlayerEffects/ItemBlock.lua34-68](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua#L34-L68)
- `SacredOrb_BlockItem(playerManager, ctx, item)`: Implements Sacred Orb quality filtering by rolling RNG to block low-quality items [Isaac/Content/PlayerEffects/ItemBlock.lua74-107](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua#L74-L107)
- `No_BlockItem(playerManager, ctx, item)`: Blocks quality 0 items when the player holds a gold-variant Trinket 'No' (`TrinketType.TRINKET_NO`) with a multiplier >= 2 [Isaac/Content/PlayerEffects/ItemBlock.lua114-126](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua#L114-L126)
- `BlockCard(playerManager, ctx, card)`: Blocks `Card.CARD_SUICIDE_KING` if the player type is Jacob [Isaac/Content/PlayerEffects/ItemBlock.lua144-151](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua#L144-L151)

```

BlockItem()

NoKeeperBlock()

NoLostBrBlock()

LostB_BlockItem()

SacredOrb_BlockItem()

No_BlockItem()
```

_Sources: [Isaac/Content/PlayerEffects/ItemBlock.lua13-151](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/ItemBlock.lua#L13-L151)_

* * *

## 3\. Pickup Interactions and Eligibility

Pickup interactions and collection permissions are evaluated in `Isaac/Content/PlayerEffects/Interactions.lua` and invoked during collision resolution phases in `Isaac/Core/Pickup/Collision.lua`.

### Core Interaction Rules

- `CanPickupShopItem(player, ctx, pickup)`: Verifies that the player is not currently holding an item (`IEntityPlayer.IsHoldingItem`) and that the shop item pricing/pickup conditions are satisfied [Isaac/Content/PlayerEffects/Interactions.lua15-18](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua#L15-L18)
- `CanCollectPickup(player, ctx, pickup)`: Enforces complex eligibility checks:

  - Co-op baby rules restrict pickup types unless the baby skin is `BabySubType.BABY_MAGNET` and the pickup can be rerolled [Isaac/Content/PlayerEffects/Interactions.lua25-32](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua#L25-L32)
  - Co-op ghosts cannot collect pickups [Isaac/Content/PlayerEffects/Interactions.lua37-39](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua#L37-L39)
  - Duplicate Book of Belial passives prevent collection of active/passive conflicting variants [Isaac/Content/PlayerEffects/Interactions.lua41-47](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua#L41-L47)
  - Sub-player entities (such as Soul of the Forgotten or Soul of Jacob) restrict pocket items, actives, and specific collectibles [Isaac/Content/PlayerEffects/Interactions.lua49-76](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua#L49-L76)
- `BabyMagnet_GetEffectTarget(ctx, pickup)`: Resolves target player entities for magnet mechanics using distance queries (`IGame.GetNearestPlayerEx`) [Isaac/Content/PlayerEffects/Interactions.lua83-90](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua#L83-L90)

```

Collision.lua:player_handle_pickup

Interactions.CanCollectPickup

Interactions.CanPickupShopItem

Interactions.BabyMagnet_GetEffectTarget

Verify SubPlayer & Soul Effects

Verify CoOp Ghost & Baby State
```

_Sources: [Isaac/Content/PlayerEffects/Interactions.lua15-90](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PlayerEffects/Interactions.lua#L15-L90) \[Isaac/Core/Pickup/Collision.lua:72-99\]_

* * *

## 4\. Player Event Hooks and Shop Transactions

Player actions involving currency expenditure and devil deals trigger centralized callbacks defined in `Isaac/Core/Player/Events.lua` and processed alongside `Isaac/Core/Pickup/ShopItem.lua`.

### Key Mechanics

- `TriggerMoneySpent(player, ctx, spentMoney)`: Updates Keeper's Sack calculations and triggers Member Card achievement checks [Isaac/Core/Player/Events.lua13-16](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Player/Events.lua#L13-L16)
- `TriggerDevilDealTaken(player, ctx, pickup, price)`: Increments devil deal counters, adds devil room stats via `IGame.AddDevilRoomDeal`, updates persistent game data event counters, and triggers Redemption mechanics [Isaac/Core/Player/Events.lua22-36](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Player/Events.lua#L22-L36)
- Shop Purchasing: `CanPickupShopItem` evaluates special prices or coupon-modified coin totals (`CouponWisp_GetExtraShopCoins_NoDecrease`), while `spend_money` handles transaction deductions and restock triggers [Isaac/Core/Pickup/ShopItem.lua20-78](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/ShopItem.lua#L20-L78)

```

ShopItem.lua:TriggerShopPurchase

ShopItem.lua:spend_money

Mechanics_PreSpentCoins

IEntityPlayer.AddCoins

Player.Events.TriggerMoneySpent

PlayerEffects.KeepersSack_AddSpentCoins

GameEffects.Achievement_MemberCard
```

_Sources: [Isaac/Core/Player/Events.lua13-36](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Player/Events.lua#L13-L36) \[Isaac/Core/Pickup/ShopItem.lua:20-78\]_

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#player-effects-and-item-interactions)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#purpose-and-scope)
- [1\. Linker Architecture and Submodule Routing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#1-linker-architecture-and-submodule-routing)
- [2\. Item and Card Blocking Logic](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#2-item-and-card-blocking-logic)
- [Key Functions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#key-functions)
- [3\. Pickup Interactions and Eligibility](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#3-pickup-interactions-and-eligibility)
- [Core Interaction Rules](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#core-interaction-rules)
- [4\. Player Event Hooks and Shop Transactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#4-player-event-hooks-and-shop-transactions)
- [Key Mechanics](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions#key-mechanics)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 2.3 Pickups

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Pickups

Relevant source files

- [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)
- [Isaac/Content/Pickup/Effects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Effects.lua)
- [Isaac/Content/Pickup/Events.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Events.lua)
- [Isaac/Content/Pickup/Interactions.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Interactions.lua)
- [Isaac/Content/Pickup/Properties.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Properties.lua)
- [Isaac/Content/PickupMechanics.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/PickupMechanics.lua)
- [Isaac/Core/Level/LevelGenerator/Utils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Level/LevelGenerator/Utils.lua)
- [Isaac/Core/Pickup/Chest.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/Chest.lua)
- [Isaac/Core/Pickup/PickupInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/PickupInit.lua)
- [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)
- [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)
- [Isaac/Utils/LootList.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua)

### Purpose and Scope

This section details the `Component.Entity.Pickup` subsystem within `Isaac.LuaDecomps`. It covers the exact memory layout of pickup components, initialization pipelines, property evaluation, chest opening mechanics, loot list resolution, shop item integration, collision handling, and associated content scripts.

* * *

### PickupComponent Memory Layout

The pickup memory layout is defined in `Isaac/Components/Entity/PickupComponent.lua` [Isaac/Components/Entity/PickupComponent.lua1-32](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua#L1-L32) It extends `Component.Entity` by allocating specific byte offsets for properties such as visual states, timers, shop data, and flags.

| Field Name | Offset | Type | Description |
| --- | --- | --- | --- |
| `m_priceANM2` | `0x360` | `Sprite` | Associated price tag sprite renderer. |
| `m_charge` | `0x474` | `integer` | Current charge for active-charge items/collectibles. |
| `m_optionsPickupIndex` | `0x478` | `integer` | Index used for "pick one of multiple" pedestal options. |
| `m_touched` | `0x47c` | `boolean` | Flag indicating whether the pickup has been collided with or touched. |
| `m_isBlind` | `0x47e` | `boolean` | Blind item indicator (hidden item appearance). |
| `m_payToPlay` | `0x47f` | `boolean` | Indicates if the chest/pickup requires coins to open (Pay to Play effect). |
| `m_price` | `0x480` | `integer` | Coin or key cost when treated as a shop or interactive item. |
| `m_shopItemId` | `0x488` | `integer` | Unique identifier linking the pickup to room shop data. |
| `m_timeout` | `0x48c` | `integer` | Countdown timer until the pickup despawns or changes state. |
| `m_wait` | `0x490` | `integer` | Initialization delay frame counter before collection/physics apply. |
| `m_dropDelay` | `0x4a0` | `integer` | Frame delay before the dropped pickup can be collected. |
| `m_state` | `0x4d0` | `integer` | Internal finite state machine value. |
| `m_coopExtra_collectedItems` | `0x4d4` | `integer` | Co-op tracking index for collected items. |
| `m_activeVarData` | `0x4e8` | `integer` | Active variant-specific data payload. |

The constructor function `New()` initializes these fields and binds virtual functions such as `Init`, `Update`, `Render`, `TakeDamage`, `Remove`, and `HandleCollision` to `Isaac.Interface.Entity_Pickup` stubs [Isaac/Components/Entity/PickupComponent.lua42-92](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua#L42-L92)

Sources: `Isaac/Components/Entity/PickupComponent.lua` [Isaac/Components/Entity/PickupComponent.lua1-92](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua#L1-L92)

* * *

### Pickup Initialization, Properties, and Events

When a pickup is spawned, `Isaac/Core/Pickup/PickupInit.lua` handles setup logic, segregating flow depending on whether the entity is a shop item, a regular collectible, or a standard consumable [Isaac/Core/Pickup/PickupInit.lua30-141](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/PickupInit.lua#L30-L141)

```

Yes

No

Yes

No

IGame.Spawn / Entity_Pickup.Init

Isaac/Core/Pickup/PickupInit.lua:Init

Is Shop Item?

init_shop_item()

Is Collectible?

init_collectible()

Standard Consumable Setup

pickup_appear()

collectible_appear()

IRoom.MakeShopItem

Isaac.Content.PickupMechanics

Isaac/Core/Pickup/PickupInit.lua

Isaac/Content/Pickup/Properties.lua

Isaac/Content/Pickup/Events.lua
```

_Figure 1: Pickup initialization routing from code entry points to specialized configuration handlers._

Properties and modifier evaluations are decoupled into `Isaac/Content/Pickup/Properties.lua` and `Isaac/Content/Pickup/Events.lua`:

- `Properties.IsIdleAppear(ctx)` determines if a pickup spawns immediately in the idle state based on room visit counts and stage configurations [Isaac/Content/Pickup/Properties.lua10-17](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Properties.lua#L10-L17)
- `Properties.ItemShouldDuplicate(pickup, ctx)` evaluates Damocles passive triggers on non-shop collectibles [Isaac/Content/Pickup/Properties.lua21-25](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Properties.lua#L21-L25)
- `Events.PostPickupInit(pickup, ctx)` handles challenge-specific removals (e.g., Ultra Hard heart removal, Backasswards trophy filtering) and initial cosmetic flags like sprite mirroring [Isaac/Content/Pickup/Events.lua9-30](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Events.lua#L9-L30)

Sources: `Isaac/Core/Pickup/PickupInit.lua` [Isaac/Core/Pickup/PickupInit.lua30-182](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/PickupInit.lua#L30-L182)`Isaac/Content/Pickup/Properties.lua` [Isaac/Content/Pickup/Properties.lua10-34](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Properties.lua#L10-L34)`Isaac/Content/Pickup/Events.lua` [Isaac/Content/Pickup/Events.lua7-30](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Events.lua#L7-L30)

* * *

### Chests and Loot Lists

Chest opening logic is centralized in `Isaac/Core/Pickup/Chest.lua`, interacting directly with utility modules like `Isaac/Utils/LootList.lua` to distribute contents [Isaac/Core/Pickup/Chest.lua69-107](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/Chest.lua#L69-L107) [Isaac/Utils/LootList.lua19-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua#L19-L52)

```

Yes

Chest Opened

Switch_ResolveLootEntry

RESOLVE_DEFAULT: LootList.Spawn()

RESOLVE_COLLECTIBLE: Morph or IGame.Spawn()

RESOLVE_DEAL_WARP: Stage 6 Red Chest Deal

RESOLVE_ENEMY_SPIDER: Spawn Enemy & Nudge Player

Is MegaChest?

m_dropDelay adjustment

Isaac/Core/Pickup/Chest.lua

Isaac/Utils/LootList.lua
```

_Figure 2: Chest loot resolution pipeline mapping resolved entries to spawned world entities._

Loot lists are managed via `Component.LootList` tables containing entries (`Component.LootList.Entry`) holding type, variant, subtype, seed, and optional RNG instances [Isaac/Utils/LootList.lua9-15](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua#L9-L15)`LootList.Spawn` translates these entries into live game entities by invoking `IGame.Spawn` with seeded RNG sequences [Isaac/Utils/LootList.lua38-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua#L38-L52)

Sources: `Isaac/Core/Pickup/Chest.lua` [Isaac/Core/Pickup/Chest.lua69-161](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/Chest.lua#L69-L161)`Isaac/Utils/LootList.lua` [Isaac/Utils/LootList.lua1-58](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua#L1-L58)

* * *

### Shop Items and Modifiers

Shop items follow a dedicated initialization path within `init_shop_item` [Isaac/Core/Pickup/PickupInit.lua30-42](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/PickupInit.lua#L30-L42)

1. The pickup links its `m_shopItemId` via `IRoom.MakeShopItem` [Isaac/Core/Pickup/PickupInit.lua33](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/PickupInit.lua#L33-L33)
2. Base prices are retrieved from room configurations and adjusted by shop discounts (`IRoom.TryGetShopDiscount`) [Isaac/Core/Pickup/PickupInit.lua39-40](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/PickupInit.lua#L39-L40)
3. Content modifiers such as `CollectibleSelectModifiers` process specific item substitutions (e.g., Wait What? transformations triggered via Butter Bean combinations) [Isaac/Content/Pickup/Effects.lua41-76](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Effects.lua#L41-L76)

Sources: `Isaac/Core/Pickup/PickupInit.lua` [Isaac/Core/Pickup/PickupInit.lua30-42](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/PickupInit.lua#L30-L42)`Isaac/Content/Pickup/Effects.lua` [Isaac/Content/Pickup/Effects.lua41-76](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Effects.lua#L41-L76)

* * *

### Collision and Interactions

Collision behavior and collection eligibility are handled by `Isaac/Content/Pickup/Interactions.lua`:

- `NeedsFreePlayer(pickup, ctx)` checks if picking up an item requires freeing the player from certain states (e.g., eternal hearts, troll bombs, or active consumables) [Isaac/Content/Pickup/Interactions.lua15-31](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Interactions.lua#L15-L31)
- `HasCustomCollect(pickup, ctx)` isolates collectible pedestals for custom inventory addition routines [Isaac/Content/Pickup/Interactions.lua35-37](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Interactions.lua#L35-L37)
- `IgnorePhysicsCollision(pickup, ctx, collider, blackboard)` determines whether physics impulses should be bypassed—such as during dungeon room transitions, big chest enemy collisions, bomb interactions, or shop item locks [Isaac/Content/Pickup/Interactions.lua56-82](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Interactions.lua#L56-L82)

Sources: `Isaac/Content/Pickup/Interactions.lua` [Isaac/Content/Pickup/Interactions.lua1-82](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Pickup/Interactions.lua#L1-L82)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups#pickups)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups#purpose-and-scope)
- [PickupComponent Memory Layout](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups#pickupcomponent-memory-layout)
- [Pickup Initialization, Properties, and Events](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups#pickup-initialization-properties-and-events)
- [Chests and Loot Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups#chests-and-loot-lists)
- [Shop Items and Modifiers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups#shop-items-and-modifiers)
- [Collision and Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups#collision-and-interactions)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 4 World: Rooms Levels And Grid

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# World: Rooms, Levels and Grid

Relevant source files

- [General/XY.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/XY.lua)
- [Isaac/Components/Game/EntityListComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/EntityListComponent.lua)
- [Isaac/Components/Level/LevelGeneratorRoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Level/LevelGeneratorRoomComponent.lua)
- [Isaac/Components/Room/RoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua)
- [Isaac/Components/Room/RoomDescriptorComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomDescriptorComponent.lua)
- [Isaac/Core/Room/PositionUtils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/PositionUtils.lua)
- [Isaac/Interface/LevelGenerator.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/LevelGenerator.lua)
- [Isaac/Linker/LevelGenerator.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/LevelGenerator.lua)
- [Isaac/Linker/Room.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua)
- [LuaEngine/Callbacks.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LuaEngine/Callbacks.lua)

The world representation and generation subsystem models the physical layout of the game world in The Binding of Isaac: Repentance. This includes individual rooms and their descriptors [Isaac/Components/Room/RoomComponent.lua1-118](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L1-L118) structural grid entities, pathfinding data, and procedural level generation algorithms [Isaac/Linker/LevelGenerator.lua16-94](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/LevelGenerator.lua#L16-L94)

As a parent page, this document provides a high-level architectural overview of world management. For low-level specifications, consult the respective child pages:

- **Room Component and Interface**: [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- **Grid Entities**: [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- **Level Generation**: [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)

* * *

## World Architecture Overview

The world pipeline bridges high-level procedural layout generation with concrete runtime rooms, grid indices, and entity containment.

```
Runtime Room System

Level Generation

Calls

Uses

Exposes

Implements

Builds

Interface.LevelGenerator

Stub.Generate

Component.LevelGenerator.Room

General.XY

Component.Room

Interface.Room

Room.PositionUtils
```

_Sources: Isaac/Linker/LevelGenerator.lua:16-34, Isaac/Components/Room/RoomComponent.lua:1-122, Isaac/Linker/Room.lua:1-60, Isaac/Core/Room/PositionUtils.lua:8-50, General/XY.lua:7-17_

* * *

## 4.1 Room Component and Interface

The room system manages active gameplay spaces. The raw memory layout is defined by `Component.Room` [Isaac/Components/Room/RoomComponent.lua1-101](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L1-L101) which tracks initialization states, dimensions (`m_gridWidth`, `m_gridHeight`), bounding boxes (`m_topLeftBound`, `m_bottomRightBound`), grid entity lists, door slots, and environmental attributes like water flow and backdrop shaders.

Interface bindings and stubs are exposed via `Interface.Room` [Isaac/Linker/Room.lua1-60](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua#L1-L60) providing query functions for water amount, grid height/width, active entities, doors, and path markers. Position utilities such as `Room.PositionUtils.GetRandomPosition` and `Room.PositionUtils.FindFreeTilePosition` calculate valid spawn coordinates within standard or L-shaped rooms [Isaac/Core/Room/PositionUtils.lua8-87](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/PositionUtils.lua#L8-L87)

For deep technical details on layouts, room initialization, environment FX, doors, and room transitions, see [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface).

_Sources: Isaac/Components/Room/RoomComponent.lua:1-101, Isaac/Linker/Room.lua:1-60, Isaac/Core/Room/PositionUtils.lua:8-87_

* * *

## 4.2 Grid Entities

Grid entities represent static or destructible world objects anchored to room grid coordinates (e.g., rocks, poops, pits, spikes, and doors). Rooms maintain a fixed grid entity array (`m_gridEntityList` of size 448) alongside door slot registries and grid path flags (`m_gridPaths` array of size 456) [Isaac/Components/Room/RoomComponent.lua10-15](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L10-L15)

Interaction with grid entities occurs through room stubs like `Stub.GetGridEntity`, `Stub.GetGridPath`, and `Stub.SetGridPath` [Isaac/Linker/Room.lua44-107](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua#L44-L107) which evaluate pathfinding restrictions and collision categories.

For details on grid collision classes, grid descriptors, and specific grid entity implementations, see [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities).

_Sources: Isaac/Components/Room/RoomComponent.lua:10-15, Isaac/Linker/Room.lua:44-107_

* * *

## 4.3 Level Generation

The level generation subsystem constructs floor layouts, places special rooms (such as secret and boss rooms), and configures room adjacencies [Isaac/Linker/LevelGenerator.lua16-94](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/LevelGenerator.lua#L16-L94)

The generator relies on `Component.LevelGenerator` structures paired with `Component.LevelGenerator.Room` definitions [Isaac/Components/Level/LevelGeneratorRoomComponent.lua8-23](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Level/LevelGeneratorRoomComponent.lua#L8-L23) which track grid positions (`m_gridPosition`), horizontal/vertical sizes, door masks, and neighbor sets using 2D coordinate utilities from `General.XY` [General/XY.lua7-17](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/XY.lua#L7-L17) Room configuration XML data and secret room placement logic coordinate to produce complete floor graphs.

For full coverage of generator routines, room shape validation, secret room algorithms, and RoomConfig loading, see [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation).

```
Code Entity Space: Level Gen Pipeline

Allocates

Allocates

Supplies

Processes

Component.LevelGenerator.New

Component.LevelGenerator

Module.LevelGenerator.Room.New

Component.LevelGenerator.Room

General.XY.New

Interface.LevelGenerator.Generate
```

_Sources: Isaac/Linker/LevelGenerator.lua:16-24, Isaac/Components/Level/LevelGeneratorRoomComponent.lua:26-49, General/XY.lua:11-17_

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid#world-rooms-levels-and-grid)
- [World Architecture Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid#world-architecture-overview)
- [4.1 Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid#41-room-component-and-interface)
- [4.2 Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid#42-grid-entities)
- [4.3 Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid#43-level-generation)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 4.1 Room Component And Interface

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Room Component and Interface

Relevant source files

- [Isaac/Components/Game/EntityListComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/EntityListComponent.lua)
- [Isaac/Components/Room/RoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua)
- [Isaac/Components/Room/RoomDescriptorComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomDescriptorComponent.lua)
- [Isaac/Content/Config/RoomShape.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Config/RoomShape.lua)
- [Isaac/Core/Pickup/Collision.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/Collision.lua)
- [Isaac/Core/Pickup/ShopItem.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/ShopItem.lua)
- [Isaac/Core/Player/Events.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Player/Events.lua)
- [Isaac/Core/Room/PositionUtils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/PositionUtils.lua)
- [Isaac/Core/Room/RoomInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua)
- [Isaac/Linker/Custom/GameEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/GameEffects.lua)
- [Isaac/Linker/Custom/PlayerEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/PlayerEffects.lua)
- [Isaac/Linker/Custom/RoomMechanics.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/RoomMechanics.lua)
- [Isaac/Linker/Room.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua)
- [Isaac/Linker/RoomTransition.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/RoomTransition.lua)
- [LuaEngine/Callbacks.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LuaEngine/Callbacks.lua)

The purpose of this page is to detail the architectural layout, memory representations, initialization routines, spatial utilities, transition handlers, and custom mechanics associated with rooms in the `Isaac.LuaDecomps` repository. Rooms form the structural backbone of level exploration, spatial collision, and entity containment in The Binding of Isaac: Repentance.

* * *

## 1\. Room Component and Descriptor Layouts

The room system relies on two primary component structures: `Component.Room`, which holds the live runtime state of an active room, and `Component.RoomDescriptor`, which manages metadata for rooms across the wider floor layout.

`Component.Room` is defined with explicit memory offsets starting at `0x0` up to `0x7778` [Isaac/Components/Room/RoomComponent.lua1-101](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L1-L101) Key fields include:

- `m_isInitialized` (`0x0`) and `m_isFirstVisit` (`0x1`): Flags tracking whether the room has been populated and visited [Isaac/Components/Room/RoomComponent.lua2-3](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L2-L3)
- `m_roomDescriptor` (`0x4`): Reference to the parent descriptor [Isaac/Components/Room/RoomComponent.lua4](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L4-L4)
- `m_type` (`0x8`), `m_gridWidth` (`0xc`), `m_gridHeight` (`0x10`): Spatial dimensions and classification [Isaac/Components/Room/RoomComponent.lua5-7](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L5-L7)
- `m_topLeftBound` (`0x14`) and `m_bottomRightBound` (`0x1c`): World coordinate boundaries for entity movement [Isaac/Components/Room/RoomComponent.lua8-9](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L8-L9)
- `m_gridEntityList` (`0x24`) and `m_doors` (`0x724`): Arrays managing obstacles, interactables, and room transitions [Isaac/Components/Room/RoomComponent.lua10-11](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L10-L11)
- `m_entityList` (`0x1218`): Container managing active entities present within the room boundary [Isaac/Components/Room/RoomComponent.lua27](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L27-L27)
- Ambient audio and visual loops (`m_ambientSFX_*` from `0x6f78` to `0x6fb0`), water physics properties (`m_waterAmount`, `m_waterColor` from `0x7134` to `0x717c`), and drop/corpse lists [Isaac/Components/Room/RoomComponent.lua40-82](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L40-L82)

The interface and linker layer (`Isaac.Interface.Room`) exposes stubs and bindings for querying these memory blocks, such as `Stub.GetWaterAmount`, `Stub.GetGridHeight`, `Stub.GetGridWidth`, `Stub.GetFloorSurface`, `Stub.GetEntityList`, and `Stub.GetDoor` [Isaac/Linker/Room.lua1-38](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua#L1-L38)

```

Component.Room (0x0 - 0x7778)

m_roomDescriptor (0x4)

m_gridEntityList (0x24)

m_doors (0x724)

m_entityList (0x1218)

m_fxLayers (0x1798)

m_backdrop (0x1d34)

m_temporaryEffects (0x71f4)

Code Entity Space

Isaac/Components/Room/RoomComponent.lua

Isaac/Components/Room/RoomDescriptorComponent.lua

Isaac/Linker/Room.lua
```

_Figure 1: Natural language to code entity space mapping for Room components._

Sources: `Isaac/Components/Room/RoomComponent.lua:1-101`, `Isaac/Components/Room/RoomDescriptorComponent.lua`, `Isaac/Linker/Room.lua:1-247`

* * *

## 2\. Room Initialization Pipeline

Room setup and initialization are handled in `Isaac/Core/Room/RoomInit.lua` [Isaac/Core/Room/RoomInit.lua1-199](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua#L1-L199) When a player transitions into a new area, the engine executes `Init(room, ctx, data, desc)` [Isaac/Core/Room/RoomInit.lua152](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua#L152-L152)

The initialization sequence performs the following steps:

1. Clears temporary status effects via `ITemporaryEffects.ClearEffects` [Isaac/Core/Room/RoomInit.lua156](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua#L156-L156)
2. Resets corpse lists, output grid registers via `reset_outputs(room)`, water currents, and miscellaneous flags (`m_babyPlum_mercyTimer`, `m_genesisItems_countdown`, `m_lavaIntensity`) [Isaac/Core/Room/RoomInit.lua157-164](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua#L157-L164)
3. Sets up grid boundary properties based on `data.m_width` and `data.m_height` [Isaac/Core/Room/RoomInit.lua186-187](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua#L186-L187)
4. Loads or checks graphic resources like the light gradient sprite (`gfx/LightGradient.anm2`) with custom blend and filter configurations [Isaac/Core/Room/RoomInit.lua189-198](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua#L189-L198)

Mechanics hooks such as `Mechanics_on_room_restore`, `Mechanics_on_first_visit`, and `Mechanics_post_room_init` handle specialized spawn conditions such as Womb teleports, Card Reading portals, stairway generation, and room graphic rendering [Isaac/Core/Room/RoomInit.lua40-68](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/RoomInit.lua#L40-L68)

Sources: `Isaac/Core/Room/RoomInit.lua:1-199`

* * *

## 3\. Position Utilities and Geometry

Spatial queries, random placement, and tile snapping are governed by `Room.PositionUtils` located in `Isaac/Core/Room/PositionUtils.lua` [Isaac/Core/Room/PositionUtils.lua1-108](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/PositionUtils.lua#L1-L108)

Key utility routines include:

- `GetRandomPosition(room, margin)`: Calculates valid random positions within standard rectangular rooms or complex L-shaped rooms using `IRoom.GetLRoomAreaDesc` to weight high and low sub-rectangles proportionally [Isaac/Core/Room/PositionUtils.lua11-50](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/PositionUtils.lua#L11-L50)
- `FindFreeTilePosition(room, startPos, margin)`: Iterates through the room grid to locate the nearest non-colliding tile position relative to `startPos` using `IRoom.GetGridCollisionAtPos` and `IRoom.GetGridCollision` [Isaac/Core/Room/PositionUtils.lua56-87](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/PositionUtils.lua#L56-L87)

```

GetRandomPosition()

FindFreeTilePosition()

GetLRoomAreaDesc()

GetGridCollisionAtPos()

Code Entity Space

Isaac/Core/Room/PositionUtils.lua

Isaac/Interface/Room.lua

Component.LRoomAreaDesc

GridCollisionClass
```

_Figure 2: Spatial query dependency mapping for PositionUtils._

Sources: `Isaac/Core/Room/PositionUtils.lua:1-108`, `Isaac/Linker/Room.lua:1-247`

* * *

## 4\. Doors, Environment FX, and Ambient Mechanics

Rooms manage dynamic environmental elements through internal component fields and linkers.

- **Doors**: Stored in `m_doors` (`GridEntityDoor[]` array of size 8 at offset `0x724`) alongside `m_doorsGridIdx` (`0x744`) [Isaac/Components/Room/RoomComponent.lua11-12](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L11-L12) Methods like `Stub.GetDoor` and `Stub.IsDoorSlotAllowed` query door availability [Isaac/Linker/Room.lua35-223](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua#L35-L223)
- **Environment FX**: Rain parameters (`m_rainPosThing`, `m_numRainEffects`, `m_rainStrength`, `m_stopRain`), lava intensity (`m_lavaIntensity`), water currents (`m_waterCurrent`), and rail networks (`m_railManager`) reside in offsets between `0x72d4` and `0x7624` [Isaac/Components/Room/RoomComponent.lua87-93](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L87-L93)
- **Ambient SFX**: Audio loops for fires, insect swarms, mega blasts, tar, blood lasers, water flows, lava, and boss mechanics are tracked via fields like `m_ambientSFX_fireBurn` (`0x6f78`) through `m_ambientSFX_animaRattle` (`0x6fb4`) [Isaac/Components/Room/RoomComponent.lua40-55](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua#L40-L55)

Sources: `Isaac/Components/Room/RoomComponent.lua:11-93`, `Isaac/Linker/Room.lua:1-247`

* * *

## 5\. Room Transitions

The `RoomTransition` subsystem handles animations, fading, surface caching, and state switches when moving between rooms. Defined via `Interface.RoomTransition` in `Isaac/Linker/RoomTransition.lua` [Isaac/Linker/RoomTransition.lua1-76](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/RoomTransition.lua#L1-L76) it exposes bindings to:

- Check animation states via `Stub.IsTeleportAnimation` and `Stub.IsActive` [Isaac/Linker/RoomTransition.lua8-21](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/RoomTransition.lua#L8-L21)
- Initiate transitions with `Stub.Start` taking room indices, directions, animation types, and target players [Isaac/Linker/RoomTransition.lua22-28](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/RoomTransition.lua#L22-L28)
- Handle boss introductions via `Stub.StartBossIntro` [Isaac/Linker/RoomTransition.lua37-39](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/RoomTransition.lua#L37-L39)
- Manage rendering, input processing, and screen fading values via `Stub.Render`, `Stub.ProcessInput`, and `Stub.GetFadeValue` [Isaac/Linker/RoomTransition.lua45-74](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/RoomTransition.lua#L45-L74)

Sources: `Isaac/Linker/RoomTransition.lua:1-76`

* * *

## 6\. Room Mechanics Extensions

Custom mechanics specific to rooms—such as challenge checks and shop restock logic—are exposed through `Interface.RoomMechanics` [Isaac/Linker/Custom/RoomMechanics.lua1-9](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/RoomMechanics.lua#L1-L9)

This linker delegates specific behaviors to content scripts:

- `Interface.IsAmbushChallenge` maps to `Misc.IsAmbushChallenge` [Isaac/Linker/Custom/RoomMechanics.lua8](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/RoomMechanics.lua#L8-L8)
- `Interface.ShouldTriggerRestock` maps to `Shop.ShouldTriggerRestock` [Isaac/Linker/Custom/RoomMechanics.lua9](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Custom/RoomMechanics.lua#L9-L9) which interacts with shop items during purchase execution [Isaac/Core/Pickup/ShopItem.lua74-78](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/ShopItem.lua#L74-L78)

Sources: `Isaac/Linker/Custom/RoomMechanics.lua:1-9`, `Isaac/Core/Pickup/ShopItem.lua:1-88`

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface#room-component-and-interface)
- [1\. Room Component and Descriptor Layouts](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface#1-room-component-and-descriptor-layouts)
- [2\. Room Initialization Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface#2-room-initialization-pipeline)
- [3\. Position Utilities and Geometry](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface#3-position-utilities-and-geometry)
- [4\. Doors, Environment FX, and Ambient Mechanics](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface#4-doors-environment-fx-and-ambient-mechanics)
- [5\. Room Transitions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface#5-room-transitions)
- [6\. Room Mechanics Extensions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface#6-room-mechanics-extensions)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 4.2 Grid Entities

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Grid Entities

Relevant source files

- [Isaac/Components/GridEntity/GridEntityComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua)
- [Isaac/Components/GridEntity/GridEntityDescComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua)
- [Isaac/Components/GridEntity/GridEntityRockComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua)
- [Isaac/Interface/GridEntity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/GridEntity.lua)
- [Isaac/Interface/GridEntity\_Rock.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/GridEntity_Rock.lua)
- [Isaac/Linker/GridEntity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua)
- [Isaac/Linker/GridEntity\_Rock.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity_Rock.lua)

## Purpose and Scope

This page covers the technical implementation of grid entities within `Isaac.LuaDecomps`. It documents the base `Component.GridEntity` and concrete subclass `Component.GridEntity.Rock` layouts, their memory offset structures, associated descriptors (`Component.GridEntityDesc`), linker stubs in `Isaac/Linker/`, and interface declarations. Additionally, it details collision classes, environmental checking functions, pathing compatibility predicates, and damage pipelines governing static world elements.

* * *

## 1\. Grid Entity Architecture and Memory Layout

The grid system models discrete tiles inside a room's grid index array. At the base level, `Component.GridEntity` defines core callbacks and state fields with strict hexadecimal memory offsets.

The memory layout of a base grid entity includes descriptor pointers, grid index locations, internal random number generators, collision classifications, and rendering sprites:

- `m_desc`: `Component.GridEntityDesc` located at offset `0x4` [Isaac/Components/GridEntity/GridEntityComponent.lua23](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua#L23-L23)
- `m_gridIdx`: `integer` located at offset `0x24` [Isaac/Components/GridEntity/GridEntityComponent.lua24](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua#L24-L24)
- `m_spawnedFrame`: `integer` located at offset `0x28` [Isaac/Components/GridEntity/GridEntityComponent.lua25](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua#L25-L25)
- `m_rng`: `RNG` located at offset `0x2c` [Isaac/Components/GridEntity/GridEntityComponent.lua26](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua#L26-L26)
- `m_collisionClass`: `EntityGridCollisionClass | integer` located at offset `0x3c` [Isaac/Components/GridEntity/GridEntityComponent.lua27](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua#L27-L27)
- `m_sprite`: `Sprite` located at offset `0x40` [Isaac/Components/GridEntity/GridEntityComponent.lua28](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua#L28-L28)

Grid entity configuration and persistence are managed via `Component.GridEntityDesc`, which records spawn identity and variant parameters:

- `m_type`: `GridEntityType | integer` at `0x0` [Isaac/Components/GridEntity/GridEntityDescComponent.lua2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L2-L2)
- `m_variant`: `integer` at `0x4` [Isaac/Components/GridEntity/GridEntityDescComponent.lua3](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L3-L3)
- `m_state`: `integer` at `0x8` [Isaac/Components/GridEntity/GridEntityDescComponent.lua4](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L4-L4)
- `m_spawnCount`: `integer` at `0xc` [Isaac/Components/GridEntity/GridEntityDescComponent.lua5](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L5-L5)
- `m_spawnSeed`: `integer` at `0x10` [Isaac/Components/GridEntity/GridEntityDescComponent.lua6](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L6-L6)
- `m_varData`: `integer` at `0x14` [Isaac/Components/GridEntity/GridEntityDescComponent.lua7](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L7-L7)
- `m_initialized`: `boolean` at `0x18` [Isaac/Components/GridEntity/GridEntityDescComponent.lua8](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L8-L8)
- `m_variableSeed`: `integer` at `0x1c` [Isaac/Components/GridEntity/GridEntityDescComponent.lua9](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L9-L9)

### Diagram: Grid Entity Component and Descriptor Layout

```
Component.GridEntityDesc

Component.GridEntity

+0x4

+0x24

+0x2c

+0x3c

+0x40

+0x0

+0x4

+0x8

+0x10

+0x14

Component.GridEntity

Component.GridEntityDesc

m_gridIdx integer

m_rng RNG

m_collisionClass EntityGridCollisionClass

m_sprite Sprite

m_type GridEntityType

m_variant integer

m_state integer

m_spawnSeed integer

m_varData integer
```

Sources: [Isaac/Components/GridEntity/GridEntityComponent.lua1-28](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityComponent.lua#L1-L28) [Isaac/Components/GridEntity/GridEntityDescComponent.lua1-9](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityDescComponent.lua#L1-L9)

* * *

## 2\. Interface Stubs and Linker Dispatch

The `Isaac/Linker/GridEntity.lua` file bridges engine execution with Lua through `Interface.GridEntity` stubs [Isaac/Linker/GridEntity.lua1-198](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L1-L198) These functions handle lifecycle events, utility lookups, and positional queries.

Key execution routines exposed by the linker include:

- **Lifecycle & Initialization**: `Stub.Constructor`, `Stub.Init`, `Stub.Init_Desc`, `Stub.PostInit`, `Stub.Update`, `Stub.Render`, `Stub.Destroy`, and `Stub.Free` [Isaac/Linker/GridEntity.lua34-56](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L34-L56)
- **Properties & State**: `Stub.GetSprite`, `Stub.GetCollisionClass`, `Stub.GetGridIndex`, `Stub.SetState`, `Stub.GetVarData`, `Stub.SetVarData`, and `Stub.GetRNG` [Isaac/Linker/GridEntity.lua10-26](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L10-L26)
- **Damage & Environment**: `Stub.hurt_func`, `Stub.hurt_surroundings`, `Stub.Hurt`, `Stub.IsBreakableRock`, and `Stub.GridEntityProjectileBreakEffects` [Isaac/Linker/GridEntity.lua73-100](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L73-L100)

### Diagram: Grid Entity Pipeline Architecture

```
Code Entity Space

Requires

Executes

Modifies

Contains

Interface.GridEntity

Isaac/Linker/GridEntity.lua

Stub.Update / Stub.Init

Component.GridEntity

Component.GridEntityDesc
```

Sources: [Isaac/Linker/GridEntity.lua1-198](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L1-L198) [Isaac/Interface/GridEntity.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/GridEntity.lua#L1-L2)

* * *

## 3\. Concrete Subclasses: Rocks (`GridEntity_Rock`)

Rocks are implemented via `Component.GridEntity.Rock`, which extends `Component.GridEntity` with specific fields for animations, rubble generation, and chain reactions [Isaac/Components/GridEntity/GridEntityRockComponent.lua1-6](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua#L1-L6)

Memory fields specific to `Component.GridEntity.Rock`:

- `m_anim`: `string` at offset `0x154` [Isaac/Components/GridEntity/GridEntityRockComponent.lua2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua#L2-L2)
- `m_rubbleAnim`: `string` at offset `0x16c` [Isaac/Components/GridEntity/GridEntityRockComponent.lua3](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua#L3-L3)
- `m_rubbleRelated`: `Vector[] [2]` at offset `0x184` [Isaac/Components/GridEntity/GridEntityRockComponent.lua4](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua#L4-L4)
- `m_frameCount`: `integer` at offset `0x190` [Isaac/Components/GridEntity/GridEntityRockComponent.lua5](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua#L5-L5)
- `m_lastState`: `integer` at offset `0x194` [Isaac/Components/GridEntity/GridEntityRockComponent.lua6](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua#L6-L6)

The linker `Isaac/Linker/GridEntity_Rock.lua` exposes rock-specific behaviors such as `Stub.GetRubbleAnim`, `Stub.UpdateNeighbors`, `Stub.TrySpawnWorms`, `Stub.TrySpawnLadder`, `Stub.SpawnDrops`, and `Stub.TriggerChainRocks` [Isaac/Linker/GridEntity\_Rock.lua8-101](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity_Rock.lua#L8-L101)

Sources: [Isaac/Components/GridEntity/GridEntityRockComponent.lua1-6](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/GridEntity/GridEntityRockComponent.lua#L1-L6) [Isaac/Linker/GridEntity\_Rock.lua1-125](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity_Rock.lua#L1-L125) [Isaac/Interface/GridEntity\_Rock.lua1-2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/GridEntity_Rock.lua#L1-L2)

* * *

## 4\. Collision Classes, Pathing, and Environment

Grid entities participate in collision evaluation and path validation through dedicated stub functions in `Isaac/Linker/GridEntity.lua` [Isaac/Linker/GridEntity.lua102-120](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L102-L120)

### Collision and Pathing Methods

- `Stub.GridCollisionClassCollidesWithGridType(ent, grid)`: Evaluates matrix intersections between entity grid collision classes and static grid types [Isaac/Linker/GridEntity.lua102-105](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L102-L105)
- `Stub.IsEasyCrushableOrWalkable(ctx, gridEntity)`: Validates if the tile permits traversal or easy destruction [Isaac/Linker/GridEntity.lua107-110](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L107-L110)
- `Stub.IsDangerousCrushableOrWalkable(ctx, gridEntity)`: Checks if crushing/walking carries hazard conditions [Isaac/Linker/GridEntity.lua112-115](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L112-L115)
- `Stub.IsCrushableOrWalkable(ctx, gridEntity)`: General fallback predicate for movement pathfinders [Isaac/Linker/GridEntity.lua117-120](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L117-L120)

### Damage Plumbing

When explosions or attacks target grid entities, `Stub.hurt_func` handles direct damage application while `Stub.hurt_surroundings` propagates radial damage to neighboring grid elements based on distance parameters, damage flags, and ignore-collision overrides [Isaac/Linker/GridEntity.lua71-90](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L71-L90)

Sources: [Isaac/Linker/GridEntity.lua71-120](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GridEntity.lua#L71-L120)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#grid-entities)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#purpose-and-scope)
- [1\. Grid Entity Architecture and Memory Layout](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#1-grid-entity-architecture-and-memory-layout)
- [Diagram: Grid Entity Component and Descriptor Layout](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#diagram-grid-entity-component-and-descriptor-layout)
- [2\. Interface Stubs and Linker Dispatch](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#2-interface-stubs-and-linker-dispatch)
- [Diagram: Grid Entity Pipeline Architecture](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#diagram-grid-entity-pipeline-architecture)
- [3\. Concrete Subclasses: Rocks (\`GridEntity\_Rock\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#3-concrete-subclasses-rocks-gridentity_rock)
- [4\. Collision Classes, Pathing, and Environment](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#4-collision-classes-pathing-and-environment)
- [Collision and Pathing Methods](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#collision-and-pathing-methods)
- [Damage Plumbing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities#damage-plumbing)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 4.3 Level Generation

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Level Generation

Relevant source files

- [General/XY.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/XY.lua)
- [Isaac/Components/Level/LevelGeneratorComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Level/LevelGeneratorComponent.lua)
- [Isaac/Components/Level/LevelGeneratorRoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Level/LevelGeneratorRoomComponent.lua)
- [Isaac/Core/Level/LevelGenerator/Constants.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Level/LevelGenerator/Constants.lua)
- [Isaac/Core/Level/LevelGenerator/SecretRooms.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Level/LevelGenerator/SecretRooms.lua)
- [Isaac/Core/Level/LevelGenerator/Utils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Level/LevelGenerator/Utils.lua)
- [Isaac/Core/Pickup/Chest.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/Chest.lua)
- [Isaac/Core/Pickup/Properties.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Pickup/Properties.lua)
- [Isaac/Interface/LevelGenerator.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/LevelGenerator.lua)
- [Isaac/Linker/LevelGenerator.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/LevelGenerator.lua)

## 1\. Purpose and Scope

This page covers the technical implementation of level generation within `Isaac.LuaDecomps`. It documents the data structures, interface stubs, spatial mathematics, and generation routines responsible for constructing floor layouts, managing room positioning, determining door constraints, and placing special rooms (such as Secret and Ultra-Secret rooms).

* * *

## 2\. LevelGenerator Component Layout

The core structural state of a generated floor is defined by `Component.LevelGenerator`, initialized with a random seed and default grid masks \[Isaac/Components/Level/LevelGeneratorComponent.lua:16-43\].

```

```

### Key Fields:

- `m_rng`: `RNG` instance initialized with seed and offset 35 \[Isaac/Components/Level/LevelGeneratorComponent.lua:29\].
- `m_allowedShapes`: Bitmask representing allowed room shapes \[Isaac/Components/Level/LevelGeneratorComponent.lua:30\].
- `m_occupiedPositions`: Fixed-size array of 169 integers mapping 13x13 grid slots to room indices (-1 if free) \[Isaac/Components/Level/LevelGeneratorComponent.lua:4, 23\].
- `m_blockedPositions`: Fixed-size boolean array of 169 entries indicating prohibited grid cells \[Isaac/Components/Level/LevelGeneratorComponent.lua:5, 24\].
- `m_rooms`: Array storing instantiated `Component.LevelGenerator.Room` objects \[Isaac/Components/Level/LevelGeneratorComponent.lua:6\].

Sources: [Isaac/Components/Level/LevelGeneratorComponent.lua1-43](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Level/LevelGeneratorComponent.lua#L1-L43)

* * *

## 3\. Room Component and Geometry

Individual rooms within the generator topology are modeled by `Component.LevelGenerator.Room`, capturing spatial dimensions, grid coordinates, and connectivity data \[Isaac/Components/Level/LevelGeneratorRoomComponent.lua:8-23\].

```

```

Rooms are instantiated via `Module.New(position, shape)` which calculates horizontal and vertical spans using `Core.LevelGenerator.Constants` \[Isaac/Components/Level/LevelGeneratorRoomComponent.lua:26-49\].

Sources: [Isaac/Components/Level/LevelGeneratorRoomComponent.lua1-61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Level/LevelGeneratorRoomComponent.lua#L1-L61) [Isaac/Core/Level/LevelGenerator/Constants.lua7-35](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Level/LevelGenerator/Constants.lua#L7-L35)

* * *

## 4\. Interface Stubs and Linkers

The interface layer `Interface.LevelGenerator` exposes entrypoints for generation control, room creation, dead-end calculations, and validation \[Isaac/Linker/LevelGenerator.lua:1-128\].

```

```

### Stub Methods and Delegations:

- `Stub.Generate`: High-level floor generation runner \[Isaac/Linker/LevelGenerator.lua:24\].
- `Stub.CreateRoom`: Allocates and registers a room at coordinates `(x, y)` \[Isaac/Linker/LevelGenerator.lua:33\].
- `Interface.GetNewSecretRoom` & `Interface.GetNewUltraSecretRoom`: Delegated directly to `Isaac.Core.Level.LevelGenerator.SecretRooms` \[Isaac/Linker/LevelGenerator.lua:102-103\].
- Utility bindings like `Interface.index`, `Interface.is_pos_free`, and `Interface.get_room_placement_offsets` map directly to `Isaac.Core.Level.LevelGenerator.Utils` \[Isaac/Linker/LevelGenerator.lua:114-117\].

Sources: [Isaac/Linker/LevelGenerator.lua1-128](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/LevelGenerator.lua#L1-L128)

* * *

## 5\. Spatial Utilities and Grid Indexing

Grid coordinate management relies on `Component.XY` \[General/XY.lua:7-54\] and helper functions in `Isaac.Core.Level.LevelGenerator.Utils` \[Isaac/Core/Level/LevelGenerator.Utils:1-188\].

```

```

### Key Spatial Operations:

- `Index(xy)`: Translates a 2D `Component.XY` coordinate into a linear grid index `0` through `168` for a 13x13 floor grid, returning `-1` if out of bounds \[Isaac/Core/Level/LevelGenerator/Utils.lua:62-71\].
- `HasShapeSlot(shape, door, ignoreClosetLimits)`: Validates whether a given room shape supports a specific door slot \[Isaac/Core/Level/LevelGenerator/Utils.lua:119-137\].
- `GetDoorSourcePosition` & `GetDoorTargetPosition`: Computes exact coordinate vectors for door placement and inter-room traversal \[Isaac/Core/Level/LevelGenerator/Utils.lua:144-176\].

Sources: [General/XY.lua1-86](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/XY.lua#L1-L86) [Isaac/Core/Level/LevelGenerator/Utils.lua1-188](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Level/LevelGenerator/Utils.lua#L1-L188)

* * *

## 6\. Secret and Ultra-Secret Room Generation

The placement of Secret and Ultra-Secret rooms is handled by `Isaac.Core.Level.LevelGenerator.SecretRooms` \[Isaac/Core/Level/LevelGenerator/SecretRooms.lua:1-184\].

```

```

### Strategy Execution:

- `Secret_get_origins`: Evaluates surrounding room accessibility to ensure standard secret room connectivity \[Isaac/Core/Level/LevelGenerator/SecretRooms.lua:95-125\].
- `UltraSecret_get_origins`: Validates dead space constraints and verifies adjacent red room alignment using `ULTRA_SECRET_ORIGIN_POSITION_OFFSETS` \[Isaac/Core/Level/LevelGenerator/SecretRooms.lua:12-21, 145-184\].

Sources: [Isaac/Core/Level/LevelGenerator/SecretRooms.lua1-184](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Level/LevelGenerator/SecretRooms.lua#L1-L184)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#level-generation)
- [1\. Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#1-purpose-and-scope)
- [2\. LevelGenerator Component Layout](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#2-levelgenerator-component-layout)
- [Key Fields:](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#key-fields)
- [3\. Room Component and Geometry](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#3-room-component-and-geometry)
- [4\. Interface Stubs and Linkers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#4-interface-stubs-and-linkers)
- [Stub Methods and Delegations:](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#stub-methods-and-delegations)
- [5\. Spatial Utilities and Grid Indexing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#5-spatial-utilities-and-grid-indexing)
- [Key Spatial Operations:](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#key-spatial-operations)
- [6\. Secret and Ultra-Secret Room Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#6-secret-and-ultra-secret-room-generation)
- [Strategy Execution:](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation#strategy-execution)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

Syntax error in textmermaid version 11.7.0

Syntax error in textmermaid version 11.7.0

Syntax error in textmermaid version 11.7.0

Syntax error in textmermaid version 11.7.0

Syntax error in textmermaid version 11.7.0

---

## 5 Game State And Managers

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Game State and Managers

Relevant source files

- [Engine/Interface/GraphicsManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/GraphicsManager.lua)
- [Isaac/Components/Game/GameComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua)
- [Isaac/Core/Game/Render.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua)
- [Isaac/Linker/BossOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/BossOverlay.lua)
- [Isaac/Linker/Manager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Manager.lua)
- [Isaac/Render.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Render.lua)
- [Isaac/Utils/Common.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Common.lua)

The Game State and Managers section provides a high-level overview of the engine's core global state coordinators: `Component.Manager` and `Component.Game`. These objects regulate execution flow, menu states, active run loops, item configurations, procedural generation inputs, and data persistence across the engine lifecycle.

As a parent page, this document summarizes the subsystem interactions and links to dedicated child pages for deep technical specifications.

* * *

### Global State Architecture

```
switches state via eState

initializes via StartNewGame

m_level

m_hud

m_itemPool

m_bossPool

Component.Manager (Isaac/Linker/Manager.lua)

Isaac/Render.lua

Component.Game (GameComponent.lua)

Component.Room

Component.HUD

Component.ItemPool

Component.BossPool
```

Sources: `Isaac/Linker/Manager.lua:1-223`, `Isaac/Components/Game/GameComponent.lua:1-96`, `Isaac/Render.lua:25-45`

* * *

## 5.1 Manager Component and Startup

The `Component.Manager` structure serves as the top-level singleton controller for application state, window resizing, input polling, hotkeys, cutscenes, and transitioning between menus, nightmare scenes, and active gameplay. Global entrypoints such as `Stub.StartNewGame` and `Stub.RestartGame` initialize state contexts via `Context.Common` \[Isaac/Linker/Manager.lua:180-190\].

For technical details on memory maps, interface stubs, fade transitions, and the menu manager, see [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup).

Sources: `Isaac/Linker/Manager.lua:1-223`, `Isaac/Render.lua:25-45`

* * *

## 5.2 Game Component and Run Lifecycle

```

Component.Game

m_playerManager

m_seeds

m_scoreSheet

m_pauseScreen

m_gameOver

m_ambush
```

Sources: `Isaac/Components/Game/GameComponent.lua:1-96`, `Isaac/Core/Game/Render.lua:39-61`

The `Component.Game` structure orchestrates an active run. It holds nested layout components such as level descriptors, player managers, score sheets, pause states, and game-over routines \[Isaac/Components/Game/GameComponent.lua:1-96\]. Rendering routines coordinate post-processing effects and overlay panels through the main game render pipeline \[Isaac/Core/Game/Render.lua:39-61\].

For detailed memory layouts, run start procedures, metrics, and ambush tracking, see [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle).

Sources: `Isaac/Components/Game/GameComponent.lua:1-96`, `Isaac/Core/Game/Render.lua:39-61`

* * *

## 5.3 Item Pools, Item Config and Boss Pools

Item distribution, item availability logic, and boss encounter tracking are managed through specialized subsystems attached directly to the game context. Fields like `m_itemPool` and `m_bossPool` manage dynamic weighting, item blacklisting, and configuration loading \[Isaac/Components/Game/GameComponent.lua:5-6\].

For comprehensive documentation on pool weights, XML-driven data parsing, and availability checks, see [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools).

Sources: `Isaac/Components/Game/GameComponent.lua:1-96`

* * *

## 5.4 Persistence, Networking and Profiles

Data persistence and networking layers bridge local user profiles with save states, procedural item generation, and run seeds. Global managers exposed via the manager interface (`Stub.GetPersistentGameData`, `Stub.GetNetManager`) handle save/restore operations and synchronization \[Isaac/Linker/Manager.lua:16-25\]. Procedural item generation parameters are maintained within `m_proceduralItemManager` \[Isaac/Components/Game/GameComponent.lua:92\].

For deep dives into save-file serialization, user profiles, seed generation mechanics, and netplay components, see [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles).

Sources: `Isaac/Components/Game/GameComponent.lua:1-96`, `Isaac/Linker/Manager.lua:1-223`

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers#game-state-and-managers)
- [Global State Architecture](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers#global-state-architecture)
- [5.1 Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers#51-manager-component-and-startup)
- [5.2 Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers#52-game-component-and-run-lifecycle)
- [5.3 Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers#53-item-pools-item-config-and-boss-pools)
- [5.4 Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers#54-persistence-networking-and-profiles)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 5.1 Manager Component And Startup

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Manager Component and Startup

Relevant source files

- [Engine/Interface/GraphicsManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/GraphicsManager.lua)
- [Isaac/Components/Manager/ManagerComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/ManagerComponent.lua)
- [Isaac/Core/Manager/Fade.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Manager/Fade.lua)
- [Isaac/Linker/Manager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Manager.lua)
- [Isaac/Linker/MenuManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/MenuManager.lua)
- [Isaac/Linker/ModManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ModManager.lua)
- [Isaac/Linker/NightmareScene.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/NightmareScene.lua)
- [Isaac/Linker/PlayerManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua)
- [Isaac/Linker/ProceduralItemManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ProceduralItemManager.lua)
- [Isaac/Linker/Seeds.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua)
- [Isaac/ModManager/LoadConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/ModManager/LoadConfig.lua)
- [Isaac/Render.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Render.lua)
- [Isaac/StateSetup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/StateSetup.lua)
- [Isaac/Utils/Common.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Common.lua)

### Purpose and Scope

This page covers the technical design and implementation of the **Manager Component** (`Component.Manager`), its interface stubs and linker bindings (`Interface.Manager`), the startup and run initiation routines (`StartNewGame`, `RestartGame`, `execute_start_menu`), window and render management (`Isaac/Render.lua`), screen fades (`Isaac/Core/Manager/Fade.lua`), and integration with downstream subsystems like the Menu Manager.

* * *

### Component.Manager Memory Map

The manager memory layout represents the top-level state machine and engine supervisor for The Binding of Isaac: Repentance. Memory offset annotations in `Isaac/Components/Manager/ManagerComponent.lua` define the precise byte alignment of major subsystems, configuration stores, rendering assets, and state flags.

Key regions within `Component.Manager` include:

- **State Control (`0x0` \- `0x10`)**: Tracks state change flags (`m_changeStateTo4` at `0x0`), current engine state (`m_state` at `0x8`), previous state (`m_previousState_qqq` at `0xc`), and the active save slot (`m_currentSaveSlot` at `0x10`) [Isaac/Components/Manager/ManagerComponent.lua2-5](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/ManagerComponent.lua#L2-L5)
- **Core Subsystems (`0x14` \- `0x29fd8`)**: Holds pointers to persistent data (`m_persistentGameData` at `0x14`), game state (`m_gameState` at `0xf34`), cutscenes, nightmare scenes, achievement overlays, music and sound effect managers, item and entity configurations, and challenge parameters [Isaac/Components/Manager/ManagerComponent.lua6-17](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/ManagerComponent.lua#L6-L17)
- **Modding and Localization (`0x29fd8` \- `0x4a264`)**: Manages the mod manager instance (`m_modManager` at `0x29fd8`), string tables, frame counters, and unlock metrics [Isaac/Components/Manager/ManagerComponent.lua18-22](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/ManagerComponent.lua#L18-L22)
- **Window, UI, and Input Resources (`0x4a26c` \- `0x20a9ac`)**: Stores UI fonts, button maps, cursor sprites (`m_cursor_sprite` at `0x1ea840`), cursor coordinates (`m_cursor_position` at `0x1ea954`), window focus flags, daily challenge configuration, network flags, and the network manager (`m_netManager` at `0x20a9ac`) [Isaac/Components/Manager/ManagerComponent.lua23-78](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/ManagerComponent.lua#L23-L78)

Sources: `Isaac/Components/Manager/ManagerComponent.lua:1-78` ()

* * *

### Interface.Manager Stubs and Linker Layer

The linker module `Isaac/Linker/Manager.lua` bridges the underlying C++ / engine component memory layout with Lua-expressed functional interfaces (`Interface.Manager`). It exposes accessor routines for subsystems and lifecycle hooks.

```

Isaac/Linker/Manager.lua

Component.Manager Memory Map

Subsystem Getters

Lifecycle & State Execution

Stub.GetModManager

Stub.GetNetManager

Stub.GetSFXManager

Stub.GetPersistentGameData

Stub.GetEntityConfig

Stub.GetMusicManager

Stub.GetItemConfig

Stub.GetStringTable

Stub.Init

Stub.Update

Stub.StartNewGame

Stub.RestartGame

Stub.execute_start_menu

Stub.SaveGameState
```

_Figure 1: Manager Subsystem Architecture linking natural concepts to `Isaac/Linker/Manager.lua` symbols._

Sources: `Isaac/Linker/Manager.lua:1-223` ()

* * *

### Startup Sequence: StateSetup and ExecuteStartGame

The startup plumbing coordinates how a run initializes from the main menu or a saved state.

- **`StartNewGame`**: Initialized via `Stub.StartNewGame`, taking a player type, challenge ID, seeds component, and difficulty setting [Isaac/Linker/Manager.lua175-180](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Manager.lua#L175-L180) It allocates game state structures and configures initial player entities.
- **`RestartGame`**: Handled by `Stub.RestartGame`, resetting player configurations, clearing specific seed effects, and optionally progressing tracking flags like the Scared Heart unlock counter [Isaac/Linker/Manager.lua185-190](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Manager.lua#L185-L190)
- **`execute_start_menu`**: Manages transitions into the main menu context (`eState.STATE_MENU`), setting up input listeners, menu rendering states, and background audio [Isaac/Linker/Manager.lua221-223](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Manager.lua#L221-L223)

Sources: `Isaac/Linker/Manager.lua:175-223` (), `Isaac/StateSetup.lua:1-1` ()

* * *

### Render Pipeline, Fades, and State Dispatch

Rendering is dispatched centrally through `Isaac/Render.lua`. The top-level `Render` function checks frame pacing, evaluates window resize events, manages render target swaps (such as HQ4X or color correction shaders), and dispatches to the correct state render handler [Isaac/Render.lua127-186](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Render.lua#L127-L186)

```

Yes

No

Yes

No

STATE_MENU

STATE_GAME

STATE_CUTSCENE

STATE_NIGHTMARE

Render(manager)

Resize Triggered?

Recreate Surfaces
 IManager.create_surfaces

Set Render Target Screen

Use Render Surface / Filters?

Push Render Target & Bind Texture

render_game_state(manager)

Switch manager.m_state

IMenuManager.Render

IGame.Render

ICutscene.Render

INightmareScene.Render
```

_Figure 2: Game State Render Flow bridging `Isaac/Render.lua` routing logic to interface render calls._

#### Fades

Screen transitions utilize helper routines defined in `Isaac/Core/Manager/Fade.lua`.

- `GameLoad_RenderFadeIn`: Applies a normal blend mode, fills a destination quad with an alpha-interpolated black color (`KColor(0.0, 0.0, 0.0, value)`), and renders loading images via `IManager.RenderLoadImage` [Isaac/Core/Manager/Fade.lua11-18](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Manager/Fade.lua#L11-L18)
- `MenuReturn_RenderFadeOut`: Draws fade-out quad fills during transitions back to menu contexts [Isaac/Core/Manager/Fade.lua20-25](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Manager/Fade.lua#L20-L25)

Sources: `Isaac/Render.lua:1-186` (), `Isaac/Core/Manager/Fade.lua:1-35` ()

* * *

### Menu Manager and Subsystems

The Menu Manager interface (`Interface.MenuManager`) is invoked directly from the render switch statement when `manager.m_state` equals `eState.STATE_MENU` [Isaac/Render.lua31-34](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Render.lua#L31-L34) It coordinates navigation across save slots, options, bestiaries, and character selection menus. Concurrently, options flags housed within `manager.m_options` dictate filtering, V-sync, window dimensions, gamma correction, and input mappings [Isaac/Components/Manager/ManagerComponent.lua13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/ManagerComponent.lua#L13-L13)

Sources: `Isaac/Render.lua:31-34` (), `Isaac/Components/Manager/ManagerComponent.lua:1-78` ()

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#manager-component-and-startup)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#purpose-and-scope)
- [Component.Manager Memory Map](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#componentmanager-memory-map)
- [Interface.Manager Stubs and Linker Layer](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#interfacemanager-stubs-and-linker-layer)
- [Startup Sequence: StateSetup and ExecuteStartGame](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#startup-sequence-statesetup-and-executestartgame)
- [Render Pipeline, Fades, and State Dispatch](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#render-pipeline-fades-and-state-dispatch)
- [Fades](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#fades)
- [Menu Manager and Subsystems](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup#menu-manager-and-subsystems)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 5.2 Game Component And Run Lifecycle

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Game Component and Run Lifecycle

Relevant source files

- [Isaac/Components/Entity/KnifeComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/KnifeComponent.lua)
- [Isaac/Components/Game/GameComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua)
- [Isaac/Components/Game/ScoreSheetComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ScoreSheetComponent.lua)
- [Isaac/Core/Game/Render.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua)
- [Isaac/Core/Game/Start.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua)
- [Isaac/Core/Game/Static.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Static.lua)
- [Isaac/Core/Npc/NpcInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Npc/NpcInit.lua)
- [Isaac/Linker/BossOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/BossOverlay.lua)
- [Isaac/Linker/Entity\_Tear.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Tear.lua)
- [Isaac/Linker/Game.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Game.lua)
- [Isaac/Linker/GameOver.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GameOver.lua)
- [Isaac/Linker/PauseScreen.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PauseScreen.lua)

This page details the implementation of `Component.Game`, the core state container managing active runs, top-level subsystem coordination, game initialization, run metrics, scoring, pause logic, and game-over flows in `Isaac.LuaDecomps`.

* * *

## 1\. Game Component Memory Map and Subsystems (`Component.Game`)

The `Component.Game` structure represents the master container for an active run. It aggregates subsystem pointers, timers, graphic effect variables, progression tracking fields, and flags aligned with memory offsets from the original engine binary [Isaac/Components/Game/GameComponent.lua1-96](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L1-L96)

Key field groupings include:

- **Subsystem Managers**: `m_level`, `m_itemPool`, `m_bossPool`, `m_roomTransition`, `m_stageTransition`, `m_playerManager`, `m_seeds`, `m_console`, `m_itemOverlay`, `m_bossOverlay`, `m_gameOver`, `m_leaderboard`, `m_hud`, `m_pauseScreen`, `m_minimap`, `m_ambush`, `m_dailyChallenge`, `m_scoreSheet`, `m_proceduralItemManager` [Isaac/Components/Game/GameComponent.lua2-92](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L2-L92)
- **Timers and Counters**: `m_frameCount`, `m_timeCounter`, `m_bossRushParTime`, `m_blueWombParTime`, `m_screenShake_countdown`, `m_ascentTimer` [Isaac/Components/Game/GameComponent.lua21-25](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L21-L25)
- **State Flags and Metrics**: `m_gameStateFlags`, `m_debugFlags`, `m_challenge`, `m_treasureRoomsVisited`, `m_planetariumsVisited`, `m_devilRoomDeals`, `m_donationModGreed` [Isaac/Components/Game/GameComponent.lua39-52](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L39-L52)

```

Component.Game

m_level Component.Level

m_itemPool Component.ItemPool

m_bossPool Component.BossPool

m_playerManager Component.PlayerManager

m_seeds Component.Seeds

m_hud Component.HUD

m_pauseScreen Component.PauseScreen

m_gameOver Component.GameOver

m_ambush Component.Ambush

m_scoreSheet Component.ScoreSheet

m_proceduralItemManager Component.ProceduralItemManager
```

_Figure 1.1: Component-to-Code mapping of `Component.Game` sub-allocations._

Sources: [Isaac/Components/Game/GameComponent.lua1-96](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L1-L96)

* * *

## 2\. Run Initialization and Game Start (`GameStart`)

Run creation is orchestrated by `Gameplay.GameStart` (`Isaac/Core/Game/Start.lua`), which initializes a fresh session using provided configuration parameters, difficulty levels, challenges, and seed structures [Isaac/Core/Game/Start.lua26-100](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L26-L100)

The initialization pipeline proceeds through the following sequence:

1. Assigns `game.m_difficulty` and `game.m_challenge` [Isaac/Core/Game/Start.lua29-30](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L29-L30)
2. Loads HUD graphics via `IHud.LoadGraphics` [Isaac/Core/Game/Start.lua35](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L35-L35)
3. Copies and populates seed data into `game.m_seeds`, handling challenge-specific seed overrides [Isaac/Core/Game/Start.lua42-54](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L42-L54)
4. Initializes the fortune RNG (`game.m_fortuneRNG`) [Isaac/Core/Game/Start.lua56-57](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L56-L57)
5. Disables achievements if running a modded state or specific challenges [Isaac/Core/Game/Start.lua59-60](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L59-L60)
6. Resets `game.m_proceduralItemManager`, initializes `game.m_itemPool` (loading `itempools.xml` via `IModManager.TryRedirectPath`), and initializes `game.m_bossPool` [Isaac/Core/Game/Start.lua65-72](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L65-L72)
7. Initializes the player manager (`game.m_playerManager`) and generates level configuration [Isaac/Core/Game/Start.lua75-84](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L75-L84)
8. Triggers save-state persistence, temporary room effects, fades, and dispatches the `LuaCallbacks.PostGameStart` callback [Isaac/Core/Game/Start.lua87-99](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L87-L99)

```
LuaCallbacksILevelIItemPoolISeedsComponent.GameGameplay.GameStartContext.managerLuaCallbacksILevelIItemPoolISeedsComponent.GameGameplay.GameStartContext.managerStart(game, ctx, playerType, challenge, seeds, difficulty)Set difficulty & challenge flagsCopy & configure start seedsInit(game.m_itemPool, ctx, seed, xmlPath)SetNextStage() & Init()SaveGameState(ctx)PostGameStart(false)
```

_Figure 2.1: Sequence flow for session startup via `Gameplay.GameStart`._

Sources: [Isaac/Core/Game/Start.lua26-100](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Start.lua#L26-L100)

* * *

## 3\. Game Statics and Rendering Integration (`Game.Static` & `Render`)

Top-level rendering pass orchestration is managed by `Isaac/Core/Game/Render.lua`, backed by procedural surfaces stored in `Game.Static` (`Isaac/Core/Game/Static.lua`) [Isaac/Core/Game/Render.lua39-193](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L39-L193)

### Surface Management and Window Resize

When `game.m_triggerWindowResize` is evaluated as true, surface targets (`PixelatedSurface`, `BloomSurface`, `OldTVSurface`, `HallucinationSurface`, `ColorModSurface`) are reallocated via `IGame.CreateSurfaces(game)` and subsystem size updates are propagated [Isaac/Core/Game/Render.lua43-61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L43-L61)

### Frame Render Order

The rendering pipeline processes layers in strict Z-order and post-processing depth:

1. **Post-Processing Target Capture**: OldTV, Hallucination, Pixelation, Bloom, and ColorMod render targets are pushed and bound if active [Isaac/Core/Game/Render.lua67-101](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L67-L101)
2. **World Rendering**: `IRoom.Render` or `IRoomTransition.Render` executes, followed by `LuaCallbacks.PostRender()` [Isaac/Core/Game/Render.lua106-112](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L106-L112)
3. **Overlays and UI**: Debug renderer, HUD, stage transitions, item overlays, boss overlays, pause screens, game-over prompts, and leaderboards are drawn [Isaac/Core/Game/Render.lua126-141](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L126-L141)
4. **Shader Application and Present**: Shaders (Bloom, Pixelation, Hallucination, OldTV) and color modifications are finalized and presented to the screen [Isaac/Core/Game/Render.lua143-178](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L143-L178)

```

Yes

No

Game.Render(game)

game.m_triggerWindowResize

Recreate Surfaces & Mod Surfaces

Push Post-Processing RenderTargets

IRoom.Render() & PostRender Callback

Render HUD, BossOverlay, PauseScreen, GameOver

Apply Shaders & Present RenderTargets
```

_Figure 3.1: Data flow for frame rendering pipeline in `Isaac/Core/Game/Render.lua`._

Sources: `[Isaac/Core/Game/Render.lua:39-193]`, [Isaac/Core/Game/Static.lua1-17](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Static.lua#L1-L17)

* * *

## 4\. Score Sheet and Run Metrics (`Component.ScoreSheet`)

Run scoring, penalties, and run metrics are tracked within `Component.ScoreSheet` (`Isaac/Components/Game/ScoreSheetComponent.lua`) [Isaac/Components/Game/ScoreSheetComponent.lua1-23](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ScoreSheetComponent.lua#L1-L23)

Key fields include:

- **Bonuses**: `m_StageBonus`, `m_SchwagBonus`, `m_LambBonus`, `m_MegaSatanBonus`, `m_RushBonus`, `m_ExplorationBonus` [Isaac/Components/Game/ScoreSheetComponent.lua2-8](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ScoreSheetComponent.lua#L2-L8)
- **Penalties**: `m_DamagePenalty`, `m_TimePenalty`, `m_ItemPenalty` [Isaac/Components/Game/ScoreSheetComponent.lua9-11](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ScoreSheetComponent.lua#L9-L11)
- **Counters**: `m_TotalScore`, `m_RunTime`, `m_clearedRoomCount` (room type to cleared count array), `m_visitedRoomCount`, `m_angelsKilled`, `m_encodedGameVersion` [Isaac/Components/Game/ScoreSheetComponent.lua12-23](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ScoreSheetComponent.lua#L12-L23)

Sources: [Isaac/Components/Game/ScoreSheetComponent.lua1-23](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ScoreSheetComponent.lua#L1-L23)

* * *

## 5\. Pause Screen, Game Over, and Ambush Mechanics

### Pause Screen

Managed via `Interface.PauseScreen` (`Isaac/Linker/PauseScreen.lua`), the pause screen subsystem tracks active menus, controller disconnections, and state updates [Isaac/Linker/PauseScreen.lua1-67](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PauseScreen.lua#L1-L67) When active (`game.m_pauseScreen.m_state ~= 0`), game world updates are suspended, and `IPauseScreen.Render` / `IPauseScreen.ProcessInput` are executed [Isaac/Core/Game/Render.lua136-138](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L136-L138)

### Game Over

The game over state is driven by `Interface.GameOver` (`Isaac/Linker/GameOver.lua`), controlling death animations, run stats presentation, and collectible item sprite rendering during defeat sequences [Isaac/Linker/GameOver.lua1-42](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GameOver.lua#L1-L42) It renders after UI overlays when player health is depleted.

### Ambush and Run Metrics

Ambush encounters (boss rushes, waves, room lockdowns) are tracked under `m_ambush` (`Component.Ambush`) within `Component.Game` [Isaac/Components/Game/GameComponent.lua60](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L60-L60) It coordinates wave spawns and room door locks dynamically during combat scenarios.

Sources: `[Isaac/Components/Game/GameComponent.lua:60]`, `[Isaac/Linker/PauseScreen.lua:1-67]`, `[Isaac/Linker/GameOver.lua:1-42]`, [Isaac/Core/Game/Render.lua136-141](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L136-L141)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#game-component-and-run-lifecycle)
- [1\. Game Component Memory Map and Subsystems (\`Component.Game\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#1-game-component-memory-map-and-subsystems-componentgame)
- [2\. Run Initialization and Game Start (\`GameStart\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#2-run-initialization-and-game-start-gamestart)
- [3\. Game Statics and Rendering Integration (\`Game.Static\` & \`Render\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#3-game-statics-and-rendering-integration-gamestatic-render)
- [Surface Management and Window Resize](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#surface-management-and-window-resize)
- [Frame Render Order](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#frame-render-order)
- [4\. Score Sheet and Run Metrics (\`Component.ScoreSheet\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#4-score-sheet-and-run-metrics-componentscoresheet)
- [5\. Pause Screen, Game Over, and Ambush Mechanics](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#5-pause-screen-game-over-and-ambush-mechanics)
- [Pause Screen](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#pause-screen)
- [Game Over](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#game-over)
- [Ambush and Run Metrics](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle#ambush-and-run-metrics)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 5.3 Item Pools Item Config And Boss Pools

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Item Pools, Item Config and Boss Pools

Relevant source files

- [Engine/Lib/XML.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Lib/XML.lua)
- [General/Table.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Table.lua)
- [Isaac/Components/Config/BossComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/BossComponent.lua)
- [Isaac/Components/Config/ItemConfigComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/ItemConfigComponent.lua)
- [Isaac/Components/Config/PillEffectComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/PillEffectComponent.lua)
- [Isaac/Components/Game/BossPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/BossPoolComponent.lua)
- [Isaac/Components/Game/ItemPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ItemPoolComponent.lua)
- [Isaac/Interface/ItemConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/ItemConfig.lua)
- [Isaac/Interface/ItemPool.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/ItemPool.lua)
- [Isaac/Interface/SoundEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/SoundEffects.lua)
- [Isaac/Linker/BossPool.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/BossPool.lua)
- [Isaac/Linker/ItemConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ItemConfig.lua)
- [Isaac/Linker/ItemPool.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ItemPool.lua)
- [Isaac/Linker/SoundEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/SoundEffects.lua)

## Purpose and Scope

This section details the subsystems responsible for managing game item pools, item static configurations, and boss generation weights within `Isaac.LuaDecomps`. It covers the memory layouts, linker stubs, selection algorithms, and XML-driven data loading pipelines for collectibles, trinkets, pills, cards, item availability rules, and stage-specific boss pools.

Sources:

- `Isaac/Linker/ItemPool.lua:1-195`
- `Isaac/Components/Game/ItemPoolComponent.lua:1-57`
- `Isaac/Linker/ItemConfig.lua:1-216`
- `Isaac/Linker/BossPool.lua:1-59`

* * *

## ItemPool Component and Selection Mechanics

The `Component.ItemPool` struct (`Isaac/Components/Game/ItemPoolComponent.lua:1-16`) tracks runtime item pool states, global seeds, blacklists, and individual weights across 31 distinct item pools. The selection engine evaluates probabilities via `Interface.ItemPool` stubs (`Isaac/Linker/ItemPool.lua:1-174`).

### Memory Layout and Pool Structures

- `Component.ItemPool`: Holds `m_seed` (`0x0`), `m_pools` (`0x4`, array of 31 `Component.ItemPool.Pool`), `m_lastPool` (`0x650`), and tracking arrays for removed or blacklisted collectibles (`Isaac/Components/Game/ItemPoolComponent.lua:1-16`).
- `Component.ItemPool.Pool`: Contains `m_totalWeight` (`0x0`), `m_itemList` (`0x4`, array of `Component.ItemPool.PoolItem`), dual RNG instances (`m_rng1`, `m_rng2`), and `m_bibleUpgrade` (`Isaac/Components/Game/ItemPoolComponent.lua:17-23`).
- `Component.ItemPool.PoolItem`: Encapsulates item identity (`m_itemID`), initial and active weights (`m_initialWeight`, `m_weight`), decrease rates, removal thresholds, unlock status, and special status flags (`Isaac/Components/Game/ItemPoolComponent.lua:24-32`).

### Selection and Blacklisting Logic

Collectible selection flows through `Stub.GetCollectible` and `Stub.pick_collectible` (`Isaac/Linker/ItemPool.lua:49-63`), which factor in room blacklists, player inventories, and item availability. Room blacklists are managed via `Stub.AddRoomBlacklist` and `Stub.ResetRoomBlacklist` (`Isaac/Linker/ItemPool.lua:15-135`).

```

Interface.ItemPool.GetCollectible

Component.ItemPool

Component.ItemPool.Pool

Component.ItemPool.PoolItem

Stub.pick_collectible

Stub.CanSpawnCollectible
```

| Function Name | File Path & Line Range | Role |
| --- | --- | --- |
| `Stub.GetCollectible` | `Isaac/Linker/ItemPool.lua:56-63` | Retrieves a collectible from a specified pool using seed and flags. |
| `Stub.pick_collectible` | `Isaac/Linker/ItemPool.lua:45-49` | Computes weighted random item picks within a given pool. |
| `Stub.CanSpawnCollectible` | `Isaac/Linker/ItemPool.lua:29-34` | Verifies whether a specific collectible can spawn under current run conditions. |
| `Stub.AddRoomBlacklist` | `Isaac/Linker/ItemPool.lua:13-15` | Adds a collectible ID to the current room's spawn blacklist. |

Sources:

- `Isaac/Linker/ItemPool.lua:1-195`
- `Isaac/Components/Game/ItemPoolComponent.lua:1-57`

* * *

## ItemConfig Availability and Metadata Management

`Component.ItemConfig` (`Isaac/Components/Config/ItemConfigComponent.lua:1-11`) stores static definitions for collectibles, trinkets, null items, cards, pill effects, and player forms loaded from XML configuration assets.

### Data Structures and Metadata

- `Component.ItemConfig`: Maps item lists and lookup tables (`m_collectibleList`, `m_trinketList`, `m_cardList`, `m_collectibleNameMap`) (`Isaac/Components/Config/ItemConfigComponent.lua:1-11`).
- `Component.ItemConfig.Item`: Stores gameplay and presentation properties including `m_itemType`, `m_id`, `m_name`, `m_description`, `m_cacheFlags`, devil/shop prices, item quality, tags, and associated costumes (`Isaac/Components/Config/ItemConfigComponent.lua:12-48`).
- `Component.ItemConfig.Card`: Records properties for cards and runes such as `m_id`, `m_name`, `m_hudAnim`, and `m_pocketItemType` (`Isaac/Components/Config/ItemConfigComponent.lua:49-63`).

### Availability Logic and XML Loading

Item availability and metadata loading are coordinated through `Isaac/Linker/ItemConfig.lua` and `Isaac/Core/ItemConfig/AvailableLogic.lua`. The engine parses configuration attributes using `Lib.XML` helpers (`Engine/Lib/XML.lua:1-74`) to populate filters and tag structures.

```

Interface.ItemConfig.Load

Lib.XML.Parse

Stub.LoadCostumes

Stub.LoadPocketItems

Stub.LoadCraftingRecipes

Component.ItemConfig
```

| Function Name | File Path & Line Range | Role |
| --- | --- | --- |
| `Stub.GetCollectible` | `Isaac/Linker/ItemConfig.lua:118-122` | Looks up item configuration data by collectible ID. |
| `Stub.IsValidCollectible` | `Isaac/Linker/ItemConfig.lua:144-147` | Validates if a collectible ID is registered in the configuration. |
| `Stub.IsTaggedCollectible` | `Isaac/Linker/ItemConfig.lua:149-153` | Checks if a collectible matches specific configuration tags. |
| `Lib.XML.Parse` | `Engine/Lib/XML.lua:19-21` | Parses XML files into node structures for item loading. |

Sources:

- `Isaac/Linker/ItemConfig.lua:1-216`
- `Isaac/Components/Config/ItemConfigComponent.lua:1-64`
- `Engine/Lib/XML.lua:1-74`

* * *

## Boss Pools and XML-Driven Pool Loading

Boss selection and spawn weights are maintained by `Component.BossPool` (`Isaac/Components/Game/BossPoolComponent.lua:1-19`) and managed via `Isaac/Linker/BossPool.lua` (`Isaac/Linker/BossPool.lua:1-59`).

### Boss Pool Layouts

- `Component.BossPool`: Contains `m_pools` (array of 37 boss pools), `m_removedBosses`, and `m_levelBlacklist` (`Isaac/Components/Game/BossPoolComponent.lua:1-5`).
- `Component.BossPool.Pool`: Holds pool metadata, `m_bosses` (array of `Component.BossPool.Pool.Boss`), `m_totalWeight`, and double-trouble room variant constraints (`Isaac/Components/Game/BossPoolComponent.lua:6-12`).
- `Component.BossPool.Pool.Boss`: Tracks boss identity (`m_id`), weights (`m_initialWeight`, `m_weight`), achievement ID, and room variant bindings (`Isaac/Components/Game/BossPoolComponent.lua:13-18`).

### Selection and Stage Integration

Boss IDs for specific stages are resolved using `Stub.GetBossId` and `Stub.PickBoss` (`Isaac/Linker/BossPool.lua:22-36`). Configuration data is loaded from XML definitions using the engine's XML parser.

| Function Name | File Path & Line Range | Role |
| --- | --- | --- |
| `Stub.PickBoss` | `Isaac/Linker/BossPool.lua:19-27` | Selects a boss from a pool based on weighted probabilities and RNG. |
| `Stub.GetBossId` | `Isaac/Linker/BossPool.lua:29-35` | Resolves a boss ID for given stage types and variants. |
| `Stub.WasBossRemoved` | `Isaac/Linker/BossPool.lua:11-14` | Checks if a boss has been excluded from pools. |
| `Stub.CommitLevelBlacklist` | `Isaac/Linker/BossPool.lua:19-20` | Applies level-specific boss blacklists. |

Sources:

- `Isaac/Linker/BossPool.lua:1-59`
- `Isaac/Components/Game/BossPoolComponent.lua:1-19`
- `Isaac/Components/Config/BossComponent.lua:1-10`

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#item-pools-item-config-and-boss-pools)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#purpose-and-scope)
- [ItemPool Component and Selection Mechanics](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#itempool-component-and-selection-mechanics)
- [Memory Layout and Pool Structures](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#memory-layout-and-pool-structures)
- [Selection and Blacklisting Logic](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#selection-and-blacklisting-logic)
- [ItemConfig Availability and Metadata Management](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#itemconfig-availability-and-metadata-management)
- [Data Structures and Metadata](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#data-structures-and-metadata)
- [Availability Logic and XML Loading](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#availability-logic-and-xml-loading)
- [Boss Pools and XML-Driven Pool Loading](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#boss-pools-and-xml-driven-pool-loading)
- [Boss Pool Layouts](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#boss-pool-layouts)
- [Selection and Stage Integration](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools#selection-and-stage-integration)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 5.4 Persistence Networking And Profiles

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Persistence, Networking and Profiles

Relevant source files

- [Engine/Global.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Global.lua)
- [Engine/Interface/ShapeRenderer.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/ShapeRenderer.lua)
- [Isaac/Components/Game/RoomTransitionComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/RoomTransitionComponent.lua)
- [Isaac/Components/NetManager/NetInputDeviceComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/NetManager/NetInputDeviceComponent.lua)
- [Isaac/Components/NetManager/NetManagerComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/NetManager/NetManagerComponent.lua)
- [Isaac/Constants.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Constants.lua)
- [Isaac/Content/Game.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/Game.lua)
- [Isaac/Content/GameEffects/BackwardsPath.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/GameEffects/BackwardsPath.lua)
- [Isaac/Content/GameEffects/Bloom.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/GameEffects/Bloom.lua)
- [Isaac/Linker/GenericPrompt.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/GenericPrompt.lua)
- [Isaac/Linker/HUD.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/HUD.lua)
- [Isaac/Linker/NetManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/NetManager.lua)
- [Isaac/Linker/PersistentGameData.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua)
- [Isaac/Linker/PlayerManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PlayerManager.lua)
- [Isaac/Linker/ProceduralItemManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ProceduralItemManager.lua)
- [Isaac/Linker/Seeds.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua)
- [Isaac/StateSetup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/StateSetup.lua)

## Purpose and Scope

This page details the implementation of persistent state management, multiplayer networking, seed handling, and procedural item generation within `Isaac.LuaDecomps`. These subsystems govern user profiles, Steam cloud integration, achievement tracking, networking states (`NetManager`), deterministic run seed generation (`Seeds`), and procedural item logic (`ProceduralItemManager`).

Sources: `[Isaac/Linker/PersistentGameData.lua:1-189]`, `[Isaac/Linker/NetManager.lua:1-31]`, `[Isaac/Linker/Seeds.lua:1-111]`

* * *

## 1\. PersistentGameData and User Profile State

The `PersistentGameData` subsystem tracks global user progression, including collection logs, bestiary entries, unlocked achievements, challenges, and completion marks.

### Key Components and Linker Stubs

The linker layer exposes low-level interface functions that delegate to core persistence handlers (`Isaac/Core/Manager/PersistentGameData/PersistentDataMisc`):

- **Save/Load Operations**: `Stub.Load`, `Stub.save`, `Stub.Save`, `Stub.Flush`, and `Stub.DeleteCurrentSave` manage disk and cloud persistence ( [Isaac/Linker/PersistentGameData.lua24-71](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua#L24-L71)).
- **Achievements & Unlocks**: `Stub.TryUnlock`, `Stub.Unlocked`, and `Stub.unlock_steam_achievement` handle conditional unlocks and Steam API synchronizations ( [Isaac/Linker/PersistentGameData.lua74-95](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua#L74-L95)).
- **Bestiary & Collection**: `Stub.AddToCollection`, `Stub.AddBestiaryHit`, and `Stub.AddBestiaryDeath` update progression counters ( [Isaac/Linker/PersistentGameData.lua125-170](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua#L125-L170)).

### Diagram: Persistence Data Flow (Natural Language to Code Space)

```
Triggers

Checks Flags

Updates State

Flushes / Syncs

Writes to Disk/Cloud

User Action / Event

Interface.PersistentGameData:Stub.TryUnlock

Core.Manager.PersistentGameData.PersistentDataMisc

Component.PersistentGameData

Interface.PersistentGameData:Stub.Flush

Stub.PushToSteamCloud / SaveToSteamCloud
```

Sources: [Isaac/Linker/PersistentGameData.lua14-88](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/PersistentGameData.lua#L14-L88)

* * *

## 2\. Networking and NetManager

The `NetManager` subsystem handles cooperative play synchronization, network input devices, and netplay state evaluation.

### Component and Linker Architecture

- **`Interface.NetManager`**: Exposes core networking hooks including `IsNetPlay`, `Init`, `Reset`, and `Update` ( [Isaac/Linker/NetManager.lua1-31](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/NetManager.lua#L1-L31)).
- **`Component.NetInputDevice`**: Defines input devices bound to network endpoints ( [Isaac/Components/NetManager/NetInputDeviceComponent.lua1](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/NetManager/NetInputDeviceComponent.lua#L1-L1)).

### Diagram: NetManager Update Loop

```
Calls Update

Checks Netplay Status

Active Network Session

Local Only

Engine Tick Loop

Interface.NetManager:Stub.Update

Interface.NetManager:Stub.IsNetPlay

Process NetInputDevice Packets

Bypass Network Sync
```

Sources: `[Isaac/Linker/NetManager.lua:8-25]`, [Isaac/Components/NetManager/NetInputDeviceComponent.lua1](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/NetManager/NetInputDeviceComponent.lua#L1-L1)

* * *

## 3\. Seed Management and String Conversion

Deterministic RNG and run seeds are handled by the `Seeds` subsystem, which manages stage seeds, player initialization seeds, seed effects, and alphanumeric string conversions.

### Key Functions

- **String Parsing & Conversion**: `SeedsStringConversion.IsStringValidSeed`, `Seed2String`, and `String2Seed` handle conversion between raw 32-bit integers and visual seed strings ( [Isaac/Linker/Seeds.lua105-107](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua#L105-L107)).
- **Seed Effects & Validation**: `Stub.IsSpecialSeed`, `Stub.CanAddSeedEffect`, and `Stub.IsSeedComboBanned` enforce game rules regarding special seed combinations and achievement disallowance ( [Isaac/Linker/Seeds.lua11-62](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua#L11-L62)).

Sources: [Isaac/Linker/Seeds.lua1-111](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Seeds.lua#L1-L111)

* * *

## 4\. Procedural Item Manager

The procedural item manager works alongside item pools and seed generation to dynamically allocate or compute procedural parameters for special items during run execution.

Sources: [Isaac/Linker/ProceduralItemManager.lua1](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ProceduralItemManager.lua#L1-L1)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#persistence-networking-and-profiles)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#purpose-and-scope)
- [1\. PersistentGameData and User Profile State](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#1-persistentgamedata-and-user-profile-state)
- [Key Components and Linker Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#key-components-and-linker-stubs)
- [Diagram: Persistence Data Flow (Natural Language to Code Space)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#diagram-persistence-data-flow-natural-language-to-code-space)
- [2\. Networking and NetManager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#2-networking-and-netmanager)
- [Component and Linker Architecture](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#component-and-linker-architecture)
- [Diagram: NetManager Update Loop](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#diagram-netmanager-update-loop)
- [3\. Seed Management and String Conversion](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#3-seed-management-and-string-conversion)
- [Key Functions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#key-functions)
- [4\. Procedural Item Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles#4-procedural-item-manager)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 6 Rendering And Ui

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Rendering and UI

Relevant source files

- [Engine/Interface/GraphicsManager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/GraphicsManager.lua)
- [Isaac/Components/Game/GameComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua)
- [Isaac/Core/Game/Render.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua)
- [Isaac/Linker/BossOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/BossOverlay.lua)
- [Isaac/Linker/Manager.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Manager.lua)
- [Isaac/Render.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Render.lua)
- [Isaac/Utils/Common.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Common.lua)

## Purpose and Scope

The rendering and user interface (UI) subsystem bridges the lower-level graphics engine facilities (`Engine.GraphicsManager`) with application-level game states, post-processing filters, world-to-screen coordinate mappings, and on-screen HUD elements. Top-level frame rendering is orchestrated via `Isaac/Render.lua` and specialized game-loop render scripts like `Isaac/Core/Game/Render.lua`, managing render targets, shader passes, and multi-layered UI views.

For deep technical dives into individual rendering layers, consult the corresponding child pages:

- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)

* * *

## 6.1 Render Pipeline and Post-Processing

The top-level render pipeline controls the sequence in which different game states are drawn. The entry point `Isaac/Render.lua` evaluates the global `eState` enum (`STATE_MENU`, `STATE_GAME`, `STATE_CUTSCENE`, `STATE_NIGHTMARE`) to delegate rendering to specific UI or game managers [Isaac/Render.lua30-45](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Render.lua#L30-L45)

When the engine is running an active session (`STATE_GAME`), execution transfers to `Isaac/Core/Game/Render.lua`, which handles world rendering, post-processing filters (such as `OldTV`, `Hallucination`, `Pixelation`, `Bloom`, and `ColorMod`), and window resize events [Isaac/Core/Game/Render.lua40-192](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L40-L192) Coordinate space transformations and utility screen calculations are managed in `Isaac/Utils/Common.lua` via functions like `GetRenderPosition` and `WindowToScreen` [Isaac/Utils/Common.lua139-175](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Common.lua#L139-L175)

### Diagram: Top-Level Render Pipeline Dispatch

```

eState.STATE_GAME

eState.STATE_MENU

eState.STATE_CUTSCene

eState.STATE_NIGHTMARE

TopLevelRenderPipelineDispatcher

Engine.GraphicsManager

Isaac/Render.lua::Render

manager.m_state

Isaac/Core/Game/Render.lua::Render

Isaac.Interface.MenuManager::Render

Isaac.Interface.Cutscene::Render

Isaac.Interface.NightmareScene::Render
```

_Sources: [Isaac/Render.lua1-202](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Render.lua#L1-L202) [Isaac/Core/Game/Render.lua1-218](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L1-L218) [Isaac/Utils/Common.lua123-222](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Common.lua#L123-L222)_

For details, see [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing).

* * *

## 6.2 Sprites, ANM2 and Graphics Primitives

Graphics primitives, color management, and animation rendering are handled through engine-backed classes and Lua wrappers. The codebase interfaces directly with `Engine.GraphicsManager` for frame clearing, render target texture switching, blending modes, and shader bindings [Engine/Interface/GraphicsManager.lua33-65](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/GraphicsManager.lua#L33-L65)

Color modifications and blending state are tracked through structures such as `Component.ColorModState` [Isaac/Components/Game/GameComponent.lua97-103](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L97-L103) while visual elements rely on ANM2 animation formats and image wrappers to project actors onto world or screen coordinates.

For details, see [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives).

* * *

## 6.3 HUD, Overlays and Console

User interfaces, overlays, debugging tools, and heads-up displays are instantiated and tracked inside the core game component layout (`Component.Game`) [Isaac/Components/Game/GameComponent.lua1-96](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L1-L96)

The UI stack includes the player HUD (`m_hud`), boss introduction overlays (`m_bossOverlay`), item pickup popups (`m_itemOverlay`), the debug console (`m_console`), end-of-run leaderboards (`m_leaderboard`), game over screens (`m_gameOver`), and generic prompt dialogs (`m_victoryRun_prompt`) [Isaac/Components/Game/GameComponent.lua1-65](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L1-L65) These UI components are rendered sequentially during the post-world rendering phase in `Isaac/Core/Game/Render.lua` [Isaac/Core/Game/Render.lua126-142](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L126-L142)

### Diagram: Game UI and HUD Component Structure

```

GameUIAndHUDComponentStructure

Component.Game

Component.HUD::m_hud

Component.BossOverlay::m_bossOverlay

Component.ItemOverlay::m_itemOverlay

Component.Console::m_console

Component.GameOver::m_gameOver

Component.Leaderboard::m_leaderboard
```

_Sources: [Isaac/Components/Game/GameComponent.lua1-96](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/GameComponent.lua#L1-L96) [Isaac/Core/Game/Render.lua126-142](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Game/Render.lua#L126-L142)_

For details, see [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console).

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui#rendering-and-ui)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui#purpose-and-scope)
- [6.1 Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui#61-render-pipeline-and-post-processing)
- [Diagram: Top-Level Render Pipeline Dispatch](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui#diagram-top-level-render-pipeline-dispatch)
- [6.2 Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui#62-sprites-anm2-and-graphics-primitives)
- [6.3 HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui#63-hud-overlays-and-console)
- [Diagram: Game UI and HUD Component Structure](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui#diagram-game-ui-and-hud-component-structure)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 7.3 Shared Utilities: Math Tables Xml Emmylua Stubs

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Shared Utilities: Math, Tables, XML, EmmyLua Stubs

Relevant source files

- [Engine/Lib/XML.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Lib/XML.lua)
- [General/Math.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua)
- [General/Math/VectorUtils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math/VectorUtils.lua)
- [General/Table.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Table.lua)
- [General/Xml/Parser.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Xml/Parser.lua)
- [General/Xml/Utils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Xml/Utils.lua)
- [Isaac/Components/Config/BossComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/BossComponent.lua)
- [Isaac/Components/Game/BossPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/BossPoolComponent.lua)
- [Isaac/Linker/BossPool.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/BossPool.lua)
- [Isaac/Utils/Capsule.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Capsule.lua)
- [\_EmmyLua/Containers.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/_EmmyLua/Containers.lua)
- [\_EmmyLua/XML.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/_EmmyLua/XML.lua)

## Purpose and Scope

This page details the shared utility libraries and framework stubs used throughout the `Isaac.LuaDecomps` codebase. These modules provide foundational mathematical operations, vector calculations, table manipulation helpers, XML document parsing, game-specific domain primitives (such as collision capsules and boss pool logic), and EmmyLua type annotations for IDE completion.

Sources: `General/Math.lua:1-175`, `General/Math/VectorUtils.lua:1-79`, `General/Table.lua:1-38`, `Engine/Lib/XML.lua:1-74`, `Isaac/Utils/Capsule.lua:1-83`, `Isaac/Linker/BossPool.lua:1-59`

* * *

## 1\. General Mathematics and Vector Utilities

The math library provides scalar and vector utilities required for game logic, physics, pathfinding, and interpolation. Scalar operations reside in `General/Math.lua`, while vector-specific calculations are implemented in `General/Math/VectorUtils.lua`.

### Scalar Math Helpers

`General/Math.lua` exposes core continuous math functions:

- **`Clamp(value, min, max)`**: Restricts a numeric value within boundaries [General/Math.lua8-10](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L8-L10).
- **`Lerp(a, b, blendFactor)`**: Linear interpolation between two numbers [General/Math.lua16-18](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L16-L18).
- **`InverseLerp(a, b, value)`**: Computes the blend factor of a value between two bounds [General/Math.lua24-27](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L24-L27).
- **`MoveTowards(current, target, rate)`**: Steps a value toward a target without overshooting [General/Math.lua33-39](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L33-L39).
- **`NormalizeAngle(angle)` / `InterpolateAngle` / `ApproachAngle`**: Handles directional angle normalization to `[-180, 180]` and angular rotation tracking [General/Math.lua84-149](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L84-L149).

### Vector Utilities

`General/Math/VectorUtils.lua` extends standard `Vector` objects with auxiliary operations:

- **`Equals(vector, other)`**: Checks coordinate-wise equality [General/Math.lua10-12](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L10-L12).
- **`GetAxisAlignedUnitVector(vector)`**: Determines the dominant orthogonal axis [General/Math.lua31-39](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L31-L39).
- **`Vec3Length(x, y, z)`**: Computes 3D Euclidean length [General/Math.lua53-55](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L53-L55).
- **`Lerp(a, b, blendFactor)`**: Vector linear interpolation [General/Math.lua61-63](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Math.lua#L61-L63).

```
CodeEntitySpace

NaturalLanguageSpace

ScalarInterpolationAndAngles

VectorAlignmentAndGeometry

General/Math.lua

General/Math/VectorUtils.lua

Clamp(value,min,max)

NormalizeAngle(angle)

GetAxisAlignedUnitVector(vector)

Vec3Length(x,y,z)
```

Sources: `General/Math.lua:1-175`, `General/Math/VectorUtils.lua:1-79`

* * *

## 2\. Data Structure Helpers: Tables and Containers

Utility functions for manipulating standard Lua tables and establishing container type aliases for type checking are located in `General/Table.lua` and `_EmmyLua/Containers.lua`.

### Table Utilities

- **`CreateDictionary(tbl)`**: Converts an array-like table into a set-like dictionary where keys map to `true` [General/Table.lua6-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Table.lua#L6-L13).
- **`Vector_Resize(tbl, newSize, constructor, ...)`**: Resizes an array, instantiating new elements using a provided constructor function when growing [General/Table.lua18-30](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Table.lua#L18-L30).

### EmmyLua Container Definitions

`_EmmyLua/Containers.lua` defines generic type stubs for static analysis:

- `Pair<K, V>`: Represents a tuple-like key-value structure [\_\_EmmyLua/Containers.lua1](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/__EmmyLua/Containers.lua#L1-L1).
- `Set<T>`: Represents a set structure mapping items to booleans [\_\_EmmyLua/Containers.lua2](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/__EmmyLua/Containers.lua#L2-L2).

Sources: `General/Table.lua:1-38`, `_EmmyLua/Containers.lua:1-2`

* * *

## 3\. XML Parsing and Utilities

XML configuration data is parsed and queried using internal engine bindings and helper libraries.

### XML Interface and Parsers

`Engine/Lib/XML.lua`, `General/Xml/Parser.lua`, and `General/Xml/Utils.lua` handle structured file ingestion.

- **`Lib.XML.Parse(file)`**: Reads an engine file handle into an `Lib.XML.Document` structure [Engine/Lib/XML.lua19-21](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Lib/XML.lua#L19-L21).
- **Node Traversal**: Functions like `FirstNode`, `FirstNode_Name`, `NextSibling`, and `NextSibling_Name` navigate hierarchical XML node trees [Engine/Lib/XML.lua23-45](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Lib/XML.lua#L23-L45).
- **Cast Utilities**: `General/Xml/Utils.lua` provides robust string-to-primitive parsers:

  - `ToInteger(value)` via pattern matching [General/Xml/Utils.lua12-16](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Xml/Utils.lua#L12-L16).
  - `ToFloat(value)` via `tonumber` casting [General/Xml/Utils.lua19-21](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Xml/Utils.lua#L19-L21).
  - `ToBoolean(value)` handling strings ("true", "True") and numeric flags [General/Xml/Utils.lua37-39](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Xml/Utils.lua#L37-L39).

```
CodeEntitySpace

NaturalLanguageSpace

XMLDocumentParsingAndTraversal

PrimitiveTypeCasting

Engine/Lib/XML.lua

General/Xml/Parser.lua

General/Xml/Utils.lua

Parse(file)

ToInteger(value)

ToBoolean(value)
```

Sources: `Engine/Lib/XML.lua:1-74`, `General/Xml/Parser.lua:1-14`, `General/Xml/Utils.lua:1-48`, `_EmmyLua/XML.lua:1-8`

* * *

## 4\. Isaac-Specific Domain Utilities

Domain-specific utilities include spatial collision primitives (`Component.Capsule`) and boss pool configuration dispatchers (`Interface.BossPool`).

### Spatial Capsules (`Isaac/Utils/Capsule.lua`)

Capsules represent line-swept sphere volumes used for collision detection:

- **`NewFromDimensions(center, size, sizeMulti, rotation)`**: Calculates segment length, radius, start point, and end point based on dimensions and rotation angles [Isaac/Utils/Capsule.lua15-51](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Capsule.lua#L15-L51).
- **`NewFromEndPoints(startPoint, endPoint, radius)`**: Derives capsule center and direction vectors directly from terminal points [Isaac/Utils/Capsule.lua53-72](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Capsule.lua#L53-L72).

```
---@class Component.Capsule
---@field center Vector : 0x0
---@field startPoint Vector : 0x8
---@field endPoint Vector : 0x10
---@field direction Vector : 0x18
---@field radius number : 0x20
---@field halfSegmentLength number : 0x24
```

_Source: [Isaac/Utils/Capsule.lua7-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/Capsule.lua#L7-L13)_

### Boss Pool Management (`Isaac/Linker/BossPool.lua`)

Boss selection logic coordinates with raw component structs (`Component.BossPool`) to query available bosses, commit level blacklists, and pick random encounters:

- **`Stub.PickBoss`**: Selects boss entries based on weights and RNG states [Isaac/Linker/BossPool.lua22-27](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/BossPool.lua#L22-L27).
- **`Stub.GetBossId`**: Resolves valid boss IDs for stage variants and level types [Isaac/Linker/BossPool.lua29-35](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/BossPool.lua#L29-L35).

Sources: `Isaac/Utils/Capsule.lua:1-83`, `Isaac/Linker/BossPool.lua:1-59`, `Isaac/Components/Game/BossPoolComponent.lua:1-19`

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#shared-utilities-math-tables-xml-emmylua-stubs)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#purpose-and-scope)
- [1\. General Mathematics and Vector Utilities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#1-general-mathematics-and-vector-utilities)
- [Scalar Math Helpers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#scalar-math-helpers)
- [Vector Utilities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#vector-utilities)
- [2\. Data Structure Helpers: Tables and Containers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#2-data-structure-helpers-tables-and-containers)
- [Table Utilities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#table-utilities)
- [EmmyLua Container Definitions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#emmylua-container-definitions)
- [3\. XML Parsing and Utilities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#3-xml-parsing-and-utilities)
- [XML Interface and Parsers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#xml-interface-and-parsers)
- [4\. Isaac-Specific Domain Utilities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#4-isaac-specific-domain-utilities)
- [Spatial Capsules (\`Isaac/Utils/Capsule.lua\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#spatial-capsules-isaacutilscapsulelua)
- [Boss Pool Management (\`Isaac/Linker/BossPool.lua\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs#boss-pool-management-isaaclinkerbosspoollua)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 7.4 Enums And Configuration Data

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Enums and Configuration Data

Relevant source files

- [Engine/Components/Image.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Components/Image.lua)
- [Engine/Interface/Shader.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/Shader.lua)
- [Isaac/Components/Config/EntityConfigComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/EntityConfigComponent.lua)
- [Isaac/Components/Config/PillEffectComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/PillEffectComponent.lua)
- [Isaac/Components/Manager/OptionsComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua)
- [Isaac/Components/Player/TearParams.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Player/TearParams.lua)
- [Isaac/Content/GameEffects/ItemExtraParams.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Content/GameEffects/ItemExtraParams.lua)
- [Isaac/Core/Manager/Static.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Manager/Static.lua)
- [Isaac/Enums.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Enums.lua)
- [Isaac/Interface/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/AchievementOverlay.lua)
- [Isaac/Interface/EntityConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/EntityConfig.lua)
- [Isaac/Interface/SoundEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/SoundEffects.lua)
- [Isaac/Linker/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/AchievementOverlay.lua)
- [Isaac/Linker/Cutscene.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua)
- [Isaac/Linker/EntityConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/EntityConfig.lua)
- [Isaac/\_OLD/AchievementOverlay/Component.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua)

This page details the implementation of game-wide enumerations, configuration components, and data loading subsystems in `Isaac.LuaDecomps`. It covers `Isaac/Enums.lua`, engine constants, configuration memory layouts (`Component.EntityConfig`, `Component.ItemConfig.PillEffect`), and the linker interfaces responsible for parsing and caching XML-driven configuration files.

* * *

## 1\. Engine Enums and Constants (`Isaac/Enums.lua`)

The `Isaac/Enums.lua` module acts as the central registry for Lua-side enumerations mirroring engine internals. It depends on `Engine.Enums` \[Isaac/Enums.lua:1-1\] and defines structured numeric and bitwise states used throughout game logic, rendering, and content systems.

Key enumerations defined in `Isaac/Enums.lua`:

- `eState`: Tracks top-level execution states like `STATE_NULL`, `STATE_MENU`, `STATE_GAME`, `STATE_CUTSCENE`, and `STATE_NIGHTMARE` \[Isaac/Enums.lua:6-13\].
- `eMode`: Differentiates between `NORMAL` and `GREED` modes \[Isaac/Enums.lua:15-19\].
- `eStageId`: Identifies physical and special floor stages (e.g., `BASEMENT`, `CAVES`, `WOMB`, `CATHEDRAL`, `THE_VOID`, `DOWNPOUR`, `HOME`) \[Isaac/Enums.lua:21-61\].
- `eWeaponModifiers`: Bitmask flags representing weapon-altering collectibles such as `CHOCOLATE_MILK`, `BRIMSTONE`, `MONSTROS_LUNG`, `LUDOVICO_TECHNIQUE`, and `C_SECTION` \[Isaac/Enums.lua:116-129\].
- `eShopItemType`: Classifies items available in shops (`HEART_FULL`, `BOMB_SINGLE`, `COLLECTIBLE`, `TRINKET`, etc.) \[Isaac/Enums.lua:194-217\].

```

Isaac/Enums.lua

Module.eState

Module.eStageId

Module.eWeaponModifiers

Module.eShopItemType

Engine.Enums
```

_Figure 1: Enum Module Dependencies and Namespace Layout_

Sources: [Isaac/Enums.lua1-271](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Enums.lua#L1-L271)

* * *

## 2\. Configuration Components (`Isaac/Components/Config/*`)

Configuration data structures define the memory layout of static game definitions loaded from XML files (e.g., items, entities, bosses, pills). These components contain hexadecimal memory offset annotations and field definitions.

### Entity Configuration Component

`Component.EntityConfig` stores maps and arrays of entity definitions, player types, babies, boss parameters, and helper structures like `Component.EntityConfig.PokeyMansEntry` \[Isaac/Components/Config/EntityConfigComponent.lua:1-14\].

| Field Name | Type | Memory Offset | Description |
| --- | --- | --- | --- |
| `m_map` | `table<integer, Component.EntityConfig.Entity>` | `0x0` | Key-value mapping of entity IDs to definitions |
| `m_players` | `Component.EntityConfig.Player[]` | `0x8` | Registered player configurations |
| `m_babies` | `Component.EntityConfig.Baby[]` | `0x14` | Co-op baby definitions |
| `m_bosses` | `Component.EntityConfig.Boss[]` | `0x20` | Boss-specific configuration profiles |
| `m_edenHair` | `string[]` | `0x2c` | Eden hair variant lookup array |
| `m_pokeyMansPool` | `Component.EntityConfig.PokeyMansEntry` | `0x38` | Pokey Mans item pool definition |

Sources: [Isaac/Components/Config/EntityConfigComponent.lua1-14](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/EntityConfigComponent.lua#L1-L14)

### Pill Effect Component

`Component.ItemConfig.PillEffect` defines pill properties, descriptions, announcer voice lines, and associated achievements \[Isaac/Components/Config/PillEffectComponent.lua:1-14\].

| Field Name | Type | Memory Offset | Description |
| --- | --- | --- | --- |
| `m_id` | `PillEffect | integer` | `0x0` | Unique pill effect identifier |
| `m_achievementId` | `Achievement | integer` | `0x4` | Associated achievement lock |
| `m_name` | `string` | `0x8` | Localization key or display name |
| `m_description` | `string` | `0x20` | Pill description string |
| `m_greedModeAllowed` | `boolean` | `0x38` | Availability flag in Greed Mode |
| `m_announcerVoice` | `SoundEffect | integer` | `0x3c` | Standard announcer sound effect |
| `m_announcerVoiceSuper` | `SoundEffect | integer` | `0x40` | Super/Mega announcer sound effect |
| `m_modEntry` | `Component.ModEntry` | `0x50` | Mod source attribution reference |

Sources: [Isaac/Components/Config/PillEffectComponent.lua1-13](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/PillEffectComponent.lua#L1-L13)

* * *

## 3\. Configuration Linkers and Loaders (`Isaac/Linker/EntityConfig.lua`)

The `Isaac/Linker/EntityConfig.lua` file implements `Interface.EntityConfig` stub bindings that interface with the underlying engine configuration parsers \[Isaac/Linker/EntityConfig.lua:1-106\]. These functions load XML definitions, resolve entity variants, and manage preloading.

Key functions exposed on `Interface.EntityConfig`:

- `Stub.GetEntity(entityConfig, id, variant, subtype)`: Retrieves a specific entity configuration node \[Isaac/Linker/EntityConfig.lua:21-26\].
- `Stub.Load(ctx, entityConfig, xmlpath, modentry)`: Parses XML configuration files into memory structures \[Isaac/Linker/EntityConfig.lua:34-44\].
- `Stub.GetBoss(entityConfig, bossID)`: Fetches boss configuration metadata \[Isaac/Linker/EntityConfig.lua:79-82\].
- `Stub.Preload(ctx, entityConfig, config)`: Preloads graphics and sound assets associated with an entity configuration entry \[Isaac/Linker/EntityConfig.lua:57-60\].

```
Stub.Load

Populates

m_map

m_bosses

Entities.xml

Isaac/Linker/EntityConfig.lua

Component.EntityConfig

Stub.GetEntity

Stub.GetBoss
```

_Figure 2: Configuration Data Loading Pipeline from XML to Component Storage_

Sources: [Isaac/Linker/EntityConfig.lua1-106](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/EntityConfig.lua#L1-L106)

* * *

## 4\. Content and XML Data Pipeline

Configuration data flows from raw XML assets parsed via core engine loaders into strongly-typed component structures. Mods can inject or modify entries via `Component.ModEntry` hooks processed during `Stub.PostLoadMods` \[Isaac/Linker/EntityConfig.lua:84-86\].

```
Interface.EntityConfig.Load

Mutates

Provides Data

Content/Config/*.xml

Isaac/Linker/EntityConfig.lua

Component.EntityConfig

Game Loop / Entities
```

_Figure 3: Natural Language Space to Code Entity Space mapping for Configuration and XML parsing_

Sources: [Isaac/Linker/EntityConfig.lua34-44](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/EntityConfig.lua#L34-L44) [Isaac/Components/Config/EntityConfigComponent.lua1-14](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/EntityConfigComponent.lua#L1-L14)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data#enums-and-configuration-data)
- [1\. Engine Enums and Constants (\`Isaac/Enums.lua\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data#1-engine-enums-and-constants-isaacenumslua)
- [2\. Configuration Components (\`Isaac/Components/Config/\*\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data#2-configuration-components-isaaccomponentsconfig)
- [Entity Configuration Component](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data#entity-configuration-component)
- [Pill Effect Component](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data#pill-effect-component)
- [3\. Configuration Linkers and Loaders (\`Isaac/Linker/EntityConfig.lua\`)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data#3-configuration-linkers-and-loaders-isaaclinkerentityconfiglua)
- [4\. Content and XML Data Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data#4-content-and-xml-data-pipeline)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

## 8 Glossary

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[Guantol-Lemat/Isaac.LuaDecomps](https://github.com/Guantol-Lemat/Isaac.LuaDecomps "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 1 October 2026 ( [8a9c61](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/commits/8a9c6186))

- [Overview](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1-overview)
- [Architectural Layers: Interface, Linker, Component, Core, Content](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.1-architectural-layers:-interface-linker-component-core-content)
- [Conventions: Context, Globals and Memory Offsets](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.2-conventions:-context-globals-and-memory-offsets)
- [Legacy and Deprecated Trees (\_Legacy, Isaac/\_OLD)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/1.3-legacy-and-deprecated-trees-(_legacy-isaac_old))
- [Entity System](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2-entity-system)
- [Base Entity, EntityPtr and Entity Lists](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.1-base-entity-entityptr-and-entity-lists)
- [Player Entity](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2-player-entity)
- [Player Effects and Item Interactions](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.2.1-player-effects-and-item-interactions)
- [Pickups](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.3-pickups)
- [NPCs and Pathfinding](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.4-npcs-and-pathfinding)
- [Slots, Beggars and Machines](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.5-slots-beggars-and-machines)
- [Familiars and Custom Actor Hooks](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/2.6-familiars-and-custom-actor-hooks)
- [Weapons and Projectiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3-weapons-and-projectiles)
- [Weapon Abstraction and Multi-Shot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.1-weapon-abstraction-and-multi-shot)
- [Tears: Components and Update Pipeline](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2-tears:-components-and-update-pipeline)
- [Tear Effect Modules (Ludovico, Fetus, Absorb, Stick)](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.2.1-tear-effect-modules-(ludovico-fetus-absorb-stick))
- [Knives and Lasers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/3.3-knives-and-lasers)
- [World: Rooms, Levels and Grid](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4-world:-rooms-levels-and-grid)
- [Room Component and Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.1-room-component-and-interface)
- [Grid Entities](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.2-grid-entities)
- [Level Generation](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/4.3-level-generation)
- [Game State and Managers](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5-game-state-and-managers)
- [Manager Component and Startup](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.1-manager-component-and-startup)
- [Game Component and Run Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.2-game-component-and-run-lifecycle)
- [Item Pools, Item Config and Boss Pools](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.3-item-pools-item-config-and-boss-pools)
- [Persistence, Networking and Profiles](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/5.4-persistence-networking-and-profiles)
- [Rendering and UI](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6-rendering-and-ui)
- [Render Pipeline and Post-Processing](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.1-render-pipeline-and-post-processing)
- [Sprites, ANM2 and Graphics Primitives](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.2-sprites-anm2-and-graphics-primitives)
- [HUD, Overlays and Console](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/6.3-hud-overlays-and-console)
- [Engine, Modding and Shared Libraries](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7-engine-modding-and-shared-libraries)
- [Engine Layer and File Manager](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.1-engine-layer-and-file-manager)
- [Mod Manager and Lua Callback Engine](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.2-mod-manager-and-lua-callback-engine)
- [Shared Utilities: Math, Tables, XML, EmmyLua Stubs](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.3-shared-utilities:-math-tables-xml-emmylua-stubs)
- [Enums and Configuration Data](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/7.4-enums-and-configuration-data)
- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary)

Menu

# Glossary

Relevant source files

- [Engine/Components/Image.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Components/Image.lua)
- [Engine/Interface/Shader.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Engine/Interface/Shader.lua)
- [General/Context.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Context.lua)
- [Isaac/Components/Config/ItemConfigComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Config/ItemConfigComponent.lua)
- [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)
- [Isaac/Components/Game/EntityListComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/EntityListComponent.lua)
- [Isaac/Components/Game/ItemPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ItemPoolComponent.lua)
- [Isaac/Components/Manager/OptionsComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Manager/OptionsComponent.lua)
- [Isaac/Components/Room/RoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua)
- [Isaac/Components/Room/RoomDescriptorComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomDescriptorComponent.lua)
- [Isaac/Core/Manager/Static.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Manager/Static.lua)
- [Isaac/Core/Room/PositionUtils.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Room/PositionUtils.lua)
- [Isaac/Core/Slot/SlotCollision.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotCollision.lua)
- [Isaac/Core/Slot/SlotDamage.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotDamage.lua)
- [Isaac/Core/Slot/SlotInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua)
- [Isaac/Core/Slot/SlotMisc.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotMisc.lua)
- [Isaac/Core/Slot/SlotRender.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotRender.lua)
- [Isaac/Core/Slot/SlotUpdate.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotUpdate.lua)
- [Isaac/Enums.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Enums.lua)
- [Isaac/Interface/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/AchievementOverlay.lua)
- [Isaac/Interface/ItemConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Interface/ItemConfig.lua)
- [Isaac/Linker/AchievementOverlay.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/AchievementOverlay.lua)
- [Isaac/Linker/Cutscene.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Cutscene.lua)
- [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)
- [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)
- [Isaac/Linker/ItemConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ItemConfig.lua)
- [Isaac/Linker/ItemPool.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ItemPool.lua)
- [Isaac/Linker/Room.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua)
- [Isaac/Linker/SoundEffects.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/SoundEffects.lua)
- [Isaac/Utils/LootList.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Utils/LootList.lua)
- [Isaac/\_OLD/AchievementOverlay/Component.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/_OLD/AchievementOverlay/Component.lua)
- [LuaEngine/Callbacks.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LuaEngine/Callbacks.lua)

## Purpose and Scope

This page defines the core architectural jargon, data structures, and naming conventions used throughout `Isaac.LuaDecomps`. It serves as a technical reference for navigating the re-expressed codebase of _The Binding of Isaac: Repentance_, mapping conceptual game engine terms to their concrete Lua implementations, file paths, and memory layouts.

* * *

## Architectural & Codebase Jargon

### Linker

A **Linker** module (`Isaac/Linker/*`) acts as the bridge between public API stubs, type definitions, and underlying functional logic. Linkers populate interface tables with actual functions implemented in the `Core/` or `Content/` layers, while declaring function stubs for type safety under EmmyLua.

- **Files:**`Isaac/Linker/Entity.lua:1-237` [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)`Isaac/Linker/Entity_Pickup.lua:1-209` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)
- **Sources:**`Isaac/Linker/Entity.lua:1-237` [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)`Isaac/Linker/Entity_Pickup.lua:1-209` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)

### Interface

An **Interface** (`Isaac/Interface/*`) defines the formal Lua namespace structures and API signatures exposed to mods or internal engine systems, mirroring the original C++ engine API exposed by Repentance.

- **Sources:**`Isaac/Linker/Entity.lua:1-2` [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)`Isaac/Linker/Entity_Pickup.lua:1-2` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)

### Component

A **Component** (`Isaac/Components/*`) represents a raw memory-offset struct mirroring engine heap allocations. Components define fields annotated with hexadecimal offsets (e.g., `: 0x474`) corresponding to C++ class member offsets.

- **Files:**`Isaac/Components/Game/ItemPoolComponent.lua:1-32` [Isaac/Components/Game/ItemPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ItemPoolComponent.lua)`Isaac/Components/Entity/PickupComponent.lua:1-32` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)
- **Sources:**`Isaac/Components/Game/ItemPoolComponent.lua:1-32` [Isaac/Components/Game/ItemPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ItemPoolComponent.lua)`Isaac/Components/Entity/PickupComponent.lua:1-32` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)

### Stub

A **Stub** is a placeholder function definition inside a linker or interface file that lacks a full implementation body or serves as a type-checking signature for un-decompiled or native-bound engine routines.

- **Sources:**`Isaac/Linker/Entity.lua:13-237` [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)`Isaac/Linker/Entity_Pickup.lua:12-209` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)

### Context.Common & ctx

`Context.Common` is a global state context container passed as the first parameter (`ctx`) to almost every engine and gameplay function. It encapsulates pointers to the global manager and active game run state.

- **File:**`General/Context.lua:1-4` [General/Context.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Context.lua)
- **Sources:**`General/Context.lua:1-4` [General/Context.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Context.lua)`Isaac/Linker/Entity_Pickup.lua:64-70` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)

### m\_ fields

Fields prefixed with `m_` in component definitions represent member variables mapped directly from the original C++ object memory layouts, complete with precise byte offset annotations.

- **Sources:**`Isaac/Components/Game/ItemPoolComponent.lua:2-15` [Isaac/Components/Game/ItemPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ItemPoolComponent.lua)`Isaac/Components/Entity/PickupComponent.lua:2-31` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)

### \_qqq

The `_qqq` suffix (or `_qqq` in field names) denotes a field, function, or parameter that has not been fully reverse-engineered, verified, or understood during the decompilation process.

- **Sources:**`Isaac/Components/Entity/PickupComponent.lua:18-27` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)`Isaac/Components/Room/RoomComponent.lua:26-32` [Isaac/Components/Room/RoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua)

* * *

## Data Structures & Engine Systems

### ANM2

**ANM2** is the proprietary animation file format used by the engine for rendering sprites, entities, and UI elements. Managed via the sprite system (`General/Sprite`).

- **Sources:**`Isaac/Components/Entity/PickupComponent.lua:2` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)`Isaac/Core/Slot/SlotInit.lua:20-25` [Isaac/Core/Slot/SlotInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua)

### EntityPtr

`EntityPtr` is a safe entity reference wrapper used to track entities across frames without retaining dangling direct memory pointers if the target entity dies or is removed.

- **Sources:**`Isaac/Components/Entity/PickupComponent.lua:21-23` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)

### TearFlags & BitSet128

**TearFlags** are bitmask enumerations modifying tear behavior (e.g., poison, piercing). **BitSet128** represents 128-bit bitsets used for tracking large collections of flags or states across the engine.

- **Sources:**`LuaEngine/Callbacks.lua:68-70` [LuaEngine/Callbacks.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LuaEngine/Callbacks.lua)

### LootList

`LootList` is a utility system used to manage drop weights and pool resolution when entities or chests spawn rewards.

- **Sources:**`Isaac/Linker/Entity_Pickup.lua:7` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)

### HitList

`HitList` tracks entities that have been struck by a projectile, laser, or knife during the current collision tick to prevent multi-hit frames against the same target.

- **Sources:**`Isaac/Linker/Entity.lua:10-12` [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)

### ItemPool / PoolItem

`ItemPool` manages collectible and trinket availability, spawn weights, and room blacklists. A `PoolItem` represents an individual item entry within a pool (`m_itemList`), holding dynamic weights and removal thresholds.

- **Files:**`Isaac/Components/Game/ItemPoolComponent.lua:1-32` [Isaac/Components/Game/ItemPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ItemPoolComponent.lua)
- **Sources:**`Isaac/Components/Game/ItemPoolComponent.lua:1-32` [Isaac/Components/Game/ItemPoolComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Game/ItemPoolComponent.lua)`Isaac/Linker/ItemPool.lua:13-50` [Isaac/Linker/ItemPool.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ItemPool.lua)

### RoomDescriptor & GridEntity & LRoomAreaDesc

- **RoomDescriptor:** Metadata struct describing a room's position, type, seed, and state within the level grid (`Isaac/Components/Room/RoomDescriptorComponent.lua`).
- **GridEntity:** Base representation for static room objects like rocks, spikes, and doors (`Isaac/Components/Room/RoomComponent.lua:10-12`).
- **LRoomAreaDesc:** Area bounds descriptor defining high and low spatial dimensions for complex room layouts (`Isaac/Components/Room/RoomComponent.lua:118-122`).
- **Sources:**`Isaac/Components/Room/RoomComponent.lua:4-15` [Isaac/Components/Room/RoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua)`Isaac/Components/Room/RoomComponent.lua:118-122` [Isaac/Components/Room/RoomComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Room/RoomComponent.lua)

### eState

`eState` represents state machine identifiers or engine execution states driving rendering, menu flow, or entity behavior loops.

- **Sources:**`Isaac/Linker/Entity_Pickup.lua:19` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)

### ModEntry

`ModEntry` tracks loaded Lua mod metadata, search paths, and sandbox state within the mod manager system.

- **Sources:**`Isaac/Linker/ItemConfig.lua:59-69` [Isaac/Linker/ItemConfig.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/ItemConfig.lua)

### ActorSlot

`ActorSlot` encapsulates logic for interactive slot machines, beggars, and donation boxes (`Isaac/Content/ActorSlot`), managing states such as idle, payout, and destruction.

- **Files:**`Isaac/Core/Slot/SlotInit.lua:5-38` [Isaac/Core/Slot/SlotInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua)`Isaac/Core/Slot/SlotDamage.lua:4-41` [Isaac/Core/Slot/SlotDamage.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotDamage.lua)
- **Sources:**`Isaac/Core/Slot/SlotInit.lua:5-38` [Isaac/Core/Slot/SlotInit.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotInit.lua)`Isaac/Core/Slot/SlotDamage.lua:4-41` [Isaac/Core/Slot/SlotDamage.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotDamage.lua)

### MultiShotParams

Parameters regulating multi-shot calculations, angle offsets, and projectile clustering for players and enemies.

- **Sources:**`Isaac/Linker/Entity.lua:1-237` [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)

### ScoreSheet

Structure responsible for compiling end-run statistics, item collections, and final score calculations.

- **Sources:**`Isaac/Linker/Room.lua:1-247` [Isaac/Linker/Room.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Room.lua)

### \_Legacy & EmmyLua

- **\_Legacy:** A repository tree containing 354 files of earlier, unrefactored decompilation attempts (`Isaac/_OLD`, `_Legacy/`) retained for reference.
- **EmmyLua:** Type annotation standard (`_EmmyLua/`) utilized across the codebase to provide IDE type-checking, autocompletion for C++ structures, and Lua FFI bindings.
- **Sources:**`LuaEngine/Callbacks.lua:266-267` [LuaEngine/Callbacks.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/LuaEngine/Callbacks.lua)

* * *

## Architecture-to-Code Mapping Diagrams

### Diagram 1: System Architectural Layers to Code Paths

```
Code Entity Space

Natural Language Space

Interface Layer

Linker Layer

Component Layer

Core Logic Layer

Content / Custom Behavior

Isaac/Interface/Entity.lua

Isaac/Linker/Entity.lua

Isaac/Components/Entity/PickupComponent.lua

Isaac/Core/Pickup/Collision.lua

Isaac/Content/ActorSlot.lua
```

_Sources:_`Isaac/Linker/Entity.lua:1-12` [Isaac/Linker/Entity.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity.lua)`Isaac/Components/Entity/PickupComponent.lua:1-52` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)`Isaac/Core/Slot/SlotDamage.lua:1-6` [Isaac/Core/Slot/SlotDamage.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotDamage.lua)

### Diagram 2: Context Plumbing and Entity Lifecycle

```

Context.Common (ctx)
General/Context.lua

Stub.Init(ctx, pickup, ...)
Isaac/Linker/Entity_Pickup.lua

Stub.Update(ctx, pickup)
Isaac/Linker/Entity_Pickup.lua

Component.Entity.Pickup
Isaac/Components/Entity/PickupComponent.lua

TakeDamage(ctx, slot, ...)
Isaac/Core/Slot/SlotDamage.lua

m_ fields & 0x offsets
PickupComponent.lua:2-31
```

_Sources:_`General/Context.lua:1-4` [General/Context.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/General/Context.lua)`Isaac/Linker/Entity_Pickup.lua:64-90` [Isaac/Linker/Entity\_Pickup.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Linker/Entity_Pickup.lua)`Isaac/Components/Entity/PickupComponent.lua:1-32` [Isaac/Components/Entity/PickupComponent.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Components/Entity/PickupComponent.lua)`Isaac/Core/Slot/SlotDamage.lua:8-42` [Isaac/Core/Slot/SlotDamage.lua](https://github.com/Guantol-Lemat/Isaac.LuaDecomps/blob/8a9c6186/Isaac/Core/Slot/SlotDamage.lua)

Dismiss

Refresh this wiki

This wiki was recently refreshed. Please wait7 days to refresh again.

### On this page

- [Glossary](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#glossary)
- [Purpose and Scope](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#purpose-and-scope)
- [Architectural & Codebase Jargon](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#architectural-codebase-jargon)
- [Linker](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#linker)
- [Interface](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#interface)
- [Component](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#component)
- [Stub](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#stub)
- [Context.Common & ctx](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#contextcommon-ctx)
- [m\_ fields](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#m_-fields)
- [\_qqq](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#_qqq)
- [Data Structures & Engine Systems](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#data-structures-engine-systems)
- [ANM2](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#anm2)
- [EntityPtr](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#entityptr)
- [TearFlags & BitSet128](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#tearflags-bitset128)
- [LootList](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#lootlist)
- [HitList](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#hitlist)
- [ItemPool / PoolItem](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#itempool-poolitem)
- [RoomDescriptor & GridEntity & LRoomAreaDesc](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#roomdescriptor-gridentity-lroomareadesc)
- [eState](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#estate)
- [ModEntry](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#modentry)
- [ActorSlot](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#actorslot)
- [MultiShotParams](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#multishotparams)
- [ScoreSheet](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#scoresheet)
- [\_Legacy & EmmyLua](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#_legacy-emmylua)
- [Architecture-to-Code Mapping Diagrams](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#architecture-to-code-mapping-diagrams)
- [Diagram 1: System Architectural Layers to Code Paths](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#diagram-1-system-architectural-layers-to-code-paths)
- [Diagram 2: Context Plumbing and Entity Lifecycle](https://deepwiki.com/Guantol-Lemat/Isaac.LuaDecomps/8-glossary#diagram-2-context-plumbing-and-entity-lifecycle)

Ask Devin about Guantol-Lemat/Isaac.LuaDecomps

Fast

---

