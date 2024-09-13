# gameDelaySystem

## Description

Allows to schedule callbacks, events or system requests in various ways.

Note:

* callback is triggered only once, but nothing prevents from rescheduling it manually at your convenience.
* callback will not get triggered when set over a certain delay (like 1 or 3min), but nothing prevents from rescheduling while keeping track of how long has elapsed, with a timestamp (see [TimeSystem](https://nativedb.red4ext.com/gameTimeSystem#GetGameTimeStamp)).
* [DelayID](https://nativedb.red4ext.com/DelayID) can be kept around to interrupt a running callback, event or tick anytime (see `CancelDelay`, `CancelEvent` and `CancelTick`). You can also check how long remains before being eventually called (see `GetRemainingDelayTime`).

## Functions

#### DelayCallback(delayCallback: handle:gameDelaySystemScriptedDelayCallbackWrapper, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

* `timeToDelay` : delay duration in seconds.
* `isAffectedByTimeDilation`: whether callback will be slowed down based on current active time dilation (e.g. when time slows during e.g. Sandevistan).

More infos and code snippets [there](https://cyb3rpsych0s1s.github.io/4ddicted/patterns/callbacks.html).

#### DelayEvent(entity: whandle:entEntity, eventToDelay: handle:redEvent, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

Supports any class inheriting from [Event](https://nativedb.red4ext.com/Event), including custom ones.

More infos and code snippets [there](https://cyb3rpsych0s1s.github.io/4ddicted/patterns/events.html#delayed-events).

#### DelayScriptableSystemRequest(systemName: CName, requestToDelay: handle:gameScriptableSystemRequest, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

Use with [ScriptableSystemRequest](https://nativedb.red4ext.com/ScriptableSystemRequest).

#### GetRemainingDelayTime(delayID: gameDelayID) -> Float

How long remains before associated callback, event or tick gets called.

#### TickOnEvent(entity: whandle:entEntity, eventToTick: handle:gameTickableEvent, duration: Float) -> gameDelayID

More infos and code snippets [there](https://cyb3rpsych0s1s.github.io/4ddicted/patterns/events.html#tickable-events).

