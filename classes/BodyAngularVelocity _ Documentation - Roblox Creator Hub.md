# BodyAngularVelocity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyAngularVelocity
Scraped: 2026-01-11T02:28:58.843565Z

## Inherits
- BodyMover
- BodyAngularVelocity
- AngularVelocity
- Instance
- Object
- BodyVelocity
- BodyGyro
- Anchored
- P
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BodyMover](/docs/reference/engine/classes/BodyMover)
6. /
7. [BodyAngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity)

English

Feedback

Engine Class

![BodyAngularVelocity](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BodyAngularVelocity-Dark.webp)BodyAngularVelocity

Deprecated

Applies a torque to maintain a constant angular velocity.

This object is deprecated and should not be used for new work. Use
[AngularVelocity](/docs/reference/engine/classes/AngularVelocity) instead, and see the
[legacy conversion notes](/docs/physics/mover-constraints#legacy-mover-conversion).

---

Summary

Properties

|  |
| --- |
| [AngularVelocity](#AngularVelocity):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [angularvelocity](#angularvelocity):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [MaxTorque](#MaxTorque):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [maxTorque](#maxTorque):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [P](#P):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BodyAngularVelocity object applies a torque (rotational force) on an
assembly such that it maintains a constant angular velocity as determined by
its [AngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity#AngularVelocity) property. This
allows for the creation of assemblies that continually rotate. It is the
rotational counterpart to a [BodyVelocity](/docs/reference/engine/classes/BodyVelocity). If you would like to
maintain a constant angular displacement, use a [BodyGyro](/docs/reference/engine/classes/BodyGyro) instead.

---

API Reference

Properties

AngularVelocity

Read Parallel

Determines the axis of rotation (direction) and the rotational velocity
(magnitude) in radians/s.

BodyAngularVelocity.AngularVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property is a [Vector3](/docs/reference/engine/datatypes/Vector3) which determines the goal angular
velocity a [BodyAngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity) should maintain through the
exertion of torque. For this property, the direction of the vector is the
axis of rotation. The magnitude is the angular velocity in radians per
second.

You can multiply a [Vector3](/docs/reference/engine/datatypes/Vector3) by [math.rad(360)](/docs/reference/engine/libraries/math#rad), or 2π,
in order to convert angular frequency (rotations per second) into the
desired angular velocity (radians per second).

Provide feedback

---

angularvelocity

Deprecated

Show details

---

MaxTorque

Read Parallel

Determines the limit of torque that may be exerted on each world axis.

BodyAngularVelocity.MaxTorque:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the limit of the torque that may be exerted on
each world axis. If an assembly isn't moving, consider raising this value
and also check that it is not [Anchored](/docs/reference/engine/classes/BasePart#Anchored) or
attached to another anchored assembly). See also
[P](/docs/reference/engine/classes/BodyAngularVelocity#P) (power).

Provide feedback

---

maxTorque

Deprecated

Show details

---

P

Read Parallel

Determines how aggressive of a torque is applied in reaching the goal
angular velocity.

BodyAngularVelocity.P:[number](/docs/luau/numbers)

This property determines how much power is used while applying torque in
order to reach the goal
[AngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity#AngularVelocity). The higher
this value, the more power will be used and the faster it will be used.

Provide feedback

---