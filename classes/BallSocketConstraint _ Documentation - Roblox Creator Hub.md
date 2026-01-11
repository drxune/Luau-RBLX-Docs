# BallSocketConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BallSocketConstraint
Scraped: 2026-01-11T02:29:38.364426Z

## Inherits
- Constraint
- BallSocketConstraint
- Instance
- Object
- Attachments
- LimitsEnabled
- UpperAngle
- TwistLimitsEnabled
- TwistLowerAngle
- TwistUpperAngle
- Attachment1
- Attachment0
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [BallSocketConstraint](/docs/reference/engine/classes/BallSocketConstraint)

English

Feedback

Engine Class

![BallSocketConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BallSocketConstraint-Dark.webp)BallSocketConstraint

Forces its two attachments into the same position and allows them to freely
rotate about all three axes, with optional limits to restrict both tilt and
twist.

---

Summary

Properties

|  |
| --- |
| [LimitsEnabled](#LimitsEnabled):[boolean](/docs/luau/booleans) |
| [MaxFrictionTorque](#MaxFrictionTorque):[number](/docs/luau/numbers) |
| [Radius](#Radius):[number](/docs/luau/numbers) |
| [Restitution](#Restitution):[number](/docs/luau/numbers) |
| [TwistLimitsEnabled](#TwistLimitsEnabled):[boolean](/docs/luau/booleans) |
| [TwistLowerAngle](#TwistLowerAngle):[number](/docs/luau/numbers) |
| [TwistUpperAngle](#TwistUpperAngle):[number](/docs/luau/numbers) |
| [UpperAngle](#UpperAngle):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A BallSocketConstraint constrains its [Attachments](/docs/reference/engine/classes/Attachment) so that
they occupy the same position. By default it allows both attachments to freely
rotate about all of their axes, but if
[LimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#LimitsEnabled) is true, the
attachments can only rotate in a limited cone.

Note that if this constraint attaches one part (A) to another part (B)
that is anchored or connected to an anchored part (Z), part A will not
be locally simulated when interacting with a player.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Limits

You can set limits to restrict both tilt and twist of a ball socket,
similar to how a human's head can tilt and turn within a limited axial range.
Enabling the [LimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#LimitsEnabled) property
exposes the [UpperAngle](/docs/reference/engine/classes/BallSocketConstraint#UpperAngle) value to
restrict tilt within a cone; it also exposes the
[TwistLimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#TwistLimitsEnabled) property
which, when enabled, lets you restrict twist rotation through the
[TwistLowerAngle](/docs/reference/engine/classes/BallSocketConstraint#TwistLowerAngle) and
[TwistUpperAngle](/docs/reference/engine/classes/BallSocketConstraint#TwistUpperAngle) limits.

---

API Reference

Properties

LimitsEnabled

Read Parallel

Sets whether the BallSocketConstraint sets a limit on rotation based on
[UpperAngle](/docs/reference/engine/classes/BallSocketConstraint#UpperAngle).

BallSocketConstraint.LimitsEnabled:[boolean](/docs/luau/booleans)

Sets whether the BallSocketConstraint has a limit on rotation based on
[UpperAngle](/docs/reference/engine/classes/BallSocketConstraint#UpperAngle). When true, it
enforces that its [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) isn't rotated
more than a set angle from its [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).

Provide feedback

---

MaxFrictionTorque

Read Parallel

Sets the maximum frictional torque applied to keep its
[Attachments](/docs/reference/engine/classes/Attachment) aligned.

BallSocketConstraint.MaxFrictionTorque:[number](/docs/luau/numbers)

Sets the maximum frictional torque applied to keep its
[Attachments](/docs/reference/engine/classes/Attachment) aligned.

MaxFrictionTorque specifies the stiffness of the BallSocketConstraint
(how much it resists rotation around its [Attachments](/docs/reference/engine/classes/Attachment)).

Provide feedback

---

Radius

Read Parallel

The visualized radius of the BallSocketConstraint.

BallSocketConstraint.Radius:[number](/docs/luau/numbers)

The visualized radius of the BallSocketConstraint.

Provide feedback

---

Restitution

Read Parallel

How elastic [Attachments](/docs/reference/engine/classes/Attachment) connected by a
BallSocketConstraint will be when they reach the end of the range
specified by [UpperAngle](/docs/reference/engine/classes/BallSocketConstraint#UpperAngle) when
[LimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#LimitsEnabled) is true.

BallSocketConstraint.Restitution:[number](/docs/luau/numbers)

How elastic [Attachments](/docs/reference/engine/classes/Attachment) connected by a
BallSocketConstraint will be when they reach the end of the range
specified by [UpperAngle](/docs/reference/engine/classes/BallSocketConstraint#UpperAngle) when
[LimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#LimitsEnabled) is true.
Constrained between 0 and 1.

Provide feedback

---

TwistLimitsEnabled

Read Parallel

Sets whether the BallSocketConstraint sets a limit on twist rotation
based on [TwistUpperAngle](/docs/reference/engine/classes/BallSocketConstraint#TwistUpperAngle) and
[TwistLowerAngle](/docs/reference/engine/classes/BallSocketConstraint#TwistLowerAngle).

BallSocketConstraint.TwistLimitsEnabled:[boolean](/docs/luau/booleans)

Sets whether the BallSocketConstraint sets a limit on twist rotation
based on [TwistUpperAngle](/docs/reference/engine/classes/BallSocketConstraint#TwistUpperAngle) and
[TwistLowerAngle](/docs/reference/engine/classes/BallSocketConstraint#TwistLowerAngle). The twist
angle is defined as the angle between the Y axis of
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) and the Y axis of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).

Provide feedback

---

TwistLowerAngle

Read Parallel

Sets the lower twist rotation limit of the BallSocketConstraint, as long
as [TwistLimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#TwistLimitsEnabled) is
true.

BallSocketConstraint.TwistLowerAngle:[number](/docs/luau/numbers)

Sets the lower twist rotation limit of the BallSocketConstraint, as long
as [TwistLimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#TwistLimitsEnabled) is
true.

Provide feedback

---

TwistUpperAngle

Read Parallel

Sets the upper twist rotation limit of the BallSocketConstraint, as long
as [TwistLimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#TwistLimitsEnabled) is
true.

BallSocketConstraint.TwistUpperAngle:[number](/docs/luau/numbers)

Sets the upper twist rotation limit of the BallSocketConstraint, as long
as [TwistLimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#TwistLimitsEnabled) is
true.

Provide feedback

---

UpperAngle

Read Parallel

Sets the upper rotation limit of the BallSocketConstraint, as long as
[LimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#LimitsEnabled) is true.

BallSocketConstraint.UpperAngle:[number](/docs/luau/numbers)

Sets the upper rotation limit of the BallSocketConstraint, as long as
[LimitsEnabled](/docs/reference/engine/classes/BallSocketConstraint#LimitsEnabled) is true.

Provide feedback

---