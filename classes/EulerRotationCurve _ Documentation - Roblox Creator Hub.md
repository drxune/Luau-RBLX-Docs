# EulerRotationCurve | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/EulerRotationCurve
Scraped: 2026-01-11T02:32:46.249080Z

## Inherits
- Instance
- EulerRotationCurve
- FloatCurves
- FloatCurve
- Object
- EulerRotationCurve:X()
- EulerRotationCurve:Y()
- EulerRotationCurve:Z()
- EulerRotationCurve:GetAnglesAtTime()
- EulerRotationCurve:GetRotationAtTime()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [EulerRotationCurve](/docs/reference/engine/classes/EulerRotationCurve)

English

Feedback

Engine Class

EulerRotationCurve

Represents a 3D rotation curve through a group of three
[FloatCurves](/docs/reference/engine/classes/FloatCurve).

---

Summary

Properties

|  |
| --- |
| [RotationOrder](#RotationOrder):[Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder) |

Methods

|  |
| --- |
| [GetAnglesAtTime](#GetAnglesAtTime)(time: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetRotationAtTime](#GetRotationAtTime)(time: [number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [X](#X)():[FloatCurve](/docs/reference/engine/classes/FloatCurve) |
| [Y](#Y)():[FloatCurve](/docs/reference/engine/classes/FloatCurve) |
| [Z](#Z)():[FloatCurve](/docs/reference/engine/classes/FloatCurve) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A EulerRotationCurve represents a 3D rotation curve through a group of
three [FloatCurves](/docs/reference/engine/classes/FloatCurve). The rotation is decomposed in three
Euler angles channels that can be accessed via [EulerRotationCurve:X()](/docs/reference/engine/classes/EulerRotationCurve#X),
[EulerRotationCurve:Y()](/docs/reference/engine/classes/EulerRotationCurve#Y), and [EulerRotationCurve:Z()](/docs/reference/engine/classes/EulerRotationCurve#Z). The three
axes can be sampled simultaneously via
[EulerRotationCurve:GetAnglesAtTime()](/docs/reference/engine/classes/EulerRotationCurve#GetAnglesAtTime), returning the three Euler angles
as a [Vector3](/docs/reference/engine/datatypes/Vector3). Similarly,
[EulerRotationCurve:GetRotationAtTime()](/docs/reference/engine/classes/EulerRotationCurve#GetRotationAtTime) samples all channels
simultaneously but returns a [CFrame](/docs/reference/engine/datatypes/CFrame) rotated by X, Y, and Z
according to the specified rotation order.

---

API Reference

Properties

RotationOrder

Read Parallel

Euler angles rotation order.

EulerRotationCurve.RotationOrder:[Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder)

Euler angles rotation order

Provide feedback

---

Methods

GetAnglesAtTime

Samples the three [FloatCurves](/docs/reference/engine/classes/FloatCurve) (X, Y, Z) at the
passed time argument and returns the result as three Euler angles.

EulerRotationCurve:GetAnglesAtTime(time:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers) |

Returns

[Array](/docs/luau/tables#arrays)

Samples the three [FloatCurves](/docs/reference/engine/classes/FloatCurve) (X, Y, Z) at the
passed time argument and returns the result as three Euler angles. If a
channel curve is missing or no key is found in the curve, the channel is
evaluated as nil.

Provide feedback

---

GetRotationAtTime

Samples the [EulerRotationCurve](/docs/reference/engine/classes/EulerRotationCurve) at a given time and returns the
corresponding rotation.

EulerRotationCurve:GetRotationAtTime(time:[number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers) |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Samples the [EulerRotationCurve](/docs/reference/engine/classes/EulerRotationCurve) at a given time and returns the
corresponding rotation. Empty Euler angles channels are interpreted as
zero.

Provide feedback

---

X

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the X Euler angle channel.

EulerRotationCurve:X():[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns

[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the X Euler angle channel. It
is the first child instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named X. If none
is found, an empty [FloatCurve](/docs/reference/engine/classes/FloatCurve) is created.

Provide feedback

---

Y

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Y Euler angle channel.

EulerRotationCurve:Y():[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns

[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Y Euler angle channel. It
is the first child instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named Y. If none
is found, an empty [FloatCurve](/docs/reference/engine/classes/FloatCurve) is created.

Provide feedback

---

Z

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Z Euler angle channel.

EulerRotationCurve:Z():[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns

[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Z Euler angle channel. It
is the first child instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named Z. If none
is found, an empty [FloatCurve](/docs/reference/engine/classes/FloatCurve) is created.

Provide feedback

---