# RotationCurveKey | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/RotationCurveKey
Scraped: 2026-01-11T02:42:01.940423Z

## Inherits
- RotationCurve
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey)

English

Feedback

Engine Data Type

RotationCurveKey

A time-value pair used with [RotationCurve](/docs/reference/engine/classes/RotationCurve) instances.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(time: [number](/docs/luau/numbers),cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),Interpolation: [Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)) |

Properties

|  |
| --- |
| [Interpolation](#Interpolation):[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) |
| [Time](#Time):[number](/docs/luau/numbers) |
| [Value](#Value):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [RightTangent](#RightTangent):[number](/docs/luau/numbers) |
| [LeftTangent](#LeftTangent):[number](/docs/luau/numbers) |

A time-value pair used with [RotationCurve](/docs/reference/engine/classes/RotationCurve) instances.

The [Interpolation](/docs/reference/engine/datatypes/RotationCurveKey#Interpolation) property dictates
the interpolation mode for the segment started by this key and ended by the
next key on the curve. Each segment may use a different interpolation mode.

The [LeftTangent](/docs/reference/engine/datatypes/RotationCurveKey#LeftTangent) and
[RightTangent](/docs/reference/engine/datatypes/RotationCurveKey#RightTangent) properties apply to the
cubic interpolation mode and define the desired tangent (slope) at the key.
Different left and right values can be used to encode discontinuities in slope
at the key. Attempting to set a
[RightTangent](/docs/reference/engine/datatypes/RotationCurveKey#RightTangent) value on a key that
doesn't use the cubic interpolation mode will result in a runtime error. It is
possible to set the [LeftTangent](/docs/reference/engine/datatypes/RotationCurveKey#LeftTangent)
property on any key, as it will be used should the preceding segment use cubic
interpolation.

---

API Reference

Constructors

new

Returns a new [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey) at a given time with a given
[CFrame](/docs/reference/engine/datatypes/CFrame).

RotationCurveKey.new(

time:[number](/docs/luau/numbers), cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) )

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to create the new [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey). |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  [CFrame](/docs/reference/engine/datatypes/CFrame) of the new [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey). |
| Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) |

Creates a new [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey) at a given time with a given
[CFrame](/docs/reference/engine/datatypes/CFrame). [LeftTangent](/docs/reference/engine/datatypes/RotationCurveKey#LeftTangent) and
[RightTangent](/docs/reference/engine/datatypes/RotationCurveKey#RightTangent) are left
uninitialized and, if not initialized, tangent values of 0 will be used
when evaluating the curve.

Provide feedback

---

Properties

Interpolation

The key interpolation mode for the segment started by this
[RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

RotationCurveKey.Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)

Defines the key interpolation mode for the segment started by this
[RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

Provide feedback

---

Time

The time position of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

RotationCurveKey.Time:[number](/docs/luau/numbers)

The time position of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

Provide feedback

---

Value

The [CFrame](/docs/reference/engine/datatypes/CFrame) value of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

RotationCurveKey.Value:[CFrame](/docs/reference/engine/datatypes/CFrame)

The [CFrame](/docs/reference/engine/datatypes/CFrame) value of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

Provide feedback

---

RightTangent

The tangent to the right of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

RotationCurveKey.RightTangent:[number](/docs/luau/numbers)

The tangent to the right of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

Provide feedback

---

LeftTangent

The tangent to the left of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

RotationCurveKey.LeftTangent:[number](/docs/luau/numbers)

The tangent to the left of this [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey).

Provide feedback

---