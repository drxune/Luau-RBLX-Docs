# UniversalConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UniversalConstraint
Scraped: 2026-01-11T02:31:56.141205Z

## Inherits
- Constraint
- UniversalConstraint
- Instance
- Object
- BallSocketConstraint
- HingeConstraint
- LimitsEnabled
- MaxAngle
- Restitution
- Attachment0
- Attachments
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [UniversalConstraint](/docs/reference/engine/classes/UniversalConstraint)

English

Feedback

Engine Class

![UniversalConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UniversalConstraint-Dark.webp)UniversalConstraint

Ensures two axes on two bodies remain perpendicular.

---

Summary

Properties

|  |
| --- |
| [LimitsEnabled](#LimitsEnabled):[boolean](/docs/luau/booleans) |
| [MaxAngle](#MaxAngle):[number](/docs/luau/numbers) |
| [Radius](#Radius):[number](/docs/luau/numbers) |
| [Restitution](#Restitution):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A UniversalConstraint ensures two axes on two bodies remain perpendicular.
Contextually, this constraint is more restrictive than a
[BallSocketConstraint](/docs/reference/engine/classes/BallSocketConstraint) but less restrictive than a
[HingeConstraint](/docs/reference/engine/classes/HingeConstraint) by one degree of freedom.

Example applications of this constraint include transmitting power between the
transmission and drive shafts of cars, robotics, and more.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Limits

Enabling the [LimitsEnabled](/docs/reference/engine/classes/UniversalConstraint#LimitsEnabled) property
exposes the [MaxAngle](/docs/reference/engine/classes/UniversalConstraint#MaxAngle) limit to restrict
tilt within a cone, as well as
[Restitution](/docs/reference/engine/classes/UniversalConstraint#Restitution) which defines the
elasticity of the attachments when they reach the limit.

---

API Reference

Properties

LimitsEnabled

Read Parallel

Determines whether the angular motion of attachments' primary axes is
limited.

UniversalConstraint.LimitsEnabled:[boolean](/docs/luau/booleans)

This property, when enabled, limits the relative angular motion of the
primary axes of attachments through a cone constraint. The default value
is false.

Provide feedback

---

MaxAngle

Read Parallel

The max angle, in degrees, of the constraint's limiting cone.

UniversalConstraint.MaxAngle:[number](/docs/luau/numbers)

This property determines the max angle, in degrees, of the constraint's
limiting cone, formed from [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) and
its primary axis. The default value is 45 degrees.

In order for this property to take affect, the constraint's
[LimitsEnabled](/docs/reference/engine/classes/UniversalConstraint#LimitsEnabled) property must be
set to true.

Provide feedback

---

Radius

Read Parallel

The constraint's visualization radius.

UniversalConstraint.Radius:[number](/docs/luau/numbers)

This property indicates the constraint's visualization radius, in studs.
Default value is 0.2.

Provide feedback

---

Restitution

Read Parallel

The restitution coefficient of the cone constraint.

UniversalConstraint.Restitution:[number](/docs/luau/numbers)

This property determines the restitution of the two
[Attachments](/docs/reference/engine/classes/Attachment) connected by the
[UniversalConstraint](/docs/reference/engine/classes/UniversalConstraint) when they reach the end of the range specified
by [MaxAngle](/docs/reference/engine/classes/UniversalConstraint#MaxAngle). The value defaults to 0
and can be any floating number in the range of 0 to 1. Only applies when
[LimitsEnabled](/docs/reference/engine/classes/UniversalConstraint#LimitsEnabled) is set to true.

Provide feedback

---