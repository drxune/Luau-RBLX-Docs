# RodConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RodConstraint
Scraped: 2026-01-11T02:37:24.177842Z

## Tags
- Not Replicated

## Inherits
- Constraint
- RodConstraint
- Length
- Instance
- Object
- LimitsEnabled
- LimitAngle0
- LimitAngle1
- Attachments
- Attachment0
- Attachment1
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [RodConstraint](/docs/reference/engine/classes/RodConstraint)

English

Feedback

Engine Class

![RodConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/RodConstraint-Dark.webp)RodConstraint

Keeps two attachments separated by its defined
[Length](/docs/reference/engine/classes/RodConstraint#Length).

---

Summary

Properties

|  |
| --- |
| [CurrentDistance](#CurrentDistance):[number](/docs/luau/numbers) |
| [Length](#Length):[number](/docs/luau/numbers) |
| [LimitAngle0](#LimitAngle0):[number](/docs/luau/numbers) |
| [LimitAngle1](#LimitAngle1):[number](/docs/luau/numbers) |
| [LimitsEnabled](#LimitsEnabled):[boolean](/docs/luau/booleans) |
| [Thickness](#Thickness):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A RodConstraint keeps two attachments separated by its defined
[Length](/docs/reference/engine/classes/RodConstraint#Length). By default, both attachments can rotate
freely, although you can enable limits to restrict rotational tilt.

Note that if this constraint attaches one part (A) to another part (B)
that is anchored or connected to an anchored part (Z), part A will not
be locally simulated when interacting with a player.

#### Limits

You can limit rotation of the attachments within a cone, independently of each
other, by enabling the [LimitsEnabled](/docs/reference/engine/classes/RodConstraint#LimitsEnabled)
property and setting [LimitAngle0](/docs/reference/engine/classes/RodConstraint#LimitAngle0) and
[LimitAngle1](/docs/reference/engine/classes/RodConstraint#LimitAngle1) respectively.

---

API Reference

Properties

CurrentDistance

Read Only

Not Replicated

Read Parallel

The current distance between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

RodConstraint.CurrentDistance:[number](/docs/luau/numbers)

The current distance between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

Length

Read Parallel

The distance apart at which the constraint attempts to keep its
[Attachments](/docs/reference/engine/classes/Attachment).

RodConstraint.Length:[number](/docs/luau/numbers)

The distance apart at which the constraint attempts to keep its
[Attachments](/docs/reference/engine/classes/Attachment). Measured in studs.

Provide feedback

---

LimitAngle0

Read Parallel

The maximum angle between the rod and
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) when
[LimitsEnabled](/docs/reference/engine/classes/RodConstraint#LimitsEnabled) is true.

RodConstraint.LimitAngle0:[number](/docs/luau/numbers)

This property determines the maximum angle between the rod and
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) when
[LimitsEnabled](/docs/reference/engine/classes/RodConstraint#LimitsEnabled) is true.

Provide feedback

---

LimitAngle1

Read Parallel

The maximum angle between the rod and
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) when
[LimitsEnabled](/docs/reference/engine/classes/RodConstraint#LimitsEnabled) is true.

RodConstraint.LimitAngle1:[number](/docs/luau/numbers)

This property determines the maximum angle between the rod and
[Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) when
[LimitsEnabled](/docs/reference/engine/classes/RodConstraint#LimitsEnabled) is true.

Provide feedback

---

LimitsEnabled

Read Parallel

Determines whether [LimitAngle0](/docs/reference/engine/classes/RodConstraint#LimitAngle0) and
[LimitAngle1](/docs/reference/engine/classes/RodConstraint#LimitAngle1) control the angles between
the rod and the respective attachments.

RodConstraint.LimitsEnabled:[boolean](/docs/luau/booleans)

This property determines whether the
[LimitAngle0](/docs/reference/engine/classes/RodConstraint#LimitAngle0) and
[LimitAngle1](/docs/reference/engine/classes/RodConstraint#LimitAngle1) properties control the
angles between the rod and the respective attachments.

Provide feedback

---

Thickness

Read Parallel

The visualized thickness of the [RodConstraint](/docs/reference/engine/classes/RodConstraint).

RodConstraint.Thickness:[number](/docs/luau/numbers)

The visualized thickness of the [RodConstraint](/docs/reference/engine/classes/RodConstraint).

Provide feedback

---