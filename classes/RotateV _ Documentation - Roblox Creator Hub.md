# RotateV | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RotateV
Scraped: 2026-01-11T02:32:55.327700Z

## Inherits
- DynamicRotate
- RotateV
- HingeConstraint
- JointInstance
- Instance
- Object
- BasePart
- JointInstance.Part0
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [DynamicRotate](/docs/reference/engine/classes/DynamicRotate)
6. /
7. [RotateV](/docs/reference/engine/classes/RotateV)

English

Feedback

Engine Class

RotateV

Deprecated

This class works alongside the deprecated [Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) and should not be
used for future work; use [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) instead.

---

Summary

Inherited Members

1 inherited from [DynamicRotate](/docs/reference/engine/classes/DynamicRotate)

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A RotateV object joins two parts together and allows rotation about a set
axis. This object is most commonly created by the [Enum.SurfaceType.Motor](/docs/reference/engine/enums/SurfaceType#Motor) on
a [BasePart](/docs/reference/engine/classes/BasePart). If created through a script, behavior is still governed by
the surface input of [JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0).

The three inputs of note are as follows:

* NoInput — The joint will not rotate under its own power. It can
  still be rotated by external forces (such as from a character pushing one of
  the parts).
* Constant — The joint will rotate based on the ParamB property of
  [JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0). This rotation is measured in radians per
  physics frame (which is approximately 1/60th of a second).
* Sin — The joint will rotate based on the ParamA and ParamB
  properties of [JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0).