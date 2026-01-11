# Rotate | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Rotate
Scraped: 2026-01-11T02:30:42.737534Z

## Inherits
- JointInstance
- Rotate
- HingeConstraint
- Instance
- Object
- BasePart
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [JointInstance](/docs/reference/engine/classes/JointInstance)
6. /
7. [Rotate](/docs/reference/engine/classes/Rotate)

English

Feedback

Engine Class

![Rotate](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Rotate-Dark.webp)Rotate

Deprecated

This class works alongside the deprecated [Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) and should not be
used for future work; use [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) instead.

---

Summary

Inherited Members

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Rotate object is used to allow rotation between two parts. Most
commonly created through the [Enum.SurfaceType.Hinge](/docs/reference/engine/enums/SurfaceType#Hinge) on a [BasePart](/docs/reference/engine/classes/BasePart).
If created like this, the rotation will be about the normal vector from the
face of the part the hinge is placed on. If created through a script, the axis
and point of rotation can be defined arbitrarily.