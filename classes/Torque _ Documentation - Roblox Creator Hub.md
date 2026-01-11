# Torque | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Torque
Scraped: 2026-01-11T02:31:35.328025Z

## Inherits
- Constraint
- Torque
- Instance
- Object
- AngularVelocity
- AssemblyAngularVelocity
- Attachment0
- RelativeTo
- Attachment1
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [Torque](/docs/reference/engine/classes/Torque)

English

Feedback

Engine Class

![Torque](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Torque-Dark.webp)Torque

Applies constant torque to an assembly from its center of mass.

---

Summary

Properties

|  |
| --- |
| [RelativeTo](#RelativeTo):[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo) |
| [Torque](#Torque):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A Torque constraint applies constant torque to an assembly from its center
of mass. Alternatively:

* Because the Torque constraint applies constant torque and angular
  acceleration, very high speeds may result if no other forces are involved.
  If you want to maintain a more steady velocity over time, use an
  [AngularVelocity](/docs/reference/engine/classes/AngularVelocity) constraint.
* If you only need initial velocity, set the
  [AssemblyAngularVelocity](/docs/reference/engine/classes/BasePart#AssemblyAngularVelocity) property
  directly on the assembly.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Relativity

By default, torque is applied relative to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). If the parent assembly rotates,
the torque will change direction to match the adjusted orientation of the
attachment.

If [RelativeTo](/docs/reference/engine/classes/Torque#RelativeTo) is set to
[World](/docs/reference/engine/enums/ActuatorRelativeTo), torque will be applied in world coordinates,
independent of the parent or attachment orientations.

If [RelativeTo](/docs/reference/engine/classes/Torque#RelativeTo) is set to
[Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo), torque will be applied relative to
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) and, if the attachment rotates,
change to match its orientation.

---

API Reference

Properties

RelativeTo

Read Parallel

The [CFrame](/docs/reference/engine/datatypes/CFrame) in which the torque is expressed.

Torque.RelativeTo:[Enum.ActuatorRelativeTo](/docs/reference/engine/enums/ActuatorRelativeTo)

The [CFrame](/docs/reference/engine/datatypes/CFrame) in which the torque is expressed.

Provide feedback

---

Torque

Read Parallel

The strength and direction of the torque.

Torque.Torque:[Vector3](/docs/reference/engine/datatypes/Vector3)

The strength and direction of the torque.

Provide feedback

---