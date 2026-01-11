# AlignPosition | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AlignPosition
Scraped: 2026-01-11T02:37:35.422456Z

## Inherits
- Constraint
- AlignPosition
- Instance
- Object
- AlignOrientation
- Attachment0
- ApplyAtCenterOfMass
- Attachment1
- ReactionForceEnabled
- RigidityEnabled
- ForceLimitMode
- MaxVelocity
- Responsiveness
- Mode
- MaxForce
- MaxAxesForce
- ForceRelativeTo
- AlignPosition.ForceLimitMode
- Position
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [AlignPosition](/docs/reference/engine/classes/AlignPosition)

English

Feedback

Engine Class

![AlignPosition](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AlignPosition-Dark.webp)AlignPosition

Constraint which applies force to move two attachments together, or to move
one attachment to a goal position.

---

Summary

Properties

|  |
| --- |
| [ApplyAtCenterOfMass](#ApplyAtCenterOfMass):[boolean](/docs/luau/booleans) |
| [ForceLimitMode](#ForceLimitMode):[Enum.ForceLimitMode](/docs/reference/engine/enums/ForceLimitMode) |
| [ForceRelativeTo](#ForceRelativeTo):[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo) |
| [MaxAxesForce](#MaxAxesForce):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [MaxForce](#MaxForce):[number](/docs/luau/numbers) |
| [MaxVelocity](#MaxVelocity):[number](/docs/luau/numbers) |
| [Mode](#Mode):[Enum.PositionAlignmentMode](/docs/reference/engine/enums/PositionAlignmentMode) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ReactionForceEnabled](#ReactionForceEnabled):[boolean](/docs/luau/booleans) |
| [Responsiveness](#Responsiveness):[number](/docs/luau/numbers) |
| [RigidityEnabled](#RigidityEnabled):[boolean](/docs/luau/booleans) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The AlignPosition constraint applies force to move two attachments together,
or to move one attachment to a goal position. As indicated by the name, it
only affects the position of the attachments, not their orientation (to
align attachments by orientation, see [AlignOrientation](/docs/reference/engine/classes/AlignOrientation)).

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Force Location

By default, force is applied to the parent of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) at that attachment's location,
meaning that if the parent's center of mass is not aligned with the direction
of the force, torque will be applied as well as force. Alternatively, force
can be applied to the parents' center of mass by toggling on
[ApplyAtCenterOfMass](/docs/reference/engine/classes/AlignPosition#ApplyAtCenterOfMass).

#### Reactionary Force

By default, the constraint only applies force to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) while
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) remains unaffected. If desired,
force can be applied to both attachments in equal and opposite directions
by enabling [ReactionForceEnabled](/docs/reference/engine/classes/AlignPosition#ReactionForceEnabled).

#### Force Limits

You can configure this constraint to apply the maximum force that constraints
allow through the [RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled)
property. When true, the physics solver reacts as quickly as possible to
complete the alignment. When false, the force applied by the constraint is
limited based on [ForceLimitMode](/docs/reference/engine/classes/AlignPosition#ForceLimitMode),
[MaxVelocity](/docs/reference/engine/classes/AlignPosition#MaxVelocity), and
[Responsiveness](/docs/reference/engine/classes/AlignPosition#Responsiveness). See
[ForceLimitMode](/docs/reference/engine/classes/AlignPosition#ForceLimitMode) for further details.

#### Attachment Mode

This constraint can use either one or two attachments in calculating
its goal. See [Mode](/docs/reference/engine/classes/AlignPosition#Mode) for details.

---

API Reference

Properties

ApplyAtCenterOfMass

Read Parallel

Whether force is applied to the parent of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) at that attachment's location,
or at the parents' center of mass.

AlignPosition.ApplyAtCenterOfMass:[boolean](/docs/luau/booleans)

When false (default), force is applied to the parent of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) at that attachment's location,
meaning that if the parent's center of mass is not aligned with the
direction of the force, torque will be applied as well as force. When
true, force is applied at the parents' center of mass.

Provide feedback

---

ForceLimitMode

Read Parallel

Determines how the constraint force will be limited. Only used if
[RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled) is false.

AlignPosition.ForceLimitMode:[Enum.ForceLimitMode](/docs/reference/engine/enums/ForceLimitMode)

Determines how the constraint force will be limited when
[RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled) is false. When set
to [Magnitude](/docs/reference/engine/enums/ForceLimitMode), the constraint force will be limited
such that the magnitude is less than
[MaxForce](/docs/reference/engine/classes/AlignPosition#MaxForce). When set to
[PerAxis](/docs/reference/engine/enums/ForceLimitMode), the constraint force along each axis will
be limited by [MaxAxesForce](/docs/reference/engine/classes/AlignPosition#MaxAxesForce). The axes
along which the force will be limited are based on the
[ForceRelativeTo](/docs/reference/engine/classes/AlignPosition#ForceRelativeTo) property.

Provide feedback

---

ForceRelativeTo

Read Parallel

Determines the axes that the constraint uses to limit the force. Only
applies when [RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled) is
false and [AlignPosition.ForceLimitMode](/docs/reference/engine/classes/AlignPosition#ForceLimitMode) is
[PerAxis](/docs/reference/engine/enums/ForceLimitMode). .

AlignPosition.ForceRelativeTo:[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo)

Determines the axes that the constraint uses to limit the force. Only
applies when [RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled) is
false and [AlignPosition.ForceLimitMode](/docs/reference/engine/classes/AlignPosition#ForceLimitMode) is
[PerAxis](/docs/reference/engine/enums/ForceLimitMode). When set to
[World](/docs/reference/engine/enums/ActuatorRelativeTo), the constraint force is computed in the
world reference frame and the force limits specified in
[MaxAxesForce](/docs/reference/engine/classes/AlignPosition#MaxAxesForce) refer to the axes of the
world coordinate system. When set to [Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo)
or [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo), the force limits specified in
[MaxAxesForce](/docs/reference/engine/classes/AlignPosition#MaxAxesForce) refer to the axes of the
specified attachment coordinate system.

Provide feedback

---

MaxAxesForce

Read Parallel

Maximum force along each axis that the constraint can apply to achieve its
goal.

AlignPosition.MaxAxesForce:[Vector3](/docs/reference/engine/datatypes/Vector3)

Maximum force along each axis that the constraint can apply to achieve its
goal. Only used if [RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled)
is false and [ForceLimitMode](/docs/reference/engine/classes/AlignPosition#ForceLimitMode) is
[PerAxis](/docs/reference/engine/enums/ForceLimitMode). The axes used to apply to the limit are
specified using the [ForceRelativeTo](/docs/reference/engine/classes/AlignPosition#ForceRelativeTo)
property.

Provide feedback

---

MaxForce

Read Parallel

Maximum force magnitude the constraint can apply to achieve its goal.

AlignPosition.MaxForce:[number](/docs/luau/numbers)

Maximum force magnitude the constraint can apply to achieve its goal. Only
used if [RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled) is false
and [ForceLimitMode](/docs/reference/engine/classes/AlignPosition#ForceLimitMode) is
[Magnitude](/docs/reference/engine/enums/ForceLimitMode).

Note that [MaxForce](/docs/reference/engine/classes/AlignPosition#MaxForce), as well as
[MaxVelocity](/docs/reference/engine/classes/AlignPosition#MaxVelocity), are caps to the force
and velocity respectively. The actual scale is determined by
[Responsiveness](/docs/reference/engine/classes/AlignPosition#Responsiveness).

Provide feedback

---

MaxVelocity

Read Parallel

Maximum speed the attachments can move when converging.

AlignPosition.MaxVelocity:[number](/docs/luau/numbers)

Maximum speed the attachments can move when converging. Only used if
[RigidityEnabled](/docs/reference/engine/classes/AlignPosition#RigidityEnabled) is false.

Note that [MaxVelocity](/docs/reference/engine/classes/AlignPosition#MaxVelocity), as well as
[MaxForce](/docs/reference/engine/classes/AlignPosition#MaxForce), are caps to the velocity and
force respectively. The actual scale is determined by
[Responsiveness](/docs/reference/engine/classes/AlignPosition#Responsiveness).

Provide feedback

---

Mode

Read Parallel

Whether the constraint uses one or two attachments in calculating its
goal.

AlignPosition.Mode:[Enum.PositionAlignmentMode](/docs/reference/engine/enums/PositionAlignmentMode)

Whether the constraint uses one or two attachments in calculating
its goal. By default, this is [TwoAttachment](/docs/reference/engine/enums/PositionAlignmentMode),
meaning that the constraint disregards
[Position](/docs/reference/engine/classes/AlignPosition#Position) and attempts to move
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) to the position of
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1).

If set to [OneAttachment](/docs/reference/engine/enums/PositionAlignmentMode), the constraint
disregards [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) and attempts to move
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) to
[Position](/docs/reference/engine/classes/AlignPosition#Position).

Provide feedback

---

Position

Read Parallel

The position to which the constraint should move its
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).

AlignPosition.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

The position to which the constraint should move its
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). Only used if
[Mode](/docs/reference/engine/classes/AlignPosition#Mode) is set to
[OneAttachment](/docs/reference/engine/enums/PositionAlignmentMode), in which case
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) is disregarded.

Provide feedback

---

ReactionForceEnabled

Read Parallel

Whether the constraint applies force only to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0), or to both attachments in
equal and opposite directions.

AlignPosition.ReactionForceEnabled:[boolean](/docs/luau/booleans)

If false (default), the constraint only applies force to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) while
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) remains unaffected. If true,
the constraint applies force to both attachments in equal and opposite
directions.

Provide feedback

---

Responsiveness

Read Parallel

Controls how quickly the constraint reaches its goal. Higher values cause
the attachment(s) to align more rapidly.

AlignPosition.Responsiveness:[number](/docs/luau/numbers)

Controls how quickly the constraint reaches its goal. Higher values cause
the attachment(s) to align more rapidly. Value can be between 5 and 200.

Provide feedback

---

RigidityEnabled

Read Parallel

Whether force is dependent on other properties, or if the physics solver
reacts as quickly as possible to complete the alignment.

AlignPosition.RigidityEnabled:[boolean](/docs/luau/booleans)

Whether force is dependent on other properties, or if the physics solver
reacts as quickly as possible to complete the alignment. If false
(default), the force is determined by
[MaxForce](/docs/reference/engine/classes/AlignPosition#MaxForce),
[MaxVelocity](/docs/reference/engine/classes/AlignPosition#MaxVelocity), and
[Responsiveness](/docs/reference/engine/classes/AlignPosition#Responsiveness). If true, the
physics solver reacts as quickly as possible to complete the alignment.

Provide feedback

---