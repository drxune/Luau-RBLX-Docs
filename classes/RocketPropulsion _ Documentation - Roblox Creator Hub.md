# RocketPropulsion | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RocketPropulsion
Scraped: 2026-01-11T02:41:35.965992Z

## Inherits
- BodyMover
- RocketPropulsion
- LineForce
- BasePart
- Instance
- Object
- BodyPosition
- BodyGyro
- BodyMovers
- Fire()
- Abort()
- ReachedTarget
- TargetRadius
- Target
- BodyGyro.MaxTorque
- TargetOffset
- BodyPosition.D
- BodyPosition.P
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BodyMover](/docs/reference/engine/classes/BodyMover)
6. /
7. [RocketPropulsion](/docs/reference/engine/classes/RocketPropulsion)

English

Feedback

Engine Class

![RocketPropulsion](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/RocketPropulsion-Dark.webp)RocketPropulsion

Deprecated

Applies a force so that an assembly follows and faces a target part.

This object is deprecated and should not be used for new work. Use
[LineForce](/docs/reference/engine/classes/LineForce) instead, and see the
[legacy conversion notes](/docs/physics/mover-constraints#legacy-mover-conversion).

---

Summary

Properties

|  |
| --- |
| [CartoonFactor](#CartoonFactor):[number](/docs/luau/numbers) |
| [MaxSpeed](#MaxSpeed):[number](/docs/luau/numbers) |
| [MaxThrust](#MaxThrust):[number](/docs/luau/numbers) |
| [MaxTorque](#MaxTorque):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Target](#Target):[BasePart](/docs/reference/engine/classes/BasePart) |
| [TargetOffset](#TargetOffset):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [TargetRadius](#TargetRadius):[number](/docs/luau/numbers) |
| [ThrustD](#ThrustD):[number](/docs/luau/numbers) |
| [ThrustP](#ThrustP):[number](/docs/luau/numbers) |
| [TurnD](#TurnD):[number](/docs/luau/numbers) |
| [TurnP](#TurnP):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Abort](#Abort)():() |
| [Fire](#Fire)():() |
| [fire](#fire)():()  Deprecated |

Events

|  |
| --- |
| [ReachedTarget](#ReachedTarget)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The RocketPropulsion object applies force on an assembly so that it both
follows and faces a target. It acts like a hybrid of
[BodyPosition](/docs/reference/engine/classes/BodyPosition) and [BodyGyro](/docs/reference/engine/classes/BodyGyro). Unlike other
[BodyMovers](/docs/reference/engine/classes/BodyMover), RocketPropulsion must be instructed to begin
applying or stopping force via [Fire()](/docs/reference/engine/classes/RocketPropulsion#Fire) or
[Abort()](/docs/reference/engine/classes/RocketPropulsion#Abort) respectively.

You can detect when the assembly reaches its target using the
[ReachedTarget](/docs/reference/engine/classes/RocketPropulsion#ReachedTarget) event which fires once
the assembly is within the [TargetRadius](/docs/reference/engine/classes/RocketPropulsion#TargetRadius)
of the [Target](/docs/reference/engine/classes/RocketPropulsion#Target) part.

---

API Reference

Properties

CartoonFactor

Read Parallel

Determines the tendency of the assembly to face the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.CartoonFactor:[number](/docs/luau/numbers)

This property determines the tendency of the assembly to face the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target). By default, this property is set
to 0.7. If set to 0, the assembly will make no effort to face the
target.

Provide feedback

---

MaxSpeed

Read Parallel

Determines the maximum speed at which the assembly will move toward the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.MaxSpeed:[number](/docs/luau/numbers)

This property determines the upper limit of the velocity at which the
assembly will move toward the [Target](/docs/reference/engine/classes/RocketPropulsion#Target).

Provide feedback

---

MaxThrust

Read Parallel

Determines the maximum amount of thrust that will be exerted to move the
assembly.

RocketPropulsion.MaxThrust:[number](/docs/luau/numbers)

This property determines the upper limit of the thrust that may be exerted
to move the assembly. Assemblies that have high mass will require more
thrust in order to remain airborne and thus track the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

Provide feedback

---

MaxTorque

Read Parallel

Determines the maximum amount of torque that may be exerted to rotate the
assembly towards the [Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.MaxTorque:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the upper limit on the amount of torque that may
be exerted in order to rotate the assembly towards the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target). It functions similarly to
[BodyGyro.MaxTorque](/docs/reference/engine/classes/BodyGyro#MaxTorque).

Provide feedback

---

Target

Read Parallel

Determines the object towards which the assembly should follow/face.

RocketPropulsion.Target:[BasePart](/docs/reference/engine/classes/BasePart)

This property determines the object towards which the RocketPropulsion
will exert force/torque. If set to nil, the
[TargetOffset](/docs/reference/engine/classes/RocketPropulsion#TargetOffset) will be used instead.

Provide feedback

---

TargetOffset

Read Parallel

Determines the world offset from the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target) toward which the force/torque is
exerted.

RocketPropulsion.TargetOffset:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the world offset from the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target). It is especially useful when
[Target](/docs/reference/engine/classes/RocketPropulsion#Target) is set to nil, since this
property then acts as the target position.

Provide feedback

---

TargetRadius

Read Parallel

Determines the maximum distance from the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target) at which the assembly must be in
order for [ReachedTarget](/docs/reference/engine/classes/RocketPropulsion#ReachedTarget) to be
fired.

RocketPropulsion.TargetRadius:[number](/docs/luau/numbers)

This property determines the maximum distance from the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target) at which the assembly must be in
order for [ReachedTarget](/docs/reference/engine/classes/RocketPropulsion#ReachedTarget) to be
fired. It does not affect the exerted forces in any way.

Provide feedback

---

ThrustD

Read Parallel

Determines the dampening applied to the assembly in order to prevent it
from overshooting the [Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.ThrustD:[number](/docs/luau/numbers)

This property is used to dampen the velocity of the assembly in order to
prevent it from overshooting the [Target](/docs/reference/engine/classes/RocketPropulsion#Target)
and causing a "rubber‑banding" effect. It behaves similarly to
[BodyPosition.D](/docs/reference/engine/classes/BodyPosition#D).

Provide feedback

---

ThrustP

Read Parallel

Determines how aggressive of a force is applied in reaching the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.ThrustP:[number](/docs/luau/numbers)

This property determines how much power is used while applying force in
order to reach the [Target](/docs/reference/engine/classes/RocketPropulsion#Target) position. The
higher this value, the more power will be used and the faster it will be
used. This property works similarly to [BodyPosition.P](/docs/reference/engine/classes/BodyPosition#P).

Provide feedback

---

TurnD

Read Parallel

Determines the amount of dampening that to use in reaching the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.TurnD:[number](/docs/luau/numbers)

This property specifies how much dampening will be applied to the torque
used to face the [Target](/docs/reference/engine/classes/RocketPropulsion#Target). When the assembly
approaches the goal orientation, it needs to decelerate, otherwise it will
rotate past the goal and have to stop and re-accelerate back toward the
goal. This often creates an undesirable "rubber‑banding" effect, avoided
by applying dampening. The higher this value is set, the greater the
dampening curve becomes, or the slower the part will approach the goal
orientation.

Provide feedback

---

TurnP

Read Parallel

Determines how aggressive of a torque is applied in facing the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.TurnP:[number](/docs/luau/numbers)

This property determines how much power is used while applying torque in
order to face the [Target](/docs/reference/engine/classes/RocketPropulsion#Target). The higher this
value, the more power will be used and the faster it will be used.

Provide feedback

---

Methods

Abort

Causes the assembly to stop moving toward its
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion:Abort():()

Returns

()

Causes the assembly to stop moving toward its
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

Provide feedback

---

Fire

Causes the assembly to start moving toward its
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion:Fire():()

Returns

()

Causes the assembly to start moving toward its
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

Provide feedback

---

fire

Deprecated

Show details

---

Events

ReachedTarget

Fires when the assembly comes within
[TargetRadius](/docs/reference/engine/classes/RocketPropulsion#TargetRadius) of the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

RocketPropulsion.ReachedTarget():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the assembly comes within
[TargetRadius](/docs/reference/engine/classes/RocketPropulsion#TargetRadius) of the
[Target](/docs/reference/engine/classes/RocketPropulsion#Target).

Provide feedback

---