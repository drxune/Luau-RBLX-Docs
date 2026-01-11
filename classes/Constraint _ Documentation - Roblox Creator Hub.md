# Constraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Constraint
Scraped: 2026-01-11T02:37:01.757552Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- Constraint
- Attachment
- AlignOrientation
- AlignPosition
- AngularVelocity
- AnimationConstraint
- BallSocketConstraint
- Workspace
- Constraint.Enabled
- Constraint.Attachment1
- Constraint.Attachment0
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Constraint](/docs/reference/engine/classes/Constraint)

English

Feedback

Engine Class

Constraint

The base class for constraint-based objects.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Active](#Active):[boolean](/docs/luau/booleans) |
| [Attachment0](#Attachment0):[Attachment](/docs/reference/engine/classes/Attachment) |
| [Attachment1](#Attachment1):[Attachment](/docs/reference/engine/classes/Attachment) |
| [Color](#Color):[BrickColor](/docs/reference/engine/datatypes/BrickColor) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Visible](#Visible):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetDebugAppliedForce](#GetDebugAppliedForce)(bodyId: [number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [GetDebugAppliedTorque](#GetDebugAppliedTorque)(bodyId: [number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[AlignOrientation](/docs/reference/engine/classes/AlignOrientation), [AlignPosition](/docs/reference/engine/classes/AlignPosition), [AngularVelocity](/docs/reference/engine/classes/AngularVelocity), [AnimationConstraint](/docs/reference/engine/classes/AnimationConstraint), [BallSocketConstraint](/docs/reference/engine/classes/BallSocketConstraint), Show more...

The base class for constraint-based objects. See
[mover constraints](/docs/physics/mover-constraints) and
[mechanical constraints](/docs/physics/mechanical-constraints) for more
details.

---

API Reference

Properties

Active

Read Only

Not Replicated

Read Parallel

Indicates if the constraint is currently active in the world.

Constraint.Active:[boolean](/docs/luau/booleans)

This property is true if the constraint and both of its parts are in the
[Workspace](/docs/reference/engine/classes/Workspace) and the constraint's [Constraint.Enabled](/docs/reference/engine/classes/Constraint#Enabled) property
is true.

Provide feedback

---

Attachment0

Read Parallel

The [Attachment](/docs/reference/engine/classes/Attachment) that is connected to
[Constraint.Attachment1](/docs/reference/engine/classes/Constraint#Attachment1).

Constraint.Attachment0:[Attachment](/docs/reference/engine/classes/Attachment)

The [Attachment](/docs/reference/engine/classes/Attachment) that is connected to [Constraint.Attachment1](/docs/reference/engine/classes/Constraint#Attachment1)

Provide feedback

---

Attachment1

Read Parallel

The [Attachment](/docs/reference/engine/classes/Attachment) that is connected to
[Constraint.Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).

Constraint.Attachment1:[Attachment](/docs/reference/engine/classes/Attachment)

The [Attachment](/docs/reference/engine/classes/Attachment) that is connected to [Constraint.Attachment0](/docs/reference/engine/classes/Constraint#Attachment0)

Provide feedback

---

Color

Read Parallel

The color of the constraint.

Constraint.Color:[BrickColor](/docs/reference/engine/datatypes/BrickColor)

The color of the constraint.

Provide feedback

---

Enabled

Read Parallel

Toggles whether or not the constraint is enabled.

Constraint.Enabled:[boolean](/docs/luau/booleans)

Toggles whether or not the constraint is enabled.

Provide feedback

---

Visible

Read Parallel

Toggles the constraint's visibility.

Constraint.Visible:[boolean](/docs/luau/booleans)

Toggles the constraint's visibility.

Provide feedback

---

Methods

GetDebugAppliedForce

Deprecated

Show details

---

GetDebugAppliedTorque

Deprecated

Show details

---