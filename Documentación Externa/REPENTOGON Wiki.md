# REPENTOGON
- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Overview

Relevant source files

- [.gitattributes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitattributes)
- [.github/workflows/release.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml)
- [LICENSE](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LICENSE)
- [README-ZH.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/README-ZH.md?plain=1)
- [README.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/README.md?plain=1)
- [appveyor.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml)
- [appveyor\_launcher.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml)
- [appveyor\_repentogon.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_repentogon.yml)
- [changelog.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt)
- [docs/docs/blog/posts/faq.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/blog/posts/faq.md?plain=1)
- [libzhl/LICENSE](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LICENSE)
- [libzhl/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp)
- [libzhl/functions/ASM.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl)
- [libzhl/functions/EntityRef.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityRef.zhl)
- [libzhl/functions/Shape.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Shape.zhl)
- [loader/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/Version.cpp)
- [repentogon/LuaInterfaces/CustomCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp)
- [repentogon/Patches/ASMPatches.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.h)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.cpp)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.h)
- [repentogon/Patches/ExtraDebugRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp)
- [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)
- [repentogon/Patches/XMLPlayerExtras.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLPlayerExtras.cpp)
- [repentogon/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp)
- [repentogon/resources/scripts/enums\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua)
- [repentogon/resources/scripts/main\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua)
- [version.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt)

REPENTOGON is a comprehensive modding framework for **The Binding of Isaac: Repentance+** (v1.9.7.12.J273) that significantly extends the game's Lua API. It acts as an intermediary layer, providing bug fixes, performance enhancements, and direct access to game internals previously inaccessible to modders.

Unlike traditional mods, REPENTOGON is an "EXE mod" powered by **LibZHL**, a framework that allows it to hook directly into the game's binary. This enables features like custom callbacks, direct memory manipulation, and assembly-level patches.

For detailed architecture information, see [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture).

## Core Components

The framework is composed of several interlocking systems that bridge the gap between the game's C++ engine and the Lua scripting environment.

### ModCallbacks System

The central nervous system of REPENTOGON is its expanded `ModCallbacks` system. It provides over 1400 callback types [repentogon/resources/scripts/enums\_ex.lua1-160](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L1-L160) allowing mods to intercept almost every major game event.

```
Logic Flow: MC_PRE_UPDATE

Yes

No

Game::Update [C++]

ASM Hook: Game_Update_MainUpdate

CallbackState Bitset Check

Lua: MC_PRE_UPDATE

Skip Update?

handle_skipped_update()

super() Game::Update
```

Sources: [repentogon/Patches/ASMPatches/ASMCallbacks.cpp28-111](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L28-L111) [repentogon/resources/scripts/enums\_ex.lua27](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L27-L27)

### Entity and Game Interfaces

REPENTOGON exposes hundreds of internal game functions and variables to Lua. This includes low-level access to `EntityPlayer`, `EntityLaser`, `EntityKnife`, and complex systems like the `ItemPool` and `History` HUD [changelog.txt54-100](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L100)

| Entity Class | Notable REPENTOGON Extensions |
| --- | --- |
| `EntityPlayer` | Innate items, `ImExcited` countdowns, `DonateLuck`, Bag of Crafting calculations [changelog.txt58-79](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L58-L79) |
| `EntityLaser` | `SetInitSound`, `NumChainedLasers` (Monstro's Lung synergy) [changelog.txt54-57](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L57) |
| `Sprite` | `Copy`, `GetSpritesheet`, `SetSpritesheet` per layer [changelog.txt101-104](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L101-L104) |
| `Renderer` | `CreateImage`, `RenderToImage`, `LoadShader` [changelog.txt108-112](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L108-L112) |

Sources: [changelog.txt54-138](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L138)

## System Architecture

REPENTOGON's architecture relies on **ASMPatcher** and **LibZHL** to redirect game logic into custom C++ handlers, which then communicate with the Lua state.

### Bridge: C++ to Lua

The following diagram illustrates how internal game events (like taking damage) are bridged to the Lua environment using `HOOK_METHOD` and `ASMPatch`.

```
Lua Space

Native Code Space (C++)

Entity_Player::TakeDamage

HOOK_METHOD: TakeDamage

CustomCallbacks::Trigger...

lua_State* L

LUA_REGISTRYINDEX

Mod Script Function
```

Sources: [repentogon/LuaInterfaces/CustomCallbacks.cpp96-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L96-L150) [libzhl/functions/ASM.zhl67-75](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl#L67-L75)

### Patching Infrastructure

The framework applies numerous assembly patches at runtime to fix vanilla bugs or inject new logic. These are managed by `PerformASMPatches` [repentogon/Patches/ASMPatches.cpp166-203](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L166-L203)

```
Patch Targets

ASMPatcher Entities

SigScan (Signature Scanning)

sASMPatcher.PatchAt

ASMDefinition (ZHL Definitions)

ASMPatchLogMessage (KAGE_LogMessage)

ASMPatchConsoleRunCommand

PatchPreLaserCollision

PatchGridCollisionCallback
```

Sources: [repentogon/Patches/ASMPatches.cpp60-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L60-L81) [repentogon/Patches/ASMPatches/ASMCallbacks.cpp144-161](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L144-L161) [libzhl/functions/ASM.zhl1-20](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl#L1-L20)

## Versioning and Compatibility

REPENTOGON tracks its version via `version.txt` and exposes it through the global `REPENTOGON` table in Lua [repentogon/resources/scripts/main\_ex.lua1-6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L1-L6) This allows mods to perform version checks using `REPENTOGON.MeetsVersion(targetVersion)` [repentogon/resources/scripts/main\_ex.lua75-101](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L75-L101)

Sources: [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1) [repentogon/resources/scripts/main\_ex.lua4-6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L4-L6) [repentogon/resources/scripts/main\_ex.lua103](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L103-L103)

## Key Features

- **Advanced Rendering**: Custom shaders, render-to-texture, and direct spritesheet manipulation [changelog.txt108-125](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L108-L125)
- **Extended XML**: Define player stats, item behaviors, and achievements directly in XML [repentogon/Patches/XMLPlayerExtras.cpp15-51](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLPlayerExtras.cpp#L15-L51)
- **Innate Item System**: Add items or trinkets to players that don't occupy standard slots, with support for durations and group keys [changelog.txt65-76](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L65-L76)
- **Developer Tools**: ImGui-based log viewer and enhanced debug console [repentogon/Patches/ASMPatches.cpp60-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L60-L81)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#overview)
- [Core Components](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#core-components)
- [ModCallbacks System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#modcallbacks-system)
- [Entity and Game Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#entity-and-game-interfaces)
- [System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#system-architecture)
- [Bridge: C++ to Lua](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#bridge-c-to-lua)
- [Patching Infrastructure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#patching-infrastructure)
- [Versioning and Compatibility](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#versioning-and-compatibility)
- [Key Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON#key-features)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 1.1 Architecture

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Architecture

Relevant source files

- [include/HookSystem.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/include/HookSystem.h)
- [include/libzhl.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/include/libzhl.h)
- [include/logger/logger.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/include/logger/logger.h)
- [libzhl/ASMPatcher.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ASMPatcher.cpp)
- [libzhl/ASMPatcher.hpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ASMPatcher.hpp)
- [libzhl/ByteBuffer.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ByteBuffer.cpp)
- [libzhl/ByteBuffer.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ByteBuffer.h)
- [libzhl/CrashHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/CrashHandler.cpp)
- [libzhl/CrashHandler.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/CrashHandler.h)
- [libzhl/SigScan.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/SigScan.cpp)
- [libzhl/SigScan.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/SigScan.h)
- [libzhl/Signature.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Signature.cpp)
- [libzhl/Signature.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Signature.h)
- [libzhl/dllmain.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/dllmain.cpp)
- [libzhl/filesystem.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/filesystem.cpp)
- [libzhl/functions/Game.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Game.zhl)
- [libzhl/functions/Isaac.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Isaac.zhl)
- [libzhl/functions/KAGE\_Filesys\_FileManager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Filesys_FileManager.zhl)
- [libzhl/functions/Manager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl)
- [libzhl/functions/ModManager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ModManager.zhl)
- [libzhlgen/parsefuncs.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/parsefuncs.lua)
- [loader/loader.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/loader.cpp)
- [logger/logger.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/logger/logger.cpp)
- [offline\_scanner/offline\_scanner.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/offline_scanner/offline_scanner.cpp)
- [repentogon/LuaInterfaces/LuaIsaac.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp)

This document provides a comprehensive overview of REPENTOGON's architecture, covering the relationship between the `libzhl` hooking library and the `repentogon` modding framework, the core design patterns, and how these components work together to enable extensive modding capabilities for The Binding of Isaac: Repentance.

## Core Architecture Overview

REPENTOGON employs a layered architecture consisting of three primary layers: the low-level hooking system (`libzhl`), the high-level modding framework (`repentogon`), and the Lua scripting interface that bridges game code with mod scripts.

```
Mod Scripts

Modding Interface Layer

REPENTOGON Framework Layer

Game Engine Layer

InitZHL

HookMain

ASMPatcher

isaac-ng.exe
Base Game Engine

Manager
g_Manager

Game Systems
Game::Update

libzhl.dll
Hook System

repentogon.dll
Core Framework

LuaEngine
Script Processing

Lua Bindings
LUA_FUNCTION

ModCallbacks
Event System

XMLData
Custom Content

Mod A

Mod B

Mod C
```

**Sources:** [libzhl/functions/Manager.zhl84-138](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L84-L138) [libzhl/dllmain.cpp93-163](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/dllmain.cpp#L93-L163) [repentogon/LuaInterfaces/LuaIsaac.cpp1-31](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L1-L31)

## Hook System Architecture

The `libzhl` library provides the foundation for REPENTOGON's runtime modification capabilities through a sophisticated hooking system that intercepts game function calls and enables custom behavior injection.

```
REPENTOGON Handlers

Game Memory

Hook Processing

ZHL Definition Files

Intercept

Redirect

super()

Manager.zhl
Function Signatures

Game.zhl
Game Logic Hooks

Isaac.zhl
Global Functions

HookSystem
Runtime Interception

SigScan
Signature Scanning

ASMPatcher
FlatPatch / PatchAt

Original Game Functions

Hooked Function Calls

Game Data Structures

HOOK_METHOD Macros

Lua Script Execution

Custom Game Logic
```

The hook system operates through several key mechanisms:

### Function Signature Definition

ZHL files define function signatures using a pattern-matching syntax that identifies functions in the compiled game binary. For example:

- `Manager::Update` and `Manager::Init` are defined in [libzhl/functions/Manager.zhl1-6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L1-L6)
- `Game::Update` and `Game::Render` are defined in [libzhl/functions/Game.zhl43-73](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Game.zhl#L43-L73)
- Global utility functions like `Isaac::Random` are declared in [libzhl/functions/Isaac.zhl6-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Isaac.zhl#L6-L8)

### Runtime Interception

The `SigScan` class performs pattern matching against the game's memory [libzhl/SigScan.cpp160-264](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/SigScan.cpp#L160-L264) Once located, the `ASMPatcher` uses `VirtualProtect` to modify function entry points, typically replacing them with a jump to the hook handler [libzhl/ASMPatcher.cpp168-215](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ASMPatcher.cpp#L168-L215)

REPENTOGON uses `HOOK_METHOD` and `HOOK_METHOD_PRIORITY` macros to define these handlers, allowing them to execute custom logic and optionally call the original function using `super()` [repentogon/LuaInterfaces/LuaIsaac.cpp25-30](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L25-L30)

**Sources:** [libzhl/functions/Manager.zhl1-60](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L1-L60) [libzhl/functions/Game.zhl1-100](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Game.zhl#L1-L100) [libzhl/ASMPatcher.cpp76-114](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ASMPatcher.cpp#L76-L114) [libzhl/SigScan.cpp160-264](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/SigScan.cpp#L160-L264)

## Lua Integration Architecture

REPENTOGON's Lua integration provides a comprehensive scripting interface that exposes game functionality to mod developers through a carefully designed binding system.

```
Mod Scripts

Lua Interface

Lua Integration

C++ Game Engine

g_Manager
Global Manager

g_Game
Global Game

Entity Classes
Entity_Player, etc.

LUA_FUNCTION
Macros

LuaBridge
Type Conversion

Metatables
lua::Metatables

Isaac Global Functions

Entity Methods

Game Methods

Mod Lua Code

ModCallbacks
```

### Type Binding and Metatables

The integration uses `LuaBridge` to map C++ classes to Lua objects. REPENTOGON extends the vanilla API by exposing previously inaccessible internal structures. For example:

- `Entity_Player` is mapped to Lua metatables to allow direct method calls [libzhl/functions/Game.zhl37-39](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Game.zhl#L37-L39)
- Custom functions like `Lua_IsaacFindByTypeFix` bridge the gap between internal `EntityList` queries and Lua tables [repentogon/LuaInterfaces/LuaIsaac.cpp32-65](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L32-L65)

### Function Registration

Functions are registered using the `LUA_FUNCTION` macro, which provides a standardized way to pull arguments from the Lua stack and return values. Examples include:

- `Lua_CreateTimer`: Bridges C++ `Entity_Effect::CreateTimer` to Lua [repentogon/LuaInterfaces/LuaIsaac.cpp167-194](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L167-L194)
- `Lua_StartNewGame`: Exposes `Manager::StartNewGame` with proper `Seeds` object handling [repentogon/LuaInterfaces/LuaIsaac.cpp196-214](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L196-L214)

**Sources:** [repentogon/LuaInterfaces/LuaIsaac.cpp32-214](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L32-L214) [libzhl/functions/Game.zhl161-163](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Game.zhl#L161-L163) [libzhl/functions/Manager.zhl140-142](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L140-L142)

## Data Flow and Integration Points

The following diagram illustrates how data flows through REPENTOGON's architecture during typical mod execution:

```
Mod Response

REPENTOGON Processing

Hook Interception

Game Execution

Intercept

Resume

Manager::Update

Game::Update

Game::Render

ASMPatch
PreserveRegisters

Function Hooks
HOOK_METHOD

SigScan
Signature.cpp

LuaEngine

ModManager
LoadConfigs

Result Processing

Mod Lua Logic

Game Modification
```

### Key Integration Points

| Component | Purpose | Key Files |
| --- | --- | --- |
| `Manager` | Central game state and mod management | [libzhl/functions/Manager.zhl84-138](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L84-L138) |
| `ASMPatcher` | Low-level binary patching for complex hooks | [libzhl/ASMPatcher.cpp14-167](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ASMPatcher.cpp#L14-L167) |
| `SigScan` | Locates game functions by byte patterns | [libzhl/SigScan.cpp1-200](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/SigScan.cpp#L1-L200) |
| `ModManager` | Handles mod loading and configuration | [libzhl/functions/ModManager.zhl1-52](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ModManager.zhl#L1-L52) |
| `Isaac` Namespace | Global utility and cleanup functions | [libzhl/functions/Isaac.zhl1-76](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Isaac.zhl#L1-L76) |

### Performance Considerations

REPENTOGON employs several optimization strategies:

- **Signature Caching**: `SigCache` stores found addresses to avoid re-scanning the entire binary on every launch [libzhl/SigScan.cpp17-152](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/SigScan.cpp#L17-L152)
- **Register Preservation**: `ASMPatch::PreserveRegisters` ensures that the CPU state is maintained during assembly-level hooks to prevent crashes [libzhl/dllmain.cpp56-61](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/dllmain.cpp#L56-L61)
- **Flat Patching**: Minimalistic patching for simple byte changes to avoid unnecessary jump overhead [libzhl/ASMPatcher.cpp111-114](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ASMPatcher.cpp#L111-L114)

**Sources:** [libzhl/ASMPatcher.cpp1-167](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/ASMPatcher.cpp#L1-L167) [libzhl/SigScan.cpp17-152](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/SigScan.cpp#L17-L152) [libzhl/dllmain.cpp41-90](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/dllmain.cpp#L41-L90)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#architecture)
- [Core Architecture Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#core-architecture-overview)
- [Hook System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#hook-system-architecture)
- [Function Signature Definition](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#function-signature-definition)
- [Runtime Interception](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#runtime-interception)
- [Lua Integration Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#lua-integration-architecture)
- [Type Binding and Metatables](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#type-binding-and-metatables)
- [Function Registration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#function-registration)
- [Data Flow and Integration Points](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#data-flow-and-integration-points)
- [Key Integration Points](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#key-integration-points)
- [Performance Considerations](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture#performance-considerations)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 1 Overview

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Overview

Relevant source files

- [.gitattributes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitattributes)
- [.github/workflows/release.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml)
- [LICENSE](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LICENSE)
- [README-ZH.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/README-ZH.md?plain=1)
- [README.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/README.md?plain=1)
- [appveyor.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml)
- [appveyor\_launcher.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml)
- [appveyor\_repentogon.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_repentogon.yml)
- [changelog.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt)
- [docs/docs/blog/posts/faq.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/blog/posts/faq.md?plain=1)
- [libzhl/LICENSE](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LICENSE)
- [libzhl/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp)
- [libzhl/functions/ASM.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl)
- [libzhl/functions/EntityRef.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityRef.zhl)
- [libzhl/functions/Shape.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Shape.zhl)
- [loader/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/Version.cpp)
- [repentogon/LuaInterfaces/CustomCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp)
- [repentogon/Patches/ASMPatches.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.h)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.cpp)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.h)
- [repentogon/Patches/ExtraDebugRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp)
- [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)
- [repentogon/Patches/XMLPlayerExtras.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLPlayerExtras.cpp)
- [repentogon/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp)
- [repentogon/resources/scripts/enums\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua)
- [repentogon/resources/scripts/main\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua)
- [version.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt)

REPENTOGON is a comprehensive modding framework for **The Binding of Isaac: Repentance+** (v1.9.7.12.J273) that significantly extends the game's Lua API. It acts as an intermediary layer, providing bug fixes, performance enhancements, and direct access to game internals previously inaccessible to modders.

Unlike traditional mods, REPENTOGON is an "EXE mod" powered by **LibZHL**, a framework that allows it to hook directly into the game's binary. This enables features like custom callbacks, direct memory manipulation, and assembly-level patches.

For detailed architecture information, see [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture).

## Core Components

The framework is composed of several interlocking systems that bridge the gap between the game's C++ engine and the Lua scripting environment.

### ModCallbacks System

The central nervous system of REPENTOGON is its expanded `ModCallbacks` system. It provides over 1400 callback types [repentogon/resources/scripts/enums\_ex.lua1-160](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L1-L160) allowing mods to intercept almost every major game event.

```
Logic Flow: MC_PRE_UPDATE

Yes

No

Game::Update [C++]

ASM Hook: Game_Update_MainUpdate

CallbackState Bitset Check

Lua: MC_PRE_UPDATE

Skip Update?

handle_skipped_update()

super() Game::Update
```

Sources: [repentogon/Patches/ASMPatches/ASMCallbacks.cpp28-111](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L28-L111) [repentogon/resources/scripts/enums\_ex.lua27](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L27-L27)

### Entity and Game Interfaces

REPENTOGON exposes hundreds of internal game functions and variables to Lua. This includes low-level access to `EntityPlayer`, `EntityLaser`, `EntityKnife`, and complex systems like the `ItemPool` and `History` HUD [changelog.txt54-100](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L100)

| Entity Class | Notable REPENTOGON Extensions |
| --- | --- |
| `EntityPlayer` | Innate items, `ImExcited` countdowns, `DonateLuck`, Bag of Crafting calculations [changelog.txt58-79](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L58-L79) |
| `EntityLaser` | `SetInitSound`, `NumChainedLasers` (Monstro's Lung synergy) [changelog.txt54-57](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L57) |
| `Sprite` | `Copy`, `GetSpritesheet`, `SetSpritesheet` per layer [changelog.txt101-104](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L101-L104) |
| `Renderer` | `CreateImage`, `RenderToImage`, `LoadShader` [changelog.txt108-112](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L108-L112) |

Sources: [changelog.txt54-138](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L138)

## System Architecture

REPENTOGON's architecture relies on **ASMPatcher** and **LibZHL** to redirect game logic into custom C++ handlers, which then communicate with the Lua state.

### Bridge: C++ to Lua

The following diagram illustrates how internal game events (like taking damage) are bridged to the Lua environment using `HOOK_METHOD` and `ASMPatch`.

```
Lua Space

Native Code Space (C++)

Entity_Player::TakeDamage

HOOK_METHOD: TakeDamage

CustomCallbacks::Trigger...

lua_State* L

LUA_REGISTRYINDEX

Mod Script Function
```

Sources: [repentogon/LuaInterfaces/CustomCallbacks.cpp96-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L96-L150) [libzhl/functions/ASM.zhl67-75](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl#L67-L75)

### Patching Infrastructure

The framework applies numerous assembly patches at runtime to fix vanilla bugs or inject new logic. These are managed by `PerformASMPatches` [repentogon/Patches/ASMPatches.cpp166-203](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L166-L203)

```
Patch Targets

ASMPatcher Entities

SigScan (Signature Scanning)

sASMPatcher.PatchAt

ASMDefinition (ZHL Definitions)

ASMPatchLogMessage (KAGE_LogMessage)

ASMPatchConsoleRunCommand

PatchPreLaserCollision

PatchGridCollisionCallback
```

Sources: [repentogon/Patches/ASMPatches.cpp60-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L60-L81) [repentogon/Patches/ASMPatches/ASMCallbacks.cpp144-161](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L144-L161) [libzhl/functions/ASM.zhl1-20](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl#L1-L20)

## Versioning and Compatibility

REPENTOGON tracks its version via `version.txt` and exposes it through the global `REPENTOGON` table in Lua [repentogon/resources/scripts/main\_ex.lua1-6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L1-L6) This allows mods to perform version checks using `REPENTOGON.MeetsVersion(targetVersion)` [repentogon/resources/scripts/main\_ex.lua75-101](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L75-L101)

Sources: [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1) [repentogon/resources/scripts/main\_ex.lua4-6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L4-L6) [repentogon/resources/scripts/main\_ex.lua103](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L103-L103)

## Key Features

- **Advanced Rendering**: Custom shaders, render-to-texture, and direct spritesheet manipulation [changelog.txt108-125](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L108-L125)
- **Extended XML**: Define player stats, item behaviors, and achievements directly in XML [repentogon/Patches/XMLPlayerExtras.cpp15-51](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLPlayerExtras.cpp#L15-L51)
- **Innate Item System**: Add items or trinkets to players that don't occupy standard slots, with support for durations and group keys [changelog.txt65-76](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L65-L76)
- **Developer Tools**: ImGui-based log viewer and enhanced debug console [repentogon/Patches/ASMPatches.cpp60-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L60-L81)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#overview)
- [Core Components](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#core-components)
- [ModCallbacks System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#modcallbacks-system)
- [Entity and Game Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#entity-and-game-interfaces)
- [System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#system-architecture)
- [Bridge: C++ to Lua](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#bridge-c-to-lua)
- [Patching Infrastructure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#patching-infrastructure)
- [Versioning and Compatibility](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#versioning-and-compatibility)
- [Key Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview#key-features)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 2 Lua Modding Api

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Lua Modding API

Relevant source files

- [changelog.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt)
- [docs/docs/Entity.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Entity.md?plain=1)
- [docs/docs/EntityNPC.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/EntityNPC.md?plain=1)
- [docs/docs/EntityPickup.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/EntityPickup.md?plain=1)
- [docs/docs/EntityPlayer.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/EntityPlayer.md?plain=1)
- [docs/docs/GridEntity.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/GridEntity.md?plain=1)
- [docs/docs/Isaac.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Isaac.md?plain=1)
- [docs/docs/Pathfinder.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Pathfinder.md?plain=1)
- [docs/docs/Room.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Room.md?plain=1)
- [docs/docs/enums/ModCallbacks.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/enums/ModCallbacks.md?plain=1)
- [docs/mkdocs.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/mkdocs.yml)
- [libzhl/LuaCore.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LuaCore.cpp)
- [libzhl/LuaCore.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LuaCore.h)
- [libzhl/functions/ASM.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl)
- [libzhl/functions/BeamRenderer.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/BeamRenderer.zhl)
- [libzhl/functions/EntityRef.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityRef.zhl)
- [libzhl/functions/Point.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Point.zhl)
- [repentogon/LuaInterfaces/CustomCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp)
- [repentogon/LuaInterfaces/LuaBeamRenderer.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaBeamRenderer.cpp)
- [repentogon/Patches/ASMPatches.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.h)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.cpp)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.h)
- [repentogon/Patches/XMLPlayerExtras.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLPlayerExtras.cpp)
- [repentogon/resources/scripts/enums\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua)
- [repentogon/resources/scripts/main\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua)

## Purpose and Scope

The Lua Modding API provides a comprehensive scripting interface that allows mods to interact with The Binding of Isaac: Repentance's game systems through Lua scripts. This system exposes C++ game functionality via carefully crafted bindings, enabling mods to modify entity behavior, handle game events, manipulate sprites, control menus, and access game state.

REPENTOGON significantly expands the vanilla API by adding over 1400 new callbacks and hundreds of new methods to existing classes like `EntityPlayer`, `EntityNPC`, and `Sprite`.

This document covers the overall architecture and mechanisms of the Lua API system.

- For specific event handling, see [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks).
- For entity-specific interfaces, see [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces).
- For room and level management APIs, see [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level).
- For item management functionality, see [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool).
- For rendering extensions, see [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis).
- For miscellaneous utilities, see [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis).

## Architecture Overview

The Lua Modding API is built around a central `LuaEngine` that manages the Lua state and coordinates between C++ game systems and Lua mod scripts. The architecture follows a layered approach where C++ game functionality is wrapped in interface functions and registered with the Lua engine.

```
C++ Game Systems

Lua Interface Layer

LuaEngine Core

Lua Mod Scripts

Mod Script A

Mod Script B

Mod Script C

lua_State*
Lua VM Instance

RegisterClasses()
Binding Registration

RunScript()
Script Execution

LuaEntity.cpp
Entity Functions

LuaEntityNPC.cpp
NPC Functions

LuaSprite.cpp
ANM2/Sprite Functions

LuaMenuManager.cpp
Menu Functions

LuaGridEntity.cpp
Grid Functions

LuaInput.cpp
Input Functions

Entity Classes
Entity, Entity_NPC, etc.

ANM2 Class
Animation System

MenuManager
Menu System

GridEntity Classes
Grid System

InputManager
Input System
```

Sources: [libzhl/functions/LuaEngine.zhl1-91](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/LuaEngine.zhl#L1-L91) [repentogon/LuaInterfaces/Entities/LuaEntity.cpp849-945](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L849-L945)

## LuaEngine Core System

The `LuaEngine` serves as the central coordinator for all Lua modding functionality. It maintains the Lua state, handles script execution, and manages the registration of C++ functions to Lua. REPENTOGON utilizes a `CallbackState` bitset to optimize performance by only executing logic for callbacks that have active listeners [repentogon/LuaInterfaces/CustomCallbacks.cpp23-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L23-L40)

| Component | Purpose | Key Methods |
| --- | --- | --- |
| `lua_State* _state` | Lua VM instance | Core Lua execution environment |
| `RegisterClasses()` | Binding registration | Registers all C++ functions to Lua metatables |
| `RunScript()` | Script execution | Executes Lua mod scripts |
| `Init()` | Initialization | Sets up the Lua environment |

The engine follows a hook-based registration pattern where each Lua interface file hooks into the `RegisterClasses` method to add its functions to the appropriate Lua metatables.

```
LuaEngine Registration Flow

LuaEngine::RegisterClasses()

super()
Call base implementation

LuaStackProtector
Stack management

Entity Interface
HOOK_METHOD RegisterClasses

EntityNPC Interface
HOOK_METHOD RegisterClasses

Sprite Interface
HOOK_METHOD RegisterClasses

Menu Interface
HOOK_METHOD RegisterClasses

lua::RegisterFunctions()
ENTITY metatable

lua::RegisterFunctions()
ENTITY_NPC metatable

lua::RegisterFunctions()
SPRITE metatable

lua::RegisterFunctions()
MenuManager global
```

Sources: [libzhl/functions/LuaEngine.zhl4-5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/LuaEngine.zhl#L4-L5) [repentogon/LuaInterfaces/Entities/LuaEntity.cpp849-851](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L849-L851) [repentogon/LuaInterfaces/CustomCallbacks.cpp23-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L23-L40)

## Lua Binding Structure

REPENTOGON uses a robust binding system to bridge the gap between Lua and the internal game engine. This includes exposing complex types like `EntityPlayer`, `EntityNPC`, and `EntityLaser` with significantly expanded functionality.

### Function Implementation Pattern

All Lua binding functions follow this structure:

1. **Parameter Extraction**: Use `lua::GetLuabridgeUserdata` to extract C++ objects from Lua.
2. **Validation**: Check parameter types and ranges using `luaL_check*` functions.
3. **C++ Method Call**: Execute the actual game functionality, often involving libzhl hooks or ASM patches.
4. **Return Value Handling**: Push results back to Lua stack using appropriate push functions.

### Metatable Organization

The Lua API organizes functions into metatables that correspond to C++ class hierarchies. REPENTOGON defines these in `lua::Metatables` [libzhl/LuaCore.h12-149](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LuaCore.h#L12-L149)

| Metatable | Purpose | Key REPENTOGON Additions |
| --- | --- | --- |
| `ENTITY_PLAYER` | Player functionality | `AddInnateTrinket`, `GetInnateCollectibleCount`, `CalculateBagOfCraftingOutput` [changelog.txt58-79](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L58-L79) |
| `ENTITY_NPC` | NPC functionality | `UpdateDirtColor`, `FireProjectilesEx`, `GetHitList` |
| `ENTITY_LASER` | Laser functionality | `SetInitSound`, `GetNumChainedLasers` [changelog.txt54-57](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L57) |
| `SPRITE` | Animation/sprite | `Copy`, `GetSpritesheet`, `SetSpritesheet` [changelog.txt101-104](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L101-L104) |
| `RENDERER` | Visual engine | `CreateImage`, `RenderToImage`, `LoadShader` [changelog.txt108-112](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L108-L112) |

Sources: [libzhl/LuaCore.h12-149](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LuaCore.h#L12-L149) [changelog.txt54-112](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L54-L112) [repentogon/LuaInterfaces/Entities/LuaEntity.cpp854-943](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L854-L943)

## Advanced Scripting Features

### ASM Callbacks and Hooks

REPENTOGON uses `ASMPatcher` to inject Lua callbacks into locations previously inaccessible to modders, such as the character select menu or internal damage calculations [repentogon/Patches/ASMPatches/ASMCallbacks.cpp144-181](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L144-L181) For example, `MC_PRE_LASER_COLLISION` is implemented by patching `Entity_Laser::damage_entities` [repentogon/Patches/ASMPatches/ASMCallbacks.cpp144-181](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L144-L181)

### Custom Type System

The API supports custom REPENTOGON-specific types such as `DestinationQuad`, `SourceQuad`, and `Image` for advanced rendering [changelog.txt117-140](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L117-L140) These are registered via `lua::RegisterNewClass` [libzhl/LuaCore.cpp92-114](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LuaCore.cpp#L92-L114)

```
System Access

Internal Entity Mapping

Metatables::ENTITY_PLAYER

Metatables::ENTITY_NPC

Metatables::ENTITY_LASER

MC_POST_TRIGGER_COLLECTIBLE_ADDED

Entity_Player (C++)

EntityPlayer (Lua)

Entity_NPC (C++)

EntityNPC (Lua)

Entity_Laser (C++)

EntityLaser (Lua)

ModCallbacks System

Lua Mod Logic
```

Sources: [libzhl/LuaCore.h12-149](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LuaCore.h#L12-L149) [repentogon/LuaInterfaces/CustomCallbacks.cpp44-59](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L44-L59) [repentogon/Patches/ASMPatches/ASMCallbacks.cpp121-141](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L121-L141)

## Type Safety and Error Handling

The Lua API implements robust type safety through several mechanisms:

- **Userdata Validation**: `lua::GetLuabridgeUserdata` ensures correct C++ object types.
- **Stack Protection**: `lua::LuaStackProtector` prevents stack corruption during complex callback chains [repentogon/LuaInterfaces/CustomCallbacks.cpp48](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L48-L48)
- **Error Reporting**: `_CBindings.RaiseModError` allows the engine to report mod-specific errors to the log [repentogon/resources/scripts/main\_ex.lua72](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L72-L72)

Sources: [libzhl/LuaCore.cpp9-10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/LuaCore.cpp#L9-L10) [repentogon/LuaInterfaces/CustomCallbacks.cpp48](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L48-L48) [repentogon/resources/scripts/main\_ex.lua15-46](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua#L15-L46)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#lua-modding-api)
- [Purpose and Scope](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#purpose-and-scope)
- [Architecture Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#architecture-overview)
- [LuaEngine Core System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#luaengine-core-system)
- [Lua Binding Structure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#lua-binding-structure)
- [Function Implementation Pattern](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#function-implementation-pattern)
- [Metatable Organization](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#metatable-organization)
- [Advanced Scripting Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#advanced-scripting-features)
- [ASM Callbacks and Hooks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#asm-callbacks-and-hooks)
- [Custom Type System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#custom-type-system)
- [Type Safety and Error Handling](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api#type-safety-and-error-handling)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 2.1 Modcallbacks

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# ModCallbacks

Relevant source files

- [changelog.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt)
- [docs/docs/Entity.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Entity.md?plain=1)
- [docs/docs/EntityNPC.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/EntityNPC.md?plain=1)
- [docs/docs/EntityPickup.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/EntityPickup.md?plain=1)
- [docs/docs/EntityPlayer.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/EntityPlayer.md?plain=1)
- [docs/docs/GridEntity.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/GridEntity.md?plain=1)
- [docs/docs/Isaac.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Isaac.md?plain=1)
- [docs/docs/Pathfinder.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Pathfinder.md?plain=1)
- [docs/docs/Room.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Room.md?plain=1)
- [docs/docs/enums/ModCallbacks.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/enums/ModCallbacks.md?plain=1)
- [docs/mkdocs.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/mkdocs.yml)
- [libzhl/functions/ASM.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl)
- [libzhl/functions/EntityRef.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityRef.zhl)
- [repentogon/LuaInterfaces/CustomCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp)
- [repentogon/LuaInterfaces/CustomCallbacks.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.h)
- [repentogon/Patches/ASMPatches.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.h)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.cpp)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.h)
- [repentogon/Patches/ItemSpoofSystem.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemSpoofSystem.cpp)
- [repentogon/Patches/ItemSpoofSystem.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemSpoofSystem.h)
- [repentogon/Patches/XMLPlayerExtras.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLPlayerExtras.cpp)
- [repentogon/resources/scripts/enums\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua)
- [repentogon/resources/scripts/main\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua)

The ModCallbacks system is REPENTOGON's event-driven API that allows mods to register functions that execute in response to specific game events. This system extends Isaac's original callback framework with over 1400 new callback types, providing comprehensive hooks into virtually every aspect of game logic, from low-level engine updates to high-level UI rendering.

## System Architecture

The ModCallbacks system operates as a central event dispatcher that intercepts game events and routes them to registered Lua mod functions. The system is built on three core components: callback registration, event interception via `HOOK_METHOD`/`HOOK_STATIC`, and performance optimization via bitsets.

### Core Data Flow

The following diagram bridges the natural language event space to the code entities responsible for routing them.

**Title: Event Routing Architecture**

```
Lua Integration Space

REPENTOGON Hook Space

Game Engine Space

Bit set?

pcall

Game::Update

Entity::TakeDamage

HUD::Update

CustomCallbacks Class
(CustomCallbacks.cpp)

ASMCallbacks Class
(ASMCallbacks.cpp)

HOOK_STATIC(Isaac, SetBuiltInCallbackState)

g_LuaEngine->_state

runCallbackRegistry->key

std::bitset<500> CallbackState

Mod Lua Function
```

Sources: [repentogon/LuaInterfaces/CustomCallbacks.cpp22-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L22-L40) [repentogon/Patches/ASMPatches/ASMCallbacks.cpp28-67](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L28-L67) [repentogon/LuaInterfaces/CustomCallbacks.cpp156-167](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L156-L167)

## Callback State Management

REPENTOGON uses two bitsets to track whether any mod has registered for a specific callback. This ensures that the overhead for an unused callback is reduced to a single bitwise check.

- `VanillaCallbackState` (bitset<75>): Tracks vanilla Isaac callbacks and their REPENTOGON reimplementations [repentogon/LuaInterfaces/CustomCallbacks.cpp24](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L24-L24)
- `CallbackState` (bitset<500>): Tracks new REPENTOGON-specific callbacks (IDs starting at 1000) [repentogon/LuaInterfaces/CustomCallbacks.cpp23](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L23-L23)

The `SetBuiltInCallbackState` hook intercepts the game's internal callback registration to update these bitsets [repentogon/LuaInterfaces/CustomCallbacks.cpp25-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L25-L40)

## Key Callback Categories

### 1\. Entity Lifecycle and Combat

REPENTOGON adds deep hooks into entity combat logic, specifically damage and collision.

| Callback ID | Name | Description |
| --- | --- | --- |
| 1006 | `MC_POST_ENTITY_TAKE_DMG` | Triggers after an entity takes damage; supports "ExtraSource" data [repentogon/resources/scripts/enums\_ex.lua6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L6-L6) |
| 1008 | `MC_PRE_PLAYER_TAKE_DMG` | Allows canceling or modifying damage to the player [repentogon/resources/scripts/enums\_ex.lua8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L8-L8) |
| 1248 | `MC_PRE_LASER_COLLISION` | Patched into `Entity_Laser::damage_entities` to allow custom collision logic [repentogon/Patches/ASMPatches/ASMCallbacks.cpp121-141](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L121-L141) |

### 2\. Item and Inventory Systems

These callbacks handle the addition, removal, and modification of items, including the new "Innate" item system.

| Callback ID | Name | Description |
| --- | --- | --- |
| 1004 | `MC_PRE_ADD_COLLECTIBLE` | Triggers before `Entity_Player::AddCollectible`. Can return a table to modify `type`, `charge`, etc [repentogon/LuaInterfaces/CustomCallbacks.cpp96-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L96-L150) |
| 1053 | `MC_POST_TRIGGER_COLLECTIBLE_ADDED` | Runs for real collectibles, wisps, and innate items [changelog.txt47-49](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L47-L49) |
| 1054 | `MC_POST_ADD_INNATE_COLLECTIBLE` | Specifically for items added via the Innate system [repentogon/resources/scripts/enums\_ex.lua55](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L55-L55) |

### 3\. Rendering and UI

REPENTOGON provides extensive hooks for the HUD, Main Menu, and Character Select screen.

**Title: UI Callback Execution Order**

```
MC_POST_RENDER_CHARACTER_SELECT_PORTRAITMC_PRE_RENDER_CHARACTER_SELECT_PORTRAITMC_CAN_SELECT_CHARACTER (1166)Game EngineMC_POST_RENDER_CHARACTER_SELECT_PORTRAITMC_PRE_RENDER_CHARACTER_SELECT_PORTRAITMC_CAN_SELECT_CHARACTER (1166)Game EngineUser hovers characterReturn false to disableStart Render LoopModify Sprite/PositionNative RenderFinalize Frame
```

Sources: [changelog.txt13-22](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L13-L22) [changelog.txt33-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L33-L38)

## Technical Implementation: ASM Injection

Many callbacks cannot be implemented via standard function hooks because the target logic is inlined or mid-function. REPENTOGON uses the `ASMPatcher` to inject calls.

### Example: `MC_PRE_UPDATE` (1026)

This callback triggers before the game's main update cycle. It can be used to effectively pause the game by returning `true`.

- **Target**: `Game_Update_MainUpdate` [repentogon/Patches/ASMPatches/ASMCallbacks.cpp91-93](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L91-L93)
- **Logic**: The patch preserves registers, calls `asm_run_pre_update_callback`, and uses a `JNZ` (Jump if Not Zero) to skip the rest of the `Game::Update` function if the callback returns true [repentogon/Patches/ASMPatches/ASMCallbacks.cpp102-110](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L102-L110)

### Example: Laser Collision

Because "sample" lasers (curving) and "non-sample" lasers (straight) use different logic, two separate ASM patches are applied to inject `MC_PRE_LASER_COLLISION` [repentogon/Patches/ASMPatches/ASMCallbacks.cpp144-181](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L144-L181)

## Callback Return Patterns

REPENTOGON callbacks often support complex return types to modify game behavior:

1. **Boolean**: Usually `false` cancels the event (e.g., `MC_PRE_UPDATE`, `MC_PRE_BOMB_DAMAGE`).
2. **Integer**: Replaces an ID (e.g., returning an integer in `MC_PRE_ADD_COLLECTIBLE` changes the item given).
3. **Table**: Used for multi-parameter modification.

   - `MC_PRE_BOMB_DAMAGE`: Return a table with `Position`, `Damage`, `Radius`, `TearFlags`, or `DamageFlags` [changelog.txt23-26](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L23-L26)
   - `MC_PRE_PLAYER_COLLISION`: Return `{ Collide = bool, SkipCollisionEffects = bool }` [docs/docs/enums/ModCallbacks.md41-48](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/enums/ModCallbacks.md?plain=1#L41-L48)

## Constants and Enums

All callback IDs are defined in the `ModCallbacks` table within the Lua environment.

- **ID Range**: REPENTOGON extensions primarily occupy the 1000–2000 range [repentogon/resources/scripts/enums\_ex.lua1-155](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L1-L155)
- **Deprecated IDs**: Some IDs like 1006 (`MC_POST_TAKE_DMG`) are kept for backwards compatibility but alias to newer names like `MC_POST_ENTITY_TAKE_DMG` [repentogon/resources/scripts/enums\_ex.lua5-6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L5-L6)

Sources: [repentogon/resources/scripts/enums\_ex.lua1-155](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua#L1-L155) [repentogon/LuaInterfaces/CustomCallbacks.cpp1-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp#L1-L150) [repentogon/Patches/ASMPatches/ASMCallbacks.cpp1-185](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L1-L185) [changelog.txt1-53](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt#L1-L53) [docs/docs/enums/ModCallbacks.md1-96](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/enums/ModCallbacks.md?plain=1#L1-L96)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#modcallbacks)
- [System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#system-architecture)
- [Core Data Flow](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#core-data-flow)
- [Callback State Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#callback-state-management)
- [Key Callback Categories](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#key-callback-categories)
- [1\. Entity Lifecycle and Combat](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#1-entity-lifecycle-and-combat)
- [2\. Item and Inventory Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#2-item-and-inventory-systems)
- [3\. Rendering and UI](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#3-rendering-and-ui)
- [Technical Implementation: ASM Injection](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#technical-implementation-asm-injection)
- [Example: \`MC\_PRE\_UPDATE\` (1026)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#example-mc_pre_update-1026)
- [Example: Laser Collision](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#example-laser-collision)
- [Callback Return Patterns](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#callback-return-patterns)
- [Constants and Enums](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks#constants-and-enums)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 2.2 Entity Interfaces

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Entity Interfaces

Relevant source files

- [docs/docs/CcpContainer\_RoomConfigSet.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/CcpContainer_RoomConfigSet.md?plain=1)
- [docs/docs/EntityFamiliar.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/EntityFamiliar.md?plain=1)
- [docs/docs/ItemPool.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/ItemPool.md?plain=1)
- [docs/docs/RoomConfig.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/RoomConfig.md?plain=1)
- [libzhl/functions/BitSet128.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/BitSet128.zhl)
- [libzhl/functions/Entity.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl)
- [libzhl/functions/EntityBomb.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityBomb.zhl)
- [libzhl/functions/EntityEffect.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityEffect.zhl)
- [libzhl/functions/EntityFamiliar.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityFamiliar.zhl)
- [libzhl/functions/EntityKnife.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityKnife.zhl)
- [libzhl/functions/EntityLaser.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityLaser.zhl)
- [libzhl/functions/EntityNPC.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityNPC.zhl)
- [libzhl/functions/EntityPickup.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPickup.zhl)
- [libzhl/functions/EntityPlayer.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPlayer.zhl)
- [libzhl/functions/EntityProjectile.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityProjectile.zhl)
- [libzhl/functions/EntitySlot.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntitySlot.zhl)
- [libzhl/functions/EntityTear.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityTear.zhl)
- [libzhl/functions/LuaEngine.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/LuaEngine.zhl)
- [libzhl/functions/TearParams.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/TearParams.zhl)
- [repentogon/LuaInterfaces/Entities/LuaEntity.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityBomb.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityBomb.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityEffect.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityEffect.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityFamiliar.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityFamiliar.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityKnife.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityKnife.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityLaser.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityLaser.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityPickup.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityPickup.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityProjectile.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityProjectile.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntitySlot.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntitySlot.cpp)
- [repentogon/LuaInterfaces/Entities/LuaEntityTear.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityTear.cpp)
- [repentogon/Patches/FamiliarTags.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/FamiliarTags.cpp)

The Entity Interfaces in REPENTOGON provide programmatic access to game objects through Lua scripting. This page documents the various entity types available in the game, their hierarchy, properties, methods, and how to use them in mods.

## Entity Hierarchy

In "The Binding of Isaac", all game objects are instances of the `Entity` class or one of its specialized subclasses. Each entity type provides functionality specific to its role in the game.

Title: Entity Class Hierarchy

```

```

Sources: [libzhl/functions/Entity.zhl126-231](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L126-L231) [libzhl/functions/EntityPlayer.zhl8-34](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPlayer.zhl#L8-L34) [libzhl/functions/EntityNPC.zhl112-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityNPC.zhl#L112-L150) [libzhl/functions/EntityFamiliar.zhl73-129](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityFamiliar.zhl#L73-L129) [libzhl/functions/EntityPickup.zhl84-147](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPickup.zhl#L84-L147)

## Base Entity Interface

The base `Entity` class provides common properties and methods available to all entity types. REPENTOGON exposes internal fields via getter/setter wrappers in Lua.

### Common Properties

| Property | Type | Description |
| --- | --- | --- |
| `Position` | `Vector` | Entity's position in the game world [libzhl/functions/Entity.zhl147](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L147-L147) |
| `Velocity` | `Vector` | Entity's velocity vector [libzhl/functions/Entity.zhl201](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L201-L201) |
| `Type` | `int` | Entity type ID [libzhl/functions/Entity.zhl129](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L129-L129) |
| `Variant` | `int` | Entity variant ID [libzhl/functions/Entity.zhl130](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L130-L130) |
| `SubType` | `int` | Entity subtype ID [libzhl/functions/Entity.zhl131](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L131-L131) |
| `Visible` | `bool` | Whether the entity is visible [libzhl/functions/Entity.zhl143](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L143-L143) |
| `Dead` | `bool` | Whether the entity is dead [libzhl/functions/Entity.zhl144](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L144-L144) |
| `ShadowSize` | `float` | Size of the entity's shadow [libzhl/functions/Entity.zhl142](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L142-L142) |
| `BossStatusEffectCooldown` | `int` | Cooldown for status effects on bosses [libzhl/functions/Entity.zhl145](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L145-L145) |

Sources: [libzhl/functions/Entity.zhl126-151](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L126-L151) [repentogon/LuaInterfaces/Entities/LuaEntity.cpp72-137](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L72-L137)

### Common Methods

| Method | Description |
| --- | --- |
| `GetPosVel()` | Returns a `PosVel` object containing position and velocity [repentogon/LuaInterfaces/Entities/LuaEntity.cpp113](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L113-L113) |
| `GetNullOffset(name)` | Gets the offset of a sprite null layer [libzhl/functions/Entity.zhl19](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L19-L19) |
| `ForceCollide(other, low)` | Forces collision with another entity [libzhl/functions/Entity.zhl28](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L28-L28) |
| `GiveMinecart(pos, vel)` | Spawns a minecart for the entity [repentogon/LuaInterfaces/Entities/LuaEntity.cpp177](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L177-L177) |
| `ComputeStatusEffectDuration(init, ref)` | Calculates duration based on resistances [libzhl/functions/Entity.zhl16](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L16-L16) |

Sources: [libzhl/functions/Entity.zhl12-55](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L12-L55) [repentogon/LuaInterfaces/Entities/LuaEntity.cpp146-189](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L146-L189)

### Status Effects

REPENTOGON significantly expands the status effect API, exposing internal `Add[Effect]` functions and duration timers.

Title: Status Effect Data Flow

```
Game Engine (libzhl)

C++ Interface

Lua Space

entity:AddBleeding(ref, duration)

Lua_EntityAddBleeding

Entity::AddBleeding

Entity::AddBrimstoneMark
```

Sources: [repentogon/LuaInterfaces/Entities/LuaEntity.cpp7-70](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L7-L70) [libzhl/functions/Entity.zhl59-106](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Entity.zhl#L59-L106)

## Entity Type-Specific Interfaces

### Entity\_Player

The player interface is the most complex, handling inventory, health, and active item logic.

| Method | Description |
| --- | --- |
| `HasCollectible(id, ignoreModifiers, ignoreSpoof)` | Checks for an item, optionally bypassing the `ItemSpoofSystem` [repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp37](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp#L37-L37) |
| `AddCollectible(id, charge, firstTime, slot, varData, pool)` | Adds an item with specific slot/pool parameters [repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp71](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp#L71-L71) |
| `BlockCollectible(id)` | Prevents an item from appearing/functioning via `ItemSpoofSystem` [repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp83](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp#L83-L83) |
| `GetMultiShotPositionVelocity(...)` | Calculates tear patterns for multi-shot items [libzhl/functions/EntityPlayer.zhl71](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPlayer.zhl#L71-L71) |
| `InitTwin(playerType)` | Spawns a Jacob/Esau style twin [libzhl/functions/EntityPlayer.zhl77](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPlayer.zhl#L77-L77) |

Sources: [libzhl/functions/EntityPlayer.zhl32-80](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPlayer.zhl#L32-L80) [repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp37-180](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityPlayer.cpp#L37-L180)

### Entity\_NPC

NPCs represent enemies and bosses. REPENTOGON exposes AI vectors and projectile storage.

| Method | Description |
| --- | --- |
| `FireProjectilesEx(...)` | Fires projectiles and returns a table of the spawned `Entity_Projectile` objects [repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp67](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp#L67-L67) |
| `GetHitList()` | Returns a table of entity indices that this NPC has hit [repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp105](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp#L105-L105) |
| `UpdateDirtColor(lerp)` | Manages the blood/dirt overlay on the NPC sprite [libzhl/functions/EntityNPC.zhl8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityNPC.zhl#L8-L8) |
| `TryForceTarget(target, duration)` | Overrides the NPC's current AI target [libzhl/functions/EntityNPC.zhl13](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityNPC.zhl#L13-L13) |

Sources: [libzhl/functions/EntityNPC.zhl1-127](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityNPC.zhl#L1-L127) [repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp9-103](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp#L9-L103)

### Entity\_Familiar

Familiars follow the player and often mirror their stats.

| Property/Method | Description |
| --- | --- |
| `GetMultiplier()` | Retrieves the familiar's damage multiplier, often cached via ASM patches [repentogon/LuaInterfaces/Entities/LuaEntityFamiliar.cpp182](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityFamiliar.cpp#L182-L182) |
| `MoveDelayNum` | Integer controlling the follower's lag behind the player [libzhl/functions/EntityFamiliar.zhl81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityFamiliar.zhl#L81-L81) |
| `TryAimAtMarkedTarget(...)` | Logic for familiars that track the "Marked" target [libzhl/functions/EntityFamiliar.zhl28](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityFamiliar.zhl#L28-L28) |
| `RemoveFromPlayer(bool)` | Detaches the familiar from the player's follower chain [libzhl/functions/EntityFamiliar.zhl52](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityFamiliar.zhl#L52-L52) |

Sources: [libzhl/functions/EntityFamiliar.zhl1-91](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityFamiliar.zhl#L1-L91) [repentogon/LuaInterfaces/Entities/LuaEntityFamiliar.cpp7-180](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityFamiliar.cpp#L7-L180)

### Entity\_Pickup

Pickups handle items, chests, and shop logic.

| Method | Description |
| --- | --- |
| `TryInitOptionCycle(num)` | Sets up a cycling item (e.g., Tainted Isaac/Choice items) [libzhl/functions/EntityPickup.zhl26](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPickup.zhl#L26-L26) |
| `SetAlternatePedestal(type)` | Changes the pedestal sprite (Devil, Angel, etc.) [libzhl/functions/EntityPickup.zhl10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPickup.zhl#L10-L10) |
| `TryFlip()` | Triggers the "Flip" item behavior on the pickup [libzhl/functions/EntityPickup.zhl38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPickup.zhl#L38-L38) |
| `GetVarData()` | Accesses internal variable data used by specific pickup types [libzhl/functions/EntityPickup.zhl87](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPickup.zhl#L87-L87) |

Sources: [libzhl/functions/EntityPickup.zhl1-147](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityPickup.zhl#L1-L147) [repentogon/LuaInterfaces/Entities/LuaEntityPickup.cpp6-188](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityPickup.cpp#L6-L188)

## Internal Data Access

REPENTOGON provides raw access to entity memory structures via `libzhl` definitions.

Title: Memory to Lua Mapping

```
REPENTOGON Lua API

Native Memory (Entity_NPC)

Offset 0xBB0: Vector _v1

Offset 0xC40: float _shieldStrength

Offset 0xBC8: uint32_t _deliriumBossType

npc.V1

npc:GetShieldStrength()
```

Sources: [libzhl/functions/EntityNPC.zhl128-149](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityNPC.zhl#L128-L149) [repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp120-162](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntityNPC.cpp#L120-L162)

## Summary of Entity Subclasses

REPENTOGON exposes the following specialized interfaces:

- **Entity\_Bomb**: Handles explosion countdowns and costume sprites [libzhl/functions/EntityBomb.zhl48-56](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityBomb.zhl#L48-L56).
- **Entity\_Effect**: Manages visual timeouts and variable data [libzhl/functions/EntityEffect.zhl49-52](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityEffect.zhl#L49-L52).
- **Entity\_Laser**: Controls beam damage and collision logic [repentogon/LuaInterfaces/Entities/LuaEntity.cpp140-144](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Entities/LuaEntity.cpp#L140-L144).
- **Entity\_Projectile**: Handles enemy bullet parameters [libzhl/functions/EntityProjectile.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityProjectile.zhl).
- **Entity\_Slot**: Manages beggars and machines [libzhl/functions/EntitySlot.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntitySlot.zhl).

Sources: [libzhl/functions/EntityBomb.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityBomb.zhl) [libzhl/functions/EntityEffect.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityEffect.zhl) [libzhl/functions/EntityLaser.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityLaser.zhl) [libzhl/functions/EntityProjectile.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityProjectile.zhl) [libzhl/functions/EntitySlot.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntitySlot.zhl)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#entity-interfaces)
- [Entity Hierarchy](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#entity-hierarchy)
- [Base Entity Interface](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#base-entity-interface)
- [Common Properties](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#common-properties)
- [Common Methods](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#common-methods)
- [Status Effects](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#status-effects)
- [Entity Type-Specific Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#entity-type-specific-interfaces)
- [Entity\_Player](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#entity_player)
- [Entity\_NPC](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#entity_npc)
- [Entity\_Familiar](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#entity_familiar)
- [Entity\_Pickup](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#entity_pickup)
- [Internal Data Access](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#internal-data-access)
- [Summary of Entity Subclasses](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces#summary-of-entity-subclasses)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

Syntax error in textmermaid version 11.7.0

---

## 2.3 Room And Level

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Room and Level

Relevant source files

- [docs/docs/Ambush.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Ambush.md?plain=1)
- [docs/docs/LayerState.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/LayerState.md?plain=1)
- [docs/docs/renderer/Beam.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/renderer/Beam.md?plain=1)
- [docs/docs/renderer/Point.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/renderer/Point.md?plain=1)
- [libzhl/functions/Level.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Level.zhl)
- [libzhl/functions/Room.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Room.zhl)
- [libzhl/functions/RoomConfig.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RoomConfig.zhl)
- [libzhl/functions/RoomDescriptor.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RoomDescriptor.zhl)
- [libzhl/functions/RoomSpawn.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RoomSpawn.zhl)
- [repentogon/LogUtility.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LogUtility.h)
- [repentogon/LuaInterfaces/LuaLevel.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaLevel.cpp)
- [repentogon/LuaInterfaces/LuaLevelGenerator.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaLevelGenerator.cpp)
- [repentogon/LuaInterfaces/Room/LuaRoom.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoom.cpp)
- [repentogon/LuaInterfaces/Room/LuaRoomConfig.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoomConfig.cpp)
- [repentogon/LuaInterfaces/Room/LuaRoomConfigSet.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoomConfigSet.cpp)
- [repentogon/LuaInterfaces/Room/LuaRoomConfigStage.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoomConfigStage.cpp)
- [repentogon/LuaInterfaces/Room/LuaRoomDescriptor.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoomDescriptor.cpp)
- [repentogon/LuaInterfaces/Room/Room.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/Room.h)
- [repentogon/Patches/ASMPatches.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.h)
- [repentogon/Patches/ASMPatches/ASMEntityNPC.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityNPC.cpp)
- [repentogon/Patches/ASMPatches/ASMLevel.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMLevel.cpp)
- [repentogon/Patches/ASMPatches/ASMLevel.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMLevel.h)
- [repentogon/Patches/ASMPatches/ASMPlayer.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMPlayer.cpp)
- [repentogon/Patches/ASMPatches/ASMPlayer.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMPlayer.h)
- [repentogon/Patches/ASMPatches/ASMRoom.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMRoom.cpp)
- [repentogon/Patches/ASMPatches/ASMRoom.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMRoom.h)
- [repentogon/Patches/PlayerTags.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/PlayerTags.cpp)
- [repentogon/Patches/StagesStuff.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/StagesStuff.cpp)
- [repentogon/Patches/VirtualRoomSets.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VirtualRoomSets.cpp)
- [repentogon/Patches/VirtualRoomSets.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VirtualRoomSets.h)
- [repentogon/RoomConfigUtility.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/RoomConfigUtility.cpp)
- [repentogon/RoomConfigUtility.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/RoomConfigUtility.h)

This document covers REPENTOGON's Lua APIs for room and level management, including room state manipulation, level progression, and integration with the game's room generation systems. These APIs allow mods to interact with the current room's properties, navigate between rooms, and control level progression.

For information about the underlying room generation algorithms, see [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation). For level generation mechanics, see [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation). For entity management within rooms, see [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces).

## System Architecture

The room and level management system in REPENTOGON operates through several primary classes that work together to maintain game state and provide modding capabilities.

### Room and Level Class Hierarchy

```
Room Components

Lua API Layer

Room Configuration

Game State Management

Game
Central Controller

Level
Stage Management

Room
Current Room State

RoomConfig
Room Templates

RoomDescriptor
Room Instance Data

RoomConfig_Room
Room Template Data

Room Lua Bindings
LuaRoom.cpp

Level Lua Bindings
LuaLevel.cpp

RoomASM
Hook State

GridEntity[447]
Grid System

EntityList
Dynamic Entities

Backdrop
Visual Theme

FXLayers
Visual Effects
```

Sources: [libzhl/functions/Room.zhl146-176](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Room.zhl#L146-L176) [libzhl/functions/Level.zhl94-99](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Level.zhl#L94-L99) [libzhl/functions/RoomConfig.zhl33-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RoomConfig.zhl#L33-L40) [repentogon/LuaInterfaces/Room/LuaRoom.cpp12-64](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoom.cpp#L12-L64)

### Room State Management Flow

```
REPENTOGON Extensions

Level Transitions

Room Lifecycle

Room::Init
Initialize Room

Room::Update
Per-Frame Logic

Room::SaveState
State Persistence

Room::RestoreState
State Restoration

Level::ChangeRoom
Room Navigation

Level::SetNextStage
Stage Progression

Level::generate_dungeon
Floor Layout Gen

VoidGenerationOverride
Multi-Floor Void

ASMPatchWaterDisabler
Custom Water Control

SetRoomClearDelay
Fast Clears
```

Sources: [libzhl/functions/Room.zhl68-96](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Room.zhl#L68-L96) [libzhl/functions/Level.zhl11-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Level.zhl#L11-L38) [repentogon/Patches/ASMPatches/ASMLevel.cpp38-68](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMLevel.cpp#L38-L68) [repentogon/Patches/ASMPatches/ASMRoom.cpp140-165](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMRoom.cpp#L140-L165)

## Room Management API

The `Room` class provides comprehensive control over the current room's state, properties, and visual effects through Lua bindings.

### Core Room Properties

| Property | Type | Description | Lua Access |
| --- | --- | --- | --- |
| `_roomType` | `uint32_t` | Room category (treasure, shop, etc.) | [Room.zhl172](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Room.zhl#L172-L172) |
| `_gridWidth` | `uint32_t` | Room width in grid units | [Room.zhl173](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Room.zhl#L173-L173) |
| `_gridHeight` | `uint32_t` | Room height in grid units | [Room.zhl174](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Room.zhl#L174-L174) |
| `_roomClearDelay` | `int` | Frames until room is considered clear | [Room.zhl178](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Room.zhl#L178-L178) |
| `_waterAmount` | `float` | Depth of water in room (0.0 to 1.0) | [Room.zhl152](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Room.zhl#L152-L152) |

### Grid System Management

The room's grid system uses a 448-slot array (`GridEntity* _gridEntities[0x1BF]`) indexed from 0-447. REPENTOGON provides extensive grid manipulation capabilities:

```
-- Spawn grid entity via descriptor or raw values
local success = room:SpawnGridEntity(gridIndex, gridType, variant, seed, varData)

-- Remove grid entity immediately with pathfinding update
room:RemoveGridEntityImmediate(gridIndex, pathTrail, keepDecoration)

-- Check if an obstacle can be placed (respects entity positions)
local canSpawn = room:CanSpawnObstacleAtPosition(gridIndex, force)
```

Sources: [repentogon/LuaInterfaces/Room/LuaRoom.cpp12-42](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoom.cpp#L12-L42) [repentogon/LuaInterfaces/Room/LuaRoom.cpp66-72](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/LuaRoom.cpp#L66-L72) [libzhl/functions/Room.zhl26-33](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Room.zhl#L26-L33)

### Visual Effects and Environment

REPENTOGON exposes numerous visual effect controls through the `Room` class:

#### Water System

The water system is managed via internal pointers to the `Room` object's state. Setting water color triggers a lerp to the target color.

- **Get/Set Water Amount**: `room:GetWaterAmount()` / `room:SetWaterAmount(float)` [LuaRoom.cpp74-89](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L74-L89)
- **Water Color**: `room:SetWaterColor(KColor)` sets `_waterLerpTargetColor` and resets the lerp duration [LuaRoom.cpp112-120](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L112-L120)
- **Water Current**: `room:SetWaterCurrent(Vector)` modifies the physics force applied to entities [LuaRoom.cpp143-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L143-L150)

#### Backdrop and Rendering

Mods can force a backdrop change or modify floor colors:

- **Set Backdrop**: `room:SetBackdrop(id, changeDecoration)` [LuaRoom.cpp54-64](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L54-L64)
- **Floor Color**: `room:GetFloorColor()` returns a `ColorMod` [LuaRoom.cpp91-99](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L91-L99)
- **Lighting Alpha**: `room:GetLightingAlpha()` [Room.zhl44](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Room.zhl#L44-L44)

### Room State Persistence

The room system includes save/restore functionality for maintaining state across room transitions, managed via the `RoomDescriptor`.

```
-- Save the current room state to its descriptor
room:SaveState()

-- Restore the room state from its descriptor
room:RestoreState()
```

Sources: [libzhl/functions/Room.zhl92-96](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Room.zhl#L92-L96) [libzhl/functions/Room.zhl171](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Room.zhl#L171-L171)

## Level Management API

The `Level` class manages stage progression, room navigation, and level-wide state.

### Level Structure and Progression

| Function | Description | Source |
| --- | --- | --- |
| `SetStage(id, alt)` | Forcefully changes the current stage and alt-path type | [Level.zhl2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Level.zhl#L2-L2) |
| `ChangeRoom(idx, dim)` | Transitions the player to a room at index in a specific dimension | [Level.zhl11](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Level.zhl#L11-L11) |
| `IsAltPath()` | Returns true if the current stage is on the alt-path (Downpour, etc.) | [Level.zhl50](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Level.zhl#L50-L50) |
| `GetDimension()` | Returns current dimension (0: Normal, 1: Secondary, 2: Death Certificate) | [LuaLevel.cpp71-75](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaLevel.cpp#L71-L75) |

### Special Path Detection

REPENTOGON allows overriding and detecting special quest paths:

- **Abandoned Mineshaft**: `level:HasAbandonedMineshaft()` [LuaLevel.cpp19-25](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaLevel.cpp#L19-L25)
- **Mirror Dimension**: `level:HasMirrorDimension()` [LuaLevel.cpp27-33](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaLevel.cpp#L27-L33)
- **Photo Door**: `level:HasPhotoDoor()` [LuaLevel.cpp35-41](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaLevel.cpp#L35-L41)
- **Force Special Quest**: Mods can use `level:SetForceSpecialQuest(int)` to force these paths regardless of stage [LuaLevel.cpp82-85](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaLevel.cpp#L82-L85)

Sources: [repentogon/LuaInterfaces/Level.cpp19-115](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Level.cpp#L19-L115) [libzhl/functions/Level.zhl22-30](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Level.zhl#L22-L30)

## Room Generation and Placement

REPENTOGON exposes the internal logic used to determine if a room can be placed in the level layout.

### Room Placement Validation

The `CanPlaceRoom` logic (and its Lua wrapper `Level:CanPlaceRoom`) checks if a room shape fits at a specific grid index without overlapping existing rooms or violating neighbor rules.

```
-- Check if a room can be placed at a specific grid index
local canPlace = level:CanPlaceRoom(roomShape, doorMask, gridIndex, dimension, allowMultipleDoors, allowSpecialNeighbors, allowNoNeighbors)
```

Sources: [repentogon/LuaInterfaces/LuaLevel.cpp180-211](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaLevel.cpp#L180-L211) [repentogon/LuaInterfaces/Room/RoomPlacement.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Room/RoomPlacement.h)

### Void Generation Override

REPENTOGON patches `Level::generate_dungeon` for the Void (Stage 12) to allow it to draw rooms from all unlocked floors, rather than just a subset.

- **Better Void Generation**: If enabled in options, it pulls from all unlocked StbTypes [ASMLevel.cpp120-133](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/ASMLevel.cpp#L120-L133)
- **Backdrop Matching**: Void rooms with specific subtypes will now load the appropriate backdrop and FX for the stage they represent [ASMLevel.cpp168-188](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/ASMLevel.cpp#L168-L188)

Sources: [repentogon/Patches/ASMPatches/ASMLevel.cpp38-68](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMLevel.cpp#L38-L68) [repentogon/Patches/ASMPatches/ASMLevel.cpp103-136](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMLevel.cpp#L103-L136)

## Advanced Room Features

### Rail System

REPENTOGON provides direct access to the rail grid used by minecarts:

- **Get Rail**: `room:GetRail(index)` returns the `RailType` or `nil` if empty [LuaRoom.cpp162-180](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L162-L180)
- **Set Rail**: `room:SetRail(index, railType)` allows building custom tracks [LuaRoom.cpp190-209](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L190-L209)

### Shop Mechanics

- **Price Calculation**: `room:GetShopItemPrice(variant, subtype, shopItemID)` calculates the final price including discounts [LuaRoom.cpp44-52](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L44-L52)
- **Restocking**: `room:TriggerRestock(gridIdx, shopIdx)` forces a shop slot to restock [LuaRoom.cpp182-188](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/LuaRoom.cpp#L182-L188)
- **Discounts**: `room:TryGetShopDiscount(shopItemIdx, price)` checks for Steam Sale/Member Card effects [Room.zhl77](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Room.zhl#L77-L77)

### Room Clear Logic

REPENTOGON allows modifying the "Quick Room Clear" behavior via options, which reduces the `_roomClearDelay` from the vanilla 10 frames to 3 frames, and the `roomSaveStateDelay` from 7 frames to 1 frame.

Sources: [repentogon/Patches/ASMPatches/ASMRoom.cpp158-165](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMRoom.cpp#L158-L165) [libzhl/functions/Room.zhl178](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Room.zhl#L178-L178)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-and-level)
- [System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#system-architecture)
- [Room and Level Class Hierarchy](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-and-level-class-hierarchy)
- [Room State Management Flow](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-state-management-flow)
- [Room Management API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-management-api)
- [Core Room Properties](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#core-room-properties)
- [Grid System Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#grid-system-management)
- [Visual Effects and Environment](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#visual-effects-and-environment)
- [Water System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#water-system)
- [Backdrop and Rendering](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#backdrop-and-rendering)
- [Room State Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-state-persistence)
- [Level Management API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#level-management-api)
- [Level Structure and Progression](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#level-structure-and-progression)
- [Special Path Detection](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#special-path-detection)
- [Room Generation and Placement](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-generation-and-placement)
- [Room Placement Validation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-placement-validation)
- [Void Generation Override](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#void-generation-override)
- [Advanced Room Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#advanced-room-features)
- [Rail System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#rail-system)
- [Shop Mechanics](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#shop-mechanics)
- [Room Clear Logic](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level#room-clear-logic)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 2.4 Itempool

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# ItemPool

Relevant source files

- [libzhl/IsaacRepentance\_static.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/IsaacRepentance_static.cpp)
- [libzhl/functions/EntitySaveState.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntitySaveState.zhl)
- [libzhl/functions/ExtraTypes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ExtraTypes)
- [libzhl/functions/Global.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Global.zhl)
- [libzhl/functions/ItemConfigCard.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemConfigCard.zhl)
- [libzhl/functions/ItemConfigCostume.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemConfigCostume.zhl)
- [libzhl/functions/ItemConfigPill.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemConfigPill.zhl)
- [libzhl/functions/ItemPool.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl)
- [libzhl/functions/ItemPool\_Item.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl)
- [repentogon/LuaInterfaces/LuaItemConfig.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemConfig.cpp)
- [repentogon/LuaInterfaces/LuaItemPool.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp)
- [repentogon/Patches/CardsExtras.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CardsExtras.cpp)
- [repentogon/Patches/CardsExtras.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CardsExtras.h)
- [repentogon/Patches/GameStateManagement.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/GameStateManagement.h)
- [repentogon/Patches/ItemPoolManager.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.cpp)
- [repentogon/Patches/ItemPoolManager.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h)
- [repentogon/Utils/EntitySaveStateUtils.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Utils/EntitySaveStateUtils.h)

The ItemPool system manages the generation and distribution of collectibles, trinkets, pills, and cards throughout The Binding of Isaac: Repentance. REPENTOGON extends this system with comprehensive Lua bindings and advanced pool management capabilities, allowing mods to inspect, modify, and create custom item pools.

For information about entity-related item interactions, see [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces). For XML-based item configuration, see [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system).

## Architecture Overview

The ItemPool system consists of multiple interconnected components that handle different aspects of item generation and management. REPENTOGON introduces `ItemPoolManager` to bridge vanilla `ItemPool` structures with extended modding capabilities.

### System Interaction Diagram

```
RNG System

Pool Management Extensions

Item Management

Core ItemPool System

ItemPool (ZHL Struct)

ItemPool_Item
Individual Pool Data

PoolItem
Item with Weight Data

ItemConfig
Item Definitions

ItemConfig_Item
Collectible Data

ItemConfig_Card
Card Data

ItemConfig_Card_EX
Extended Weight/Availability

ItemPoolManager
Pool Registration System

LuaItemPool.cpp
Lua Interface Layer

CardsExtras.cpp
Weighted Card System

RNG Struct

WeightedOutcomePicker
Weighted Selection
```

Sources: [repentogon/LuaInterfaces/LuaItemPool.cpp1-100](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp#L1-L100) [libzhl/functions/ItemPool.zhl73-88](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L73-L88) [libzhl/functions/ItemPool\_Item.zhl1-17](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl#L1-L17) [repentogon/Patches/CardsExtras.h29-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CardsExtras.h#L29-L40)

## Core Components

### ItemPool Structure

The `ItemPool` class contains 31 individual item pools, each corresponding to different game contexts such as treasure rooms, shops, boss rewards, and special pools.

| Component | Type | Purpose |
| --- | --- | --- |
| `_pools[31]` | `ItemPool_Item` | Array of individual item pools [libzhl/functions/ItemPool.zhl78](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L78-L78) |
| `_itemPoolRNG` | `RNG` | Random number generator for pool selection [libzhl/functions/ItemPool.zhl80](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L80-L80) |
| `_removedCollectibles` | `vector_bool` | Tracks permanently removed items [libzhl/functions/ItemPool.zhl81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L81-L81) |
| `_roomBlacklistedCollectibles` | `vector_bool` | Tracks room-specific blacklisted items [libzhl/functions/ItemPool.zhl82](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L82-L82) |
| `_trinketPoolItems` | `vector_TrinketPoolItem` | Available trinkets [libzhl/functions/ItemPool.zhl83](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L83-L83) |
| `_pillEffects[15]` | `int` | Pill color to effect mappings [libzhl/functions/ItemPool.zhl85](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L85-L85) |
| `_idendifiedPillEffects[15]` | `bool` | Pill identification status [libzhl/functions/ItemPool.zhl86](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L86-L86) |

Sources: [libzhl/functions/ItemPool.zhl73-88](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L73-L88)

### ItemPool\_Item Structure

Each individual pool contains weighted item lists and management data.

| Member | Type | Description |
| --- | --- | --- |
| `_totalWeight` | `float` | Sum of all item weights in the pool [libzhl/functions/ItemPool\_Item.zhl12](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl#L12-L12) |
| `_poolList` | `vector_PoolItem` | List of items available in this pool [libzhl/functions/ItemPool\_Item.zhl13](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl#L13-L13) |
| `_rng1`, `_rng2` | `RNG` | Internal RNG states for item selection [libzhl/functions/ItemPool\_Item.zhl14-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl#L14-L15) |
| `_bibleUpgrade` | `uint32_t` | Bible transformation counter [libzhl/functions/ItemPool\_Item.zhl16](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl#L16-L16) |

Sources: [libzhl/functions/ItemPool\_Item.zhl1-17](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl#L1-L17)

## Lua API Interface

REPENTOGON provides extensive Lua bindings for ItemPool manipulation through the `ItemPool` userdata type.

### Extended Card Logic (CardsEX)

REPENTOGON replaces the vanilla card picking logic with a weighted system.

```

Success

Success

Success

Lua_ItemPoolGetCardEx

CardsEX::pick_card

Check Special Chance

Check Rune Chance

Check Suit Chance

CardPool::PickCard
```

Sources: [repentogon/Patches/CardsExtras.cpp227-260](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CardsExtras.cpp#L227-L260) [repentogon/LuaInterfaces/LuaItemPool.cpp69-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp#L69-L81)

### Weighted Item Selection

The `PickCollectible` function exposes the internal weighted selection mechanism to Lua.

| Argument | Type | Description |
| --- | --- | --- |
| `poolType` | `int` | The pool to pick from |
| `decrease` | `bool` | Whether to decrease item weight after picking |
| `rng` | `RNG*` | RNG object to use for selection |
| `flags` | `uint32_t` | Generation flags |

Sources: [repentogon/LuaInterfaces/LuaItemPool.cpp174-244](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp#L174-L244)

## Item Pool Manager

The `ItemPoolManager` is a singleton that handles the lifecycle of item pools, including custom pools defined by mods.

### Core Manager Functions

- `__LoadPools()`: Parses item pools from XML files [repentogon/Patches/ItemPoolManager.h61](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h#L61-L61)
- `GetItemPool(id)`: Retrieves an `ItemPool` object by its ID [repentogon/Patches/ItemPoolManager.h75](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h#L75-L75)
- `IsItemPoolInitialized()`: Checks if the system is ready for item generation [repentogon/Patches/ItemPoolManager.h74](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h#L74-L74)

### Custom Pool Logic

REPENTOGON allows for "Virtual Items" and "Temporary Items":

- **Virtual Items**: Items added to pools that persist across the session [repentogon/Patches/ItemPoolManager.h126](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h#L126-L126)
- **Temporary Items**: Items added to a pool that are removed under specific conditions [repentogon/Patches/ItemPoolManager.h169](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h#L169-L169)

Sources: [repentogon/Patches/ItemPoolManager.h1-180](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h#L1-L180)

## Data Flow: Item Generation

The following diagram illustrates the data flow when a collectible is requested via the Lua API.

```
RNGItemPoolManagerItemPoolLuaItemPoolLuaRNGItemPoolManagerItemPoolLuaItemPoolLuaGetCollectibleEx(pool, seed, flags)GetCollectible(poolType, seed, flags, default)pick_collectible(targetWeight, poolData, flags)RandomFloat()PoolItem* (result)Item ID (integer)
```

Sources: [repentogon/LuaInterfaces/LuaItemPool.cpp83-109](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp#L83-L109) [libzhl/functions/ItemPool.zhl26-32](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L26-L32)

## Pill and Card Management

The ItemPool system also manages pills and cards with identification mechanics:

| Function | Source | Purpose |
| --- | --- | --- |
| `IdentifyPill` | [libzhl/functions/ItemPool.zhl68](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L68-L68) | Marks a pill color as identified |
| `IsPillIdentified` | [libzhl/functions/ItemPool.zhl70](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L70-L70) | Checks if a pill color is identified |
| `GetPillEffect` | [libzhl/functions/ItemPool.zhl64](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L64-L64) | Returns the effect assigned to a color |
| `ForceAddPillEffect` | [libzhl/functions/ItemPool.zhl52](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L52-L52) | Forces a specific pill effect into the rotation |

Sources: [libzhl/functions/ItemPool.zhl52-72](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L52-L72)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#itempool)
- [Architecture Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#architecture-overview)
- [System Interaction Diagram](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#system-interaction-diagram)
- [Core Components](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#core-components)
- [ItemPool Structure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#itempool-structure)
- [ItemPool\_Item Structure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#itempool_item-structure)
- [Lua API Interface](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#lua-api-interface)
- [Extended Card Logic (CardsEX)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#extended-card-logic-cardsex)
- [Weighted Item Selection](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#weighted-item-selection)
- [Item Pool Manager](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#item-pool-manager)
- [Core Manager Functions](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#core-manager-functions)
- [Custom Pool Logic](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#custom-pool-logic)
- [Data Flow: Item Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#data-flow-item-generation)
- [Pill and Card Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool#pill-and-card-management)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 2.5 Rendering And Visual Apis

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Rendering and Visual APIs

Relevant source files

- [docs/docs/Input.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Input.md?plain=1)
- [docs/docs/RNG.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/RNG.md?plain=1)
- [docs/docs/enums/BlendFactor.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/enums/BlendFactor.md?plain=1)
- [docs/docs/enums/BlendType.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/enums/BlendType.md?plain=1)
- [docs/docs/renderer/BlendMode.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/renderer/BlendMode.md?plain=1)
- [docs/docs/renderer/Shape.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/renderer/Shape.md?plain=1)
- [libzhl/functions/ANM2.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ANM2.zhl)
- [libzhl/functions/AnimationState.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/AnimationState.zhl)
- [libzhl/functions/BlendMode.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/BlendMode.zhl)
- [libzhl/functions/ColorMod.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ColorMod.zhl)
- [libzhl/functions/DestinationQuad.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/DestinationQuad.zhl)
- [libzhl/functions/FXParams.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/FXParams.zhl)
- [libzhl/functions/KAGE\_Graphics\_Manager\_GL.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Graphics_Manager_GL.zhl)
- [libzhl/functions/KAGE\_Graphics\_Shader.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Graphics_Shader.zhl)
- [libzhl/functions/KAGE\_Graphics\_Vertex.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Graphics_Vertex.zhl)
- [libzhl/functions/LayerData.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/LayerData.zhl)
- [libzhl/functions/LayerState.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/LayerState.zhl)
- [libzhl/functions/SourceQuad.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/SourceQuad.zhl)
- [libzhl/functions/Vector2.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Vector2.zhl)
- [repentogon/LuaInterfaces/LuaBlendMode.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaBlendMode.cpp)
- [repentogon/LuaInterfaces/LuaBlendMode.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaBlendMode.h)
- [repentogon/LuaInterfaces/LuaColor.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaColor.cpp)
- [repentogon/LuaInterfaces/LuaColorModifier.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaColorModifier.cpp)
- [repentogon/LuaInterfaces/LuaFXParams.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaFXParams.cpp)
- [repentogon/LuaInterfaces/LuaRNG.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaRNG.cpp)
- [repentogon/LuaInterfaces/LuaRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaRender.cpp)
- [repentogon/LuaInterfaces/LuaRender.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaRender.h)
- [repentogon/LuaInterfaces/LuaSprite.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaSprite.cpp)
- [repentogon/LuaInterfaces/LuaVector.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaVector.cpp)
- [repentogon/Patches/Init.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/Init.cpp)
- [repentogon/Patches/MesaShaderFix.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MesaShaderFix.cpp)
- [repentogon/ShaderLoader.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ShaderLoader.cpp)
- [repentogon/ShaderLoader.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ShaderLoader.h)
- [repentogon/Utils/ImageUtils.hpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Utils/ImageUtils.hpp)
- [repentogon/Utils/ShaderUtils.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Utils/ShaderUtils.h)
- [repentogon/Utils/ShaderUtils.hpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Utils/ShaderUtils.hpp)
- [repentogon/resources/scripts/repentogon\_extras/changelog\_official\_text.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/changelog_official_text.lua)

REPENTOGON significantly expands the rendering capabilities of _The Binding of Isaac: Repentance_ by exposing internal engine structures and providing new Lua-facing APIs for advanced visual manipulation. This includes direct access to the `ANM2` (Sprite) animation system, custom shader loading, programmable blend modes, and the `FXParams` system for room-wide visual effects.

## The ANM2 and Sprite System

In REPENTOGON, the `Sprite` class (internally `ANM2`) is a high-level wrapper around the game's animation engine. REPENTOGON exposes the underlying `LayerState` and `AnimationState` structures, allowing mods to manipulate individual animation layers, swap spritesheets with raw image data, and query frame-perfect event data.

### Data Flow: Sprite Rendering

The following diagram illustrates how an `ANM2` object processes its internal states to produce a rendered frame.

**Sprite Rendering Architecture**

```
Lua Interface [repentogon/LuaInterfaces/LuaSprite.cpp]

ANM2 [libzhl/functions/ANM2.zhl]

ANM2::Render

AnimationState [_animState]

LayerState Array [_layerState]

AnimationData [_animData]

KAGE_SmartPointer_ImageBase [_spriteSheet]

Lua_SpriteGetLayer

Lua_SpriteSetSpritesheet

glBlendFuncSeparate

OpenGL Texture
```

Sources: [libzhl/functions/ANM2.zhl1-114](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ANM2.zhl#L1-L114) [repentogon/LuaInterfaces/LuaSprite.cpp114-137](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaSprite.cpp#L114-L137)

### Key Components

- **LayerState**: Represents a single layer within an `.anm2` file. It contains its own `ColorMod`, `BlendMode`, and `Vector` position [libzhl/functions/LayerState.zhl1-50](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/LayerState.zhl#L1-L50)
- **AnimationState**: Tracks the current playback progress, including `_animFrame`, whether it `_isPlaying`, and event triggers [libzhl/functions/AnimationState.zhl34-65](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/AnimationState.zhl#L34-L65)
- **NullFrame**: Provides transform data for "null" layers used as attachment points [libzhl/functions/AnimationState.zhl1-7](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/AnimationState.zhl#L1-L7)

## Custom Shaders and ShaderLoader

REPENTOGON introduces a `ShaderLoader` system that allows mods to load custom `.vs` (vertex) and `.fs` (fragment) shaders from mod folders. Unlike vanilla shaders, these can have custom vertex descriptors and attributes.

### Shader Loading Logic

The `ShaderLoader` ensures that custom shaders are compatible with the game's rendering pipeline by validating vertex attributes.

**Shader Validation and Compilation**

```

No

Success

ShaderLoader::LoadShader

normalize_shader_path

In Cache?

find_shader (Mod Folders)

KAGE_Graphics_Manager_GL::LoadShader

is_vertex_descriptor_compatible

Store in s_shaderMap

Return KAGE_Graphics_Shader*
```

Sources: [repentogon/ShaderLoader.cpp1-196](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ShaderLoader.cpp#L1-L196) [libzhl/functions/KAGE\_Graphics\_Shader.zhl36-64](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Graphics_Shader.zhl#L36-L64)

### Vertex Attributes

REPENTOGON maps Lua tables to C++ vertex buffers using `fill_shader_vertices`. It supports several formats:

- `FLOAT`: Single value.
- `VEC_2`, `VEC_3`, `VEC_4`: Mapped from Lua tables to `float` arrays [repentogon/LuaInterfaces/LuaRender.cpp49-141](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaRender.cpp#L49-L141)

## Blend Modes and Color Modifiers

REPENTOGON exposes the `BlendMode` struct, allowing for arbitrary OpenGL blending equations beyond the standard `Normal` and `Additive` modes.

### BlendMode Configuration

The `BlendMode` class controls the parameters for `glBlendFuncSeparate`.

| Parameter | Description |
| --- | --- |
| `RGBSourceFactor` | Factor for source RGB (internally `_rgbSourceFactor`) |
| `RGBDestinationFactor` | Factor for destination RGB (internally `_rgbDestFactor`) |
| `AlphaSourceFactor` | Factor for source Alpha (internally `_alphaSourceFactor`) |
| `AlphaDestinationFactor` | Factor for destination Alpha (internally `_alphaDestFactor`) |
| `Equation` | The blend equation (e.g., `FUNC_ADD`) |

Sources: [repentogon/LuaInterfaces/LuaBlendMode.cpp33-120](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaBlendMode.cpp#L33-L120) [docs/docs/renderer/BlendMode.md7-42](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/renderer/BlendMode.md?plain=1#L7-L42)

### ColorMod

The `ColorMod` structure is used extensively for tinting and colorizing. It consists of:

- `_tint`: A `VEC_4` multiplied with the texture color.
- `_colorize`: A `VEC_4` used to override the texture color.
- `_offset`: A `VEC_3` added to the final color result.

Sources: [libzhl/functions/ColorMod.zhl1-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ColorMod.zhl#L1-L15) [repentogon/LuaInterfaces/LuaColor.cpp8-100](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaColor.cpp#L8-L100)

## FXParams System

The `FXParams` system controls room-wide visual effects, including water rendering, shadows, and global brightness/contrast. REPENTOGON exposes these values to Lua, allowing for dynamic environment changes.

### FXParams Structure

The `FXParams` struct is initialized via `FXParams::Init()` and contains:

- **Water**: `useWaterV2` (bool), `waterColor` (KColor), and `waterEffectColor` (ColorMod).
- **Lighting**: `lightColor` (KColor) and `roomColor` (KColor).
- **Post-Processing**: `brightness` and `contrast` (float).

Sources: [libzhl/functions/FXParams.zhl1-21](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/FXParams.zhl#L1-L21) [repentogon/LuaInterfaces/LuaFXParams.cpp1-50](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaFXParams.cpp#L1-L50)

## Image and Surface Rendering

REPENTOGON allows mods to load raw images into `LuaImage` objects, which can then be used as spritesheets or render targets.

### RenderToSurface

The `RenderToSurface` utility function facilitates drawing to a specific graphics surface:

1. **Push**: Saves the current render target using `Rendering::PushCurrentRenderTarget`.
2. **Set**: Changes the target to the desired surface via `g_KAGE_Graphics_Manager.SetCurrentRenderTarget`.
3. **Render**: Executes the provided Lua/C++ render function.
4. **Present/Restore**: Finalizes the draw call and restores the previous target.

Sources: [repentogon/LuaInterfaces/LuaRender.cpp35-47](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaRender.cpp#L35-L47) [repentogon/LuaInterfaces/LuaRender.cpp224-260](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaRender.cpp#L224-L260)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#rendering-and-visual-apis)
- [The ANM2 and Sprite System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#the-anm2-and-sprite-system)
- [Data Flow: Sprite Rendering](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#data-flow-sprite-rendering)
- [Key Components](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#key-components)
- [Custom Shaders and ShaderLoader](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#custom-shaders-and-shaderloader)
- [Shader Loading Logic](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#shader-loading-logic)
- [Vertex Attributes](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#vertex-attributes)
- [Blend Modes and Color Modifiers](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#blend-modes-and-color-modifiers)
- [BlendMode Configuration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#blendmode-configuration)
- [ColorMod](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#colormod)
- [FXParams System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#fxparams-system)
- [FXParams Structure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#fxparams-structure)
- [Image and Surface Rendering](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#image-and-surface-rendering)
- [RenderToSurface](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis#rendertosurface)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 2.6 Utility Apis

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Utility APIs

Relevant source files

- [docs/docs/Capsule.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/Capsule.md?plain=1)
- [docs/docs/CostumeSpriteDesc.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/CostumeSpriteDesc.md?plain=1)
- [docs/docs/ProceduralItem.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/ProceduralItem.md?plain=1)
- [docs/docs/WeightedOutcomePicker.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/WeightedOutcomePicker.md?plain=1)
- [docs/docs/examples/WeightedOutcomes.md](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/examples/WeightedOutcomes.md?plain=1)
- [docs/docs/examples/videos/capsule\_null\_layer.mp4](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/examples/videos/capsule_null_layer.mp4)
- [docs/docs/examples/videos/weighted\_outcome\_chest.mp4](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/examples/videos/weighted_outcome_chest.mp4)
- [docs/docs/examples/zips/repentogon-null-capsules.zip](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/examples/zips/repentogon-null-capsules.zip)
- [docs/docs/examples/zips/repentogon-weighted-outcome.zip](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/examples/zips/repentogon-weighted-outcome.zip)
- [include/logger/logger.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/include/logger/logger.h)
- [libzhl/dllmain.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/dllmain.cpp)
- [libzhl/functions/Camera.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Camera.zhl)
- [libzhl/functions/Capsule.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Capsule.zhl)
- [libzhl/functions/Font.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Font.zhl)
- [libzhl/functions/FontSettings.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/FontSettings.zhl)
- [libzhl/functions/Isaac.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Isaac.zhl)
- [libzhl/functions/KAGE\_Filesys\_FileManager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Filesys_FileManager.zhl)
- [libzhl/functions/KColor.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KColor.zhl)
- [libzhl/functions/Manager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl)
- [libzhl/functions/ModManager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ModManager.zhl)
- [libzhl/functions/RNG.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RNG.zhl)
- [libzhl/functions/WeightedOutcomePicker.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/WeightedOutcomePicker.zhl)
- [libzhl/functions/WeightedOutcomePicker\_Outcome.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/WeightedOutcomePicker_Outcome.zhl)
- [loader/loader.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/loader.cpp)
- [logger/logger.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/logger/logger.cpp)
- [repentogon/LuaInterfaces/LuaCamera.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaCamera.cpp)
- [repentogon/LuaInterfaces/LuaCapsule.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaCapsule.cpp)
- [repentogon/LuaInterfaces/LuaIsaac.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp)
- [repentogon/LuaInterfaces/LuaWeightedOutcomePicker.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaWeightedOutcomePicker.cpp)
- [repentogon/Patches/ASMPatches/ASMCamera.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCamera.cpp)
- [repentogon/Patches/ASMPatches/ASMCamera.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCamera.h)

This page documents the miscellaneous Lua utility APIs provided by REPENTOGON. These include extensions to the global `Isaac` namespace, mathematical and collision utilities like `Capsule`, random number generation via `RNG`, and specialized data structures like `WeightedOutcomePicker`.

## Isaac Global Functions

REPENTOGON extends the global `Isaac` table with several high-performance utility functions and fixes for vanilla API limitations.

### Entity Query Fixes

REPENTOGON provides optimized versions of entity search functions that bypass certain vanilla limitations and provide more filtering options.

| Function | Description |
| --- | --- |
| `Isaac.FindByType` | A fixed version of the vanilla function that includes options for caching and ignoring friendly entities. [repentogon/LuaInterfaces/LuaIsaac.cpp32-65](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L32-L65) |
| `Isaac.GetRoomEntities` | Returns a table of all entities currently in the room using the internal `EntityList`. [repentogon/LuaInterfaces/LuaIsaac.cpp68-89](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L68-L89) |
| `Isaac.FindInRadius` | Finds entities within a specific radius of a position, filtered by partition. [repentogon/LuaInterfaces/LuaIsaac.cpp98-144](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L98-L144) |

### Game Management

Functions for controlling the game lifecycle and state.

- **`Isaac.StartNewGame`**: Starts a new run with specified parameters.
  - `playerType`: The ID of the character.
  - `challenge`: Challenge ID (0 for none).
  - `difficulty`: Difficulty level.
  - `seed`: Optional seed (integer or `Seeds` object).
  - Sources: [repentogon/LuaInterfaces/LuaIsaac.cpp196-214](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L196-L214) [libzhl/functions/Manager.zhl40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L40-L40)
- **`Isaac.CreateTimer`**: Spawns a non-rendering `Entity_Effect` that executes a Lua callback after a specified delay.
  - Supports persistence across room transitions and multiple executions.
  - Sources: [repentogon/LuaInterfaces/LuaIsaac.cpp167-194](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L167-L194)

### Rendering Helpers

- **`Isaac.DrawLine`**: Renders a line between two vectors with custom colors and thickness. [repentogon/LuaInterfaces/LuaIsaac.cpp216-226](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaIsaac.cpp#L216-L226)
- **`Isaac.GetRenderPosition`**: Calculates the screen position for a world position, accounting for render scale. [libzhl/functions/Isaac.zhl47](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Isaac.zhl#L47-L47)

* * *

## RNG (Random Number Generator)

The `RNG` class provides access to the game's internal random number generation logic, allowing mods to maintain deterministic behavior synchronized with the game seed.

### RNG Class Structure

The `RNG` structure consists of a seed and three shift values used for the internal Xorshift algorithm. [libzhl/functions/RNG.zhl22-28](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RNG.zhl#L22-L28)

### Key Functions

| Function | Description |
| --- | --- |
| `SetSeed(seed, shiftIdx)` | Initializes the RNG with a specific seed and shift index. [libzhl/functions/RNG.zhl4-5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RNG.zhl#L4-L5) |
| `RandomInt(max)` | Returns a random integer between 0 and `max - 1`. [libzhl/functions/RNG.zhl7-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RNG.zhl#L7-L8) |
| `RandomFloat()` | Returns a random float between 0.0 and 1.0. [libzhl/functions/RNG.zhl10-11](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RNG.zhl#L10-L11) |
| `Next()` | Advances the RNG state and returns the next raw value. [libzhl/functions/RNG.zhl13-14](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/RNG.zhl#L13-L14) |

* * *

## Capsule

The `Capsule` class represents a 2D capsule shape (a cylinder in 2D) used for advanced collision detection. It is particularly useful for detecting hits against non-circular areas, such as laser beams or elongated enemy hitboxes.

### Capsule Implementation Data Flow

The following diagram illustrates how `Capsule` objects are generated from entities and used in collision checks.

**Capsule Entity Interaction**

```
Code Entities

Capsule Logic

Entity Interface

Maps to

Implemented in

Calls

Entity:GetCollisionCapsule(offset)

Internal Capsule

Entity:GetNullCapsule(nullName)

Capsule:Collide(otherCapsule, hitPos)

Capsule:GetDirection()

Capsule:GetStartPoint()

struct Capsule

Lua_EntityGetCollisionCapsule

Capsule::Collide
```

Sources: [repentogon/LuaInterfaces/LuaCapsule.cpp22-47](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaCapsule.cpp#L22-L47) [libzhl/functions/Capsule.zhl10-29](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Capsule.zhl#L10-L29)

### Constructors

1. **Standard**: `Capsule(Position, SizeMult, Rotation, Size)` \- Creates a capsule based on a center point and orientation. [libzhl/functions/Capsule.zhl2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Capsule.zhl#L2-L2)
2. **Point-to-Point**: `Capsule(Position, TargetPosition, Size)` \- Creates a capsule stretching between two specific points. [libzhl/functions/Capsule.zhl5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Capsule.zhl#L5-L5)

* * *

## Camera

The `Camera` class manages the game's viewport. REPENTOGON exposes the ability to override camera behavior, allowing for cinematic effects or custom room tracking.

### Camera State Management

The camera is owned by the `Manager` and tracks a specific `Room` object. [libzhl/functions/Camera.zhl1-3](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Camera.zhl#L1-L3)

| Function | Description |
| --- | --- |
| `SetFocusPosition(pos)` | Sets the target position the camera should attempt to center on. [libzhl/functions/Camera.zhl4-5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Camera.zhl#L4-L5) |
| `SnapToPosition(pos)` | Instantly moves the camera to the target position without smoothing. [libzhl/functions/Camera.zhl13-14](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Camera.zhl#L13-L14) |
| `IsPosVisible(pos)` | Returns true if the given world position is within the current camera frustum. [libzhl/functions/Camera.zhl7-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Camera.zhl#L7-L8) |
| `ClampedToRoom(pos)` | Returns a vector clamped to the camera's valid bounds within the room. [libzhl/functions/Camera.zhl17-18](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Camera.zhl#L17-L18) |

Sources: [libzhl/functions/Camera.zhl31-42](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Camera.zhl#L31-L42) [libzhl/functions/Manager.zhl103-138](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L103-L138)

* * *

## WeightedOutcomePicker

`WeightedOutcomePicker` is a utility class for handling random selection based on weights (e.g., loot tables).

### Logic Flow

```

WeightedOutcomePicker:Add(Value, Weight)

Internal Outcome List

WeightedOutcomePicker:Pick(RNG)

Selected Value
```

- **Add**: Adds an entry with a specific weight. [repentogon/LuaInterfaces/LuaWeightedOutcomePicker.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaWeightedOutcomePicker.cpp)
- **Pick**: Uses a provided `RNG` object to select an outcome based on the relative weights of all added entries.

* * *

## Font

The `Font` API allows for loading and rendering text using the game's `.fnt` (AngelCode BMFont) format.

### Font Management

The `Manager` class pre-loads several system fonts (e.g., `TeamMeatEx10`, `Upheaval`, `Terminus`) which are accessible via the internal `Font` struct. [libzhl/functions/Manager.zhl120-128](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Manager.zhl#L120-L128)

### Key Functions

- **`Load(path)`**: Loads a font file from the filesystem. [libzhl/functions/Font.zhl2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Font.zhl#L2-L2)
- **`DrawString(str, pos, scale, color, settings)`**: Renders text to the screen. [libzhl/functions/Font.zhl4-5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Font.zhl#L4-L5)
- **`GetStringWidth(str)`**: Returns the pixel width of a string given the font's current configuration. [libzhl/functions/Font.zhl8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Font.zhl#L8-L8)

Sources: [libzhl/functions/Font.zhl12-45](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Font.zhl#L12-L45) [libzhl/functions/FontSettings.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/FontSettings.zhl)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#utility-apis)
- [Isaac Global Functions](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#isaac-global-functions)
- [Entity Query Fixes](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#entity-query-fixes)
- [Game Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#game-management)
- [Rendering Helpers](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#rendering-helpers)
- [RNG (Random Number Generator)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#rng-random-number-generator)
- [RNG Class Structure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#rng-class-structure)
- [Key Functions](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#key-functions)
- [Capsule](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#capsule)
- [Capsule Implementation Data Flow](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#capsule-implementation-data-flow)
- [Constructors](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#constructors)
- [Camera](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#camera)
- [Camera State Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#camera-state-management)
- [WeightedOutcomePicker](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#weightedoutcomepicker)
- [Logic Flow](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#logic-flow)
- [Font](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#font)
- [Font Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#font-management)
- [Key Functions](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis#key-functions-1)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 4.5 Achievement And Challenge System

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Achievement and Challenge System

Relevant source files

- [libzhl/functions/GameOver.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/GameOver.zhl)
- [libzhl/functions/Input.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Input.zhl)
- [libzhl/functions/ItemOverlay.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemOverlay.zhl)
- [libzhl/functions/PersistentGameData.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/PersistentGameData.zhl)
- [libzhl/functions/Seeds.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Seeds.zhl)
- [repentogon/LuaInterfaces/GridEntities/LuaGridEntity.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/GridEntities/LuaGridEntity.cpp)
- [repentogon/LuaInterfaces/LuaInput.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaInput.cpp)
- [repentogon/LuaInterfaces/LuaPersistentGameData.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaPersistentGameData.cpp)
- [repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp)
- [repentogon/Patches/ASMPatches/ASMMenu.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMMenu.cpp)
- [repentogon/Patches/AchievementsStuff.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp)
- [repentogon/Patches/AchievementsStuff.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.h)
- [repentogon/Patches/ChallengesStuff.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp)
- [repentogon/Patches/CompletionTracker.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CompletionTracker.cpp)
- [repentogon/Patches/MainMenuBlock.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MainMenuBlock.cpp)
- [repentogon/Patches/MainMenuBlock.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MainMenuBlock.h)
- [repentogon/Patches/ModsMenuStuff.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ModsMenuStuff.cpp)
- [repentogon/Patches/ModsMenuStuff.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ModsMenuStuff.h)
- [repentogon/Patches/NullItemsAndCostumes.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NullItemsAndCostumes.cpp)
- [repentogon/Patches/XMLData.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLData.cpp)
- [repentogon/Patches/XMLData.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLData.h)
- [repentogon/resources-repentogon/gfx/ui/modsmenupentogon.anm2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/modsmenupentogon.anm2)
- [repentogon/resources-repentogon/gfx/ui/modsmenuundo.png](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/modsmenuundo.png)

REPENTOGON provides a comprehensive system for creating and managing custom achievements and challenges that extend beyond the base game's limitations. This system allows mods to define XML-based achievements and challenges with complex unlock conditions, custom graphics, and progression tracking.

For information about the underlying XML data system that powers achievement definitions, see [XML Data System](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/XML%20Data%20System) For details about completion tracking integration with player statistics, see [Custom Cache System](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Custom%20Cache%20System)

## Architecture Overview

The achievement and challenge system consists of three primary components working together to provide a complete modding framework:

```
UI Layer

Persistence Layer

Core Processing Layer

XML Definition Layer

XMLStuff.AchievementData
Achievement Definitions

XMLStuff.ChallengeData
Challenge Definitions

XMLStuff.PlayerData
Character Unlock Requirements

AchievementsStuff.cpp
Achievement Logic

ChallengesStuff.cpp
Challenge Logic

CompletionTracker.cpp
Completion Events

JSON Save Files
Per-Slot Achievement Data

PersistentGameData
Vanilla Integration

AchievementOverlay
Custom Notifications

Menu_Stats
Secrets Screen

Menu_CustomChallenge
Challenge Selection
```

Sources: [repentogon/Patches/AchievementsStuff.cpp41-48](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L41-L48) [repentogon/Patches/ChallengesStuff.cpp41-43](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L41-L43) [repentogon/Patches/CompletionTracker.cpp30-46](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CompletionTracker.cpp#L30-L46) [repentogon/Patches/XMLData.cpp95-157](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLData.cpp#L95-L157)

## Achievement System

### Core Achievement Management

The achievement system extends the vanilla game's achievement handling to support unlimited custom achievements with IDs starting at 641. Custom achievements are managed separately from vanilla achievements using JSON persistence and XML definitions.

```
Custom Processing

Achievement Flow

No

Yes

PersistentGameData::TryUnlock
Achievement Trigger

ID >= 641?

super(achievementID)
Vanilla Processing

Custom Achievement
Processing

XMLStuff.AchievementData
GetNodeById()

Achievements Map
Update State

SaveAchieveemntsToJson()
Persist Data

Achievement Overlay
Display System
```

The achievement state is tracked using a string-based key system combining achievement name and source ID in the `Achievements` map:

| Achievement State | Meaning |
| --- | --- |
| `< 1` | In progress |
| `1` | Accomplished but not notified |
| `2` | Accomplished and notified |

Sources: [repentogon/Patches/AchievementsStuff.cpp42](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L42-L42) [repentogon/Patches/AchievementsStuff.cpp105-163](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L105-L163) [repentogon/Patches/AchievementsStuff.cpp63-78](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L63-L78)

### Achievement Listeners and Tracking

REPENTOGON provides multiple listener systems for tracking achievement progress based on game events. These listeners are initialized in `InitAchievs()` and checked during various game triggers.

```
Tracking Functions

Listener Systems

Event Sources

Player Actions
Item Use, Damage

Boss Deaths
Character-Specific

Completion Marks
Character + Boss

Event Counters
Statistical Tracking

CompletionMarkListeners
unordered_map

EventCounterListeners
unordered_map

BossDeathListeners
unordered_map

AchievementListeners
unordered_map

RunTrackersForCompletionMark()

RunTrackersForEventCounter()

RunTrackersForAchievementCounter()
```

Sources: [repentogon/Patches/AchievementsStuff.cpp41-47](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L41-L47) [repentogon/Patches/CompletionTracker.cpp94-96](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CompletionTracker.cpp#L94-L96)

### Achievement Display System

Custom achievements use a sophisticated display system that hijacks vanilla achievement notifications. When a custom achievement is unlocked, REPENTOGON triggers a "dummy" vanilla achievement unlock to start the overlay animation, then swaps the spritesheet in `ReplaceAchievementSprite`.

```
Graphics Components

Display Process

Achievement Unlocked

Dummy Achievement
System

AchievementOverlay::Update
Hook

ReplaceAchievementSprite()

Custom Achievement
Graphics Display

gfxback
Background Sprite

gfx
Achievement Icon

achievement_locked.png
Locked State
```

Sources: [repentogon/Patches/AchievementsStuff.cpp132-154](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L132-L154) [repentogon/Patches/AchievementsStuff.cpp173-203](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L173-L203) [repentogon/Patches/AchievementsStuff.cpp205-220](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.cpp#L205-L220)

## Challenge System

### Challenge Definition and Management

Custom challenges extend the vanilla challenge system starting from ID 46. They are defined in `challenges.xml` and tracked via `ChallengesStuff.cpp`.

```
Challenge Execution

Challenge Selection

Challenge Flow

Menu_CustomChallenge

visiblechallenges vector
Filtered Challenge List

XMLStuff.ChallengeData
Challenge XML Data

lockedchallenges map
Achievement Requirements

Menu_CustomChallenge::Update()

Filter Locked Challenges

boundselchal()
Constrain Selection

skiplocked()
Navigation Logic

Manager::StartNewGame()

Custom Challenge ID

New Game with
Challenge Parameters
```

Sources: [repentogon/Patches/ChallengesStuff.cpp107-119](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L107-L119) [repentogon/Patches/ChallengesStuff.cpp191-214](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L191-L214) [repentogon/Patches/ChallengesStuff.cpp226-245](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L226-L245)

### Challenge Completion and Rewards

When a challenge is completed, the system checks if it is a vanilla or custom challenge. Custom challenge completion is persisted to a JSON file named `challenges[saveslot].json`.

Sources: [repentogon/Patches/ChallengesStuff.cpp44-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L44-L58) [repentogon/Patches/ChallengesStuff.cpp90-98](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L90-L98)

## Completion Tracking Integration

### Character Completion Mapping

REPENTOGON maps completion marks to specific event counters. This allows modded characters to have their own completion marks tracked via the same internal logic as vanilla characters.

| Completion Type | Render Constant |
| --- | --- |
| Mom's Heart | `MOMS_HEART` |
| Isaac | `ISAAC` |
| Satan | `SATAN` |
| Boss Rush | `BOSS_RUSH` |
| Blue Baby | `BLUE_BABY` |
| The Lamb | `LAMB` |
| Mega Satan | `MEGA_SATAN` |
| Ultra Greed | `ULTRA_GREED` |
| Hush | `HUSH` |
| Delirium | `DELIRIUM` |
| Mother | `MOTHER` |
| The Beast | `BEAST` |

Sources: [repentogon/Patches/CompletionTracker.cpp32-46](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CompletionTracker.cpp#L32-L46) [repentogon/Patches/CompletionTracker.cpp110-124](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/CompletionTracker.cpp#L110-L124)

### Event Counter Integration

The achievement system integrates with Isaac's `PersistentGameData::IncreaseEventCounter` system. REPENTOGON provides a `simplifiedeventsenum` to map human-readable strings to internal event IDs.

| Event Category | Examples |
| --- | --- |
| Kill Tracking | `MOM_KILLS`, `ISAAC_KILLS`, `SATAN_KILLS` |
| Statistical | `ROCKS_DESTROYED`, `POOP_DESTROYED`, `PILLS_EATEN` |
| Interaction | `ARCADES_ENTERED`, `SHOPKEEPER_KILLED`, `ANGEL_DEALS_TAKEN` |
| Meta-game | `DEATHS`, `EDEN_TOKENS`, `STREAK_COUNTER` |

Sources: [repentogon/Patches/AchievementsStuff.h27-100](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/AchievementsStuff.h#L27-L100) [libzhl/functions/PersistentGameData.zhl4-5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/PersistentGameData.zhl#L4-L5)

## Lua API Integration

Mods can interact with the achievement and challenge systems through the `PersistentGameData` class exposed to Lua.

| Function | Description |
| --- | --- |
| `Unlock(id, skipOverlay)` | Forces an achievement unlock, optionally skipping the popup. |
| `Unlocked(id)` | Returns true if the achievement is unlocked. |
| `IncreaseEventCounter(id, num)` | Increases a specific event counter. |
| `IsChallengeCompleted(id)` | Checks completion for both vanilla and custom challenges. |
| `GetBestiaryKillCount(type, variant)` | Retrieves kill statistics for a specific entity. |

Sources: [repentogon/LuaInterfaces/LuaPersistentGameData.cpp183-204](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaPersistentGameData.cpp#L183-L204) [repentogon/LuaInterfaces/LuaPersistentGameData.cpp20-54](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaPersistentGameData.cpp#L20-L54) [repentogon/LuaInterfaces/LuaPersistentGameData.cpp107-120](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaPersistentGameData.cpp#L107-L120)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#achievement-and-challenge-system)
- [Architecture Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#architecture-overview)
- [Achievement System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#achievement-system)
- [Core Achievement Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#core-achievement-management)
- [Achievement Listeners and Tracking](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#achievement-listeners-and-tracking)
- [Achievement Display System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#achievement-display-system)
- [Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#challenge-system)
- [Challenge Definition and Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#challenge-definition-and-management)
- [Challenge Completion and Rewards](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#challenge-completion-and-rewards)
- [Completion Tracking Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#completion-tracking-integration)
- [Character Completion Mapping](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#character-completion-mapping)
- [Event Counter Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#event-counter-integration)
- [Lua API Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system#lua-api-integration)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 4.6 Save State And Persistence

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Save State and Persistence

Relevant source files

- [libzhl/functions/EntitySaveState.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntitySaveState.zhl)
- [libzhl/functions/GameStateIO.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/GameStateIO.zhl)
- [libzhl/functions/KAGE.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE.zhl)
- [libzhl/functions/KAGE\_Filesys\_File.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Filesys_File.zhl)
- [libzhl/functions/KAGE\_Filesys\_FileStream.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Filesys_FileStream.zhl)
- [libzhl/functions/KAGE\_Filesys\_IFile.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/KAGE_Filesys_IFile.zhl)
- [libzhl/functions/SteamCloudFile.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/SteamCloudFile.zhl)
- [repentogon/LuaInit.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInit.cpp)
- [repentogon/LuaInterfaces/LuaEntitySaveState.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaEntitySaveState.cpp)
- [repentogon/LuaInterfaces/LuaEntitySaveState.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaEntitySaveState.h)
- [repentogon/LuaInterfaces/\_Internals.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/_Internals.cpp)
- [repentogon/LuaInterfaces/\_Internals.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/_Internals.h)
- [repentogon/Patches/ExtraRenderSteps.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraRenderSteps.h)
- [repentogon/Patches/GameStateManagement.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/GameStateManagement.cpp)
- [repentogon/Patches/ItemPoolManager.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.cpp)
- [repentogon/Patches/ItemPoolManager.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ItemPoolManager.h)
- [repentogon/SaveStateManagement/EntitySaveStateManagement.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.cpp)
- [repentogon/SaveStateManagement/EntitySaveStateManagement.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.h)
- [repentogon/SaveSyncing/SaveFile.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveFile.cpp)
- [repentogon/SaveSyncing/SaveFile.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveFile.h)
- [repentogon/SaveSyncing/SaveSyncing.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.cpp)
- [repentogon/SaveSyncing/SaveSyncing.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.h)
- [repentogon/Utils/EntitySaveStateUtils.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Utils/EntitySaveStateUtils.h)
- [repentogon/resources/scripts/repentogon\_extras/\_emmy\_lua.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/_emmy_lua.lua)
- [repentogon/resources/scripts/repentogon\_extras/entity\_save\_state\_manager.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/entity_save_state_manager.lua)
- [repentogon/resources/scripts/repentogon\_extras/mod\_manager.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/mod_manager.lua)

REPENTOGON implements a robust system for managing entity save states, persistent mod data, and synchronization between vanilla and custom save files. This system extends the base game's `EntitySaveState` and `GameState` structures to allow for deeper modding capabilities while maintaining data integrity across game versions.

## Entity Save State Management (ESSM)

The Entity Save State Management (ESSM) system is designed to extend vanilla save state structures (`EntitySaveState`, `GameStatePlayer`, and `FamiliarData`) without breaking compatibility. Since these structures have fixed sizes, REPENTOGON "hijacks" specific low-risk fields to store a unique ID that correlates to extended data managed by the framework.

### Hijacking Mechanism

To store custom data, the system replaces specific fields in vanilla structures with a unique ID and a "Hijacked Marker" [repentogon/SaveStateManagement/EntitySaveStateManagement.cpp4-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.cpp#L4-L8).

| Structure | Hijacked Field 1 (ID) | Hijacked Field 2 (Marker) |
| --- | --- | --- |
| `EntitySaveState` | `gridSpawnIdx` | `_intStorage7` |
| `GameStatePlayer` | `immaculateConceptionState` | `cambionConceptionState` |
| `FamiliarData` | `state` | `roomClearCount` |

**Sources:** [repentogon/SaveStateManagement/EntitySaveStateManagement.cpp4-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.cpp#L4-L8), [libzhl/functions/EntitySaveState.zhl16-21](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntitySaveState.zhl#L16-L21).

### Core Operations

The ESSM lifecycle ensures that hijacked values are transparently managed during game operations:

1. **Hijacking/Storing:** Generates a new ID and copies original field values into a side-buffer before replacing them in the structure [repentogon/SaveStateManagement/EntitySaveStateManagement.cpp11-13](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.cpp#L11-L13).
2. **Restoring:** Temporarily replaces the ID/Marker with original values before calling the vanilla `Restore` function, then restores the ID/Marker for continued tracking [repentogon/SaveStateManagement/EntitySaveStateManagement.cpp14](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.cpp#L14-L14).
3. **Serialization:** During `GameState::write`, local IDs are generated for the serialization process, tying vanilla structures to REPENTOGON's sidecar save files [repentogon/SaveStateManagement/EntitySaveStateManagement.cpp20-21](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.cpp#L20-L21).

**Sources:** [repentogon/SaveStateManagement/EntitySaveStateManagement.cpp10-25](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveStateManagement/EntitySaveStateManagement.cpp#L10-L25), [repentogon/Patches/GameStateManagement.cpp217-222](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/GameStateManagement.cpp#L217-L222).

## Data Flow: Persistence and Serialization

The persistence system hooks into the game's native save/load routines to ensure that REPENTOGON-specific data (like extended item pools and entity states) is written to disk alongside vanilla data.

### Game State Hook Points

REPENTOGON monitors the `GameStateSlot` to determine if data belongs to a standard save file or a temporary state like the Glowing Hourglass [repentogon/Patches/GameStateManagement.cpp23-27](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/GameStateManagement.cpp#L23-L27).

```
Code Entity Space

Natural Language Space

User Saves Game

User Loads Game

Hook: GameState::write

Hook: GameState::read

ESSM::detail::SaveData::Serialize

ESSM::detail::SaveData::Deserialize

ItemPoolManager::__SaveToDisk

VirtualRoomSetManager::__WriteSave

ItemPoolManager::__LoadFromDisk
```

**Sources:** [repentogon/Patches/GameStateManagement.cpp16-27](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/GameStateManagement.cpp#L16-L27), [repentogon/Patches/GameStateManagement.cpp217-242](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/GameStateManagement.cpp#L217-L242), [repentogon/Patches/GameStateManagement.cpp261-285](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/GameStateManagement.cpp#L261-L285).

## Lua Persistence API

REPENTOGON provides a Lua-facing manager for persistent entity data. This allows mods to attach arbitrary tables to entities that persist through room transitions and game restarts by leveraging the ESSM ID system.

### Entity Save State Manager (Lua)

The internal script `entity_save_state_manager.lua` manages the mapping between entity pointers and their corresponding save state IDs.

- **`_OnStoreEntity(entityId, saveStateId)`**: Deep copies a mod's data from the active entity table to the save state table when an entity is stored by the game [repentogon/resources/scripts/repentogon\_extras/entity\_save\_state\_manager.lua180-187](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/entity_save_state_manager.lua#L180-L187).
- **`_OnRestoreEntity(entityId, saveStateId)`**: Restores the table back to the active entity when the game restores an entity from a save state [repentogon/resources/scripts/repentogon\_extras/entity\_save\_state\_manager.lua191-200](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/entity_save_state_manager.lua#L191-L200).

**Sources:** [repentogon/resources/scripts/repentogon\_extras/entity\_save\_state\_manager.lua156-225](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/entity_save_state_manager.lua#L156-L225).

## Save Syncing and Versioning

REPENTOGON uses separate save files (`rgon_persistentgamedata.dat`) to prevent corruption of vanilla saves during game updates.

### Synchronization Logic

The `SaveSyncing` namespace handles the migration and merging of progress between different game versions and REPENTOGON's custom format.

| Mode | Behavior |
| --- | --- |
| `SAVE_SYNC_TAKE_MAX` | Merges two saves by taking the highest value for counters and achievements [repentogon/SaveSyncing/SaveSyncing.h70-74](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.h#L70-L74). |
| `SyncStatus` | Tracks checksums of the last successful sync to detect out-of-sync states [repentogon/SaveSyncing/SaveSyncing.h19-48](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.h#L19-L48). |

### Save Path Redirection

REPENTOGON applies ASM patches to the game's file system calls to redirect save operations to the `Repentogon/` subdirectory [repentogon/SaveSyncing/SaveSyncing.cpp52-59](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.cpp#L52-L59).

```
REPENTOGON Redirection

Vanilla Logic

ASM Patch

Merges with

Triggered on

persistentgamedata1.dat

Repentogon/rgon_persistentgamedata1.dat

SaveSyncing::PerformVanillaSaveSynchronization

Game Startup
```

**Sources:** [repentogon/SaveSyncing/SaveSyncing.cpp52-59](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.cpp#L52-L59), [repentogon/SaveSyncing/SaveSyncing.cpp165-166](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.cpp#L165-L166), [repentogon/SaveSyncing/SaveSyncing.h76-79](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/SaveSyncing.h#L76-L79).

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#save-state-and-persistence)
- [Entity Save State Management (ESSM)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#entity-save-state-management-essm)
- [Hijacking Mechanism](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#hijacking-mechanism)
- [Core Operations](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#core-operations)
- [Data Flow: Persistence and Serialization](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#data-flow-persistence-and-serialization)
- [Game State Hook Points](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#game-state-hook-points)
- [Lua Persistence API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#lua-persistence-api)
- [Entity Save State Manager (Lua)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#entity-save-state-manager-lua)
- [Save Syncing and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#save-syncing-and-versioning)
- [Synchronization Logic](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#synchronization-logic)
- [Save Path Redirection](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence#save-path-redirection)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 4.7 Menu System

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Menu System

Relevant source files

- [libzhl/functions/AchievementOverlay.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/AchievementOverlay.zhl)
- [libzhl/functions/ColorModState.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ColorModState.zhl)
- [libzhl/functions/CompletionWidget.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/CompletionWidget.zhl)
- [libzhl/functions/GameOver.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/GameOver.zhl)
- [libzhl/functions/Input.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Input.zhl)
- [libzhl/functions/MenuCharacter.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuCharacter.zhl)
- [libzhl/functions/MenuDailyChallenge.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuDailyChallenge.zhl)
- [libzhl/functions/MenuGame.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuGame.zhl)
- [libzhl/functions/MenuManager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuManager.zhl)
- [libzhl/functions/MenuMods.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuMods.zhl)
- [libzhl/functions/MenuOptions.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuOptions.zhl)
- [libzhl/functions/MenuSave.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuSave.zhl)
- [libzhl/functions/MenuSpecialSeeds.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuSpecialSeeds.zhl)
- [libzhl/functions/MenuStats.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuStats.zhl)
- [libzhl/functions/MenuTitle.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuTitle.zhl)
- [repentogon/LuaInterfaces/GridEntities/LuaGridEntity.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/GridEntities/LuaGridEntity.cpp)
- [repentogon/LuaInterfaces/LuaInput.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaInput.cpp)
- [repentogon/LuaInterfaces/Menus/LuaCharacterMenu.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaCharacterMenu.cpp)
- [repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp)
- [repentogon/LuaInterfaces/Menus/LuaSaveMenu.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaSaveMenu.cpp)
- [repentogon/Patches/ASMPatches/ASMMenu.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMMenu.cpp)
- [repentogon/Patches/ChallengesStuff.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp)
- [repentogon/Patches/MainMenuBlock.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MainMenuBlock.cpp)
- [repentogon/Patches/MainMenuBlock.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MainMenuBlock.h)
- [repentogon/Patches/ModsMenuStuff.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ModsMenuStuff.cpp)
- [repentogon/Patches/ModsMenuStuff.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ModsMenuStuff.h)
- [repentogon/resources-repentogon/gfx/ui/modsmenupentogon.anm2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/modsmenupentogon.anm2)
- [repentogon/resources-repentogon/gfx/ui/modsmenuundo.png](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/modsmenuundo.png)

The REPENTOGON menu system provides deep integration into the game's native UI management. It exposes the `MenuManager` and its constituent sub-menus (Character, Save, Mods, etc.) to Lua, allowing for real-time manipulation of menu states, sprites, and color modifiers. Additionally, REPENTOGON implements several quality-of-life patches to the vanilla menus, such as a searchable Mods menu and improved challenge navigation.

## MenuManager Architecture

The `MenuManager` is the central hub for all UI states outside of active gameplay. It manages the transitions, background rendering, and the lifecycle of specific sub-menu objects.

### Core Structure

The `MenuManager` contains instances of every major menu type used by the game. Each sub-menu (e.g., `Menu_Title`, `Menu_Save`) is stored at a fixed offset within the `MenuManager` structure.

| Field | Offset | Type | Description |
| --- | --- | --- | --- |
| `_state` | `0xc` | `int` | The current active menu state. |
| `_selectedMenuID` | `0x40` | `int` | The ID of the currently active menu. |
| `_ViewPosition` | `0x44` | `Vector` | The current camera/view offset for the menu. |
| `_menuTitle` | `0x1d4` | `Menu_Title` | Logic for the title screen. |
| `_menuSave` | `0x2f8` | `Menu_Save` | Logic for the save file selection. |
| `_menuGame` | `0xb90` | `Menu_Game` | Logic for the Main Menu (New Game, Continue, etc.). |
| `_menuCharacter` | `0x1530` | `Menu_Character` | Logic for the character selection wheel. |
| `_menuMods` | `0xd92c` | `Menu_Mods` | Logic for the mod list. |

**Sources:** [libzhl/functions/MenuManager.zhl27-100](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuManager.zhl#L27-L100)

### Color Modifiers

REPENTOGON exposes the internal color grading system used by the menus. This system uses `ColorModState` to interpolate between different color profiles (brightness, contrast, and RGBA tints) as the user navigates between menus.

- **`GetCurrentColorModifier()`**: Returns the currently active color state.
- **`GetTargetColorModifier()`**: Returns the state the menu is currently lerping toward.
- **`SetColorModifier(pColor, lerp, rate)`**: Allows Lua to manually trigger a color transition.

**Sources:** [libzhl/functions/ColorModState.zhl1-99](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ColorModState.zhl#L1-L99) [repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp101-170](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp#L101-L170)

## Sub-Menu Systems

### Character Selection (`Menu_Character`)

The character menu manages the rotating wheel of characters. REPENTOGON exposes the `ANM2` sprites for nearly every element of this UI, including portraits, completion marks, and the "Tainted" menu deco.

- **Completion Marks**: Managed via `CompletionWidget`, which contains its own `ANM2` instance [libzhl/functions/CompletionWidget.zhl9-16](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/CompletionWidget.zhl#L9-L16)
- **Page Swapping**: The transition between Normal and Tainted characters is handled by `DoPageSwap` [libzhl/functions/MenuCharacter.zhl24](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuCharacter.zhl#L24-L24)
- **Dynamic Entry Access**: The game uses a global array `g_MenuCharacterEntries` to determine which characters appear in the wheel [libzhl/functions/MenuCharacter.zhl104](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuCharacter.zhl#L104-L104)

**Sources:** [libzhl/functions/MenuCharacter.zhl29-92](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuCharacter.zhl#L29-L92) [repentogon/LuaInterfaces/Menus/LuaCharacterMenu.cpp6-144](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaCharacterMenu.cpp#L6-L144)

### Save Selection (`Menu_Save`)

The save menu handles the three save slots. REPENTOGON adds the ability to dynamically replace the "drawing" sprites on the save files via `SetSlotSpritesheet`.

- **Custom Graphics**: The `replace_slot_graphics` method is hooked to inject custom spritesheets based on the active save slot [repentogon/LuaInterfaces/Menus/LuaSaveMenu.cpp138-148](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaSaveMenu.cpp#L138-L148)

**Sources:** [libzhl/functions/MenuSave.zhl10-30](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuSave.zhl#L10-L30) [repentogon/LuaInterfaces/Menus/LuaSaveMenu.cpp5-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaSaveMenu.cpp#L5-L81)

## Menu Logic Flow

The following diagram illustrates the relationship between the global `MenuManager` and the specific sub-menu logic during the `Update` and `Render` cycles.

**Menu System Entity Relationship**

```
Sub-Menus

MenuManager (Class)

Global Scope

Uses

Patched by

g_MenuManager

g_MenuControllerIndex

MenuManager::Update()

MenuManager::Render()

_selectedMenuID

Menu_Character

Menu_Game

Menu_Save

Menu_Mods

CompletionWidget

ModsMenuStuff.cpp
```

**Sources:** [libzhl/functions/MenuManager.zhl1-20](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuManager.zhl#L1-L20) [libzhl/functions/MenuCharacter.zhl29-30](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuCharacter.zhl#L29-L30) [repentogon/Patches/ModsMenuStuff.cpp102-128](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ModsMenuStuff.cpp#L102-L128)

## REPENTOGON Enhancements

### Mods Menu Search and Filtering

REPENTOGON significantly overhauls `Menu_Mods` to improve usability for players with large mod lists.

- **Search Bar**: Pressing `Left Control` opens a search interface. This captures keyboard input and filters the mod list in real-time [repentogon/Patches/ModsMenuStuff.cpp36-46](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ModsMenuStuff.cpp#L36-L46)
- **Mass Toggle**: Implements functionality to undo changes or bulk-enable/disable mods.
- **Input Blocking**: When the search bar is active, standard menu navigation input is blocked to prevent the menu from scrolling while typing [repentogon/Patches/ModsMenuStuff.cpp130-135](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ModsMenuStuff.cpp#L130-L135)

### Custom Challenge Navigation

Vanilla Isaac has limited support for navigating large numbers of custom challenges. REPENTOGON patches `Menu_CustomChallenge` and `Menu_Challenge` to:

- **Smooth Scrolling**: Adds lerped Y-offsets to the challenge list for smoother visual transitions [repentogon/Patches/ChallengesStuff.cpp121-133](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L121-L133)
- **Visibility Logic**: Correctly handles hidden challenges and locks entries based on achievement requirements [repentogon/Patches/ChallengesStuff.cpp191-214](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ChallengesStuff.cpp#L191-L214)

### Input Masking

The `MainMenuInputBlock` system allows mods to disable specific menu actions (e.g., preventing the user from starting a game or entering the options menu). This is achieved by hooking `InputManager::IsActionTriggered` and checking against a bitmask [repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp191-206](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp#L191-L206)

## Data Mapping: Lua to Internal Structures

The following table maps Lua API concepts to the internal C++ classes and variables.

| System Name | Internal Entity | File Reference |
| --- | --- | --- |
| `MenuManager` | `MenuManager` | [libzhl/functions/MenuManager.zhl27](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuManager.zhl#L27-L27) |
| `Main Menu` | `Menu_Game` | [libzhl/functions/MenuGame.zhl16](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuGame.zhl#L16-L16) |
| `Character Menu` | `Menu_Character` | [libzhl/functions/MenuCharacter.zhl29](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuCharacter.zhl#L29-L29) |
| `Save Menu` | `Menu_Save` | [libzhl/functions/MenuSave.zhl10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuSave.zhl#L10-L10) |
| `Title Screen` | `Menu_Title` | [libzhl/functions/MenuTitle.zhl7](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuTitle.zhl#L7-L7) |
| `Mod Menu` | `Menu_Mods` | [libzhl/functions/MenuMods.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuMods.zhl) |
| `Completion Marks` | `CompletionWidget` | [libzhl/functions/CompletionWidget.zhl9](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/CompletionWidget.zhl#L9-L9) |

**Sources:** [libzhl/functions/MenuManager.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuManager.zhl) [libzhl/functions/MenuCharacter.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuCharacter.zhl) [libzhl/functions/MenuSave.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuSave.zhl)

## Technical Implementation: World to Menu Translation

Because the menu uses a different coordinate system than the game world (and varies based on which sub-menu is active), REPENTOGON provides `WorldToMenuPosition`. This function calculates the offset by referencing `_viewPositionSet`, an array of 23 vectors stored in `MenuManager` that defines the camera anchor for every menu state.

**Sources:** [repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp7-35](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/Menus/LuaMenuManager.cpp#L7-L35) [libzhl/functions/MenuManager.zhl92](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuManager.zhl#L92-L92)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#menu-system)
- [MenuManager Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#menumanager-architecture)
- [Core Structure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#core-structure)
- [Color Modifiers](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#color-modifiers)
- [Sub-Menu Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#sub-menu-systems)
- [Character Selection (\`Menu\_Character\`)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#character-selection-menu_character)
- [Save Selection (\`Menu\_Save\`)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#save-selection-menu_save)
- [Menu Logic Flow](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#menu-logic-flow)
- [REPENTOGON Enhancements](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#repentogon-enhancements)
- [Mods Menu Search and Filtering](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#mods-menu-search-and-filtering)
- [Custom Challenge Navigation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#custom-challenge-navigation)
- [Input Masking](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#input-masking)
- [Data Mapping: Lua to Internal Structures](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#data-mapping-lua-to-internal-structures)
- [Technical Implementation: World to Menu Translation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system#technical-implementation-world-to-menu-translation)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 5 Tools And Features

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Tools and Features

Relevant source files

- [.gitattributes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitattributes)
- [.github/workflows/release.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml)
- [appveyor.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml)
- [appveyor\_launcher.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml)
- [appveyor\_repentogon.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_repentogon.yml)
- [libzhl/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp)
- [libzhl/functions/Shape.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Shape.zhl)
- [loader/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/Version.cpp)
- [repentogon/ImGuiFeatures/ConsoleMega.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h)
- [repentogon/ImGuiFeatures/CustomImGui.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/CustomImGui.h)
- [repentogon/ImGuiFeatures/HelpMenu.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/HelpMenu.h)
- [repentogon/ImGuiFeatures/ImGui.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp)
- [repentogon/ImGuiFeatures/ImGuiEx.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGuiEx.h)
- [repentogon/ImGuiFeatures/LogViewer.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LogViewer.h)
- [repentogon/ImGuiFeatures/LuaImGui.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LuaImGui.cpp)
- [repentogon/ImGuiFeatures/NotificationHandler.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/NotificationHandler.h)
- [repentogon/ImGuiFeatures/PerformanceWindow.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/PerformanceWindow.h)
- [repentogon/ImGuiFeatures/SavedataHandler.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/SavedataHandler.h)
- [repentogon/ImGuiFeatures/UnifontSupport.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/UnifontSupport.h)
- [repentogon/Patches/ExtraDebugRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp)
- [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)
- [repentogon/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp)
- [repentogon/resources/scripts/repentogon\_tests/test\_imgui.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_tests/test_imgui.lua)
- [version.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt)

This document covers REPENTOGON's comprehensive suite of development and debugging tools designed to enhance the modding experience for The Binding of Isaac: Repentance. These tools provide real-time game state inspection, enhanced console functionality, configurable game options, and various quality-of-life improvements.

For information about the core modding APIs and Lua interfaces, see [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api). For details about XML data systems, see [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache).

## ImGui Debug Interface

REPENTOGON integrates Dear ImGui to provide a modern, interactive debug interface accessible during gameplay. The system is activated by pressing the grave key (\`) and provides a comprehensive suite of development tools.

```
Integration Points

ImGui Integration System

UI Components

Core Windows

ImGui_ImplOpenGL2_RenderDrawData
Main Rendering Loop

WindowBeginEx()
Custom Window Management

ConsoleMega
Enhanced Debug Console

LogViewer
Real-time Log Display

GameOptionsWindow
Settings Interface

PerformanceWindow
Performance Metrics

Main Menu Bar
Tool Navigation

NotificationHandler
Alert System

CustomImGui
Lua-driven UI

ImGui_ImplWin32_WndProcHandler
Input Handling

SaveSettings/LoadSettings
State Persistence
```

The ImGui system provides several key features:

- **Window Management**: Custom window handling via `WindowBeginEx` with pinning, scaling, and persistence [repentogon/ImGuiFeatures/ImGui.cpp143-158](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L143-L158)
- **Input Interception**: Seamless input routing between game and debug interface using `ImGui_ImplWin32_WndProcHandler` [repentogon/ImGuiFeatures/ImGui.cpp31-33](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L31-L33)
- **Multi-language Support**: Localization system managed by the `LANG` global object [repentogon/ImGuiFeatures/Lang.h1-10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Lang.h#L1-L10)
- **Font Rendering**: Support for `Unifont` and `FontAwesome6` for international character sets and icons [repentogon/ImGuiFeatures/UnifontSupport.h1-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/UnifontSupport.h#L1-L15) [repentogon/ImGuiFeatures/IconsFontAwesome6.h1-10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/IconsFontAwesome6.h#L1-L10)

For details, see [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration).

Sources: [repentogon/ImGuiFeatures/ImGui.cpp31-158](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L31-L158) [repentogon/ImGuiFeatures/ConsoleMega.h111-126](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L111-L126) [repentogon/ImGuiFeatures/CustomImGui.h20-55](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/CustomImGui.h#L20-L55)

## Enhanced Console System

The `ConsoleMega` class extends the vanilla debug console with advanced features including autocomplete, command history, and macro support.

### ConsoleMega Architecture

```
Autocomplete System

Input Handling

Command Processing

commands
std::set

autocompleteBuffer
std::vector

macros
std::vector

inputBuf[1024]
Command Input

ParseCommand
String Tokenization

RegisterMacro
Macro Definition

AutocompleteType enum
ENTITY, ITEM, STAGE, etc.

SI::natural::compare
Human-friendly sorting
```

### Key Console Features

- **Command Registration**: Commands are registered with metadata including aliases and autocomplete types [repentogon/ImGuiFeatures/ConsoleMega.h21-44](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L21-L44)
- **Macros**: Pre-defined sequences of commands (e.g., "beast", "hush", "ms") for rapid testing [repentogon/ImGuiFeatures/ConsoleMega.h173-184](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L173-L184)
- **Autocomplete**: Context-aware suggestions for entities, items, and stages [repentogon/ImGuiFeatures/ConsoleMega.h129-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L129-L150)

Sources: [repentogon/ImGuiFeatures/ConsoleMega.h21-184](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L21-L184) [repentogon/ImGuiFeatures/ConsoleMega.h46-83](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L46-L83)

## ASM Patches and Vanilla Tweaks

REPENTOGON includes numerous low-level patches that fix bugs and improve performance without breaking mod compatibility. These are managed through the `ASMPatcher` system [repentogon/ImGuiFeatures/ImGui.cpp1-2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L1-L2)

### Patching Examples

- **Exception Handling**: Improved crash reporting via `NewExceptionHandler` [repentogon/Patches/NewExceptionHandler.cpp1-10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp#L1-L10)
- **Virtual Rooms**: Management of custom room sets for modded content [repentogon/Patches/VirtualRoomSets.h1-10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VirtualRoomSets.h#L1-L10)
- **Debug Rendering**: Enhanced visual debugging tools [repentogon/Patches/ExtraDebugRender.cpp1-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp#L1-L15)

For details, see [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks).

Sources: [repentogon/ImGuiFeatures/ImGui.cpp1-13](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L1-L13) [repentogon/Patches/XMLData.h1-10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLData.h#L1-L10)

## Developer Tools

REPENTOGON provides several developer-facing tools to assist in the creation and debugging of mods.

### Performance and Logging

- **Log Viewer**: Real-time capture of `[GAME]`, `[REPENTOGON]`, and `[CONSOLE]` logs with filtering and autoscroll [repentogon/ImGuiFeatures/LogViewer.h27-50](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LogViewer.h#L27-L50)
- **Performance Window**: Real-time tracking of Lua memory usage (totalbytes + GCdebt) and frame time metrics [repentogon/ImGuiFeatures/PerformanceWindow.h10-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/PerformanceWindow.h#L10-L58)

### Build and CI Tools

- **AppVeyor Integration**: Automated build scripts for the main DLL and the launcher [appveyor.yml1-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L1-L58) [appveyor\_launcher.yml1-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml#L1-L38)
- **GitHub Actions**: Release workflows for generating changelogs and uploading artifacts [.github/workflows/release.yml1-74](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L1-L74)
- **Version Tracking**: Centralized version management via `version.txt` and `Version.h` [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1)

For details, see [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools).

Sources: [repentogon/ImGuiFeatures/LogViewer.h27-50](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LogViewer.h#L27-L50) [repentogon/ImGuiFeatures/PerformanceWindow.h10-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/PerformanceWindow.h#L10-L58) [appveyor.yml1-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L1-L58) [.github/workflows/release.yml1-74](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L1-L74)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#tools-and-features)
- [ImGui Debug Interface](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#imgui-debug-interface)
- [Enhanced Console System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#enhanced-console-system)
- [ConsoleMega Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#consolemega-architecture)
- [Key Console Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#key-console-features)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#asm-patches-and-vanilla-tweaks)
- [Patching Examples](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#patching-examples)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#developer-tools)
- [Performance and Logging](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#performance-and-logging)
- [Build and CI Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features#build-and-ci-tools)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 5.1 Imgui Integration

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# ImGui Integration

Relevant source files

- [libzhl/functions/OptionsConfig.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/OptionsConfig.zhl)
- [libzhl/functions/SoundEffects.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/SoundEffects.zhl)
- [repentogon/ImGuiFeatures/ConsoleMega.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h)
- [repentogon/ImGuiFeatures/CustomImGui.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/CustomImGui.h)
- [repentogon/ImGuiFeatures/GameOptions.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/GameOptions.h)
- [repentogon/ImGuiFeatures/HelpMenu.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/HelpMenu.h)
- [repentogon/ImGuiFeatures/ImGui.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp)
- [repentogon/ImGuiFeatures/ImGuiEx.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGuiEx.h)
- [repentogon/ImGuiFeatures/Lang.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Lang.cpp)
- [repentogon/ImGuiFeatures/Lang.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Lang.h)
- [repentogon/ImGuiFeatures/Localization/de.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/de.inl)
- [repentogon/ImGuiFeatures/Localization/en\_us.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/en_us.inl)
- [repentogon/ImGuiFeatures/Localization/es.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/es.inl)
- [repentogon/ImGuiFeatures/Localization/fr.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/fr.inl)
- [repentogon/ImGuiFeatures/Localization/jp.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/jp.inl)
- [repentogon/ImGuiFeatures/Localization/kr.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/kr.inl)
- [repentogon/ImGuiFeatures/Localization/ru.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/ru.inl)
- [repentogon/ImGuiFeatures/Localization/zh\_cn.inl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/zh_cn.inl)
- [repentogon/ImGuiFeatures/LogViewer.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LogViewer.h)
- [repentogon/ImGuiFeatures/LuaImGui.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LuaImGui.cpp)
- [repentogon/ImGuiFeatures/NotificationHandler.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/NotificationHandler.h)
- [repentogon/ImGuiFeatures/PerformanceWindow.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/PerformanceWindow.h)
- [repentogon/ImGuiFeatures/SavedataHandler.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/SavedataHandler.h)
- [repentogon/ImGuiFeatures/UnifontSupport.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/UnifontSupport.h)
- [repentogon/LuaInterfaces/LuaOptions.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaOptions.cpp)
- [repentogon/REPENTOGONOptions.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONOptions.cpp)
- [repentogon/REPENTOGONOptions.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONOptions.h)
- [repentogon/SaveSyncing/OptionsSyncing.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/SaveSyncing/OptionsSyncing.cpp)
- [repentogon/resources/scripts/repentogon\_tests/test\_imgui.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_tests/test_imgui.lua)
- [tools/cppToDocsChecker.py](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/cppToDocsChecker.py)

REPENTOGON's ImGui integration provides a comprehensive set of developer and debugging tools accessible through an overlay interface. This system replaces and enhances the vanilla debug console with a modern, feature-rich GUI framework that includes console improvements, game options management, performance monitoring, and various development utilities.

For information about the underlying Lua modding capabilities exposed through these tools, see [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api).

## Architecture Overview

The ImGui integration operates as an overlay system injected into Isaac's rendering pipeline. The implementation hooks into the game's window procedure and rendering loop to provide seamless access to debugging tools without disrupting gameplay.

Title: ImGui System Data Flow

```

Game Render Loop

RunImGui Hook

ImGui Core System

Window Procedure

windowProc_hook

ImGui Input Processing

Main Menu Bar

ConsoleMega

GameOptionsWindow

LogViewer

PerformanceWindow

CustomImGui Windows

REPENTOGONOptions

Font Management

Unicode Support

Lang System
```

**Sources:** [repentogon/ImGuiFeatures/ImGui.cpp686-702](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L686-L702) [repentogon/ImGuiFeatures/ImGui.cpp283-431](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L283-L431)

### Core Components

The system consists of several key components that work together to provide the complete debugging interface:

| Component | File | Purpose |
| --- | --- | --- |
| `RunImGui` | [repentogon/ImGuiFeatures/ImGui.cpp686-702](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L686-L702) | Main rendering and update loop |
| `ConsoleMega` | [repentogon/ImGuiFeatures/ConsoleMega.h111-190](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L111-L190) | Enhanced debug console |
| `GameOptionsWindow` | [repentogon/ImGuiFeatures/GameOptions.h19-23](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/GameOptions.h#L19-L23) | Game settings interface |
| `LogViewer` | [repentogon/ImGuiFeatures/LogViewer.h27-50](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LogViewer.h#L27-L50) | Log viewing utility |
| `PerformanceWindow` | [repentogon/ImGuiFeatures/PerformanceWindow.h1-20](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/PerformanceWindow.h#L1-L20) | Performance monitoring |
| `REPENTOGONOptions` | [repentogon/REPENTOGONOptions.h20-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONOptions.h#L20-L150) | Settings management |
| `CustomImGui` | [repentogon/ImGuiFeatures/CustomImGui.h200-210](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/CustomImGui.h#L200-L210) | Lua-driven custom window system |

**Sources:** [repentogon/ImGuiFeatures/ImGui.cpp43-50](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L43-L50)

## Injection and Initialization

### Rendering Hook

ImGui is injected into the game's rendering pipeline through an assembly patch that intercepts the swap buffer call in the Manager's render method:

Title: Rendering Pipeline Injection

```

Manager::Render

SwapBuffers Call

ASM Patch Injection

RunImGui Function

Original SwapBuffers

ImGui_ImplOpenGL2_NewFrame

Window Rendering

ImGui::Render
```

**Sources:** [repentogon/ImGuiFeatures/ImGui.cpp686-702](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L686-L702)

### Input Handling

Input is captured through a window procedure hook (`windowProc_hook`) that intercepts Windows messages before they reach the game. If `menuShown` is true, inputs are directed to ImGui and blocked from the game.

**Sources:** [repentogon/ImGuiFeatures/ImGui.cpp283-431](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ImGui.cpp#L283-L431)

## Console System

### ConsoleMega Architecture

The `ConsoleMega` class extends the vanilla console with modern features including autocomplete, command history, and improved UI rendering.

Title: ConsoleMega Class Structure

```

ConsoleMega Class

commands (std::set)

autocompleteBuffer

historyPos

inputBuf

ConsoleCommand

aliases

helpText

AutocompleteType Enum

ENTITY

ITEM

STAGE

DEBUG_FLAG

TextEditCallback

ExecuteCommand
```

**Sources:** [repentogon/ImGuiFeatures/ConsoleMega.h111-190](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L111-L190) [repentogon/ImGuiFeatures/ConsoleMega.h21-44](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L21-L44)

### Command Registration and Macros

REPENTOGON registers several default macros to replace vanilla functionality with mod-safe versions (e.g., using IDs instead of names that might change with mods).

| Macro | Commands |
| --- | --- |
| `beast` | `stage 13`, `goto x.itemdungeon.666`, `combo 0.8`, `combo 2.8`, `combo 4.3` |
| `mom` | `stage 6`, `g c33`, `g k5`, `debug 3`, `debug 4` |
| `qk` | Quick kill setup with various items and `debug 3`, `debug 10` |

**Sources:** [repentogon/ImGuiFeatures/ConsoleMega.h173-182](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/ConsoleMega.h#L173-L182)

## Options Management

### REPENTOGONOptions System

Settings are managed through an INI-based system (`options.ini`) that handles both vanilla game options and REPENTOGON-specific features.

Title: REPENTOGONOptions Mapping

```

REPENTOGONOptions

options.ini

VanillaTweaks Section

internal Section

betterVoidGeneration

hushLaserSpeedFix

quickRoomClear

statHUDPlanetarium

skipIntro

preventModUpdates

enableUnifont

unifontRenderMode

lastSaveFile

fileMap

imGuiScale
```

**Sources:** [repentogon/REPENTOGONOptions.h20-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONOptions.h#L20-L150)

### Game Options Interface

The `GameOptionsWindow` provides a tabbed interface for configuring both vanilla and REPENTOGON settings. It uses `AddResetButton` to allow users to revert individual settings to defaults.

**Sources:** [repentogon/ImGuiFeatures/GameOptions.h71-90](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/GameOptions.h#L71-L90) [repentogon/ImGuiFeatures/GameOptions.h135-150](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/GameOptions.h#L135-L150)

## Custom ImGui and Lua Integration

REPENTOGON allows Lua mods to create their own ImGui windows and elements through the `CustomImGui` class.

### Supported Elements and Callbacks

The system supports a wide range of UI elements defined in the `IMGUI_ELEMENT` enum:

- Windows, Menus, Popups
- Buttons, Checkboxes, RadioButtons
- Input fields (Int, Float, Text)
- Plots (Lines, Histograms)
- Progress Bars

Callbacks are handled via the `IMGUI_CALLBACK` enum, allowing Lua to respond to events like `Clicked`, `Hovered`, `Edited`, or `Render`.

**Sources:** [repentogon/ImGuiFeatures/CustomImGui.h20-83](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/CustomImGui.h#L20-L83)

### Lua API Functions

The Lua interface provides several functions to manipulate the ImGui state:

- `ImGui.AddElement(parentId, id, type, text)`: [repentogon/ImGuiFeatures/LuaImGui.cpp40-52](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LuaImGui.cpp#L40-L52)
- `ImGui.CreateWindow(id, title, parentId)`: [repentogon/ImGuiFeatures/LuaImGui.cpp97-114](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LuaImGui.cpp#L97-L114)
- `ImGui.AddCallback(parentId, type, function)`: [repentogon/ImGuiFeatures/LuaImGui.cpp115-131](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LuaImGui.cpp#L115-L131)
- `ImGui.UpdateData(id, dataType, value)`: [repentogon/ImGuiFeatures/LuaImGui.cpp158-174](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LuaImGui.cpp#L158-L174)

## Log Viewer

The `LogViewer` provides a real-time view of game and REPENTOGON logs. It features:

- **Buffer Management**: Uses a circular-style buffer (`logBuf`) with a max size of 4MB. When full, it reduces size by 25% to make room for new entries.
- **Filtering**: Supports both user-defined filters and internal filters to separate `[GAME]`, `[REPENTOGON]`, and `[CONSOLE]` logs.

**Sources:** [repentogon/ImGuiFeatures/LogViewer.h24-30](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LogViewer.h#L24-L30) [repentogon/ImGuiFeatures/LogViewer.h110-143](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/LogViewer.h#L110-L143)

## Font and Localization

### Unicode Support

REPENTOGON uses `UnifontSupport` to provide broad character support, including CJK (Chinese, Japanese, Korean) and Cyrillic ranges.

**Sources:** [repentogon/ImGuiFeatures/UnifontSupport.h8-20](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/UnifontSupport.h#L8-L20)

### Localization

All UI strings are localized. Files like `en_us.inl` define string constants used throughout the ImGui windows.

**Sources:** [repentogon/ImGuiFeatures/Localization/en\_us.inl17-120](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/ImGuiFeatures/Localization/en_us.inl#L17-L120)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#imgui-integration)
- [Architecture Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#architecture-overview)
- [Core Components](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#core-components)
- [Injection and Initialization](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#injection-and-initialization)
- [Rendering Hook](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#rendering-hook)
- [Input Handling](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#input-handling)
- [Console System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#console-system)
- [ConsoleMega Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#consolemega-architecture)
- [Command Registration and Macros](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#command-registration-and-macros)
- [Options Management](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#options-management)
- [REPENTOGONOptions System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#repentogonoptions-system)
- [Game Options Interface](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#game-options-interface)
- [Custom ImGui and Lua Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#custom-imgui-and-lua-integration)
- [Supported Elements and Callbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#supported-elements-and-callbacks)
- [Lua API Functions](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#lua-api-functions)
- [Log Viewer](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#log-viewer)
- [Font and Localization](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#font-and-localization)
- [Unicode Support](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#unicode-support)
- [Localization](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration#localization)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 5.2 Asm Patches And Vanilla Tweaks

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# ASM Patches and Vanilla Tweaks

Relevant source files

- [changelog.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/changelog.txt)
- [libzhl/functions/ASM.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl)
- [libzhl/functions/EntityRef.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/EntityRef.zhl)
- [libzhl/functions/MenuOnline.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuOnline.zhl)
- [libzhl/functions/MenuOnlineLobby.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuOnlineLobby.zhl)
- [libzhl/functions/MenuOnlineOptions.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/MenuOnlineOptions.zhl)
- [libzhl/functions/StatHUD.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/StatHUD.zhl)
- [repentogon/HookTest.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/HookTest.cpp)
- [repentogon/LuaInterfaces/CustomCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/CustomCallbacks.cpp)
- [repentogon/MiscFunctions.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/MiscFunctions.h)
- [repentogon/Patches/ASMPatches.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp)
- [repentogon/Patches/ASMPatches/ASMCallbacks.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.h)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.cpp)
- [repentogon/Patches/ASMPatches/ASMEntityKnife.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityKnife.h)
- [repentogon/Patches/ASMPatches/ASMEntityNPC.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMEntityNPC.h)
- [repentogon/Patches/ASMPatches/ASMRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMRender.cpp)
- [repentogon/Patches/ASMPatches/ASMStatusEffects.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMStatusEffects.cpp)
- [repentogon/Patches/ASMPatches/ASMStatusEffects.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMStatusEffects.h)
- [repentogon/Patches/ASMPatches/ASMStatusEffects\_Definitions.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMStatusEffects_Definitions.h)
- [repentogon/Patches/ASMPatches/ASMTweaks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp)
- [repentogon/Patches/ASMPatches/ASMTweaks.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.h)
- [repentogon/Patches/MiscFixes.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MiscFixes.cpp)
- [repentogon/Patches/VanillaTweaks.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VanillaTweaks.cpp)
- [repentogon/Patches/XMLPlayerExtras.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/XMLPlayerExtras.cpp)
- [repentogon/dllmain.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/dllmain.cpp)
- [repentogon/resources-repentogon/font/luamini.fnt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/font/luamini.fnt)
- [repentogon/resources-repentogon/font/luamini\_0.png](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/font/luamini_0.png)
- [repentogon/resources-repentogon/gfx/ui/bestiary\_tabs.anm2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/bestiary_tabs.anm2)
- [repentogon/resources-repentogon/gfx/ui/bestiary\_tabs.png](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/bestiary_tabs.png)
- [repentogon/resources-repentogon/gfx/ui/changelogpaper.png](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/changelogpaper.png)
- [repentogon/resources-repentogon/gfx/ui/daily\_destinations.anm2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/daily_destinations.anm2)
- [repentogon/resources-repentogon/gfx/ui/leaderboardgoals.png](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/leaderboardgoals.png)
- [repentogon/resources-repentogon/gfx/ui/leaderboardgoals\_sketchAlt.png](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/leaderboardgoals_sketchAlt.png)
- [repentogon/resources-repentogon/gfx/ui/leaderboardmenu.anm2](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/gfx/ui/leaderboardmenu.anm2)
- [repentogon/resources-repentogon/stringtable\_pc.sta](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources-repentogon/stringtable_pc.sta)
- [repentogon/resources/scripts/enums\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/enums_ex.lua)
- [repentogon/resources/scripts/main\_ex.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/main_ex.lua)
- [repentogon/resources/scripts/repentogon\_extras/bestiary\_menu.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/bestiary_menu.lua)
- [repentogon/resources/scripts/repentogon\_extras/changelog.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/changelog.lua)
- [repentogon/resources/scripts/repentogon\_extras/daily\_stats.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/daily_stats.lua)
- [repentogon/resources/scripts/repentogon\_extras/mods\_menu\_tweaks.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/mods_menu_tweaks.lua)
- [repentogon/resources/scripts/repentogon\_extras/onlinestub.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/onlinestub.lua)
- [repentogon/resources/scripts/repentogon\_extras/stats\_menu.lua](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/resources/scripts/repentogon_extras/stats_menu.lua)

This document covers REPENTOGON's binary modification and game improvement systems. These components fix vanilla bugs, optimize performance, and enhance game functionality through runtime patching of the game's executable code.

The system operates at two levels: **Vanilla Tweaks** implement higher-level improvements using the hook system, while **ASM Patches** perform low-level binary modifications for fixes that require direct assembly code manipulation.

For information about the underlying hook system architecture, see [Architecture](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/Architecture) For debugging tools that complement these patches, see [ImGui Integration](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/ImGui%20Integration)

## Patching System Architecture

REPENTOGON's patching system operates through two complementary approaches that modify the game's runtime behavior:

### Patching Architecture Overview

```
REPENTOGON Patching Layer

Isaac Game Executable

ASM Patches

Vanilla Tweaks

Game Binary Code

Game Methods
(RoomConfig, Manager, etc.)

Game Memory Layout

Hook System
(ZHL Framework)

ASMPatcher
(Direct Binary Modification)

Void Rooms Fix
RoomConfig::LoadStageBinary

Console Restrictions
Console::RunCommand

Planetarium Optimization
Level::Init, Game::RestoreState

Eco Mode
Manager::Render

Hornfel Crash Fix
Entity_NPC methods

Godhead Entity Partition Fix
Binary signature patching

Tear Detonator Fix
EntityList modification

Hush FX Veins Fix
Rendering patches

Custom Resource Path
File system patches

KAGE_LogMessage Hook
Manual Varargs Patch
```

**Sources:** [repentogon/Patches/VanillaTweaks.cpp1-172](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VanillaTweaks.cpp#L1-L172) [repentogon/Patches/ASMPatches/ASMTweaks.cpp1-201](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L1-L201) [repentogon/Patches/ASMPatches.cpp54-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L54-L81)

### Patch Application Methods

```
Runtime Application

Binary Patches (ASM)

Hook-Based Patches (Vanilla Tweaks)

HOOK_METHOD
Intercepts function calls

HOOK_STATIC
Hooks static functions

Pre/Post Execution
Calls original with super()

SigScan
Pattern matching in binary

ASMPatch
Code injection/replacement

ByteBuffer
Raw byte manipulation

Game Startup

Patch Initialization

Runtime Code Modification
```

**Sources:** [repentogon/Patches/VanillaTweaks.cpp11-36](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VanillaTweaks.cpp#L11-L36) [repentogon/Patches/ASMPatches/ASMTweaks.cpp17-55](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L17-L55) [repentogon/Patches/ASMPatches.cpp60-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L60-L81)

## Vanilla Tweaks (Hook-Based Patches)

Vanilla Tweaks use the hook system to intercept and modify game method calls. These patches maintain compatibility while fixing bugs and adding features.

### Core Game System Fixes

| Patch | Target Method | Purpose | Implementation |
| --- | --- | --- | --- |
| Void Rooms Fix | `RoomConfig::LoadStageBinary` | Redirects Void stage to proper room files | [VanillaTweaks.cpp11-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/VanillaTweaks.cpp#L11-L15) |
| Console Daily Challenge | `Console::RunCommand` | Prevents console use in non-practice dailies | [VanillaTweaks.cpp52-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/VanillaTweaks.cpp#L52-L58) |
| Options Save Integration | `OptionsConfig::Save` | Ensures REPENTOGON options are saved | [VanillaTweaks.cpp33-36](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/VanillaTweaks.cpp#L33-L36) |
| Death Screen Fix | `GameOver::Show` | Clears mod death portraits to prevent overlap | [repentogon/Patches/MiscFixes.cpp10-13](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MiscFixes.cpp#L10-L13) |
| Animation Safety | `AnimationState::GetNullFrame` | Prevents crash when AnimationData is null | [repentogon/Patches/MiscFixes.cpp19-26](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MiscFixes.cpp#L19-L26) |

### Performance Optimizations

```
Eco Mode System

Window State Check
IsIconic(hwnd)

Process Priority
IDLE_PRIORITY_CLASS

Power Throttling
PROCESS_POWER_THROTTLING

Sleep Delay
5-333ms based on state

Planetarium Chance Optimization

Replaced by

Level::Init
Triggers recalculation

StatHUD::RecomputeStats
Updates planetarium chance

Game::RestoreState
Triggers on save/continue

Per-frame calculation
(Original behavior)

On-demand calculation
(Optimized behavior)
```

**Sources:** [repentogon/Patches/VanillaTweaks.cpp61-70](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VanillaTweaks.cpp#L61-L70) [repentogon/Patches/VanillaTweaks.cpp128-170](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VanillaTweaks.cpp#L128-L170)

### Entity Bug Fixes

The system addresses several critical entity-related crashes and bugs:

#### Hornfel Minecart Crash Fix

- **Problem**: Hornfel NPC could crash when minecart reference becomes invalid.
- **Solution**: State validation in `Entity_NPC::Hornfel_UpdateAI` and `Entity_NPC::Hornfel_UpdateFrame`.
- **Implementation**: [VanillaTweaks.cpp98-118](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/VanillaTweaks.cpp#L98-L118)

#### Follower Chain Safety

- **Problem**: `AddToFollowers` or `AddToDelayed` could cause infinite loops if a familiar parents to itself.
- **Solution**: Check if familiar is already at the front of the chain before adding.
- **Implementation**: [repentogon/Patches/MiscFixes.cpp34-54](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/MiscFixes.cpp#L34-L54)

#### Mystery Gift/Eden's Soul Wisps Bug

- **Problem**: `_wispCollectibleType` not properly reset, causing incorrect wisp behavior.
- **Solution**: Reset `_wispCollectibleType` to 0 in `Entity_Familiar::Init`.
- **Implementation**: [VanillaTweaks.cpp121-125](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/VanillaTweaks.cpp#L121-L125)

## ASM Patches (Binary-Level Modifications)

ASM Patches perform direct binary code modifications using signature scanning and assembly injection. These patches address issues that cannot be resolved through method hooking alone.

### Critical Bug Fixes

```
File System

Custom Resource Paths
PatchResourcePath()

Archive Checksum Skip
SkipArchiveChecksums()

System Fixes

ImGui Log Integration
ASMPatchLogMessage()

Console::RunCommand Fix
ASMPatchConsoleRunCommand()

Leaderboard Validation
LeaderboarEntryCheckerUpdate()

Rendering Fixes

Hush FX Veins
FixHushFXVeins()

History HUD Recompute
HistoryHudRecomputeGfx

Entity System Fixes

Godhead Entity Partition
FixGodheadEntityPartition()

Tear Detonator EntityList
FixTearDetonatorEntityList()

Status Effect System
ASMStatusEffects.cpp
```

**Sources:** [repentogon/Patches/ASMPatches.cpp60-99](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L60-L99) [repentogon/Patches/ASMPatches/ASMTweaks.cpp17-157](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L17-L157) [libzhl/functions/ASM.zhl29-31](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ASM.zhl#L29-L31)

### Manual Hooking: KAGE\_LogMessage

LibZHL cannot hook functions with varargs. REPENTOGON manually patches `KAGE_LogMessage` to capture engine logs for the ImGui Log Viewer.

- **Implementation**: Scans for signature `8d51??8a014184c075??2bca80b9????????0a`.
- **Method**: Pushes `ECX` (containing the formatted string) and calls `LogMessageCallback`.
- **Sources**: [repentogon/Patches/ASMPatches.cpp54-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L54-L81)

### Binary Patch Implementation Pattern

```
"sASMPatcher""ASMPatch""SigScan""Game Code""sASMPatcher""ASMPatch""SigScan""Game Code"Binary signature searchPattern matchingReturn addressBuild patch bytesAdd jumps/callsSubmit patchApply binary modificationExecute patched code
```

**Sources:** [repentogon/Patches/ASMPatches/ASMTweaks.cpp41-55](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L41-L55) [repentogon/Patches/ASMPatches.cpp60-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L60-L81)

### Custom Resource System

REPENTOGON adds support for custom resource directories through binary patching:

#### Custom Resource Path Implementation

- **Primary Path**: `resources` (vanilla)
- **Secondary Path**: `resources-repentogon` (custom)
- **Patch Target**: `RebuildContentMountPoints` function.
- **Method**: Inject additional `addFilepath` calls to mount the custom directory.

```
Resource Loading

RebuildContentMountPoints
Function entry point

addFilepath
File system registration

resources/
Vanilla path

resources-repentogon/
REPENTOGON path
```

**Sources:** [repentogon/Patches/ASMPatches/ASMTweaks.cpp168-199](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L168-L199)

### Command Line Integration

Several patches respond to command line arguments:

| Flag | Patch Function | Effect |
| --- | --- | --- |
| `-unpacked` | `KAGE_Filesys_FileManager::LoadArchiveFile` | Skips archive file loading entirely |
| `-skipchecksum` | `SkipArchiveChecksums()` | Bypasses archive integrity checks |

**Sources:** [repentogon/Patches/VanillaTweaks.cpp71-94](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/VanillaTweaks.cpp#L71-L94) [repentogon/Patches/ASMPatches/ASMTweaks.cpp93-121](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L93-L121)

### Callback Integration (ASM)

Many `ModCallbacks` are implemented via ASM patches to intercept events that have no clean function to hook:

| Callback | Patch Method | Purpose |
| --- | --- | --- |
| `MC_PRE_UPDATE` | `Patch_GameUpdate_MainUpdate` | Allows pausing the game update cycle |
| `MC_PRE_LASER_COLLISION` | `PatchPreSampleLaserCollision` | Intercepts laser hits before damage |
| `MC_PRE_GRID_ENTITY_SPAWN` | `PatchGridSpawnCallback` | Intercepts grid entity creation |

**Sources:** [repentogon/Patches/ASMPatches/ASMCallbacks.cpp90-111](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L90-L111) [repentogon/Patches/ASMPatches/ASMCallbacks.cpp144-161](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMCallbacks.cpp#L144-L161) [repentogon/Patches/ASMPatches.cpp218-220](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches.cpp#L218-L220)

### Entity Management Patches

#### Tear Detonator EntityList Fix

- **Problem**: Shared entity lists cause unintended interactions.
- **Solution**: Call `EntityList_EL::Untie()` to create independent list copies.
- **Implementation**: Assembly patch with custom trampoline function `__TearDetonatorPatch`.
- **Sources**: [repentogon/Patches/ASMPatches/ASMTweaks.cpp31-65](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L31-L65)

#### Godhead Entity Partition Fix

- **Problem**: Incorrect memory allocation size for entity partitioning.
- **Solution**: Change push instruction from `0xFF` to `0x08`.
- **Binary Change**: `6a ff` → `6a 08`.
- **Sources**: [repentogon/Patches/ASMPatches/ASMTweaks.cpp17-29](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ASMPatches/ASMTweaks.cpp#L17-L29)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#asm-patches-and-vanilla-tweaks)
- [Patching System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#patching-system-architecture)
- [Patching Architecture Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#patching-architecture-overview)
- [Patch Application Methods](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#patch-application-methods)
- [Vanilla Tweaks (Hook-Based Patches)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#vanilla-tweaks-hook-based-patches)
- [Core Game System Fixes](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#core-game-system-fixes)
- [Performance Optimizations](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#performance-optimizations)
- [Entity Bug Fixes](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#entity-bug-fixes)
- [Hornfel Minecart Crash Fix](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#hornfel-minecart-crash-fix)
- [Follower Chain Safety](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#follower-chain-safety)
- [Mystery Gift/Eden's Soul Wisps Bug](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#mystery-giftedens-soul-wisps-bug)
- [ASM Patches (Binary-Level Modifications)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#asm-patches-binary-level-modifications)
- [Critical Bug Fixes](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#critical-bug-fixes)
- [Manual Hooking: KAGE\_LogMessage](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#manual-hooking-kage_logmessage)
- [Binary Patch Implementation Pattern](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#binary-patch-implementation-pattern)
- [Custom Resource System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#custom-resource-system)
- [Custom Resource Path Implementation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#custom-resource-path-implementation)
- [Command Line Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#command-line-integration)
- [Callback Integration (ASM)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#callback-integration-asm)
- [Entity Management Patches](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#entity-management-patches)
- [Tear Detonator EntityList Fix](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#tear-detonator-entitylist-fix)
- [Godhead Entity Partition Fix](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks#godhead-entity-partition-fix)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 5.3 Developer Tools

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Developer Tools

Relevant source files

- [.gitattributes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitattributes)
- [.github/workflows/release.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml)
- [appveyor.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml)
- [appveyor\_launcher.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml)
- [appveyor\_repentogon.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_repentogon.yml)
- [delirium/ASMDelirium.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/delirium/ASMDelirium.cpp)
- [delirium/Delirium.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/delirium/Delirium.cpp)
- [delirium/Delirium.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/delirium/Delirium.h)
- [libzhl/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp)
- [libzhl/functions/DeliriumASM.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/DeliriumASM.zhl)
- [libzhl/functions/Shape.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Shape.zhl)
- [loader/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/Version.cpp)
- [repentogon/LuaInterfaces/LuaDelirium.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaDelirium.cpp)
- [repentogon/Patches/ExtraDebugRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp)
- [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)
- [repentogon/REPENTOGONDelirium.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONDelirium.h)
- [repentogon/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp)
- [tools/enums2mkdocs.py](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/enums2mkdocs.py)
- [tools/requirements.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/requirements.txt)
- [version.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt)

The REPENTOGON project includes a suite of developer-facing tools designed to facilitate game reverse engineering, automate documentation, and streamline the build and release process. These tools bridge the gap between the raw game binaries and the high-level Lua API provided to modders.

## Documentation Generation

REPENTOGON utilizes automated scripts to ensure that the Lua API documentation remains in sync with the codebase.

### Enum to Markdown Converter (`enums2mkdocs.py`)

The `enums2mkdocs.py` script is a utility used to parse `enums_ex.lua` and generate Markdown files compatible with MkDocs. This ensures that the extensive list of custom enums and `ModCallbacks` added by REPENTOGON is always documented accurately.

**Key Implementation Details:**

- **Parsing Logic:** The script reads `enums_ex.lua` [tools/enums2mkdocs.py23-33](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/enums2mkdocs.py#L23-L33) identifying class definitions and individual enum entries.
- **Bitwise Support:** It specifically identifies enums marked with `--bitwise` to include a bitset calculator in the generated documentation [tools/enums2mkdocs.py61-62](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/enums2mkdocs.py#L61-L62)
- **MkDocs Integration:** It automatically updates the `mkdocs.yml` navigation structure to include newly generated enum pages [tools/enums2mkdocs.py110-118](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/enums2mkdocs.py#L110-L118)
- **Automation:** When run in a GitHub Actions environment, it automatically commits and pushes the updated documentation back to the repository [tools/enums2mkdocs.py129-132](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/enums2mkdocs.py#L129-L132)

| Feature | Description |
| --- | --- |
| **Input** | `repentogon/resources/scripts/enums_ex.lua` |
| **Output** | `docs/enums/*.md` |
| **Special Handling** | Filters out internal values like `.MC_`, `.ALL`, and `0xffffffff` [tools/enums2mkdocs.py42](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/enums2mkdocs.py#L42-L42) |

**Sources:** [tools/enums2mkdocs.py1-133](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/tools/enums2mkdocs.py#L1-L133)

* * *

## Reverse Engineering & Integration Tools

REPENTOGON relies heavily on `libzhl` and assembly patching to extend the game. Several tools and definitions facilitate this process.

### Ghidra & ZHL Integration

The project uses `.zhl` (ZHL) files to define function signatures and assembly patterns for the `libzhl` library. These definitions allow the C++ code to interact with internal game functions.

**Example: Delirium ASM Definitions**
The file `DeliriumASM.zhl` defines patterns used by the `SigScan` system to locate specific instructions within the Isaac executable [libzhl/functions/DeliriumASM.zhl1-3](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/DeliriumASM.zhl#L1-L3) These addresses are then used by the `ASMPatcher` to modify game logic at runtime.

### ASMPatcher Utility

The `ASMPatcher` class provides a developer-friendly interface for applying hot-patches to the game's machine code.

**Data Flow: From ZHL Definition to Applied Patch**

1. **Definition:** An `asm` signature is defined in a `.zhl` file.
2. **Lookup:** The `sASMDefinitionHolder` retrieves the resolved memory address [delirium/ASMDelirium.cpp30](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/delirium/ASMDelirium.cpp#L30-L30)
3. **Patch Creation:** A `ByteBuffer` is populated with new instructions (e.g., `xor eax, eax` to skip frames) [delirium/ASMDelirium.cpp36-37](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/delirium/ASMDelirium.cpp#L36-L37)
4. **Application:** The `sASMPatcher` applies either a `FlatPatch` (overwriting bytes) or a complex `PatchAt` (redirecting flow to a C++ function) [delirium/ASMDelirium.cpp40-71](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/delirium/ASMDelirium.cpp#L40-L71)

**Diagram: ASM Patching Workflow**

```
Code Entity Space

Natural Language Space

Defines DeliriumAggression

Calls

Creates ASMPatch

Overwrites bytes at address

'I want to disable Delirium's frame skipping'

libzhl/functions/DeliriumASM.zhl

sASMDefinitionHolder::GetDefinition

delirium::PatchSkipFrames

ASMPatcher::FlatPatch

Isaac.exe Binary
```

**Sources:** [delirium/ASMDelirium.cpp29-73](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/delirium/ASMDelirium.cpp#L29-L73) [libzhl/functions/DeliriumASM.zhl1-4](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/DeliriumASM.zhl#L1-L4)

* * *

## Build and Release Automation

REPENTOGON uses a complex CI/CD pipeline involving GitHub Actions and AppVeyor to manage builds, versioning, and artifact distribution.

### Versioning System

The version is centrally managed in `version.txt` [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1) During the build process:

1. The version string is read and injected into `Version.h` as a macro [.github/workflows/release.yml35-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/%20.github/workflows/release.yml#L35-L38)
2. The Lua environment is updated by replacing the `"dev build"` placeholder in `main_ex.lua` [appveyor.yml15-16](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L15-L16)
3. The version is passed to CMake to set `CMAKE_REPENTOGON_VERSION` [appveyor.yml17-18](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L17-L18)

### Build Pipeline (`release.yml` & `appveyor.yml`)

The build system automates the compilation of multiple DLLs and the packaging of resources.

**Diagram: Artifact Generation Pipeline**

```
Artifacts

Build Process

version.txt

PowerShell Script

Version.h

main_ex.lua

CMake (Win32)

MSBuild (Release)

zhlREPENTOGON.dll

libzhl.dll

dsound.dll

resources/

REPENTOGON.zip
```

**Sources:** [.github/workflows/release.yml1-74](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L1-L74) [appveyor.yml1-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L1-L58) [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1)

* * *

## Debugging Tools

### Extra Debug Rendering

REPENTOGON extends the game's internal debug renderer. Developers can toggle specialized visualizations, such as the `QueryRadius` visualization which draws a circle in the game world whenever the engine performs a proximity check for entities [repentogon/Patches/ExtraDebugRender.cpp6-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp#L6-L15)

### Exception Handling

A custom exception handler is implemented to provide more detailed crash logs than the vanilla game, aiding in the debugging of low-level C++ hooks [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)

**Sources:** [repentogon/Patches/ExtraDebugRender.cpp6-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp#L6-L15) [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#developer-tools)
- [Documentation Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#documentation-generation)
- [Enum to Markdown Converter (\`enums2mkdocs.py\`)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#enum-to-markdown-converter-enums2mkdocspy)
- [Reverse Engineering & Integration Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#reverse-engineering-integration-tools)
- [Ghidra & ZHL Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#ghidra-zhl-integration)
- [ASMPatcher Utility](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#asmpatcher-utility)
- [Build and Release Automation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#build-and-release-automation)
- [Versioning System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#versioning-system)
- [Build Pipeline (\`release.yml\` & \`appveyor.yml\`)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#build-pipeline-releaseyml-appveyoryml)
- [Debugging Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#debugging-tools)
- [Extra Debug Rendering](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#extra-debug-rendering)
- [Exception Handling](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools#exception-handling)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 6 Development

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Development

Relevant source files

- [.gitattributes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitattributes)
- [.github/workflows/release.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml)
- [.gitmodules](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitmodules)
- [CMakeLists.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt)
- [appveyor.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml)
- [appveyor\_launcher.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml)
- [appveyor\_repentogon.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_repentogon.yml)
- [libzhl/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp)
- [libzhl/functions/Shape.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Shape.zhl)
- [loader/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/Version.cpp)
- [repentogon/Patches/ExtraDebugRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp)
- [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)
- [repentogon/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp)
- [version.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt)

This page provides guidance for developers working on REPENTOGON itself, covering the development workflow, architecture, build systems, and contribution patterns. For information about using REPENTOGON's modding API, see [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api). For build system specifics, see [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning). For technical implementation details, see [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference).

## Development Architecture

REPENTOGON is built as a two-layer architecture where `libzhl` provides the foundational hooking and Lua integration infrastructure, while `repentogon` implements the game-specific extensions and API.

### Core Component Structure

```
REPENTOGON Development Stack

External Dependencies

libzhl Layer (libzhl.dll)

REPENTOGON Layer (zhlREPENTOGON.dll)

Game Integration Layer

Lua 5.3.3r
Scripting Engine

Isaac Game Engine
isaac-ng.exe

ModCallbacks Extensions
1400+ Callback Types

ASM Patches & Vanilla Fixes
Game Behavior Modifications

HookSystem
Runtime Function Interception

Lua Interface Implementations
Entity, Room, ItemPool APIs

LuaCore
Lua State Management

XML Data System
Custom Content Loading

zhlparser
Function Signature Processing

SigScan
Memory Pattern Matching

FreeType
Font Rendering

Zydis
Disassembler Library

Isaac DLLs
Native Game Logic
```

Sources: [CMakeLists.txt29-80](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L29-L80) [appveyor.yml37-48](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L37-L48) [repentogon/Patches/ExtraDebugRender.cpp1-15](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp#L1-L15)

### Development Workflow Components

```
Release Artifacts

CI/CD Systems

Build Pipeline

Source Management

GitHub Repository
TeamREPENTOGON/REPENTOGON

.gitmodules
External Dependencies

CMakeLists.txt
Cross-platform Configuration

Visual Studio 2022
Win32 Compilation

version.txt
Master Version String

release.yml
Automated Releases

appveyor.yml
Continuous Integration

SignPath Webhook
Code Signing

zhlREPENTOGON.dll
Core Extension

libzhl.dll
Hook Framework

Lua5.3.3r.dll
Scripting Engine

resources-repentogon/
Lua Scripts & Data
```

Sources: [.github/workflows/release.yml1-75](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L1-L75) [appveyor.yml1-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L1-L58) [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1) [.gitmodules1-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitmodules#L1-L38)

## Build System Architecture

The build system uses CMake to orchestrate the compilation of multiple internal libraries and the generation of code from ZHL definitions.

### Build and Versioning Overview

For a comprehensive guide on the CI/CD pipeline and versioning logic, see [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning).

- **Version Tracking**: The project version is maintained in `version.txt` [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1) and passed to CMake via `-DCMAKE_REPENTOGON_VERSION` [appveyor.yml18](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L18-L18)
- **Version Embedding**: Version strings are embedded into C++ via `Version.cpp` [repentogon/Version.cpp4](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp#L4-L4) and patched into Lua scripts like `main_ex.lua` during the build process [appveyor.yml15-16](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L15-L16)
- **Dependency Management**: External libraries (Zydis, ANTLR4, ImGui, etc.) are managed as git submodules [.gitmodules1-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitmodules#L1-L38) and integrated via `add_subdirectory` or direct source inclusion in `CMakeLists.txt` [CMakeLists.txt33-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L33-L40)

### Release Pipeline Process

```
"Release""SignPath""AppVeyor""GitHub Actions""Git Repository""Developer""Release""SignPath""AppVeyor""GitHub Actions""Git Repository""Developer"Release Tag BuildsPush to main branchTrigger release.ymlRead version.txtGenerate Version.hPatch main_ex.luaCMake Build (Win32)Upload REPENTOGON.zipTrigger on "chore: release"Build Release ArtifactsWebhook to SignPathSign BinariesPush Signed Artifacts
```

Sources: [.github/workflows/release.yml27-75](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L27-L75) [appveyor.yml1-65](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L1-L65) [appveyor\_repentogon.yml1-61](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_repentogon.yml#L1-L61)

## Technical Reference Overview

The core of REPENTOGON's power lies in its ability to interface directly with the game's memory and internal functions. For deep technical details on these systems, see [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference).

### ZHL Function Definition System

REPENTOGON uses a custom tool, `zhlparser`, to process `.zhl` files which contain function signatures and memory offsets [CMakeLists.txt47-57](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L47-L57)

- **Code Generation**: `zhlparser` generates `IsaacRepentance.h` and `IsaacRepentance.cpp` based on the definitions in `libzhl/functions/` [CMakeLists.txt67-73](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L67-L73)
- **Hooking**: The `HOOK_METHOD` and `HOOK_GLOBAL` macros are used to intercept game functions at runtime [repentogon/Patches/ExtraDebugRender.cpp6](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp#L6-L6)

### Crash Handling and Debugging

REPENTOGON implements a custom exception handler to provide better diagnostic information for vanilla game crashes.

- **Minidumps**: The handler uses `MiniDumpWriteDump` from `dbghelp.dll` to create `.dmp` files in the REPENTOGON data path [repentogon/Patches/NewExceptionHandler.cpp41-62](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp#L41-L62)
- **Lua Tracebacks**: If the `g_LuaEngine` is active during a crash, the handler attempts to extract a Lua stack trace to aid in debugging mod-related issues [repentogon/Patches/NewExceptionHandler.cpp17-30](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp#L17-L30)

Sources: [CMakeLists.txt67-73](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L67-L73) [repentogon/Patches/NewExceptionHandler.cpp1-71](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp#L1-L71) [libzhl/Version.cpp1-9](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp#L1-L9)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#development)
- [Development Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#development-architecture)
- [Core Component Structure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#core-component-structure)
- [Development Workflow Components](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#development-workflow-components)
- [Build System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#build-system-architecture)
- [Build and Versioning Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#build-and-versioning-overview)
- [Release Pipeline Process](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#release-pipeline-process)
- [Technical Reference Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#technical-reference-overview)
- [ZHL Function Definition System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#zhl-function-definition-system)
- [Crash Handling and Debugging](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development#crash-handling-and-debugging)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 6.1 Build And Versioning

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Build and Versioning

Relevant source files

- [.gitattributes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitattributes)
- [.github/workflows/docs.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/docs.yml)
- [.github/workflows/release.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml)
- [.gitmodules](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitmodules)
- [CMakeLists.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt)
- [appveyor.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml)
- [appveyor\_launcher.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml)
- [appveyor\_repentogon.yml](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_repentogon.yml)
- [docs/docs/css/custom.css](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/docs/css/custom.css)
- [docs/overrides/home.html](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/overrides/home.html)
- [docs/overrides/main.html](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/docs/overrides/main.html)
- [libzhl/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp)
- [libzhl/functions/Shape.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Shape.zhl)
- [loader/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/loader/Version.cpp)
- [repentogon/Patches/ExtraDebugRender.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/ExtraDebugRender.cpp)
- [repentogon/Patches/NewExceptionHandler.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Patches/NewExceptionHandler.cpp)
- [repentogon/Version.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp)
- [version.txt](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt)

This document covers REPENTOGON's build system, versioning strategy, and CI/CD pipeline. It explains how version information flows through the codebase, the automated build processes, and artifact distribution mechanisms.

## Version Management System

REPENTOGON uses a centralized versioning approach where the canonical version is stored in `version.txt` and propagated throughout the build system during the CI process.

### Version Propagation Flow

The following diagram illustrates how the version string from `version.txt` is injected into various code entities and build variables.

```
Build System Variables

Runtime Version Exports

Build-Time Generation

version.txt
Canonical Version Source

Version.h
#define VERSION

changelog_official_text.lua
Lua Changelog Text

main_ex.lua
Script Version Display

libzhl/Version.cpp
__ZHL_VERSION export

repentogon/Version.cpp
__REPENTOGON_VERSION export

CMAKE_ZHL_VERSION
CMake Variable

CMAKE_REPENTOGON_VERSION
CMake Variable
```

**Sources:** [version.txt1](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/version.txt#L1-L1) [.github/workflows/release.yml36-40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L36-L40) [libzhl/Version.cpp1-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp#L1-L8) [repentogon/Version.cpp1-5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp#L1-L5) [CMakeLists.txt8-14](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L8-L14)

### Version Export Mechanism

Both `libzhl` and `repentogon` components export their version strings as DLL exports for runtime version checking. This allows external tools or the loader to verify compatibility.

| Component | Export Symbol | Source Variable | Fallback Value |
| --- | --- | --- | --- |
| `libzhl` | `__ZHL_VERSION` | `CMAKE_ZHL_VERSION` | `"zhl-nover"` |
| `repentogon` | `__REPENTOGON_VERSION` | `CMAKE_REPENTOGON_VERSION` | N/A (CMake define) |

In `libzhl/Version.cpp`, a preprocessor check ensures the build process is "safe" by verifying `CMAKE_ZHL_VERSION` is defined [libzhl/Version.cpp1-4](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp#L1-L4)

**Sources:** [libzhl/Version.cpp1-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Version.cpp#L1-L8) [repentogon/Version.cpp1-5](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/Version.cpp#L1-L5) [CMakeLists.txt82](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L82-L82) [CMakeLists.txt92](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L92-L92)

## Build System Architecture

REPENTOGON uses CMake as its primary build system with Visual Studio 2022 as the compiler toolchain. The build process targets the `Win32` (x86) architecture to match the game's executable.

### Build Configuration and Dependency Tree

The project manages a significant number of dependencies via git submodules, which are initialized during the build script [appveyor.yml9-10](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L9-L10)

```
Core Libraries

Build Tools

External Dependencies (Submodules)

Processes .zhl files

libs/zydis

libs/antlr4

libs/lua

libs/imgui

libs/freetype

zhlparser (Executable)

libzhlgen/*.cpp

libzhl.dll

zhlLoader.dll

Lua5.3.3r.dll

libzhl/IsaacRepentance.cpp
```

**Sources:** [CMakeLists.txt16](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L16-L16) [CMakeLists.txt33](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L33-L33) [CMakeLists.txt40](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L40-L40) [CMakeLists.txt47-49](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L47-L49) [CMakeLists.txt62](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L62-L62) [CMakeLists.txt67-73](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L67-L73) [CMakeLists.txt79](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L79-L79) [CMakeLists.txt89-90](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L89-L90) [.gitmodules1-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.gitmodules#L1-L38)

### Key Build Targets

1. **zhlparser**: A standalone executable built from `libzhlgen` that parses `.zhl` files to generate C++ headers and implementation files [CMakeLists.txt47-49](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L47-L49)
2. **Lua5.3.3r**: A shared library version of Lua 5.3.3 [CMakeLists.txt62](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L62-L62)
3. **libzhl**: The core hooking library. It depends on the output of `zhlparser` [CMakeLists.txt79-81](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L79-L81)
4. **freetype**: A shared library for font rendering, used by ImGui [CMakeLists.txt141](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/CMakeLists.txt#L141-L141)

## CI/CD Pipeline

REPENTOGON employs a dual CI/CD strategy using GitHub Actions for general releases and documentation, and AppVeyor for specialized signing and launcher builds.

### GitHub Actions Release Pipeline

The `release.yml` workflow automates the creation of GitHub Releases.

| Step | Action | Code Reference |
| --- | --- | --- |
| **Changelog** | Converts `changelog.txt` to a Lua string for in-game display | [.github/workflows/release.yml30-34](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L30-L34) |
| **Headers** | Generates `Version.h` with the current version string | [.github/workflows/release.yml35-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L35-L38) |
| **Configure** | Runs CMake with `-G "Visual Studio 17 2022" -A "Win32"` | [.github/workflows/release.yml42](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L42-L42) |
| **Build** | Executes `cmake --build` in Release configuration | [.github/workflows/release.yml45](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L45-L45) |
| **Package** | Compresses artifacts into `REPENTOGON.zip` | [.github/workflows/release.yml61](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L61-L61) |

### AppVeyor Pipelines

AppVeyor is used for builds that require integration with SignPath for code signing.

- **Main Build**: Triggered by commit messages starting with `chore: release`. It builds the main project and pushes the artifact to AppVeyor's internal storage [appveyor.yml1-58](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L1-L58)
- **Launcher Build**: A separate pipeline specifically for the `REPENTOGONLauncher`, using Visual Studio 2019 [appveyor\_launcher.yml1-38](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml#L1-L38)
- **Deployment**: Both AppVeyor pipelines use Webhooks to trigger signing policies on SignPath [appveyor.yml60-65](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L60-L65) [appveyor\_launcher.yml40-45](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor_launcher.yml#L40-L45)

### Documentation CI/CD

Documentation is managed via GitHub Actions in `docs.yml`. It includes:

- **Enums Update**: Runs `tools/enums2mkdocs.py` to keep documentation in sync with `enums_ex.lua` [.github/workflows/docs.yml28-29](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/docs.yml#L28-L29)
- **Code Checks**: Runs a Node.js script `code_checks.js` to validate documentation integrity [.github/workflows/docs.yml42-44](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/docs.yml#L42-L44)
- **Deployment**: Builds the site using `zensical` and deploys to GitHub Pages [.github/workflows/docs.yml57-64](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/docs.yml#L57-L64)

## Artifact Creation

The build process gathers outputs from multiple targets into a standardized structure.

```
Data Artifacts

Binary Artifacts

dsound.dll (Proxy)

libzhl.dll

zhlREPENTOGON.dll

Lua5.3.3r.dll / Lua5.4.dll

freetype.dll

resources/

resources-repentogon/

rgon_changelog.txt

REPENTOGON.zip
```

**Sources:** [appveyor.yml25-56](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L25-L56) [.github/workflows/release.yml50-61](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L50-L61)

**Note on Proxy DLLs:** The project often includes `dsound.dll`, which acts as a DLL hijacking proxy to load the REPENTOGON framework when the game starts [appveyor.yml31-32](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L31-L32)

**Sources:** [appveyor.yml31-32](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/appveyor.yml#L31-L32) [.github/workflows/release.yml54](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/.github/workflows/release.yml#L54-L54)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#build-and-versioning)
- [Version Management System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#version-management-system)
- [Version Propagation Flow](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#version-propagation-flow)
- [Version Export Mechanism](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#version-export-mechanism)
- [Build System Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#build-system-architecture)
- [Build Configuration and Dependency Tree](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#build-configuration-and-dependency-tree)
- [Key Build Targets](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#key-build-targets)
- [CI/CD Pipeline](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#cicd-pipeline)
- [GitHub Actions Release Pipeline](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#github-actions-release-pipeline)
- [AppVeyor Pipelines](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#appveyor-pipelines)
- [Documentation CI/CD](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#documentation-cicd)
- [Artifact Creation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning#artifact-creation)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

## 6.2 Technical Reference

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[TeamREPENTOGON/REPENTOGON](https://github.com/TeamREPENTOGON/REPENTOGON "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [7242aa](https://github.com/TeamREPENTOGON/REPENTOGON/commits/7242aa5b))

- [Overview](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1-overview)
- [Architecture](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/1.1-architecture)
- [Lua Modding API](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2-lua-modding-api)
- [ModCallbacks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.1-modcallbacks)
- [Entity Interfaces](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.2-entity-interfaces)
- [Room and Level](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.3-room-and-level)
- [ItemPool](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.4-itempool)
- [Rendering and Visual APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.5-rendering-and-visual-apis)
- [Utility APIs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/2.6-utility-apis)
- [XML and Custom Cache](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3-xml-and-custom-cache)
- [XML Data System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.1-xml-data-system)
- [Custom Cache System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/3.2-custom-cache-system)
- [Game Systems](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4-game-systems)
- [Entity System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.1-entity-system)
- [Room Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.2-room-generation)
- [Level Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.3-level-generation)
- [Animation System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.4-animation-system)
- [Achievement and Challenge System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.5-achievement-and-challenge-system)
- [Save State and Persistence](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.6-save-state-and-persistence)
- [Menu System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/4.7-menu-system)
- [Tools and Features](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5-tools-and-features)
- [ImGui Integration](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.1-imgui-integration)
- [ASM Patches and Vanilla Tweaks](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.2-asm-patches-and-vanilla-tweaks)
- [Developer Tools](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/5.3-developer-tools)
- [Development](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6-development)
- [Build and Versioning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.1-build-and-versioning)
- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference)
- [Glossary](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/7-glossary)

Menu

# Technical Reference

Relevant source files

- [libzhl/HookSystem.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem.cpp)
- [libzhl/HookSystem\_private.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem_private.h)
- [libzhl/IsaacRepentance\_static.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/IsaacRepentance_static.cpp)
- [libzhl/Log.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Log.cpp)
- [libzhl/Log.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/Log.h)
- [libzhl/functions/ExtraTypes](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ExtraTypes)
- [libzhl/functions/Global.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Global.zhl)
- [libzhl/functions/ItemPool.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl)
- [libzhl/functions/ItemPool\_Item.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool_Item.zhl)
- [libzhl/functions/VCRuntime.zhl](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/VCRuntime.zhl)
- [libzhlgen/CodeEmitter.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/CodeEmitter.cpp)
- [libzhlgen/CodeEmitter.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/CodeEmitter.h)
- [libzhlgen/ParserCore.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ParserCore.cpp)
- [libzhlgen/ParserCore.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ParserCore.h)
- [libzhlgen/ParserDefinitions.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ParserDefinitions.cpp)
- [libzhlgen/ParserDefinitions.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ParserDefinitions.h)
- [libzhlgen/ZHLParser.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParser.cpp)
- [libzhlgen/ZHLParser.g4](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParser.g4)
- [libzhlgen/ZHLParser.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParser.h)
- [libzhlgen/ZHLParser.interp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParser.interp)
- [libzhlgen/ZHLParserBaseListener.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParserBaseListener.h)
- [libzhlgen/ZHLParserBaseVisitor.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParserBaseVisitor.h)
- [libzhlgen/ZHLParserListener.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParserListener.h)
- [libzhlgen/ZHLParserVisitor.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/ZHLParserVisitor.h)
- [libzhlgen/parser.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/parser.cpp)
- [repentogon/LuaInterfaces/LuaItemPool.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp)
- [repentogon/REPENTOGONFileMap.cpp](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONFileMap.cpp)
- [repentogon/REPENTOGONFileMap.h](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONFileMap.h)

This page provides comprehensive technical reference documentation for REPENTOGON's internal implementation, including global data structures, type definitions, ZHL code generation, and advanced implementation details. This reference is intended for framework contributors and advanced mod developers who need deep technical knowledge of REPENTOGON's architecture.

## Global Data Structures and Type System

REPENTOGON defines an extensive type system and global data structures that form the foundation of the framework. These definitions ensure type safety and consistent data handling across the C++/Lua boundary.

### Core Type Definitions

REPENTOGON defines numerous primitive and compound types used throughout the system. These are primarily defined in `ExtraTypes` to assist the ZHL generator in calculating memory offsets and alignments.

```
STL Container Definitions

std_vector_int (Size 12)

std_vector_float (Size 12)

std_string (Size 24)

deque_Point (Size 20)

LootList (Size 20)

Game-Specific Type Info

CollectibleType (Size 4)

Direction (Size 4)

GridEntityType (Size 4)

TrinketType (Size 4)

WeaponType (Size 4)

Primitive Type Mapping

uint64_t (unsigned long long)

uint32_t (unsigned int)

uint16_t (unsigned short)

uint8_t (unsigned char)

int64_t (long long)

int32_t (int)
```

Sources: [libzhl/functions/ExtraTypes1-52](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ExtraTypes#L1-L52) [libzhl/functions/ExtraTypes103-126](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ExtraTypes#L103-L126) [libzhl/functions/ExtraTypes238-241](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ExtraTypes#L238-L241)

### STL Container Typedefs

To bridge C++ templates with the ZHL hooking system, REPENTOGON uses explicit typedefs for common STL containers. This allows the `libzhlgen` tool to generate appropriate C-style wrappers.

```
// libzhl/functions/Global.zhl
typedef std::vector<MusicEntry> vector_MusicEntry;
typedef std::vector<SoundEffect> vector_SoundEffect;
typedef std::vector<ColorParams> vector_ColorParams;
typedef std::deque<Point> deque_Point;
typedef std::vector<Entity_Player*> vector_EntityPlayerPtr;
typedef std::vector<ItemConfig_Item*> vector_ItemPtr;
typedef std::deque<LootListEntry> LootList;
typedef std::map<int, int> std_map_int_int;
typedef std::bitset<8> DoorsBitSet;
```

Sources: [libzhl/functions/Global.zhl54-98](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Global.zhl#L54-L98) [libzhl/functions/Global.zhl128](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Global.zhl#L128-L128)

### Key Game Structures

Several critical structures are mapped directly to game memory. For example, the `PoolItem` structure defines how items are weighted within the game's item pool system.

| Field | Type | Offset | Description |
| --- | --- | --- | --- |
| `_itemID` | `uint32_t` | 0x0 | The ID of the collectible |
| `_initialWeight` | `float` | 0x4 | Starting weight in the pool |
| `_weight` | `float` | 0x8 | Current weight (dynamic) |
| `_decreaseBy` | `float` | 0xC | Amount to reduce weight on pick |
| `_removeOn` | `float` | 0x10 | Weight threshold for removal |
| `_isUnlocked` | `bool` | 0x14 | Unlock status |
| `_isSpecial` | `bool` | 0x15 | Special item flag |

Sources: [libzhl/functions/Global.zhl102-113](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/Global.zhl#L102-L113)

## ZHL (Zero Hook Library) Code Generation

The core of REPENTOGON's interoperability is **libzhl**, a system that parses `.zhl` files to generate C++ headers, implementation files, and JSON hook definitions.

### ZHL Processing Pipeline

The `CodeEmitter` class manages the lifecycle of code generation, transforming high-level function signatures and structure definitions into compilable C++ code.

```
Internal Logic

Output Generation

.zhl Files

ZHLParser (ANTLR4)

CodeEmitter::Emit()

ZHLInterface.h

ZHLInterface.cpp

ZHLHooks.json

TypeMap Validation

Signature Extraction

ASM Definitions
```

Sources: [libzhlgen/CodeEmitter.cpp35-41](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/CodeEmitter.cpp#L35-L41) [libzhlgen/CodeEmitter.cpp106-142](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/CodeEmitter.cpp#L106-L142) [libzhlgen/parser.cpp100-111](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhlgen/parser.cpp#L100-L111)

### Function and Variable Definitions

The `HookSystem` uses `FunctionDefinition` and `VariableDefinition` classes to manage runtime memory addresses found via signature scanning.

- **FunctionDefinition**: Stores metadata about a function, including its calling convention (e.g., `__thiscall`), argument count, and whether it can be hooked. [libzhl/HookSystem\_private.h99-143](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem_private.h#L99-L143)
- **VariableDefinition**: Stores a pointer to a global variable in game memory, resolved via `SigScan`. [libzhl/HookSystem\_private.h147-159](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem_private.h#L147-L159)

### Signature Scanning

Signatures are defined as hex strings with masks (e.g., `?` for wildcards). The `Definition::Load()` method triggers a `SigScan` to find the physical address in the game's memory space.

```
// Example ZHL definition for ItemPool::GetTrinket
"558bec83ec40a1????????33c58945??53568bf1":
__thiscall uint32_t ItemPool::GetTrinket(bool DontAdvanceRNG);
```

Sources: [libzhl/functions/ItemPool.zhl7-8](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L7-L8) [libzhl/HookSystem.cpp116-130](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem.cpp#L116-L130)

## Implementation Details: ItemPool System

The `ItemPool` system is a prime example of how REPENTOGON bridges vanilla game logic with Lua.

### ItemPool Structure Layout

The `ItemPool` class is defined in ZHL with specific memory offsets to match the game's internal layout.

```
struct ItemPool depends (ItemPool_Item, RNG) {
    ItemPool_Item _pools[31] : 0x4;
    int _lastPool : 0x650;
    RNG _itemPoolRNG : 0x654;
    vector_bool _removedCollectibles : 0x67c;
    vector_bool _roomBlacklistedCollectibles : 0x68c;
    vector_TrinketPoolItem _trinketPoolItems : 0x794;
    int _pillEffects[15] : 0x7a4;
} : 0x830;
```

Sources: [libzhl/functions/ItemPool.zhl73-88](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/functions/ItemPool.zhl#L73-L88)

### Lua Bridge Logic

When a mod calls `ItemPool:GetCollectibleEx`, the C++ backend performs validation, ensures a valid RNG seed, and calls the original game function via the ZHL-resolved pointer.

```

```

Sources: [repentogon/LuaInterfaces/LuaItemPool.cpp83-109](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp#L83-L109) [repentogon/LuaInterfaces/LuaItemPool.cpp24-26](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/LuaInterfaces/LuaItemPool.cpp#L24-L26)

## File System Mapping (REPENTOGONFileMap)

REPENTOGON implements a high-performance file mapping system to handle path redirection for mods, replacing the vanilla path resolution logic when enabled.

### Path Normalization and Hashing

To ensure fast lookups, paths are normalized (converting `\` to `/`, resolving `..`) and hashed.

1. **Normalization**: `NormalizePathString` handles directory traversal logic. [repentogon/REPENTOGONFileMap.cpp61-97](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONFileMap.cpp#L61-L97)
2. **Hashing**: Paths are converted to lowercase and hashed using `std::hash<std::wstring>`. [repentogon/REPENTOGONFileMap.cpp107-112](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONFileMap.cpp#L107-L112)
3. **Redirection**: The `ModManager::TryRedirectPath` hook intercepts file requests and checks the `_filemap` for overrides. [repentogon/REPENTOGONFileMap.cpp174-201](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/repentogon/REPENTOGONFileMap.cpp#L174-L201)

## Grid and Room Logic

REPENTOGON provides helper methods for complex game logic, such as validating grid indices based on room shapes. This is critical for custom room generation and entity placement.

### Room Shape Validation

The `RoomConfig_Room::IsValidGridIndex` function contains hardcoded logic for every `RoomShape` (1x1, IH, IV, 1x2, etc.) to determine if a specific grid index is within bounds or represents a wall.

```
// libzhl/IsaacRepentance_static.cpp
switch (Shape) {
    case ROOMSHAPE_1x1:
        if (includeWalls) return index <= 134;
        else return index <= 118 && index % 15 != 0 && index % 15 != 14 && index >= 16;
    case ROOMSHAPE_IH:
        // Narrow horizontal room logic
        if (includeWalls) return index >= 30 && index <= 104;
        // ...
}
```

Sources: [libzhl/IsaacRepentance\_static.cpp48-104](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/IsaacRepentance_static.cpp#L48-L104)

## Hooking Infrastructure

The `HookSystem` utilizes `MologieDetours` to perform runtime function detouring.

### Hook Installation Process

1. **Initialization**: `ZHL::Init()` prepares the detour engine. [libzhl/HookSystem.cpp22-34](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem.cpp#L22-L34)
2. **Loading**: `FunctionDefinition::Load()` uses `SigScan` to find the target address. [libzhl/HookSystem.cpp281-300](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem.cpp#L281-L300)
3. **Detouring**: `FunctionHook_private::Install()` applies the actual jump in memory to redirect execution to REPENTOGON's custom logic. [libzhl/HookSystem\_private.h201](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem_private.h#L201-L201)

Sources: [libzhl/HookSystem.cpp22-34](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem.cpp#L22-L34) [libzhl/HookSystem\_private.h165-216](https://github.com/TeamREPENTOGON/REPENTOGON/blob/7242aa5b/libzhl/HookSystem_private.h#L165-L216)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Technical Reference](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#technical-reference)
- [Global Data Structures and Type System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#global-data-structures-and-type-system)
- [Core Type Definitions](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#core-type-definitions)
- [STL Container Typedefs](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#stl-container-typedefs)
- [Key Game Structures](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#key-game-structures)
- [ZHL (Zero Hook Library) Code Generation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#zhl-zero-hook-library-code-generation)
- [ZHL Processing Pipeline](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#zhl-processing-pipeline)
- [Function and Variable Definitions](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#function-and-variable-definitions)
- [Signature Scanning](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#signature-scanning)
- [Implementation Details: ItemPool System](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#implementation-details-itempool-system)
- [ItemPool Structure Layout](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#itempool-structure-layout)
- [Lua Bridge Logic](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#lua-bridge-logic)
- [File System Mapping (REPENTOGONFileMap)](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#file-system-mapping-repentogonfilemap)
- [Path Normalization and Hashing](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#path-normalization-and-hashing)
- [Grid and Room Logic](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#grid-and-room-logic)
- [Room Shape Validation](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#room-shape-validation)
- [Hooking Infrastructure](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#hooking-infrastructure)
- [Hook Installation Process](https://deepwiki.com/TeamREPENTOGON/REPENTOGON/6.2-technical-reference#hook-installation-process)

Ask Devin about TeamREPENTOGON/REPENTOGON

Fast

---

