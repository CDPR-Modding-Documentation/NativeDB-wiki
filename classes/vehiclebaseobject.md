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

# vehicleBaseObject

## Description

Base class of a vehicle used for cars, bikes, tanks and AVs.

## Functions

#### GetActiveWeapons(out weaponList: array:whandle:gameweaponObject) -> Void

Parsing parameter's flags and nested types.

#### GetCurrentSpeed() -> Float

Always in km/h.

#### GetTotalMass() -> Float

Always in kg.

#### NotifyWindowChange(windowName: CName, isOpened: Bool) -> Void

`windowName` accepts the following known values:

* n"Left"
* n"Right"

#### SetDestructionGridPointValues(layer: Uint32, values: \[15]Float, accumulate: Bool) -> Void

Parsing static array with pseudo-code syntax...
