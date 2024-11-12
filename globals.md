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

# GLOBALS

#### GetGameInstance() -> ScriptGameInstance

When [Codeware](https://github.com/psiberx/cp2077-codeware/wiki) is installed, you can use this function without issues. Otherwise, you may need to get \[GameInstance] through other functions like \[GameObject.GetGame] for example.

This function will only work when the game engine is initialized, meaning a \[GameInstance] do exists.

#### FTLog(value: script\_ref:String) -> Void

Use this function to write in logs, along with \[FTLogWarning] and \[FTLogError].

See [wiki](https://wiki.redmodding.org/redscript/references-and-examples/logging) for more about logging.
