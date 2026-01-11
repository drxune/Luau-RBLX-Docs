# PrismaticConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PrismaticConstraint
Scraped: 2026-01-11T02:30:37.592066Z

## Inherits
- SlidingBallConstraint
- PrismaticConstraint
- Attachments
- Constraint
- Instance
- Object
- ActuatorType
- LimitsEnabled
- Velocity
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint)
6. /
7. [PrismaticConstraint](/docs/reference/engine/classes/PrismaticConstraint)

English

Feedback

Engine Class

![PrismaticConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/PrismaticConstraint-Dark.webp)PrismaticConstraint

Constraint which creates a rigid joint between two
[Attachments](/docs/reference/engine/classes/Attachment), allowing them to slide along one axis but not
rotate.

---

Summary

Inherited Members

15 inherited from [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint)

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A PrismaticConstraint creates a rigid joint between two
[Attachments](/docs/reference/engine/classes/Attachment), allowing them to slide along one axis but not
rotate. This constrains the attachments so that their X axes are collinear
but pointing in opposite directions. It also constrains the attachments so
that their Y axes are parallel.

This constraint inherits many properties from [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint)
including [ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType),
[LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint#LimitsEnabled),
[Velocity](/docs/reference/engine/classes/SlidingBallConstraint#Velocity), and more. Please refer to
[SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint) for details on configuring a
[PrismaticConstraint](/docs/reference/engine/classes/PrismaticConstraint).

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.