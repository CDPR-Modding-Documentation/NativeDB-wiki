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

# entIComponent

## Description

Components in the game define the functionality of various objects and NPCs, such as physics, animations, interactions, and more. `IComponent` serves as a base class for all the specific components that can be attached to entities.

* Modularity: components can be thought of as modules that add specific functionality to an entity. For example, you could add a physics component to give an object physical interactions with the environment or an AI component to allow an NPC to make decisions.
* Reuse: since components are reusable, you can apply the same component to different entities. This makes it easier to add consistent behavior across various objects or NPCs.
* Separation of Concerns: each component is responsible for handling a specific aspect of an entity. This makes it easier to focus on one feature at a time (such as movement, interaction, or combat behavior).

## Functions

#### GetEntity() -> whandle:entEntity

Retrieve entity owner.
