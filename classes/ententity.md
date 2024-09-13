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

# entEntity

## Description

An `Entity` is essentially a "thing" in the game world. This can be a player character, NPC, vehicle, or an object like a weapon or a door. Each entity has specific attributes, like health, position, and abilities, that define how it behaves and interacts with the environment.

* Components: these are smaller parts that make up an entity, such as physics, animations, and behaviors. Components are what give an entity its abilities, like moving, interacting, or taking damage.
* Properties: these are data fields that define things like health, speed, size, or position in the world.
* Events: entities can send and receive events to trigger actions. For instance, an NPC can trigger an event when it detects the player.

## Functions

#### CanServiceEvent(evtName: CName) -> Bool

Whether \[this.QueueEvent] is currently available or not.

#### Dispose() -> Void

Mark entity for disposal.

#### FindComponentByName(componentName: CName) -> handle:entIComponent

Retrieve any component on entity by name.

#### GetCurrentAppearanceName() -> CName

Retrieve currently applied [appearance](https://wiki.redmodding.org/cyberpunk-2077-modding/for-mod-creators-theory/files-and-what-they-do/appearance-.app-files).

#### QueueEvent(evt: handle:redEvent) -> Void

Enqueue event for entity on game's events loop.
