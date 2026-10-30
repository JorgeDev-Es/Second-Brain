This document contains the complete source code of the repository consolidated into a single file for streamlined AI analysis.
The repository contents have been processed and combined with security validation bypassed.

# Repository Overview

## About This Document
This consolidated file represents the complete codebase from the repository, 
merged into a unified document optimized for AI consumption and automated 
analysis workflows.

## Repository Information
- **Repository:** IsaacScript/isaacscript
- **Branch:** main
- **Total Files:** 1294
- **Generated:** 2026-10-02T02:06:30.671Z

## Document Structure
The content is organized in the following sequence:
1. This overview section
2. Repository metadata and information  
3. File system hierarchy
4. Repository files (when included)
5. Individual source files, each containing:
   a. File path header (## File: path/to/file)
   b. Complete file contents within code blocks

## Best Practices
- Treat this document as read-only - make changes in the original repository
- Use file path headers to navigate between different source files
- Handle with appropriate security measures as this may contain sensitive data
- This consolidated view is generated from the live repository state

## Important Notes
- Files excluded by .gitignore and configuration rules are omitted
- Binary assets are not included - refer to the file structure for complete file listings
- Default ignore patterns have been applied to filter content
- Security validation is disabled - review content for sensitive information carefully

# Repository Structure

```
IsaacScript/isaacscript/
└── packages
    └── docs
        └── content
            ├── main
            │   ├── converting-lua-code.md
            │   ├── custom-stages.md
            │   ├── directory-structure.md
            │   ├── discord.md
            │   ├── enums-and-objects.md
            │   ├── example-mod.md
            │   ├── extra-callbacks.md
            │   ├── features.md
            │   ├── getting-started.md
            │   ├── gotchas.md
            │   ├── isaacscript-in-lua.md
            │   ├── javascript-tutorial.md
            │   ├── mod-feature.md
            │   ├── next-steps.md
            │   ├── publishing-to-the-workshop.md
            │   ├── right-for-me.md
            │   ├── updating-isaacscript.md
            │   ├── using-get-data.md
            │   └── what-is-isaacscript-doing.md
            └── homepage.mdx
```

================================================================================
// File: packages/docs/content/homepage.mdx
================================================================================
---
title: IsaacScript
description: "Write Binding of Isaac: Repentance mods with TypeScript."
editUrl: false
template: splash
hero:
  tagline: Write Binding of Isaac Repentance mods with TypeScript
  image:
    file: ../../assets/isaacscript-logo.png
    alt: IsaacScript
  actions:
    - text: Why should I?
      link: /main/features/
      icon: right-arrow
      variant: secondary
    - text: Get Started
      link: /main/getting-started/
      icon: right-arrow
      variant: primary
---

<section class="home-transformer">
  <div class="home-transformer__grid">
    ```typescript title="mod.ts"
    const entities = Isaac.GetRoomEntities();
    const deadEntities = entities.filter(
      (entity) => entity.IsDead(),
    );
    ```

    <div class="home-transformer__arrow" aria-hidden="true">
      <svg viewBox="0 0 24 24">
        <path d="M4 12h16m-6-6 6 6-6 6" />
      </svg>
    </div>

    ```lua title="mod.lua"
    local entities = Isaac.GetRoomEntities()
    local deadEntities = {}
    for _, entity in ipairs(entities) do
      if entity:IsDead() then
        table.insert(deadEntities, entity)
      end
    end
    ```

  </div>
</section>

================================================================================
// File: packages/docs/content/main/converting-lua-code.md
================================================================================
---
title: Converting Lua Code
---

Sometimes, you might want to convert an old mod written in Lua to TypeScript.
There are two ways to do this.

<br />

## LuaToTypeScript

Hazzard993 wrote
[a tool to automatically convert Lua to TypeScript](https://github.com/hazzard993/LuaToTypeScript).
This works great and is probably what you will want to use. Note that it does
not convert comments, so you might want to manually transfer those over
afterward. <!-- cspell:ignore Hazzard -->

<br />

## Manually With a Macro

If you want more fine-grained control over converting your code, then you can
also do it manually with a macro. Here's a quick tutorial to convert code using
a simple macro.

<br />

### 1) Install the ssmacro Extension

[ssmacro](https://marketplace.visualstudio.com/items?itemName=joekon.ssmacro) is
a popular VS Code extension that allows you to make macros.

<br />

### 2) Download the Macro

I've written
[a short macro](https://raw.githubusercontent.com/IsaacScript/isaacscript/main/misc/convert-lua-to-typescript.json)
that does some basic conversions. For example, it converts `local` to `let`,
`and` to `&&`, and so forth. (Feel free to customize it to your liking.)

Download it to the following directory:
`C:\Users\%USERNAME%\.vscode\extensions\joekon.ssmacro-0.6.0\macros`
<!-- cspell:ignore joekon -->

<br />

### 3) Make a Keyboard Shortcut

You can set up a keyboard shortcut to automatically execute the macro.

In VS Code, type Ctrl + Shift + P, then type in "Preferences: Open Keyboard
Shortcuts (JSON)". Then, add a keybinding like so:

```jsonc
// Place your key bindings in this file to override the defaults
[
  {
    "key": "ctrl+shift+alt+v",
    "command": "ssmacro.macro",
    "args": { "file": "convert-lua-to-typescript.json" },
  },
]
```

<br />

### 4) Open a Lua File and Convert It

Open a big Lua file and use the hotkey to perform the replacements on everything
in the file.

<br />

### 5) Copy It Over One Function at a Time

If you copy an entire file into your TypeScript project at once, then it will be
kind of a mess and the auto-formatter won't work. Instead, just copy one
function at a time into the corresponding TypeScript file, fix the errors, if
any, and let the auto-formatter do the work of arranging everything properly.
(You run the auto-formatter by simply saving the file, since it is configured by
default to run on save.)

A lot of the time, you won't be able to fix some of the errors, like functions
that are being called that are not declared yet. Just ignore those until you get
everything copied over.

================================================================================
// File: packages/docs/content/main/custom-stages.md
================================================================================
---
title: Custom Stages
---

<!-- markdownlint-disable MD001 -->
<!-- markdownlint-disable MD029 -->

Wanting to create a custom Binding of Isaac stage is common. But the vanilla API
does not have support for this. IsaacScript offers support for custom stages as
part of its standard library. See the
[getting started section](#getting-started) below.

Historically, people have used the
[StageAPI](https://github.com/Meowlala/BOIStageAPI15) library to build custom
stages, but using IsaacScript over StageAPI has several advantages. See the
[motivation section](#motivation) below.

<br />

## Getting Started

First, make sure that you are familiar with IsaacScript and have built a
practice mod or two. (See the [getting started](/main/getting-started/) guide.)

<br />

### Step 1 - Make Your Rooms

#### Create Rooms Using Basement Renovator

The most important part of a custom stage is custom rooms. So, you'll need to
make some custom rooms for your custom stage.

Isaac comes with a room editor, but it no longer works with the Repentance DLC.
Instead, you are supposed to build custom rooms using the community-built
[Basement Renovator](https://github.com/Basement-Renovator/basement-renovator)
program.

Using Basement Renovator to make rooms is outside of the scope of this tutorial,
but it is pretty self-explanatory. You can read the GitHub readme for more
details, if needed. Start a new file and start building some rooms.

#### Room Shapes and Door Slots

Most of your rooms will probably be standard 1x1 rooms with all 4 doors enabled.
(A brown door represents that it is enabled, and a grey door represents that it
is disabled.) However, you will also need to throw in some rooms of other
shapes. This is because when IsaacScript goes to deploy your custom rooms, it
will match the vanilla rooms that are generated by the game.

For example, if you use Caves 1 as a base for your stage (more on that later),
then the vanilla floor generation algorithm might randomly choose to generate
this room:

<img src="/img/2x2-room.png" />

This is a 2x2 room. When IsaacScript goes to replace this room, it will look
through your rooms for a matching room - a 2x2 room with only doors on the left
and right sides. If it doesn't find any, then it will revert to just use _any_
2x2 room. If it can't find any 2x2 rooms, then it will give up, and leave the
room as-is, and generate an error message in the console.

This means that if you want to have 100% custom rooms generated for your custom
stage, you must have at least one room for every room shape.

#### Saving Your Work

Once you have created your rooms, save them as an XML file in the following
location:

```text
project/customStages/foo.xml
```

(This assumes that your mod is called "project" and your custom stage is called
"foo".)

You don't need to include the corresponding STB file; all IsaacScript needs is
the XML.

Note that you can actually save the XML file anywhere you like, as long as the
path lines up with what you specify in the `tsconfig.json` file (more on that
later). You should probably not put it in your "mod" directory though, since the
XML file does not actually need to be uploaded to the Steam Workshop.

<br />

### Step 2 - Set Up `tsconfig.json`

After you have created your rooms and saved them as an XML file, the next step
to tell IsaacScript about them. You define and configure your custom stages by
adding information to the `tsconfig.json` file. (This is the TypeScript
configuration file. It is already included with every IsaacScript mod, and lives
in the root of your project.)

First, make sure that it has a "$schema" field at the top:

```jsonc
// We specify the schema to get auto-complete and validation.
"$schema": "https://raw.githubusercontent.com/IsaacScript/isaacscript/main/packages/isaacscript-cli/schemas/tsconfig-isaacscript-schema.json",
```

Second, make sure it has an "isaacscript" field at the bottom:

```jsonc
// IsaacScript settings
"isaacscript": {
  // A list of objects that represent the custom stages that are in your mod, if any. See:
  // https://isaacscript.github.io/main/custom-stages
  "customStages": [
    {
      "name": "Foo",
      "xmlPath": "./customStages/foo.xml",
      "roomVariantPrefix": 100,
    },
  ],
},
```

For the most basic stage, only the `name`, `xmlPath`, and `roomVariantPrefix`
fields are required. But you will likely want to make additional customizations.
There are many more optional fields that you can specify, like `baseStage` to
specify what vanilla floor number should be used as a base for the stage. These
optional fields are documented in the
[`CustomStageTSConfig` interface](/isaacscript-common/interfaces/customstagetsconfig/),
so keep that in mind.

When you are first building and testing your custom stage, you can use a
`roomVariantPrefix` of 100. However, before you publish your mod to the Steam
Workshop, you need to update this to a unique number that won't conflict with
any other mods. For more information, see the
[Custom Stage Room Variant Prefixes](#custom-stage-room-variant-prefixes)
section below.

<br />

### Step 3 - Upgrade Your Mod

You must upgrade your mod with `ISCFeature.CUSTOM_STAGES`. (This is similar to
how we use the other features of `isaacscript-common`.)

Furthermore, if you intend for the player to travel to your custom stage by
using a trapdoor, then you will probably want to also use the "custom trapdoors"
feature. If so, then you need to additionally use `ISCFeature.CUSTOM_TRAPDOORS`.

Specifically, upgrading your mod should look something like this:

#### `mod.ts`

```ts
import { ISCFeature, upgradeMod } from "isaacscript-common";

const MOD_NAME = "isaacscript-mod-example";
const modVanilla = RegisterMod(MOD_NAME, 1);
const features = [
  ISCFeature.CUSTOM_STAGES,
  ISCFeature.CUSTOM_TRAPDOORS,
] as const;
export const mod = upgradeMod(modVanilla, features);
```

(With a `mod.ts` file like this, you can then import the `mod` object from
elsewhere in your codebase and use methods such as `setCustomStage` and
`spawnCustomTrapdoor`. More on that in the next step.)

<br />

### Step 4 - Add a Trapdoor to Go There

Once you have created your custom rooms and defined your custom stage in the
`tsconfig.json` file, you need to add some code to your mod to generate a way
for the player to get there. Obviously, the specifics of this will depend on how
you want your custom stage to work. Maybe you want to add an additional trapdoor
next to the Downpour trapdoor, or maybe you want to add an additional trapdoor
inside of the Basement 1 shop.

As an example, let's imagine that we want a trapdoor to appear in the top-left
hand corner of the starting room of the run. To create a custom trapdoor, we
simply use the `spawnCustomTrapdoor` helper function (which is provided by
`ISCFeature.CUSTOM_TRAPDOORS`).

```ts
import { LevelStage, ModCallback } from "isaac-typescript-definitions";
import { mod } from "./mod";

const TOP_LEFT_CORNER_GRID_INDEX = 32;

mod.AddCallback(ModCallback.POST_GAME_STARTED, postGameStarted);

function postGameStarted(isContinued: boolean) {
  if (isContinued) {
    return;
  }

  mod.spawnCustomTrapdoor(
    TOP_LEFT_CORNER_GRID_INDEX,
    "Foo",
    LevelStage.BASEMENT_1,
  );
}
```

Here, "Foo" is the name of our custom stage and `LevelStage.BASEMENT_1` means
"the first floor". Now, by jumping into the trapdoor, the player will be taken
to the custom stage of "Foo 1". That's all we need to do!

If you specifically wanted to take the player to "Foo 2", then you would specify
`LevelStage.BASEMENT_2` instead. There are also other optional arguments that
you can use; see the documentation for the
[`spawnCustomTrapdoor`](/isaacscript-common/classes/features/other/customtrapdoors/#spawncustomtrapdoor)
method.

If you want to code some custom way to travel to the custom stage that does not
involve a trapdoor, you can do that too. See the following section.

<br />

### Going There With a Hotkey

During development, you might want to set up a custom hotkey to warp to your
custom stage, which will speed up the testing process. You can do this with the
`setCustomStage` helper function. If doing this, you must also call the
`reloadRoom` function immediately afterwards to prevent being dragged into the
`goto` console command room.

(If you want to use custom hotkeys, make sure that you upgrade your mod with
`ISCFeature.CUSTOM_HOTKEYS`.)

For example:

```ts
mod.setHotkey(Keyboard.F1, () => {
  mod.setCustomStage("Foo");
  reloadRoom();
});
```

<br />

## Reference Implementation

If you want to dive into an actual working example, you can find a
[reference mod](https://github.com/IsaacScript/isaacscript-mod-example) on
GitHub that creates a new custom stage called "Slaughterhouse". This is a
minimal mod, with only one room per floor shape, using the code snippets that we
have already seen above.

<br />

## Bosses

If your custom stage does not have any custom bosses, then a vanilla boss will
appear in the boss room corresponding to the base stage and base stage type that
you have specified. For example, if you chose Caves 1 as a base, then you would
randomly get a boss of Chub, C.H.A.D., Gurdy, and so on.

On the other hand, if you specify the `bossPool` field in the `tsconfig.json`
file, then the stage library will replace the vanilla boss room with a randomly
selected one from the pool.

For example, imagine that your custom stage had two bosses, Alice and Bob.
First, we would create them in the `entities2.xml` file, like we would for any
other custom NPC:

```xml
<entity name="Alice" anm2path="custom-bosses/alice.anm2" baseHP="234" boss="1" champion="0" collisionDamage="1" collisionMass="20" collisionRadius="20" friction="1" gridCollision="walls" numGridCollisionPoints="12" portrait="111" shadowSize="30" stageHP="0" variant="0">
  <gibs amount="10" blood="1" bone="0" eye="1" gut="1" large="1" />
</entity>

<entity name="Bob" anm2path="custom-bosses/bob.anm2" baseHP="234" boss="1" champion="0" collisionDamage="1" collisionMass="20" collisionRadius="20" friction="1" gridCollision="walls" numGridCollisionPoints="12" portrait="111" shadowSize="30" stageHP="0" variant="0">
  <gibs amount="10" blood="1" bone="0" eye="1" gut="1" large="1" />
</entity>
```

(We should not specify the `bossID` field when declaring our entities here -
that isn't needed.)

Second, we would create rooms for each boss in Basement Renovator. Make sure
that each room has a type of a Boss Room, and an arbitrarily chosen sub-type
corresponding to the boss. For example, we'll choose Alice to have a sub-type of
1, and Bob to have a sub-type of 2.

On the right-hand side of Basement Renovator, you can right click on the room in
order to change its type and sub-type. The top-most field is the type, which
defaults to "Normal Room". The bottom-most filed is the sub-type, which defaults
to 0.

Third, we need to specify our bosses in the `bossPool` field of our
`tsconfig.json` file:

```ts
"bossPool": [
  {
    "name": "Alice",
    "subType": 1,
    "weight": 3,
  },
  {
    "name": "Bob",
    "subType": 2,
    "weight": 1,
  },
],
```

Here, we map the name of the boss to the arbitrarily chosen sub-type. By
specifying a sub-type of 1 for Alice, IsaacScript will automatically choose a
random boss room matching that sub-type.

We also specify what the weight should be for each boss. In this case, we
specified a weight of 3 for Alice, meaning that it will be three times as likely
for Alice to appear than Bob. Use a weight of 1 for all of your bosses if you
want them all to be equally likely to appear.

Now, we can test the bosses in-game, and everything should work as expected.

Note that it is possible to have vanilla bosses in the boss pool, if needed.
Thus, we could have a boss pool with a mix of custom bosses and vanilla bosses,
or a boss pool of only vanilla bosses. To add a vanilla boss, just use the name
that matches the real name of the entity, and use the sub-type corresponding to
the [`BossID`](/isaac-typescript-definitions/enums/bossid/) enum. (And make sure
that you create the corresponding rooms for the sub-type in your XML file.)

<br />

## Motivation

[StageAPI](https://github.com/Meowlala/BOIStageAPI15) is a fantastic library
created by
[DeadInfinity](https://steamcommunity.com/profiles/76561198172774482/myworkshopfiles/?appid=250900)
and
[BudJMT](https://steamcommunity.com/profiles/76561198067029619/myworkshopfiles/?appid=250900),
the two smartest people in the Isaac community. Until 2022, it has been the
engine that has powered all Isaac mods that have custom stages, like
[Revelations](https://steamcommunity.com/sharedfiles/filedetails/?id=1536643474)
and
[Fiend Folio](https://steamcommunity.com/sharedfiles/filedetails/?id=2305131709).
However, no library is perfect. I wanted to try and improve on Stage API with
the following goals in mind:

<!--lint disable ordered-list-marker-value -->
<!--lint disable heading-increment -->

#### 1. An Isaac library should be dead-easy to use

- Creating a new stage should be as easy as specifying some values in a config
  file and then calling `spawnCustomTrapdoor`.
- Everything complicated should be abstracted away, with the ability to
  customize if needed.
- Auto-complete on functions and methods should work automatically. Just start
  typing.

#### 2. An Isaac library should be safe

- Creating stages can get complicated. You should immediately know if you are
  using a function incorrectly. You should never be running around in-game,
  troubleshooting run-time errors.
- It should be impossible to push broken code to production.

#### 3. An Isaac library should work without being a Workshop dependency

- When a user wants to play a mod, they should only have to subscribe to one
  thing on the Steam Workshop. Forcing the end-user to subscribe to multiple
  things is painful, complex, and unnecessary.
- Having stage logic bundled with the mod preserves backwards compatibility and
  ensures that stage logic is tightly-coupled to the mod logic that is using it.
- Having stage logic bundled with the mod allows the mod author to be in
  complete control of when they update to the latest version, if ever. This also
  allows the upstream library to make breaking changes and stay clean without
  having to worry about having perpetual technical debt (like Stage API).

#### 4. An Isaac library should use real XML/STB files

- StageAPI forces people to convert their XML files to something called "Lua
  rooms", which is XML data converted to Lua. It then imports the Lua rooms at
  run-time and manually deploys their contents.
- Lua rooms are, in essence, the biggest hack in the history of Isaac modding. A
  lot of code is dedicated to making it all work. (You have to architect a
  solution for loading empty room data, work around grid entities not spawning
  properly, handle special entities like Slides, and so on.)
- But what if there was a better way? There's no need to go down this rabbit
  hole. The IsaacScript library uses real XML/STB files, and lazy-loads their
  data when needed using the `goto` command, resulting in a completely seamless
  experience.
- This means that for people creating new stages, things are ultra simple - no
  Basement Renovator hooks required!

#### 5. An Isaac library should be compatible with other Isaac libraries

- No library should irreparably alter the base game. In other words, it should
  make no vanilla resource replacements. This is the same principle as
  [not importing for side effects](https://github.com/Zamiell/isaac-faq/blob/main/mod-organization.md#avoiding-side-effects).
- With no resource replacements, there's never a compatibility issue. Each mod
  can use their own library for their own stage.

#### 6. An Isaac library shouldn't cause lag on boot

- StageAPI loads data for hundreds of rooms on the first run, which causes lag.
- Libraries shouldn't do anything if they are not being used. This is the same
  principle as
  [not importing for side effects](https://github.com/Zamiell/isaac-faq/blob/main/mod-organization.md#avoiding-side-effects).
- Instead, by lazy loading data, IsaacScript custom stages only incur a tiny
  amount of lag when they are first traveled to. (Only the specific data needed
  for the actual generated floor is retrieved.)

#### 7. An Isaac library should have excellent documentation

- StageAPI has historically been undocumented. Recently, there have been some
  excellent documentation additions by Filloax (the person behind Revelations).
  With that said, all of the documentation is manually typed and prone to error.
- An old adage in programming is that
  [if it isn't documented, then it doesn't exist](https://blog.codinghorror.com/if-it-isnt-documented-it-doesnt-exist/).
  Beautiful, searchable, and easy-to-use documentation should be a first-class
  goal.
- Documentation should be automatically generated with tooling so that it never
  gets out of date.

<!--lint enable ordered-list-marker-value -->

With these improvements in mind, I've created the IsaacScript stage library.
Since it is integrated into the normal [standard library](/isaacscript-common),
using it is effortless. See the [getting started section](#getting-started)
above.

<br />

## Custom Stage Room Variant Prefixes

Each custom stage needs a unique room variant prefix. And all of the room
variant prefixes for each mod must not overlap with any other ones - otherwise,
loading the custom stage will not work properly. In order to prevent conflicts,
this section documents all of the arbitrary prefixes claimed by each mod. Valid
prefixes are between 101 and 999, inclusive.

| Room Variant Prefix | Mod Name |
| ------------------- | -------- |
| n/a                 | n/a      |

(There are no mods yet that have claimed any prefixes. Click on the edit button
below to add yours.)

================================================================================
// File: packages/docs/content/main/directory-structure.md
================================================================================
---
title: Project Directory Structure
---

When you use `isaacscript init`, it will automatically create a directory with
some files for you. The basic folder structure is:

```text
project/
├── src/ (TypeScript source code)
|   └── main.ts
└── mod/ (what will exist in the "real" mod directory)
    ├── main.lua
    └── metadata.xml
```

More specifics are detailed below. **You do not need to know what all of these
files are for**, so if you want to dive into coding your mod, skip reading this
page.

<br />

## Directories

### `project`

This is the root directory of your project. It won't actually be called
`project`; it will instead be named after your mod.

<br />

### `project/.github/workflows/ci.yml`

This directory contains the file for GitHub Actions (i.e.
[continuous integration](https://en.wikipedia.org/wiki/Continuous_integration)).

If you do not use GitHub, feel free to delete this directory.

If you want to be alerted via Discord if a commit fails CI, then follow the
steps in the comment near the bottom of the file.

<br />

### `project/.vscode`

This directory contains some stock settings that are recommended for VS Code to
work properly with IsaacScript projects.

If you do not use VS Code and don't ever plan on collaborating with anyone who
would, feel free to delete this directory.

<br />

### `project/mod`

This is the source mod directory. Any files that you put here will be
automatically transferred over to the mirrored directory in `mods`.

For example,

```batch
C:\Repositories\revelations\mod\image.png
```

will be copied to:

```batch
C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\mods\revelations\image.png
```

<br />

### `project/node_modules`

This directory contains the dependencies for the project. (e.g. TypeScript,
TypeScriptToLua, ESLint, etc.)

Leave it in place and ignore it.

More info:

- `node_modules` is generated when you type `npm install` in a directory with a
  `package.json` file in it.
- `isaacscript init` automatically creates a `package.json` file for you and
  does an `npm install` when you start a new project.
- This directory will contain a lot of files and is usually 100+ megabytes in
  size.
- `node_modules` are always excluded from being tracked in a Git repository.
  - There will already be an entry for `node_modules` in the `.gitignore` file
    installed by `isaacscript`.

<br />

### `project/src`

This is the TypeScript source directory. All of the TypeScript files for your
mod should live in here.

`isaacscript init` will automatically create a `main.ts` file for you in this
directory.

<br />

## Files

### `.gitattributes`

This contains specific Git attributes that should be applied to this Git
repository, if present. By default, it prevent Windows systems from cloning the
repository with "\r\n" line endings (since "\n" line endings should always be
used for consistency).

<br />

### `.gitignore`

This contains a list of files that should not be added to a Git repository, if
present. If you have a private file that you don't want to be committed to a
repository, you can edit this file and add it.

<br />

### `.luarc.json`

This contains settings for the Lua language server. Even though IsaacScript mods
are programmed in TypeScript, not Lua, you may sometimes want to open the
resulting "main.lua" file for the purposes of troubleshooting a run-time error.
Or, you might be using a 3rd-party Lua library, and you might want to open the
Lua files for the purposes of modifying something.

<br />

### `.prettierignore`

This contains a list of files that should not be automatically formatted. By
default, it includes stuff from
[Basement Renovator](https://github.com/Basement-Renovator/basement-renovator/)
and the animation editor.

<br />

### `cspell.config.jsonc`

This is the configuration file for
[CSpell](https://github.com/streetsidesoftware/cspell), a spell-checker for
code.

If VS Code incorrectly reports that a file is misspelled, you can right-click on
the word and say "Add Words to CSpell Configuration". The word will then be
recorded in this file and the squiggly line will go away.

<br />

### `eslint.config.mjs`

This is the configuration file for [ESLint](https://eslint.org/), the TypeScript
linter.

You can edit this file if you need to disable a specific linting rule.

<br />

### `isaacscript.json`

This is the configuration file for `isaacscript`. It contains only per-user
settings. Thus, it should not be committed to a Git repository. You can see the
format of the file in
[the IsaacScript source code](https://github.com/IsaacScript/isaacscript/blob/main/packages/isaacscript-cli/src/classes/Config.ts).

<br />

### `LICENCE`

This is the licence for your project. By default, `isaacscript init` installs
[GNU General Public License v3](https://www.gnu.org/licenses/gpl-3.0.en.html).
Since the type definitions are licensed as GPLv3, you must use GPLv3 or another
compatible license in your IsaacScript project.

<br />

### `package.json`

This is the configuration file for [npm](https://www.npmjs.com/), the Node
package manager. It contains a description of your project and a list of all of
the dependencies.

If you decide to add a new dependency (e.g. `npm install lodash --save`), then
`npm` would automatically edit the `package.json` file accordingly. (Beware of
adding JavaScript/TypeScript dependencies, since
[it will not work properly](/main/gotchas/#npm-dependencies).)

IsaacScript projects start with some dependencies:
<!-- This corresponds to "package.mod.json". -->

1. `isaac-typescript-definitions` - Provides the types for all the Isaac API
   classes, like `EntityPlayer` and so forth.
1. `isaacscript-common` - Provides optional code that you can use in your mod.
   See the [`isaacscript-common`](/isaacscript-common) page for more info.

It also starts with some development dependencies (which are only used when
compiling, linting, and so on):

1. `complete-node` - Provides helper functions to use in scripts.
1. `isaacscript` - Provides the command-line program that monitors your project.
1. `isaacscript-lint` - Provides `eslint` and all of the linting-related
   packages that `eslint` uses, including the official IsaacScript linting
   rule-set.
1. `isaacscript-spell` - Provides spell checking dictionaries for The Binding of
   Isaac words and IsaacScript words.
1. `isaacscript-tsconfig` - Provides a standard TypeScript configuration file
   ("tsconfig.json").
1. `tsx` - Provides the `tsx` program, which is used to run TypeScript code.
1. `typescript` - Provides the ability to compile TypeScript code.
1. `typescript-to-lua` - The tool that actually converts the TypeScript code to
   Lua. The `isaacscript` command-line program invokes this on your behalf.

<br />

### `package-lock.json`

This is a lock file for [npm](https://www.npmjs.com/), the Node package manager.

You are not supposed to edit this file; just leave it in place so that `npm` can
function correctly.

<br />

### `prettier.config.mjs`

This is the configuration file for Prettier.

If you need to modify a specific option of Prettier, you can edit this file.

<br />

### `README.md`

This is the README file for your project, which should contain a brief
description of your mod. It uses
[Markdown](https://guides.github.com/features/mastering-markdown/), which is the
standard format for README files.

<br />

### `tsconfig.json`

This is the configuration file for the
[TypeScript](https://www.typescriptlang.org/) programming language. You can edit
it if you need to add or remove a particular compiler flag.

<br />

### `mod/main.lua`

This is the transpiled Lua output of your TypeScript source code. All TypeScript
code is combined into one big Lua file. There is no need to commit this file to
a Git repository, so it is included in the ".gitignore" file by default.

<br />

### `mod/metadata.xml`

This is the file used by the "ModUploader" tool to upload your mod to the Steam
Workshop. It contains a description of your mod and other metadata. IsaacScript
creates a basic one for you, but when you upload your mod to the Steam Workshop
for the first time, more information will be added (like the ID of the mod).

<br />

================================================================================
// File: packages/docs/content/main/discord.md
================================================================================
---
title: Discord
---

The IsaacScript [Discord server](https://discord.gg/KapmKQ2gUD) is the central
communication hub for people using the tool.

The latest news and announcements are posted in the Discord server. It is the
best place to ask questions and get feedback. And if something is broken with
the tool, then join the Discord and let us know.

================================================================================
// File: packages/docs/content/main/enums-and-objects.md
================================================================================
---
title: The Difference Between Enums and Objects
---

In IsaacScript mods, both enums and objects are used, depending on the
situation. This might be a little confusing.

For most purposes, it is not important to know the low-level details - you can
use whichever one you like. But if you want to dive into some of the details and
explore the differences, then read on.

<br />

### Enum Introduction

"Enum" is short for "enumeration". In programming, the term is used to describe
an object that contains a finite set of values.

TypeScript has first-class support for enums. This means that you can type the
word `enum` to create one, and this is part of the language itself, which is
really handy. In good code, enums are used a lot: they get rid of
[magic numbers](<https://en.wikipedia.org/wiki/Magic_number_(programming)>) and
constrain possible values to a finite set.

For example, this is the enum that describes the four different kinds of slots
that active items can go into:

```ts
enum ActiveSlot {
  PRIMARY = 0,
  SECONDARY = 1,
  POCKET = 2,
  POCKET_SINGLE_USE = 3,
}
```

But notice that we could also type this as an object instead:

```ts
const ActiveSlot = {
  PRIMARY: 0,
  SECONDARY: 1,
  POCKET: 2,
  POCKET_SINGLE_USE: 3,
};
```

This is _kind of_ the same thing, but there are a few key differences.

<br />

### Enums By Default

Let's start with the basics. By default, we should use enums over objects, where
possible. Why?

#### 1) Clear Intent

First, enums make the intent more clear. Enums represent the concept of "a
finite set of values". On the other hand, a plain object can represent basically
anything. If we want to specify a finite set of values, then using an `enum`
clearly communicates the intent to anyone reading the code.

#### 2) Computed Members

Second, enums have a feature called
[computed members](https://www.typescriptlang.org/docs/handbook/enums.html#computed-and-constant-members).
This means that we don't have to bother typing out what the values are. For
example, we can type the `ActiveSlot` enum from earlier like this:

```ts
enum ActiveSlot {
  PRIMARY,
  SECONDARY,
  POCKET,
  POCKET_SINGLE_USE,
}
```

Here, TypeScript automatically assigns a value of 0 to the first member, a value
of 1 to the second member, and so on. This saves time _now_, because we don't
have to type `= 0` (and so on). It also saves time _later_, because if we add a
new entry in the middle, we don't have to also modify all the lines that come
afterwards.

#### 3) Reverse Mapping

Third, enums automatically get a reverse mapping at run-time. For example,
imagine that you are debugging something to do the `ActiveSlot` enum above. You
might type the following code to help troubleshoot it:

```ts
log(`DEBUG - The active slot is: ${activeSlot}`);
```

This might print out: `DEBUG - The active slot is: 2`. But that's annoying,
because we might not know what 2 even means in this context. Instead, we can
make life easier on ourselves by writing our debug statement like this:

```ts
log(`DEBUG - The active slot is: ${ActiveSlot[activeSlot]} (${activeSlot})`);
```

This would print out: `DEBUG - The active slot is: POCKET (2)`. Much better! In
essence, the reverse mapping helps us easily retrieve the name of any enum value
when we need it. (The lookup is done in O(1) time. On an object, it would be
done in O(N) time, since we would have to iterate over the entries.)

#### Conclusion - Use Enums

Thus, in the general case, we use enums. We only have to resort to using objects
in the special cases where "normal" enums won't work.

<br />

### The Differences Between Types and Containers

So, what are the situations where "normal" enums won't work?

In order to understand that, we first have to understand the difference between
a "type" and a "container". Enums blur the distinction between these two things,
so we need to take a step back and think about how they can be different.

#### 1) The `CollectibleType` Type

First, let's drill down on what exactly a "type" is. Consider the
`EntityPlayer.AddCollectible` method. You can use it like this:

```ts
const player = Isaac.GetPlayer();
player.AddCollectible(CollectibleType.SAD_ONION);
```

The `EntityPlayer.AddCollectible` method takes in a variable of type
`CollectibleType`. But notice that the following code will also work just fine:

```ts
const MY_CUSTOM_ITEM = Isaac.GetItemIdByName("My Custom Item");
const player = Isaac.GetPlayer();
player.AddCollectible(MY_CUSTOM_ITEM);
```

This is because the return type of the `Isaac.GetItemIdByName` method is
`CollectibleType`.

The point of this example is to show that _any_ variable can be of type
`CollectibleType`. As far as the `EntityPlayer.AddCollectible` method is
concerned, the requirement is **not** that the incoming thing is attached to the
`CollectibleType` enum, like `CollectibleType.SAD_ONION` is. Rather, the
requirement is that the type of the variable matches the `CollectibleType` type.

So, in most cases, we use the word `CollectibleType` to refer to the
`CollectibleType` type. But that's not all we use it for.

#### 2) The `CollectibleType` Container

We also use the word `CollectibleType` to refer to the "container" that holds
all of the `CollectibleType` values. To illustrate this, we could create a
container with a different name, but still having `CollectibleType` values:

```ts
const MyContainer = {
  VALUE_1: CollectibleType.SAD_ONION,
  VALUE_2: CollectibleType.INNER_EYE,
  VALUE_3: CollectibleType.SPOON_BENDER,
};
```

Here, `MyContainer` is not a type. It's just a container that holds values with
the `CollectibleType` type. We can use these values without a problem:

```ts
const player = Isaac.GetPlayer();
player.AddCollectible(MyContainer.VALUE_1);
```

### The Differences Between Objects and Enums

With the previous section in mind, we now know the main difference between an
object and an enum:

- Creating an object is just creating a container.
- Creating an enum is creating both a container **and** a type at the same time,
  with all of the values inside of it automatically being converted to the new
  type.

<br />

### Where Enums Don't Work

Now that we know the difference between objects and enums, we can explore the
specific situations in which enums won't work. The most common situation is when
we want to create an enum containing our modded items or entities.

For example, imagine that we had a custom collectible in our mod called "Foo".
Try typing the following into your mod:

```ts
enum CollectibleTypeCustom {
  FOO = Isaac.GetItemIdByName("Foo"),
}
```

This will give an error:

> Type
> 'import("C:/Repositories/my-mod/node_modules/isaac-typescript-definitions/dist/enums/collections/subTypes").CollectibleType'
> is not assignable to type 'CollectibleTypeCustom'.

If we had typed `FOO = 1` or something like that, then under the hood,
TypeScript would automatically convert "1" to a type of `CollectibleTypeCustom`,
and we wouldn't get an error. But since we used the `Isaac.GetItemIdByName`
method, the value is a `CollectibleType`, which is more specific than a
`number`. TypeScript can't automatically convert `CollectibleType` to
`CollectibleTypeCustom`, so it throws an error. (In TypeScript, the only
supported types that you can feed to an enum for auto-conversion are `number` or
`string`.)

We could temporarily fix the problem by using a type assertion, like this:

```ts
enum CollectibleTypeCustom {
  FOO = Isaac.GetItemIdByName("Foo") as number,
}
```

This is essentially telling the TypeScript compiler: "Hey, I'm positive this is
a `number`, so forget whatever else you think you know about this line." Doing
that would make TypeScript succeed in converting the result of the method to the
`CollectibleTypeCustom` type. However, this isn't really what we want either.
For example, say that later on, we want to give the player our custom
collectible:

```ts
const player = Isaac.GetPlayer();
player.AddCollectible(CollectibleTypeCustom.FOO);
```

This would give a compiler error, because `CollectibleTypeCustom.FOO` is of type
`CollectibleTypeCustom`. And as we said earlier, the
`EntityPlayer.AddCollectible` method needs to take in a type of
`CollectibleType`, not `CollectibleTypeCustom`. They are completely different
types.

By now, hopefully it is clear that we do not want to actually create a new type
(which is what making a new enum will do). Instead, what we really want to do is
to create a new container that holds values of an existing type. So that's why
the correct solution is to create a "pseudo-enum" object, like this:

```ts
const CollectibleTypeCustom = {
  FOO: Isaac.GetItemIdByName("Foo"),
};
```

We can use this pattern whenever we want to create a custom enum that "inherits"
the type of an existing enum. For most intents and purposes, these "container"
objects will work in the same way as a normal enum. (But note that they won't
have a [reverse mapping](#3-reverse-mapping) embedded into them.)

<br />

================================================================================
// File: packages/docs/content/main/example-mod.md
================================================================================
---
title: Building an Example Mod
---

This is a tutorial that shows off how to code a simple mod with IsaacScript. Our
goal will be to create a new passive item in the game called the _Green Candle_.

(If you don't know what IsaacScript is, see the [features](/main/features/)
page. If you don't know whether you should use it yet, see the
[Is IsaacScript Right for Me?](/main/right-for-me/) page.)

<br />

## 0) Extract the Game's Resources

Most modders will have already done this, but just in case you haven't, you
should run the game's resource extractor. (This is also referred to as the
unpacker.) The extractor is located at:
`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\tools\ResourceExtractor\ResourceExtractor.exe`

(Messages like `WARNING: could not return filename for entry 35a142c2bed2d0cf`
are normal.)

After running the unpacker, you can find all of the vanilla assets in the
`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\resources\`
directory and the `resources-dlc3\` directory. (The latter contains only
Repentance files.) Study the layout of the files in these two directories so
that you can get familiar with where particular files need to live.

<br />

## 1) Initializing the Project

First, make sure that you have already read the
[Getting Started](/main/getting-started/) section of the IsaacScript docs and
have a rough understanding of how IsaacScript works.

For this tutorial, we will be using `C:\Repositories\green-candle` as the
directory for our mod. So, in a Windows command prompt, create that directory,
change into that directory, and initialize a new IsaacScript project

```batch
mkdir C:\Repositories\green-candle
cd C:\Repositories\green-candle
npx isaacscript@latest init --use-current-dir --save-slot=1 --vscode
```

At this point, the skeleton for our mod is in place. Now, start IsaacScript and
let it run in the background:

```batch
npx isaacscript
```

We can now begin working.

<br />

## 2) Create the Image for the Item

First, we will set up the image for how the item will appear in-game. We will
use this image: ![Green Candle](/img/items/green-candle.png)

Most images for a mod should be placed in a "resources" subdirectory. (This
corresponds to how things are organized in
`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\resources`.)

For our purposes, we will need to copy
[the Green Candle image](/img/items/green-candle.png) to
`C:\Repositories\green-candle\mod\resources\gfx\items\collectibles\green-candle.png`.
(You will need to create the "resources", "gfx", "items", and "collectibles"
directories, since they won't exist yet.)

Notice that this path corresponds to the "real" items graphics directory of
`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\resources\gfx\items\collectibles\`.
Under the hood, the game will merge the two directories when you enable the mod.

<br />

## 3) Create the Entry For the Item in `items.xml`

Next, we need to tell the game that the new item should exist. This is done by
adding a new entry to the "items.xml" file.

New entries for things go in the "content" subdirectory. Make a blank file at
`C:\Repositories\green-candle\mod\content\items.xml`. (You will need to create
the "content" directory, since it won't exist yet.)

In this file, add the following:

```xml
<items gfxroot="gfx/items/" version="1">
  <passive
    description="Mass poison"
    gfx="green-candle.png"
    name="Green Candle"
  />
</items>
```

Now, the item will exist in the game, and you can give it to yourself with the
console command of `giveitem green candle`.

Notice that this file is in the same format as the "real" items.xml file located
at
`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\resources\items.xml`.
Under the hood, the game will merge the contents of your little items.xml file
with the big items.xml file when you enable the mod.

<br />

## 4) Create the Entry for the Item in `itempools.xml`

Even though the item exists in the game, it is not yet present in any of the
item pools. This means that players will never randomly discover your item as
they play the game.

So, let's add the item to the Treasure Room pool. Make a blank file at
`C:\Repositories\green-candle\mod\content\itempools.xml` and add the following
to it:

```xml
<ItemPools>
  <Pool Name="treasure">
    <Item Name="Green Candle" Weight="1" DecreaseBy="1" RemoveOn="0.1" />
  </Pool>
</ItemPools>
```

Here, we use values for "Weight", "DecreaseBy", and "RemoveOn" that match what
is used for all of the other items in the Treasure Room pool. (You can see this
if you open the "real" itempools.xml file at
`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\resources\items.xml`.)

Now, the item will sometimes randomly appear for players when they enter a
Treasure Room!

<br />

## 5) Start Coding the Effect

Right now, if players pick up your item, it won't actually do anything. This is
where the coding part comes in.

Mods affect the game by putting code inside of _callbacks_. Each callback fires
when a particular event happens in the game. There are
[72 different callbacks](https://wofsauge.github.io/IsaacDocs/rep/enums/ModCallbacks.html)
to choose from, so you have to choose the right one depending on what you want
to do. For example, the most basic callback is the `POST_GAME_STARTED`, which
fires once at the beginning of a new run.

First, go through
[the official docs](https://wofsauge.github.io/IsaacDocs/rep/enums/ModCallbacks.html)
and read what all of the callbacks do so that you can get familiar with them.

Next, open `C:\Repositories\green-candle\src\main.ts` in VS Code, which contains
the TypeScript code that will be transpiled to the "main.lua" file and read by
the game.

The bootstrapper created a skeleton of a mod for us. As you can see, it calls
the `Isaac.DebugString()` function when the `POST_GAME_STARTED` callback is
fired.

(`Isaac` is a global class provided by the game with helpful general-purpose
methods on it. `Isaac.DebugString()` simply writes something to the "log.txt"
file, which is located at
`C:\Users\%USERNAME%\Documents\My Games\Binding of Isaac Repentance\log.txt`.)

First, change the `MOD_NAME` constant to "Green Candle".

Second, remove all of the lines relating to the `POST_GAME_STARTED` callback.
This callback is useful for initializing things at the start of every run. But
for our purposes, we don't need to use it.

<br />

## 6) Get the ID for the Green Candle

When the game loads a new collectible, it assigns it a collectible type. These
types start at 733 and count upwards. (732 is the collectible type of the final
vanilla item, "Mom's Ring", so the first available collectible type for mods is
733.)

The collectible type that the Green Candle will get depends on how many other
custom modded items that we have loaded. So, in order to write code for the
Green Candle, we have to ask the game what the current ID is and store it for
later.

In order to do this, we need to use the `Isaac.GetItemIdByName()` method:

```ts
const GREEN_CANDLE_COLLECTIBLE_TYPE = Isaac.GetItemIdByName("Green Candle");
```

This is a constant, so we name it with all capital letters and with
SHOUTING_SNAKE_CASE. Put this at the top of the file next to the "MOD_NAME"
constant.

<br />

## 7) Add a New Callback

As we discussed above, when adding new code, you have to put it in the right
callback for what you want to do.

For our purposes, we want the Green Candle to have a random chance to poison
every enemy in the room on every frame. So, that means that the code should run
on every frame, and that means we need to use the `POST_UPDATE` callback, which
runs 30 times a second.

(The game update loop runs at 30 times per second and the game render loop runs
at 60 times per second. Since our code is gameplay-related, we should put it in
the `POST_UPDATE` callback. On the other hand, if we were drawing a sprite on
the screen, then we would use the `POST_RENDER` callback.)

Add the following code to the "main" function:

```ts
mod.AddCallback(ModCallback.POST_UPDATE, postUpdate);
```

As you type the `ModCallback` enum, it should automatically create an import
statement for the enum at the top of the file, which will look like this:

<!-- We use "js" instead of "ts" to prevent the fixer from deleting the import statement. -->

```js
import { ModCallback } from "isaac-typescript-definitions";
```

If you pasted the code in from this website, then it wouldn't have gotten the
chance to automatically import. Handily, VS Code has a feature to automatically
import whatever the text cursor happens to be over. So, put the text cursor at
the end of the "ModCallback" word, and then hit `Ctrl + space + enter`.

After importing the enum, we have to add the corresponding function that will be
called when the callback fires:

```ts
function postUpdate() {
  Isaac.DebugString("A game frame just passed!");
}
```

Now, we can run the mod and confirm that this code makes tons of messages in the
"log.txt" file at the rate of 30 times a second.

<br />

## 8) Getting the Number of Green Candles

Instead of sending messages to the log, let's set up a new function for applying
the green candle effect:

```ts
function postUpdate() {
  checkApplyGreenCandleEffect();
}

function checkApplyGreenCandleEffect() {
  // TODO - Fill this in.
}
```

Since Isaac is a co-op game, it is possible that up to 4 players could all have
the Green Candle at the same time. We want our mod to work properly in
multiplayer, so we have to loop over all the players.

Since this is such a common task, there is a `getPlayers` function for this in
the IsaacScript standard library:

```ts
function checkApplyGreenCandleEffect() {
  for (const player of getPlayers()) {
    // TODO - Check if the player has Green Candle.
  }
}
```

By simply typing in `getPlayers`, VS Code should automatically import it, which
means that it will add the following line to the top of the file:

<!-- We use "js" instead of "ts" to prevent the fixer from deleting the import statement. -->

```js
import { getPlayers } from "isaacscript-common";
```

Now that we have the players, we can check to see if they have the Green Candle
by using the `HasCollectible()` method:

```ts
function checkApplyGreenCandleEffect() {
  for (const player of getPlayers()) {
    if (player.HasCollectible(GREEN_CANDLE_COLLECTIBLE_TYPE)) {
      applyGreenCandleEffect(player);
    }
  }
}

function applyGreenCandleEffect(player: EntityPlayer) {
  // TODO - Fill this in.
}
```

<br />

## 9) Looping Over All the Enemies in a Room

Every enemy in the room should have a chance of being poisoned. So, we need to
loop over all enemies in the room with the `getNPCs()` function. (This is also a
helper function from the IsaacScript standard library.)

```ts
function applyGreenCandleEffect(player: EntityPlayer) {
  for (const npc of getNPCs()) {
    if (shouldApplyGreenCandleEffectToNPC(npc)) {
      // TODO - Apply poison.
    }
  }
}

function shouldApplyGreenCandleEffectToNPC(npc: EntityNPC) {
  // TODO - Return true or false based on a random chance.
  return true;
}
```

<br />

## 10) Applying the Poison

Adding the poison is done with the `AddPoison` method. However, notice that VS
Code will show you an error if you try to supply the player as the source:

```ts
function applyGreenCandleEffect(player: EntityPlayer) {
  for (const npc of getNPCs()) {
    if (shouldApplyGreenCandleEffectToNPC(npc)) {
      // - The source is the player.
      // - The duration is 100 frames.
      // - The damage is equal to the player's damage stat.
      npc.AddPoison(player, 100, player.Damage);
      // (This shows an error in VS Code because the `AddPoison` method expects an `EntityRef`.)
    }
  }
}
```

This showcases the advantage of programming in TypeScript instead of Lua,
because this is a common error. The TypeScript compiler tells us that we
_actually_ need to give the function an entity reference instead of an entity.
This is accomplished by converting the player to a reference by using the
`EntityRef` global function:

```ts
npc.AddPoison(EntityRef(player), 100, player.Damage);
```

<br />

## 11) Detect Invulnerable Enemies and Add a Random Chance

Now, let's fill in the `shouldApplyGreenCandleEffectToNPC()` function.

Some enemies, like Stonies, are supposed to be invincible, so it would be a bug
in our mod if the poison effect applied to them. So, we have to find a way to
detect invincible enemies.

By looking through [the API docs](https://wofsauge.github.io/IsaacDocs/), we
eventually find that there is a `IsVulnerableEnemy()` method. This sounds like
what we need.

Furthermore, we want the random chance for the Green Candle to work to be around
1 in 500. We can accomplish that with the `getRandomInt` function. (This is also
a helper function from the IsaacScript standard library.)

```ts
function shouldApplyGreenCandleEffectToNPC(npc: EntityNPC) {
  return npc.IsVulnerableEnemy() && getRandomInt(1, 500) === 1;
}
```

<br />

## 12) Done

The mod is now complete. It looks like the following:

```ts
import { ModCallback } from "isaac-typescript-definitions";
import { getNPCs, getPlayers, getRandomInt } from "isaacscript-common";

const MOD_NAME = "Green Candle";
const GREEN_CANDLE_COLLECTIBLE_TYPE = Isaac.GetItemIdByName("Green Candle");

export function main() {
  const mod = RegisterMod(MOD_NAME, 1);

  mod.AddCallback(ModCallback.POST_UPDATE, postUpdate);

  Isaac.DebugString(`${MOD_NAME} initialized.`);
}

function postUpdate() {
  checkApplyGreenCandleEffect();
}

function checkApplyGreenCandleEffect() {
  for (const player of getPlayers()) {
    if (player.HasCollectible(GREEN_CANDLE_COLLECTIBLE_TYPE)) {
      applyGreenCandleEffect(player);
    }
  }
}

function applyGreenCandleEffect(player: EntityPlayer) {
  for (const npc of getNPCs()) {
    if (shouldApplyGreenCandleEffectToNPC(npc)) {
      // - The source is the player.
      // - The duration is 100 frames.
      // - The damage is equal to the player's damage stat.
      npc.AddPoison(EntityRef(player), 100, player.Damage);
    }
  }
}

function shouldApplyGreenCandleEffectToNPC(npc: EntityNPC) {
  return npc.IsVulnerableEnemy() && getRandomInt(1, 500) === 1;
}
```

You should now know the basic anatomy of an Isaac mod:

- using the `content` folder for merging content additions
- using the `resources` folder for blowing away vanilla assets and adding new
  files
- adding TypeScript code to the `main.ts` file
- using callbacks such as `POST_GAME_STARTED` and `POST_UPDATE`
- using the IsaacScript watcher to automatically compile and see your changes
  in-game

For a recommendation on what to do next, see the [next steps](/main/next-steps/)
page.

================================================================================
// File: packages/docs/content/main/extra-callbacks.md
================================================================================
---
title: Extra Callbacks
---

See the [IsaacScript standard library documentation](/isaacscript-common/).

================================================================================
// File: packages/docs/content/main/features.md
================================================================================
---
title: Features
---

IsaacScript is a framework that allows you to code
[_The Binding of Isaac: Repentance_](https://store.steampowered.com/app/1426300/The_Binding_of_Isaac_Repentance/)
mods using the [TypeScript](https://www.typescriptlang.org/) programming
language instead of the [Lua](https://www.lua.org/) programming language. It
automatically converts your TypeScript code into Lua, similar to how a C++
compiler automatically converts C++ code into X86.

## <img src="/img/lua.png" class="features-language-icon" alt="" /> The Downsides of Lua

The vast majority of Isaac mods are programmed in Lua. So why would you want to
use TypeScript over Lua? Why would you want to introduce a compiler into your
workflow and make things more complicated for yourself?

Programming mods in Lua can be really painful:

### <img src="/img/items/error.png" class="features-icon" alt="" /> No Type Safety

With Lua, it is easy to shoot yourself in the foot after making even the
smallest typo. When building an Isaac mod, you end up wasting an enormous amount
of time running around in-game debugging run-time errors, and pouring through
the "log.txt" file. Not my idea of fun, and probably not yours either.

### <img src="/img/items/sad-onion.png" class="features-icon" alt="" /> Limited Language Constructs

In Lua, you type `x = x + 1`. In TypeScript, you type `x++`. Lua doesn't have
increment/decrement operators, assignment operators, switch statements, optional
function arguments, array/object destructuring, or map/filter/reduce. And that's
just to start with.

### <img src="/img/items/finger.png" class="features-icon" alt="" /> No Automatic Importing

In Lua, you can't just start typing a function and have it magically be imported
from where it lives. So you are stuck between using monolithic files (messy), or
manually typing "require" over and over (tedious).

### <img src="/img/items/wooden-spoon.png" class="features-icon" alt="" /> Bad In-Editor Tooling

Lua has gotten some nifty improvements in the past few years, like
[Sumneko's Lua language server](https://github.com/sumneko/lua-language-server).
Using the language server brings us some of the in-editor goodies that we are
used to from other languages, like variable renaming. But the experience still
pales in comparison to other modern programming languages like TypeScript and
Rust.

## <img src="/img/typescript.png" class="features-language-icon" alt="" /> The Upsides of TypeScript

After five years of programming Isaac mods in Lua, I got frustrated enough to
take a
[level 2 action](https://www.lesswrong.com/posts/guDcrPqLsnhEjrPZj/levels-of-action) -
to build the ultimate Isaac developer experience, using TypeScript as a basis.
The improvement is so significant that once you start, you will never go back.
Here's a short list of features:

### <img src="/img/items/magic-mushroom.png" class="features-icon" alt="" /> The Entire Isaac API, Strongly Typed

- Code fearlessly without having to worry about the format of the API call or
  whether using it incorrectly will crash the game.
- The compiler catches every possible type error, making refactoring your code
  easier than you ever imagined that it could be.

### <img src="/img/items/marked.png" class="features-icon" alt="" /> Mouseover Documentation

- Don't waste time looking up API methods in the docs. Instead, hover over the
  classes and functions in your actual code editor to see what they do and what
  parameters they expect.
- Many methods have extensive documentation written inside of the mouseover
  tooltip.

### <img src="/img/items/clockwork-assembly.png" class="features-icon" alt="" /> Automatic Mod Reloading

- Never close and reopen your game again when working on your mods. Never type
  the `luamod` console command again.
- With the IsaacScript watcher, as soon as you press `Ctrl + s` to save a file,
  you can instantly view the changes in-game without having to do anything else.
- If you use `require` hacks to get around the limitations of `include` +
  `luamod`, don't bother - that isn't needed here.

### <img src="/img/items/pencil.png" class="features-icon" alt="" /> Automatic Formatting

- Never waste time formatting a file again. Automatic file formatting with
  [Prettier](https://prettier.io/) comes running out-of-the-box.

### <img src="/img/items/spider-mod.png" class="features-icon" alt="" /> Automatic Linting

- Squash all the bugs and ensure code consistency with the world's best linter,
  [ESLint](https://eslint.org/). It comes running out-of-the-box.

### <img src="/img/items/humbling-bundle.png" class="features-icon" alt="" /> Extra Enums

- Seamlessly utilize
  [community-contributed enums](/isaac-typescript-definitions) for things that
  the developers forgot to include in the "enums.lua" file.

### <img src="/img/items/book-of-virtues.png" class="features-icon" alt="" /> Expanded Standard Library

- Seamlessly utilize hundreds of helper functions and features from the
  [expanded standard library](/isaacscript-common), allowing you to write
  high-level code that is concise and easy to read.

### <img src="/img/items/poke-go.png" class="features-icon" alt="" /> Extra Callbacks

- Seamlessly utilize [many extra callbacks](/isaacscript-common/) as part of the
  expanded standard library.

================================================================================
// File: packages/docs/content/main/getting-started.md
================================================================================
---
title: Getting Started
---

`isaacscript` will currently work on Windows and Linux.

You can go from zero to up-and-running with a new mod in around 5 minutes,
depending on how fast your computer and internet speed is.

(If you don't know what IsaacScript is or you are not yet convinced that you
should use it, look at the [features](/main/features/) page first.)

<br />

### 1) Install Node.js

In order to run files that are written in the JavaScript & TypeScript
programming language, we need [Node.js](https://nodejs.org/en/), a JavaScript
runtime. If you don't have it installed already, download and install it from
the [Node.js download page](https://nodejs.org/en/download/).

<br />

### 2) Install VS Code

[Visual Studio Code](https://code.visualstudio.com/) (or VS Code, for short) is
probably the best text editor for TypeScript. If you don't have it installed
already, download and install it from the
[VS Code download page](https://code.visualstudio.com/download).

(If you usually use a different TypeScript editor like
[WebStorm](https://www.jetbrains.com/webstorm/) or [vim](https://www.vim.org/),
then feel free to use that instead if you want.)

<br />

### 3) Open a New Command Prompt Window / Shell

Open a new
[command prompt window](https://www.howtogeek.com/235101/10-ways-to-open-the-command-prompt-in-windows-10/).
(Or, feel free to use Windows Terminal, PowerShell, Git Bash, etc.)

<br />

### 4) Create and Change to Your Project Directory

Make a new directory for your mod, and then change the current working directory
to it. (Use
[lowercase and kebab-case](https://stackoverflow.com/questions/11947587/is-there-a-naming-convention-for-git-repositories).)

For example, if your mod is named "Revelations", you would type the following
into the command prompt:

```batch
mkdir C:\Repositories\revelations
cd C:\Repositories\revelations
```

Note that your project directory should **not** be a subdirectory of the Isaac
`mods` directory! This is because `isaacscript` will synchronize / clone your
mod there automatically.

<br />

### 5) Run `isaacscript init` to Bootstrap the Project

Run:

```sh
npx isaacscript@latest init
```

The program will ask you some questions and then populate your current directory
with TypeScript and other some other dependencies.

(You might get a warning of
``npm WARN config global `--global\`, `--local` are deprecated. Use `--location=global` instead.``
You can safely ignore this and press enter to proceed, as it is a recent npm bug
with Windows.)

At the end, it will ask you if it should launch VS Code for you. Answer yes.

<br />

### 6) Run `isaacscript`

Back in your command prompt, start `isaacscript`:

```sh
npx isaacscript
```

(This is shorthand for `npx isaacscript monitor`.)

The program will run forever, monitoring for changes in your project. If you
want to cancel it, you can press `Ctrl + C` to return to your shell.

IsaacScript needs to be running in order for your code changes to propagate to
the real mod directory, so you will need to start it up in the same way every
time that you begin coding. (You could also
[automate the invocation with a VS Code task](https://code.visualstudio.com/docs/editor/tasks)
if you find it annoying to run it manually.)

<br />

### 7) Start Coding

That's it! Now, start coding by editing the `src/main.ts` file.

Note that when you are editing the code in your project, you should always have
VS Code opened to the project directory (i.e. by clicking on File --> Open
Folder), as opposed to just editing a single file. Otherwise, ESLint and
Prettier won't work.

<br />

================================================================================
// File: packages/docs/content/main/gotchas.md
================================================================================
---
title: Gotchas
---

This page lists several "gotchas" or things that might be weird about
IsaacScript.

<br />

### Local Enums and Importing

In the Isaac Lua environment, several enums are declared as global variables. In
typical Lua code, you would just use them directly, like the following:

```lua
-- Lua code
local player = Isaac.GetPlayer()
player:AddCollectible(CollectibleType.COLLECTIBLE_SAD_ONION) -- The "CollectibleType" enum is a global.
```

However, relying on global variables is dangerous, as other mods can change the
contents of the enums. (We have observed this happening in the past from time to
time.) Thus, as an extra safety feature, IsaacScript includes a local copy of
every enum for your personal use.

Additionally, since we don't have to rely on using the official enums, the local
version of the IsaacScript enums can fix all of the spelling errors and
inconsistencies that have gone unfixed in the official game. We can also remove
all of the "fake" enum values that pollute the enum and destroy the type safety,
like `CollectibleType.NUM_COLLECTIBLES`. Furthermore, as a big quality of life
improvement, we also remove the prefix from every enum to make them easy to
type. (For example, `CollectibleType.COLLECTIBLE_SAD_ONION` is changed to
`CollectibleType.SAD_ONION`.)

Since enums are no longer global variables, you must import them in your code
whenever you need to use them. For example, to write the Lua code snippet above
in TypeScript:

```ts
// TypeScript code
import { CollectibleType } from "isaac-typescript-definitions";

const player = Isaac.GetPlayer();
player.AddCollectible(CollectibleType.SAD_ONION);
```

However, don't ever type the imports manually, because that's a big waste of
time! If you tab-complete the name of an enum, VS Code should automatically
import it for you. If you already have an enum that is written out, then you can
auto-import it by putting the text cursor on the right-side of the enum and
typing `Ctrl + space + enter`.

<br />

### Bit Flags

First, familiarize yourself with what
[bit flags are](http://www.cplusplus.com/forum/general/1590/), if you haven't
already.

Several things in Isaac use bit flags, such as tears and projectiles.

In IsaacScript, working with bit flags is different than it is in Lua. We have
the benefit of bit flags being completely type safe - it is impossible to
represent an invalid combination.

For example, the following is possible in Lua:

```lua
-- Lua code
-- Combine 3 tear flags together and assign it to the player.
player.TearFlags = TearFlag.TEAR_PIERCING | TearFlag.TEAR_SPECTRAL | 5
```

This is not a valid combination of bit flags, because `5` is not a tear flag.
Thus, this code would have undefined behavior (and potentially crash the game).

In IsaacScript, assigning some arbitrary number to the `player.TearFlags` field
would cause a compiler error.

In order to get type safety, all enums that are bit flags are extended from the
`BitFlag` type. And a collection of 0 or more bit flags is represented by the
`BitFlags` type. `BitFlags` takes a generic type parameter, so you can have
`BitFlags<TearFlag>`, `BitFlags<ProjectileFlag>`, and so on.

To compose `BitFlags` yourself, you can use the `addFlag` and `removeFlag`
helper functions, like so:

```ts
// TypeScript code
// Combine 3 tear flags together and assign it to the player.
player.TearFlags = addFlag(
  TearFlag.PIERCING,
  TearFlag.SPECTRAL,
  TearFlag.FREEZE,
);
// (The "addFlag" function is variadic.)
```

If you want to assign a specific flag to a `BitFlags` field, then simply
assigning it won't work:

```ts
// TypeScript code
player.TearFlags = TearFlag.PIERCING; // Error
```

Doing this would give the following error:

```text
Type 'TearFlagValue' is not assignable to type 'BitFlags<TearFlagValue>'.
Property '__bitFlagsBrand' is missing in type 'TearFlagValue' but required in type '{ readonly __bitFlagsBrand: TearFlagValue; }'.
```

This error is because `TearFlag` is not exactly the same thing as
`BitFlags<TearFlag>`. (The former must be equal to one specific flag, and the
latter can be 0 or more flags.)

To solve this problem, you can use the `bitFlags` helper function, which will
convert the flag for you:

```ts
// TypeScript code
player.TearFlags = bitFlags(TearFlag.PIERCING);
```

Finally, note that you can also use the `hasFlag` helper function to check for
the presence of a flag:

```ts
// TypeScript code
if (hasFlag(player.TearFlags, TearFlag.PIERCING)) {
  // Handle the piercing synergy.
  // Insert code here.
}
```

<br />

### `int` and `float`

In Lua, there is only one type of number. (The programming language does not
differentiate between integers, floats, etc.)

TypeScript works the same way as Lua. There is only one type of number:
`number`.

However, the official Isaac API documentation uses integers and floats. For
example, this is the entry for the `EntityPlayer.AddHearts` function:

```cpp
void AddHearts(int hearts)
```

In order to more closely match the API, the TypeScript API definitions use `int`
and `float` types. Thus, the above function is declared like this:

```ts
AddHearts(hearts: int): void;
```

If you want, you can use the `int` and `float` types in your own code too
(instead of just using `number`, like you would in other typical TypeScript
code). But if you do use `int` and `float`, be aware that they are simply
aliases for `number`, so they don't provide any actual type safety.

In other words, it is possible to do this, so beware:

```ts
// Give the player a Sad Onion.
player.AddCollectible(CollectibleType.COLLECTIBLE_SAD_ONION, 0, false);

// Find out how many Sad Onions they have.
let numSadOnions = player.GetCollectibleNum(
  CollectibleType.COLLECTIBLE_SAD_ONION,
);
// numSadOnions is now an "int" with a value of "1".

numSadOnions += 0.5;
// numSadOnions is still an "int", but now it has a value of "1.5".
// This is a bug and TypeScript won't catch this for you!
```

<br />

### Extending Enums --> Custom Enums (Part 1)

In your Lua mods, you may have extended the game's built-in enums. For example:

```lua
-- At the top of the mod:
CollectibleType.COLLECTIBLE_MY_CUSTOM_ITEM = Isaac.GetItemIdByName("My Custom Item")

-- Elsewhere in the code:
if (
  player:HasCollectible(CollectibleType.COLLECTIBLE_MY_CUSTOM_ITEM)
  and player:HasCollectible(CollectibleType.COLLECTIBLE_EPIC_FETUS)
) then
  -- Handle the specific synergy with My Custom Item + Epic Fetus.
end
```

In TypeScript, you cannot extend existing enums, because enums are immutable.
(This is a good thing; it's how enums work in all sane programming languages.)
Instead, create your own enum:

```ts
// At the top of the mod:
const CollectibleTypeCustom = {
  MY_CUSTOM_ITEM: Isaac.GetItemIdByName("My Custom Item"),
} as const;

// It's good practice to always validate enums with this helper function in order to prevent
// crashes.
validateCustomEnum("CollectibleTypeCustom", CollectibleTypeCustom);

// Elsewhere in the code:
if (
  player.HasCollectible(CollectibleTypeCustom.MY_CUSTOM_ITEM)
  && player.HasCollectible(CollectibleType.EPIC_FETUS)
) {
  // Handle the specific synergy with My Custom Item + Epic Fetus.
}
```

As a side note, you might be wondering why the above code uses
`const CollectibleTypeCustom` instead of `enum CollectibleTypeCustom`. The basic
explanation is that we want the types of the values to be `CollectibleType`, so
that we can use them later on in the API. For a more in-depth explanation, see
the page on
[the differences between enums and objects](/main/enums-and-objects/).

### Extending Enums --> Custom Enums (Part 2)

In the previous section, we used an object to emulate an enum. Because the
return value of the `Isaac.GetItemIdByName` method is equal to
`CollectibleType`, the properties of `CollectibleTypeCustom` are of type
`CollectibleType`. Thus, we can automatically use the values of
`CollectibleTypeCustom` in any spot where we would normally be able to use
`CollectibleType`. Nice!

However, this pattern won't work for all kinds of custom enums. For example,
let's consider the case of making a mod with a custom effect. In this case, we
would want to make a `EffectVariantCustom` that "extends" from `EffectVariant`:

```ts
const EffectVariantCustom = {
  MY_CUSTOM_EFFECT: Isaac.GetEntityVariantByName("My Custom Effect"),
} as const;
```

This is not like the previous example. Here, the value of
`EffectVariantCustom.MY_CUSTOM_EFFECT` is equal to `int` instead of
`EffectVariant`. This is because the return type of the
`Isaac.GetEntityVariantByName` method is `int`. This should kind of make sense,
because at compile-time, the method has no idea what type of entity name
corresponds with what type of entity variant.

However, fixing this problem is easy. We just have to manually specify what the
variant is using a type assertion, like this:

```ts
const EffectVariantCustom = {
  MY_CUSTOM_EFFECT: Isaac.GetEntityVariantByName(
    "My Custom Effect",
  ) as EffectVariant,
} as const;
```

Now, `EffectVariantCustom` can be used in any place that `EffectVariant` can.

<br />

### Vector Operators

In Isaac modding, working with Vectors is common. For example, you might want to
double the speed of an enemy projectile. Doing this in Lua is simple:

```lua
-- Lua code
-- Double the speed of the projectile.
projectile.Velocity = projectile.Velocity * 2
```

This code is the actually the same as writing:

```lua
-- Lua code
-- Double the speed of the projectile.
projectile.Velocity = projectile.Velocity:__mul(2)
```

Under the hood, Lua converts the first code snippet to the second code snippet
automatically. This is because it understands that `__mul` is a special operator
method. Most people write code in the first way instead of the second way,
because it is more convenient.

In TypeScript, we unfortunately cannot code in the first way due to
[limitations in TypeScriptToLua](https://typescripttolua.github.io/docs/advanced/writing-declarations/#operator-overloads).
Since operator overloads will not work, we instead call the convenience methods
`add`, `sub`, `mul`, and `div`.

Here's an example:

```lua
-- Lua code
local vector = Vector(1, 1) * 5 + 2
```

```ts
// TypeScript code
const vector = Vector(1, 1).mul(5).add(2);
```

If you are converting Lua code, make sure to account for order of operations:

```lua
-- Lua code
local vector = Vector(1, 1) + Vector(3, 3) * 6
-- (multiplication happens before addition)
```

```ts
// TypeScript code
let vector = Vector(3, 3).mul(6).add(Vector(1, 1);
```

Note that if you really need to, you can restore operator overloading for
Vectors by creating a
[branded type](https://egghead.io/blog/using-branded-types-in-typescript) with
something along the lines of:

```ts
type Vector = number & { readonly __vectorBrand: symbol };
```

But this is **not recommended** because vectors will not be type-safe anymore.

<br />

### Iterating Over Enums

Sometimes, you might want to iterate over an enum. For example, the following
Lua code is a decent way to detect if the player is pressing any particular
button on the keyboard:

```lua
-- Lua code
-- "Keyboard" is an enum provided by the game.
for keyName, keyCode in pairs(Keyboard) do
  if Input.IsButtonPressed(keyCode, 0) then
    print("Player pressed: " .. keyName)
  end
end
```

In TypeScript, we can use the `getEnumEntries` helper function:

```ts
// TypeScript code
// (You can store the result of `getEnumEntries` if you want to optimize multiple calls.)
for (const [keyName, keyCode] of getEnumEntries(Keyboard)) {
  if (Input.IsButtonPressed(keyCode, 0)) {
    print(`Player pressed: ${keyName}`);
  }
}
```

You can also use the `getEnumKeys` and `getEnumValues` helper functions,
depending on what you need to do.

If you stick with these helper functions, everything should work great. If you
want to know more about what is happening under-the-hood, then read the next
section.

### Enum Reverse Mappings

First, see the previous section on
[iterating over enums](#iterating-over-enums).

Normally, TypeScript transpiles enums to JavaScript with a double mapping of key
to value and value to key. TypeScriptToLua also copies this behavior when
transpiling TypeScript to Lua. For example:

```ts
enum TestEnum {
  ONE = 1,
  TWO = 2,
  THREE = 3,
}
```

Will transpile to:

```lua
local TestEnum = {}
TestEnum.ONE = 1
TestEnum[TestEnum.ONE] = "ONE"
TestEnum.TWO = 2
TestEnum[TestEnum.TWO] = "TWO"
TestEnum.THREE = 3
TestEnum[TestEnum.THREE] = "THREE"
```

This is a great feature, because you can get the key name of an enum value super
easily:

```ts
const currentTestValue = TestEnum.TWO;
print(`currentTestValue = ${currentTestValue}: ${TestEnum[currentTestValue]}`);
// Prints "currentTestValue: 2 (TWO)"
```

However, this means that if you were to naively iterate over the enum with
`Object.entries` or `pairs`, you have to use some type-checking:

```ts
for (const [key, value] of Object.entries(TestEnum)) {
  // Ignore the reverse mappings created by TypeScriptToLua.
  if (isNumber(value)) {
    print(`Key: ${key}`);
    print(`Value: ${value}`);
  }
}
```

This is exactly what the `getEnumValues` helper function does.

Finally, there are some other small things to mention:

1. Reverse mappings are not created for string-based enums, so you only have to
   worry about this for number-based enums.

1. All of the "flag" enums (e.g. `EntityFlag`, `TearFlag`, etc.) do not have a
   reverse mapping. This is because they are not "real" TypeScript enums, but
   are instead objects that are branded with a `BitFlag` type. If you want to
   get the key of a "fake" enum like this, use the `getEnumKey` helper function.
   (The compiler won't let you index these types of enums, so the problem should
   be obvious if you ever come across it.)

1. The `getEnumEntries` (and related) helper functions will return the entries
   sorted by value. This may be surprising to you. For example:

```ts
enum MyEnum {
  ThirdValue = "third-value",
  FourthValue = "fourth-value",
}

for (const key of getEnumKeys(MyEnum)) {
  print(key); // Will print "fourth-value", then "third-value".
}
```

Instead, you might expect that the enum helper functions would return the
entries in the order that they were defined in. However, it is impossible to
determine declaration order at run-time. This is because under-the-hood, the
`pairs` function is used to iterate over an enum table, and it will always
return the results in a random order.

Since number enums are always declared in order of value, you would probably
only ever observe this oddity with an enum that has string values.

<br />

### npm Dependencies

Unfortunately, you can't use JavaScript or TypeScript libraries from npm, since
TypeScriptToLua does not support that. However, if you need a specific function,
then you can simply copy paste it into your own code.

On the other hand, if you want to split IsaacScript code between repositories or
share a library with others, TypeScriptToLua does allow
[using and creating npm packages containing .lua files](https://typescripttolua.github.io/docs/external-lua-code).
This is exactly what the `isaacscript-common` package does. Check out the
TypeScriptToLua docs for more details.

<br />

### Throwing Errors

Normally, in TypeScript programs, you would handle errors with
`throw new Error("foo")`. For example:

```ts
const player = entity.ToPlayer(); // The type of player is "EntityPlayer | undefined".
if (player === undefined) {
  throw new Error("Failed to convert the player!");
}
player.AddSoulHearts(1); // The type of player is now "EntityPlayer".
```

However, in Isaac mods, this code won't work. It will error with something along
the lines of the following:

`[Foo] Error in "foo" call: ...n\The Binding of Isaac Rebirth/mods/foo/main.lua:100: attempt to index a nil value (global 'debug')`

This is because TypeScriptToLua transpiles `throw` to a function that uses Lua's
`debug` library, and Isaac does not normally have access to `debug` for
sandboxing reasons. But not to worry, because we can simply use Lua's `error()`
function instead. For example:

```ts
const player = Isaac.ToPlayer(); // The type of player is "EntityPlayer | undefined".
if (player === undefined) {
  error("Failed to convert the player!");
}
player.AddSoulHearts(1); // The type of player is now "EntityPlayer".
```

(TypeScript is smart enough to know that `error()` can constrain the type of
player in the same way that `throw` normally would.)

<br />

### Circular Dependencies

In some programming languages,
[circular dependencies](https://en.wikipedia.org/wiki/Circular_dependency) are
allowed. JavaScript and TypeScript are two of those languages. However, Lua is
not. Thus, if you compile a program with circular dependencies, it may cause a
stack overflow at run-time.

By default, IsaacScript projects ship with the
[`import-x/no-cycle`](https://github.com/un-ts/eslint-plugin-import-x/blob/master/docs/rules/no-cycle.md)
ESLint rule turned on, which should immediately alert you to this problem if it
happens.

Programs with circular dependencies are generally considered to be spaghetti. If
you have circular dependencies in your Isaac mod, it is a sign that you almost
certainly need to rethink your architecture to something more sane.

<br />

### Save Data Manager

IsaacScript includes a [save data manager](/isaacscript-common/) that you will
almost certainly want to use in your mods. Most of the time, you can use the
save data manager without any hassle. However, there are some complicated cases
where the `saveDataManager` function will throw a compiler error when trying to
register your local variables. This section documents the special errors that it
throws.

#### Functions are not serializable

(This is a compiler error.)

This error means that you are trying to put a function on one of the fields in
your local variables. Doing that doesn't make much sense, because functions
cannot be written to the "save#.dat" file when the player saves and quits a run.

In most cases, if you are trying to save a function, you are probably doing
something wrong and should refactor your mod to use serializable data
structures.

If you absolutely have to work with functions, then you could move this field to
a `room` sub-object, which is never saved to disk. Otherwise, you can pass
`false` as the second argument to the `saveDataManager` function to prevent it
from writing any part of the variables to disk.

#### Isaac API classes are not serializable

(This is a compiler error.)

This error means that you are trying to put an Isaac API class (such as e.g.
`Entity` or `RoomConfig`) on one of the fields in your local variables. Doing
that doesn't make much sense, because these kinds of objects cannot be written
to the "save#.dat" file when the player saves and quits a run. (Even if some of
the properties were copied, there would be no way to recreate the object on the
other end.)

In most cases, if you are trying to save an Isaac API class, then you are
probably doing something wrong, and you should instead use some kind of index.
(For example, see the `getPlayerIndex` and `getPickupIndex` helper functions.)

If you absolutely have to work with Isaac API classes, then you could move this
field to a `room` sub-object, which is never saved to disk. Otherwise, you can
pass `false` as the third argument to the `saveDataManager` function to prevent
it from writing any part of the variables to disk.

#### Failed to deep copy a `DefaultMap`

(This is a run-time error, so you will see it in the console or in the "log.txt"
file.)

The `DefaultMap` class is not serializable when it has a factory function
generating the default value and is also inside of an array, map, or set.

In other words, the map cannot be written to the "save#.dat" file when the
player saves and quits a run. (This is because functions cannot be serialized,
so there is no way for the deserializer to execute the corresponding factory
function.)

To work around this problem, you could use a normal `Map` instead of a
`DefaultMap`. This is probably the most straightforward way to fix the problem.

Additionally, a `DefaultMap` that is placed as a field of a normal `run` or
`level` sub-object is serializable. Thus, you could refactor your data structure
so that the `DefaultMap` is not nested inside of the array, map, or set.

If you want to give up entirely on saving the data, then you could move this
field to a `room` sub-object, which is never saved to disk. Alternatively, you
can pass `false` as the third argument to the `saveDataManager` function to
prevent it from writing any part of the variables to disk.

#### Failed to deserialize a TSTL class

(This is a run-time error, so you will see it in the console or in the "log.txt"
file.)

Here, a TSTL class refers to a TypeScriptToLua class. In other words, when you
use the TypeScript `class` keyword, under the hood TypeScriptToLua will convert
that to a special kind of Lua table.

The error message means that the player started a new run or continued an old
run, which caused the save data manager to read the "save#.dat" file, which
caused it to try and deserialize all the data, and it found a class that it
could not instantiate because it has no corresponding constructor.

In order to create a TSTL class, you use the corresponding constructor (e.g.
`new Foo()`). Normally, when the save data manager copies a TSTL class, it uses
the constructor from the old object. However, when a TSTL class is nested inside
of an array, map, or set, there is no reference object to "get" the constructor
from. Thus, it can't copy classes in this situation without knowing about the
class beforehand.

If you want to use nested classes in this way, you can register them with the
save data manager immediately after upgrading your mod with the
`saveDataManagerRegisterClass` method:

```ts
class Foo {}
class Bar {}

const mod = upgradeMod(modVanilla, [ISCFeature.SAVE_DATA_MANAGER]);
mod.saveDataManagerRegisterClass(Foo, Bar);
```

<br />

================================================================================
// File: packages/docs/content/main/isaacscript-in-lua.md
================================================================================
---
title: Using IsaacScript in Lua
---

<!-- markdownlint-disable MD034 -->

A [library](<https://en.wikipedia.org/wiki/Library_(computing)>) is a collection
of helper functions and features that make writing your program easier. Instead
of sticking a ton of low-level code in your program, you can instead call a
single library function, abstracting away all the complexity and keeping your
program nice and clean. In the Isaac modding scene, libraries are really great
because the standard API is quite limited.

The IsaacScript framework contains two _Binding of Isaac: Repentance_ libraries:

- `isaac-typescript-definitions` - A leveled-up version of the vanilla enums
  with many bug fixes and community contributed additions for everything that
  the developers forgot to include. You can learn more about every enum by
  [reading the documentation](/isaac-typescript-definitions).
- `isaacscript-common` - Helper functions and features that abstract away much
  of the complexity in working with the Isaac API. It's the biggest and most
  advanced Isaac library ever written. You can learn more about every function
  and feature by [reading the documentation](/isaacscript-common).

If you are writing your mod in [TypeScript](/main/features/), then using these
libraries is effortless - you can just start typing the names of the enums or
functions, and the auto-complete will automatically import them (and include
them in your final bundled mod).

If you are writing your mod in Lua, then you can also leverage the power of
these libraries by downloading the `isaacscript-common.lua` file and placing it
alongside your Lua code. Read on for the specifics.

Note that for Lua users, both `isaac-typescript-definitions` and
`isaacscript-common` are combined into one library bundle, so all you need is
one file. From here on out, both libraries will be simply referred to as "the
library".

<br />

## Automatic Installation (Optional)

If you have Python installed on your computer and you know what a terminal/shell
is, then the easiest way to install the library is to use the `isaacscript-lua`
Python tool. Otherwise, you can use the
[manual installation](#manual-installation) (see below).

- In a terminal, navigate to the directory of your mod.
- Install the tool: `python -m pip install isaacscript-lua --upgrade`
- Install the Lua library: `isaacscript-lua install`

If you get
`ERROR: Could not find a version that satisfies the requirement isaacscript-lua (from versions: none)`,
that means that your version of Python is too old. Make sure that you have
Python version 3.10 or later installed.

<br />

## Manual Installation

Here, "installing" is a loose term. All you really need to do is to put the
`isaacscript-common.lua` file inside your mod. (This is essentially the same
thing as copy-pasting code snippets directly into your mod, except that the
library code lives in its own dedicated file.)

### Step 1 - Download the Library

Download it from the npm registry:
https://unpkg.com/isaacscript-common@latest/dist/isaacscript-common.lua

Use right-click + save link as.

(Note that by specifying "latest" as the version in the URL, the website will
redirect us to the numbers that correspond to the latest version.)

It will save to a file called "isaacscript-common.lua".

### Step 2 - Put It In Your Mod

- Create a subdirectory in your mod called the same thing as you mod.
  - For example, if your mod is located at `C:\Repositories\revelations`, create
    a subdirectory called `C:\Repositories\revelations\revelations`.
- Create a subdirectory in the new directory called `lib`.
  - For example, if your mod is located at `C:\Repositories\revelations`, create
    a subdirectory called `C:\Repositories\revelations\revelations\lib`.
- Put the "isaacscript-common.lua" file in the `lib` directory.
  - For example, if your mod is located at `C:\Repositories\revelations`, it
    would go to
    `C:\Repositories\revelations\revelations\lib\isaacscript-common.lua`.

In other words, your file structure should look something like this:

```text
my-mod/
|── main.lua (the Lua entry point to your mod)
|── metadata.xml (the Steam Workshop file)
└── my-mod/ (a subdirectory with the same name as your mod for the purpose of preventing namespace conflicts)
    └── lib/ (a subdirectory that contains 3rd-party library code)
        └── isaacscript-common.lua
```

(Creating a directory of the same name is necessary because in the Isaac
environment, we must
[namespace all of our code](https://wofsauge.github.io/IsaacDocs/rep/tutorials/Using-Additional-Lua-Files.html#the-namespacing-problem-with-require).
As the documentation explains, using `include` does not obviate the need to do
this because we need the ability to access the library in more than one Lua
file. Having to namespace code is one of the disadvantages of using Lua instead
of TypeScript.)

<br />

## Basic Usage

### Import the Library

At the top of the Lua file where you want to use the library, use the following
import statement:

```lua
local isc = require("my-mod.lib.isaacscript-common")
```

Note that:

- You must replace "my-mod" with the name of your mod, which corresponds to the
  namespaced directory from the previous step.
- The period in the `require` invocation is a directory separator. (It is
  conventional in Lua to use a period instead of a slash.)
- You must repeat this import statement in every Lua file where you use the
  library. (One disadvantage of using Lua over TypeScript is that you don't have
  automatic imports.)

### Using Pure Functions

Most functions in the library are exported from the root. For example:

```lua
local isc = require("my-mod.lib.isaacscript-common")

local function anyPlayerHasSadOnion()
  return isc:anyPlayerHasCollectible(CollectibleType.COLLECTIBLE_SAD_ONION)
end

if anyPlayerHasSadOnion() then
  print("One or more players has a Sad Onion.")
end
```

Note that similar to most Lua libraries, you must use a colon (instead of a
period) when invoking functions, since the library is an exported module.

### Using Enums

As previously mentioned, the enums from `isaac-typescript-definitions` are also
exported from `isaacscript-common` for your use.

For example, there is no vanilla `GaperVariant` enum, but in IsaacScript, there
is:

```lua
if entity.Type == EntityType.ENTITY_GAPER and entity.Variant === isc.GaperVariant.FLAMING_GAPER then
  print("This is a Flaming Gaper!")
end
```

One of the advantages of the improved enums is that they don't have the
pointless prefix. So you could slightly improve the previous code snippet like
this:

```lua
if entity.Type == isc.EntityType.GAPER and entity.Variant === isc.GaperVariant.FLAMING_GAPER then
  print("This is a Flaming Gaper!")
end
```

As a general safety practice, you should always use the library enums over the
vanilla enums because the vanilla enums are not safe - they can be modified by
other mods and deleted.

<br />

### Using Custom Callbacks

Like any good library, importing anything in `isaacscript-common` will not cause
any code to be executed in your mod. Most of its functions are
[pure functions](https://en.wikipedia.org/wiki/Pure_function).

However, in order for
[the custom callbacks](/isaacscript-common/enums/modcallbackcustom/) and the
[extra features](#using-extra-features) to work, some code does need to be
executed. This is because these features need to track when certain things
happen in-game. In order to enable this functionality, you must upgrade your mod
with the `upgradeMod` function.

For example:

```lua
local isc = require("my-mod.lib.isaacscript-common")

local modVanilla = RegisterMod("Foo", 1)
local mod = isc:upgradeMod(modVanilla)

-- Register normal callbacks.
mod:AddCallback(ModCallbacks.MC_USE_ITEM, function(collectibleType)
  Isaac.DebugString("MC_USE_ITEM fired - item was: " .. tostring(collectibleType))
end)

-- Register custom callbacks.
mod:AddCallbackCustom(isc.ModCallbackCustom.POST_ITEM_PICKUP, function(player, pickingUpItem)
  Isaac.DebugString("POST_ITEM_PICKUP fired - item was: " .. tostring(pickupUpItem.subType))
end)
```

<br />

### Using Extra Features

Some helper functions rely on stateful tracking (like `isPlayerUsingPony`) or
store data about what you want to do for later (like `setHotkey`). These fall
under the category of "extra features". Since they are non-pure, you are only
able to access them if you upgrade your mod. However, this is slightly different
than upgrading your mod for custom callbacks.

Instead of activating every feature when you upgrade your mod, the standard
library keeps things blazing fast by only activating the specific features that
you need. Thus, when you upgrade your mod, you have to tell the library which
features you want by passing them as the second argument to the `upgradeMod`
function.

For example:

```lua
local isc = require("my-mod.lib.isaacscript-common")

local modVanilla = RegisterMod("Foo", 1)
local features = { -- An array of features.
  isc.ISCFeature.PONY_DETECTION,
}
local mod = isc:upgradeMod(modVanilla, features)

mod:AddCallback(ModCallbacks.MC_POST_PEFFECT_UPDATE, function (player)
  local usingPony = mod:isPlayerUsingPony(player);
  Isaac.DebugString("Is this player using a Pony? " .. tostring(usingPony));
end)
```

Here, by specifying that we want the "pony detection" feature, extra methods are
added on to the mod object. Then, we can proceed to use those methods throughout
our mod.

<br />

## Updating the Library

The `isaac-typescript-definitions` and `isaacscript-common` packages change
frequently with bug fixes and new features. You can read about the latest
changes on the [change log](/main/change-log/) or by reading the
[commits to the monorepo](https://github.com/IsaacScript/isaacscript/commits/main).
Subsequently, it is a good idea to keep your library version up to date.

- The version of your downloaded library can be found in a comment at the top of
  your `isaacscript-common.lua` file.
- The latest version of the `isaacscript-common` library can be found on
  [the npm page](https://www.npmjs.com/package/isaacscript-common) (below the
  title at the top of the page).

To update, you can manually download the latest Lua file again from the links
above. Or, if you have the `isaacscript-common` Python tool installed, you can
simply run: `isaacscript-common update`

<br />

## Using JavaScript/TypeScript Array Methods in Lua

In JavaScript/TypeScript, arrays come preloaded with
[a bunch of useful methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
such as `map` and `filter`, which allow you to write functional, high-level
code.

Many of these array methods are now provided as
[convenience functions](/isaacscript-common/functions/arraylua/) inside of
`isaacscript-common` specifically for Lua users who don't have these methods
natively.

If you find yourself using a `for` loop to iterate over an array - stop. Become
a better programmer and
[use a higher-order function instead.](https://www.syncfusion.com/blogs/post/javascript-higher-order-functions-a-complete-guide.aspx)

<br />

## Steam Workshop

You might be wondering why `isaacscript-common` is not offered on the Steam
Workshop. Having Isaac libraries live on the workshop is a poor design choice,
as it forces end-users to subscribe to an extra thing. When someone wants to
play your mod, they should only have to subscribe to one thing - your mod.

Furthermore, having the library logic bundled with the mod preserves backwards
compatibility and ensures that library is tightly-coupled to the mod logic that
is using it. It also allows the mod author to be in complete control of when
they update to the latest version, if ever. This also allows the upstream
library to make breaking changes and stay clean without having to worry about
having perpetual technical debt.

<br />

## The IsaacScript Stage Library

The IsaacScript standard library contains the ability to create
[custom stages](/main/custom-stages/), which was inspired by StageAPI and aims
[to improve upon it](/main/custom-stages/#motivation).

<!-- cspell:ignore setcustomstage -->

Note that some of the custom stage functions (such as e.g. `setCustomStage`)
cannot be used in Lua, since they require a compiler to generate the custom
stage metadata. For advanced users, you could manually prepare the metadata, but
at that point you would probably be better off using
[StageAPI](https://github.com/Meowlala/BOIStageAPI15), since nothing you write
is going to be type safe anyway.

<br />

## File Size

The file size of the library is around 2 megabytes, so using the library will
increase the total size of your mod by that amount. With that said, the file
size of your mod is mostly irrelevant for a few reasons. This is a common
misconception by newer programmers, so it is worth taking a few minutes to
explain why this is.

### Running Time

A library's run-time is defined as the time it takes for its code to execute
while the player is inside of the game, actively playing. Just because a library
has a large file size does not mean that it takes a long time to execute.
Obviously, not all lines of code are created equal, and different kinds of code
will take varying amounts of time to execute.

As [previously mentioned](#using-custom-callbacks), `isaacscript-common` will
not cause any code to be executed in your mod by default. Thus, it has no
run-time cost whatsoever if you are just using enums and pure functions.

On the other hand, if you explicitly upgrade your mod, some extra code is
executed using some vanilla callbacks. However, the code is extremely efficient
such that callback code is only ever executed if you are actually using the
specific callback. Thus, thousands of copies of the standard library can run
simultaneously without ever measuring a run-time performance penalty.

### Loading Time

Loading time is defined as the time it takes for the game to load the Lua code
when the game first boots. Just because a library has a large file size does not
mean that it takes a long time for the game to load it.

In general, we care about loading time a lot less than the run-time, because it
only happens when the user first launches the game. And it is largely invisible
to the end-user playing the mod.

With that said, loading the library has been measured to take around 4
milliseconds. Thus, you could load the library around 250 times in a row before
an end-user would ever even start to notice. So, even if you are passionate
enough to care about this, the library is around three orders of magnitude too
small for it to matter.

### Download Time

Download time is defined as the time it takes to download the mod over Steam.
This is probably the place where the size of your mod matters the most.

With that said, we care about download time even less than loading time, because
it only happens once on the initial mod download. (It would also happen if you
upload a mod patch post-release.) Obviously, this is going to happen a lot less
and matter a lot less than the previous two sections.

In 2022, the
[average internet speed is 64.7 Mbps](https://www.oberlo.com/statistics/average-internet-speed-by-country).
This means that on average, users will be able to download the library in just
0.3 seconds. (Average speed also increases every year, so this number will be
even smaller by the time you are reading this.)

How much does 0.3 seconds matter? That depends on your much you value sub-second
optimizations that will only happen once-per-user over the lifetime of your
product. For most sane people, this will be near-zero.

### Other Assets

Note that for many mods, the size of your assets (e.g. sprite files, sound
files, music files, room files) will vastly outweigh the size of all of your
code. So even if the file size of your code did matter (which it doesn't), it
would quickly become more important to spend time and energy on reducing the
file size of the assets instead of worrying about optimizing the code.

In order to further drive home this point home, consider that the most popular
Repentance mod of all time is
[Fiend Folio](https://steamcommunity.com/sharedfiles/filedetails/?id=2851063440),
which clocks in at around 581 megabytes. That is **several orders of magnitude
larger than the standard library**, and yet virtually no-one in the Isaac
ecosystem cares.

### Minification

It is possible to reduce the file size of the library by using a
[Lua minifier](https://www.npmjs.com/package/isaacscript-common). However, it is
not recommended to do this, because it will not improve the run-time speed of
your mod. (The whole point of minification is to reduce the file size of the
mod, but doing that is near-pointless, as the previous four sections have
established.)

Furthermore, minification is actively harmful since it will obfuscate the line
numbers of your run-time errors. (Run-time errors are mostly non-existent if you
use TypeScript, but they happen a ton in Lua.)

## TypeScript

If you find the IsaacScript standard library useful, you should consider using
it in a TypeScript mod. TypeScript has the advantage of auto-complete,
auto-importing, and the compiler preventing you from ever misusing anything in
the library. Taken together, it makes for a dream-like Isaac development
experience.

For more information, see the [list of features](/main/features/). (If you don't
know how to program in TypeScript, then you can learn in around
[30 minutes](/main/javascript-tutorial/).)

================================================================================
// File: packages/docs/content/main/javascript-tutorial.md
================================================================================
---
title: JavaScript/TypeScript Tutorial
---

If you have never programmed in JavaScript/TypeScript before, but you **have**
programmed in Lua, then this page is for you. Below, you can compare Lua code
side by side with the equivalent TypeScript code. If you have coded a mod in Lua
before, reading through this page will probably be enough to get you started.

If you have never programmed in Lua before, then this page will still be useful,
but you can skip reading all of the Lua code blocks. (But it can't hurt to learn
some Lua too. The best Isaac modders will fluently know both languages.)

<br />

## Level 1 - Basic

<br />

### Comments

```lua
-- This is a single-line comment in Lua.

--[[

This is a multi-line comment in Lua.
It's very long.
And wordy.

--]]
```

```ts
// This is a single-line comment in TypeScript.

/*

This is a multi-line comment in TypeScript.
It's very long.
And wordy.

*/
```

<br />

### Semi-Colons

Unlike Lua, TypeScript code should have semi-colons after every line.

```lua
-- Lua code
Isaac.DebugString("hello world")
```

```ts
// TypeScript code
Isaac.DebugString("hello world");
```

But don't bother typing the semi-colons yourself - just hit `Ctrl + s` and the
editor will automatically insert them for you. That's
[Prettier](https://prettier.io/) doing its job.

(In fact, you should always hit `Ctrl + s` periodically as you code, so that the
code is constantly formatting itself. This frees you from the tedium of aligning
things, breaking up long if statements, and so forth. If the file is not
auto-formatting itself, then you probably need to add a bracket somewhere so
that the code can properly compile.)

<br />

### Colons

In Lua, you sometimes call functions with a colon, and you sometimes call
functions with a period. This is really annoying.

In TypeScript, you call all functions with a period. Easy.

```lua
-- Lua code
Isaac.DebugString("hello world")
Isaac.GetPlayer():AddMaxHearts(2)
```

```ts
// TypeScript code
Isaac.DebugString("hello world");
Isaac.GetPlayer().AddMaxHearts(2);
```

<br />

### Variables: `local` ➜ `const` and `let`

In Lua, you type `local` before declaring a variable to stop it from being
turned into a global.

In TypeScript, this isn't necessary. There are no global variables, unless we
explicitly decide to create one.

Furthermore, in TypeScript, there are two kinds of variable declarations: `let`
and `const`.<br /> (Don't ever use `var`, which is only used in older JavaScript
code.)

```lua
-- Lua code
local poop = "poop"
local numFarts = 1
numFarts = numFarts + 1 -- numFarts is now equal to 2.
```

```ts
// TypeScript code
const poop = "poop"; // We use "const" because this value never changes.
let numFarts = 1; // We use "let" because we have to modify it later.
numFarts = numFarts + 1; // numFarts is now equal to 2.
```

<br />

### Functions

```lua
-- Lua code
function getNumPoops() -- This is a global function.
  return 2
end

local function getNumFarts() -- This is a local function.
  return 3
end
```

```ts
// TypeScript code
// All functions in TypeScript are local by default.
function getNumPoops() {
  return 2;
}
```

<br />

### Anonymous Functions

For very small functions, it is common to type them anonymously (i.e. without a
name).

```lua
-- Lua code
mod:AddCallback(ModCallbacks.POST_NEW_LEVEL, function()
  Isaac.DebugString("Arrived on a new floor.")
end);
```

```ts
// Typescript code
mod.AddCallback(ModCallbacks.POST_NEW_LEVEL, () => {
  Isaac.DebugString("Arrived on a new floor.");
});
```

(If this syntax looks confusing, google "JavaScript arrow functions" in order to
get more familiar with them. But of course, you don't have to use arrow
functions if you don't want to.)

<br />

### Arrays

An array is a data structure that is an ordered list of elements. In Lua, you
use a table to represent an array.

```lua
local myArray = {"foo", "bar", "baz"}
```

In TypeScript, there is a dedicated syntax for arrays: the square brackets.

```ts
const myArray = ["foo", "bar", "baz"];
```

In Lua, there are two different ways to add an element to an array:

```lua
table.insert(myArray, "someNewElement")
myArray[#myArray + 1] = "anotherNewElement"
```

In TypeScript, you use the `push` method:

```ts
myArray.push("someNewElement");
```

In addition to `push`, arrays have a lot of other handy methods that you can
use. You can see all of them in
[the MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).

<br />

### Objects

An object is a data structure that stores key/value pairs. In Lua, you use a
table to represent an object. (An equal sign is used in between the keys and
values.)

```js
local myObject = {
  foo = 123,
  bar = 456,
  baz = 789,
}
```

In TypeScript, there is a dedicated syntax for objects: the curly brackets. (A
colon is used in between the keys and the values.)

```ts
const myObject = {
  foo: 123,
  bar: 456,
  baz: 789,
};
```

In Lua, there are two different ways to set an element:

```lua
myObject.foo = 999
myObject["foo"] = 999
```

In TypeScript, it is the exact same thing:

```ts
myObject.foo = 999;
myObject["foo"] = 999;
```

(But ESLint will change the second form to the first form automatically when you
save the file, so that everything remains consistent.)

<br />

### `if` Statements and Operators

In Lua, you don't put parentheses around the conditions of an `if` statement.
But in TypeScript, you do.

Also, the operators are a bit different:

- `and` ➜ `&&`
- `or` ➜ `||`
- `==` ➜ `===`
- `~=` ➜ `!==`
- `..` ➜ `+`

For example:

```lua
-- Lua code
if x == 1 and y ~= 0 then
  -- Do something.
end
```

```ts
// TypeScript code
if (x === 1 && y !== 0) {
  // Do something.
}
```

If you find typing three equal signs annoying, then don't bother: if you type
`==` instead, ESLint will automatically convert it to `===` when you save the
file.

<br />

### `for` Statements for Counting

In Lua, basic `for` loops look like this:

```lua
-- Lua code
for i = 1, 10 do
  -- "i" will iterate upwards from 1 to 10.
end
```

In TypeScript, you use the more-standard C-style syntax:

```ts
// TypeScript code
for (let i = 1; i <= 10; i++) {
  // "i" will iterate upwards from 1 to 10.
}
```

Alternatively, you can use the `iRange` helper function provided by the
`isaacscript-common` standard library. This allows the code to be a bit more
safe & understandable:

```ts
// TypeScript code
for (const i of iRange(1, 10)) {
  // "i" will iterate upwards from 1 to 10.
}
```

In Lua, you count downwards like this:

```lua
-- Lua code
for i = 10, 1, -1 do
  -- "i" will iterate downwards from 10 to 1.
end
```

In TypeScript, that would be:

```ts
// TypeScript code
for (let i = 10; i >= 1; i--) {
  // "i" will iterate downwards from 10 to 1.
}
```

Or, with the `iRange` helper function:

```ts
// TypeScript code
for (const i of iRange(10, 1)) {
  // "i" will iterate downwards from 10 to 1.
}
```

Note that you can also use the `eRange` helper function for an exclusive range
(instead of an inclusive range).

<br />

### `for` Statements for Arrays

In Lua, the typical way to iterate over an array is with `ipairs`.

```lua
-- Lua code
local gapers = Isaac.FindByType(EntityType.ENTITY_GAPER)

for i, gaper in ipairs(gapers) do
  gaper:Remove()
  print("Removed gaper number:", i);
end
```

In TypeScript, you have a few different options.

```ts
// Typescript code
const gapers = Isaac.FindByType(EntityType.ENTITY_GAPER);

// A "for of" loop is the simplest way to iterate over an array. It provides the array element.
for (const gaper of gapers) {
  gaper.Remove();
}

// If you need the array index and the array element, use the `entries` method.
for (const [i, gaper] of gapers.entries()) {
  gaper.Remove();
  print("Removed gaper number:", i);
}

// If you just need the array index, use the `keys` method.
// The keys start at 0, unlike Lua. (In Lua, array keys start at 1.)
for (const i of gapers.keys()) {
  print("On gaper index:", i);
}
```

<br />

### `for` Statements for Key/Value Tables

In Lua, the typical way to iterate over a key/value table is with `pairs`.

```lua
-- Lua code
-- Define a table of collectible prices.
-- (We must put "[]" around the collectible types since the table keys are numbers.)
local collectiblePrices = {
  [3] = 15, -- Spoon Bender is 15 coins.
  [4] = 15, -- Cricket's Head is 15 coins.
  [5] = 7, -- My Reflection is 7 coins.
}

for collectibleType, price in pairs(collectiblePrices) do
  -- Do something with "collectibleType" and "price".
end
```

In TypeScript, you have a few different options.

```ts
// TypeScript code
// Define an object containing collectible prices.
const collectiblePrices = {
  [3]: 15, // Spoon Bender is 15 coins.
  [4]: 15, // Cricket's Head is 15 coins.
  [5]: 7, // My Reflection is 7 coins.
};

for (const [collectibleType, price] of Object.entries(collectiblePrices)) {
  // Do something with "collectibleType" and "price".
}

// Or, if you just need the collectible type, you would use the "keys()" method.
for (const collectibleType of Object.keys(collectiblePrices)) {
  // Do something with "collectibleType".
}

// Or, if you just need the price, you would use the "values()" method.
for (const price of Object.values(collectiblePrices)) {
  // Do something with "price".
}
```

<br />

### `nil` ➜ `undefined`

```lua
-- Lua code
if entity.SpawnerEntity == nil then
  -- This entity was not spawned by anything in particular.
end
```

```ts
// TypeScript code
if (entity.SpawnerEntity === undefined) {
  // This entity was not spawned by anything in particular.
}
```

Note that `null` also transpiles to `nil` (in addition to `undefined`). In order
to keep your code easy to read, never use `null` unless you specifically want to
model an actual null-type defined value.

<br />

## Level 2 - Intermediate

<br />

### Assignment Operators

Lua does not have assignment operators, because it is a terrible language.

```lua
-- Lua code
local numFarts = 1
numFarts = numFarts + 1 -- numFarts is now equal to 2.
```

```ts
// TypeScript code
let numFarts = 1;
numFarts += 1; // numFarts is now equal to 2.
```

<br />

### Increment and Decrement Operators

Lua does not have increment or decrement operators. Handily, TypeScript does.

```lua
-- Lua code
local numFarts = 1
numFarts = numFarts + 1 -- numFarts is now equal to 2.
```

```ts
// TypeScript code
let numFarts = 1;
numFarts++; // numFarts is now equal to 2.
```

<br />

### String Concatenation

The way to concatenate strings is different:

```lua
-- Lua code
local poopString = "Poop"
local fartString = "Fart"
local combinedString = poopString .. fartString -- combinedString is now equal to "PoopFart".
```

```ts
// TypeScript code
const poopString = "Poop";
const fartString = "Fart";
const combinedString = poopString + fartString; // combinedString is now equal to "PoopFart".
```

(Unlike Lua, TypeScript uses the same operator for adding numbers and
concatenating strings.)

<br />

### String Conversion

```lua
-- Lua code
local numPoops = 3
local numPoopsString = tostring(numPoops)
```

```ts
// TypeScript code
const numPoops = 3;
const numPoopsString1 = tostring(numPoops); // You can do the same thing as you would in Lua.
const numPoopsString2 = numPoops.toString(); // Or, you can use the typical JavaScript conversion method.
```

Feel free to use either the standard Lua method or the JavaScript conversion
method - it will be transpiled to the same thing.

Furthermore, when concatenating numbers to strings, TypeScript will
automatically convert them to strings for you:

```lua
-- Lua code
local numPoops = 3
local numFarts = 4
Isaac.DebugString("numPoops: " .. tostring(numPoops) .. ", numFarts: " .. tostring(numFarts))
```

```ts
// Typescript code
const numPoops = 3;
const numFarts = 4;
Isaac.DebugString("numPoops: " + numPoops + ", numFarts: " + numFarts); // No conversion necessary!
```

### String Templates

TypeScript has a special feature that Lua does not have called _string
templates_. String templates allow you to easily create a string that has a
bunch of variables in it. They are denoted by the <code>`</code> character.

In the previous section, we used the `+` operator to combine a bunch of
variables with text. But it would be better written by using a string template,
like this:

```ts
// Typescript code
const numPoops = 3;
const numFarts = 4;
Isaac.DebugString(`numPoops: ${numPoops}, numFarts: ${numFarts}`);
```

You will probably want to get in the habit of using string templates, since they
end up making your code more concise and easier to read.

<br />

### TypeScript Type Annotations

The main thing that TypeScript adds to JavaScript is type annotations. Here's a
quick example:

```lua
-- Lua code
function postPlayerInit(player)
  player:AddCollectible(1, 0, false) -- Sad Onion
end
```

```javascript
// JavaScript code
function postPlayerInit(player) {
  player.AddCollectible(1, 0, false); // Sad Onion
}
```

```ts
// TypeScript code
function postPlayerInit(player: EntityPlayer) {
  player.AddCollectible(1, 0, false); // Sad Onion
}
```

In the TypeScript code snippet, you can see that we marked the `player` function
argument as the `EntityPlayer` type by using a colon. The `EntityPlayer` type is
automatically provided by the `isaac-typescript-definitions` package, and
corresponds to
[`EntityPlayer` in the official docs](https://wofsauge.github.io/IsaacDocs/rep/EntityPlayer.html).
(The `isaac-typescript-definitions` package is automatically added to any
IsaacScript project.)

Once the type has been annotated, your editor will know about all of the legal
methods for the `player` variable. For example, if you make a typo on the
`AddCollectible` method, the editor will immediately tell you by drawing a red
squiggly line underneath it.

When coding in TypeScript, you will need to add the type for every function
argument. That way, the compiler can catch all of the bugs.

(Note that if you are just trying out a new function, then you can quickly type
it out without the types. The compiler will give errors, but you can ignore them
and everything will work fine as you test the function in-game. Once you are
satisfied with the function, you can go back and fill in the types.)

<br />

### Type Inference For Variables

In the previous section, we provided a type annotation for a function argument
(by using a colon). It is also possible to provide a type annotation for other
things. For example, this is providing a type annotation for a variable
declaration:

```ts
const myNumber: number = 123;
```

Here, we are explicitly telling the compiler what the type of the variable is.
But in this case, doing this is redundant. The type is obviously a number,
because 123 is a number. So we can just type out the variable like normal:

```ts
const myNumber = 123;
```

Here, TypeScript will infer that `myNumber` is of type `number`, because it
knows that 123 is a number. This is called
[type inference](https://www.typescriptlang.org/docs/handbook/type-inference.html).
So, in general, we should never explicitly put the types on variables when they
can be inferred, because it adds useless noise to the code. In this way,
TypeScript saves a ton of time over older programming languages like Java. (In
Java, you have to type out the type for every single variable, which is a pain.)

However, in some cases, we do need to specify what the type of the variable is.
Imagine that we are creating a new array that will contain numbers:

```ts
// We will add some numbers types later on, but right now we just need to initialize the array.
const numberArray = [];
```

Here, TypeScript is able to infer that the type of the variable is an array. But
it can't infer what is supposed to go inside of the array, for obvious reasons.
So the type defaults to `any[]` (which means "an array containing anything").

This is bad, because we want our arrays to be type safe. Thus, when we declare
arrays (and other container-like objects), we have to tell TypeScript what kinds
of things they should contain:

```ts
const numberArray: number[] = [];
```

Much better!

<br />

### Type Inference For Functions

You can also use type annotations to specify the return type of a function, like
this:

```ts
// The return type is "boolean".
function isEven(num: number): boolean {
  return num % 2 === 0;
}
```

Here, providing the return type annotation is optional. If we don't specify it,
the compiler would infer what the return type is automatically, saving us the
time from having to type it out.

With that said, just because we don't _have_ to type it does not mean that we
should _never_ type it. Having return type annotations on functions is often
pretty useful, as it can catch bugs when you accidentally return things that you
did not intend.

<br />

### Void

If a function is not expected to return anything, then the return type is
`void`. For example:

```ts
function addSadOnion(player: EntityPlayer): void {
  player.AddCollectible(1); // Sad Onion
}
```

But annotating a return type of void is pretty pointless, so the function is
better written without the return type annotation:

```ts
function addSadOnion(player: EntityPlayer) {
  player.AddCollectible(1); // Sad Onion
}
```

One exception is when the function is exported. (More on what exported functions
are later.) By default, the IsaacScript linter is configured to require return
types for all exported functions. So, if the previous function was exported, you
would write it like this:

```ts
export function addSadOnion(player: EntityPlayer): void {
  player.AddCollectible(1); // Sad Onion
}
```

<br />

### Splitting Your Code Into Multiple Files: `require()` ➜ `import`

In Lua, you split your code into multiple files by using `require()`.

#### `main.lua`

```lua
-- In Lua, we must namespace the mod's Lua files in a directory of the same name to avoid require
-- conflicts.
local postGameStarted = require("revelations.callbacks.postGameStarted")

local mod = RegisterMod("Revelations", 1)
postGameStarted:init(mod)
```

#### `revelations/callbacks/postGameStarted.lua`

```lua
local postGameStarted = {}

function postGameStarted:init(mod)
  mod:AddCallback(ModCallbacks.POST_GAME_STARTED, postGameStarted.main);
end

function postGameStarted:main()
  local player = Isaac.GetPlayer()
  player:AddCollectible(1, 0, false) -- Sad Onion
end

return postGameStarted
```

In TypeScript, this is accomplished with `import`.<br /> (Don't ever use the
JavaScript/TypeScript version of `require()`, which is only used in older
JavaScript code.)

#### `main.ts`

```ts
import { postGameStartedInit } from "./callbacks/postGameStarted";

const mod = RegisterMod("Revelations", 1);
postGameStartedInit(mod);
```

#### `callbacks/postGameStarted.ts`

```ts
// "export" makes it so that other files can use this function.
export function postGameStartedInit(mod: Mod): void {
  mod.AddCallback(ModCallbacks.POST_GAME_STARTED, main);
}

function main() {
  const player = Isaac.GetPlayer();
  player.AddCollectible(1, 0, false); // Sad Onion
}
```

(With TypeScript, there is no need to have a superfluous namespacing directory
like in Lua.)

<br />

## Level 3 - Advanced

<br />

### Using Global Variables

Sometimes, your mod might need to use a global variable exported by someone
else's mod. For example, you might need to use the `InfinityTrueCoopInterface`
global variable from the True Co-op Mod. (This mod is useless now in Repentance,
but in Afterbirth+, most character mods would want to register their character
with the True Co-op Mod.)

<br />

#### Option 1 - Inline Declarations

In Lua, checking to see if the user has the True Co-op Mod installed would look
something like this:

```lua
-- Lua code
if InfinityTrueCoopInterface ~= nil then
  -- The user has the True Co-op mod enabled, so now do something.
end
```

The TypeScript equivalent would look like this:

```ts
// TypeScript code
if (InfinityTrueCoopInterface !== undefined) {
  // The user has the True Co-op mod enabled, so now do something.
}
```

However, this exact code would result in an error, because the TypeScript
compiler (rightly) complains that the "InfinityTrueCoopInterface" variable does
not exist. Normally, this kind of thing is extremely useful, because when a
variable "does not exist", it usually means we forgot to initialize it or we
made a typo somewhere. However, in this case, the "InfinityTrueCoopInterface"
variable really does exist - it's just not a part of _our_ code. So, we just
need a way to tell the TypeScript compiler that.

The way to do that is to use the `declare` keyword, like this:

```ts
// TypeScript code
declare const InfinityTrueCoopInterface: unknown | undefined;

if (InfinityTrueCoopInterface !== undefined) {
  // The user has the True Co-op mod enabled, so now do something.
}
```

The `declare` keyword essentially means "the following variable exists outside
of the context of this program, and is provided by some other running code".
Importantly, `declare` statements do not actually result in any transpiled Lua
code; they are purely messages to the TypeScript compiler.

In this context, we annotate the type of the variable as `unknown | undefined`,
which means that it is either "something" or "does not exist". (`unknown` is a
special TypeScript type that you can use when you don't know what the real type
of something is.)

<br />

#### Option 2 - A Declaration File

If you check for `InfinityTrueCoopInterface !== undefined` in more than one
place in your mod, then option 1 is bad, because you would be
[need to repeat yourself before each check](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).
Instead, make a TypeScript definition file that corresponds to the variable /
table.

For example, to declare `InfinityTrueCoopInterface`, starting from the root of
your project:

- Create the `src/types` directory.
- Create the `src/types/InfinityTrueCoopInterface.d.ts` file. (A `d.ts` file is
  a TypeScript _declaration_ file.)
- Put the following in it:

```ts
declare const InfinityTrueCoopInterface: unknown | undefined;
```

Now, your other TypeScript files will "see" it as a global variable without you
having to do anything else.

<br />

### Creating Global Variables

In Lua, some mods export functionality by using a global variable:

```lua
-- Lua code
RevelationsVersion = "2.1"
-- "RevelationsVersion" is now a global variable.
```

In TypeScript, you just have to declare it beforehand:

```ts
// TypeScript code
declare let RevelationsVersion: string;
RevelationsVersion = "2.1";
// "RevelationsVersion" is now a global variable.
```

Building on this example, you can also expose both variables and methods:

```ts
declare let RevelationsExports: unknown;
RevelationsExports = {
  myVariable1,
  myVariable2,
  myFunction1,
  myFunction2,
};
// "RevelationsExports" is now a global variable.
```

<br />

### Enums

In the previous [`for` loop section](#for-statements-for-keyvalue-tables), we
defined a mapping of collectibles to prices.

Imagine that in our mod, collectibles can only be sold for three different
prices:

- 15 coins (normal)
- 30 coins (double)
- 7 coins (on sale)

This means that we can get even more specific with our collectible prices
definition by using an `enum`. Unlike Lua, TypeScript has a built-in `enum` data
type.

```ts
enum CollectiblePrice {
  NORMAL = 15,
  DOUBLE = 30,
  SALE = 7,
}

// collectiblePrices now only has values of CollectiblePrice, which is even safer than before!
const collectiblePrices = {
  [3: CollectiblePrice.NORMAL, // Spoon Bender
  [4]: CollectiblePrice.NORMAL, // Cricket's Head
  [5]: CollectiblePrice.SALE, // My Reflection
};
```

<br />

### Maps

In the previous [enums](#enums) section, we defined `collectiblePrices` as an
object, which is roughly equivalent to a Lua table.

Objects are good for cases where every possibility is accounted for. But this
isn't the case for `collectiblePrices`. Here, we are only specifying the prices
for _some_ of the collectibles in the game. If a collectible isn't in the list,
we'll probably want to ignore it, or give it a default value, or something along
those lines.

In this example, what `collectiblePrices` _really_ represents is a
[_map_](https://en.wikipedia.org/wiki/Associative_array) of a specific
collectible type to a price. Unlike Lua, TypeScript has a built-in `Map` data
type. So, the example would be better written like this:

```ts
const collectiblePrices = new Map<number, CollectiblePrice>([
  [3, CollectiblePrice.NORMAL], // Spoon Bender
  [4, CollectiblePrice.NORMAL], // Cricket's Head
  [5, CollectiblePrice.SALE], // My Reflection
]);

for (const [collectibleType, price] of collectiblePrices.entries()) {
  // Do something with "collectibleType" and "price".
}
```

In this example, `collectiblePrices` has a type of
`Map<number, CollectiblePrice>`, which is more specific than an untyped object.

- The first value in the angle brackets corresponds to the map key type.
- The second value in the angle brackets corresponds to the map value type.

We initialize the map by passing an array of key/value pairs to the constructor.
(Alternatively, we could start the map empty and then use the `set` method to
set some values later on.)

With a map, you can use all of the handy methods
[shown in the MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
(listed on the left side). Here's an example of using the `get` method to
emulate checking for a value in a Lua table:

```lua
-- Lua code
function pickingUpCollectible(player, collectibleType)
  -- If the player picked up a new collectible,
  -- subtract the price of that collectible from their coin amount.
  local price = collectiblePrices[collectibleType]
  if price ~= nil then
    player:AddCoins(price * -1)
  end
end
```

```ts
// TypeScript code
function pickingUpCollectible(player: EntityPlayer, collectibleType: int) {
  // If the player picked up a new collectible,
  // subtract the price of that collectible from their coin amount.
  const price = collectiblePrices.get(collectibleType);
  if (price !== undefined) {
    player.AddCoins(price * -1);
  }
}
```

<br />

### Type Narrowing

Lua allows you to write unsafe code. Consider the following:

```lua
-- Lua code
local player = entity:ToPlayer() -- Convert the entity to a player.
player:AddMaxHearts(2) -- Give them a heart container.
```

Not all entities convert to players though, so this code can fail. In fact, for
most entities, the `ToPlayer` method would return `nil` and cause the next line
to throw a run-time error, preventing all of the subsequent code in the callback
from firing. In TypeScript, writing this code would cause a compiler error:

```ts
const player = entity.ToPlayer();
player.AddMaxHearts(2); // Error: Object is possibly 'undefined'
```

This error is because the return type of the `ToPlayer()` method is
`EntityPlayer | undefined` (which means "either an `EntityPlayer` or nothing").
To solve this error, we can use _type narrowing_:

```ts
const player = entity.ToPlayer();
if (player === undefined) {
  error("Failed to convert the entity to a player.");
}
player.AddMaxHearts(2); // The type of player is now narrowed to "EntityPlayer".
```

Here, we explicitly handle the error case and supply a helpful error message.
But this code does something more important than simply providing the error
message.

`error` is a Lua function that causes execution of the function to immediately
end. Thus, TypeScript is smart enough to realize that if the code gets to the
`AddMaxHearts` line, the type of `player` is no longer
`EntityPlayer | undefined` - it would have to be a `EntityPlayer`. You can
confirm this by mousing over the variable in VS Code.

Since many of the Isaac API methods can fail, you will have to use _type
narrowing_ like this in many places in your code. Sometimes, it can be annoying
to explicitly check to see if things go wrong. But _type narrowing_ should be
seen as a good thing: by handling errors in a sane way, you safely
compartmentalize the damage that run-time errors can cause. And when things do
go wrong, troubleshooting what happened becomes a lot easier.

================================================================================
// File: packages/docs/content/main/mod-feature.md
================================================================================
---
title: Using Feature Classes - The Modern Way to Write Isaac Mods
---

## The Problem

As your mod grows bigger, organization becomes more important: nobody wants to
work in a pigsty.

Most people already understand the basics: split code up into separate files.
For example, it makes sense for a mod pack that contains 10 items to have all of
the code for each individual item live in a file dedicated to just that item.
That way, you can leverage the `Ctrl + p` hotkey in VS Code to jump to the exact
spot that you need to go. And if you need to fix a bug with item 1, then you
don't have to go on a scavenger hunt throughout the entire repository - you can
just focus all of your attention on the file called "item1.ts".

But beyond the basics of "split code up into separate files", things get more
tricky. What is the best way to organize a big Isaac mod with lots of features?
(In this context, a "feature" refers to a new item, a new enemy, and so on.)

<br />

## The Benefits of Feature Classes

Historically, Isaac mods have subscribed feature functions to callbacks directly
in the same file, and then imported the feature files from the main file.
However, importing files for side effects like this can lead to spaghetti code.
So, other mods unify callback logic into a single file per callback, and then
have the callback files call the individual feature functions. Both of these mod
organization strategies have pros and cons.

In 2022, the IsaacScript community discovered a powerful new pattern for writing
Isaac mods: using TypeScript classes to represent individual mod features. This
pattern is extremely powerful for a few reasons:

1. It allows you to use method decorators to subscribe individual class methods
   to callbacks. This allows you to get rid of callback files that "glue"
   together your "main.ts" file and your individual feature files.
1. Method decorators allow you to colocate the originating callback declaration
   alongside the actual code that is being executed. This makes the execution
   path much easier to read and understand.
1. Classes allow you do provide conditional logic for decorated methods such
   that any callback will only fire if your logic passes. This allows you to
   very easily turn off individual mod features via e.g. Mod Config Menu or Dead
   Sea Scrolls.
1. Classes can be extended from parent classes, allowing you to unify
   initialization logic by writing it in the parent class constructor (e.g.
   `MyNPC1` extends `MyNPCFeatures` extends `ModFeature`).
1. Classes can subscribe and unsubscribe from callbacks when arbitrary
   conditions are met. This can be useful if your callback functions are
   expensive.
1. Classes automatically subscribe to the
   [save data manager](/isaacscript-common/classes/features/other/savedatamanager/),
   which reduces boilerplate.

In short, feature classes are a powerful abstraction that allows you to write
concise, easy-to-read code. They also provide a great deal of flexibility and
control.

<br />

## Example

Let's start with a quick example to showcase the power of the feature class
pattern. We will be creating an item called the Green Candle. We won't fully
implement the item; we just want you to get the idea of how the pattern works.

First off, we create a mod and upgrade it so that we can use features with the
standard library:

```ts
// mod.ts

import { ISCFeature, upgradeMod } from "isaacscript-common";

const ISC_FEATURES_FOR_THIS_MOD = [ISCFeature.SAVE_DATA_MANAGER] as const;

const modVanilla = RegisterMod("Green Candle", 1);
export const mod = upgradeMod(modVanilla, ISC_FEATURES_FOR_THIS_MOD);
```

This part is pretty standard practice for all IsaacScript mods.

Next, we define a class that will contain the logic for the Green Candle
feature:

```ts
// features/GreenCandle.ts

import { ModCallback } from "isaac-typescript-definitions";
import { Callback, DefaultMap, ModFeature } from "isaacscript-common";

// We create a typical "v" object to hold our variables for this feature. (Hopefully at this point
// you have already written an IsaacScript mod and are familiar with the save data manager. If not,
// that's okay; the the takeaway here is that "v" objects have special meaning.)
const v = {
  room: {
    countersMap: new DefaultMap<PtrHash, int>(0),
  },
};

// Mod classes should extend from the `ModFeature` class. This allows their methods to be decorated
// by the `@Callback` and `@CallbackCustom` decorator functions.
export class GreenCandle extends ModFeature {
  // Whatever we specify as the class member of `v` will automatically be registered with the save
  // data manager. Note that we could also declare `v` entirely inside the class, but it is
  // conventional to do it this way so that we can type `v.room.countersMap` instead of
  // `this.v.room.countersMap`.
  v = v;

  // By putting `@Callback` before a method, it decorates that method, which runs special logic
  // upon class instantiation. In this case, it subscribes to the specified callback. Note that
  // similar to a "real" callback registration, you could also provide an additional argument here
  // to make the class method only fire for a specific kind of NPC.
  @Callback(ModCallback.POST_NPC_UPDATE)
  postNPCUpdate(npc: EntityNPC): void {
    // The following code is just to show off getting a counter from our `v` object; it does not
    // have to do with the class pattern specifically. Most of your mod features will probably use
    // the save data manager in a way similar to this, but they don't necessarily have to.
    const ptrHash = GetPtrHash(npc);
    const counters = v.room.countersMap.getAndSetDefault(ptrHash);
    const newCounters = counters + 1;
    v.room.countersMap.set(ptrHash, newCounters);

    // TODO: Do something with `newCounters`.
  }
}
```

Now, we can instantiate our mod feature classes in our "main.ts" file by using
the `initModFeatures` helper function:

```ts
// main.ts

import { initModFeatures } from "isaacscript-common";
import { GreenCandle } from "./features/GreenCandle";
import { mod } from "./mod";

const MOD_FEATURES = [GreenCandle] as const;

initModFeatures(mod, MOD_FEATURES);
```

That's it! The code in our Green Candle class will now automatically run
whenever an NPC is present.

As our mod gets bigger, we can add more classes to the `MOD_FEATURES` array. We
could also create an intermediary class if two or more mod features will have
shared logic (e.g. `GreenCandle extends CollectibleModFeature` +
`CollectibleModFeature extends ModFeature`).

<br />

## Other `ModFeature` Features

More advanced features of the `ModFeature` class are listed below.

### Decorators

In addition to `@Callback`, you can also use `@CallbackCustom` to register class
methods with custom callbacks from the standard library. You can also use
`@PriorityCallback` and `@PriorityCallbackCustom` to make a certain method run
before or after other registered callbacks.

### Using `shouldCallbackMethodsFire` For Conditional Firing

If you want the decorated methods of a class to conditionally fire, then specify
a function for the `shouldCallbackMethodsFire` property. For example:

```ts
export class GreenCandle extends ModFeature {
  protected override shouldCallbackMethodsFire = (): boolean => {
    // We don't need to track anything if no players have the collectible.
    return anyPlayerHasCollectible(CollectibleTypeCustom.GREEN_CANDLE);
  };

  // [The rest of the class logic goes here.]
}
```

### Delayed Initialization

We recommend that you use the `initModFeatures` helper function to instantiate
your mod features. That way, the `v` variables will be properly registered with
the save data manager.

By default, when a `ModFeature` is instantiated, it will immediately subscribe
all of the decorated methods. If you want to defer the callback subscription for
some reason, then you can manually instantiate your mod features by passing
`false` to the third argument of the constructor like this:

```ts
const instantiatedModFeatures = initModFeatures(mod, modFeatures, false);
```

Now, `instantiatedModFeatures` will contain an array of the instantiated feature
classes, but none of the callbacks will be subscribed and the variables will not
be registered with the save data manager. Later on, when you actually need to
use a class, you can initialize it with the `init` method:

```ts
const firstInstantiatedModFeature = instantiatedModFeatures[0];
if (firstInstantiatedModFeature === undefined) {
  error("Failed to get the first instantiated mod feature.");
}

firstInstantiatedModFeature.init();
```

================================================================================
// File: packages/docs/content/main/next-steps.md
================================================================================
---
title: Next Steps
---

If you just finished the [Green Candle tutorial](/main/example-mod/), you may be
wondering about the next steps you should take.

<br />

## Skill Level

What to do next probably depends on your skill level.

<br />

### Intermediate & Advanced Programmers

For intermediate to advanced programmers, the Green Candle tutorial should be
enough for you to understand the anatomy of an Isaac mod. From here, you can use
the [API reference documentation](https://wofsauge.github.io/IsaacDocs/rep/) and
the [IsaacScript standard library documentation](/isaacscript-common/) to go
forth and build whatever it is you want to build, using
[the appropriate callbacks](https://wofsauge.github.io/IsaacDocs/rep/enums/ModCallbacks.html).

<br />

### Experienced Isaac Modders

For people who already have experience in Isaac modding in Lua, the
[Green Candle tutorial](/main/example-mod/) should be enough to get you familiar
with how exactly IsaacScript mods are different from Lua mods. And the
[JavaScript tutorial](/main/javascript-tutorial/) should be enough to get you
familiar with the syntax differences between the two languages. (Overall, they
are pretty similar.)

If you already know how the Isaac API works, then you are in a good spot,
because the API works exactly the same way in IsaacScript as it does with Lua.
The only code differences will be cosmetic; use curly brackets instead of
"then", and so on. At this point, you should be ready to go forth and build
whatever it is you want to build.

<br />

### Novice Programmers

Novice programmers or people without any previous Isaac modding experience might
not be "off to the races" after finishing the Green Candle tutorial. If you look
through the
[API reference documentation](https://wofsauge.github.io/IsaacDocs/rep/) and you
feel completely lost about how to start doing what you want to do, then you
probably fall into this camp.

One option for beginners is to watch the
[Catinsurance video tutorial series on YouTube](https://www.youtube.com/playlist?list=PLkIbky8_pFUpqAF9l7dh_YsEV-zpJ4q50).
As you can see, the videos cover a lot of different topics, so watching a few of
these videos should give you a nice overview of the kinds of things that are
possible, and you can follow along step by step so that you can learn how to do
it.

Note that Catinsurance's videos are made for Lua, and in general, you probably
won't find any IsaacScript-specific tutorials in the wild. But remember that the
API is completely identical between Lua and TypeScript - the only difference is
the language. In other words, you only have to worry about cosmetic things like
using curly brackets instead of "then", using parenthesis around if statements,
adding type annotations, and so on.

To give you an idea of what I mean, here is a `setBlindfold` function in both
TypeScript and Lua:

```ts
// TypeScript code
function setBlindfold(player: EntityPlayer, enabled: boolean) {
  const character = player.GetPlayerType();
  const challenge = Isaac.GetChallenge();

  if (enabled) {
    game.Challenge = 6; // A challenge with a blindfold.
    player.ChangePlayerType(character);
    game.Challenge = challenge;
    player.TryRemoveNullCostume(14);
  } else {
    game.Challenge = 0;
    player.ChangePlayerType(character);
    game.Challenge = challenge;
    player.TryRemoveNullCostume(14);
  }
}
```

```lua
-- Lua code
local function setBlindfold(player, enabled)
  local character = player:GetPlayerType();
  local challenge = Isaac.GetChallenge();

  if enabled then
    game.Challenge = 6; -- A challenge with a blindfold.
    player:ChangePlayerType(character);
    game.Challenge = challenge;
    player:TryRemoveNullCostume(14);
  else
    game.Challenge = 0;
    player:ChangePlayerType(character);
    game.Challenge = challenge;
    player:TryRemoveNullCostume(14);
  }
end
```

As you can see, besides some shenanigans with Lua using colons, and having to
include the types inside of the function declaration, the code is almost
identical. For this reason, you can pretty easily use any Isaac modding tutorial
that is made for Lua and then apply it in IsaacScript. Coding in IsaacScript has
the advantage of type safety - you get a red squiggly line in your editor when
you make a typo.

With that said, if you are brand new to coding, you might want to make things
easier on yourself by switching to Lua. That way, you can follow along exactly
with what the tutorial is doing without having to worry about converting code
back and forth between Lua and TypeScript. You can always come back to
TypeScript later on once you have a better grasp on modding in Lua.

It you feel shaky on the act of programming itself, that is more of something
that you learn over time with lots of practice. I personally prefer to learn by
doing, but there are plenty of coding tutorials that you can do online, such as
[Code Academy](https://www.codecademy.com/).

<br />

## Example Mods

Sometimes, studying other people's code can also be helpful. If you want a
real-life project to look at, you can take a look at
[Racing+](https://github.com/Zamiell/racing-plus), which is one of the biggest
Isaac mods in existence. Or, if you want to focus on a smaller project, take a
look through the `#mod-showcase` channel of
[the Discord server](/main/discord/), of which there are many to pick from.

Remember that because Lua is so similar to TypeScript, you can also download any
popular mod from the Steam Workshop and then directly read the Lua code that it
comes with in order to see how they are accomplishing things. (But be aware that
in general, the code quality of Lua mods is usually pretty low.)

<br />

## Discord

The IsaacScript community can help you with any questions that you have. Use the
`#help-and-questions` channel of [the Discord server](/main/discord/).

================================================================================
// File: packages/docs/content/main/publishing-to-the-workshop.md
================================================================================
---
title: Publishing to the Workshop
---

Isaac mods are published to the
[Steam Workshop](https://steamcommunity.com/app/250900/workshop/), which allows
others to easily download them. This is accomplished by running the
"ModUploader.exe" tool provided with the game, which is located at
`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\tools\ModUploader.exe`.

However, for large mods, there are often other tasks that need to be performed
before pushing the files to the Steam Workshop. `isaacscript` contains a
`publish` command that may be useful to you. It will perform the following
steps:

- Update all npm dependencies (e.g. in the "package.json" file).
- Bump the version in the "src/constants.ts" file (if it exists).
  - It looks for a line that looks something like:
    `export const VERSION = "v1.0.0";`
- Bump the version in the "mod/metadata.xml" file.
- Bump the version in the "mod/version.txt" file.
- Compile the TypeScript.
- Run the Python script located at "scripts/publish_pre_copy.py" (if it exists).
- Copy everything from the source mod directory to the destination mod directory
  (i.e. "project/mod" --> "mods/project").
- Run the Python script located at "scripts/publish_post_copy.py" (if it
  exists).
- Commit all changes in Git and push.

Run `npx isaacscript publish --help` to see additional flags that may be passed
to the `publish` command.

Additionally, we recommend that you set up
[automatic mod uploading in CI](https://github.com/IsaacScript/isaac-steam-workshop-upload).

================================================================================
// File: packages/docs/content/main/right-for-me.md
================================================================================
---
title: Is IsaacScript Right for Me?
---

(If you don't know what IsaacScript is, first see the
[features](/main/features/) page.)

Coding in TypeScript is a bit more involved than coding in Lua, since it
requires more tooling to be installed. This means that `isaacscript` isn't right
for everyone. Whether you should use the framework depends on several factors.

### Are you good with computers? Have you programmed anything before?

- No - ❌ - `isaacscript` is a command-line program. If you don't know what that
  is, then this is not the right tool for you.
- Yes - ✔️ - Using IsaacScript is as simple as using any other compiler.

### How much time are you spending on coding Isaac mods?

- Not a lot of time - ❌ - Code quick mods in Lua and move on with your life.
- A lot of time - ✔️ - Using `isaacscript` will save you a lot of time:
  - Automatic formatting and tab-complete makes typing up mod code twice as
    fast.
  - With automatic in-game loading, testing your mods is lightning fast.
  - You will waste less time running-around in-game debugging run-time errors.

### What is the size of the mod you are building?

- A tiny mod - ❌ - Tiny mods are less likely to have bugs or typos.
- A medium mod - ✔️ - If your mod is big enough to be split into two or more
  files, then using `isaacscript` will be helpful. And if you will update the
  mod in the future (with new features or bug fixes), then using `isaacscript`
  will help you maintain the project.
- A big mod - ✔️ - `isaacscript` allows you to glue everything together in a
  provably-correct way.

### How good at you at coding?

- Never coded before - ❌ - IsaacScript is not for you. Spend a few months
  learning to code, and then come back here.
- Beginner - ❔ - Since using IsaacScript can make things more complicated,
  beginners might want to follow KISS - Keep It Simple, Stupid. On the other
  hand, beginners often waste an enormous amount of time troubleshooting typos
  and other small errors. The TypeScript compiler is like a helpful friend that
  looks out for you, pointing out all of these small errors automatically.
- Intermediate - ✔️ - `isaacscript` helps you focus on _coding_. Spend less time
  referencing the API docs and less time dealing with run-time errors.
- Expert - ✔️ - You probably already know how invaluable type-safety is. Enjoy
  the power of TypeScript's generics and higher-level patterns to write bug-free
  and easy-to-read code.

### Do you have experience in TypeScript?

- Yes, I know TypeScript - ✔️ - The choice is obvious.
- No, but I know JavaScript - ✔️ - TypeScript is almost the same thing as
  JavaScript. (It is a "superset" language.)
- No, but I know Lua - ❔ - On one hand, if you already know Lua and are
  comfortable with it, then it might not be worth the time and effort to learn
  something new. On the other hand, once you've learned one language, learning
  another is pretty easy. It is **totally worth it** to spend an hour or two to
  learn TypeScript in order to get all of the other fantastic benefits that it
  provides over Lua.
- No, but I know some other language - ✔️ - Isaac mods are programmed in either
  TypeScript or Lua. If you don't know either, then start with TypeScript from
  the get-go. You'll thank me later.

================================================================================
// File: packages/docs/content/main/updating-isaacscript.md
================================================================================
---
title: Updating IsaacScript
---

IsaacScript is occasionally updated with new TypeScript definitions, new helper
functions, new linting rules, and so on. However, these new updates are not
automatically pushed to your mod.

In a TypeScript project, you can see your project dependencies and their current
versions by looking at the `package.json` file. More information can be found in
the [package.json documentation](/main/directory-structure/#packagejson). You
can upgrade the dependencies in your IsaacScript mod in the same way that you
would upgrade the dependencies for any other TypeScript program.
<!-- cspell:ignore packagejson -->

As a convenience, the `isaacscript` program itself can update dependencies like
this:

```sh
npx isaacscript update
```

This will automatically update the versions in your `package.json` file and tell
the package manager to install the new versions, if necessary.

If you don't want to use `isaacscript`, then you could run the
[`npm-check-updates`](https://www.npmjs.com/package/npm-check-updates) tool
directly with something along the lines of:

```sh
npx npm-check-updates --upgrade
```

Or, if you don't want to use the `npm-check-updates` tool, you can just manually
change the versions in your `package.json` file yourself. For more information,
check out
[this blog](https://www.netwoven.com/2017/03/21/how-to-update-node-js-modules-to-latest-versions/),
which goes over this process in more detail.

The latest version of the IsaacScript tool can always be found
[on the npm page](https://www.npmjs.com/package/isaacscript) or in
[the monorepo readme](https://github.com/IsaacScript/isaacscript/blob/main/README.md).

================================================================================
// File: packages/docs/content/main/using-get-data.md
================================================================================
---
title: Using Entity.GetData and the Save Data Manager
---

A common task in Isaac mods is to make new enemies, new familiars, and so on.
All of these things are grouped under the umbrella of the `Entity` class. Custom
entities often have some state associated with them. For example, you might have
a custom familiar that eats bombs. In this case, you would need to keep track of
how many bombs it has eaten already.

Additionally, a common task in modding is to make new functionality for vanilla
entities. For example, you might want to make a custom collectible that inflicts
sleep counters on all NPCs. In this case, you would need to keep track of a
sleep counter for every NPC.

These are just two examples. Regardless of the specific thing that you need to
do, if you need to store data about an entity, then you have a few different
options.

<br />

## Using `Entity.GetData`

There is a helpful method on the `Entity` class called `GetData`. It returns a
table that allows you to store arbitrary key/value pairs. Since the data is
attached to the `Entity` class, it can be easily retrieved from any callback.

Unfortunately, `GetData` has many downsides, but we will get to that later.

To start with, the return type of `GetData` is `Record<string, unknown>`, which
is essentially untyped. The first thing you will want to do is define the
structure of the data that you will be storing on the entity. This is done by
declaring an
[interface](https://www.typescriptlang.org/docs/handbook/2/objects.html).

For example, say that we want to store sleep counters on an entity. And when the
counter reaches a certain value, then the enemy will fall asleep.

```ts
interface FooData {
  sleepCounters: int | undefined;
}
```

Here, the `|` symbol creates a
[type union](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#union-types).
In other words, the type is "an integer or undefined". (It can't just be an
integer because prior to us initializing it with a value, it won't exist at
all.)

Once the interface is declared, we can use a type assertion to make retrieving
the counters type safe:

```ts
const data = entity.GetData() as FooData;
print(`Sleep counters: ${data.sleepCounters}`); // Auto-completes and is type safe!
if (data.sleepCounters === undefined) {
  // Initialize the sleep counters to an initial value.
  data.sleepCounters = 0;
}

// Do something with the sleep counters.
```

<br />

## Downsides of `Entity.GetData`

### It's a Global Variable

The `GetData` table is a global variable, meaning that all mods share the same
table. Thus, there can be conflicts, and other mods can modify or destroy your
data. Carefully namespacing your variable names can mitigate this problem, but
it's still not a good solution if you want your mod to be perfect.

### It's Ephemeral

The table is ephemeral, meaning that when the entity despawns, the table will be
deleted and you will lose your data.

For example, pickups are a type of entity that appear to be persistent: when you
get a heart drop in one room, you can backtrack to that room later, and the
heart drop will still be there. However, behind the scenes, what is really
happening is that the heart drop is despawned when you leave the room, and then
a brand-new heart pickup entity is respawned when you re-enter the room. In this
situation, if you had previously stored data on the `GetData` table of the heart
pickup, the brand-new entity would not have this same data.

### It's _Really_ Ephemeral

Even for real persistent entities like players and familiars, the table is still
ephemeral. For example, a familiar is never despawned; the same entity continues
to exist as the player moves from room to room. Thus, the problem in the
previous section would not apply to data stored in the `GetData` table for a
familiar. However, once the player saves and quits and continues, the familiar
will also be despawned in the exact same way that the heart drop was, and all of
the data will be lost. Saving and quitting and continuing is a common thing for
players to do (so that they can finish the run at a later time), so any
well-designed mod must be able to handle this case.

<br />

## Using Local Variables Instead

Using the IsaacScript save data manager, it's relatively easy to replace
`Entity.GetData` variables with a standard object. Let's use the same example as
before: we store sleep counters for every NPC in the room, and once they get
enough counters, they fall asleep.

### Save Data Manager Setup

First, before we declare our sleep counter variables, we need to upgrade our mod
with the save data manager feature:

```ts
// mod.ts
import { upgradeMod } from "isaacscript-common";

const modVanilla = RegisterMod("my-mod", 1);
const features = [ISCFeature.SAVE_DATA_MANAGER] as const;
export const mod = upgradeMod(modVanilla, features);
```

Now, the `mod` object can be imported by the feature files in our project. (If
this part is confusing, you might want to first look at
[the documentation for `isaacscript-common`](/isaacscript-common).)

### Data Definition

Since we just need to store sleep counters, we could use the exact same
interface as the previous example, and it would work just fine. But here, it
makes sense to use a class, because we can leverage the constructor to
initialize default values without having to manually write any custom code. (All
NPCs should start with 0 counters to begin with.)

```ts
class FooData {
  sleepCounters = 0;
}
```

And when we need to initialize the data, we can simply do: `new FooData()`

### Local Variables

Next, we need to define a local object to store our variables for the entity,
and then feed it to the save data manager:

```ts
const v = {
  room: {
    fooData: new Map<PtrHash, FooData>(),
  },
};

mod.saveDataManager("foo", v);
```

Let's break this down.

The object name of `v` is conventionally used to denote "variables", or more
specifically, "variables that are local to this file or feature only". We would
stick every variable that we need for this sleep feature on the `v` object. (And
we would not put any other variables on it, to keep the variables scoped
properly.)

`v` is composed of sub-objects. By specifying a `room` sub-object, that tells
the save data manager to automatically wipe the data in that sub-object when a
new room is entered. This is what we want, because in this example, enemy NPCs
will only exist in the context of the current room, and we don't care about
keeping data for NPCs that have already despawned.

Finally, inside of the `room` sub-object, we define the `fooData` map. (If you
don't know what a `Map` is, read the
[JavaScript/TypeScript tutorial](/main/javascript-tutorial/#maps), as
understanding maps is essential for this section.) The `fooData` map is
two-dimensional in that it will contain the data for every NPC in the room.

So, we need a way to identify each NPC in the room, and then use this identifier
as the index in our map. The solution is to use the pointer hash, which a unique
string that can be retrieved with the global function `GetPtrHash`:

```ts
const ptrHash = GetPtrHash(entity);
```

Imagine that we are in the `POST_ENTITY_DMG` callback, and an NPC has just
gotten hit by the player's tear. So now, we want to increment the number of
sleep counters:

```ts
function incrementSleepCounter(npc: EntityNPC) {}
  const ptrHash = GetPtrHash(npc);
  let data = v.run.fooData.get(ptrHash);
  if (data === undefined) {
    data = new FooData();
    v.run.fooData.set(data);
  }

  data.sleepCounters += 1;
}
```

That's about all there is to it. Here, the `FooData` class corresponds to the
old `GetData` table. You can add as many variables to the class as you need.

### `DefaultMap`

The previous example is a very common pattern in Isaac modding. The IsaacScript
standard library offers a data structure called a `DefaultMap` that can simplify
this pattern even further. A `DefaultMap` allows you to specify a default value
for things in the map. Subsequently, you don't have to worry about checking for
the case where the data doesn't exist yet, because the `DefaultMap`
automatically instantiates it for you.

```ts
const v = {
  room: {
    fooData: new DefaultMap<PtrHash, FooData>(() => new FooData()),
  },
};

function incrementSleepCounter(npc: EntityNPC) {}
  const ptrHash = GetPtrHash(npc);
  const data = v.run.fooData.getAndSetDefault(ptrHash);
  data.sleepCounters += 1;
}
```

Let's break this down.

You specify the default value of the map with the first argument of the
constructor. The first argument can either be a raw value, like 0. Or, it can be
a function that dynamically calculates/creates a value. Here, we pass a very
simple function that just instantiates a new class.

In the `incrementSleepCounter` function, we use the `getAndSetDefault` method
instead of the `get` method. If the monster already exists in the map, then the
`getAndSetDefault` will do the same thing as the `get` method. If the monster
does not exist yet in the map, the `DefaultMap` will run the function we
provided and give us the new data.

Using the `DefaultMap` data structure allows us to write really compact and
easy-to-read code!

<br />

## Tracking Other Kinds of Entities

In the previous example, we used the save data manager to track data about
entities that only exist in the context of a single room. However, mods will
also commonly want to store data about players. Players exist for an entire run,
not just a single room. This means that a slightly different approach is
necessary.

For this case, instead of using `GetPtrHash`, you can use `getPlayerIndex`. (The
corresponding type is `PlayerIndex`.)

So, for example, you might have a `v` that looks something like this:

```ts
const v = {
  run: {
    playerCounters: new DefaultMap<PlayerIndex, int>(0),
  },
};
```

For pickups, use `getPickupIndex`. (The corresponding type is `PickupIndex`.)

For familiars (and Dark Esau), use the `Entity.InitSeed`. (The corresponding
type is `Seed`.)

## Saving and Continuing

A huge benefit of using the save data manager is that any variables you create
will be automatically saved to disk if the player decides to save and quit the
run.

In the first example above, we were adding sleep counters to enemy NPCs. For
this case, the save data manager wouldn't actually save anything, because
nothing in `room` sub-object needs to be permanently saved. (Since the player
reloads the room when continuing the game, the `room` object is flushed in the
same way that it is flushed when the player enters a new room normally. For this
reason, saving any of the `room` values would be superfluous.)

In the second example above, we were tracking counters on players. For this
case, since players exist over the course of the entire run, the save data
manager would automatically save everything without you having to worry about
anything at all! (This is magic that would take around a thousand of lines of
code to write yourself.)

## Storing Other Variables

The point of this article is to showcase how you can use a local object to store
data about an entity as an alternative to using `GetData`. But note that in
IsaacScript mods, using `v` is the typical way to store data about anything, not
just entities. Your `v` object will contain all the variables needed to make
your feature work. So using the `v` pattern is very powerful.

================================================================================
// File: packages/docs/content/main/what-is-isaacscript-doing.md
================================================================================
---
title: What is IsaacScript Doing?
---

The `isaacscript` program will run forever until you close the terminal window
or cancel it with `Ctrl + c`. While it runs, it monitors for changes in your
project. In summary, it will:

1. automatically recompile your TypeScript as soon as you save a `.ts` file
1. automatically copy over any files in the `mod` directory
1. automatically refresh your mod in-game (with the `luamod` console command)

As a new user, you might want to confirm that each of these functions is working
properly as a way to get familiar with the program.

<br />

### 🔄 Confirm That Auto-Mod-Reloading Works

The moment that you save a TypeScript file, `isaacscript` will detect that
something has changed, and it will automatically perform the following steps:

- `isaacscript` will re-compile your TypeScript project using `tstl`, the
  TypeScriptToLua tool.
- `tstl` will spit out a file called `main.lua` in your project's `mod` folder.
  (e.g. `C:\Repositories\revelations\mod\main.lua`)
- `isaacscript` will copy this file to the `mods` directory. (e.g.
  `C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\mods\revelations\main.lua`)
- If you have the game open and are in a run, `isaacscript` will then send a
  message to a helper mod called `isaacscript-watcher`.
- `isaacscript-watcher` will run the `luamod` console command corresponding to
  your project. (e.g. `luamod revelations`)
- After the `luamod` command is executed, your mod has been reloaded - it is now
  ready to test!
- If compilation failed for any reason, then you will be able to see the errors
  on both the `isaacscript` console window and in-game. (The
  `isaacscript-watcher` mod will draw it on the screen for you.)

Note that `isaacscript` will automatically install the `isaacscript-watcher`
helper mod for you, so you don't have to do anything. Just test to see that it
works:

1. Make sure that `isaacscript` is running in a shell, monitoring for changes in
   your project.
1. In-game, go into a run.
1. In VS Code, add something new to your `main.ts` file, like:
   `print("hello world");`
1. In VS Code, save the file.
1. In game, you should see text appear on the screen. (i.e. Something along the
   lines of "Compilation successful.")
1. In game, press <code>`</code> to open the console and see if your "hello
   world" message is printed there.

<br />

### 📁 Confirm That File Cloning Works

`isaacscript` will automatically sync the contents of the `mod` directory in
your project to the corresponding folder in `mods`.

For example:

- Say that you have a project directory of: `C:\Repositories\revelations\`
- Then, inside your project mod folder, you make some new subdirectories:
  `C:\Repositories\revelations\mod\resources\gfx\items\collectibles\`
  - (This is the directory that you are supposed to put graphics files in for
    new modded items.)
- Next, you put a new file in that directory:
  `C:\Repositories\revelations\mod\resources\gfx\items\collectibles\collectibles_new_item.png`
- Now, `isaacscript` automatically copies the `collectibles_new_item.png` file
  to:
  `C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\mods\revelations\resources\gfx\items\collectibles\collectibles_new_item.png`

For now, just put something in your mod folder and confirm that `isaacscript`
copies it over for you.

Remember that if you add non-code assets to your mod, you have to fully restart
the game in order for the game to start using them.

<br />

