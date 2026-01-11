# ValueCurveKey | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/ValueCurveKey
Scraped: 2026-01-11T02:42:40.489416Z

## Inherits
- ValueCurve
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey)

English

Feedback

Engine Data Type

ValueCurveKey

A time-value pair used with [ValueCurve](/docs/reference/engine/classes/ValueCurve) instances.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(time: [number](/docs/luau/numbers),value: any,Interpolation: [Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)) |

Properties

|  |
| --- |
| [Interpolation](#Interpolation):[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) |
| [Time](#Time):[number](/docs/luau/numbers) |
| [Value](#Value):any |
| [RightTangent](#RightTangent):[number](/docs/luau/numbers) |
| [LeftTangent](#LeftTangent):[number](/docs/luau/numbers) |

A time-value pair used with [ValueCurve](/docs/reference/engine/classes/ValueCurve) instances.

The [Interpolation](/docs/reference/engine/datatypes/ValueCurveKey#Interpolation) property dictates the
interpolation mode for the segment started by this key and ended by the next
key on the curve. Each segment may use a different interpolation mode.

The [LeftTangent](/docs/reference/engine/datatypes/ValueCurveKey#LeftTangent) and
[RightTangent](/docs/reference/engine/datatypes/ValueCurveKey#RightTangent) properties apply to the
cubic interpolation mode and define the desired tangent (slope) at the key.
Different left and right values can be used to encode discontinuities in slope
at the key. Attempting to set a
[RightTangent](/docs/reference/engine/datatypes/ValueCurveKey#RightTangent) value on a key that doesn't
use the cubic interpolation mode will result in a runtime error. It is
possible to set the [LeftTangent](/docs/reference/engine/datatypes/ValueCurveKey#LeftTangent) property
on any key, as it will be used should the preceding segment use cubic
interpolation.

---

API Reference

Constructors

new

Returns a new [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey) from the given time and value.

ValueCurveKey.new(

time:[number](/docs/luau/numbers), value:any, Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) )

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to create the new [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey). |
| value:any  Value of the new [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey). |
| Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode) |

Creates a new [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey) at a given time and value.
[LeftTangent](/docs/reference/engine/datatypes/ValueCurveKey#LeftTangent) and
[RightTangent](/docs/reference/engine/datatypes/ValueCurveKey#RightTangent) are left uninitialized
and, if not initialized, tangent values of '0' will be used when evaluating
the curve.

Provide feedback

---

Properties

Interpolation

The key interpolation mode for the segment started by this
[ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

ValueCurveKey.Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)

Defines this key's interpolation mode for the segment started by this
[ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

Provide feedback

---

Time

The time position of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

ValueCurveKey.Time:[number](/docs/luau/numbers)

The time position of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

Provide feedback

---

Value

The value of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

ValueCurveKey.Value:any

The value of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

Provide feedback

---

RightTangent

The tangent to the right of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

ValueCurveKey.RightTangent:[number](/docs/luau/numbers)

The tangent to the right of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

Provide feedback

---

LeftTangent

The tangent to the left of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

ValueCurveKey.LeftTangent:[number](/docs/luau/numbers)

The tangent to the left of this [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey).

Provide feedback

---