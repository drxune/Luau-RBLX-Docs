# RopeConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RopeConstraint
Scraped: 2026-01-11T02:36:32.202947Z

## Tags
- Not Replicated

## Inherits
- Constraint
- RopeConstraint
- Instance
- Object
- Length
- WinchEnabled
- WinchTarget
- WinchSpeed
- WinchResponsiveness
- WinchForce
- Attachments
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [RopeConstraint](/docs/reference/engine/classes/RopeConstraint)

English

Feedback

Engine Class

![RopeConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/RopeConstraint-Dark.webp)RopeConstraint

Simulates rope dynamics, preventing two attachments from separating further
than a defined length.

---

Summary

Properties

|  |
| --- |
| [CurrentDistance](#CurrentDistance):[number](/docs/luau/numbers) |
| [Length](#Length):[number](/docs/luau/numbers) |
| [Restitution](#Restitution):[number](/docs/luau/numbers) |
| [Thickness](#Thickness):[number](/docs/luau/numbers) |
| [WinchEnabled](#WinchEnabled):[boolean](/docs/luau/booleans) |
| [WinchForce](#WinchForce):[number](/docs/luau/numbers) |
| [WinchResponsiveness](#WinchResponsiveness):[number](/docs/luau/numbers) |
| [WinchSpeed](#WinchSpeed):[number](/docs/luau/numbers) |
| [WinchTarget](#WinchTarget):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A RopeConstraint prevents two attachments from separating further than a
defined [Length](/docs/reference/engine/classes/RopeConstraint#Length). The attachments can move closer
together than this length and both can freely rotate. This constraint can also
be powered to behave as a motorized winch.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Winch

If a rope's [WinchEnabled](/docs/reference/engine/classes/RopeConstraint#WinchEnabled) property is
enabled, it attempts to translate the attachments to a set separation
specified by [WinchTarget](/docs/reference/engine/classes/RopeConstraint#WinchTarget), effectively the
target length of the rope in studs. This translation is controlled by
[WinchSpeed](/docs/reference/engine/classes/RopeConstraint#WinchSpeed),
[WinchResponsiveness](/docs/reference/engine/classes/RopeConstraint#WinchResponsiveness), and
[WinchForce](/docs/reference/engine/classes/RopeConstraint#WinchForce).

Note that [WinchSpeed](/docs/reference/engine/classes/RopeConstraint#WinchSpeed) must be a positive
value, used to either contract or extend the rope length to
[WinchTarget](/docs/reference/engine/classes/RopeConstraint#WinchTarget). Setting a negative speed will
revert to 0, not reverse the winch servo direction.

---

API Reference

Properties

CurrentDistance

Read Only

Not Replicated

Read Parallel

The current distance between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

RopeConstraint.CurrentDistance:[number](/docs/luau/numbers)

The current distance between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

Length

Read Parallel

The maximum distance apart the two [Attachments](/docs/reference/engine/classes/Attachment) can be.

RopeConstraint.Length:[number](/docs/luau/numbers)

The maximum distance apart the two [Attachments](/docs/reference/engine/classes/Attachment) can be.
Measured in studs.

Provide feedback

---

Restitution

Read Parallel

Elasticity of the [Attachments](/docs/reference/engine/classes/Attachment) connected by the
constraint when reaching the maximum defined
[Length](/docs/reference/engine/classes/RopeConstraint#Length). Constrained between 0 and 1.

RopeConstraint.Restitution:[number](/docs/luau/numbers)

Elasticity of the [Attachments](/docs/reference/engine/classes/Attachment) connected by the
constraint when reaching the maximum defined
[Length](/docs/reference/engine/classes/RopeConstraint#Length). Constrained between 0 and 1.

Provide feedback

---

Thickness

Read Parallel

The visualized thickness of the [RopeConstraint](/docs/reference/engine/classes/RopeConstraint).

RopeConstraint.Thickness:[number](/docs/luau/numbers)

The visualized thickness of the [RopeConstraint](/docs/reference/engine/classes/RopeConstraint).

Provide feedback

---

WinchEnabled

Read Parallel

Enables the winch motor.

RopeConstraint.WinchEnabled:[boolean](/docs/luau/booleans)

Enables the winch motor which has the effect or reeling in/out the length
of the rope to [WinchTarget](/docs/reference/engine/classes/RopeConstraint#WinchTarget).

Provide feedback

---

WinchForce

Read Parallel

The maximum force that the winch motor can apply.

RopeConstraint.WinchForce:[number](/docs/luau/numbers)

The maximum force that the winch motor can apply.

Provide feedback

---

WinchResponsiveness

Read Parallel

The sharpness of the winch motor in reaching the
[WinchTarget](/docs/reference/engine/classes/RopeConstraint#WinchTarget).

RopeConstraint.WinchResponsiveness:[number](/docs/luau/numbers)

The sharpness of the winch motor in reaching the
[WinchTarget](/docs/reference/engine/classes/RopeConstraint#WinchTarget).

Provide feedback

---

WinchSpeed

Read Parallel

A positive desired velocity at which the winch motor changes the rope
length.

RopeConstraint.WinchSpeed:[number](/docs/luau/numbers)

A positive desired velocity at which the winch motor changes the rope
length.

Provide feedback

---

WinchTarget

Read Parallel

The target length for the winch motor.

RopeConstraint.WinchTarget:[number](/docs/luau/numbers)

The target length for the winch motor.

Provide feedback

---