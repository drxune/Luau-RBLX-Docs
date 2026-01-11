# AirController | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AirController
Scraped: 2026-01-11T02:29:13.257446Z

## Tags
- Not Replicated

## Inherits
- ControllerBase
- AirController
- Instance
- Object
- BalanceSpeed
- ControllerBase.BalanceRigidityEnabled
- TurningMaxTorque
- MoveMaxForce
- ControllerManager.RootPart
- ControllerManager.MovingDirection
- MaintainLinearMomentum
- ControllerManager.FacingDirection
- MaintainAngularMomentum
- ControllerManager.BaseTurnSpeed
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ControllerBase](/docs/reference/engine/classes/ControllerBase)
6. /
7. [AirController](/docs/reference/engine/classes/AirController)

English

Feedback

Engine Class

![AirController](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AirController-Dark.webp)AirController

---

Summary

Properties

|  |
| --- |
| [BalanceMaxTorque](#BalanceMaxTorque):[number](/docs/luau/numbers) |
| [BalanceSpeed](#BalanceSpeed):[number](/docs/luau/numbers) |
| [LinearImpulse](#LinearImpulse):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [MaintainAngularMomentum](#MaintainAngularMomentum):[boolean](/docs/luau/booleans) |
| [MaintainLinearMomentum](#MaintainLinearMomentum):[boolean](/docs/luau/booleans) |
| [MoveMaxForce](#MoveMaxForce):[number](/docs/luau/numbers) |
| [TurnMaxTorque](#TurnMaxTorque):[number](/docs/luau/numbers) |
| [TurnSpeedFactor](#TurnSpeedFactor):[number](/docs/luau/numbers) |

Inherited Members

3 inherited from [ControllerBase](/docs/reference/engine/classes/ControllerBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Properties

BalanceMaxTorque

Read Parallel

The maximum torque the character can use to remain balanced upright.

AirController.BalanceMaxTorque:[number](/docs/luau/numbers)

The maximum torque the character can use to remain balanced upright. When
misaligned, this amount of torque is applied to reach the
[BalanceSpeed](/docs/reference/engine/classes/AirController#BalanceSpeed) and realign the character.
A higher torque means more force is required to cause the character to
tilt. A lower torque means it's easer for the character to flip in the
air. This property is hidden and has no effect when
[ControllerBase.BalanceRigidityEnabled](/docs/reference/engine/classes/ControllerBase#BalanceRigidityEnabled) is true.

Provide feedback

---

BalanceSpeed

Read Parallel

The maximum angular speed used to align the character upright.

AirController.BalanceSpeed:[number](/docs/luau/numbers)

The maximum angular speed used to align the character upright. A lower
value means it takes longer for the character to recover to the upright
position when misaligned. A higher value results in a quicker recovery.

Provide feedback

---

LinearImpulse

Hidden

Not Replicated

Read Parallel

AirController.LinearImpulse:[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---

MaintainAngularMomentum

Read Parallel

Determines whether angular momentum is preserved when input has stopped.

AirController.MaintainAngularMomentum:[boolean](/docs/luau/booleans)

Determines whether angular momentum is preserved when input has stopped.
If false, the character will apply
[TurningMaxTorque](/docs/reference/engine/classes/AirController#TurningMaxTorque) to bring the
angular velocity toward 0 when there is no input.

Provide feedback

---

MaintainLinearMomentum

Read Parallel

Determines whether linear momentum is preserved when input has stopped.

AirController.MaintainLinearMomentum:[boolean](/docs/luau/booleans)

Determines whether linear momentum is preserved when input has stopped. If
false, the character will apply
[MoveMaxForce](/docs/reference/engine/classes/AirController#MoveMaxForce) to bring the linear
velocity towards 0 when there is no input.

Provide feedback

---

MoveMaxForce

Read Parallel

The maximum force that can be applied on the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) for moving in the
[ControllerManager.MovingDirection](/docs/reference/engine/classes/ControllerManager#MovingDirection).

AirController.MoveMaxForce:[number](/docs/luau/numbers)

The maximum force that can be applied on the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) for moving in the
[ControllerManager.MovingDirection](/docs/reference/engine/classes/ControllerManager#MovingDirection). This affects how quickly
different target linear velocities are reached and how quick the linear
acceleration is if
[MaintainLinearMomentum](/docs/reference/engine/classes/AirController#MaintainLinearMomentum) is
off.

Provide feedback

---

TurnMaxTorque

Read Parallel

The maximum torque that can be applied on the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) for turning towards the
[ControllerManager.FacingDirection](/docs/reference/engine/classes/ControllerManager#FacingDirection).

AirController.TurnMaxTorque:[number](/docs/luau/numbers)

The maximum torque that can be applied on the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) for turning towards the
[ControllerManager.FacingDirection](/docs/reference/engine/classes/ControllerManager#FacingDirection). This effects how quickly
different target angular velocities are reached and how quick angular
deceleration is if
[MaintainAngularMomentum](/docs/reference/engine/classes/AirController#MaintainAngularMomentum) is
off.

Provide feedback

---

TurnSpeedFactor

Read Parallel

The value multiplied by the [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed).

AirController.TurnSpeedFactor:[number](/docs/luau/numbers)

The value multiplied by the [ControllerManager.BaseTurnSpeed](/docs/reference/engine/classes/ControllerManager#BaseTurnSpeed) to
determine the final target angular velocity while this controller is
active. The angular velocity is applied when turning towards the
[ControllerManager.FacingDirection](/docs/reference/engine/classes/ControllerManager#FacingDirection).

Provide feedback

---