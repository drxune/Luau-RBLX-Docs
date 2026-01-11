# BodyVelocity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyVelocity
Scraped: 2026-01-11T02:34:32.547996Z

## Inherits
- BodyMover
- BodyVelocity
- LinearVelocity
- Instance
- Object
- Velocity
- BasePart.AssemblyLinearVelocity
- BodyAngularVelocity
- BodyPosition
- BodyForce
- BodyThrust
- P
- MaxForce
- Anchored
- BasePart.Velocity
- AlignPosition
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BodyMover](/docs/reference/engine/classes/BodyMover)
6. /
7. [BodyVelocity](/docs/reference/engine/classes/BodyVelocity)

English

Feedback

Engine Class

![BodyVelocity](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BodyVelocity-Dark.webp)BodyVelocity

Deprecated

Applies a force to maintain a constant velocity.

This object is deprecated and should not be used for new work. Use
[LinearVelocity](/docs/reference/engine/classes/LinearVelocity) instead, and see the
[legacy conversion notes](/docs/physics/mover-constraints#legacy-mover-conversion).

---

Summary

Properties

|  |
| --- |
| [MaxForce](#MaxForce):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [maxForce](#maxForce):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [P](#P):[number](/docs/luau/numbers) |
| [Velocity](#Velocity):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [velocity](#velocity):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |

Methods

|  |
| --- |
| [GetLastForce](#GetLastForce)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [lastForce](#lastForce)():[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BodyVelocity object applies a force on an assembly such that it will
maintain a constant velocity. The [Velocity](/docs/reference/engine/classes/BodyVelocity#Velocity)
property, not to be confused with [BasePart.AssemblyLinearVelocity](/docs/reference/engine/classes/BasePart#AssemblyLinearVelocity),
controls the goal velocity.

[BodyVelocity](/docs/reference/engine/classes/BodyVelocity) is the linear counterpart to [BodyAngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity).
If you need the assembly to move toward a goal position, use
[BodyPosition](/docs/reference/engine/classes/BodyPosition) instead. If you need further control on a force applied
to an object, consider using a [BodyForce](/docs/reference/engine/classes/BodyForce) or [BodyThrust](/docs/reference/engine/classes/BodyThrust)
instead.

The strength of the force applied by this object is controlled by several
factors, namely the difference between the assembly's current velocity and the
goal velocity. This is multiplied by [P](/docs/reference/engine/classes/BodyVelocity#P) (power) to
either amplify or diminish it. The resulting force is then capped by
[MaxForce](/docs/reference/engine/classes/BodyVelocity#MaxForce).

---

API Reference

Properties

MaxForce

Read Parallel

Determines the limit on how much force that may be applied to each axis.

BodyVelocity.MaxForce:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the limit on the amount of force that may be
applied on each axis in reaching the goal
[Velocity](/docs/reference/engine/classes/BodyVelocity#Velocity). If an assembly isn't moving,
consider increasing this value and also check that it is not
[Anchored](/docs/reference/engine/classes/BasePart#Anchored) or attached to any anchored assemblies.

Provide feedback

---

maxForce

Deprecated

Show details

---

P

Read Parallel

Determines how aggressive of a force is applied in reaching the goal
velocity.

BodyVelocity.P:[number](/docs/luau/numbers)

This property determines how much power is used while applying force in
order to reach the goal [Velocity](/docs/reference/engine/classes/BodyVelocity#Velocity). The higher
this value, the more power will be used and the faster it will be used.
The force the [BodyVelocity](/docs/reference/engine/classes/BodyVelocity) exerts increases as the difference
between the assembly's current velocity and the goal velocity increases.
This property is multiplied to this force to either amplify or diminish
it.

Provide feedback

---

Velocity

Read Parallel

Determines the goal velocity.

BodyVelocity.Velocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property (not to be confused with [BasePart.Velocity](/docs/reference/engine/classes/BasePart#Velocity))
determines the target velocity towards which force will be exerted. It is
specified relative to the world, not the assembly.

Provide feedback

---

velocity

Deprecated

Show details

---

Methods

GetLastForce

Not implemented and will always return the 0 vector.

BodyVelocity:GetLastForce():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

This method is not implemented and it will always return the 0 vector.
You are advised to use [AlignPosition](/docs/reference/engine/classes/AlignPosition) instead.

Provide feedback

---

lastForce

Returns the last force in the object.

BodyVelocity:lastForce():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the last force in the object.

Provide feedback

---