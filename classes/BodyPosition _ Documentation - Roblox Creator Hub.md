# BodyPosition | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyPosition
Scraped: 2026-01-11T02:40:32.132119Z

## Inherits
- BodyMover
- BodyPosition
- AlignPosition
- Instance
- Object
- Position
- BasePart.Position
- BodyGyro
- BodyForce
- BodyThrust
- P
- D
- MaxForce
- Anchored
- BodyPosition.Position
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BodyMover](/docs/reference/engine/classes/BodyMover)
6. /
7. [BodyPosition](/docs/reference/engine/classes/BodyPosition)

English

Feedback

Engine Class

![BodyPosition](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BodyPosition-Dark.webp)BodyPosition

Deprecated

Applies a force to maintain a constant position.

This object is deprecated and should not be used for new work. Use
[AlignPosition](/docs/reference/engine/classes/AlignPosition) instead, and see the
[legacy conversion notes](/docs/physics/mover-constraints#legacy-mover-conversion).

---

Summary

Properties

|  |
| --- |
| [D](#D):[number](/docs/luau/numbers) |
| [MaxForce](#MaxForce):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [maxForce](#maxForce):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [P](#P):[number](/docs/luau/numbers) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [position](#position):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |

Methods

|  |
| --- |
| [GetLastForce](#GetLastForce)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [lastForce](#lastForce)():[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |

Events

|  |
| --- |
| [ReachedTarget](#ReachedTarget)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BodyPosition object applies a force on an assembly such that it will
maintain a constant position in the world. The
[Position](/docs/reference/engine/classes/BodyPosition#Position) property, not to be confused with
[BasePart.Position](/docs/reference/engine/classes/BasePart#Position), controls the target world position. This is the
translational counterpart to a [BodyGyro](/docs/reference/engine/classes/BodyGyro).

If you need further control on a force applied to an object, consider using a
[BodyForce](/docs/reference/engine/classes/BodyForce) or [BodyThrust](/docs/reference/engine/classes/BodyThrust) instead.

The strength of the force applied by this object is controlled by several
factors, namely the distance to the goal position: the force is stronger when
farther away from the goal. This is amplified by [P](/docs/reference/engine/classes/BodyPosition#P)
(power). The present velocity will also dampen the force applied by this
object, and this is amplified by [D](/docs/reference/engine/classes/BodyPosition#D) (dampening). The
resulting force is then capped by [MaxForce](/docs/reference/engine/classes/BodyPosition#MaxForce). Note
the force applied on the assembly to achieve the goal position may vary on a
per-axis basis.

---

API Reference

Properties

D

Read Parallel

Determines the amount of dampening to use in reaching the goal
[Position](/docs/reference/engine/classes/BodyPosition#Position).

BodyPosition.D:[number](/docs/luau/numbers)

This property determines how much dampening will be applied to the force
used toward reaching the goal [Position](/docs/reference/engine/classes/BodyPosition#Position). When
the assembly approaches the goal position it needs to decelerate,
otherwise it will move past the goal and have to stop and re-accelerate
back toward the goal. This is often creates an undesirable
"rubber‑banding" effect, avoided by applying dampening. The higher this
value is set, the greater the dampening curve becomes, or the slower the
assembly will approach the goal position.

Provide feedback

---

MaxForce

Read Parallel

Determines the limit on how much force that may be applied to each axis.

BodyPosition.MaxForce:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the limit on the amount of force that may be
applied on each axis in reaching the goal
[Position](/docs/reference/engine/classes/BodyPosition#Position). If an assembly isn't moving,
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
position.

BodyPosition.P:[number](/docs/luau/numbers)

This property determines how much power is used while applying force in
order to reach the goal [Position](/docs/reference/engine/classes/BodyPosition#Position). The higher
this value, the more power will be used and the faster it will be used.
The force the [BodyPosition](/docs/reference/engine/classes/BodyPosition) exerts increases as the difference
between the assembly's current position and the goal position increases.
This property is multiplied to this force to either amplify or diminish
it.

Provide feedback

---

Position

Read Parallel

Determines the goal position towards which force will be applied.

BodyPosition.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the goal position towards which the
[BodyPosition](/docs/reference/engine/classes/BodyPosition) will apply force.

Provide feedback

---

position

Deprecated

Show details

---

Methods

GetLastForce

Returns the last force in the object.

BodyPosition:GetLastForce():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

This function returns the last force in the object.

Provide feedback

---

lastForce

Deprecated

Show details

---

Events

ReachedTarget

Fired when the Parent of the BodyPosition reaches the desired
[BodyPosition.Position](/docs/reference/engine/classes/BodyPosition#Position) (within .1 studs). Once this event fires it
will not fire again until [BodyPosition.Position](/docs/reference/engine/classes/BodyPosition#Position) is updated.

BodyPosition.ReachedTarget():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fired when the Parent of the BodyPosition reaches the desired
[BodyPosition.Position](/docs/reference/engine/classes/BodyPosition#Position) (within .1 studs). Once this event fires it
will not fire again until [BodyPosition.Position](/docs/reference/engine/classes/BodyPosition#Position) is updated.

Provide feedback

---