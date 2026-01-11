# BodyForce | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyForce
Scraped: 2026-01-11T02:29:15.821832Z

## Inherits
- BodyMover
- BodyForce
- VectorForce
- Instance
- Object
- Force
- BodyThrust
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BodyMover](/docs/reference/engine/classes/BodyMover)
6. /
7. [BodyForce](/docs/reference/engine/classes/BodyForce)

English

Feedback

Engine Class

![BodyForce](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BodyForce-Dark.webp)BodyForce

Deprecated

Applies a constant force to an object.

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

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BodyForce object applies (or exerts) a force on the assembly to which it
is parented. If the magnitude of such a force is great enough, assemblies can
begin to accelerate. The force is determined by the
[Force](/docs/reference/engine/classes/BodyForce#Force) property, and is defined on the three world
axes.

A BodyForce alone cannot apply a torque (it cannot cause the parent to
rotate on its own). To apply a force at a specific point or apply forces
relative to the orientation of the assembly, use a [BodyThrust](/docs/reference/engine/classes/BodyThrust) instead.

---

API Reference

Properties

Force

Read Parallel

Determines the force exerted on each axis.

BodyForce.Force:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines the magnitude of force exerted on each axis,
relative to the world.

Provide feedback

---

force

Deprecated

Show details

---