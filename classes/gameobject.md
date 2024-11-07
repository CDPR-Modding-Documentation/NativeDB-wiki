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

# gameObject

## Description

A `GameObject` is any in-game item or structure that the player or NPCs can interact with. This includes things like weapons, doors, vending machines, lootable containers, and even some environmental elements.

## Functions

#### RegisterInputListener(listener: handle:IScriptable, opt name: CName) -> Void

`name` (of action) is allowed but using known object (e.g. \[PlayerPuppet]) as `listener` is a source of potential issues. Mods should always declare and use a custom listener object, like in [this example](https://discord.com/channels/717692382849663036/867332475553054740/888415535992291379).
