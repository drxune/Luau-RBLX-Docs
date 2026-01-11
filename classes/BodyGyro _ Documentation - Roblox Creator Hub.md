# BodyGyro | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyGyro
Scraped: 2026-01-11T02:29:16.019508Z

## Inherits
- BodyMover
- BodyGyro
- AlignOrientation
- Instance
- Object
- BodyPosition
- BodyAngularVelocity
- CFrame
- MaxTorque
- P
- D
- BasePart.CFrame
- Anchored
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BodyMover](/docs/reference/engine/classes/BodyMover)
6. /
7. [BodyGyro](/docs/reference/engine/classes/BodyGyro)

English

Feedback

Engine Class

![BodyGyro](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BodyGyro-Dark.webp)BodyGyro

Deprecated

Applies a torque to maintain a constant orientation.

This object is deprecated and should not be used for new work. Use
[AlignOrientation](/docs/reference/engine/classes/AlignOrientation) instead, and see the
[legacy conversion notes](/docs/physics/mover-constraints#legacy-mover-conversion).

---

Summary

Properties

|  |
| --- |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [cframe](#cframe):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [D](#D):[number](/docs/luau/numbers) |
| [MaxTorque](#MaxTorque):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [maxTorque](#maxTorque):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [P](#P):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BodyGyro object applies a torque (rotational force) on an assembly such
that it maintains a constant angular displacement, or orientation. This allows
for the creation of assemblies that point in a certain direction, as if a real
gyroscope were acting upon it. Essentially, it's the rotational counterpart to
a [BodyPosition](/docs/reference/engine/classes/BodyPosition).

If you would like to maintain a constant angular velocity, use a
[BodyAngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity) instead.

The [CFrame](/docs/reference/engine/classes/BodyGyro#CFrame) property controls the goal orientation.
Only the angular components of the [CFrame](/docs/reference/engine/datatypes/CFrame) are used; position will
make no difference. [MaxTorque](/docs/reference/engine/classes/BodyGyro#MaxTorque) limits the amount of
angular force that may be applied, [P](/docs/reference/engine/classes/BodyGyro#P) controls the power
used in achieving the goal orientation, and [D](/docs/reference/engine/classes/BodyGyro#D) controls
dampening behavior.

---

API Reference

Properties

CFrame

Read Parallel

Determines the target orientation (translational component ignored).

BodyGyro.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property (not to be confused with [BasePart.CFrame](/docs/reference/engine/classes/BasePart#CFrame)) determines
the target orientation towards which torque will be exerted. Since
[BodyGyro](/docs/reference/engine/classes/BodyGyro) does not apply translational force, the
translational/positional component of the [CFrame](/docs/reference/engine/datatypes/CFrame) is ignored.
Consider using one of the following CFrame constructors in setting this
property: [CFrame.fromAxisAngle()](/docs/reference/engine/datatypes/CFrame#fromAxisAngle),
[CFrame.fromEulerAnglesXYZ()](/docs/reference/engine/datatypes/CFrame#fromEulerAnglesXYZ), or
[CFrame.fromEulerAnglesYXZ()](/docs/reference/engine/datatypes/CFrame#fromEulerAnglesYXZ).

Provide feedback

---

cframe

Deprecated

Show details

---

D

Read Parallel

Determines the amount of dampening to use in reaching the goal
[CFrame](/docs/reference/engine/classes/BodyGyro#CFrame).

BodyGyro.D:[number](/docs/luau/numbers)

This property defines how much dampening will be applied to the torque
used to reach the goal [CFrame](/docs/reference/engine/classes/BodyGyro#CFrame). When the assembly
approaches the goal orientation, it needs to decelerate, otherwise it will
rotate past the goal and have to stop and re-accelerate back toward the
goal. This often creates an undesirable "rubber‑banding" effect, avoided
by applying dampening. The higher this value is set, the greater the
dampening curve becomes, or the slower the assembly will approach the goal
orientation.

Provide feedback

---

MaxTorque

Read Parallel

Determines the limit on how much torque that may be applied to each axis.

BodyGyro.MaxTorque:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the limit on the amount of torque that may be
applied on each axis in reaching the goal orientation
([CFrame](/docs/reference/engine/classes/BodyGyro#CFrame)). If an assembly isn't moving, consider
increasing this value and also check that it is not
[Anchored](/docs/reference/engine/classes/BasePart#Anchored) or attached to any anchored assemblies.

Provide feedback

---

maxTorque

Deprecated

Show details

---

P

Read Parallel

Determines how aggressive of a torque is applied in reaching the goal
orientation.

BodyGyro.P:[number](/docs/luau/numbers)

This property determines how much power is used while applying torque in
order to reach the goal [CFrame](/docs/reference/engine/classes/BodyGyro#CFrame). The higher this
value, the more power will be used and the faster it will be used.

Provide feedback

---