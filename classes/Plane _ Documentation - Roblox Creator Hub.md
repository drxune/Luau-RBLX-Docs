# Plane | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Plane
Scraped: 2026-01-11T02:28:06.353652Z

## Inherits
- PlaneConstraint
- Plane
- Constraint
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PlaneConstraint](/docs/reference/engine/classes/PlaneConstraint)
6. /
7. [Plane](/docs/reference/engine/classes/Plane)

English

Feedback

Engine Class

![Plane](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Plane-Dark.webp)Plane

Deprecated

Constrains Attachment0 and Attachment1 such that both points lie in a plane
with origin at Attachment0's position and unit normal vector equal to
Attachment0's primary axis.

---

Summary

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Constrains Attachment0 and Attachment1 such that both points lie in a plane
defined by Attachment0. The plane origin is at Attachment0 and the plane unit
normal is the primary axis of Attachment0. This means that Attachment0 and
Attachment1 will move to a position/orientation such that the distance between
Attachment1 and Attachment0, projected onto the Plane unit normal, is zero.