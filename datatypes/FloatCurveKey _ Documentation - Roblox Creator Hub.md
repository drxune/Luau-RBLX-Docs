# FloatCurveKey | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/FloatCurveKey
Scraped: 2026-01-11T02:42:17.476998Z

## Inherits
- FloatCurve
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey)

English

Feedback

Engine Data Type

FloatCurveKey

A time-value pair used with [FloatCurve](/docs/reference/engine/classes/FloatCurve) instances.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(time: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers),Interpolation: [Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)) |

Properties

|  |
| --- |
| [Interpolation](#Interpolation):[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) |
| [Time](#Time):[number](/docs/luau/numbers) |
| [Value](#Value):[number](/docs/luau/numbers) |
| [RightTangent](#RightTangent):[number](/docs/luau/numbers) |
| [LeftTangent](#LeftTangent):[number](/docs/luau/numbers) |

A time-value pair used with [FloatCurve](/docs/reference/engine/classes/FloatCurve) instances.

The [Interpolation](/docs/reference/engine/datatypes/FloatCurveKey#Interpolation) property dictates the
interpolation mode for the segment started by this key and ended by the next
key on the curve. Each segment may use a different interpolation mode.

The [LeftTangent](/docs/reference/engine/datatypes/FloatCurveKey#LeftTangent) and
[RightTangent](/docs/reference/engine/datatypes/FloatCurveKey#RightTangent) properties apply to the
cubic interpolation mode and define the desired tangent (slope) at the key.
Different left and right values can be used to encode discontinuities in slope
at the key. Attempting to set a
[RightTangent](/docs/reference/engine/datatypes/FloatCurveKey#RightTangent) value on a key that doesn't
use the cubic interpolation mode will result in a runtime error. It is
possible to set the [LeftTangent](/docs/reference/engine/datatypes/FloatCurveKey#LeftTangent) property
on any key, as it will be used should the preceding segment use cubic
interpolation.

---

API Reference

Constructors

new

Returns a new [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey) from the given time and value.

FloatCurveKey.new(

time:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers), Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) )

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to create the new [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey). |
| value:[number](/docs/luau/numbers)  Value of the new [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey). |
| Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) |

Creates a new [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey) at a given time and value.
[LeftTangent](/docs/reference/engine/datatypes/FloatCurveKey#LeftTangent) and
[RightTangent](/docs/reference/engine/datatypes/FloatCurveKey#RightTangent) are left uninitialized
and, if not initialized, tangent values of 0 will be used when evaluating
the curve.

Provide feedback

---

Properties

Interpolation

The key interpolation mode for the segment started by this
[FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

FloatCurveKey.Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)

Defines this key interpolation mode for the segment started by this
[FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

Provide feedback

---

Time

The time position of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

FloatCurveKey.Time:[number](/docs/luau/numbers)

The time position of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

Provide feedback

---

Value

The value of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

FloatCurveKey.Value:[number](/docs/luau/numbers)

The value of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

Provide feedback

---

RightTangent

The tangent to the right of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

FloatCurveKey.RightTangent:[number](/docs/luau/numbers)

The tangent to the right of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

Provide feedback

---

LeftTangent

The tangent to the left of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

FloatCurveKey.LeftTangent:[number](/docs/luau/numbers)

The tangent to the left of this [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey).

Provide feedback

---