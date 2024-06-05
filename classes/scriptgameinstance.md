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

Main entry-point to get systems for gameplay / environment / etc. It can be obtained using global function \[GetGameInstance].

## Functions

#### GetDelaySystem(self: ScriptGameInstance) -> handle:gameDelaySystem

Get system used to execute callback functions after a delay. It runs functions asynchronously in game loop.

#### GetTelemetrySystem(self: ScriptGameInstance) -> handle:gameTelemetryTelemetrySystem

CDPR only.

#### GetTeleportationFacility(self: ScriptGameInstance) -> handle:gameTeleportationFacility

Get system used to teleport a \[GameObject] to \[Vector4] coordinates or to a \[NodeRef].

#### GetTimeSystem(self: ScriptGameInstance) -> handle:gameTimeSystem

Get system used to change game time, including time dilation.

#### GetVehicleSystem(self: ScriptGameInstance) -> handle:gameVehicleSystem

Get system used to summon vehicles and unlock vehicles in player's garage.

See also \[VehicleObject], \[VehicleComponent] and \[vehicleController] to access more vehicle behaviours.
