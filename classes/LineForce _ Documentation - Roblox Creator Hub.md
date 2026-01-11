# LineForce | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LineForce
Scraped: 2026-01-11T02:30:24.033480Z

## Inherits
- Constraint
- LineForce
- Attachments
- Instance
- Object
- ApplyAtCenterOfMass
- InverseSquareLaw
- MaxForce
- Attachment0
- Attachment1
- ReactionForceEnabled
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [LineForce](/docs/reference/engine/classes/LineForce)

English

Feedback

Engine Class

![LineForce](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/LineForce-Dark.webp)LineForce

Applies a force along the theoretical line connecting its two
[Attachments](/docs/reference/engine/classes/Attachment).

---

Summary

Properties

|  |
| --- |
| [ApplyAtCenterOfMass](#ApplyAtCenterOfMass):[boolean](/docs/luau/booleans) |
| [InverseSquareLaw](#InverseSquareLaw):[boolean](/docs/luau/booleans) |
| [Magnitude](#Magnitude):[number](/docs/luau/numbers) |
| [MaxForce](#MaxForce):[number](/docs/luau/numbers) |
| [ReactionForceEnabled](#ReactionForceEnabled):[boolean](/docs/luau/booleans) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The LineForce constraint applies a force along the theoretical line
connecting its two [Attachments](/docs/reference/engine/classes/Attachment). As the end points
(attachments) move, the direction of force will change accordingly.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Force Location

By default, force is applied to either parent at its attachment location. If
desired, force can be focused at each parent's center of mass by enabling
[ApplyAtCenterOfMass](/docs/reference/engine/classes/LineForce#ApplyAtCenterOfMass).

#### Inverse Square Law

When [InverseSquareLaw](/docs/reference/engine/classes/LineForce#InverseSquareLaw) is true, the force
magnitude is multiplied by the inverse square of the distance, meaning the
force will increase exponentially as the two attachments get closer together,
like magnets. When using this setting, it's recommended that you set a
[MaxForce](/docs/reference/engine/classes/LineForce#MaxForce) threshold to prevent infinite force if the
attachments align precisely.

#### Reactionary Force

By default, the constraint only applies force to
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0), while
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) remains unaffected. However, force
can be applied to both attachments in equal and opposite directions by
enabling [ReactionForceEnabled](/docs/reference/engine/classes/LineForce#ReactionForceEnabled).

---

API Reference

Properties

ApplyAtCenterOfMass

Read Parallel

Whether force is applied at the center of mass of the parent assembly.

LineForce.ApplyAtCenterOfMass:[boolean](/docs/luau/booleans)

When true, force is applied at the center of mass of the parent assembly
of [Attachment0](/docs/reference/engine/classes/LineForce#Attachment0), and the line determining the
direction of the force will start at the said center of mass. When
false, force is applied at [Attachment0](/docs/reference/engine/classes/LineForce#Attachment0) and
the line determining the direction will also start at
[Attachment0](/docs/reference/engine/classes/LineForce#Attachment0).

Provide feedback

---

InverseSquareLaw

Read Parallel

When true, the force magnitude is multiplied by the inverse square of
the distance.

LineForce.InverseSquareLaw:[boolean](/docs/luau/booleans)

When true, the force magnitude is multiplied by the inverse square of
the distance.

Provide feedback

---

Magnitude

Read Parallel

The magnitude of the force.

LineForce.Magnitude:[number](/docs/luau/numbers)

The magnitude of the force.

Provide feedback

---

MaxForce

Read Parallel

Maximum absolute force that can be applied.

LineForce.MaxForce:[number](/docs/luau/numbers)

The maximum absolute force that can be applied. This property is enabled
only when [InverseSquareLaw](/docs/reference/engine/classes/LineForce#InverseSquareLaw) is also
enabled. This property is mainly used to address the issue that the force
of the body mover becomes infinite the closer the two attachments are,
causing explosions that can't be prevented by scripts. This property
bounds the force's absolute value.

Provide feedback

---

ReactionForceEnabled

Read Parallel

Enables an equal and opposite reaction force on the parent of
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1).

LineForce.ReactionForceEnabled:[boolean](/docs/luau/booleans)

Enables a reaction force (equal an opposite) to be applied to the parent
of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1). By default line force only
applies a force on the parent of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) and uses
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) as the target direction without
any dynamic relationship.

Provide feedback

---