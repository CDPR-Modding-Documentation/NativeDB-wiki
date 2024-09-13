---
description: Allows to schedule callbacks, events or system requests in various ways.
---

# gameDelaySystem

## Functions

#### DelayCallback(delayCallback: handle:gameDelaySystemScriptedDelayCallbackWrapper, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

Note that callback is triggered only once, but nothing prevents from rescheduling it manually at your convenience.

* `timeToDelay` : delay duration in seconds.
* `isAffectedByTimeDilation`: whether callback will be slowed down based on current active time dilation (e.g. when time slows during e.g. Sandevistan).
