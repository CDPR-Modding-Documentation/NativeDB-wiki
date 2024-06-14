---
description: >-
  This guide describes how documentation should be written. It also explains
  what should be documented or not, and why.
---

# Guidelines

## Introduction

The goal of this documentation is to share acquired knowledge about the codebase. It is not useful to document every single class and functions of this entire codebase.

{% hint style="success" %}
Guidelines below are not hard rules that you must absolutely and always follow. The purpose is to give you (and contributors) a common ground to start from.
{% endhint %}

## Explicit

One big rule is to add documentation when a class / a function is **not** explicit.

For example, the name of the class [PreventionSystem](https://nativedb.red4ext.com/PreventionSystem) is not clear for someone who only played the game. In this case it is useful to add a sentence describing that **Prevention** means NCPD / the police.

{% hint style="success" %}
**DO** add documentation to describe a behavior that is not already explicit.
{% endhint %}

{% hint style="danger" %}
**DON'T** add documentation about a class like [PlayerPuppet](https://nativedb.red4ext.com/PlayerPuppet), only to say "Class of the player".
{% endhint %}

{% hint style="danger" %}
**DON'T** add documentation about a function like [IsMoving](https://nativedb.red4ext.com/PlayerPuppet#IsMoving), only to say "Return true when player is moving, false otherwise".
{% endhint %}

## Avoid code

This documentation is not about showing how to use a snippet of code: be it in Redscript, Lua or else. In this spirit, writing code in the documentation should be avoided. If it is deemed really useful, it should be as short as possible.

{% hint style="success" %}
[Scripting Cyberpunk](https://app.gitbook.com/o/-MP5ijqI11FeeX7c8-N8/s/fwsaoju1TBAUvMpI6NIw/) is already present to share knowledge about the code and scripting in general. You should share your findings in this space, not in this documentation.
{% endhint %}

## Game vocabulary

More than often, people played the game and knows about the vocabulary it uses. It is preferable to use game's vocabulary to be on the same page.

For example, it is preferred to tell **Prevention** is about **NCPD**. This way, when you document other parts of the game related to Prevention, you can use the keyword **NCPD**. Others will understand what you're talking about.

As another example, you can write **V** when talking about the [PlayerPuppet](https://nativedb.red4ext.com/PlayerPuppet). It should be explicit for anyone, and is shorter to write than **the player**.

## List known data

A function might need some kind of predefined data as arguments. Think about the `CName` type, it is a string-like type but values are not listed like enums. We don't know about them. In this case, a modder will have to dig and search what values the function accepts as a `CName`.

If you know all or even only one valid value, you should list them when documenting the function. This way, others know what data to use when they need to call this function too.

If the list of values is very big, use a link instead to reference some Sheet-like document containing all known values.

If the list of values is accessible using WolvenKit, add a note about it and provide the path where to look for the data.

## CDPR only

In the codebase, you can find features that are not related to the gameplay, saves, the world, etc. For example, you should not care nor mess around with the [TelemetrySystem](https://nativedb.red4ext.com/ScriptGameInstance#GetTelemetrySystem).

In this case, you can add the comment "CDPR only". It is short and explicit enough to tell other modders:

> There is nothing to see for modding purpose.

## Conclusion

After reading this, you should better grasp what you can document and how. Don't hesitate to go through the current documentation. It can be helpful to see how other parts are already documented, to get more familiar with these guidelines.
