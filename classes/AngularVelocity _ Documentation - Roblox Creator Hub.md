# AngularVelocity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AngularVelocity
Scraped: 2026-01-11T02:29:06.541977Z

## Inherits
- Constraint
- AngularVelocity
- Instance
- Object
- Torque
- AssemblyAngularVelocity
- RelativeTo
- Attachment1
- ReactionTorqueEnabled
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [AngularVelocity](/docs/reference/engine/classes/AngularVelocity)

English

Feedback

Engine Class

![AngularVelocity](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AngularVelocity-Dark.webp)AngularVelocity

Applies torque on an assembly to maintain a constant angular velocity.

---

Summary

Properties

|  |
| --- |
| [AngularVelocity](#AngularVelocity):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [MaxTorque](#MaxTorque):[number](/docs/luau/numbers) |
| [ReactionTorqueEnabled](#ReactionTorqueEnabled):[boolean](/docs/luau/booleans) |
| [RelativeTo](#RelativeTo):[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The AngularVelocity constraint applies torque on an assembly to maintain a
constant angular velocity. Alternatively:

* If you want to control the amount of torque applied, use a [Torque](/docs/reference/engine/classes/Torque)
  constraint.
* If you only need initial angular velocity, set the
  [AssemblyAngularVelocity](/docs/reference/engine/classes/BasePart#AssemblyAngularVelocity) method
  directly on the assembly.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Relativity

Application of velocity can be controlled through the constraint's
[RelativeTo](/docs/reference/engine/classes/AngularVelocity#RelativeTo) property. If set to
[World](/docs/reference/engine/enums/ActuatorRelativeTo), the angular velocity vector is used as is. If
set to [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo) and the constraint's
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) property is set to another
attachment, the angular velocity will be affected by that of the other
attachment. Setting [RelativeTo](/docs/reference/engine/classes/AngularVelocity#RelativeTo) to
[Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo) also exposes the
[ReactionTorqueEnabled](/docs/reference/engine/classes/AngularVelocity#ReactionTorqueEnabled) property.

---

API Reference

Properties

AngularVelocity

Read Parallel

A [Vector3](/docs/reference/engine/datatypes/Vector3) that gives the desired or target angular velocity.

AngularVelocity.AngularVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) that gives the desired or target angular velocity.
This vector is set in the [CFrame](/docs/reference/engine/datatypes/CFrame) expressed by the
[RelativeTo](/docs/reference/engine/classes/AngularVelocity#RelativeTo) property.

Provide feedback

---

MaxTorque

Read Parallel

Magnitude of the maximum torque the constraint can apply.

AngularVelocity.MaxTorque:[number](/docs/luau/numbers)

Magnitude of the maximum torque the constraint can apply.

Provide feedback

---

ReactionTorqueEnabled

Read Parallel

Causes the constraint to apply equal and opposite reaction forces.

AngularVelocity.ReactionTorqueEnabled:[boolean](/docs/luau/booleans)

This property, when enabled, causes the constraint to apply equal and
opposite reaction forces. This is important if the two attached parts can
collide, since without reaction forces collisions can create energy that
would otherwise be disregarded.

When enabled, the reaction forces cause the constraint to act like an
angular motor between the two attachments.

Only meaningful when [RelativeTo](/docs/reference/engine/classes/AngularVelocity#RelativeTo) is set
to [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo).

Provide feedback

---

RelativeTo

Read Parallel

AngularVelocity.RelativeTo:[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo)

The [CFrame](/docs/reference/engine/datatypes/CFrame) in which the AngularVelocity force is specified.
If set to [World](/docs/reference/engine/enums/ActuatorRelativeTo), the angular velocity vector is
used as is. If set to [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo), the angular
velocity is transformed by the [CFrame](/docs/reference/engine/datatypes/CFrame) of the assigned
attachment.

[RelativeTo](/docs/reference/engine/classes/AngularVelocity#RelativeTo) can also be set to
[Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo), but it makes no physical sense and
will lead to unpredictable behaviors.

Provide feedback

---