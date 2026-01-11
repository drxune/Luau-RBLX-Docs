# SwimController | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SwimController
Scraped: 2026-01-11T02:35:18.212118Z

## Inherits
- ControllerBase
- SwimController
- Instance
- Object
- ControllerBase.RigidityEnabled
- ControllerManager.BaseTurnSpeed
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ControllerBase](/docs/reference/engine/classes/ControllerBase)
6. /
7. [SwimController](/docs/reference/engine/classes/SwimController)

English

Feedback

Engine Class

![SwimController](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SwimController-Dark.webp)SwimController

---

Summary

Properties

|  |
| --- |
| [AccelerationTime](#AccelerationTime):[number](/docs/luau/numbers) |
| [PitchMaxTorque](#PitchMaxTorque):[number](/docs/luau/numbers) |
| [PitchSpeedFactor](#PitchSpeedFactor):[number](/docs/luau/numbers) |
| [RollMaxTorque](#RollMaxTorque):[number](/docs/luau/numbers) |
| [RollSpeedFactor](#RollSpeedFactor):[number](/docs/luau/numbers) |

Inherited Members

3 inherited from [ControllerBase](/docs/reference/engine/classes/ControllerBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Properties

AccelerationTime

Read Parallel

SwimController.AccelerationTime:[number](/docs/luau/numbers)

Provide feedback

---

PitchMaxTorque

Read Parallel

The maximum torque used to rotate to the desired pitch.

SwimController.PitchMaxTorque:[number](/docs/luau/numbers)

The maximum torque used to rotate on the local X axis to the desired
pitch orientation. Has no effect if [ControllerBase.RigidityEnabled](/docs/reference/engine/classes/ControllerBase#RigidityEnabled)
is true.

Provide feedback

---

PitchSpeedFactor

Read Parallel

Multiplied by [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed) to determine the
maximum angular velocity for pitch.

SwimController.PitchSpeedFactor:[number](/docs/luau/numbers)

Multiplied by [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed) to determine the
maximum angular velocity rotating on the local X axis. Has no effect
if [ControllerBase.RigidityEnabled](/docs/reference/engine/classes/ControllerBase#RigidityEnabled) is true.

Provide feedback

---

RollMaxTorque

Read Parallel

The maximum torque applied to rotate to the desired roll.

SwimController.RollMaxTorque:[number](/docs/luau/numbers)

The maximum torque applied to rotate on the local Z axis to the
desired roll orientation. Has no effect if
[ControllerBase.RigidityEnabled](/docs/reference/engine/classes/ControllerBase#RigidityEnabled) is true.

Provide feedback

---

RollSpeedFactor

Read Parallel

Multiplied by [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed) to determine the
maximum angular velocity for roll.

SwimController.RollSpeedFactor:[number](/docs/luau/numbers)

Multiplied by [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed) to determine the
maximum angular velocity rotating on the local Z axis. Has no effect
if [ControllerBase.RigidityEnabled](/docs/reference/engine/classes/ControllerBase#RigidityEnabled) is true.

Provide feedback

---