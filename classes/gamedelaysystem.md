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

# gameDelaySystem

## Description

Allows to schedule callbacks, events or system requests in various ways. Time / delay is expressed in seconds.

* callback is triggered only once, but nothing prevents from rescheduling it manually at your convenience.
* callback will not get triggered when set over a certain delay (like 1 or 3 minutes), but nothing prevents from rescheduling while keeping track of how long has elapsed, with a timestamp (see \[TimeSystem]).
* \[DelayID] can be kept around to interrupt a running callback, event or tick anytime (see \[this.CancelDelay], \[this.CancelEvent] and \[this.CancelTick]). You can also check how long remains before being eventually called (see \[this.GetRemainingDelayTime]).

## Functions

#### DelayCallback(delayCallback: handle:gameDelaySystemScriptedDelayCallbackWrapper, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

* `timeToDelay` : delay duration in seconds.
* `isAffectedByTimeDilation`: whether callback will be slowed down based on current active time dilation (e.g. when time slows during Sandevistan).

More info and code snippets [there](https://cyb3rpsych0s1s.github.io/4ddicted/patterns/callbacks.html).

#### DelayEvent(entity: whandle:entEntity, eventToDelay: handle:redEvent, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

Supports any class inheriting from \[Event], including custom ones.

More info and code snippets [there](https://cyb3rpsych0s1s.github.io/4ddicted/patterns/events.html#delayed-events).

#### GetRemainingDelayTime(delayID: gameDelayID) -> Float

How long remains before associated callback, event or tick gets called.

#### TickOnEvent(entity: whandle:entEntity, eventToTick: handle:gameTickableEvent, duration: Float) -> gameDelayID

More info and code snippets [there](https://cyb3rpsych0s1s.github.io/4ddicted/patterns/events.html#tickable-events).

