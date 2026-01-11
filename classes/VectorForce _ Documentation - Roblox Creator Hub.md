# VectorForce | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VectorForce
Scraped: 2026-01-11T02:30:10.314144Z

## Inherits
- Constraint
- VectorForce
- Instance
- Object
- LinearVelocity
- AssemblyLinearVelocity
- Attachment0
- ApplyAtCenterOfMass
- RelativeTo
- Attachment1
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [VectorForce](/docs/reference/engine/classes/VectorForce)

English

Feedback

Engine Class

![VectorForce](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/VectorForce-Dark.webp)VectorForce

Applies constant force to an assembly.

---

Summary

Properties

|  |
| --- |
| [ApplyAtCenterOfMass](#ApplyAtCenterOfMass):[boolean](/docs/luau/booleans) |
| [Force](#Force):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [RelativeTo](#RelativeTo):[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The VectorForce constraint applies constant force to an assembly. The
direction and strength of the force is determined by a [Vector3](/docs/reference/engine/datatypes/Vector3) and
can be relative to an attachment on the part, another attachment, or the world
coordinate system. Alternatively:

* Because the VectorForce constraint applies constant force and
  acceleration, very high speeds may result if no other forces are involved.
  If you want to maintain a more steady velocity over time, use a
  [LinearVelocity](/docs/reference/engine/classes/LinearVelocity) constraint.
* If you only need initial velocity, set the
  [AssemblyLinearVelocity](/docs/reference/engine/classes/BasePart#AssemblyLinearVelocity) property
  directly on the assembly.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Force Location

By default, force is applied to the assembly at the location of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). Thus, if its center of mass is not
aligned with the direction/point of force, torque will be applied as well. If
desired, force can be focused at the center of mass by toggling on
[ApplyAtCenterOfMass](/docs/reference/engine/classes/VectorForce#ApplyAtCenterOfMass).

#### Relativity

By default, force is applied relative to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). If the parent assembly rotates,
the force will change direction to match the adjusted orientation of the
attachment; visualize this behavior in how the thruster of a rocket pushes it
forward, regardless of the rocket's rotation.

If [RelativeTo](/docs/reference/engine/classes/VectorForce#RelativeTo) is set to
[World](/docs/reference/engine/enums/ActuatorRelativeTo), force will be applied in world coordinates,
independent of the parent or attachment orientations; visualize this behavior
as a directional force like the wind blowing against an object.

If [RelativeTo](/docs/reference/engine/classes/VectorForce#RelativeTo) is set to
[Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo), force will be applied relative to
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) and, if the attachment rotates, the
force will change to match its orientation.

---

API Reference

Properties

ApplyAtCenterOfMass

Read Parallel

Whether force is applied at the center of mass of the parent assembly.

VectorForce.ApplyAtCenterOfMass:[boolean](/docs/luau/booleans)

When true, force is applied at the center of mass of the parent assembly
of [Attachment0](/docs/reference/engine/classes/VectorForce#Attachment0). When false, force is
applied at [Attachment0](/docs/reference/engine/classes/VectorForce#Attachment0).

Provide feedback

---

Force

Read Parallel

The strength and direction of the force.

VectorForce.Force:[Vector3](/docs/reference/engine/datatypes/Vector3)

The strength and direction of the force.

Provide feedback

---

RelativeTo

Read Parallel

The [CFrame](/docs/reference/engine/datatypes/CFrame) in which the force is expressed.

VectorForce.RelativeTo:[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo)

This property determines the [CFrame](/docs/reference/engine/datatypes/CFrame) in which the force is
expressed.

Provide feedback

---