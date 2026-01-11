# ClimbController | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ClimbController
Scraped: 2026-01-11T02:32:39.259202Z

## Inherits
- ControllerBase
- ClimbController
- Instance
- Object
- ControllerManager.RootPart
- BalanceSpeed
- ControllerBase.BalanceRigidityEnabled
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ControllerBase](/docs/reference/engine/classes/ControllerBase)
6. /
7. [ClimbController](/docs/reference/engine/classes/ClimbController)

English

Feedback

Engine Class

![ClimbController](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ClimbController-Dark.webp)ClimbController

---

Summary

Properties

|  |
| --- |
| [AccelerationTime](#AccelerationTime):[number](/docs/luau/numbers) |
| [BalanceMaxTorque](#BalanceMaxTorque):[number](/docs/luau/numbers) |
| [BalanceSpeed](#BalanceSpeed):[number](/docs/luau/numbers) |
| [MoveMaxForce](#MoveMaxForce):[number](/docs/luau/numbers) |

Inherited Members

3 inherited from [ControllerBase](/docs/reference/engine/classes/ControllerBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Properties

AccelerationTime

Read Parallel

The amount of time taken to reach the desired climb velocity from 0.

ClimbController.AccelerationTime:[number](/docs/luau/numbers)

The amount of time taken to reach the desired climb velocity from 0. May
be inaccurate depending on max force and gravity.

Provide feedback

---

BalanceMaxTorque

Read Parallel

The maximum torque used to keep the [ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart)
aligned upright and aligned to the climbed surface.

ClimbController.BalanceMaxTorque:[number](/docs/luau/numbers)

The maximum torque used to keep the [ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart)
aligned upright and aligned to the
Class.ControllerManager.ClimbSensor.HitNormal. When misaligned, this
amount of torque is applied to reach the
[BalanceSpeed](/docs/reference/engine/classes/ClimbController#BalanceSpeed) and realign the root
part. A higher torque means more force is required to cause the root part
to tilt. This property is hidden and has no effect when
[ControllerBase.BalanceRigidityEnabled](/docs/reference/engine/classes/ControllerBase#BalanceRigidityEnabled) is true.

Provide feedback

---

BalanceSpeed

Read Parallel

The maximum angular speed used to align the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) upright and with the climbed surface.

ClimbController.BalanceSpeed:[number](/docs/luau/numbers)

The maximum angular speed used to align the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) upright and aligned to the
Class.ControllerManager.ClimbSensor.HitNormal. A lower value means it
takes longer for the root part to recover to the align position when
misaligned. A higher value results in a quicker recovery.

Provide feedback

---

MoveMaxForce

Read Parallel

The maximum force used by the climbing "motor" to move the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) or keep it stationary.

ClimbController.MoveMaxForce:[number](/docs/luau/numbers)

The maximum force used by the climbing "motor" to move the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) or keep it stationary.

Provide feedback

---