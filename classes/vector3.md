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

# Vector3

## Description

3D coordinates with floating point precision.

## Functions

#### Lerp(a: Vector3, b: Vector3, t: Float) -> Vector3

Linearly compute an intermediate position between `a` and `b`.

`t` is a factor between 0.0 and 1.0 (0.0 returns `a` while 1.0 returns `b`).
