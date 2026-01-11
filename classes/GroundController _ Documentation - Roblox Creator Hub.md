# GroundController | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GroundController
Scraped: 2026-01-11T02:31:31.575663Z

## Inherits
- ControllerBase
- GroundController
- Instance
- Object
- ControllerManager.RootPart
- BalanceSpeed
- ControllerBase.BalanceRigidityEnabled
- BasePart.CustomPhysicalProperties
- ControllerManager.BaseTurnSpeed
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ControllerBase](/docs/reference/engine/classes/ControllerBase)
6. /
7. [GroundController](/docs/reference/engine/classes/GroundController)

English

Feedback

Engine Class

![GroundController](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/GroundController-Dark.webp)GroundController

---

Summary

Properties

|  |
| --- |
| [AccelerationLean](#AccelerationLean):[number](/docs/luau/numbers) |
| [AccelerationTime](#AccelerationTime):[number](/docs/luau/numbers) |
| [BalanceMaxTorque](#BalanceMaxTorque):[number](/docs/luau/numbers) |
| [BalanceSpeed](#BalanceSpeed):[number](/docs/luau/numbers) |
| [DecelerationTime](#DecelerationTime):[number](/docs/luau/numbers) |
| [Friction](#Friction):[number](/docs/luau/numbers) |
| [FrictionWeight](#FrictionWeight):[number](/docs/luau/numbers) |
| [GroundOffset](#GroundOffset):[number](/docs/luau/numbers) |
| [StandForce](#StandForce):[number](/docs/luau/numbers) |
| [StandSpeed](#StandSpeed):[number](/docs/luau/numbers) |
| [TurnSpeedFactor](#TurnSpeedFactor):[number](/docs/luau/numbers) |

Inherited Members

3 inherited from [ControllerBase](/docs/reference/engine/classes/ControllerBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Properties

AccelerationLean

Read Parallel

GroundController.AccelerationLean:[number](/docs/luau/numbers)

Provide feedback

---

AccelerationTime

Read Parallel

Estimated time taken to reach the desired speed.

GroundController.AccelerationTime:[number](/docs/luau/numbers)

Estimated time (in seconds) taken to reach the desired speed after walking
input begins. The character will accelerate linearly at the computed rate,
impacted by friction, so a given time may be less accurate with lower
friction.

Provide feedback

---

BalanceMaxTorque

Read Parallel

The maximum torque used to keep the [ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart)
aligned upright.

GroundController.BalanceMaxTorque:[number](/docs/luau/numbers)

The maximum torque used to keep the [ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart)
aligned upright. When misaligned, this amount of torque is applied to
reach the [BalanceSpeed](/docs/reference/engine/classes/GroundController#BalanceSpeed) and realign
the root part. A higher torque means more force is required to cause the
root part to tilt. A lower torque means it's easer for the root part to
get knocked over when running into things. This property is hidden and has
no effect when [ControllerBase.BalanceRigidityEnabled](/docs/reference/engine/classes/ControllerBase#BalanceRigidityEnabled) is true.

Provide feedback

---

BalanceSpeed

Read Parallel

The maximum angular speed used to align the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) upright.

GroundController.BalanceSpeed:[number](/docs/luau/numbers)

The maximum angular speed used to align the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) upright. A lower value means it takes
longer for the root part to recover to the upright position when
misaligned. A higher value results in a quicker recovery.

Provide feedback

---

DecelerationTime

Read Parallel

Estimated time taken to reach a complete stop from full speed.

GroundController.DecelerationTime:[number](/docs/luau/numbers)

Estimated time (in seconds) taken to reach a complete stop from full speed
after walking input ends. The character will decelerate linearly at the
computed rate, impacted by friction, so a given time may be less accurate
with lower friction.

Provide feedback

---

Friction

Read Parallel

The coefficient of friction of the character on the ground.

GroundController.Friction:[number](/docs/luau/numbers)

The coefficient of friction for the character at the point between it and
the ground. Determines how much force is available for locomotion or to
keep the character stationary on slopes.

Provide feedback

---

FrictionWeight

Read Parallel

Amount the character's friction is weighed against the ground friction.

GroundController.FrictionWeight:[number](/docs/luau/numbers)

Amount the character's friction is weighed against the ground friction,
equal in behavior to the
[FrictionWeight](/docs/reference/engine/datatypes/PhysicalProperties#FrictionWeight) data type of
[BasePart.CustomPhysicalProperties](/docs/reference/engine/classes/BasePart#CustomPhysicalProperties). Higher values mean more of a
part's [Friction](/docs/reference/engine/datatypes/PhysicalProperties#Friction) will be used.

Provide feedback

---

GroundOffset

Read Parallel

The target distance above the ground to keep the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) at.

GroundController.GroundOffset:[number](/docs/luau/numbers)

The target distance above the
Class.ControllerManager.GroundSensor.HitPosition to keep the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) at. If the root part is below this
offset from the ground, a force is applied to raise up to this height. If
it's above, nothing happens.

Provide feedback

---

StandForce

Read Parallel

GroundController.StandForce:[number](/docs/luau/numbers)

Provide feedback

---

StandSpeed

Read Parallel

GroundController.StandSpeed:[number](/docs/luau/numbers)

Provide feedback

---

TurnSpeedFactor

Read Parallel

The value multiplied by the [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed).

GroundController.TurnSpeedFactor:[number](/docs/luau/numbers)

The value multiplied by the [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed) to
determine the final target angular velocity while this controller is
active. The angular velocity is applied when turning towards the
Class.ControllerManager.FacingDirection.

Provide feedback

---