# LinearVelocity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LinearVelocity
Scraped: 2026-01-11T02:33:32.867402Z

## Inherits
- Constraint
- LinearVelocity
- Instance
- Object
- VectorForce
- AssemblyLinearVelocity
- RelativeTo
- Attachment0
- Attachment1
- MaxForce
- MaxAxesForce
- VelocityConstraintMode
- MaxPlanarAxesForce
- ForceLimitsEnabled
- ForceLimitMode
- Axis
- SecondaryAxis
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [LinearVelocity](/docs/reference/engine/classes/LinearVelocity)

English

Feedback

Engine Class

![LinearVelocity](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/LinearVelocity-Dark.webp)LinearVelocity

Applies force on an assembly to maintain a constant linear velocity.

---

Summary

Properties

|  |
| --- |
| [ForceLimitMode](#ForceLimitMode):[Enum.ForceLimitMode](/docs/reference/engine/enums/ForceLimitMode) |
| [ForceLimitsEnabled](#ForceLimitsEnabled):[boolean](/docs/luau/booleans) |
| [LineDirection](#LineDirection):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [LineVelocity](#LineVelocity):[number](/docs/luau/numbers) |
| [MaxAxesForce](#MaxAxesForce):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [MaxForce](#MaxForce):[number](/docs/luau/numbers) |
| [MaxPlanarAxesForce](#MaxPlanarAxesForce):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [PlaneVelocity](#PlaneVelocity):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [PrimaryTangentAxis](#PrimaryTangentAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ReactionForceEnabled](#ReactionForceEnabled):[boolean](/docs/luau/booleans) |
| [RelativeTo](#RelativeTo):[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo) |
| [SecondaryTangentAxis](#SecondaryTangentAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [VectorVelocity](#VectorVelocity):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [VelocityConstraintMode](#VelocityConstraintMode):[Enum.VelocityConstraintMode](/docs/reference/engine/enums/VelocityConstraintMode) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The LinearVelocity constraint applies force on an assembly to maintain a
constant linear velocity. It can be set to apply force along a
[Vector3](/docs/reference/engine/datatypes/Vector3), line, or 2D plane. Alternatively:

* If you want to control the amount of force applied, use a
  [VectorForce](/docs/reference/engine/classes/VectorForce) constraint.
* If you only need initial linear velocity, set the
  [AssemblyLinearVelocity](/docs/reference/engine/classes/BasePart#AssemblyLinearVelocity) property
  directly on the assembly.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Relativity

Application of velocity can be controlled through the constraint's
[RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) property. If set to
[World](/docs/reference/engine/enums/ActuatorRelativeTo), force will be applied in world coordinates,
independent of the parent or attachment orientations. If set to
[Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo) or
[Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo), force will be applied relative to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) or
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) respectively.

---

API Reference

Properties

ForceLimitMode

Read Parallel

Determines how the constraint force will be limited.

LinearVelocity.ForceLimitMode:[Enum.ForceLimitMode](/docs/reference/engine/enums/ForceLimitMode)

Determines how the constraint force will be limited. When set to
[Magnitude](/docs/reference/engine/enums/ForceLimitMode), the constraint force will have a
magnitude less than [MaxForce](/docs/reference/engine/classes/LinearVelocity#MaxForce). When set to
[PerAxis](/docs/reference/engine/enums/ForceLimitMode), the force along each axis will be less than
the corresponding value in
[MaxAxesForce](/docs/reference/engine/classes/LinearVelocity#MaxAxesForce) when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
[Vector](/docs/reference/engine/enums/VelocityConstraintMode) or the corresponding value in
[MaxPlanarAxesForce](/docs/reference/engine/classes/LinearVelocity#MaxPlanarAxesForce) when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
[Plane](/docs/reference/engine/enums/VelocityConstraintMode). Only used when
[ForceLimitsEnabled](/docs/reference/engine/classes/LinearVelocity#ForceLimitsEnabled) is true.

Provide feedback

---

ForceLimitsEnabled

Read Parallel

Determines if the constraint force will be limited or if the physics
solver can apply an unlimited force to achieve the target velocity.

LinearVelocity.ForceLimitsEnabled:[boolean](/docs/luau/booleans)

Determines if the constraint force will be limited or if the physics
solver can apply an unlimited force to achieve the target velocity. When
enabled, the constraint force is limited based on
[ForceLimitMode](/docs/reference/engine/classes/LinearVelocity#ForceLimitMode). When disabled, the
physics solver will always apply a force that is large enough to achieve
the target velocity.

Provide feedback

---

LineDirection

Read Parallel

The normalized [Vector3](/docs/reference/engine/datatypes/Vector3) direction for constraining the velocity
along a line.

LinearVelocity.LineDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)

The normalized [Vector3](/docs/reference/engine/datatypes/Vector3) direction for constraining the velocity
along a line, when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Line](/docs/reference/engine/enums/VelocityConstraintMode).

Provide feedback

---

LineVelocity

Read Parallel

Float value of the velocity when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Line](/docs/reference/engine/enums/VelocityConstraintMode).

LinearVelocity.LineVelocity:[number](/docs/luau/numbers)

Float value of the velocity when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Line](/docs/reference/engine/enums/VelocityConstraintMode).

Provide feedback

---

MaxAxesForce

Read Parallel

Maximum force along each axis that the constraint can apply to achieve the
vector velocity. Only used if
[ForceLimitsEnabled](/docs/reference/engine/classes/LinearVelocity#ForceLimitsEnabled) is true,
[ForceLimitMode](/docs/reference/engine/classes/LinearVelocity#ForceLimitMode) is
[PerAxis](/docs/reference/engine/enums/ForceLimitMode), and
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
[Vector](/docs/reference/engine/enums/VelocityConstraintMode).

LinearVelocity.MaxAxesForce:[Vector3](/docs/reference/engine/datatypes/Vector3)

Maximum force along each axis that the constraint can apply to achieve the
target velocity. Only used if
[ForceLimitsEnabled](/docs/reference/engine/classes/LinearVelocity#ForceLimitsEnabled) is true,
[ForceLimitMode](/docs/reference/engine/classes/LinearVelocity#ForceLimitMode) is
[PerAxis](/docs/reference/engine/enums/ForceLimitMode), and
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
[Vector](/docs/reference/engine/enums/VelocityConstraintMode). The axes used to apply the limit
correspond to the [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) property.

Provide feedback

---

MaxForce

Read Parallel

Maximum magnitude of the force vector the constraint can apply.

LinearVelocity.MaxForce:[number](/docs/luau/numbers)

Maximum magnitude of the force vector the constraint can apply. Only used
if [ForceLimitsEnabled](/docs/reference/engine/classes/LinearVelocity#ForceLimitsEnabled) is true
and [ForceLimitMode](/docs/reference/engine/classes/LinearVelocity#ForceLimitMode) is
[Magnitude](/docs/reference/engine/enums/ForceLimitMode).

Provide feedback

---

MaxPlanarAxesForce

Read Parallel

Maximum force along each axis that the constraint can apply to achieve the
plane velocity. Only used if
[ForceLimitsEnabled](/docs/reference/engine/classes/LinearVelocity#ForceLimitsEnabled) is true,
[ForceLimitMode](/docs/reference/engine/classes/LinearVelocity#ForceLimitMode) is
[PerAxis](/docs/reference/engine/enums/ForceLimitMode), and
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
[Plane](/docs/reference/engine/enums/VelocityConstraintMode).

LinearVelocity.MaxPlanarAxesForce:[Vector2](/docs/reference/engine/datatypes/Vector2)

Maximum force along each axis that the constraint can apply to achieve the
plane velocity. Only used if
[ForceLimitsEnabled](/docs/reference/engine/classes/LinearVelocity#ForceLimitsEnabled) is true,
[ForceLimitMode](/docs/reference/engine/classes/LinearVelocity#ForceLimitMode) is
[PerAxis](/docs/reference/engine/enums/ForceLimitMode), and
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
[Plane](/docs/reference/engine/enums/VelocityConstraintMode). The axes used to apply the limit
correspond to the [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) property.

Provide feedback

---

PlaneVelocity

Read Parallel

[Vector2](/docs/reference/engine/datatypes/Vector2) value of the velocity in each tangent direction of the
plane.

LinearVelocity.PlaneVelocity:[Vector2](/docs/reference/engine/datatypes/Vector2)

[Vector2](/docs/reference/engine/datatypes/Vector2) value of the velocity in each tangent direction of the
plane, when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Plane](/docs/reference/engine/enums/VelocityConstraintMode).

Provide feedback

---

PrimaryTangentAxis

Read Parallel

The primary axis in the plane, when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Plane](/docs/reference/engine/enums/VelocityConstraintMode).

LinearVelocity.PrimaryTangentAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The primary axis in the plane, when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Plane](/docs/reference/engine/enums/VelocityConstraintMode). Value depends on the value of
[RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) as follows:

* If [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) is set to
  [Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo), this axis is the
  [Axis](/docs/reference/engine/classes/Attachment#Axis) of
  [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).
* If [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) is set to
  [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo), this axis is the
  [Axis](/docs/reference/engine/classes/Attachment#Axis) of
  [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1).
* If [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) is set to
  [World](/docs/reference/engine/enums/ActuatorRelativeTo), this value must be specified in the
  world space.

Provide feedback

---

ReactionForceEnabled

Read Parallel

LinearVelocity.ReactionForceEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

RelativeTo

Read Parallel

Sets the [Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo) property for the constraint.

LinearVelocity.RelativeTo:[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo)

Sets the [Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo) property for the constraint.

Provide feedback

---

SecondaryTangentAxis

Read Parallel

The secondary axis in the plane, when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Plane](/docs/reference/engine/enums/VelocityConstraintMode).

LinearVelocity.SecondaryTangentAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The secondary axis in the plane, when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Plane](/docs/reference/engine/enums/VelocityConstraintMode). Value depends on the value of
[RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) as follows:

* If [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) is set to
  [Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo), this axis is the
  [SecondaryAxis](/docs/reference/engine/classes/Attachment#SecondaryAxis) of
  [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).
* If [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) is set to
  [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo), this axis is the
  [SecondaryAxis](/docs/reference/engine/classes/Attachment#SecondaryAxis) of
  [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1).
* If [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) is set to
  [World](/docs/reference/engine/enums/ActuatorRelativeTo), this value must be specified in the
  world space.

Provide feedback

---

VectorVelocity

Read Parallel

[Vector3](/docs/reference/engine/datatypes/Vector3) velocity value when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Vector](/docs/reference/engine/enums/VelocityConstraintMode).

LinearVelocity.VectorVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

[Vector3](/docs/reference/engine/datatypes/Vector3) velocity value when
[VelocityConstraintMode](/docs/reference/engine/classes/LinearVelocity#VelocityConstraintMode) is
set to [Vector](/docs/reference/engine/enums/VelocityConstraintMode).

Provide feedback

---

VelocityConstraintMode

Read Parallel

The mode of the constraint.

LinearVelocity.VelocityConstraintMode:[Enum.VelocityConstraintMode](/docs/reference/engine/enums/VelocityConstraintMode)

The mode of the constraint: [Line](/docs/reference/engine/enums/VelocityConstraintMode),
[Plane](/docs/reference/engine/enums/VelocityConstraintMode), or
[Vector](/docs/reference/engine/enums/VelocityConstraintMode). Default is
[Vector](/docs/reference/engine/enums/VelocityConstraintMode).

Provide feedback

---