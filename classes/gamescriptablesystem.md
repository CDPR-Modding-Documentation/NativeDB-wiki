---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# gameScriptableSystem

## Description

Only available in-game, and re-created on each load.

See Codeware [ScriptableService](https://github.com/psiberx/cp2077-codeware/wiki#scriptable-services) if you need to add logic outside of game sessions.

## Functions

#### WasRestored() -> Bool

Whether session was restored (e.g. on save load), or not (e.g. on new game).

#### IsSavingLocked() -> Bool

Whether saving is currently disabled or not (e.g. during combat).

#### OnAttach() -> Void

Automatically called when attached to game session (e.g. on save load).

#### OnDetach() -> Void

Automatically called when detached from game session (e.g. on exit to main menu).

#### OnRestored(saveVersion: Int32, gameVersion: Int32) -> Void

Automatically called when restoring game session (e.g. on save load).
