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

# ScriptGameInstance

## Description

Main entry-point to get systems for gameplay / environment / etc.

You can get it using global function \[GetGameInstance]. When [Codeware](https://github.com/psiberx/cp2077-codeware/wiki) is installed, you can always use \[GetGameInstance] without issues. Otherwise, you may need to get \[GameInstance] through other functions like \[GameObject.GetGame] for example.

## Functions

#### GetAchievementSystem(self: ScriptGameInstance) -> handle:gameAchievementSystem

CDPR only.

#### GetDelaySystem(self: ScriptGameInstance) -> handle:gameDelaySystem

Get system used to execute callback functions after a delay. It runs functions asynchronously in game loop.

#### GetSimTime(self: ScriptGameInstance) -> EngineTime

Get elapsed time since the simulation started. Time is reset when navigating between menu and in-game scenes. Time is paused when game is paused (e.g. inventory menu is open).

#### GetTelemetrySystem(self: ScriptGameInstance) -> handle:gameTelemetryTelemetrySystem

CDPR only.

#### GetTeleportationFacility(self: ScriptGameInstance) -> handle:gameTeleportationFacility

Get system used to teleport a \[GameObject] to \[Vector4] coordinates or to a \[NodeRef].

#### GetTimeSystem(self: ScriptGameInstance) -> handle:gameTimeSystem

Get system used to change game time, including time dilation.

#### GetVehicleSystem(self: ScriptGameInstance) -> handle:gameVehicleSystem

Get system used to summon vehicles and unlock vehicles in V's garage.

See also \[VehicleObject], \[VehicleComponent] and \[vehicleController] to access more vehicle behaviours.
