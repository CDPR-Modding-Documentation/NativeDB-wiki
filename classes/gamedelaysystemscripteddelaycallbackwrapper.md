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

# gameDelaySystemScriptedDelayCallbackWrapper

## Description

Allows creating custom callbacks to use in-game with \[DelaySystem].

If you're looking to trigger callbacks outside of game sessions, see [wiki of Codeware](https://github.com/psiberx/cp2077-codeware/wiki#custom-events) for custom events.

## Functions

#### Call() -> Void

Method which gets automatically called after delay, see \[DelayCallback] and \[DelaySystem.DelayCallbackNextFrame].
