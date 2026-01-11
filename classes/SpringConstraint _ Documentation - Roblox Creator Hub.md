# SpringConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SpringConstraint
Scraped: 2026-01-11T02:39:28.670594Z

## Tags
- Not Replicated

## Inherits
- Constraint
- SpringConstraint
- Instance
- Object
- Attachments
- CylindricalConstraint
- FreeLength
- Damping
- Stiffness
- LimitsEnabled
- MinLength
- MaxLength
- PrismaticConstraint
- RopeConstraint
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [SpringConstraint](/docs/reference/engine/classes/SpringConstraint)

English

Feedback

Engine Class

![SpringConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SpringConstraint-Dark.webp)SpringConstraint

Simulates spring and damper behavior between two attachments.

---

Summary

Properties

|  |
| --- |
| [Coils](#Coils):[number](/docs/luau/numbers) |
| [CurrentLength](#CurrentLength):[number](/docs/luau/numbers) |
| [Damping](#Damping):[number](/docs/luau/numbers) |
| [FreeLength](#FreeLength):[number](/docs/luau/numbers) |
| [LimitsEnabled](#LimitsEnabled):[boolean](/docs/luau/booleans) |
| [MaxForce](#MaxForce):[number](/docs/luau/numbers) |
| [MaxLength](#MaxLength):[number](/docs/luau/numbers) |
| [MinLength](#MinLength):[number](/docs/luau/numbers) |
| [Radius](#Radius):[number](/docs/luau/numbers) |
| [Stiffness](#Stiffness):[number](/docs/luau/numbers) |
| [Thickness](#Thickness):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A SpringConstraint applies a force to its [Attachments](/docs/reference/engine/classes/Attachment)
based on spring and damper behavior. This constraint, along with a
[CylindricalConstraint](/docs/reference/engine/classes/CylindricalConstraint), is ideal for building vehicle suspension.

Note that if this constraint attaches one part (A) to another part (B)
that is anchored or connected to an anchored part (Z), part A will not
be locally simulated when interacting with a player.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Free Length

[FreeLength](/docs/reference/engine/classes/SpringConstraint#FreeLength) defines the natural resting
length of the spring. If the attachments are further apart than the free
length, they are forced together; if the attachments are closer together than
the free length, they are forced apart.

#### Damping

The [Damping](/docs/reference/engine/classes/SpringConstraint#Damping) value controls how fast the
spring's oscillation dies down. A value of 0 allows the spring to oscillate
endlessly, while higher values bring the spring to a rest more quickly.

#### Stiffness

[Stiffness](/docs/reference/engine/classes/SpringConstraint#Stiffness) sets the strength of the spring.
Higher values create a spring that responds with more force when its
attachments are closer together or further apart than
[FreeLength](/docs/reference/engine/classes/SpringConstraint#FreeLength).

#### Limits

Enabling the [LimitsEnabled](/docs/reference/engine/classes/SpringConstraint#LimitsEnabled) property
exposes the [MinLength](/docs/reference/engine/classes/SpringConstraint#MinLength) and
[MaxLength](/docs/reference/engine/classes/SpringConstraint#MaxLength) values for setting the minimum
and maximum length of the spring. If the spring's attachments reach these
limits, they stop moving apart from one another without restitution.

---

API Reference

Properties

Coils

Read Parallel

The number of coils visualized on the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint).

SpringConstraint.Coils:[number](/docs/luau/numbers)

The number of coils visualized on the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint). This can
only be set between 0 and 8.

Provide feedback

---

CurrentLength

Read Only

Not Replicated

Read Parallel

The current distance between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

SpringConstraint.CurrentLength:[number](/docs/luau/numbers)

The current distance between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

Damping

Read Parallel

Damping constant for the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint). Multiplied to the
velocity of the constraint's [Attachments](/docs/reference/engine/classes/Attachment) to reduce the
spring force applied.

SpringConstraint.Damping:[number](/docs/luau/numbers)

Damping constant for the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint). Multiplied to the
velocity of the constraint's [Attachments](/docs/reference/engine/classes/Attachment) to reduce the
spring force applied.

Provide feedback

---

FreeLength

Read Parallel

Natural resting length of the spring.

SpringConstraint.FreeLength:[number](/docs/luau/numbers)

Natural resting length of the spring.

Provide feedback

---

LimitsEnabled

Read Parallel

Sets whether the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint) enforces a minimum and maximum
length.

SpringConstraint.LimitsEnabled:[boolean](/docs/luau/booleans)

Sets whether the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint) enforces a minimum and maximum
length. If the constraint's [Attachments](/docs/reference/engine/classes/Attachment) reach these
limits, they will simply stop moving apart from one another without
restitution. If you need restitution or elasticity at the ends of the
range of motion, you can combine a [SpringConstraint](/docs/reference/engine/classes/SpringConstraint) with another
constraint that allows restitution at the end of its range, such as a
[PrismaticConstraint](/docs/reference/engine/classes/PrismaticConstraint) or [RopeConstraint](/docs/reference/engine/classes/RopeConstraint).

Provide feedback

---

MaxForce

Read Parallel

The maximum force the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint) can apply on its
[Attachments](/docs/reference/engine/classes/Attachment).

SpringConstraint.MaxForce:[number](/docs/luau/numbers)

The maximum force the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint) can apply on its
[Attachments](/docs/reference/engine/classes/Attachment). Some spring systems can give rise to
forces that grow fast leading to instability. In such cases it is
recommended to set MaxForce to a reasonable value.

Provide feedback

---

MaxLength

Read Parallel

The maximum separation the SpringConstraint will allow if
[LimitsEnabled](/docs/reference/engine/classes/SpringConstraint#LimitsEnabled) is true.

SpringConstraint.MaxLength:[number](/docs/luau/numbers)

The maximum separation the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint) will allow if
[LimitsEnabled](/docs/reference/engine/classes/SpringConstraint#LimitsEnabled) is true.

Provide feedback

---

MinLength

Read Parallel

The minimum separation the SpringConstraint will allow if
[LimitsEnabled](/docs/reference/engine/classes/SpringConstraint#LimitsEnabled) is true.

SpringConstraint.MinLength:[number](/docs/luau/numbers)

The minimum separation the [SpringConstraint](/docs/reference/engine/classes/SpringConstraint) will allow if
[LimitsEnabled](/docs/reference/engine/classes/SpringConstraint#LimitsEnabled) is true.

Provide feedback

---

Radius

Read Parallel

The visualized radius of the spring's coils.

SpringConstraint.Radius:[number](/docs/luau/numbers)

The visualized radius of the spring's coils.

Provide feedback

---

Stiffness

Read Parallel

The strength of the spring. The higher this value the more force will be
applied when the attachments are separated a different length than the
[FreeLength](/docs/reference/engine/classes/SpringConstraint#FreeLength).

SpringConstraint.Stiffness:[number](/docs/luau/numbers)

The strength of the spring. The higher this value the more force will be
applied when the attachments are separated a different length than the
[FreeLength](/docs/reference/engine/classes/SpringConstraint#FreeLength).

Provide feedback

---

Thickness

Read Parallel

The visualized thickness of the spring's coils.

SpringConstraint.Thickness:[number](/docs/luau/numbers)

The visualized thickness of the spring's coils.

Provide feedback

---