# isaacscript
- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# IsaacScript Overview

Relevant source files

- [package-lock.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package-lock.json)
- [package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json)
- [packages/docs/docs/main/change-log.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/change-log.md?plain=1)
- [packages/docs/docs/main/features.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/features.md?plain=1)
- [packages/docs/docs/main/getting-started.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1)
- [packages/docs/docs/main/isaacscript-in-typescript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-typescript.md?plain=1)
- [packages/docs/docusaurus.config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docusaurus.config.ts)
- [packages/docs/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/package.json)
- [packages/docs/sidebars.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/sidebars.ts)
- [packages/docs/src/css/custom.css](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/src/css/custom.css)
- [packages/docs/static/img/lua.png](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/static/img/lua.png)
- [packages/docs/static/img/typescript.png](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/static/img/typescript.png)
- [packages/eslint-config-isaacscript/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/package.json)
- [packages/eslint-plugin-isaacscript/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json)
- [packages/isaac-lua-polyfill/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/package.json)
- [packages/isaac-typescript-definitions-repentogon/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/package.json)
- [packages/isaac-typescript-definitions/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json)
- [packages/isaacscript-cli/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json)
- [packages/isaacscript-common/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json)
- [packages/isaacscript-common/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/index.ts)
- [packages/isaacscript-lint/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json)
- [packages/isaacscript-lua/isaacscript\_lua.py](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py)
- [packages/isaacscript-lua/publish.sh](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/publish.sh)
- [packages/isaacscript-lua/pyproject.toml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/pyproject.toml)
- [packages/isaacscript-spell/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/package.json)
- [todo.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/todo.txt)

IsaacScript is a comprehensive monorepo and framework designed to modernize modding for _The Binding of Isaac: Repentance_. It enables developers to write mods in TypeScript, which are then transpiled to Lua using [TypeScript-to-Lua (TSTL)](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/TypeScript-to-Lua%20(TSTL))

The project provides a complete ecosystem including a CLI for project management, a robust standard library (`isaacscript-common`), high-quality type definitions for the game API, and a strict linting stack to ensure code quality.

## High-Level Ecosystem

The IsaacScript monorepo is organized into several specialized packages that work together to provide a seamless development experience.

### Core Components

- **`isaacscript` (CLI)**: The entry point for developers. It handles project initialization, automatic mod syncing, and the build pipeline. [packages/isaacscript-cli/package.json2-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L2-L27)
- **`isaacscript-common`**: A standard library providing high-level wrappers for the vanilla API, custom callbacks, and utility functions. [packages/isaacscript-common/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L2-L4)
- **`isaac-typescript-definitions`**: Comprehensive TypeScript interfaces for the Isaac Lua API, including community-added definitions and REPENTOGON support. [packages/isaac-typescript-definitions/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L2-L4)
- **`isaacscript-lint`**: A meta-package that bundles ESLint, Prettier, and custom rules to enforce best practices. [packages/isaacscript-lint/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json#L2-L4)

### Bridge: Natural Language to Code Entities

This diagram maps conceptual modding tasks to the specific code entities and packages that handle them.

```
Code Entity Space

Natural Language Space

Uses

Defined in

Exports

Rules in

'I want to create a new mod project'

'I want to use high-level helpers like spawn() or getPlayers()'

'I want autocomplete for the Isaac API'

'I want to catch bugs before running the game'

'isaacscript init' (CLI)

'isaacscript-common' (Library)

'isaac-typescript-definitions' (Types)

'eslint-plugin-isaacscript' (Linter)

packages/isaacscript-cli/src/main.ts

packages/isaacscript-common/src/index.ts

packages/isaac-typescript-definitions/dist/index.d.ts

packages/eslint-plugin-isaacscript/src/index.js
```

Sources: [packages/isaacscript-cli/package.json25-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L25-L27) [packages/isaacscript-common/package.json25-26](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L25-L26) [packages/isaac-typescript-definitions/package.json22-23](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L22-L23) [packages/eslint-plugin-isaacscript/package.json33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json#L33-L33)

## Project Architecture

The monorepo structure allows for shared logic across tools while maintaining clear boundaries between the compiler, the library, and the documentation.

### Package Dependency Flow

The following diagram illustrates how the various packages depend on one another.

```
Base Layer

Logic Layer

Tooling Layer

isaacscript (CLI)

isaacscript-lint

isaacscript-common

isaac-typescript-definitions

isaac-lua-polyfill
```

Sources: [packages/isaacscript-common/package.json36-38](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L36-L38) [packages/isaacscript-lint/package.json23-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json#L23-L31) [packages/isaac-lua-polyfill/package.json30-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/package.json#L30-L33)

## Detailed Sections

### [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)

This section covers the installation of the environment (Node.js, VS Code) and the use of the `isaacscript init` command. It explains how the CLI scaffolds a new project from `file-templates` and how the `monitor` command orchestrates the development loop.

- **Key Files**: `packages/isaacscript-cli/file-templates/`, `packages/isaacscript-cli/src/commands/init.ts`

### [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)

A deep dive into the `packages/` directory. It explains the tiered dependency system and how workspace scripts in the root `package.json` (like `lint-all` and `publish`) manage the entire repository.

- **Key Files**: `package.json:16-23](),`scripts/lint-all.ts\`

### [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))

While designed for TypeScript, the logic in `isaacscript-common` is available to pure Lua modders. This section documents the `isaacscript-lua` Python tool and how to consume the bundled Lua library.

- **Key Files**: `packages/isaacscript-lua/isaacscript_lua.py`

## Summary Table

| Package | Purpose | Primary Language |
| --- | --- | --- |
| `isaacscript` | CLI tool for mod lifecycle | TypeScript (Node.js) |
| `isaacscript-common` | Standard library for mods | TypeScript (TSTL) |
| `isaac-typescript-definitions` | Isaac API Typings | TypeScript |
| `eslint-plugin-isaacscript` | Custom lint rules for Isaac | JavaScript |
| `docs` | Docusaurus-based documentation | TypeScript (React) |

Sources: [packages/isaacscript-cli/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L4-L4) [packages/isaacscript-common/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L4-L4) [packages/isaac-typescript-definitions/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L4-L4) [packages/eslint-plugin-isaacscript/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json#L4-L4) [package.json29-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L29-L33)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript#isaacscript-overview)
- [High-Level Ecosystem](https://deepwiki.com/IsaacScript/isaacscript#high-level-ecosystem)
- [Core Components](https://deepwiki.com/IsaacScript/isaacscript#core-components)
- [Bridge: Natural Language to Code Entities](https://deepwiki.com/IsaacScript/isaacscript#bridge-natural-language-to-code-entities)
- [Project Architecture](https://deepwiki.com/IsaacScript/isaacscript#project-architecture)
- [Package Dependency Flow](https://deepwiki.com/IsaacScript/isaacscript#package-dependency-flow)
- [Detailed Sections](https://deepwiki.com/IsaacScript/isaacscript#detailed-sections)
- [\[Getting Started & Project Setup\](#1.1)](https://deepwiki.com/IsaacScript/isaacscript#getting-started-project-setup11)
- [\[Monorepo Architecture & Package Dependency Graph\](#1.2)](https://deepwiki.com/IsaacScript/isaacscript#monorepo-architecture-package-dependency-graph12)
- [\[Using IsaacScript in Lua (Without TypeScript)\](#1.3)](https://deepwiki.com/IsaacScript/isaacscript#using-isaacscript-in-lua-without-typescript13)
- [Summary Table](https://deepwiki.com/IsaacScript/isaacscript#summary-table)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 1 Isaacscript Overview

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# IsaacScript Overview

Relevant source files

- [package-lock.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package-lock.json)
- [package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json)
- [packages/docs/docs/main/change-log.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/change-log.md?plain=1)
- [packages/docs/docs/main/features.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/features.md?plain=1)
- [packages/docs/docs/main/getting-started.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1)
- [packages/docs/docs/main/isaacscript-in-typescript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-typescript.md?plain=1)
- [packages/docs/docusaurus.config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docusaurus.config.ts)
- [packages/docs/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/package.json)
- [packages/docs/sidebars.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/sidebars.ts)
- [packages/docs/src/css/custom.css](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/src/css/custom.css)
- [packages/docs/static/img/lua.png](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/static/img/lua.png)
- [packages/docs/static/img/typescript.png](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/static/img/typescript.png)
- [packages/eslint-config-isaacscript/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/package.json)
- [packages/eslint-plugin-isaacscript/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json)
- [packages/isaac-lua-polyfill/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/package.json)
- [packages/isaac-typescript-definitions-repentogon/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/package.json)
- [packages/isaac-typescript-definitions/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json)
- [packages/isaacscript-cli/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json)
- [packages/isaacscript-common/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json)
- [packages/isaacscript-common/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/index.ts)
- [packages/isaacscript-lint/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json)
- [packages/isaacscript-lua/isaacscript\_lua.py](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py)
- [packages/isaacscript-lua/publish.sh](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/publish.sh)
- [packages/isaacscript-lua/pyproject.toml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/pyproject.toml)
- [packages/isaacscript-spell/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/package.json)
- [todo.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/todo.txt)

IsaacScript is a comprehensive monorepo and framework designed to modernize modding for _The Binding of Isaac: Repentance_. It enables developers to write mods in TypeScript, which are then transpiled to Lua using [TypeScript-to-Lua (TSTL)](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/TypeScript-to-Lua%20(TSTL))

The project provides a complete ecosystem including a CLI for project management, a robust standard library (`isaacscript-common`), high-quality type definitions for the game API, and a strict linting stack to ensure code quality.

## High-Level Ecosystem

The IsaacScript monorepo is organized into several specialized packages that work together to provide a seamless development experience.

### Core Components

- **`isaacscript` (CLI)**: The entry point for developers. It handles project initialization, automatic mod syncing, and the build pipeline. [packages/isaacscript-cli/package.json2-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L2-L27)
- **`isaacscript-common`**: A standard library providing high-level wrappers for the vanilla API, custom callbacks, and utility functions. [packages/isaacscript-common/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L2-L4)
- **`isaac-typescript-definitions`**: Comprehensive TypeScript interfaces for the Isaac Lua API, including community-added definitions and REPENTOGON support. [packages/isaac-typescript-definitions/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L2-L4)
- **`isaacscript-lint`**: A meta-package that bundles ESLint, Prettier, and custom rules to enforce best practices. [packages/isaacscript-lint/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json#L2-L4)

### Bridge: Natural Language to Code Entities

This diagram maps conceptual modding tasks to the specific code entities and packages that handle them.

```
Code Entity Space

Natural Language Space

Uses

Defined in

Exports

Rules in

'I want to create a new mod project'

'I want to use high-level helpers like spawn() or getPlayers()'

'I want autocomplete for the Isaac API'

'I want to catch bugs before running the game'

'isaacscript init' (CLI)

'isaacscript-common' (Library)

'isaac-typescript-definitions' (Types)

'eslint-plugin-isaacscript' (Linter)

packages/isaacscript-cli/src/main.ts

packages/isaacscript-common/src/index.ts

packages/isaac-typescript-definitions/dist/index.d.ts

packages/eslint-plugin-isaacscript/src/index.js
```

Sources: [packages/isaacscript-cli/package.json25-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L25-L27) [packages/isaacscript-common/package.json25-26](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L25-L26) [packages/isaac-typescript-definitions/package.json22-23](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L22-L23) [packages/eslint-plugin-isaacscript/package.json33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json#L33-L33)

## Project Architecture

The monorepo structure allows for shared logic across tools while maintaining clear boundaries between the compiler, the library, and the documentation.

### Package Dependency Flow

The following diagram illustrates how the various packages depend on one another.

```
Base Layer

Logic Layer

Tooling Layer

isaacscript (CLI)

isaacscript-lint

isaacscript-common

isaac-typescript-definitions

isaac-lua-polyfill
```

Sources: [packages/isaacscript-common/package.json36-38](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L36-L38) [packages/isaacscript-lint/package.json23-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json#L23-L31) [packages/isaac-lua-polyfill/package.json30-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/package.json#L30-L33)

## Detailed Sections

### [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)

This section covers the installation of the environment (Node.js, VS Code) and the use of the `isaacscript init` command. It explains how the CLI scaffolds a new project from `file-templates` and how the `monitor` command orchestrates the development loop.

- **Key Files**: `packages/isaacscript-cli/file-templates/`, `packages/isaacscript-cli/src/commands/init.ts`

### [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)

A deep dive into the `packages/` directory. It explains the tiered dependency system and how workspace scripts in the root `package.json` (like `lint-all` and `publish`) manage the entire repository.

- **Key Files**: `package.json:16-23](),`scripts/lint-all.ts\`

### [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))

While designed for TypeScript, the logic in `isaacscript-common` is available to pure Lua modders. This section documents the `isaacscript-lua` Python tool and how to consume the bundled Lua library.

- **Key Files**: `packages/isaacscript-lua/isaacscript_lua.py`

## Summary Table

| Package | Purpose | Primary Language |
| --- | --- | --- |
| `isaacscript` | CLI tool for mod lifecycle | TypeScript (Node.js) |
| `isaacscript-common` | Standard library for mods | TypeScript (TSTL) |
| `isaac-typescript-definitions` | Isaac API Typings | TypeScript |
| `eslint-plugin-isaacscript` | Custom lint rules for Isaac | JavaScript |
| `docs` | Docusaurus-based documentation | TypeScript (React) |

Sources: [packages/isaacscript-cli/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L4-L4) [packages/isaacscript-common/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L4-L4) [packages/isaac-typescript-definitions/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L4-L4) [packages/eslint-plugin-isaacscript/package.json4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json#L4-L4) [package.json29-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L29-L33)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#isaacscript-overview)
- [High-Level Ecosystem](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#high-level-ecosystem)
- [Core Components](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#core-components)
- [Bridge: Natural Language to Code Entities](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#bridge-natural-language-to-code-entities)
- [Project Architecture](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#project-architecture)
- [Package Dependency Flow](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#package-dependency-flow)
- [Detailed Sections](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#detailed-sections)
- [\[Getting Started & Project Setup\](#1.1)](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#getting-started-project-setup11)
- [\[Monorepo Architecture & Package Dependency Graph\](#1.2)](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#monorepo-architecture-package-dependency-graph12)
- [\[Using IsaacScript in Lua (Without TypeScript)\](#1.3)](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#using-isaacscript-in-lua-without-typescript13)
- [Summary Table](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview#summary-table)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 1.1 Getting Started And Project Setup

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Getting Started & Project Setup

Relevant source files

- [.vscode/extensions.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.vscode/extensions.json)
- [.vscode/settings.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.vscode/settings.json)
- [packages/docs/docs/main/converting-lua-code.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/converting-lua-code.md?plain=1)
- [packages/docs/docs/main/directory-structure.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/directory-structure.md?plain=1)
- [packages/docs/docs/main/getting-started.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1)
- [packages/docs/docs/main/isaacscript-in-typescript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-typescript.md?plain=1)
- [packages/docs/docs/main/publishing-to-the-workshop.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/publishing-to-the-workshop.md?plain=1)
- [packages/docs/docs/main/updating-isaacscript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/updating-isaacscript.md?plain=1)
- [packages/docs/docusaurus.config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docusaurus.config.ts)
- [packages/docs/sidebars.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/sidebars.ts)
- [packages/eslint-plugin-isaacscript/scripts/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/utils.ts)
- [packages/isaac-typescript-definitions/src/enums/Controller.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/Controller.ts)
- [packages/isaac-typescript-definitions/src/enums/RoomShape.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/RoomShape.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Level.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Level.d.ts)
- [packages/isaacscript-cli/custom-stage/shaders.xml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/custom-stage/shaders.xml)
- [packages/isaacscript-cli/file-templates/static/.vscode/extensions.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.vscode/extensions.json)
- [packages/isaacscript-cli/file-templates/static/.vscode/settings.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.vscode/settings.json)
- [packages/isaacscript-cli/file-templates/static/scripts/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/scripts/tsconfig.json)
- [packages/isaacscript-cli/src/banner.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/banner.ts)
- [packages/isaacscript-cli/src/commands/check/check.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts)
- [packages/isaacscript-cli/src/commands/copy/copy.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/copy/copy.ts)
- [packages/isaacscript-cli/src/commands/init/createProject.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts)
- [packages/isaacscript-cli/src/commands/init/getProjectPath.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/getProjectPath.ts)
- [packages/isaacscript-cli/src/commands/init/init.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts)
- [packages/isaacscript-cli/src/commands/monitor/monitor.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts)
- [packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts)
- [packages/isaacscript-cli/src/commands/publish/publish.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts)
- [packages/isaacscript-cli/src/configFile.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/configFile.ts)
- [packages/isaacscript-cli/src/constants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts)
- [packages/isaacscript-cli/src/customStage.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts)
- [packages/isaacscript-cli/src/enums/copied/RoomShape.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/enums/copied/RoomShape.ts)
- [packages/isaacscript-cli/src/exec.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/exec.ts)
- [packages/isaacscript-cli/src/git.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts)
- [packages/isaacscript-cli/src/main.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/main.ts)
- [packages/isaacscript-cli/src/packageManager.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/packageManager.ts)
- [packages/isaacscript-cli/src/parseArgs.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts)
- [packages/isaacscript-cli/src/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/utils.ts)
- [packages/isaacscript-cli/src/validateMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/validateMod.ts)
- [packages/isaacscript-cli/src/validateNodeVersion.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/validateNodeVersion.ts)
- [packages/isaacscript-lua/isaacscript\_lua.py](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py)
- [packages/isaacscript-lua/publish.sh](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/publish.sh)
- [packages/isaacscript-lua/pyproject.toml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/pyproject.toml)
- [packages/isaacscript-spell/dictionaries/isaacscript/isaacscript.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaacscript/isaacscript.txt)
- [prettier.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/prettier.config.mjs)

This page provides a technical guide for setting up an IsaacScript development environment and initializing a new mod project. It covers the system requirements, the scaffolding process performed by the CLI, and the resulting project architecture.

## System Requirements & Installation

IsaacScript requires a modern Node.js environment and a configured code editor to ensure type safety and automatic transpilation.

1. **Node.js**: IsaacScript requires Node.js to run the CLI and the TypeScript-to-Lua (TSTL) compiler. The version is validated at runtime via `validateNodeVersion` [packages/isaacscript-cli/src/main.ts13](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/main.ts#L13-L13)
2. **Visual Studio Code**: The recommended IDE. The project templates include an `extensions.json` file that recommends the ESLint, Prettier, and TypeScriptToLua extensions [packages/isaacscript-cli/file-templates/static/.vscode/extensions.json4-9](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.vscode/extensions.json#L4-L9)
3. **Package Manager**: The CLI supports `npm`, `yarn`, and `pnpm`. The user's choice is detected or prompted during initialization [packages/isaacscript-cli/src/packageManager.ts1-21](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/packageManager.ts#L1-L21)

## Project Initialization (`isaacscript init`)

The `init` command is the entry point for creating a new mod. It is defined in `packages/isaacscript-cli/src/commands/init/init.ts` and orchestrates several validation and scaffolding steps.

### Initialization Workflow

The following diagram illustrates the data flow and function calls during the `init` process:

**Project Initialization Logic**

```
Code Entities

initCommand.action

getPackageManagerUsedForNewProject

getProjectPath

getModsDirectory

getSaveSlot

createProject

createConfigFile (isaacscript.json)

copyStaticFiles

copyDynamicFiles

installNodeModules

initGitRepository

vsCodeInit
```

Sources: [packages/isaacscript-cli/src/commands/init/init.ts98-159](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts#L98-L159) [packages/isaacscript-cli/src/commands/init/createProject.ts43-80](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L43-L80)

### Scaffolding Mechanics

The `createProject` function performs the actual file operations:

- **Configuration**: Creates `isaacscript.json` using the `Config` class [packages/isaacscript-cli/src/commands/init/createProject.ts59-60](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L59-L60)
- **Static Templates**: Copies non-changing files like `tsconfig.json` and `.vscode/settings.json` from `TEMPLATES_STATIC_DIR` [packages/isaacscript-cli/src/commands/init/createProject.ts83-88](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L83-L88)
- **Dynamic Templates**: Processes files that require string replacement (e.g., `package.json`, `README.md`, and GitHub Actions workflows) from `TEMPLATES_DYNAMIC_DIR` [packages/isaacscript-cli/src/commands/init/createProject.ts121-205](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L121-L205)
- **Dependency Management**: Runs `updatePackageJSONDependencies` to ensure the latest versions of `isaacscript-common` and type definitions are used [packages/isaacscript-cli/src/commands/init/createProject.ts66](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L66-L66)

## Project Structure

A generated IsaacScript project follows a specific layout to separate source TypeScript from the transpiled Lua assets required by the game.

| Path | Purpose |
| --- | --- |
| `src/` | Contains the TypeScript source code. `main.ts` is the entry point [packages/isaacscript-cli/src/constants.ts69-74](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L69-L74) |
| `mod/` | The "Source Mod Directory". Contains `metadata.xml` and static resources (GFX, rooms) [packages/isaacscript-cli/src/constants.ts105-108](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L105-L108) |
| `isaacscript.json` | Project configuration, including the path to the Isaac mods folder and the target save slot [packages/isaacscript-cli/src/constants.ts98-99](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L98-L99) |
| `tsconfig.json` | TypeScript configuration that extends `isaacscript-tsconfig` [packages/isaacscript-cli/src/constants.ts100-101](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L100-L101) |
| `.vscode/` | Editor settings for consistent linting and formatting [packages/isaacscript-cli/file-templates/static/.vscode/settings.json1-146](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.vscode/settings.json#L1-L146) |

## Development Loop (`isaacscript monitor`)

Once initialized, the `monitor` command starts the development lifecycle. It is the default command for the CLI [packages/isaacscript-cli/src/parseArgs.ts48](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts#L48-L48)

### Subprocess Orchestration

The `monitor` function [packages/isaacscript-cli/src/commands/monitor/monitor.ts54](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L54-L54) spawns four critical background tasks:

1. **`spawnSaveDatWriter`**: Monitors the `save#.dat` file to prevent the game from overwriting mod data during development [packages/isaacscript-cli/src/commands/monitor/monitor.ts98](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L98-L98)
2. **`spawnModDirectorySyncer`**: Watches the `mod/` source folder and syncs assets (XML, PNG) to the actual game directory [packages/isaacscript-cli/src/commands/monitor/monitor.ts101](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L101-L101)
3. **`spawnTSTLWatcher`**: Runs `tstl --watch` to transpile `.ts` files in `src/` into `.lua` files in the target mod directory [packages/isaacscript-cli/src/commands/monitor/monitor.ts104](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L104-L104)
4. **Game Pinger**: Calls `notifyGamePing` every 1000ms to communicate with the `isaacscript-watcher` Lua mod for hot-reloading [packages/isaacscript-cli/src/commands/monitor/monitor.ts129-131](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L129-L131)

**Monitor Execution Flow**

```
Subprocesses & Tasks

isaacscript monitor

validateInIsaacScriptProject

getConfigFromFile

copyWatcherMod

spawnSaveDatWriter

spawnModDirectorySyncer

spawnTSTLWatcher

notifyGamePing (Interval)
```

Sources: [packages/isaacscript-cli/src/commands/monitor/monitor.ts54-132](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L54-L132)

## Template Integrity (`isaacscript check`)

To prevent projects from falling behind the standard IsaacScript configuration, the `check` command compares local project files against the latest templates [packages/isaacscript-cli/src/commands/check/check.ts42-46](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L42-L46)

It uses customization markers to allow users to modify certain parts of template files without triggering errors:

- `@template-customization-start` / `@template-customization-end`: Blocks that are ignored during comparison [packages/isaacscript-cli/src/commands/check/check.ts28-29](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L28-L29)
- `@template-ignore-next-line`: Skips the subsequent line [packages/isaacscript-cli/src/commands/check/check.ts32](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L32-L32)

Sources: [packages/isaacscript-cli/src/commands/check/check.ts28-32](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L28-L32) [packages/isaacscript-cli/src/commands/check/check.ts201-211](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L201-L211)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#getting-started-project-setup)
- [System Requirements & Installation](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#system-requirements-installation)
- [Project Initialization (\`isaacscript init\`)](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#project-initialization-isaacscript-init)
- [Initialization Workflow](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#initialization-workflow)
- [Scaffolding Mechanics](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#scaffolding-mechanics)
- [Project Structure](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#project-structure)
- [Development Loop (\`isaacscript monitor\`)](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#development-loop-isaacscript-monitor)
- [Subprocess Orchestration](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#subprocess-orchestration)
- [Template Integrity (\`isaacscript check\`)](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup#template-integrity-isaacscript-check)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 1.2 Monorepo Architecture And Package Dependency Graph

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Monorepo Architecture & Package Dependency Graph

Relevant source files

- [.github/workflows/ci.yml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml)
- [.github/workflows/setup/action.yml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/setup/action.yml)
- [knip.config.js](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/knip.config.js)
- [package-lock.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package-lock.json)
- [package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json)
- [packages/docs/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/package.json)
- [packages/docs/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/build.mts)
- [packages/docs/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/lint.mts)
- [packages/eslint-config-isaacscript/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/package.json)
- [packages/eslint-config-isaacscript/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/scripts/lint.ts)
- [packages/eslint-plugin-isaacscript/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json)
- [packages/eslint-plugin-isaacscript/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/lint.ts)
- [packages/isaac-lua-polyfill/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/package.json)
- [packages/isaac-lua-polyfill/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/scripts/lint.ts)
- [packages/isaac-typescript-definitions-repentogon/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/package.json)
- [packages/isaac-typescript-definitions-repentogon/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/scripts/build.mts)
- [packages/isaac-typescript-definitions-repentogon/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/scripts/lint.mts)
- [packages/isaac-typescript-definitions/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json)
- [packages/isaac-typescript-definitions/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/scripts/build.mts)
- [packages/isaac-typescript-definitions/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/scripts/lint.mts)
- [packages/isaacscript-cli/file-templates/dynamic/.github/workflows/setup/action.yml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/.github/workflows/setup/action.yml)
- [packages/isaacscript-cli/file-templates/static/.github/workflows/ci.yml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.github/workflows/ci.yml)
- [packages/isaacscript-cli/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json)
- [packages/isaacscript-cli/schemas/isaacscript-schema.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/schemas/isaacscript-schema.json)
- [packages/isaacscript-cli/scripts/build.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/build.ts)
- [packages/isaacscript-cli/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/lint.ts)
- [packages/isaacscript-cli/src/classes/Config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/classes/Config.ts)
- [packages/isaacscript-common/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json)
- [packages/isaacscript-common/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/scripts/build.mts)
- [packages/isaacscript-common/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/scripts/lint.mts)
- [packages/isaacscript-lint/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json)
- [packages/isaacscript-spell/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/package.json)
- [packages/isaacscript-spell/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/scripts/lint.ts)
- [scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/scripts/lint.ts)
- [scripts/publish.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/scripts/publish.ts)
- [scripts/update.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/scripts/update.ts)

The IsaacScript project is managed as a monorepo, containing all the core libraries, CLI tools, type definitions, and documentation in a single repository. This architecture ensures that changes to the core API definitions are immediately reflected in the standard library and the CLI, maintaining strict type safety across the entire ecosystem.

## Monorepo Layout

The repository uses npm workspaces to manage multiple packages under the `packages/` directory. Each package is a self-contained unit with its own `package.json`, but they share a root `package-lock.json` and node\_modules for efficient dependency management [package.json1-91](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L1-L91)

### Package Tiers

The monorepo is structured into four distinct tiers based on their role in the ecosystem:

1. **Base Definitions (Tier 0):** Pure type definitions for the Isaac Lua API.
2. **Logic & Polyfills (Tier 1):** Shared logic and Lua-compatible helper libraries.
3. **Tooling & Quality (Tier 2):** CLI, linters, and build-time plugins.
4. **Documentation (Tier 3):** The user-facing Docusaurus site.

### Core Package Registry

| Package Name | Path | Description |
| --- | --- | --- |
| `isaac-typescript-definitions` | `packages/isaac-typescript-definitions` | The primary TS definitions for the Repentance API [packages/isaac-typescript-definitions/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L2-L4) |
| `isaac-typescript-definitions-repentogon` | `packages/isaac-typescript-definitions-repentogon` | Extensions for the REPENTOGON exe-hack [packages/isaac-typescript-definitions-repentogon/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/package.json#L2-L4) |
| `isaacscript-common` | `packages/isaacscript-common` | The standard library (ISC) used by mod authors [packages/isaacscript-common/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L2-L4) |
| `isaacscript` (CLI) | `packages/isaacscript-cli` | The command-line tool for mod management [packages/isaacscript-cli/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L2-L4) |
| `isaac-lua-polyfill` | `packages/isaac-lua-polyfill` | Lua implementations of JS-like features [packages/isaac-lua-polyfill/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/package.json#L2-L4) |
| `eslint-plugin-isaacscript` | `packages/eslint-plugin-isaacscript` | Custom ESLint rules for Isaac modding [packages/eslint-plugin-isaacscript/package.json2-4](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/package.json#L2-L4) |

**Sources:** [package.json1-24](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L1-L24) [packages/isaacscript-common/package.json1-46](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L1-L46) [packages/isaacscript-cli/package.json1-78](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L1-L78)

* * *

## Package Dependency Graph

The following diagram illustrates the internal dependencies within the monorepo. IsaacScript follows a strict "bottom-up" dependency flow to prevent circular references.

### Internal Dependency Flow

```
Tier 0: Base Definitions

Tier 1: Logic & Polyfills

Tier 2: Tooling & Linting

Tier 3: Docs

packages/docs

isaacscript (CLI)

isaacscript-lint

eslint-config-isaacscript

eslint-plugin-isaacscript

isaacscript-spell

isaacscript-tsconfig

isaacscript-common

isaac-lua-polyfill

isaac-typescript-definitions

isaac-typescript-definitions-repentogon
```

### Dependency Logic

- **Base Definitions:** Packages like `isaac-typescript-definitions` have zero internal dependencies, relying only on `lua-types` [packages/isaac-typescript-definitions/package.json33-35](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L33-L35)
- **Standard Library:**`isaacscript-common` depends on the base definitions to provide typed helper functions [packages/isaacscript-common/package.json36-38](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L36-L38)
- **CLI Orchestration:** The CLI (`isaacscript`) manages the build process and templates, but remains decoupled from the runtime logic of `isaacscript-common` to keep the toolchain lightweight [packages/isaacscript-cli/package.json42-59](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L42-L59)

**Sources:** [packages/isaac-typescript-definitions/package.json33-35](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/package.json#L33-L35) [packages/isaacscript-common/package.json36-38](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L36-L38) [packages/isaacscript-cli/package.json42-59](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L42-L59) [packages/isaacscript-lint/package.json23-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/package.json#L23-L31)

* * *

## Workspace Scripts & Orchestration

The monorepo uses a set of root-level TypeScript scripts (run via `tsx`) to orchestrate tasks across all packages.

### Key Management Scripts

- **`npm run lint-all`**: Executes the `lint.ts` script in every package [package.json19](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L19-L19)
- **`npm run publish`**: A specialized script that handles version bumping and NPM publishing for the entire suite [package.json21](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L21-L21)
- **`npm run update`**: Synchronizes dependency versions across all `package.json` files in the monorepo [package.json22](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L22-L22)

### Build Pipeline Association

The following diagram maps the high-level commands to the underlying implementation scripts and packages.

```
Package Layer

Implementation Layer

npm run lint-all

npm run publish

npm run update

User/CI Command

Root Scripts (./scripts/)

lint-all.ts

publish.ts

update.ts

packages/isaacscript-cli/scripts/lint.ts

packages/isaacscript-common/scripts/lint.mts

packages/isaac-typescript-definitions/scripts/lint.mts

packages/*/scripts/build.ts
```

**Sources:** [package.json16-23](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L16-L23) [packages/isaacscript-cli/package.json36-41](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/package.json#L36-L41) [packages/isaacscript-common/package.json31-35](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/package.json#L31-L35)

* * *

## CI Pipeline & GitHub Actions

The IsaacScript monorepo uses a dynamic CI pipeline defined in `.github/workflows/ci.yml`. Instead of hardcoding package names, it uses a matrix strategy to scale with the repository.

### CI Job Matrix Strategy

1. **Discovery:** The `get-build-packages` job uses `complete-ts/get-package-names` to find all packages with a `build` script [ci.yml6-16](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/ci.yml#L6-L16)
2. **Parallel Execution:** The `build`, `lint`, and `test` jobs run in parallel for every discovered package [ci.yml17-87](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/ci.yml#L17-L87)
3. **Artifact Handling:** If the `docs` package is being built, the resulting Docusaurus site is uploaded as a `docs-build` artifact [ci.yml29-34](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/ci.yml#L29-L34)
4. **Notifications:** On failure, a Discord notification is sent via a webhook [ci.yml176-187](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/ci.yml#L176-L187)

### Pipeline Visualization

```
Discord WebhookPackage Job (Node 20)Matrix DiscoveryGitHub ActionsDiscord WebhookPackage Job (Node 20)Matrix DiscoveryGitHub Actionsloop[Per Package]Pipeline Completealt[Job Fails][Job Succeeds]Run get-build-packages["isaacscript", "isaacscript-common", ...]Run npm run buildRun npm run lintRun npm run testSend failure notification
```

**Sources:** [.github/workflows/ci.yml1-187](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L1-L187) [package.json17-23](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/package.json#L17-L23)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#monorepo-architecture-package-dependency-graph)
- [Monorepo Layout](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#monorepo-layout)
- [Package Tiers](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#package-tiers)
- [Core Package Registry](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#core-package-registry)
- [Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#package-dependency-graph)
- [Internal Dependency Flow](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#internal-dependency-flow)
- [Dependency Logic](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#dependency-logic)
- [Workspace Scripts & Orchestration](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#workspace-scripts-orchestration)
- [Key Management Scripts](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#key-management-scripts)
- [Build Pipeline Association](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#build-pipeline-association)
- [CI Pipeline & GitHub Actions](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#ci-pipeline-github-actions)
- [CI Job Matrix Strategy](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#ci-job-matrix-strategy)
- [Pipeline Visualization](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph#pipeline-visualization)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 1.3 Using Isaacscript In Lua (Without Typescript)

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Using IsaacScript in Lua (Without TypeScript)

Relevant source files

- [packages/docs/docs/main/isaacscript-in-lua.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1)
- [packages/eslint-config-isaacscript/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/README.md?plain=1)
- [packages/isaac-lua-polyfill/LICENSE](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/LICENSE)
- [packages/isaac-lua-polyfill/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/README.md?plain=1)
- [packages/isaac-lua-polyfill/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/src/index.ts)
- [packages/isaac-typescript-definitions-repentogon/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/README.md?plain=1)
- [packages/isaac-typescript-definitions/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/README.md?plain=1)
- [packages/isaacscript-cli/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/README.md?plain=1)
- [packages/isaacscript-cli/file-templates/dynamic/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/package.json)
- [packages/isaacscript-cli/file-templates/static/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/scripts/lint.ts)
- [packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts)
- [packages/isaacscript-cli/file-templates/static/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json)
- [packages/isaacscript-common/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/README.md?plain=1)
- [packages/isaacscript-common/src/functions/ambush.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/ambush.ts)
- [packages/isaacscript-common/website-root.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/website-root.md?plain=1)
- [packages/isaacscript-lint/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1)
- [packages/isaacscript-lua/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1)
- [packages/isaacscript-spell/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/README.md?plain=1)

This page documents how pure-Lua mod authors can consume the IsaacScript framework's power without switching their entire development environment to TypeScript. By using a bundled version of the library, Lua authors gain access to thousands of helper functions and corrected game enums.

## Overview

The IsaacScript framework provides two primary libraries for _The Binding of Isaac: Repentance_ development:

1. `isaac-typescript-definitions`: A corrected version of the vanilla enums and classes, fixing numerous bugs and missing entries in the official API [packages/docs/docs/main/isaacscript-in-lua.md11](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L11-L11)
2. `isaacscript-common`: An extensive standard library of helper functions that abstract away complex Isaac API tasks [packages/docs/docs/main/isaacscript-in-lua.md12](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L12-L12)

For Lua users, these two packages are combined into a single bundled file: `isaacscript-common.lua` [packages/docs/docs/main/isaacscript-in-lua.md18](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L18-L18)

### Data Flow and Distribution

The following diagram illustrates how the TypeScript-based libraries are transformed into a single Lua asset for consumption in a standard Lua mod.

**Library Distribution Pipeline**

```
User Mod (Lua)

Distribution

Build Process

Source Space (TypeScript)

Download

Install/Upgrade

require()

isaac-typescript-definitions

isaacscript-common (TS)

TypeScript-to-Lua Compiler

Bundler

NPM Registry (unpkg)

isaacscript-lua (Python Tool)

lib/isaacscript-common.lua

main.lua
```

**Sources:** [packages/docs/docs/main/isaacscript-in-lua.md16-18](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L16-L18) [packages/isaacscript-lua/README.md1-28](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1#L1-L28)

* * *

## Installation Methods

### 1\. Automatic Installation (isaacscript-lua)

The recommended way to manage the library is via the `isaacscript-lua` Python tool. This tool automates the downloading and updating of the library file [packages/isaacscript-lua/README.md1-3](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1#L1-L3)

**Commands:**

- **Install Tool:**`python -m pip install isaacscript-lua --upgrade` [packages/isaacscript-lua/README.md12](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1#L12-L12)
- **Install Library:**`isaacscript-lua install` (Run inside your mod directory) [packages/isaacscript-lua/README.md19](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1#L19-L19)
- **Update Library:**`isaacscript-lua upgrade` [packages/isaacscript-lua/README.md26](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1#L26-L26)

### 2\. Manual Installation

If Python is not available, the library can be installed manually by downloading the latest bundle from the NPM registry [packages/docs/docs/main/isaacscript-in-lua.md40](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L40-L40)

**File Structure Requirement:**
To prevent namespace conflicts in the Isaac environment, the library must be placed in a specific directory structure [packages/docs/docs/main/isaacscript-in-lua.md50-55](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L50-L55)

```
my-mod/
├── main.lua
├── metadata.xml
└── my-mod/             <-- Namespaced directory (matches mod folder name)
    └── lib/
        └── isaacscript-common.lua
```

**Sources:** [packages/docs/docs/main/isaacscript-in-lua.md59-66](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L59-L66) [packages/isaacscript-lua/README.md1-28](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1#L1-L28)

* * *

## Usage in Lua

### Importing

To use the library, it must be required in every Lua file where its functions are needed. The period `.` is used as a directory separator [packages/docs/docs/main/isaacscript-in-lua.md79-86](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L79-L86)

```
-- Replace "my-mod" with your actual mod directory name
local isc = require("my-mod.lib.isaacscript-common")
```

### Pure Functions vs. State-Based Features

The library functions are categorized into two types:

| Type | Description | Usage Requirement |
| --- | --- | --- |
| **Pure Functions** | Helper functions with no side effects (e.g., `anyPlayerHasCollectible`). | Can be used immediately after `require`. |
| **State-Based Features** | Features requiring game state tracking (e.g., `Custom Callbacks`, `Save Data Manager`). | Requires calling `upgradeMod`. |

**Sources:** [packages/docs/docs/main/isaacscript-in-lua.md89-104](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L89-L104) [packages/isaacscript-common/website-root.md19-35](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/website-root.md?plain=1#L19-L35)

### Code Integration Example

The following diagram maps the natural language concepts of "Upgrading a Mod" to the specific Lua code entities required to enable advanced features.

**Mod Upgrading Logic**

```
Code Entity Space (Lua)

Natural Language

Returns upgraded mod

Vanilla Mod Object

Enable Custom Callbacks

Enable Specific Features

RegisterMod()

isc:upgradeMod(vanillaMod, features)

isc.ISCFeature

ModCallbackCustom
```

**Sources:** [packages/docs/docs/main/isaacscript-in-lua.md130-140](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L130-L140) [packages/isaacscript-common/website-root.md35-60](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/website-root.md?plain=1#L35-L60)

### Corrected Enums

One of the primary benefits for Lua users is access to corrected enums. Vanilla enums are often incomplete or can be modified/deleted by other mods. IsaacScript enums are local to the library and safer [packages/docs/docs/main/isaacscript-in-lua.md126-127](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L126-L127)

```
-- Using a corrected enum from the library
if entity.Type == isc.EntityType.GAPER and entity.Variant == isc.GaperVariant.FLAMING_GAPER then
  -- Logic here
end
```

**Sources:** [packages/docs/docs/main/isaacscript-in-lua.md113-124](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L113-L124)

* * *

## Advanced Features: `upgradeMod`

To use stateful features like `ModCallbackCustom` or the `SaveDataManager`, you must "upgrade" your mod object. This process injects the library's logic into your mod's lifecycle [packages/isaacscript-common/website-root.md35-44](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/website-root.md?plain=1#L35-L44)

### Enabling Features

To keep performance high, features are opt-in. You pass a list of `ISCFeature` enums to the `upgradeMod` function [packages/isaacscript-common/website-root.md68-78](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/website-root.md?plain=1#L68-L78)

```
local isc = require("my-mod.lib.isaacscript-common")

local modVanilla = RegisterMod("MyMod", 1)
-- Opt-in to specific features like Pony Detection
local features = { isc.ISCFeature.PONY_DETECTION }
local mod = isc:upgradeMod(modVanilla, features)

-- Now custom callbacks and feature-specific methods are available
mod:AddCallbackCustom(isc.ModCallbackCustom.POST_ITEM_PICKUP, function(player, item)
    -- ...
end)
```

**Sources:** [packages/isaacscript-common/website-root.md73-84](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/website-root.md?plain=1#L73-L84) [packages/docs/docs/main/isaacscript-in-lua.md130-140](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1#L130-L140)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#using-isaacscript-in-lua-without-typescript)
- [Overview](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#overview)
- [Data Flow and Distribution](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#data-flow-and-distribution)
- [Installation Methods](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#installation-methods)
- [1\. Automatic Installation (isaacscript-lua)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#1-automatic-installation-isaacscript-lua)
- [2\. Manual Installation](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#2-manual-installation)
- [Usage in Lua](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#usage-in-lua)
- [Importing](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#importing)
- [Pure Functions vs. State-Based Features](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#pure-functions-vs-state-based-features)
- [Code Integration Example](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#code-integration-example)
- [Corrected Enums](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#corrected-enums)
- [Advanced Features: \`upgradeMod\`](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#advanced-features-upgrademod)
- [Enabling Features](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript)#enabling-features)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 2 Isaacscript Cli: The Command Line Tool

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# isaacscript-cli: The Command-Line Tool

Relevant source files

- [packages/docs/docs/main/publishing-to-the-workshop.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/publishing-to-the-workshop.md?plain=1)
- [packages/docs/docs/main/updating-isaacscript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/updating-isaacscript.md?plain=1)
- [packages/eslint-plugin-isaacscript/scripts/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/utils.ts)
- [packages/isaacscript-cli/schemas/isaacscript-schema.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/schemas/isaacscript-schema.json)
- [packages/isaacscript-cli/src/classes/Config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/classes/Config.ts)
- [packages/isaacscript-cli/src/commands/check/check.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts)
- [packages/isaacscript-cli/src/commands/copy/copy.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/copy/copy.ts)
- [packages/isaacscript-cli/src/commands/init/createProject.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts)
- [packages/isaacscript-cli/src/commands/init/init.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts)
- [packages/isaacscript-cli/src/commands/monitor/monitor.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts)
- [packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts)
- [packages/isaacscript-cli/src/commands/publish/publish.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts)
- [packages/isaacscript-cli/src/configFile.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/configFile.ts)
- [packages/isaacscript-cli/src/constants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts)
- [packages/isaacscript-cli/src/customStage.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts)
- [packages/isaacscript-cli/src/git.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts)
- [packages/isaacscript-cli/src/main.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/main.ts)
- [packages/isaacscript-cli/src/packageManager.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/packageManager.ts)
- [packages/isaacscript-cli/src/parseArgs.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts)
- [packages/isaacscript-cli/src/validateMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/validateMod.ts)

The `isaacscript-cli` package is the central orchestrator for developing mods with IsaacScript. It provides a suite of commands to manage the entire development lifecycle, from project initialization and template synchronization to real-time monitoring and automated publishing.

## CLI Overview

The CLI is built using the `commander` library [\[packages/isaacscript-cli/src/parseArgs.ts31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/[packages/isaacscript-cli/src/parseArgs.ts#L31-L31)\] and serves as the primary interface for developers. It abstracts away the complexity of managing TypeScript-to-Lua (TSTL) transpilation, asset syncing, and Steam Workshop integration.\
\
### Command Structure\
\
The entry point of the CLI is `isaacscript`, which supports the following primary commands:\
\
| Command | Description |\
| --- | --- |\
| `monitor` | The default command. Watches for file changes and syncs them to the game. |\
| `init` | Scaffolds a new IsaacScript mod project from templates. |\
| `check` | Verifies that project configuration and template files are up to date. |\
| `publish` | Automates versioning, Git operations, and Workshop uploads. |\
| `copy` | Performs a one-time build and copy of the mod to the game directory. |\
| `nuke` | Deletes and reinstalls all Node.js dependencies. |\
| `update` | Updates npm dependencies to their latest versions. |\
\
**Sources:** [packages/isaacscript-cli/src/parseArgs.ts40-59](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts#L40-L59) [packages/isaacscript-cli/src/parseArgs.ts66-88](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts#L66-L88)\
\
## System Orchestration\
\
The CLI bridges the gap between the TypeScript source code and the The Binding of Isaac: Repentance game environment.\
\
### Relationship Diagram: CLI to Code Entities\
\
This diagram illustrates how CLI commands map to specific logic handlers and configuration entities within the codebase.\
\
```\
Asset Pipeline\
\
Core Orchestrators\
\
Command Handlers\
\
CLI Entry\
\
monitor\
\
init\
\
check\
\
publish\
\
Config\
\
TSTL\
\
Assets\
\
Templates\
\
Workshop\
\
Prepare\
\
Merge\
\
main.ts\
\
parseArgs.ts\
\
monitor.ts\
\
init.ts\
\
check.ts\
\
publish.ts\
\
classes/Config.ts\
\
spawnTSTLWatcher.ts\
\
spawnModDirectorySyncer.ts\
\
createProject.ts\
\
isaacscriptMod.ts\
\
customStage.ts\
\
xml-converter.exe\
```\
\
**Sources:** [packages/isaacscript-cli/src/main.ts10-15](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/main.ts#L10-L15) [packages/isaacscript-cli/src/parseArgs.ts40-54](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts#L40-L54) [packages/isaacscript-cli/src/commands/monitor/monitor.ts97-105](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L97-L105)\
\
## Configuration\
\
The CLI is configured via an `isaacscript.json` file located in the project root [\[packages/isaacscript-cli/src/constants.ts98-99](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/[packages/isaacscript-cli/src/constants.ts#L98-L99)\]. This file is managed by the `Config` class [\[packages/isaacscript-cli/src/classes/Config.ts25](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/[packages/isaacscript-cli/src/classes/Config.ts#L25-L25)\].\
\
Key configuration parameters include:\
\
- `modsDirectory`: The path to the game's local mod folder.\
- `saveSlot`: The save slot (1, 2, or 3) used for development testing.\
- `isaacScriptCommonDev`: A boolean flag to link to a local development version of the standard library.\
\
## Sub-System Summaries\
\
### Monitor & Hot-Reload\
\
The `monitor` command is the most complex part of the CLI. It spawns multiple subprocesses to watch for TypeScript changes, sync the `mod` directory, and communicate with the game via a dedicated "watcher" mod.\
\
- For details, see [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher).\
\
### Project Lifecycle (Init, Check, Publish)\
\
The CLI handles the "scaffolding" of new projects using static and dynamic templates. It also includes a "drift detection" system (`check`) to ensure mods stay updated with the latest IsaacScript standards, and a `publish` pipeline that automates Steam Workshop updates.\
\
- For details, see [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands).\
\
### Custom Stage Pipeline\
\
IsaacScript provides a specialized pipeline for creating custom floors. This involves validating PNG assets, merging XML room definitions, and running the `xml-converter.exe` tool to generate binary `.stb` files.\
\
- For details, see [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline).\
\
### TSTL Plugins\
\
During the transpilation process, the CLI applies several custom TypeScript-to-Lua plugins. These plugins handle tasks like adding debug statements for crash reporting and stripping incompatible Lua features.\
\
- For details, see [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation).\
\
## Development Workflow Diagram\
\
```\
Isaac GameTypeScriptToLuaisaacscript-cliDeveloperIsaac GameTypeScriptToLuaisaacscript-cliDeveloperloop[Every Change]isaacscript initProject Scaffolding Completeisaacscript monitorspawn --watchspawnModDirectorySyncerspawnSaveDatWriterEdit .ts fileTranspiled .luaSync to Mods FoldernotifyGamePing (Hot-Reload)\
```\
\
**Sources:** [packages/isaacscript-cli/src/commands/monitor/monitor.ts97-131](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L97-L131) [packages/isaacscript-cli/src/commands/init/init.ts144-155](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts#L144-L155)\
\
Dismiss\
\
Refresh this wiki\
\
Enter email to refresh\
\
### On this page\
\
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#isaacscript-cli-the-command-line-tool)\
- [CLI Overview](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#cli-overview)\
- [Command Structure](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#command-structure)\
- [System Orchestration](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#system-orchestration)\
- [Relationship Diagram: CLI to Code Entities](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#relationship-diagram-cli-to-code-entities)\
- [Configuration](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#configuration)\
- [Sub-System Summaries](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#sub-system-summaries)\
- [Monitor & Hot-Reload](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#monitor-hot-reload)\
- [Project Lifecycle (Init, Check, Publish)](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#project-lifecycle-init-check-publish)\
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#custom-stage-pipeline)\
- [TSTL Plugins](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#tstl-plugins)\
- [Development Workflow Diagram](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool#development-workflow-diagram)\
\
Ask Devin about IsaacScript/isaacscript\
\
Fast

---

## 2.1 Monitor Command And Development Watcher

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Monitor Command & Development Watcher

Relevant source files

- [.gitattributes](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.gitattributes)
- [.luarc.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.luarc.json)
- [.prettierignore](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.prettierignore)
- [packages/docs/docs/main/publishing-to-the-workshop.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/publishing-to-the-workshop.md?plain=1)
- [packages/docs/docs/main/updating-isaacscript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/updating-isaacscript.md?plain=1)
- [packages/eslint-plugin-isaacscript/scripts/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/utils.ts)
- [packages/isaacscript-cli/file-templates/dynamic/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/README.md?plain=1)
- [packages/isaacscript-cli/file-templates/dynamic/\_gitignore](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/_gitignore)
- [packages/isaacscript-cli/file-templates/static/.luarc.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.luarc.json)
- [packages/isaacscript-cli/file-templates/static/.prettierignore](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.prettierignore)
- [packages/isaacscript-cli/file-templates/static/\_cspell.config.jsonc](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/_cspell.config.jsonc)
- [packages/isaacscript-cli/file-templates/static/\_gitattributes](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/_gitattributes)
- [packages/isaacscript-cli/isaacscript-watcher/main.lua](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/isaacscript-watcher/main.lua)
- [packages/isaacscript-cli/isaacscript-watcher/resources/gfx/logo-green.png](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/isaacscript-watcher/resources/gfx/logo-green.png)
- [packages/isaacscript-cli/isaacscript-watcher/resources/gfx/logo.anm2](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/isaacscript-watcher/resources/gfx/logo.anm2)
- [packages/isaacscript-cli/schemas/isaacscript-schema.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/schemas/isaacscript-schema.json)
- [packages/isaacscript-cli/src/classes/Config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/classes/Config.ts)
- [packages/isaacscript-cli/src/commands/check/check.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts)
- [packages/isaacscript-cli/src/commands/copy/copy.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/copy/copy.ts)
- [packages/isaacscript-cli/src/commands/init/createProject.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts)
- [packages/isaacscript-cli/src/commands/init/init.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts)
- [packages/isaacscript-cli/src/commands/monitor/monitor.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts)
- [packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts)
- [packages/isaacscript-cli/src/commands/publish/publish.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts)
- [packages/isaacscript-cli/src/configFile.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/configFile.ts)
- [packages/isaacscript-cli/src/constants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts)
- [packages/isaacscript-cli/src/customStage.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts)
- [packages/isaacscript-cli/src/git.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts)
- [packages/isaacscript-cli/src/main.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/main.ts)
- [packages/isaacscript-cli/src/packageManager.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/packageManager.ts)
- [packages/isaacscript-cli/src/parseArgs.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts)
- [packages/isaacscript-cli/src/validateMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/validateMod.ts)

The `monitor` command is the primary development entry point for IsaacScript. It orchestrates a suite of subprocesses that handle TypeScript transpilation, file synchronization, and communication with the game client to enable a "hot-reload" experience.

## Overview of the Monitor Command

The `monitor` command is defined in `packages/isaacscript-cli/src/commands/monitor/monitor.ts`. When executed, it performs environment validation and then spawns four persistent subprocesses and one recurring interval task to manage the mod development lifecycle.

### Execution Flow

1. **Banner & Environment Check**: Prints the IsaacScript banner and identifies the package manager (npm, yarn, or pnpm) [packages/isaacscript-cli/src/commands/monitor/monitor.ts54-60](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L54-L60)
2. **Project Validation**: Ensures the command is run within a valid IsaacScript project and that dependencies are installed [packages/isaacscript-cli/src/commands/monitor/monitor.ts62-70](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L62-L70)
3. **Watcher Setup**: Copies the `isaacscript-watcher` mod to the game's mod directory and initializes its `save#.dat` files [packages/isaacscript-cli/src/commands/monitor/monitor.ts76-78](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L76-L78)
4. **Custom Stages**: Prepares custom stage metadata and XMLs if configured in `tsconfig.json` [packages/isaacscript-cli/src/commands/monitor/monitor.ts87-91](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L87-L91)
5. **Subprocess Orchestration**: Launches the four core background tasks [packages/isaacscript-cli/src/commands/monitor/monitor.ts98-104](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L98-L104)
6. **Game Ping**: Starts a 1-second interval to notify the game of the monitor's status [packages/isaacscript-cli/src/commands/monitor/monitor.ts129-131](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L129-L131)

### Subprocess Orchestration

| Subprocess | Function | Purpose |
| --- | --- | --- |
| **SaveDatWriter** | `spawnSaveDatWriter` | Writes to the watcher's save files to trigger Lua-side reloads. |
| **ModDirectorySyncer** | `spawnModDirectorySyncer` | Watches the `./mod` folder and syncs assets (PNGs, XMLs) to the game directory. |
| **TSTL Watcher** | `spawnTSTLWatcher` | Runs `tstl --watch` to transpile `.ts` files to `.lua` in real-time. |
| **ISC Dev Watcher** | `spawnTSTLWatcher` | (Optional) Watches a local `isaacscript-common` for library development. |

Sources: [packages/isaacscript-cli/src/commands/monitor/monitor.ts98-126](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L98-L126)

## Data Flow & Hot Reloading

The hot-reload mechanism relies on a handshake between the CLI and the `isaacscript-watcher` Lua mod. The CLI "pings" the mod by updating a file on disk, which the Lua mod detects via the game's `Isaac.HasModData` or by checking save file timestamps.

### System Architecture Diagram

This diagram illustrates how the CLI entities interact with the file system and the game process.

```
Game (Lua Space)

File System

CLI (Node.js Space)

Transpiles

Syncs

Updates

Detected by

Triggers

monitor.ts

Config Class

spawnTSTLWatcher

spawnModDirectorySyncer

spawnSaveDatWriter

notifyGamePing

/src/*.ts

/mod/**/*

Isaac Mods Folder

save1.dat (Watcher)

isaacscript-watcher/main.lua

Your Mod/main.lua
```

Sources: [packages/isaacscript-cli/src/commands/monitor/monitor.ts98-131](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L98-L131) [packages/isaacscript-cli/src/constants.ts105-108](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L105-L108)

## Configuration and the Config Class

The `monitor` command relies on the `Config` class to locate the game's mod directory and determine project-specific settings.

### The `isaacscript.json` File

The CLI reads settings from `isaacscript.json`. If it doesn't exist, the `Config` class attempts to resolve defaults (like the Steam mods path) [packages/isaacscript-cli/src/classes/Config.ts25-59](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/classes/Config.ts#L25-L59)

Key properties in the `Config` class include:

- `modsDirectory`: The absolute path to the Isaac mods folder [packages/isaacscript-cli/src/classes/Config.ts74](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/classes/Config.ts#L74-L74)
- `saveSlot`: The save slot (1, 2, or 3) used for communication [packages/isaacscript-cli/src/classes/Config.ts59](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/classes/Config.ts#L59-L59)
- `isaacScriptCommonDev`: Boolean indicating if the CLI should link to a local version of the standard library [packages/isaacscript-cli/src/commands/monitor/monitor.ts82-84](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L82-L84)

## Custom Stage Pipeline Integration

If the project uses custom stages, the `monitor` command invokes `prepareCustomStages` before starting the watchers.

### Preparation Steps

1. **Validation**: Checks that all PNG paths defined in `tsconfig.json` exist and are inside a `gfx` directory [packages/isaacscript-cli/src/customStage.ts74-163](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L74-L163)
2. **Asset Injection**: Copies internal IsaacScript custom stage assets (like `isaacscript-custom-stage` anm2 files) into the mod's resource folder [packages/isaacscript-cli/src/customStage.ts166-183](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L166-L183)
3. **Shader Merging**: Injects the `IsaacScript-RenderAboveHUD` shader into the mod's `shaders.xml` to enable advanced rendering [packages/isaacscript-cli/src/customStage.ts189-224](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L189-L224)
4. **Metadata Generation**: Generates `customStageMetadata.lua` which `isaacscript-common` uses to handle stage logic [packages/isaacscript-cli/src/customStage.ts78-82](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L78-L82)

Sources: [packages/isaacscript-cli/src/customStage.ts64-84](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L64-L84)

## Development Mode (`isaacScriptCommonDev`)

When the `dev` flag is set to `true` (via `isaacscript monitor --dev` or the config file), the CLI facilitates development of the `isaacscript-common` library itself.

1. **Linking**: It uses the package manager to `link` the local `packages/isaacscript-common` directory to the mod's `node_modules` [packages/isaacscript-cli/src/commands/monitor/monitor.ts144-193](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L144-L193)
2. **Dual Watching**: It spawns a second TSTL watcher specifically for the `isaacscript-common` source code. This allows changes in the library to be transpiled and immediately reflected in the mod being monitored [packages/isaacscript-cli/src/commands/monitor/monitor.ts107-126](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L107-L126)

Sources: [packages/isaacscript-cli/src/commands/monitor/monitor.ts82-84](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L82-L84) [packages/isaacscript-cli/src/commands/monitor/monitor.ts107-126](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L107-L126)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#monitor-command-development-watcher)
- [Overview of the Monitor Command](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#overview-of-the-monitor-command)
- [Execution Flow](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#execution-flow)
- [Subprocess Orchestration](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#subprocess-orchestration)
- [Data Flow & Hot Reloading](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#data-flow-hot-reloading)
- [System Architecture Diagram](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#system-architecture-diagram)
- [Configuration and the Config Class](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#configuration-and-the-config-class)
- [The \`isaacscript.json\` File](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#the-isaacscriptjson-file)
- [Custom Stage Pipeline Integration](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#custom-stage-pipeline-integration)
- [Preparation Steps](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#preparation-steps)
- [Development Mode (\`isaacScriptCommonDev\`)](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher#development-mode-isaacscriptcommondev)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 2.2 Init Check And Publish Commands

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Init, Check, and Publish Commands

Relevant source files

- [packages/docs/docs/main/example-mod.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/example-mod.md?plain=1)
- [packages/docs/docs/main/getting-started.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1)
- [packages/docs/docs/main/isaacscript-in-typescript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-typescript.md?plain=1)
- [packages/docs/docs/main/next-steps.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/next-steps.md?plain=1)
- [packages/docs/docs/main/publishing-to-the-workshop.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/publishing-to-the-workshop.md?plain=1)
- [packages/docs/docs/main/updating-isaacscript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/updating-isaacscript.md?plain=1)
- [packages/docs/docusaurus.config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docusaurus.config.ts)
- [packages/docs/sidebars.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/sidebars.ts)
- [packages/eslint-plugin-isaacscript/scripts/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/utils.ts)
- [packages/isaacscript-cli/schemas/tsconfig-isaacscript-schema.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/schemas/tsconfig-isaacscript-schema.json)
- [packages/isaacscript-cli/src/banner.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/banner.ts)
- [packages/isaacscript-cli/src/commands/check/check.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts)
- [packages/isaacscript-cli/src/commands/copy/copy.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/copy/copy.ts)
- [packages/isaacscript-cli/src/commands/init/createProject.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts)
- [packages/isaacscript-cli/src/commands/init/getProjectPath.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/getProjectPath.ts)
- [packages/isaacscript-cli/src/commands/init/init.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts)
- [packages/isaacscript-cli/src/commands/monitor/monitor.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts)
- [packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts)
- [packages/isaacscript-cli/src/commands/publish/publish.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts)
- [packages/isaacscript-cli/src/configFile.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/configFile.ts)
- [packages/isaacscript-cli/src/constants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts)
- [packages/isaacscript-cli/src/customStage.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts)
- [packages/isaacscript-cli/src/exec.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/exec.ts)
- [packages/isaacscript-cli/src/git.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts)
- [packages/isaacscript-cli/src/main.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/main.ts)
- [packages/isaacscript-cli/src/packageManager.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/packageManager.ts)
- [packages/isaacscript-cli/src/parseArgs.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts)
- [packages/isaacscript-cli/src/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/utils.ts)
- [packages/isaacscript-cli/src/validateMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/validateMod.ts)
- [packages/isaacscript-cli/src/validateNodeVersion.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/validateNodeVersion.ts)
- [packages/isaacscript-lua/isaacscript\_lua.py](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py)
- [packages/isaacscript-lua/publish.sh](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/publish.sh)
- [packages/isaacscript-lua/pyproject.toml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/pyproject.toml)

This section covers the command-line tools provided by `isaacscript-cli` for the lifecycle management of an IsaacScript project. These commands handle project creation (`init`), maintaining template consistency (`check`), and releasing the mod to Git and the Steam Workshop (`publish`).

## 1\. Init Command (`isaacscript init`)

The `init` command scaffolds a new IsaacScript project from predefined templates. It is orchestrated by `initCommand` [packages/isaacscript-cli/src/commands/init/init.ts23-75](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts#L23-L75)

### Project Creation Flow

The `init` command performs several validation and configuration steps before writing files:

1. **Environment Validation**: Checks for a supported Node.js version and detects the available package manager (npm, yarn, or pnpm) [packages/isaacscript-cli/src/commands/init/init.ts112-113](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts#L112-L113)
2. **User Input**: Prompts the user for the project name, save slot (1-3), and the path to the Isaac `mods` directory [packages/isaacscript-cli/src/commands/init/init.ts115-141](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts#L115-L141)
3. **Git Integration**: Optionally initializes a Git repository and can interact with the GitHub CLI (`gh`) to create a remote repository [packages/isaacscript-cli/src/git.ts10-105](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts#L10-L105)
4. **Scaffolding**: Calls `createProject` to write the physical files [packages/isaacscript-cli/src/commands/init/createProject.ts43-80](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L43-L80)

### Template System

IsaacScript uses two types of templates located in `packages/isaacscript-cli/file-templates/`:

- **Static Templates**: Files copied directly, such as `tsconfig.json` or `eslint.config.mjs` [packages/isaacscript-cli/src/commands/init/createProject.ts83-101](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L83-L101)
- **Dynamic Templates**: Files where placeholders (e.g., `PROJECT-NAME`) are replaced with user-specific values. This includes `package.json`, `README.md`, and GitHub Action workflows [packages/isaacscript-cli/src/commands/init/createProject.ts121-205](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L121-L205)

### Initialization Sequence Diagram

Title: "Project Scaffolding Sequence"

```
git.tscreateProjectinitCommandUsergit.tscreateProjectinitCommandUserisaacscript init [name]Prompt for Mods Directory & Save SlotpromptGitHubRepoOrGitRemoteURL()createProject()createConfigFile() (isaacscript.json)copyStaticFiles()copyDynamicFiles() (Replace Placeholders)installNodeModules()initGitRepository()Success Message
```

Sources: [packages/isaacscript-cli/src/commands/init/init.ts98-159](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts#L98-L159) [packages/isaacscript-cli/src/commands/init/createProject.ts43-80](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts#L43-L80) [packages/isaacscript-cli/src/git.ts161-208](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts#L161-L208)

## 2\. Check Command (`isaacscript check`)

The `check` command detects "template drift"—situations where a project's configuration files have fallen out of sync with the latest IsaacScript templates [packages/isaacscript-cli/src/commands/check/check.ts42-46](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L42-L46)

### Customization Markers

To allow users to modify certain parts of template files without triggering errors, the CLI supports special comment markers [packages/isaacscript-cli/src/commands/check/check.ts28-32](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L28-L32):

- `@template-customization-start` / `@template-customization-end`: Content between these is ignored during comparison.
- `@template-ignore-block-start` / `@template-ignore-block-end`: Entire blocks to be skipped.
- `@template-ignore-next-line`: Skips the immediate following line.

### Comparison Logic

The `compareTextFiles` function handles the verification [packages/isaacscript-cli/src/commands/check/check.ts188-240](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L188-L240) It uses `getTruncatedFileText` to strip ignored sections from both the project file and the template before performing a string comparison [packages/isaacscript-cli/src/commands/check/check.ts201-211](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L201-L211)

Sources: [packages/isaacscript-cli/src/commands/check/check.ts1-240](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts#L1-L240)

## 3\. Publish Command (`isaacscript publish`)

The `publish` command automates the release process for a mod [packages/isaacscript-cli/src/commands/publish/publish.ts26-49](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L26-L49)

### Release Pipeline

The command executes the following steps in order:

1. **Pre-flight Checks**: Ensures the Git working directory is clean and the project is in a valid state [packages/isaacscript-cli/src/commands/publish/publish.ts61-62](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L61-L62)
2. **Dependency Update**: Runs `updatePackageJSONDependencies` and performs a fresh install [packages/isaacscript-cli/src/commands/publish/publish.ts90-109](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L90-L109)
3. **Version Bumping**: Increments the version in `package.json` and propagates it to `metadata.xml`, `version.txt`, and `src/constants.ts` [packages/isaacscript-cli/src/commands/publish/publish.ts111-134](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L111-L134)
4. **Build & Lint**: Runs `npm run build` and `npm run lint` to ensure the code is production-ready [packages/isaacscript-cli/src/commands/publish/publish.ts84-87](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L84-L87)
5. **Git Operations**: Commits the changes and pushes to the remote repository [packages/isaacscript-cli/src/git.ts226-233](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts#L226-L233)
6. **Workshop Upload**: If on Windows, it invokes the Steam `ModUploader.exe` to push the mod to the Steam Workshop [packages/isaacscript-cli/src/constants.ts11](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L11-L11)

### Entity Association Diagram

Title: "Publish Command Logic Flow"

```
External Integration

File Sync

Pre-Publish Phase

CLI Entry Point

publishCommand

publish()

prePublish()

updateDependencies()

incrementVersion()

tryRunNPMScript('build')

writeVersionToMetadataXML()

writeVersionToConstantsTS()

writeVersionToVersionTXT()

publishIsaacScriptMod()

gitCommitAllAndPush()

ModUploader.exe (Steam)
```

Sources: [packages/isaacscript-cli/src/commands/publish/publish.ts55-67](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L55-L67) [packages/isaacscript-cli/src/commands/publish/publish.ts73-88](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L73-L88) [packages/isaacscript-cli/src/commands/publish/publish.ts111-134](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L111-L134) [packages/isaacscript-cli/src/constants.ts11](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L11-L11)

### Version Propagation

When a version is bumped (e.g., from `1.0.0` to `1.0.1`), the CLI updates multiple files to ensure consistency:

| File | Mechanism | Purpose |
| --- | --- | --- |
| `package.json` | `npm version` | Primary source of truth for Node.js ecosystem. |
| `metadata.xml` | Regex replacement | Required by Isaac game engine for the Mods menu. |
| `version.txt` | File write | Used by some community tools and legacy scripts. |
| `src/constants.ts` | Regex replacement | Allows the mod code to access its own version string via `VERSION`. |

Sources: [packages/isaacscript-cli/src/commands/publish/publish.ts158-192](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts#L158-L192)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#init-check-and-publish-commands)
- [1\. Init Command (\`isaacscript init\`)](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#1-init-command-isaacscript-init)
- [Project Creation Flow](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#project-creation-flow)
- [Template System](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#template-system)
- [Initialization Sequence Diagram](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#initialization-sequence-diagram)
- [2\. Check Command (\`isaacscript check\`)](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#2-check-command-isaacscript-check)
- [Customization Markers](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#customization-markers)
- [Comparison Logic](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#comparison-logic)
- [3\. Publish Command (\`isaacscript publish\`)](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#3-publish-command-isaacscript-publish)
- [Release Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#release-pipeline)
- [Entity Association Diagram](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#entity-association-diagram)
- [Version Propagation](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands#version-propagation)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 2.3 Custom Stage Pipeline

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Custom Stage Pipeline

Relevant source files

- [packages/docs/docs/main/custom-stages.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/custom-stages.md?plain=1)
- [packages/docs/docs/main/publishing-to-the-workshop.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/publishing-to-the-workshop.md?plain=1)
- [packages/docs/docs/main/updating-isaacscript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/updating-isaacscript.md?plain=1)
- [packages/eslint-plugin-isaacscript/scripts/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/utils.ts)
- [packages/isaac-typescript-definitions/src/enums/collections/roomSubTypes.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/roomSubTypes.ts)
- [packages/isaacscript-cli/schemas/tsconfig-isaacscript-section-schema.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/schemas/tsconfig-isaacscript-section-schema.json)
- [packages/isaacscript-cli/src/commands/check/check.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/check/check.ts)
- [packages/isaacscript-cli/src/commands/copy/copy.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/copy/copy.ts)
- [packages/isaacscript-cli/src/commands/init/createProject.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/createProject.ts)
- [packages/isaacscript-cli/src/commands/init/init.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/init/init.ts)
- [packages/isaacscript-cli/src/commands/monitor/monitor.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts)
- [packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/isaacscriptMod.ts)
- [packages/isaacscript-cli/src/commands/publish/publish.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/publish/publish.ts)
- [packages/isaacscript-cli/src/common.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/common.ts)
- [packages/isaacscript-cli/src/configFile.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/configFile.ts)
- [packages/isaacscript-cli/src/constants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts)
- [packages/isaacscript-cli/src/customStage.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts)
- [packages/isaacscript-cli/src/enums/copied/DoorSlot.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/enums/copied/DoorSlot.ts)
- [packages/isaacscript-cli/src/enums/copied/DoorSlotFlag.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/enums/copied/DoorSlotFlag.ts)
- [packages/isaacscript-cli/src/git.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/git.ts)
- [packages/isaacscript-cli/src/interfaces/copied/CustomStageTSConfig.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/interfaces/copied/CustomStageTSConfig.ts)
- [packages/isaacscript-cli/src/interfaces/copied/JSONRoomsFile.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/interfaces/copied/JSONRoomsFile.ts)
- [packages/isaacscript-cli/src/main.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/main.ts)
- [packages/isaacscript-cli/src/objects/copied/doorSlotToDoorSlotFlag.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/objects/copied/doorSlotToDoorSlotFlag.ts)
- [packages/isaacscript-cli/src/packageManager.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/packageManager.ts)
- [packages/isaacscript-cli/src/parseArgs.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/parseArgs.ts)
- [packages/isaacscript-cli/src/prompt.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/prompt.ts)
- [packages/isaacscript-cli/src/validateMod.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/validateMod.ts)
- [packages/isaacscript-common/src/classes/features/other/CustomStages.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/CustomStages.ts)
- [packages/isaacscript-common/src/classes/features/other/CustomTrapdoors.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/CustomTrapdoors.ts)
- [packages/isaacscript-common/src/classes/features/other/DisableAllSound.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/DisableAllSound.ts)
- [packages/isaacscript-common/src/classes/features/other/DisableInputs.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/DisableInputs.ts)
- [packages/isaacscript-common/src/classes/features/other/FastReset.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/FastReset.ts)
- [packages/isaacscript-common/src/classes/features/other/Pause.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/Pause.ts)
- [packages/isaacscript-common/src/classes/features/other/PreventGridEntityRespawn.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/PreventGridEntityRespawn.ts)
- [packages/isaacscript-common/src/enums/RockAltType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/enums/RockAltType.ts)
- [packages/isaacscript-common/src/functions/curses.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/curses.ts)
- [packages/isaacscript-common/src/functions/input.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/input.ts)
- [packages/isaacscript-common/src/functions/logMisc.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/logMisc.ts)
- [packages/isaacscript-common/src/functions/transformations.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/transformations.ts)
- [packages/isaacscript-common/src/interfaces/CustomStageTSConfig.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/interfaces/CustomStageTSConfig.ts)
- [packages/isaacscript-common/src/objects/backdropTypeToRockAltType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/backdropTypeToRockAltType.ts)
- [packages/isaacscript-common/src/objects/bossIDToEntityTypeVariant.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/bossIDToEntityTypeVariant.ts)
- [packages/isaacscript-common/src/objects/bossNamePNGFileNames.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/bossNamePNGFileNames.ts)
- [packages/isaacscript-common/src/objects/bossNames.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/bossNames.ts)
- [packages/isaacscript-common/src/objects/bossPortraitPNGFileNames.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/bossPortraitPNGFileNames.ts)
- [packages/isaacscript-common/src/objects/playerPortraitPNGFileNames.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/playerPortraitPNGFileNames.ts)
- [packages/isaacscript-common/src/objects/roomTypeNames.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/roomTypeNames.ts)
- [packages/isaacscript-common/src/objects/roomTypeSpecialGotoPrefixes.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/roomTypeSpecialGotoPrefixes.ts)

The **Custom Stage Pipeline** is a specialized build-and-prepare sequence within the `isaacscript-cli` that enables mod authors to create fully custom floors. Since the vanilla Binding of Isaac API does not natively support custom stages, IsaacScript provides a robust infrastructure to validate assets, merge room data, and generate the necessary metadata for the `isaacscript-common` library to inject these stages at runtime [packages/docs/docs/main/custom-stages.md8-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/custom-stages.md?plain=1#L8-L10)

The core logic resides in `prepareCustomStages`, which is executed during the `monitor` command lifecycle [packages/isaacscript-cli/src/commands/monitor/monitor.ts87-91](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L87-L91)

## Pipeline Overview

The pipeline automates the transformation of human-readable XML room files and configuration into binary `.stb` files and Lua metadata.

### Data Flow Diagram

The following diagram illustrates how stage definitions move from the `tsconfig.json` through the CLI's processing functions into the final mod directory.

**Stage Pipeline Data Flow**

```
Output Space

isaacscript-cli (Code Entity Space)

Input Space

getCustomStagesFromTSConfig()

Read

Path Validation

Generates

Merges

Writes

execExe()

Produces

injects shader

tsconfig.json

Custom Room XMLs

GFX Assets (.png)

prepareCustomStages

validateCustomStagePaths

fillCustomStageMetadata

combineCustomStageXMLs

xml-converter.exe

combined.stb

customStageMetadata.lua

shaders.xml (Injected)

Custom .anm2 files
```

Sources: [packages/isaacscript-cli/src/customStage.ts64-84](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L64-L84) [packages/isaacscript-cli/src/commands/monitor/monitor.ts87-91](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/monitor.ts#L87-L91) [packages/isaacscript-cli/src/tsconfig.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/tsconfig.ts#L1-L10)

## Implementation Details

### 1\. Validation and Asset Management

The pipeline first ensures all paths defined in the `tsconfig.json``customStages` array point to valid files.

- **Path Validation**: `validateCustomStagePaths` iterates through all asset fields (backdrops, decorations, rocks, pits, doors, and boss portraits) [packages/isaacscript-cli/src/customStage.ts91-144](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L91-L144)
- **Strict GFX Requirements**: All PNG files must reside within a `gfx` directory, or the CLI throws a `fatalError` [packages/isaacscript-cli/src/customStage.ts151-155](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L151-L155)
- **Internal Assets**: The function `copyCustomStageFilesToProject` copies internal IsaacScript `.anm2` files required for custom stage rendering into the mod's `resources/gfx/isaacscript-custom-stage` folder [packages/isaacscript-cli/src/customStage.ts166-183](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L166-L183)

### 2\. Shader Injection

Custom stages require the `IsaacScript-RenderAboveHUD` shader to render certain UI elements and effects correctly.

- `insertEmptyShader` checks for the existence of `content/shaders.xml` [packages/isaacscript-cli/src/customStage.ts190-196](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L190-L196)
- If the file exists but lacks the specific shader, it parses the XML using `xml2js` and injects the required `<shader>` node [packages/isaacscript-cli/src/customStage.ts198-224](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L198-L224)

### 3\. Metadata Generation

The CLI bridges the gap between TypeScript configuration and Lua runtime via `customStageMetadata.lua`.

- **Metadata Logic**: `fillCustomStageMetadata` converts the `CustomStageTSConfig` objects into a Lua-readable format [packages/isaacscript-cli/src/customStage.ts246-248](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L246-L248)
- **Room Metadata**: It parses the room XMLs to extract room shapes, variants, and door slots, storing them in `CustomStageRoomMetadata` [packages/isaacscript-cli/src/customStage.ts316-335](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L316-L335)
- **Output**: The final metadata is written to `node_modules/isaacscript-common/dist/customStageMetadata.lua`, where the standard library can access it [packages/isaacscript-cli/src/customStage.ts43-46](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L43-L46) [packages/isaacscript-cli/src/customStage.ts358](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L358-L358)

### 4\. XML Processing and STB Conversion

To make rooms compatible with the game, they must be merged and converted to binary.

- **Merging**: `combineCustomStageXMLs` reads all XML files specified in the config and merges them into a single temporary XML structure [packages/isaacscript-cli/src/customStage.ts404-418](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L404-L418)
- **Variant Shifting**: To prevent ID conflicts, room variants are shifted using the `roomVariantPrefix` multiplied by `ROOM_VARIANT_MULTIPLIER` (10,000) [packages/isaacscript-cli/src/customStage.ts58](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L58-L58) [packages/isaacscript-cli/src/customStage.ts433-440](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L433-L440)
- **Binary Conversion**: The CLI invokes `xml-converter.exe` (a bundled Windows executable) via `execExe` to transform the merged XML into the final `rooms.stb` file used by the game [packages/isaacscript-cli/src/customStage.ts23-25](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L23-L25) [packages/isaacscript-cli/src/customStage.ts457-463](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L457-L463)

## System Interaction Diagram

This diagram maps the CLI functions to the specific files they manipulate.

**Function-to-File Mapping**

```
Project Filesystem

isaacscript-cli Logic

Read by

Writes to

Writes to

Produces

validateCustomStagePaths()

insertEmptyShader()

fillCustomStageMetadata()

combineCustomStageXMLs()

tsconfig.json

mod/content/shaders.xml

.../customStageMetadata.lua

mod/resources/rooms.stb
```

Sources: [packages/isaacscript-cli/src/customStage.ts87-470](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L87-L470) [packages/isaacscript-cli/src/tsconfig.ts33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/tsconfig.ts#L33-L33)

## Key Constants and Configuration

| Constant | Value / Purpose |
| --- | --- |
| `ROOM_VARIANT_MULTIPLIER` | `10000`; used to offset custom room IDs [packages/isaacscript-cli/src/customStage.ts58](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L58-L58) |
| `EMPTY_SHADER_NAME` | `"IsaacScript-RenderAboveHUD"` [packages/isaacscript-cli/src/customStage.ts62](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L62-L62) |
| `XML_CONVERTER_PATH` | Path to the `xml-converter.exe` utility [packages/isaacscript-cli/src/constants.ts35-38](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L35-L38) |
| `roomVariantPrefix` | User-defined ID in `tsconfig.json` to ensure mod compatibility [packages/docs/docs/main/custom-stages.md84](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/custom-stages.md?plain=1#L84-L84) |

Sources: [packages/isaacscript-cli/src/customStage.ts58-62](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/customStage.ts#L58-L62) [packages/isaacscript-cli/src/constants.ts35-38](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/constants.ts#L35-L38) [packages/docs/docs/main/custom-stages.md84](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/custom-stages.md?plain=1#L84-L84)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#custom-stage-pipeline)
- [Pipeline Overview](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#pipeline-overview)
- [Data Flow Diagram](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#data-flow-diagram)
- [Implementation Details](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#implementation-details)
- [1\. Validation and Asset Management](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#1-validation-and-asset-management)
- [2\. Shader Injection](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#2-shader-injection)
- [3\. Metadata Generation](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#3-metadata-generation)
- [4\. XML Processing and STB Conversion](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#4-xml-processing-and-stb-conversion)
- [System Interaction Diagram](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#system-interaction-diagram)
- [Key Constants and Configuration](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline#key-constants-and-configuration)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 2.4 Tstl Plugins And Code Generation

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# TSTL Plugins & Code Generation

Relevant source files

- [packages/docs/docs/main/isaacscript-in-lua.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-lua.md?plain=1)
- [packages/isaacscript-cli/file-templates/dynamic/mod/metadata.xml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/mod/metadata.xml)
- [packages/isaacscript-cli/file-templates/dynamic/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/package.json)
- [packages/isaacscript-cli/file-templates/dynamic/src/main-dev.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/src/main-dev.ts)
- [packages/isaacscript-cli/file-templates/dynamic/src/main.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/src/main.ts)
- [packages/isaacscript-cli/file-templates/static/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/scripts/lint.ts)
- [packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts)
- [packages/isaacscript-cli/file-templates/static/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json)
- [packages/isaacscript-cli/isaacscript-watcher/metadata.xml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/isaacscript-watcher/metadata.xml)
- [packages/isaacscript-common/src/functions/ambush.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/ambush.ts)
- [packages/isaacscript-common/tsconfig.bundle.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json)
- [packages/isaacscript-common/website-root.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/website-root.md?plain=1)
- [packages/isaacscript-tsconfig/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/README.md?plain=1)
- [packages/isaacscript-tsconfig/tsconfig.mod.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/tsconfig.mod.json)

This page documents the TypeScript-to-Lua (TSTL) compiler plugins and post-processing steps used by the IsaacScript CLI to transform TypeScript code into optimized, game-compatible Lua. These plugins address specific limitations of the Isaac Lua environment, such as global namespace pollution and the lack of native crash stack traces.

## Overview of the Compilation Pipeline

The IsaacScript build process relies on `typescript-to-lua` (TSTL) to transpile source code. The CLI configures TSTL via the project's `tsconfig.json` to use a set of custom plugins that modify the Abstract Syntax Tree (AST) or the resulting Lua string.

### Plugin Execution Flow

The following diagram illustrates how plugins are integrated into the TSTL lifecycle:

**TSTL Plugin Lifecycle**

```
Lua Output Space

TSTL Plugin Pipeline

TypeScript Space

TS Source Files

TypeScript AST

addCrashDebugStatements (AST Transformation)

noExtendedEnums (AST Transformation)

TSTL Core (Emit Lua)

addIsaacScriptCommentHeader (Lua String Post-process)

main.lua (Bundled)
```

Sources: [packages/isaacscript-cli/file-templates/static/tsconfig.json16-35](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L16-L35) [packages/isaacscript-common/tsconfig.bundle.json12-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json#L12-L31)

* * *

## Bundled Plugins

The IsaacScript CLI provides three primary plugins located in `isaacscript/plugins/`. These are referenced in the `tstl` section of the `tsconfig.json` [packages/isaacscript-cli/file-templates/static/tsconfig.json20-32](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L20-L32)

### 1\. addIsaacScriptCommentHeader

This plugin adds a standardized explanatory header to the top of the generated `main.lua` file. It informs users that the file is auto-generated and should not be edited manually, as changes will be overwritten during the next build [packages/isaacscript-cli/file-templates/static/tsconfig.json21-22](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L21-L22)

A specialized version, `addIsaacScriptCommentHeaderCommon.cjs`, is used when bundling the `isaacscript-common` library itself [packages/isaacscript-common/tsconfig.bundle.json20-22](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json#L20-L22)

### 2\. noExtendedEnums

In standard TSTL, enums are often transpiled into objects that can be affected by global variable lookups or extended in ways that may conflict with the Isaac API. This plugin ensures that enums are "safe" from global variable interference, preventing bugs where a global variable in the Isaac environment might accidentally shadow or collide with an enum member [packages/isaacscript-cli/file-templates/static/tsconfig.json24-25](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L24-L25)

### 3\. addCrashDebugStatements

This is a specialized debugging tool. When enabled, it injects logic into the transpiled Lua to track the exact line of TypeScript/Lua that causes a game crash. Because the Isaac engine often crashes without a useful stack trace, this plugin provides the necessary instrumentation to identify the "death line" [packages/isaacscript-cli/file-templates/static/tsconfig.json27-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L27-L31)

* * *

## Configuration and Implementation

The behavior of these plugins is governed by the `tsconfig.json` file found in every IsaacScript project.

### Project Configuration

The CLI generates a `tsconfig.json` that extends `isaacscript-tsconfig/tsconfig.mod.json` [packages/isaacscript-cli/file-templates/static/tsconfig.json7-13](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L7-L13) Key TSTL settings include:

| Setting | Value | Description |
| --- | --- | --- |
| `luaTarget` | `"5.3"` | Matches the version of Lua used by _The Binding of Isaac: Repentance_ [packages/isaacscript-cli/file-templates/static/tsconfig.json17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L17-L17) |
| `luaBundle` | `"main.lua"` | Ensures all TypeScript files are bundled into a single entry point [packages/isaacscript-cli/file-templates/static/tsconfig.json18](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L18-L18) |
| `luaBundleEntry` | `"./src/bundleEntry.ts"` | Points to the entry file that executes the `main()` function [packages/isaacscript-cli/file-templates/static/tsconfig.json19](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L19-L19) |
| `noImplicitGlobalVariables` | `true` | Prevents accidental leaks into the Lua global namespace [packages/isaacscript-cli/file-templates/static/tsconfig.json34](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L34-L34) |

### The Bundle Entry Point

To avoid issues with the "Temporal Dead Zone" (where variables are accessed before they are defined due to Lua's script execution order), the CLI uses a dedicated `bundleEntry.ts`. This file's sole responsibility is to import and call the `main()` function from `src/main.ts` [packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts1-11](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts#L1-L11)

**Code Entity Relationship: Entry Point**

```
Functions

Project Structure

imports

calls

RegisterMod

bundleEntry.ts

main.ts

main.lua (Output)

export function main()

Isaac Engine
```

Sources: [packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts6-8](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts#L6-L8) [packages/isaacscript-cli/file-templates/dynamic/src/main.ts5-15](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/src/main.ts#L5-L15)

* * *

## Code Generation for Libraries

When `isaacscript-common` is bundled for Lua users, it uses a specific configuration (`tsconfig.bundle.json`) that targets `isaacscript-common.lua` as the output [packages/isaacscript-common/tsconfig.bundle.json15](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json#L15-L15)

This process:

1. Sets `declaration` to `false` to suppress `.d.ts` generation during the Lua bundle phase [packages/isaacscript-common/tsconfig.bundle.json7](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json#L7-L7)
2. Uses the `indexLua.ts` entry point [packages/isaacscript-common/tsconfig.bundle.json16](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json#L16-L16)
3. Applies the `noExtendedEnums` plugin to ensure the library's internal enums do not conflict with the user's mod environment [packages/isaacscript-common/tsconfig.bundle.json25-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json#L25-L27)

Sources:

- [packages/isaacscript-cli/file-templates/static/tsconfig.json1-44](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/tsconfig.json#L1-L44)
- [packages/isaacscript-common/tsconfig.bundle.json1-32](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json#L1-L32)
- [packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts1-11](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/src/bundleEntry.ts#L1-L11)
- [packages/isaacscript-cli/file-templates/dynamic/src/main.ts1-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/src/main.ts#L1-L20)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#tstl-plugins-code-generation)
- [Overview of the Compilation Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#overview-of-the-compilation-pipeline)
- [Plugin Execution Flow](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#plugin-execution-flow)
- [Bundled Plugins](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#bundled-plugins)
- [1\. addIsaacScriptCommentHeader](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#1-addisaacscriptcommentheader)
- [2\. noExtendedEnums](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#2-noextendedenums)
- [3\. addCrashDebugStatements](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#3-addcrashdebugstatements)
- [Configuration and Implementation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#configuration-and-implementation)
- [Project Configuration](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#project-configuration)
- [The Bundle Entry Point](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#the-bundle-entry-point)
- [Code Generation for Libraries](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation#code-generation-for-libraries)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 4 Type Definitions: Isaac Typescript Definitions And Repentogon

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Type Definitions: isaac-typescript-definitions & REPENTOGON

Relevant source files

- [packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts)
- [packages/isaac-typescript-definitions-repentogon/src/enums/NullPickupSubType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/NullPickupSubType.ts)
- [packages/isaac-typescript-definitions-repentogon/src/enums/StatusEffect.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/StatusEffect.ts)
- [packages/isaac-typescript-definitions-repentogon/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/index.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/Game.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/Game.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/PlayerManager.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/PlayerManager.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityFamiliar.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityFamiliar.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityKnife.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityKnife.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityLaser.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityLaser.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityTear.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityTear.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/unofficial/AddCallbackParametersRepentogon.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/unofficial/AddCallbackParametersRepentogon.d.ts)
- [packages/isaac-typescript-definitions/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/index.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EffectList.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EffectList.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityList.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityList.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityNPC.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityNPC.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityPtr.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPtr.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Game.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Game.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/ModDescription.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/ModDescription.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Sprite.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Sprite.d.ts)
- [packages/isaac-typescript-definitions/src/types/index.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts)

This section provides an overview of the two primary type-definition packages used in IsaacScript. These packages provide the TypeScript interfaces, namespaces, and enums that allow the TypeScript-to-Lua (TSTL) compiler to understand the Binding of Isaac: Repentance API.

## Overview of Type Packages

IsaacScript splits its type definitions into two distinct packages to support both vanilla modding and extended modding via the REPENTOGON executable hack.

| Package | Purpose | Target Environment |
| --- | --- | --- |
| `isaac-typescript-definitions` | Base definitions for the official Rebirth/Afterbirth+/Repentance API. | Vanilla Game (Lua API) |
| `isaac-typescript-definitions-repentogon` | Extensions for the REPENTOGON exe-hack. | REPENTOGON-enabled Game |

These definitions bridge the gap between the game's internal C++ logic (exposed via Lua `userdata` and `tables`) and TypeScript's static analysis.

### Type System Relationship

The following diagram illustrates how the type definitions wrap the game's underlying structures.

**API Mapping Architecture**

```
Code Entities

Lua / Game Space

TypeScript Space

Interfaces/Namespaces

Extends & Overlays

New Functionality

isaac-typescript-definitions

isaac-typescript-definitions-repentogon

Vanilla API (userdata)

REPENTOGON Extensions

EntityPlayer

Isaac

Game

ModCallbackRepentogon
```

Sources: [packages/isaac-typescript-definitions/src/types/index.d.ts1-129](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L1-L129) [packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts1-140](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts#L1-L140)

* * *

## Base Game API Definitions

The `isaac-typescript-definitions` package is the core requirement for any IsaacScript project. It provides comprehensive coverage of the official API.

### Core Components

- **Classes & Interfaces**: High-level game objects like `EntityPlayer` [packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts36](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts#L36-L36)`Game` [packages/isaac-typescript-definitions/src/types/classes/Game.d.ts21](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Game.d.ts#L21-L21) and `Sprite` [packages/isaac-typescript-definitions/src/types/classes/Sprite.d.ts3](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Sprite.d.ts#L3-L3)
- **Global Namespaces**: Static utility methods provided by the game, primarily the `Isaac` namespace [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts#L27-L27)
- **Enums**: Exhaustive TypeScript enums for everything from `EntityType` [packages/isaac-typescript-definitions/src/index.ts33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/index.ts#L33-L33) to `SoundEffect` [packages/isaac-typescript-definitions/src/index.ts96](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/index.ts#L96-L96)
- **Popular Mod Support**: Includes definitions for community-standard mods like `StageAPI` and `EID` [packages/isaac-typescript-definitions/src/types/index.d.ts118-128](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L118-L128)

For a deep dive into the base definitions, including how unofficial primitives and community mod typings are structured, see **[Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))**.

Sources: [packages/isaac-typescript-definitions/src/index.ts1-101](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/index.ts#L1-L101) [packages/isaac-typescript-definitions/src/types/index.d.ts1-129](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L1-L129)

* * *

## REPENTOGON Extension Definitions

`isaac-typescript-definitions-repentogon` is an optional package for developers using the [REPENTOGON](https://repentogon.com/) engine enhancement. It does not replace the base definitions but rather extends them.

### Key Enhancements

- **Extended Callbacks**: Adds support for `ModCallbackRepentogon`, which provides more granular control over game events like `PRE_ENTITY_TAKE_DMG` [packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts58](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts#L58-L58)
- **New Engine Classes**: Exposes internal engine features like `PlayerManager` [packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts126](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts#L126-L126) and `ImGui` [packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts109](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts#L109-L109)
- **Method Overloads**: Provides "Ex" versions of vanilla methods (e.g., `StartStageTransitionEx`) that return proper TypeScript types instead of raw `userdata` [packages/isaac-typescript-definitions-repentogon/src/types/classes/Game.d.ts197](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/Game.d.ts#L197-L197)

For details on how to configure your project for REPENTOGON and a list of all added callbacks, see **[REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)**.

Sources: [packages/isaac-typescript-definitions-repentogon/src/index.ts1-67](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/index.ts#L1-L67) [packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts6-163](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts#L6-L163)

* * *

## Entity Hierarchy Diagram

This diagram bridges the natural language concepts of game entities to their specific TypeScript interface names used in the definition files.

**Entity Type Mapping**

```

«Interface»

Entity

[packages/isaac-typescript-definitions/src/types/classes/Entity.d.ts]

EntityPlayer

[packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts]

EntityNPC

[packages/isaac-typescript-definitions/src/types/classes/EntityNPC.d.ts]

EntityPickup

[packages/isaac-typescript-definitions/src/types/classes/EntityPickup.d.ts]

EntityTear

[packages/isaac-typescript-definitions/src/types/classes/EntityTear.d.ts]
```

Sources: [packages/isaac-typescript-definitions/src/types/index.d.ts32-45](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L32-L45)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#type-definitions-isaac-typescript-definitions-repentogon)
- [Overview of Type Packages](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#overview-of-type-packages)
- [Type System Relationship](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#type-system-relationship)
- [Base Game API Definitions](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#base-game-api-definitions)
- [Core Components](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#core-components)
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#repentogon-extension-definitions)
- [Key Enhancements](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#key-enhancements)
- [Entity Hierarchy Diagram](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon#entity-hierarchy-diagram)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 4.1 Base Game Api Definitions (Isaac Typescript Definitions)

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Base Game API Definitions (isaac-typescript-definitions)

Relevant source files

- [.vscode/extensions.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.vscode/extensions.json)
- [.vscode/settings.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.vscode/settings.json)
- [packages/isaac-typescript-definitions/src/enums/BackdropType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/BackdropType.ts)
- [packages/isaac-typescript-definitions/src/enums/ButtonAction.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/ButtonAction.ts)
- [packages/isaac-typescript-definitions/src/enums/Challenge.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/Challenge.ts)
- [packages/isaac-typescript-definitions/src/enums/Controller.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/Controller.ts)
- [packages/isaac-typescript-definitions/src/enums/CopyableIsaacAPIClassType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/CopyableIsaacAPIClassType.ts)
- [packages/isaac-typescript-definitions/src/enums/DrawStringAlignment.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/DrawStringAlignment.ts)
- [packages/isaac-typescript-definitions/src/enums/EntityType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/EntityType.ts)
- [packages/isaac-typescript-definitions/src/enums/GameStateFlag.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/GameStateFlag.ts)
- [packages/isaac-typescript-definitions/src/enums/GridRoom.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/GridRoom.ts)
- [packages/isaac-typescript-definitions/src/enums/JacobEsauControls.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/JacobEsauControls.ts)
- [packages/isaac-typescript-definitions/src/enums/LevelStage.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/LevelStage.ts)
- [packages/isaac-typescript-definitions/src/enums/Music.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/Music.ts)
- [packages/isaac-typescript-definitions/src/enums/NPCID.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/NPCID.ts)
- [packages/isaac-typescript-definitions/src/enums/PillEffect.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/PillEffect.ts)
- [packages/isaac-typescript-definitions/src/enums/RoomShape.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/RoomShape.ts)
- [packages/isaac-typescript-definitions/src/enums/RoomType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/RoomType.ts)
- [packages/isaac-typescript-definitions/src/enums/SoundEffect.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/SoundEffect.ts)
- [packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts)
- [packages/isaac-typescript-definitions/src/enums/collections/variants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/variants.ts)
- [packages/isaac-typescript-definitions/src/enums/mods/EncyclopediaItemPoolType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/mods/EncyclopediaItemPoolType.ts)
- [packages/isaac-typescript-definitions/src/enums/mods/ModConfigMenuOptionType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/mods/ModConfigMenuOptionType.ts)
- [packages/isaac-typescript-definitions/src/enums/mods/StageAPIEnums.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/mods/StageAPIEnums.ts)
- [packages/isaac-typescript-definitions/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/index.ts)
- [packages/isaac-typescript-definitions/src/types/classes/BitSet128.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/BitSet128.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/CardConfigList.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/CardConfigList.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Color.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Color.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EffectList.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EffectList.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Entity.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Entity.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityEffect.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityEffect.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityFamiliar.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityFamiliar.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityLaser.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityLaser.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityList.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityList.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityNPC.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityNPC.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityPickup.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPickup.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntityPtr.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPtr.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/EntriesList.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntriesList.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Game.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Game.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/GridEntity.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/GridEntity.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/HUD.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/HUD.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Input.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Input.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/ItemConfig.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/ItemConfig.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/ItemConfigList.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/ItemConfigList.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/ItemPool.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/ItemPool.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/KColor.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/KColor.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Level.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Level.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/ModDescription.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/ModDescription.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/MusicManager.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/MusicManager.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Options.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Options.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/RNG.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/RNG.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Room.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Room.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/RoomConfig.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/RoomConfig.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/RoomConfigSpawn.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/RoomConfigSpawn.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/RoomDescriptor.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/RoomDescriptor.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Seeds.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Seeds.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Sprite.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Sprite.d.ts)
- [packages/isaac-typescript-definitions/src/types/classes/Vector.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Vector.d.ts)
- [packages/isaac-typescript-definitions/src/types/index.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/EID.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/EID.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/Encyclopedia.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/Encyclopedia.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/InputHelper.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/InputHelper.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/MinimapAPI.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/MinimapAPI.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/ModConfigMenu.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/ModConfigMenu.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/MusicModCallback.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/MusicModCallback.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/Sandbox.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/Sandbox.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/SandboxGlobals.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/SandboxGlobals.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/StageAPI.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/StageAPI.d.ts)
- [packages/isaac-typescript-definitions/src/types/mods/StageAPIInterfaces.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/StageAPIInterfaces.d.ts)
- [packages/isaacscript-cli/file-templates/static/.vscode/extensions.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.vscode/extensions.json)
- [packages/isaacscript-cli/file-templates/static/.vscode/settings.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/static/.vscode/settings.json)
- [packages/isaacscript-cli/src/enums/copied/RoomShape.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/enums/copied/RoomShape.ts)
- [packages/isaacscript-common/src/classes/callbacks/PostPlayerInitFirst.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/callbacks/PostPlayerInitFirst.ts)
- [packages/isaacscript-common/src/functions/emptyRoom.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/emptyRoom.ts)
- [packages/isaacscript-common/src/functions/gridIndex.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/gridIndex.ts)
- [packages/isaacscript-common/src/functions/pickupVariants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/pickupVariants.ts)
- [packages/isaacscript-common/src/functions/roomShapeWalls.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/roomShapeWalls.ts)
- [packages/isaacscript-common/src/maps/characterNameToTypeMap.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/maps/characterNameToTypeMap.ts)
- [packages/isaacscript-common/src/objects/colors.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/colors.ts)
- [packages/isaacscript-common/src/objects/kColors.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/kColors.ts)
- [packages/isaacscript-common/src/sets/entitiesWithArmorSet.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/sets/entitiesWithArmorSet.ts)
- [packages/isaacscript-spell/dictionaries/isaacscript/isaacscript.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaacscript/isaacscript.txt)

The `isaac-typescript-definitions` package provides the TypeScript interface and type definitions for the _Binding of Isaac: Repentance_ Lua API. It transforms the weakly-typed Lua environment into a type-safe development experience by defining the game's global namespaces, classes, and extensive enum catalogs.

### Package Structure and Entry Point

The package is organized into three main directories under `src/`:

1. `types/classes/`: Contains `.d.ts` files for vanilla game classes (e.g., `EntityPlayer`, `Game`, `Level`).
2. `enums/`: Contains the full catalog of game constants, including sub-types and variants.
3. `types/mods/`: Contains typings for popular community mods to facilitate cross-mod compatibility.

The main entry point is `src/index.ts`, which exports all enums, while `src/types/index.d.ts` acts as the reference hub for all class declarations [packages/isaac-typescript-definitions/src/index.ts1-101](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/index.ts#L1-L101) [packages/isaac-typescript-definitions/src/types/index.d.ts1-129](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L1-L129)

### Core API Classes

The definitions represent the game's `userdata` and `table` structures as TypeScript interfaces and namespaces.

#### The Isaac Namespace

The `Isaac` namespace contains miscellaneous general-purpose methods. Unlike most API objects, `Isaac` is a Lua `table` rather than `userdata` [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts22-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts#L22-L27) It provides critical utility functions for entity manipulation and debug logging.

| Function | Description |
| --- | --- |
| `GetPlayer` | Returns the `EntityPlayer` at a specific index [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts213](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts#L213-L213) |
| `Spawn` | Spawns a new entity into the game world [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts383-389](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts#L383-L389) |
| `DebugString` | Prints a string to the game's `log.txt` [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts92](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts#L92-L92) |
| `GetIdByName` | Retrieves the ID for items, entities, or sounds by their string name [packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts200-205](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Isaac.d.ts#L200-L205) |

#### Game and Level Logic

The `Game` interface manages the global state of the current run, while `Level` handles the floor-specific structure.

- **Game**: Handles rendering fades, explosions, and global run state [packages/isaac-typescript-definitions/src/types/classes/Game.d.ts21-154](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Game.d.ts#L21-L154)
- **Level**: Manages the grid of rooms, stage transitions, and curses [packages/isaac-typescript-definitions/src/types/classes/Level.d.ts1-100](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Level.d.ts#L1-L100)
- **Room**: Represents the current room Isaac is in, providing methods for grid entities and collision [packages/isaac-typescript-definitions/src/types/classes/Room.d.ts1-100](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Room.d.ts#L1-L100)

#### Entity Hierarchy

The definitions follow the game's inheritance-like structure where specific entities extend the base `Entity` interface.

**Entity Definition Mapping**

```
Code Entity Space (classes/)

Natural Language Space

extends

extends

extends

extends

A Character (Isaac/Cain)

An Enemy (Gaper)

A Collectible (Sad Onion)

A Familiar (Brother Bobby)

Entity

EntityPlayer

EntityNPC

EntityPickup

EntityFamiliar
```

Sources: [packages/isaac-typescript-definitions/src/types/classes/Entity.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Entity.d.ts#L1-L10) [packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts36](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPlayer.d.ts#L36-L36) [packages/isaac-typescript-definitions/src/types/classes/EntityNPC.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityNPC.d.ts#L1-L10) [packages/isaac-typescript-definitions/src/types/classes/EntityPickup.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityPickup.d.ts#L1-L10) [packages/isaac-typescript-definitions/src/types/classes/EntityFamiliar.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/EntityFamiliar.d.ts#L1-L10)

### The Enum Catalog

The package provides exhaustive enums for every ID in the game. This is the primary mechanism for avoiding "magic numbers" in mod code.

- **EntityType**: The primary category of an entity (e.g., `PLAYER`, `TEAR`, `PICKUP`) [packages/isaac-typescript-definitions/src/enums/EntityType.ts1-100](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/EntityType.ts#L1-L100)
- **Sub-Types**: Contained in `subTypes.ts`, these define specific identities like `PlayerType.ISAAC` or `HeartSubType.SOUL` [packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts13-28](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts#L13-L28) [packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts244-276](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts#L244-L276)
- **Variants**: Contained in `variants.ts`, these define visual or functional variations, such as `TearVariant.CUPID_BLUE` or `FamiliarVariant.INCUBUS` [packages/isaac-typescript-definitions/src/enums/collections/variants.ts22-41](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/variants.ts#L22-L41) [packages/isaac-typescript-definitions/src/enums/collections/variants.ts166](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/variants.ts#L166-L166)

**Enum and Entity Association**

```
Enum Catalog (enums/)

Code Entity Space

Entity Class

Type: EntityType

Variant: int

SubType: int

EntityType Enum

TearVariant / BombVariant

PlayerType / HeartSubType
```

Sources: [packages/isaac-typescript-definitions/src/enums/EntityType.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/EntityType.ts#L1-L10) [packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts1-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/subTypes.ts#L1-L20) [packages/isaac-typescript-definitions/src/enums/collections/variants.ts1-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/collections/variants.ts#L1-L20)

### Unofficial and Community Additions

#### Unofficial Typings

The package includes `unofficial` definitions that add TypeScript-specific helpers not present in the vanilla Lua API:

- `BitFlags<T>`: A helper type for handling bitwise operations on enums [packages/isaac-typescript-definitions/src/types/index.d.ts104](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L104-L104)
- `IsaacAPIClass`: A base interface for classes that share common Isaac API traits [packages/isaac-typescript-definitions/src/types/index.d.ts106](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L106-L106)
- `AddCallbackParameters`: A complex mapping used to provide type-safety for the `Mod.AddCallback` arguments based on the `ModCallback` type [packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts26-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts#L26-L31) [packages/isaac-typescript-definitions/src/types/index.d.ts100](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L100-L100)

#### Third-Party Mod Typings

To support the ecosystem, the package bundles typings for major mods, allowing developers to interact with them safely:

- **StageAPI**: Interfaces for custom floor and room generation [packages/isaac-typescript-definitions/src/types/mods/StageAPI.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/StageAPI.d.ts#L1-L10)
- **EID (External Item Descriptions)**: Typings for adding custom descriptions to items [packages/isaac-typescript-definitions/src/types/mods/EID.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/EID.d.ts#L1-L10)
- **MinimapAPI**: Methods for modifying the in-game minimap [packages/isaac-typescript-definitions/src/types/mods/MinimapAPI.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/MinimapAPI.d.ts#L1-L10)
- **ModConfigMenu**: Typings for creating in-game configuration menus [packages/isaac-typescript-definitions/src/types/mods/ModConfigMenu.d.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/mods/ModConfigMenu.d.ts#L1-L10)

Sources: [packages/isaac-typescript-definitions/src/types/index.d.ts100-129](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/index.d.ts#L100-L129) [packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts26-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/types/classes/Mod.d.ts#L26-L31)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#base-game-api-definitions-isaac-typescript-definitions)
- [Package Structure and Entry Point](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#package-structure-and-entry-point)
- [Core API Classes](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#core-api-classes)
- [The Isaac Namespace](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#the-isaac-namespace)
- [Game and Level Logic](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#game-and-level-logic)
- [Entity Hierarchy](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#entity-hierarchy)
- [The Enum Catalog](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#the-enum-catalog)
- [Unofficial and Community Additions](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#unofficial-and-community-additions)
- [Unofficial Typings](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#unofficial-typings)
- [Third-Party Mod Typings](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions)#third-party-mod-typings)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 4.2 Repentogon Extension Definitions

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# REPENTOGON Extension Definitions

Relevant source files

- [packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts)
- [packages/isaac-typescript-definitions-repentogon/src/enums/NullPickupSubType.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/NullPickupSubType.ts)
- [packages/isaac-typescript-definitions-repentogon/src/enums/StatusEffect.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/enums/StatusEffect.ts)
- [packages/isaac-typescript-definitions-repentogon/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/index.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/Game.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/Game.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/GenericPrompt.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/GenericPrompt.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/Isaac.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/Isaac.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/ItemPool.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/ItemPool.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/PersistentGameData.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/PersistentGameData.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/PlayerManager.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/PlayerManager.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/Room.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/Room.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityDelirium.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityDelirium.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityFamiliar.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityFamiliar.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityKnife.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityKnife.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityLaser.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityLaser.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityNPC.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityNPC.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityPlayer.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityPlayer.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityTear.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityTear.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/grid-entity/GridEntityRock.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/grid-entity/GridEntityRock.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/hud/HUD.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/hud/HUD.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/sprite/Sprite.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/sprite/Sprite.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/unofficial/AddCallbackParametersRepentogon.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/unofficial/AddCallbackParametersRepentogon.d.ts)

The `isaac-typescript-definitions-repentogon` package provides TypeScript type definitions for the **REPENTOGON** exe-hack. This extension significantly expands the Binding of Isaac: Repentance modding API by exposing internal game engine functions, adding new callbacks, and fixing bugs in the vanilla Lua API.

These definitions are designed to be used alongside the base `isaac-typescript-definitions` to provide a seamless development experience for modders using the REPENTOGON expansion.

Sources: `packages/isaac-typescript-definitions-repentogon/src/types/index.d.ts` [1-135](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/1-135)`packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts` [1-6](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/1-6)

## Architecture Overview

The extension definitions are organized into three primary categories:

1. **Class Extensions**: Augmenting existing classes (e.g., `EntityPlayer`, `Game`) with new methods and properties.
2. **New Classes**: Introducing entirely new engine abstractions (e.g., `PlayerManager`, `ImGui`, `GenericPrompt`).
3. **Custom Callbacks**: Implementing `ModCallbackRepentogon`, which provides more granular and high-performance hooks than the vanilla `ModCallback`.

### System Entity Mapping

The following diagram illustrates how REPENTOGON entities bridge the gap between the game's internal state and the TypeScript API.

**REPENTOGON API Structure**

```

```

Sources: `packages/isaac-typescript-definitions-repentogon/src/types/classes/PersistentGameData.d.ts` [19-75](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/19-75)`packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts` [6-163](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/6-163)`packages/isaac-typescript-definitions-repentogon/src/types/classes/GenericPrompt.d.ts` [19-75](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/19-75)

## Key Class Extensions

REPENTOGON adds "Ex" versions of many vanilla methods to fix bugs or add parameters. For example, `EntityPlayer.AddCacheFlagsEx` allows for immediate evaluation of items.

### EntityPlayer

The `EntityPlayer` interface is heavily extended to include management of active charges, innate collectibles, and custom cache tags.

| Method | Purpose |
| --- | --- |
| `AddActiveCharge` | Adds charges to a specific active item slot. |
| `AddCustomCacheTag` | Evaluates custom stats outside the vanilla `CacheFlag` system. |
| `AddInnateCollectible` | Grants item effects without adding the item to the inventory. |
| `GetPlayerIndex` | Returns the unique index for the player entity. |

Sources: `packages/isaac-typescript-definitions-repentogon/src/types/classes/entity/EntityPlayer.d.ts` [37-176](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/37-176)

### Game and Room

The `Game` and `Room` classes receive methods for global state manipulation, such as color modifiers and environment intensity.

| Class | Method | Description |
| --- | --- | --- |
| `Game` | `SetColorModifier` | Smoothly transitions the game's global color correction. |
| `Game` | `RecordPlayerCompletion` | Unlocks achievements and marks for all players. |
| `Room` | `SetWaterAmount` | Dynamically changes the water level in the current room. |
| `Room` | `SetPauseTimer` | Freezes NPC AI and animations for a set duration. |

Sources: `packages/isaac-typescript-definitions-repentogon/src/types/classes/Game.d.ts` [12-161](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/12-161)`packages/isaac-typescript-definitions-repentogon/src/types/classes/Room.d.ts` [12-208](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/12-208)

## ModCallbackRepentogon

REPENTOGON introduces a new set of callbacks that are registered via `Mod.AddCallbackRepentogon`. These often provide better performance or more arguments than vanilla counterparts.

**Callback Data Flow**

```
Modification Examples

Return Object

{ Damage: number }

{ Collide: boolean }

Isaac Engine (REPENTOGON)

Internal Event

ModCallbackRepentogon

TypeScript Mod Logic

Modify Damage Amount

Cancel Collision
```

### Notable Callbacks

- **`PRE_ENTITY_TAKE_DMG`**: Unlike the vanilla version, this allows returning an object (e.g., `{ Damage: 10, DamageFlags: ... }`) to modify damage parameters before they are applied.
- **`POST_PICKUP_SELECTION`**: Provides the `requestedVariant` and `requestedSubType`, allowing mods to see what the game _intended_ to spawn before randomization.
- **`PRE_PLAYER_COLLISION`**: Allows fine-grained control over whether a player should collide with a specific entity.

Sources: `packages/isaac-typescript-definitions-repentogon/src/enums/ModCallbackRepentogon.ts` [26-163](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/26-163)`packages/isaac-typescript-definitions-repentogon/src/types/unofficial/AddCallbackParametersRepentogon.d.ts` [76-131](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/76-131)

## Sprite and Rendering Extensions

REPENTOGON provides deep access to the `Sprite` class, allowing mods to inspect animation data and apply custom shaders.

- **`GetAnimationData`**: Retrieves metadata for a specific animation from the `.anm2` file.
- **`SetCustomShader`**: Overrides the default `coloroffset` shader with a custom `.vs` and `.fs` file pair.
- **`ReplaceSpritesheetEx`**: Replaces a sprite layer and can optionally force an immediate `LoadGraphics` call.

Sources: `packages/isaac-typescript-definitions-repentogon/src/types/classes/sprite/Sprite.d.ts` [11-145](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/11-145)`packages/isaac-typescript-definitions-repentogon/src/types/classes/sprite/Sprite.d.ts` [101-120](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/101-120)

## Global Helper Objects

New global namespaces and classes are introduced to handle systems previously inaccessible to Lua:

1. **`PlayerManager`**: Provides functions to get total player counts and manage player-specific collections.
2. **`PersistentGameData`**: Allows reading and writing to the game's persistent save file, including bestiary counts and achievement status.
3. **`GenericPrompt`**: A class to create and display standard "Yes/No" style UI prompts (like the Victory Lap prompt).

Sources: `packages/isaac-typescript-definitions-repentogon/src/types/classes/PlayerManager.d.ts` [1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/1-10)`packages/isaac-typescript-definitions-repentogon/src/types/classes/PersistentGameData.d.ts` [19-75](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/19-75)`packages/isaac-typescript-definitions-repentogon/src/types/classes/GenericPrompt.d.ts` [19-75](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/19-75)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#repentogon-extension-definitions)
- [Architecture Overview](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#architecture-overview)
- [System Entity Mapping](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#system-entity-mapping)
- [Key Class Extensions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#key-class-extensions)
- [EntityPlayer](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#entityplayer)
- [Game and Room](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#game-and-room)
- [ModCallbackRepentogon](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#modcallbackrepentogon)
- [Notable Callbacks](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#notable-callbacks)
- [Sprite and Rendering Extensions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#sprite-and-rendering-extensions)
- [Global Helper Objects](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions#global-helper-objects)

Ask Devin about IsaacScript/isaacscript

Fast

Syntax error in textmermaid version 11.7.0

---

## 5 Linting And Code Quality Stack

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Linting & Code Quality Stack

Relevant source files

- [packages/docs/docsearch.config.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docsearch.config.json)
- [packages/eslint-config-isaacscript/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/README.md?plain=1)
- [packages/isaac-lua-polyfill/LICENSE](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/LICENSE)
- [packages/isaac-lua-polyfill/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/README.md?plain=1)
- [packages/isaac-lua-polyfill/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/src/index.ts)
- [packages/isaac-typescript-definitions-repentogon/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/README.md?plain=1)
- [packages/isaac-typescript-definitions/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/README.md?plain=1)
- [packages/isaacscript-cli/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/README.md?plain=1)
- [packages/isaacscript-common/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/README.md?plain=1)
- [packages/isaacscript-lint/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1)
- [packages/isaacscript-lua/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/README.md?plain=1)
- [packages/isaacscript-spell/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/README.md?plain=1)

The IsaacScript ecosystem employs a multi-layered linting and code quality system to ensure that TypeScript-to-Lua mods are robust, performant, and free of common pitfalls. This stack is orchestrated primarily through the `isaacscript-lint` meta-package, which bundles configuration, custom rules, and specialized dictionaries tailored for _The Binding of Isaac_ modding.

### System Overview

The linting stack bridges the gap between standard JavaScript/TypeScript tooling and the specific constraints of the Isaac Lua environment.

**Stack Components Relationship**

```
External Tools

Logic & Data

Core Configurations

Meta Package

isaacscript-lint

eslint-config-isaacscript

isaacscript-tsconfig

eslint-plugin-isaacscript

isaacscript-spell

Prettier

ESLint

CSpell
```

Sources: [packages/isaacscript-lint/README.md1-18](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L1-L18) [packages/eslint-config-isaacscript/README.md1-6](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/README.md?plain=1#L1-L6)

* * *

### isaacscript-lint: The Meta-Package

`isaacscript-lint` serves as the primary entry point for code quality in IsaacScript projects [packages/isaacscript-lint/README.md1-5](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L1-L5) It is a meta-package that simplifies dependency management by bundling everything required for a standard IsaacScript linting environment.

Key inclusions in this package:

- **`complete-lint`**: A base meta-package for ESLint and Prettier [packages/isaacscript-lint/README.md12](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L12-L12)
- **`@prettier/plugin-xml`**: Essential for formatting the `.xml` files (entities, items, etc.) common in Isaac mods [packages/isaacscript-lint/README.md11](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L11-L11)
- **`ts-prune`**: Used to identify and remove unused exports to keep the transpiled Lua bundle lean [packages/isaacscript-lint/README.md17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L17-L17)

Sources: [packages/isaacscript-lint/README.md1-18](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L1-L18)

* * *

### eslint-config-isaacscript

This package provides the master ESLint configuration used by all IsaacScript mods [packages/eslint-config-isaacscript/README.md1-5](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/README.md?plain=1#L1-L5) It composes multiple layered configurations, including base TypeScript rules, import sorting, JSDoc requirements, and specific rules for the IsaacScript monorepo.

For details on the layered config files (base, mod, monorepo) and how to extend them, see **[eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)**.

Sources: [packages/eslint-config-isaacscript/README.md1-6](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/README.md?plain=1#L1-L6)

* * *

### eslint-plugin-isaacscript: Custom Rules

Standard ESLint rules are often insufficient for the unique requirements of the Isaac Lua API. `eslint-plugin-isaacscript` implements custom rules to prevent common errors, such as:

- **`no-throw`**: Preventing the use of the JavaScript `throw` keyword, which does not behave correctly in the Isaac environment (polyfilled via `error` in some contexts) [packages/isaac-lua-polyfill/src/index.ts10-14](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/src/index.ts#L10-L14)
- **`strict-enums`**: Ensuring type safety when dealing with the game's many numeric enums.
- **`require-v-registration`**: Ensuring variables intended for save data are properly registered with the Save Data Manager.

For a full catalog of custom rules and the testing infrastructure, see **[eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)**.

Sources: [packages/isaac-lua-polyfill/src/index.ts10-14](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/src/index.ts#L10-L14)

* * *

### isaacscript-spell & isaacscript-tsconfig

Code quality extends beyond logic to include documentation and configuration consistency:

- **`isaacscript-spell`**: Provides CSpell dictionaries containing the specialized vocabulary of the Isaac API, Lua keywords, and common modding terms (e.g., "entities2.xml" contents) [packages/isaacscript-spell/README.md9-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/README.md?plain=1#L9-L20)
- **`isaacscript-tsconfig`**: Offers standardized TypeScript configurations for different environments (Mod, Node, Browser) to ensure the compiler behaves predictably across the ecosystem.

For details on dictionary word lists and tsconfig variants, see **[isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)**.

**Code Entity to Tooling Mapping**

| Tool / Package | Code Entity / Concept | Purpose |
| --- | --- | --- |
| `eslint-plugin-isaacscript` | `no-throw` | Replaces `throw` with Lua-compatible `error()` [packages/isaac-lua-polyfill/src/index.ts10-14](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/src/index.ts#L10-L14) |
| `isaacscript-spell` | `api.txt` | Validates spelling of Isaac Lua API members [packages/isaacscript-spell/README.md17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/README.md?plain=1#L17-L17) |
| `isaacscript-lint` | `ts-prune` | Detects dead code in the project [packages/isaacscript-lint/README.md17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L17-L17) |
| `isaac-lua-polyfill` | `globalThis.Isaac` | Provides stubs for linting/testing in Node.js [packages/isaac-lua-polyfill/src/index.ts42-51](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/src/index.ts#L42-L51) |

Sources: [packages/isaacscript-lint/README.md17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lint/README.md?plain=1#L17-L17) [packages/isaacscript-spell/README.md17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/README.md?plain=1#L17-L17) [packages/isaac-lua-polyfill/src/index.ts10-51](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/src/index.ts#L10-L51)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack#linting-code-quality-stack)
- [System Overview](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack#system-overview)
- [isaacscript-lint: The Meta-Package](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack#isaacscript-lint-the-meta-package)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack#eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom Rules](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack#eslint-plugin-isaacscript-custom-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack#isaacscript-spell-isaacscript-tsconfig)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 5.1 Eslint Config Isaacscript

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# eslint-config-isaacscript

Relevant source files

- [packages/docs/docsearch.config.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docsearch.config.json)
- [packages/docs/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/eslint.config.mjs)
- [packages/eslint-config-isaacscript/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/eslint.config.mjs)
- [packages/eslint-config-isaacscript/src/mod.js](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js)
- [packages/eslint-plugin-isaacscript/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/eslint.config.mjs)
- [packages/isaac-lua-polyfill/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/eslint.config.mjs)
- [packages/isaac-typescript-definitions-repentogon/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/eslint.config.mjs)
- [packages/isaac-typescript-definitions/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/eslint.config.mjs)
- [packages/isaacscript-cli/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/eslint.config.mjs)
- [packages/isaacscript-common/api-extractor.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/api-extractor.json)
- [packages/isaacscript-common/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/eslint.config.mjs)
- [packages/isaacscript-spell/eslint.config.mjs](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/eslint.config.mjs)

The `eslint-config-isaacscript` package provides a shareable ESLint configuration designed specifically for the IsaacScript ecosystem. It builds upon `eslint-config-complete` and adds specialized rules for TypeScriptToLua (TSTL) development, Isaac API conventions, and monorepo management.

## Configuration Architecture

The configuration is layered to provide sensible defaults for different project types. It leverages the ESLint "Flat Config" format (v9+), using the `defineConfig` helper from `eslint/config`.

### Core Composition

The configuration ecosystem is divided into two primary paths:

1. **Monorepo/Tooling Config**: Used for internal packages like `isaacscript-cli` or `eslint-plugin-isaacscript`. It relies on `completeConfigBase` [packages/eslint-config-isaacscript/eslint.config.mjs1-6](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/eslint.config.mjs#L1-L6)
2. **Mod Config**: Specifically tuned for Isaac mods and TSTL projects. This is exported as `isaacScriptModConfigBase` [packages/eslint-config-isaacscript/src/mod.js8-207](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L8-L207)

### Configuration Inheritance Diagram

This diagram shows how different packages in the monorepo consume and extend the base configurations.

**Config Entity Flow**

```
Consuming Packages

eslint-config-isaacscript

External Dependencies

eslint-config-complete

isaacScriptModConfigBase (mod.js)

Isaac Mod Project

isaacscript-common

isaac-typescript-definitions

isaacscript-cli
```

Sources: [packages/eslint-config-isaacscript/src/mod.js8-207](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L8-L207) [packages/isaacscript-common/eslint.config.mjs8-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/eslint.config.mjs#L8-L10) [packages/isaac-typescript-definitions/eslint.config.mjs8-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/eslint.config.mjs#L8-L10) [packages/isaacscript-cli/eslint.config.mjs3-7](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/eslint.config.mjs#L3-L7)

* * *

## The Mod Configuration (`isaacScriptModConfigBase`)

The `isaacScriptModConfigBase` is the primary entry point for mod authors. It integrates `eslint-plugin-isaacscript` and overrides several standard rules to accommodate the unique environment of the Isaac Lua API.

### Custom Rule Logic

| Rule | Setting | Reason |
| --- | --- | --- |
| `isaacscript/enum-member-number-separation` | `warn` | Enforces readability in numeric enums [packages/eslint-config-isaacscript/src/mod.js17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L17-L17) |
| `isaacscript/no-throw` | `warn` | Prevents `throw` keywords which are problematic in TSTL [packages/eslint-config-isaacscript/src/mod.js19](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L19-L19) |
| `isaacscript/require-v-registration` | `warn` | Ensures variables are registered with the Save Data Manager [packages/eslint-config-isaacscript/src/mod.js20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L20-L20) |
| `@typescript-eslint/naming-convention` | Custom | Allows `UPPER_CASE` for enum members to match vanilla Isaac docs [packages/eslint-config-isaacscript/src/mod.js45-74](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L45-L74) |
| `no-param-reassign` | `off` | Isaac API callbacks (e.g., `MC_POST_ENTITY_KILL`) often require modifying the provided object [packages/eslint-config-isaacscript/src/mod.js198-200](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L198-L200) |
| `no-bitwise` | `off` | Essential for handling Isaac bitmasks like `EntityFlag` [packages/eslint-config-isaacscript/src/mod.js190-192](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L190-L192) |

### TSTL Specific Adjustments

Because TSTL projects transpile to Lua, certain JavaScript/TypeScript restrictions are relaxed:

- **Array Sorting**: `@typescript-eslint/require-array-sort-compare` is disabled because `table.sort` in Lua does not share the coercion bugs of JavaScript's `Array.prototype.sort` [packages/eslint-config-isaacscript/src/mod.js127-132](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L127-L132)
- **This Context**: `@typescript-eslint/no-invalid-void-type` allows `this: void` as a parameter, which is a TSTL convention for static-like functions [packages/eslint-config-isaacscript/src/mod.js95-100](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L95-L100)
- **Math Truncation**: `unicorn/prefer-math-trunc` is disabled because Lua bitwise operators used for truncation are safe [packages/eslint-config-isaacscript/src/mod.js166-170](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L166-L170)

Sources: [packages/eslint-config-isaacscript/src/mod.js1-207](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/src/mod.js#L1-L207)

* * *

## Extension and Overrides

Packages within the monorepo frequently extend the base config to handle specific requirements.

### Implementation Mapping

The following diagram maps specific configuration files to their role in the system.

**Config Implementation Map**

```
Rule Sets

Logic Layer

Defines

Overrides

Overrides

Exports

mod.js

eslint.config.mjs (Root)

isaacscript/*

@typescript-eslint/*

unicorn/*
```

### Common Override Patterns

- **Export Sorting**: Packages like `isaac-typescript-definitions` and `isaacscript-common` use `eslint-plugin-sort-exports` to maintain alphabetical order in index files [packages/isaac-typescript-definitions/eslint.config.mjs13-16](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/eslint.config.mjs#L13-L16) [packages/isaacscript-common/eslint.config.mjs13-17](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/eslint.config.mjs#L13-L17)
- **Documentation Relaxing**: For definition files (`.d.ts`), `jsdoc/require-param-description` is often turned off because the vanilla API docs are often incomplete [packages/isaac-typescript-definitions/eslint.config.mjs27-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/eslint.config.mjs#L27-L31)
- **Triple-Slash Directives**: While usually discouraged in modern TypeScript, they are re-enabled for definition packages as recommended by the TSTL author [packages/isaac-typescript-definitions/eslint.config.mjs19-24](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/eslint.config.mjs#L19-L24)

Sources: [packages/isaac-typescript-definitions/eslint.config.mjs1-60](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/eslint.config.mjs#L1-L60) [packages/isaacscript-common/eslint.config.mjs1-65](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/eslint.config.mjs#L1-L65)

* * *

## Specialized Configurations

### IsaacScript CLI

The CLI package includes specific ignores for its template system. It avoids linting `file-templates` because they contain placeholders that are not valid TypeScript until processed by `isaacscript init` [packages/isaacscript-cli/eslint.config.mjs38-41](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/eslint.config.mjs#L38-L41)

### IsaacScript Common

The standard library re-enables `require-array-sort-compare` because it is cross-compiled to both Lua and JavaScript (Node.js), meaning it must remain compatible with standard JS sorting behavior [packages/isaacscript-common/eslint.config.mjs30-37](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/eslint.config.mjs#L30-L37)

### API Extractor Integration

While not strictly an ESLint config, the `api-extractor.json` in `isaacscript-common` works in tandem with the linting layer to manage the public API surface. It suppresses specific TSDoc warnings (like `tsdoc-undefined-tag`) to allow for more flexible documentation comments that the linter might otherwise flag [packages/isaacscript-common/api-extractor.json127-152](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/api-extractor.json#L127-L152)

Sources: [packages/isaacscript-cli/eslint.config.mjs37-47](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/eslint.config.mjs#L37-L47) [packages/isaacscript-common/eslint.config.mjs30-37](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/eslint.config.mjs#L30-L37) [packages/isaacscript-common/api-extractor.json127-152](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/api-extractor.json#L127-L152)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#eslint-config-isaacscript)
- [Configuration Architecture](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#configuration-architecture)
- [Core Composition](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#core-composition)
- [Configuration Inheritance Diagram](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#configuration-inheritance-diagram)
- [The Mod Configuration (\`isaacScriptModConfigBase\`)](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#the-mod-configuration-isaacscriptmodconfigbase)
- [Custom Rule Logic](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#custom-rule-logic)
- [TSTL Specific Adjustments](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#tstl-specific-adjustments)
- [Extension and Overrides](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#extension-and-overrides)
- [Implementation Mapping](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#implementation-mapping)
- [Common Override Patterns](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#common-override-patterns)
- [Specialized Configurations](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#specialized-configurations)
- [IsaacScript CLI](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#isaacscript-cli)
- [IsaacScript Common](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#isaacscript-common)
- [API Extractor Integration](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript#api-extractor-integration)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 5.2 Eslint Plugin Isaacscript: Custom Eslint Rules

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# eslint-plugin-isaacscript: Custom ESLint Rules

Relevant source files

- [README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/README.md?plain=1)
- [packages/docs/docs/main/javascript-tutorial.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1)
- [packages/docs/docs/main/right-for-me.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/right-for-me.md?plain=1)
- [packages/eslint-plugin-isaacscript/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/README.md?plain=1)
- [packages/eslint-plugin-isaacscript/src/configs.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/configs.ts)
- [packages/eslint-plugin-isaacscript/src/configs/recommended.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/configs/recommended.ts)
- [packages/eslint-plugin-isaacscript/src/rules.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules.ts)
- [packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts)
- [packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts)
- [packages/eslint-plugin-isaacscript/src/typeUtils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/typeUtils.ts)
- [packages/eslint-plugin-isaacscript/src/utils.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/utils.ts)
- [packages/eslint-plugin-isaacscript/test-rule-specific.sh](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/test-rule-specific.sh)
- [packages/eslint-plugin-isaacscript/test-rule.sh](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/test-rule.sh)
- [packages/eslint-plugin-isaacscript/tests/rules/no-invalid-default-map.test.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/tests/rules/no-invalid-default-map.test.ts)
- [packages/isaacscript-common/src/objects/coinSubTypeToValue.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/objects/coinSubTypeToValue.ts)

`eslint-plugin-isaacscript` is a collection of [ESLint](https://eslint.org/) rules specifically designed for IsaacScript mods. It ensures code quality, prevents common pitfalls in the TypeScript-to-Lua transpilation process, and enforces patterns required by the `isaacscript-common` standard library [packages/eslint-plugin-isaacscript/README.md1-5](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/README.md?plain=1#L1-L5)

## Rule Architecture and Implementation

The plugin is built using `@typescript-eslint/utils` to provide type-aware linting. Rules are defined in `packages/eslint-plugin-isaacscript/src/rules/` and exported via a central registry [packages/eslint-plugin-isaacscript/src/rules.ts1-15](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules.ts#L1-L15)

### Core Utility: `createRule`

Every custom rule is instantiated using a wrapper function, `createRule`, which automatically generates documentation URLs pointing to the GitHub repository [packages/eslint-plugin-isaacscript/src/utils.ts6-9](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/utils.ts#L6-L9)

### Type Checking Helpers

For rules requiring type information (e.g., `no-invalid-default-map`), the plugin utilizes `typeUtils.ts`. This file contains logic to:

- Decompose union types to check flags [packages/eslint-plugin-isaacscript/src/typeUtils.ts46-49](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/typeUtils.ts#L46-L49)
- Identify function-like types by checking for call signatures [packages/eslint-plugin-isaacscript/src/typeUtils.ts41-44](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/typeUtils.ts#L41-L44)
- Extract type names, including handling for `int` and `float` aliases used in IsaacScript [packages/eslint-plugin-isaacscript/src/typeUtils.ts15-35](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/typeUtils.ts#L15-L35)

**Sources:**

- [packages/eslint-plugin-isaacscript/src/utils.ts1-10](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/utils.ts#L1-L10)
- [packages/eslint-plugin-isaacscript/src/typeUtils.ts1-74](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/typeUtils.ts#L1-L74)
- [packages/eslint-plugin-isaacscript/src/rules.ts1-15](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules.ts#L1-L15)

## Custom Rules Reference

### enum-member-number-separation

**Purpose:** Disallows numbers immediately adjacent to letters in enum members (e.g., `ITEM1` must be `ITEM_1`).
**Implementation:**

- Iterates through `TSEnumMember` nodes [packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts22](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts#L22-L22)
- Whitelists short names (4 characters or less) [packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts31-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts#L31-L33)
- Uses a regex to detect digits and ensures they are bordered by underscores or other digits [packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts48-63](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts#L48-L63)

### no-invalid-default-map

**Purpose:** Prevents passing complex data structures (like new Arrays or Objects) directly into the `DefaultMap` constructor, which would lead to reference sharing across all keys.
**Implementation:**

- Uses `ESLintUtils.getParserServices` to access the TypeScript TypeChecker [packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts29-30](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts#L29-L30)
- Checks `NewExpression` for `DefaultMap` [packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts33-42](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts#L33-L42)
- Validates that the first argument is a primitive (boolean, number, string) or a factory function [packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts52-77](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts#L52-L77)

### no-throw

**Purpose:** Disallows the `throw` keyword. Since the Isaac Lua VM handles errors differently than JavaScript, throwing an exception in TypeScript can lead to hard-to-debug crashes or silent failures in the mod [packages/eslint-plugin-isaacscript/src/rules.ts13](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules.ts#L13-L13)

### require-v-registration

**Purpose:** Ensures that any variable named `v` (conventionally used for persistent state) is properly registered with the Save Data Manager to ensure it is included in the mod's save file [packages/eslint-plugin-isaacscript/README.md27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/README.md?plain=1#L27-L27)

**Sources:**

- [packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts1-73](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/enum-member-number-separation.ts#L1-L73)
- [packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts1-87](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts#L1-L87)
- [packages/eslint-plugin-isaacscript/README.md22-28](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/README.md?plain=1#L22-L28)

## Data Flow: Type-Aware Linting

The following diagram illustrates how a rule like `no-invalid-default-map` interacts with the TypeScript compiler to validate code.

### Logic Flow for Type Validation

```

```

**Sources:**

- [packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts28-85](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/rules/no-invalid-default-map.ts#L28-L85)
- [packages/eslint-plugin-isaacscript/src/typeUtils.ts41-44](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/typeUtils.ts#L41-L44)

## Testing Infrastructure

The plugin includes a dedicated testing suite using Jest. Tests are located in `packages/eslint-plugin-isaacscript/tests/rules/`.

### Testing Scripts

The monorepo provides shell scripts to streamline the development of new rules:

- **`test-rule.sh`**: Runs all Jest tests associated with a specific rule name [packages/eslint-plugin-isaacscript/test-rule.sh11-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/test-rule.sh#L11-L20)
- **`test-rule-specific.sh`**: Runs a single specific test case within a rule's test file, useful for debugging individual edge cases [packages/eslint-plugin-isaacscript/test-rule-specific.sh14-26](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/test-rule-specific.sh#L14-L26)

### Test Execution Flow

```
Rule ImplementationJest Runnertest-rule.shDeveloperRule ImplementationJest Runnertest-rule.shDeveloper./test-rule.sh no-thrownpx jest tests/rules/no-throw.test.tsExecute Rule.create(context)context.report(errors)Pass/Fail Results
```

**Sources:**

- [packages/eslint-plugin-isaacscript/test-rule.sh1-21](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/test-rule.sh#L1-L21)
- [packages/eslint-plugin-isaacscript/test-rule-specific.sh1-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/test-rule-specific.sh#L1-L27)

## Summary Table of Rules

| Rule Name | Recommended | Fixable | Type-Aware |
| --- | --- | --- | --- |
| `enum-member-number-separation` | Yes | No | No |
| `no-invalid-default-map` | Yes | No | Yes |
| `no-throw` | Yes | No | No |
| `require-v-registration` | Yes | No | No |

**Sources:**

- [packages/eslint-plugin-isaacscript/README.md22-28](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/README.md?plain=1#L22-L28)
- [packages/eslint-plugin-isaacscript/src/configs/recommended.ts10-16](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/configs/recommended.ts#L10-L16)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#eslint-plugin-isaacscript-custom-eslint-rules)
- [Rule Architecture and Implementation](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#rule-architecture-and-implementation)
- [Core Utility: \`createRule\`](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#core-utility-createrule)
- [Type Checking Helpers](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#type-checking-helpers)
- [Custom Rules Reference](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#custom-rules-reference)
- [enum-member-number-separation](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#enum-member-number-separation)
- [no-invalid-default-map](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#no-invalid-default-map)
- [no-throw](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#no-throw)
- [require-v-registration](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#require-v-registration)
- [Data Flow: Type-Aware Linting](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#data-flow-type-aware-linting)
- [Logic Flow for Type Validation](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#logic-flow-for-type-validation)
- [Testing Infrastructure](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#testing-infrastructure)
- [Testing Scripts](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#testing-scripts)
- [Test Execution Flow](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#test-execution-flow)
- [Summary Table of Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules#summary-table-of-rules)

Ask Devin about IsaacScript/isaacscript

Fast

Syntax error in textmermaid version 11.7.0

---

## 5.3 Isaacscript Spell And Isaacscript Tsconfig

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# isaacscript-spell & isaacscript-tsconfig

Relevant source files

- [packages/docs/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/tsconfig.json)
- [packages/eslint-config-isaacscript/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/tsconfig.json)
- [packages/eslint-plugin-isaacscript/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/tsconfig.json)
- [packages/isaac-lua-polyfill/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/tsconfig.json)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/ImGui.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/ImGui.d.ts)
- [packages/isaac-typescript-definitions-repentogon/src/types/classes/XMLData.d.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/src/types/classes/XMLData.d.ts)
- [packages/isaac-typescript-definitions-repentogon/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/tsconfig.json)
- [packages/isaac-typescript-definitions/src/enums/PickupPrice.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/PickupPrice.ts)
- [packages/isaac-typescript-definitions/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/tsconfig.json)
- [packages/isaacscript-cli/file-templates/dynamic/mod/metadata.xml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/mod/metadata.xml)
- [packages/isaacscript-cli/file-templates/dynamic/src/main-dev.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/src/main-dev.ts)
- [packages/isaacscript-cli/file-templates/dynamic/src/main.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/file-templates/dynamic/src/main.ts)
- [packages/isaacscript-cli/isaacscript-watcher/metadata.xml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/isaacscript-watcher/metadata.xml)
- [packages/isaacscript-cli/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/tsconfig.json)
- [packages/isaacscript-common/src/classes/DefaultMap.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/DefaultMap.ts)
- [packages/isaacscript-common/tsconfig.bundle.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.bundle.json)
- [packages/isaacscript-common/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.json)
- [packages/isaacscript-spell/dictionaries/isaac/api.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/api.txt)
- [packages/isaacscript-spell/dictionaries/isaac/cspell-ext.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/cspell-ext.json)
- [packages/isaacscript-spell/dictionaries/isaac/files.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/files.txt)
- [packages/isaacscript-spell/dictionaries/isaac/isaac.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/isaac.txt)
- [packages/isaacscript-spell/dictionaries/isaac/lua.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/lua.txt)
- [packages/isaacscript-spell/dictionaries/isaacscript/cspell-ext.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaacscript/cspell-ext.json)
- [packages/isaacscript-spell/dictionaries/isaacscript/general.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaacscript/general.txt)
- [packages/isaacscript-spell/tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/tsconfig.json)
- [packages/isaacscript-tsconfig/README.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/README.md?plain=1)
- [packages/isaacscript-tsconfig/package.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/package.json)
- [packages/isaacscript-tsconfig/tsconfig.mod.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/tsconfig.mod.json)
- [tsconfig.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/tsconfig.json)

This page documents the shared configuration packages used across the IsaacScript monorepo and by end-user mod projects. `isaacscript-spell` provides specialized dictionaries for the CSpell spell-checker, while `isaacscript-tsconfig` provides standardized TypeScript compiler configurations tailored for Isaac modding and Node.js development.

## isaacscript-spell

`isaacscript-spell` is a dictionary package that extends CSpell with terms specific to _The Binding of Isaac_ modding, the Lua programming language, and the IsaacScript ecosystem. It ensures that technical terms, item names, and API-specific identifiers do not trigger false positives during linting.

### Dictionary Structure

The package is divided into two primary dictionary sets: `isaac` and `isaacscript`.

#### 1\. Isaac Dictionary (`isaac`)

Contains words related to the game's internal files, Lua API, and community tools.

- **API Words**: Identifiers from the game's Lua API and console commands (e.g., `addplayer`, `gridspawn`, `luamod`) [packages/isaacscript-spell/dictionaries/isaac/api.txt1-207](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/api.txt#L1-L207)
- **File/Resource Words**: Attribute names and strings found in game XMLs like `entities2.xml` or `items.xml` (e.g., `addcostumeonpickup`, `cansacrifice`, `pocketitems`) [packages/isaacscript-spell/dictionaries/isaac/files.txt1-92](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/files.txt#L1-L92)
- **General Modding**: Community terms, REPENTOGON API additions, and creator names (e.g., `REPENTOGON`, `hitbox`, `Wofsauge`, `Kilburn`) [packages/isaacscript-spell/dictionaries/isaac/isaac.txt1-191](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/isaac.txt#L1-L191)
- **Lua Specifics**: Keywords and standard library functions specific to the Lua environment (e.g., `setmetatable`, `pcall`, `userdata`, `ipairs`) [packages/isaacscript-spell/dictionaries/isaac/lua.txt1-44](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/lua.txt#L1-L44)

#### 2\. IsaacScript Dictionary (`isaacscript`)

Contains general technical terms used throughout the monorepo that may be missing from standard dictionaries.

- **General Technical**: Terms like `backticks`, `bitmask`, `cyclomatic`, `transpiles`, and `vararg` [packages/isaacscript-spell/dictionaries/isaacscript/general.txt1-73](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaacscript/general.txt#L1-L73)

### Data Flow: Spell Checking Integration

The following diagram shows how these dictionaries are consumed by the linting infrastructure.

**CSpell Configuration Flow**

```
Package Configs

Dictionary Files

isaac/api.txt

isaac/files.txt

isaacscript/general.txt

isaac/cspell-ext.json

isaacscript/cspell-ext.json

eslint-config-isaacscript

User Mod Project

VS Code / CI Linting
```

Sources: [packages/isaacscript-spell/dictionaries/isaac/api.txt1-5](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaac/api.txt#L1-L5) [packages/isaacscript-spell/dictionaries/isaacscript/general.txt1-5](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/dictionaries/isaacscript/general.txt#L1-L5)

* * *

## isaacscript-tsconfig

`isaacscript-tsconfig` provides a collection of shareable `tsconfig.json` files. These configurations ensure consistency across the monorepo and simplify the setup for mod authors by abstracting away complex compiler options.

### Available Configurations

The package exports four main variants:

| Config | Purpose | Key Features |
| --- | --- | --- |
| `tsconfig.base.json` | The foundation for all other configs. | Extends `@tsconfig/strictest`. |
| `tsconfig.mod.json` | For Isaac mod projects using TSTL. | Targets Lua 5.3, includes `isaac-typescript-definitions`. |
| `tsconfig.node.json` | For Node.js tools and scripts. | Extends `@tsconfig/node-lts`. |
| `tsconfig.browser.json` | For web-based components (e.g., Docusaurus). | Configures DOM libraries. |

Sources: [packages/isaacscript-tsconfig/package.json23-32](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/package.json#L23-L32)

### Implementation in the Monorepo

The monorepo uses these configs to maintain strict typing while handling different environment requirements (Node.js vs. Lua).

#### Mod & Library Configuration

Packages like `isaacscript-common` and `isaac-typescript-definitions` extend `tsconfig.mod.json`. They often override specific options to support library builds:

- **Module System**: Forced to `CommonJS` to work around TypeScriptToLua (TSTL) limitations [packages/isaacscript-common/tsconfig.json31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.json#L31-L31)
- **Output**: `declaration` and `declarationMap` are enabled for library consumption [packages/isaac-typescript-definitions/tsconfig.json20-21](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/tsconfig.json#L20-L21)
- **TSTL Plugins**: Configurations include specific plugins like `noExtendedEnums.cjs` to ensure Lua compatibility [packages/isaacscript-common/tsconfig.json44-48](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.json#L44-L48)

#### Tooling Configuration

The CLI and scripts extend `tsconfig.node.json`. For example, `packages/isaacscript-cli/tsconfig.json` enables `sourceMap` to support better debugging in the Node.js environment [packages/isaacscript-cli/tsconfig.json15](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/tsconfig.json#L15-L15)

### Entity Relationship: Configuration Inheritance

This diagram illustrates how specific packages in the monorepo inherit from the shared configurations.

**TSConfig Inheritance Hierarchy**

```
Packages

isaacscript-tsconfig

extends

extends

extends

extends

tsconfig.base.json

tsconfig.mod.json

tsconfig.node.json

isaacscript-common/tsconfig.json

isaac-typescript-definitions/tsconfig.json

isaacscript-cli/tsconfig.json

/tsconfig.json (Monorepo Root)
```

Sources: [packages/isaacscript-common/tsconfig.json8](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.json#L8-L8) [packages/isaac-typescript-definitions/tsconfig.json8](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/tsconfig.json#L8-L8) [packages/isaacscript-cli/tsconfig.json9](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/tsconfig.json#L9-L9) [tsconfig.json11](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/tsconfig.json#L11-L11)

### Key Compiler Options

- **Strictness**: All configs leverage `@tsconfig/strictest` to enforce the highest level of type safety [packages/isaacscript-tsconfig/package.json31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/package.json#L31-L31)
- **Lua Target**: `tsconfig.mod.json` sets the `luaTarget` to `5.3`, matching the version used by _The Binding of Isaac: Repentance_ [packages/isaac-typescript-definitions/tsconfig.json43](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/tsconfig.json#L43-L43)
- **Path Resolution**: Many packages use `${configDir}` to ensure that `outDir` and `rootDir` resolve correctly regardless of where the config is extended from [packages/isaacscript-common/tsconfig.json14](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.json#L14-L14)

Sources: [packages/isaacscript-tsconfig/package.json1-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-tsconfig/package.json#L1-L33) [packages/isaacscript-common/tsconfig.json1-52](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/tsconfig.json#L1-L52) [packages/isaac-typescript-definitions/tsconfig.json1-53](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/tsconfig.json#L1-L53)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#isaacscript-spell-isaacscript-tsconfig)
- [isaacscript-spell](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#isaacscript-spell)
- [Dictionary Structure](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#dictionary-structure)
- [1\. Isaac Dictionary (\`isaac\`)](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#1-isaac-dictionary-isaac)
- [2\. IsaacScript Dictionary (\`isaacscript\`)](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#2-isaacscript-dictionary-isaacscript)
- [Data Flow: Spell Checking Integration](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#data-flow-spell-checking-integration)
- [isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#isaacscript-tsconfig)
- [Available Configurations](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#available-configurations)
- [Implementation in the Monorepo](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#implementation-in-the-monorepo)
- [Mod & Library Configuration](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#mod-library-configuration)
- [Tooling Configuration](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#tooling-configuration)
- [Entity Relationship: Configuration Inheritance](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#entity-relationship-configuration-inheritance)
- [Key Compiler Options](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig#key-compiler-options)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 6 Documentation Site (Docusaurus)

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Documentation Site (Docusaurus)

Relevant source files

- [packages/docs/docs/main/change-log.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/change-log.md?plain=1)
- [packages/docs/docs/main/features.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/features.md?plain=1)
- [packages/docs/scripts/fixIsaacScriptCommon.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts)
- [packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts)
- [packages/docs/src/css/custom.css](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/src/css/custom.css)
- [packages/docs/static/img/lua.png](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/static/img/lua.png)
- [packages/docs/static/img/typescript.png](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/static/img/typescript.png)
- [packages/eslint-plugin-isaacscript/scripts/constants.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/constants.ts)
- [packages/eslint-plugin-isaacscript/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/src/index.ts)
- [packages/isaacscript-cli/src/commands/monitor/spawnSaveDatWriter.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/spawnSaveDatWriter.ts)
- [packages/isaacscript-cli/src/commands/monitor/touchWatcherSaveDatFiles.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/commands/monitor/touchWatcherSaveDatFiles.ts)
- [packages/isaacscript-cli/src/dev.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/src/dev.ts)
- [packages/isaacscript-common/src/index.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/index.ts)
- [todo.txt](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/todo.txt)

The IsaacScript documentation site is the central hub for mod authors, providing both hand-written guides and automatically generated API references. It is built using [Docusaurus](https://docusaurus.io/) and is located in the `packages/docs` directory. The site serves as a unified interface for `isaacscript-common`, `isaac-typescript-definitions`, and general framework usage.

## API Reference Generation Pipeline

The site integrates technical documentation directly from the source code of other packages in the monorepo. This is achieved by combining [TypeDoc](https://typedoc.org/) with specialized post-processing scripts to ensure the generated Markdown fits the Docusaurus theme and structure.

### TypeDoc Integration

To generate API documentation, the system uses `typedoc-plugin-markdown`. Because the default output is often disorganized (placing all modules in a single directory), the build process involves a manual invocation followed by mutation scripts [packages/docs/scripts/fixIsaacScriptCommon.mts1-18](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts#L1-L18)

### Post-Processing Scripts

The documentation build uses two primary TypeScript scripts to "fix" the raw Markdown output from TypeDoc:

1. **`fixIsaacScriptCommon.mts`**:

   - Moves files from the flat `modules` directory into categorized subdirectories like `functions`, `features`, and `callbacks` [packages/docs/scripts/fixIsaacScriptCommon.mts177-209](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts#L177-L209)
   - Hard-codes labels for sidebars (e.g., mapping "functions" to "Helper Functions by Category") [packages/docs/scripts/fixIsaacScriptCommon.mts69-75](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts#L69-L75)
   - Generates a dedicated `extra-callbacks.md` file to expose the `ModCallbackCustom` enum as a top-level navigation item [packages/docs/scripts/fixIsaacScriptCommon.mts159-175](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts#L159-L175)
2. **`fixIsaacTypeScriptDefinitions.mts`**:

   - Processes the game's type definitions.
   - Simplifies file names (e.g., stripping prefixes like `collections_`) so they appear alphabetically by enum name in the sidebar [packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts154-175](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts#L154-L175)
   - Removes breadcrumb links and titles generated by TypeDoc that conflict with Docusaurus headers [packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts107-117](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts#L107-L117)

### API Reference Build Flow

The following diagram illustrates how code entities are transformed into documentation pages:

**Documentation Generation Workflow**

```
Docusaurus Space

Processing Space

Source Space

isaacscript-common/src/index.ts

isaac-typescript-definitions

TypeDoc + typedoc-plugin-markdown

fixIsaacScriptCommon.mts

fixIsaacTypeScriptDefinitions.mts

packages/docs/docs/

category.yml

Docusaurus Site
```

Sources: [packages/docs/scripts/fixIsaacScriptCommon.mts1-152](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts#L1-L152) [packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts1-61](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts#L1-L61)

## Sidebar and Navigation

The site structure is managed via `_category_.yml` files generated during the "fix" scripts. These files define the `label` and `position` for the Docusaurus sidebar [packages/docs/scripts/fixIsaacScriptCommon.mts101-108](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts#L101-L108)

| Sidebar Section | Source/Label | Position |
| --- | --- | --- |
| **Core** | `upgradeMod`, `constants` | 1 |
| **Helper Functions** | `functions/` directory | 2 |
| **Extra Callbacks** | `extra-callbacks.md` | 3 |
| **Extra Features** | `features/` directory | 4 |

Sources: [packages/docs/scripts/fixIsaacScriptCommon.mts101-108](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacScriptCommon.mts#L101-L108) [packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts37-47](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/fixIsaacTypeScriptDefinitions.mts#L37-L47)

## Deployment and CI

The documentation site is automatically deployed via GitHub Actions. The pipeline handles:

1. Running TypeDoc to generate raw Markdown.
2. Executing the `fix` scripts to organize the content.
3. Building the Docusaurus static site.
4. Uploading the resulting artifact for hosting.

There is also infrastructure for [Typesense](https://typesense.org/) search indexing, although it may require periodic maintenance to match the latest site structure [todo.txt4-8](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/todo.txt#L4-L8)

## User-Facing Documentation

While the API reference is auto-generated, the "Main" section contains hand-written guides. This includes the project's **Change Log**, which tracks breaking changes such as the splitting of `isaacscript-lint` or the move to ESLint flat configs [packages/docs/docs/main/change-log.md12-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/change-log.md?plain=1#L12-L27)

For details on the specific guides available to users, see [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages).

**Documentation Content Mapping**

```
Docusaurus Output

Code-to-Doc Links

Natural Language Docs

Refers to

Tracks

Tracks

features.md

change-log.md

Getting Started

isaacscript-common

isaacscript-cli

eslint-plugin-isaacscript

Top Navbar
```

Sources: [packages/docs/docs/main/features.md66-73](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/features.md?plain=1#L66-L73) [packages/docs/docs/main/change-log.md19-27](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/change-log.md?plain=1#L19-L27)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#documentation-site-docusaurus)
- [API Reference Generation Pipeline](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#api-reference-generation-pipeline)
- [TypeDoc Integration](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#typedoc-integration)
- [Post-Processing Scripts](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#post-processing-scripts)
- [API Reference Build Flow](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#api-reference-build-flow)
- [Sidebar and Navigation](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#sidebar-and-navigation)
- [Deployment and CI](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#deployment-and-ci)
- [User-Facing Documentation](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus)#user-facing-documentation)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 6.1 User Facing Documentation Pages

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# User-Facing Documentation Pages

Relevant source files

- [packages/docs/docs/main/example-mod.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/example-mod.md?plain=1)
- [packages/docs/docs/main/getting-started.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1)
- [packages/docs/docs/main/gotchas.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/gotchas.md?plain=1)
- [packages/docs/docs/main/isaacscript-in-typescript.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/isaacscript-in-typescript.md?plain=1)
- [packages/docs/docs/main/javascript-tutorial.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1)
- [packages/docs/docs/main/next-steps.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/next-steps.md?plain=1)
- [packages/docs/docs/main/right-for-me.md](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/right-for-me.md?plain=1)
- [packages/docs/docusaurus.config.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docusaurus.config.ts)
- [packages/docs/sidebars.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/sidebars.ts)
- [packages/isaac-typescript-definitions/src/enums/RoomTransitionAnim.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/src/enums/RoomTransitionAnim.ts)
- [packages/isaacscript-cli/schemas/tsconfig-isaacscript-schema.json](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/schemas/tsconfig-isaacscript-schema.json)
- [packages/isaacscript-common/src/classes/callbacks/PostSlotDestroyed.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/callbacks/PostSlotDestroyed.ts)
- [packages/isaacscript-common/src/classes/features/callbackLogic/GameReorderedCallbacks.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/callbackLogic/GameReorderedCallbacks.ts)
- [packages/isaacscript-common/src/classes/features/callbackLogic/SlotDestroyedDetection.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/callbackLogic/SlotDestroyedDetection.ts)
- [packages/isaacscript-common/src/classes/features/other/RoomHistory.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/RoomHistory.ts)
- [packages/isaacscript-common/src/classes/features/other/RunInNFrames.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/RunInNFrames.ts)
- [packages/isaacscript-common/src/classes/features/other/SaveDataManager.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/SaveDataManager.ts)
- [packages/isaacscript-common/src/classes/features/other/saveDataManager/glowingHourGlass.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/saveDataManager/glowingHourGlass.ts)
- [packages/isaacscript-common/src/classes/features/other/saveDataManager/loadFromDisk.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/saveDataManager/loadFromDisk.ts)
- [packages/isaacscript-common/src/classes/features/other/saveDataManager/saveToDisk.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/saveDataManager/saveToDisk.ts)
- [packages/isaacscript-common/src/functions/hex.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/hex.ts)
- [packages/isaacscript-common/src/functions/jsonHelpers.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/functions/jsonHelpers.ts)
- [packages/isaacscript-lua/isaacscript\_lua.py](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py)
- [packages/isaacscript-lua/publish.sh](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/publish.sh)
- [packages/isaacscript-lua/pyproject.toml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/pyproject.toml)

This page catalogs the primary documentation resources available to mod authors within the IsaacScript ecosystem. These pages are designed to guide users from initial setup through advanced TypeScript development and final mod publishing.

### Documentation Overview

The documentation is primarily hosted as a Docusaurus site, with content sourced from Markdown files and auto-generated API references [packages/docs/docusaurus.config.ts33-42](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docusaurus.config.ts#L33-L42)

| Page | Description |
| --- | --- |
| **Getting Started** | Environment setup (Node.js, VS Code) and project initialization [packages/docs/docs/main/getting-started.md1-82](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1#L1-L82) |
| **Features Overview** | High-level summary of the benefits of using IsaacScript over pure Lua. |
| **JS/TS Tutorial** | A side-by-side comparison for Lua developers transitioning to TypeScript [packages/docs/docs/main/javascript-tutorial.md1-104](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1#L1-L104) |
| **Gotchas** | Common pitfalls, including enum immutability and bit flag handling [packages/docs/docs/main/gotchas.md1-103](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/gotchas.md?plain=1#L1-L103) |
| **Example Mod** | A step-by-step walkthrough of creating a "Green Candle" item mod [packages/docs/docs/main/example-mod.md1-130](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/example-mod.md?plain=1#L1-L130) |

**Sources:** [packages/docs/docs/main/getting-started.md1-82](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1#L1-L82) [packages/docs/docs/main/javascript-tutorial.md1-104](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1#L1-L104) [packages/docs/docs/main/gotchas.md1-103](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/gotchas.md?plain=1#L1-L103) [packages/docs/docs/main/example-mod.md1-130](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/example-mod.md?plain=1#L1-L130) [packages/docs/docusaurus.config.ts33-42](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docusaurus.config.ts#L33-L42)

* * *

### Getting Started & Project Scaffolding

The entry point for any new mod is the `isaacscript init` command. This process bootstraps a project by installing dependencies and creating a standard directory structure.

**Initialization Data Flow:**

1. User runs `npx isaacscript@latest init` [packages/docs/docs/main/getting-started.md53](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1#L53-L53)
2. The CLI prompts for configuration (e.g., save slot, VS Code integration) [packages/docs/docs/main/example-mod.md30](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/example-mod.md?plain=1#L30-L30)
3. A `src/main.ts` file is generated as the code entry point [packages/docs/docs/main/getting-started.md82](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1#L82-L82)
4. The `isaacscript monitor` (or simply `npx isaacscript`) command is started to watch for changes and sync to the game's mod folder [packages/docs/docs/main/getting-started.md64-72](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1#L64-L72)

**Sources:** [packages/docs/docs/main/getting-started.md48-82](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/getting-started.md?plain=1#L48-L82) [packages/docs/docs/main/example-mod.md21-39](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/example-mod.md?plain=1#L21-L39)

* * *

### JavaScript/TypeScript for Lua Developers

A core part of the documentation is the syntax bridge. Since the Isaac API is functionally identical between Lua and TypeScript, the documentation focuses on "cosmetic" and structural differences [packages/docs/docs/main/next-steps.md35-79](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/next-steps.md?plain=1#L35-L79)

**Language Mapping Logic**

| Lua Concept | TypeScript Equivalent | Notes |
| --- | --- | --- |
| `local x = 1` | `const x = 1` or `let x = 1` | `const` is preferred for immutable values [packages/docs/docs/main/javascript-tutorial.md83-104](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1#L83-L104) |
| `..` (Concatenation) | `+` | Also supports Template Literals. |
| `~=` (Inequality) | `!==` | Strict inequality is enforced by ESLint [packages/docs/docs/main/javascript-tutorial.md233](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1#L233-L233) |
| `table.insert` | `array.push()` | Uses standard JS Array methods [packages/docs/docs/main/javascript-tutorial.md167-180](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1#L167-L180) |
| `:` (Method call) | `.` | All calls use the dot notation in TS [packages/docs/docs/main/javascript-tutorial.md63-79](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1#L63-L79) |

**Sources:** [packages/docs/docs/main/javascript-tutorial.md1-250](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/javascript-tutorial.md?plain=1#L1-L250) [packages/docs/docs/main/next-steps.md35-79](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/next-steps.md?plain=1#L35-L79)

* * *

### Advanced Concepts & Gotchas

Technical documentation covers internal mechanics that differ from standard Isaac Lua modding, specifically regarding type safety and memory management.

#### Bit Flags and Type Branding

In Lua, bit flags are simple numbers. In IsaacScript, flags like `TearFlags` use a branded type system to prevent invalid combinations [packages/docs/docs/main/gotchas.md37-57](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/gotchas.md?plain=1#L37-L57)

**Code Entity Relationship: BitFlags**
The following diagram shows how the documentation explains the transition from raw Lua numbers to TypeScript's `BitFlags<T>` system.

```
Underlying Logic

Code Entity Space (isaacscript-common)

Natural Language Space

Transpiles to

User wants to add Piercing

User wants to check for Spectral

addFlag(TearFlag.PIERCING)

hasFlag(player.TearFlags, TearFlag.SPECTRAL)

BitFlags

Bitwise OR (|) in Lua
```

**Sources:** [packages/docs/docs/main/gotchas.md37-103](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/docs/main/gotchas.md?plain=1#L37-L103)

#### Save Data Management

The `SaveDataManager` documentation explains the lifecycle of persistent mod data. It automates the `loadFromDisk` and `saveToDisk` calls during specific game events like `POST_PLAYER_INIT` and `PRE_GAME_EXIT` [packages/isaacscript-common/src/classes/features/other/SaveDataManager.ts133-174](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/SaveDataManager.ts#L133-L174)

**SaveData Lifecycle Diagram**
This diagram maps game events described in the documentation to the internal class methods that handle them.

```
saveToDisk.tsloadFromDisk.tsSaveDataManager.tsGame (C++ Engine)saveToDisk.tsloadFromDisk.tsSaveDataManager.tsGame (C++ Engine)Data loaded into 'v' globalsMitigates data loss on crashModCallback.POST_PLAYER_INITloadFromDisk(mod, saveDataMap, ...)ModCallback.POST_NEW_LEVELsaveToDisk(...)ModCallback.PRE_GAME_EXITsaveToDisk(...)
```

**Sources:** [packages/isaacscript-common/src/classes/features/other/SaveDataManager.ts88-189](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/SaveDataManager.ts#L88-L189) [packages/isaacscript-common/src/classes/features/other/saveDataManager/loadFromDisk.ts1-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/saveDataManager/loadFromDisk.ts#L1-L20) [packages/isaacscript-common/src/classes/features/other/saveDataManager/saveToDisk.ts1-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/src/classes/features/other/saveDataManager/saveToDisk.ts#L1-L20)

* * *

### Lua Compatibility (isaacscript-lua)

For authors who prefer pure Lua but want the benefits of the `isaacscript-common` standard library, the documentation points to the `isaacscript-lua` Python tool [packages/isaacscript-lua/isaacscript\_lua.py24-30](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py#L24-L30)

Key functions documented for Lua users:

- `install`: Downloads the latest `isaacscript-common.lua` bundle from `unpkg` [packages/isaacscript-lua/isaacscript\_lua.py80-108](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py#L80-L108)
- `update`: Checks the local version against the `npms.io` API and upgrades if necessary [packages/isaacscript-lua/isaacscript\_lua.py110-152](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py#L110-L152)

**Sources:** [packages/isaacscript-lua/isaacscript\_lua.py1-203](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-lua/isaacscript_lua.py#L1-L203)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#user-facing-documentation-pages)
- [Documentation Overview](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#documentation-overview)
- [Getting Started & Project Scaffolding](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#getting-started-project-scaffolding)
- [JavaScript/TypeScript for Lua Developers](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#javascripttypescript-for-lua-developers)
- [Advanced Concepts & Gotchas](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#advanced-concepts-gotchas)
- [Bit Flags and Type Branding](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#bit-flags-and-type-branding)
- [Save Data Management](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#save-data-management)
- [Lua Compatibility (isaacscript-lua)](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages#lua-compatibility-isaacscript-lua)

Ask Devin about IsaacScript/isaacscript

Fast

---

## 7 Infrastructure And Cicd

Index your code with Devin

[DeepWiki](https://deepwiki.com/)

[DeepWiki](https://deepwiki.com/)

[IsaacScript/isaacscript](https://github.com/IsaacScript/isaacscript "Open repository")

Index your code with

Devin
Edit WikiShare

Last indexed: 3 April 2026 ( [e59e2f](https://github.com/IsaacScript/isaacscript/commits/e59e2f26))

- [IsaacScript Overview](https://deepwiki.com/IsaacScript/isaacscript/1-isaacscript-overview)
- [Getting Started & Project Setup](https://deepwiki.com/IsaacScript/isaacscript/1.1-getting-started-and-project-setup)
- [Monorepo Architecture & Package Dependency Graph](https://deepwiki.com/IsaacScript/isaacscript/1.2-monorepo-architecture-and-package-dependency-graph)
- [Using IsaacScript in Lua (Without TypeScript)](https://deepwiki.com/IsaacScript/isaacscript/1.3-using-isaacscript-in-lua-(without-typescript))
- [isaacscript-cli: The Command-Line Tool](https://deepwiki.com/IsaacScript/isaacscript/2-isaacscript-cli:-the-command-line-tool)
- [Monitor Command & Development Watcher](https://deepwiki.com/IsaacScript/isaacscript/2.1-monitor-command-and-development-watcher)
- [Init, Check, and Publish Commands](https://deepwiki.com/IsaacScript/isaacscript/2.2-init-check-and-publish-commands)
- [Custom Stage Pipeline](https://deepwiki.com/IsaacScript/isaacscript/2.3-custom-stage-pipeline)
- [TSTL Plugins & Code Generation](https://deepwiki.com/IsaacScript/isaacscript/2.4-tstl-plugins-and-code-generation)
- [isaacscript-common: The Standard Library](https://deepwiki.com/IsaacScript/isaacscript/3-isaacscript-common:-the-standard-library)
- [ModUpgraded, ModFeature & Callback System](https://deepwiki.com/IsaacScript/isaacscript/3.1-modupgraded-modfeature-and-callback-system)
- [Custom Callbacks (ModCallbackCustom)](https://deepwiki.com/IsaacScript/isaacscript/3.2-custom-callbacks-(modcallbackcustom))
- [Save Data Manager](https://deepwiki.com/IsaacScript/isaacscript/3.3-save-data-manager)
- [Room, Level & Grid Entity Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.4-room-level-and-grid-entity-helpers)
- [Entity, Player & Collectible Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.5-entity-player-and-collectible-helpers)
- [Utility & Data Structure Helpers](https://deepwiki.com/IsaacScript/isaacscript/3.6-utility-and-data-structure-helpers)
- [Optional ISCFeatures Reference](https://deepwiki.com/IsaacScript/isaacscript/3.7-optional-iscfeatures-reference)
- [Type Definitions: isaac-typescript-definitions & REPENTOGON](https://deepwiki.com/IsaacScript/isaacscript/4-type-definitions:-isaac-typescript-definitions-and-repentogon)
- [Base Game API Definitions (isaac-typescript-definitions)](https://deepwiki.com/IsaacScript/isaacscript/4.1-base-game-api-definitions-(isaac-typescript-definitions))
- [REPENTOGON Extension Definitions](https://deepwiki.com/IsaacScript/isaacscript/4.2-repentogon-extension-definitions)
- [Linting & Code Quality Stack](https://deepwiki.com/IsaacScript/isaacscript/5-linting-and-code-quality-stack)
- [eslint-config-isaacscript](https://deepwiki.com/IsaacScript/isaacscript/5.1-eslint-config-isaacscript)
- [eslint-plugin-isaacscript: Custom ESLint Rules](https://deepwiki.com/IsaacScript/isaacscript/5.2-eslint-plugin-isaacscript:-custom-eslint-rules)
- [isaacscript-spell & isaacscript-tsconfig](https://deepwiki.com/IsaacScript/isaacscript/5.3-isaacscript-spell-and-isaacscript-tsconfig)
- [Documentation Site (Docusaurus)](https://deepwiki.com/IsaacScript/isaacscript/6-documentation-site-(docusaurus))
- [User-Facing Documentation Pages](https://deepwiki.com/IsaacScript/isaacscript/6.1-user-facing-documentation-pages)
- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)
- [Glossary](https://deepwiki.com/IsaacScript/isaacscript/8-glossary)

Menu

# Infrastructure & CI/CD

Relevant source files

- [.github/workflows/ci.yml](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml)
- [knip.config.js](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/knip.config.js)
- [packages/docs/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/build.mts)
- [packages/docs/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/lint.mts)
- [packages/eslint-config-isaacscript/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-config-isaacscript/scripts/lint.ts)
- [packages/eslint-plugin-isaacscript/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/eslint-plugin-isaacscript/scripts/lint.ts)
- [packages/isaac-lua-polyfill/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-lua-polyfill/scripts/lint.ts)
- [packages/isaac-typescript-definitions-repentogon/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/scripts/build.mts)
- [packages/isaac-typescript-definitions-repentogon/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions-repentogon/scripts/lint.mts)
- [packages/isaac-typescript-definitions/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/scripts/build.mts)
- [packages/isaac-typescript-definitions/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaac-typescript-definitions/scripts/lint.mts)
- [packages/isaacscript-cli/scripts/build.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/build.ts)
- [packages/isaacscript-cli/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/lint.ts)
- [packages/isaacscript-common/scripts/build.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/scripts/build.mts)
- [packages/isaacscript-common/scripts/lint.mts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/scripts/lint.mts)
- [packages/isaacscript-spell/scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/scripts/lint.ts)
- [scripts/lint.ts](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/scripts/lint.ts)

The IsaacScript monorepo utilizes a standardized infrastructure for building, linting, and testing its constituent packages. This infrastructure ensures that changes to the core logic, CLI, or type definitions do not introduce regressions across the ecosystem.

## Infrastructure Overview

The monorepo infrastructure is built on **GitHub Actions** for automation and a set of **TypeScript-based scripts** for local and remote execution. Every package within the `packages/` directory follows a consistent pattern for lifecycle scripts (e.g., `npm run build`, `npm run lint`).

### System Relationship Diagram

The following diagram illustrates how the root orchestration scripts interact with individual package scripts and the CI environment.

**Infrastructure Orchestration Flow**

```
Per-Package Scripts

Root Orchestration

CI Environment (GitHub Actions)

Calls

Calls

.github/workflows/ci.yml

./.github/workflows/setup

scripts/lint.ts

packages/*/scripts/lint.ts

packages/*/scripts/build.ts

tsc --noEmit

eslint
```

Sources: [.github/workflows/ci.yml5-94](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L5-L94) [scripts/lint.ts6-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/scripts/lint.ts#L6-L33) [packages/isaacscript-cli/scripts/lint.ts17-24](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/lint.ts#L17-L24)

## GitHub Actions CI Pipeline

The primary CI pipeline is defined in `.github/workflows/ci.yml`. It uses a dynamic matrix strategy to parallelize jobs across all packages that contain specific scripts.

- **Dynamic Matrix**: The pipeline uses `complete-ts/get-package-names` to detect which packages have `build`, `lint`, or `test` scripts defined in their `package.json` [.github/workflows/ci.yml13-15](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L13-L15) [.github/workflows/ci.yml43-45](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L43-L45)
- **Job Types**:

  - **Build**: Compiles TypeScript/TSTL code and generates artifacts (like Docusaurus builds) [.github/workflows/ci.yml17-35](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L17-L35)
  - **Lint**: Runs static analysis across the codebase [.github/workflows/ci.yml47-58](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L47-L58)
  - **Test**: Executes unit tests, specifically increasing memory via `NODE_OPTIONS='--max-old-space-size=8192'` to handle heavy ESLint plugin tests [.github/workflows/ci.yml71-87](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L71-L87)
- **Notifications**: If any part of the pipeline fails, a notification is sent to a Discord webhook [.github/workflows/ci.yml176-187](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L176-L187)

For details on the pipeline configuration and the `setup` composite action, see **[GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7.1-github-actions-ci-pipeline)**.

Sources: [.github/workflows/ci.yml1-187](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/.github/workflows/ci.yml#L1-L187)

## Per-Package Build & Lint Scripts

While the CI orchestrates the high-level jobs, the actual logic for building and linting resides within each package's `scripts/` directory. These scripts typically use `complete-node` helpers to run commands.

### Build Infrastructure

The build process varies significantly by package:

- **isaacscript-cli**: Copies shared enums and interfaces from other packages into its source tree to satisfy build requirements before compiling [packages/isaacscript-cli/scripts/build.ts40-45](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/build.ts#L40-L45)
- **isaacscript-common**: Performs a dual-build: one for standard TypeScript/JavaScript (for tests) and a bundled version for Lua consumers using TSTL [packages/isaacscript-common/scripts/build.mts11-31](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/scripts/build.mts#L11-L31) It also uses `api-extractor` to scrub internal exports from `.d.ts` files [packages/isaacscript-common/scripts/build.mts64-66](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/scripts/build.mts#L64-L66)
- **docs**: Orchestrates TypeDoc generation for `isaac-typescript-definitions` and `isaacscript-common` before running the Docusaurus build [packages/docs/scripts/build.mts16-37](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/docs/scripts/build.mts#L16-L37)

### Lint Infrastructure

Linting is multi-layered. Package-level `lint.ts` scripts run standard tools like `tsc`, `eslint`, and `prettier`, but also include specialized checks:

- **Spell Checking**: `isaacscript-spell` validates that dictionaries are unique and alphabetically sorted [packages/isaacscript-spell/scripts/lint.ts22-78](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/scripts/lint.ts#L22-L78)
- **Template Drift**: The CLI linter checks if `Node.gitignore` matches the latest upstream version [packages/isaacscript-cli/scripts/lint.ts26-40](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/lint.ts#L26-L40)
- **Monorepo Consistency**: The root `lint.ts` ensures `package.json` files across the monorepo are synchronized [scripts/lint.ts31-32](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/scripts/lint.ts#L31-L32)

For details on individual script implementations and the `lintCommands` helper, see **[Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7.2-per-package-build-and-lint-scripts)**.

Sources: [packages/isaacscript-cli/scripts/build.ts20-29](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-cli/scripts/build.ts#L20-L29) [packages/isaacscript-common/scripts/build.mts1-42](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-common/scripts/build.mts#L1-L42) [packages/isaacscript-spell/scripts/lint.ts15-20](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/packages/isaacscript-spell/scripts/lint.ts#L15-L20) [scripts/lint.ts1-33](https://github.com/IsaacScript/isaacscript/blob/e59e2f26/scripts/lint.ts#L1-L33)

Dismiss

Refresh this wiki

Enter email to refresh

### On this page

- [Infrastructure & CI/CD](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd#infrastructure-cicd)
- [Infrastructure Overview](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd#infrastructure-overview)
- [System Relationship Diagram](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd#system-relationship-diagram)
- [GitHub Actions CI Pipeline](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd#github-actions-ci-pipeline)
- [Per-Package Build & Lint Scripts](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd#per-package-build-lint-scripts)
- [Build Infrastructure](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd#build-infrastructure)
- [Lint Infrastructure](https://deepwiki.com/IsaacScript/isaacscript/7-infrastructure-and-cicd#lint-infrastructure)

Ask Devin about IsaacScript/isaacscript

Fast

---

