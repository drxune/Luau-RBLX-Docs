# RotateP | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RotateP
Scraped: 2026-01-11T02:30:36.613432Z

## Inherits
- DynamicRotate
- RotateP
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
7. [RotateP](/docs/reference/engine/classes/RotateP)

English

Feedback

Engine Class

RotateP

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

A RotateP object joins two parts together and allows rotation about a set
axis. The joint will attempt to rotate the two parts until a desired
rotational position is reached. This object is most commonly created by the
[Enum.SurfaceType.SteppingMotor](/docs/reference/engine/enums/SurfaceType#SteppingMotor) on a [BasePart](/docs/reference/engine/classes/BasePart). If created through a
script, behavior is still governed by the surface input of
[JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0).

The three inputs of note are as follows:

* NoInput — The joint will not rotate under its own power. It can
  still be rotated by external forces (such as from a character pushing one of
  the parts).
* Constant — The joint will rotate based on the ParamB property of
  [JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0). This rotation is measured in radians per
  physics frame (which is approximately 1/60th of a second).
* Sin — The joint will rotate based on the ParamA and ParamB
  properties of [JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0).