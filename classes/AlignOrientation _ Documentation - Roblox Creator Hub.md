# AlignOrientation | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AlignOrientation
Scraped: 2026-01-11T02:39:23.275893Z

## Tags
- Not Replicated

## Inherits
- Constraint
- AlignOrientation
- Instance
- Object
- AlignPosition
- AlignType
- Attachment0
- Attachment1
- ReactionTorqueEnabled
- RigidityEnabled
- MaxTorque
- MaxAngularVelocity
- Responsiveness
- Mode
- CFrame
- PrimaryAxis
- SecondaryAxis
- Axis
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [AlignOrientation](/docs/reference/engine/classes/AlignOrientation)

English

Feedback

Engine Class

![AlignOrientation](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AlignOrientation-Dark.webp)AlignOrientation

Constraint which applies torque to align two attachments, or to align one
attachment with a goal orientation.

---

Summary

Properties

|  |
| --- |
| [AlignType](#AlignType):[Enum.AlignType](/docs/reference/engine/enums/AlignType) |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [LookAtPosition](#LookAtPosition):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [MaxAngularVelocity](#MaxAngularVelocity):[number](/docs/luau/numbers) |
| [MaxTorque](#MaxTorque):[number](/docs/luau/numbers) |
| [Mode](#Mode):[Enum.OrientationAlignmentMode](/docs/reference/engine/enums/OrientationAlignmentMode) |
| [PrimaryAxis](#PrimaryAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [PrimaryAxisOnly](#PrimaryAxisOnly):[boolean](/docs/luau/booleans)  Deprecated |
| [ReactionTorqueEnabled](#ReactionTorqueEnabled):[boolean](/docs/luau/booleans) |
| [Responsiveness](#Responsiveness):[number](/docs/luau/numbers) |
| [RigidityEnabled](#RigidityEnabled):[boolean](/docs/luau/booleans) |
| [SecondaryAxis](#SecondaryAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The AlignOrientation constraint applies torque to align two attachments, or
to align one attachment with a goal orientation. As indicated by the name, it
only affects the orientation of the attachments, not their position (to
align attachments positionally, see [AlignPosition](/docs/reference/engine/classes/AlignPosition)).

Torque created by AlignOrientation is applied about the center of mass of
the parent of the attachments, or the center of mass of parts rigidly
connected to the parents.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Affected Axes

The axes affected by torque are controlled through the constraint's
[AlignType](/docs/reference/engine/classes/AlignOrientation#AlignType) property. When set to
[PrimaryAxisParallel](/docs/reference/engine/enums/AlignType),
[PrimaryAxisPerpendicular](/docs/reference/engine/enums/AlignType) or
[PrimaryAxisLookAt](/docs/reference/engine/enums/AlignType), torque will only occur when the primary
axes become misaligned. Otherwise, the constraint will apply torque about all
3 axes to achieve alignment.

#### Reactionary Torque

By default, the constraint only applies torque to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) while
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) remains unaffected. If desired,
torque can be applied to both attachments in equal and opposite directions
by enabling
[ReactionTorqueEnabled](/docs/reference/engine/classes/AlignOrientation#ReactionTorqueEnabled).

#### Torque Magnitude

You can configure this constraint to apply the maximum torque that constraints
allow through the [RigidityEnabled](/docs/reference/engine/classes/AlignOrientation#RigidityEnabled)
property. When true, the physics solver reacts as quickly as possible to
complete the alignment. When false, the torque is determined by
[MaxTorque](/docs/reference/engine/classes/AlignOrientation#MaxTorque),
[MaxAngularVelocity](/docs/reference/engine/classes/AlignOrientation#MaxAngularVelocity), and
[Responsiveness](/docs/reference/engine/classes/AlignOrientation#Responsiveness).

#### Attachment Mode

This constraint can use either one or two attachments in calculating
its goal. See [Mode](/docs/reference/engine/classes/AlignOrientation#Mode) for details.

---

API Reference

Properties

AlignType

Read Parallel

The constraint's axis alignment type.

AlignOrientation.AlignType:[Enum.AlignType](/docs/reference/engine/enums/AlignType)

Specifies the desired relationship between the primary axes of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) and the goal. Available options
are [AllAxes](/docs/reference/engine/enums/AlignType), [PrimaryAxisParallel](/docs/reference/engine/enums/AlignType),
[PrimaryAxisPerpendicular](/docs/reference/engine/enums/AlignType), and
[PrimaryAxisLookAt](/docs/reference/engine/enums/AlignType). The constraint will attempt to
maintain the specified relationship, as given by the [Enum.AlignType](/docs/reference/engine/enums/AlignType), by
applying torques onto the relevant axes.

Provide feedback

---

CFrame

Read Parallel

The [CFrame](/docs/reference/engine/datatypes/CFrame) orientation with which the constraint will attempt
to match the orientation of [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).

AlignOrientation.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

The [CFrame](/docs/reference/engine/datatypes/CFrame) orientation (translation component ignored) with
which the constraint will attempt to match the orientation of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). Only used when
[Mode](/docs/reference/engine/classes/AlignOrientation#Mode) is set to
[OneAttachment](/docs/reference/engine/enums/OrientationAlignmentMode).

Provide feedback

---

LookAtPosition

Not Replicated

Read Parallel

A [Vector3](/docs/reference/engine/datatypes/Vector3) world space location toward which the primary axis
will attempt to align.

AlignOrientation.LookAtPosition:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) world space location toward which the primary axis
will attempt to align. This is only active when
[AlignType](/docs/reference/engine/classes/AlignOrientation#AlignType) is set to
[PrimaryAxisLookAt](/docs/reference/engine/enums/AlignType) and [Mode](/docs/reference/engine/classes/AlignOrientation#Mode)
is set to [OneAttachment](/docs/reference/engine/enums/OrientationAlignmentMode).

Provide feedback

---

MaxAngularVelocity

Read Parallel

Maximum angular velocity the constraint can use to reach its goal.

AlignOrientation.MaxAngularVelocity:[number](/docs/luau/numbers)

Maximum angular velocity the constraint can use to reach its goal. Only
used if [RigidityEnabled](/docs/reference/engine/classes/AlignOrientation#RigidityEnabled) is
false.

Note that [MaxAngularVelocity](/docs/reference/engine/classes/AlignOrientation#MaxAngularVelocity),
as well as [MaxTorque](/docs/reference/engine/classes/AlignOrientation#MaxTorque), are caps to
the angular velocity and torque respectively. The actual scale is
determined by [Responsiveness](/docs/reference/engine/classes/AlignOrientation#Responsiveness).

Provide feedback

---

MaxTorque

Read Parallel

Maximum torque the constraint can use to reach its goal.

AlignOrientation.MaxTorque:[number](/docs/luau/numbers)

Maximum torque the constraint can use to reach its goal. Only used if
[RigidityEnabled](/docs/reference/engine/classes/AlignOrientation#RigidityEnabled) is false.

Note that [MaxTorque](/docs/reference/engine/classes/AlignOrientation#MaxTorque), as well as
[MaxAngularVelocity](/docs/reference/engine/classes/AlignOrientation#MaxAngularVelocity), are
caps to the torque and angular velocity respectively. The actual scale
is determined by [Responsiveness](/docs/reference/engine/classes/AlignOrientation#Responsiveness).

Provide feedback

---

Mode

Read Parallel

Whether the constraint uses one or two attachments in calculating its
goal.

AlignOrientation.Mode:[Enum.OrientationAlignmentMode](/docs/reference/engine/enums/OrientationAlignmentMode)

Whether the constraint uses one or two attachments in calculating
its goal. By default, this is
[TwoAttachment](/docs/reference/engine/enums/OrientationAlignmentMode), meaning that the constraint
attempts to match the orientation of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) with the orientation of
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1), disregarding
[CFrame](/docs/reference/engine/classes/AlignOrientation#CFrame),
[PrimaryAxis](/docs/reference/engine/classes/AlignOrientation#PrimaryAxis), and
[SecondaryAxis](/docs/reference/engine/classes/AlignOrientation#SecondaryAxis).

If set to [OneAttachment](/docs/reference/engine/enums/OrientationAlignmentMode), the constraint
disregards [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) and attempts to
match the orientation of [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) with
the orientation of [CFrame](/docs/reference/engine/classes/AlignOrientation#CFrame), or match the
attachment's [Axis](/docs/reference/engine/classes/Attachment#Axis) and
[SecondaryAxis](/docs/reference/engine/classes/Attachment#SecondaryAxis) with the constraint's
[PrimaryAxis](/docs/reference/engine/classes/AlignOrientation#PrimaryAxis) and
[SecondaryAxis](/docs/reference/engine/classes/AlignOrientation#SecondaryAxis) properties
respectively.

Provide feedback

---

PrimaryAxis

Not Replicated

Read Parallel

The direction of the goal's X axis, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3).

AlignOrientation.PrimaryAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The direction of the goal's X axis, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3). Only used when [Mode](/docs/reference/engine/classes/AlignOrientation#Mode) is
[OneAttachment](/docs/reference/engine/enums/OrientationAlignmentMode).

Provide feedback

---

PrimaryAxisOnly

Deprecated

Show details

---

ReactionTorqueEnabled

Read Parallel

Whether the constraint applies torque only to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0), or to both attachments in
equal and opposite directions.

AlignOrientation.ReactionTorqueEnabled:[boolean](/docs/luau/booleans)

If false (default), the constraint only applies torque to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) while
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) remains unaffected. If true,
the constraint applies torque to both attachments in equal and opposite
directions.

Provide feedback

---

Responsiveness

Read Parallel

Controls how quickly the constraint reaches its goal. Higher values cause
the attachment(s) to align more rapidly.

AlignOrientation.Responsiveness:[number](/docs/luau/numbers)

Controls how quickly the constraint reaches its goal. Higher values cause
the attachment(s) to align more rapidly. Value can be between 5 and 200.

Provide feedback

---

RigidityEnabled

Read Parallel

Whether torque is dependent on other properties, or if the physics solver
reacts as quickly as possible to complete the alignment.

AlignOrientation.RigidityEnabled:[boolean](/docs/luau/booleans)

Whether torque is dependent on other properties, or if the physics solver
reacts as quickly as possible to complete the alignment. If false
(default), the torque is determined by
[MaxTorque](/docs/reference/engine/classes/AlignOrientation#MaxTorque),
[MaxAngularVelocity](/docs/reference/engine/classes/AlignOrientation#MaxAngularVelocity), and
[Responsiveness](/docs/reference/engine/classes/AlignOrientation#Responsiveness). If true, the
physics solver reacts as quickly as possible to complete the alignment.

Provide feedback

---

SecondaryAxis

Not Replicated

Read Parallel

The direction of the goal's Y axis, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3).

AlignOrientation.SecondaryAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The direction of the goal's Y axis, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3). Only used when [Mode](/docs/reference/engine/classes/AlignOrientation#Mode) is
[OneAttachment](/docs/reference/engine/enums/OrientationAlignmentMode).

Provide feedback

---