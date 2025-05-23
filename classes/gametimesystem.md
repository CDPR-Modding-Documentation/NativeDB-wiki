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

# gameTimeSystem

## Description

Use with everything time-based:

* real time
* time in V's storyline
* REDengine simulation time
* time dilation (e.g. when activating Sandevistan)

You can convert real-time to/from game-time with the table below (or use \[this.RealTimeSecondsToGameTime]):

* `GameTime` to `RealTime`
* `24:00:00.000` to `03:00:00.000`
* `00:08:00.000` to `00:01:00.000`
* `00:01:00.000` to `00:00:07.500`

## Functions

#### GetGameTime() -> GameTime

Time elapsed in V's storyline.

#### GetGameTimeStamp() -> Float

Real time, as a [timestamp epoch](https://www.epochconverter.com/).

#### GetSimTime() -> EngineTime

REDengine simulation time.

#### IsTimeDilationActive(opt reason: CName) -> Bool

Whether V or NPCs are currently using time dilation (usually via cyberware, e.g. Sandevistan).

#### RealTimeSecondsToGameTime(seconds: Float) -> GameTime

Convert from real-time seconds to game time.
