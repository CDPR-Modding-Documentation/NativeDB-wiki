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

#### ActivateNetrunnerQuickhack(chooseHack: vehicleVehicleNetrunnerQuickhackType) -> Void

This is a paragraph with a reference to \[WeaponObject].

* an unordered
* list

1. an ordered
2. list

* [ ] a task
* [ ] list

***

{% hint style="info" %}
A hint
{% endhint %}

> Some quote

```swift
// Some Redscript code
public class Test {
  private let m_field: Int32;
}
```

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
