# gameDelaySystem

## Description

Allows to schedule callbacks, events or system requests in various ways.

Note:

* callback is triggered only once, but nothing prevents from rescheduling it manually at your convenience.
* callback will not get triggered when set over a certain delay (like 1 or 3min), but nothing prevents from rescheduling while keeping track of how long has elapsed, with a timestamp (see [TimeSystem](https://nativedb.red4ext.com/gameTimeSystem#GetGameTimeStamp)).
* [DelayID](https://nativedb.red4ext.com/DelayID) can be kept around to interrupt a running callback, event or tick anytime (see `CancelDelay`, `CancelEvent` and `CancelTick`). You can also check how long remains before calling them (see `GetRemainingDelayTime`).

## Functions

#### DelayCallback(delayCallback: handle:gameDelaySystemScriptedDelayCallbackWrapper, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

* `timeToDelay` : delay duration in seconds.
* `isAffectedByTimeDilation`: whether callback will be slowed down based on current active time dilation (e.g. when time slows during e.g. Sandevistan).

#### DelayEvent(entity: whandle:entEntity, eventToDelay: handle:redEvent, timeToDelay: Float, opt isAffectedByTimeDilation: Bool) -> gameDelayID

Supports any `Event`, including custom ones.

e.g.

```swift
// You can also create your own custom event.
public class MyEvent extends Event {
  public let v: wref<PlayerPuppet>;
}

// Trigger event on game attached.
@wrapMethod(PlayerPuppet)
protected cb func OnGameAttached() -> Bool {
  wrappedMethod();
  if !this.IsReplacer() {
    let event: ref<MyEvent> = new MyEvent();
    event.v = this;
    GameInstance
      .GetDelaySystem(this.GetGame())
      .DelayEvent(this, event, 2.0, false);
      // 2.0 == 2 real life seconds. 1 min in-game is 10 real seconds.
  }
}

// Has to be added on owner's class: function signature matters!
@addMethod(PlayerPuppet)
protected cb func OnMyEvent(event: ref<MyEvent>) -> Void {
  FTLog(AsRef("Received MyEvent now!"));
}
```
