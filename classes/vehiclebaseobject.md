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

#### GetCurrentSpeed() -> Float

Always in km/h.

#### GetTotalMass() -> Float

Always in kg.

#### NotifyWindowChange(windowName: CName, isOpened: Bool) → Void

`windowName` accepts the following known values:

* n"Left"
* n"Right"
