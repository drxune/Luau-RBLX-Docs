# BodyThrust | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyThrust
Scraped: 2026-01-11T02:31:01.363017Z

## Inherits
- BodyMover
- BodyThrust
- VectorForce
- Instance
- Object
- BodyForce
- Location
- BodyAngularVelocity
- BodyGyro
- Force
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BodyMover](/docs/reference/engine/classes/BodyMover)
6. /
7. [BodyThrust](/docs/reference/engine/classes/BodyThrust)

English

Feedback

Engine Class

![BodyThrust](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BodyThrust-Dark.webp)BodyThrust

Deprecated

Applies a constant force to an object at a specific point.

This object is deprecated and should not be used for new work. Use
[VectorForce](/docs/reference/engine/classes/VectorForce) instead, and see the
[legacy conversion notes](/docs/physics/mover-constraints#legacy-mover-conversion).

---

Summary

Properties

|  |
| --- |
| [Force](#Force):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [force](#force):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [Location](#Location):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [location](#location):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BodyThrust object applies a force relative to the assembly to which it
is parented at a specific location. It behaves similar to a [BodyForce](/docs/reference/engine/classes/BodyForce)
except that this object's force applies at a specific point
([Location](/docs/reference/engine/classes/BodyThrust#Location)), allowing you to exert a torque
(rotational force). To apply a force dynamically so that an assembly maintains
a constant angular velocity, use a [BodyAngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity) instead. To
apply a force dynamically so that an assembly maintains a constant orientation
(angular position), use a [BodyGyro](/docs/reference/engine/classes/BodyGyro).

---

API Reference

Properties

Force

Read Parallel

Determines the amount of force exerted on each axis relative to the
assembly.

BodyThrust.Force:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the amount of force exerted on each axis relative
to the assembly. The force is exerted at the
[Location](/docs/reference/engine/classes/BodyThrust#Location) which is also relative to the
assembly.

Provide feedback

---

force

Deprecated

Show details

---

Location

Read Parallel

Determines the relative position where the [Force](/docs/reference/engine/classes/BodyThrust#Force)
is exerted.

BodyThrust.Location:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the relative position where the
[Force](/docs/reference/engine/classes/BodyThrust#Force) is exerted. This is the primary means for
turning force into torque.

Provide feedback

---

location

Deprecated

Show details

---