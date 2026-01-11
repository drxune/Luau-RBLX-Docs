# CompositeValueCurve | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CompositeValueCurve
Scraped: 2026-01-11T02:29:18.969449Z

## Inherits
- Instance
- CompositeValueCurve
- FloatCurves
- Object
- CurveType
- GetComponentCurves()
- GetValueAtTime()
- FloatCurve
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve)

English

Feedback

Engine Class

CompositeValueCurve

An animation curve that groups child [FloatCurves](/docs/reference/engine/classes/FloatCurve) which each
animate a different component of a non-unary value.

---

Summary

Properties

|  |
| --- |
| [CurveType](#CurveType):[Enum.CompositeValueCurveType](/docs/reference/engine/enums/CompositeValueCurveType) |

Methods

|  |
| --- |
| [GetValueAtTime](#GetValueAtTime)(time: [number](/docs/luau/numbers)):Variant |
| [GetComponentCurves](#GetComponentCurves)():Instances |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An animation curve that groups child [FloatCurves](/docs/reference/engine/classes/FloatCurve) which each
animate a different component of a non-unary value. The
[CurveType](/docs/reference/engine/classes/CompositeValueCurve#CurveType) property specifies the type of
value to be animated and, depending on this value, differently named children
are used to drive the animation of the components of the value.

As follows are the names of the child curves that drive the animation for each
possible [Enum.CompositeValueCurveType](/docs/reference/engine/enums/CompositeValueCurveType) value for
[CurveType](/docs/reference/engine/classes/CompositeValueCurve#CurveType):

* [ColorRGB](/docs/reference/engine/enums/CompositeValueCurveType#ColorRGB): { "R", "G", "B" }
* [ColorHSV](/docs/reference/engine/enums/CompositeValueCurveType#ColorHSV): { "H", "S", "V" }
* [NumberRange](/docs/reference/engine/enums/CompositeValueCurveType#NumberRange): { "Min", "Max" }
* [Rect](/docs/reference/engine/enums/CompositeValueCurveType#Rect): { "MinX", "MaxX", "MinY",
  "MaxY" }
* [UDim](/docs/reference/engine/enums/CompositeValueCurveType#UDim): { "Scale", "Offset" }
* [UDim2](/docs/reference/engine/enums/CompositeValueCurveType#UDim2): { "ScaleX", "OffsetX",
  "ScaleY", "OffsetY" }
* [Vector2](/docs/reference/engine/enums/CompositeValueCurveType#Vector2): { "X", "Y"}
* [Vector3](/docs/reference/engine/enums/CompositeValueCurveType#Vector3): { "X", "Y", "Z" }

The children that drive the animation can be accessed via the
[GetComponentCurves()](/docs/reference/engine/classes/CompositeValueCurve#GetComponentCurves) method
which returns an array of curves in the order specified above. The value of
the curve at a given time in the animation may be sampled by the
[GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime) method.

---

API Reference

Properties

CurveType

Read Parallel

The type of value animated by this [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve).

CompositeValueCurve.CurveType:[Enum.CompositeValueCurveType](/docs/reference/engine/enums/CompositeValueCurveType)

The type of value animated by this [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve). See
[Enum.CompositeValueCurveType](/docs/reference/engine/enums/CompositeValueCurveType) for options.

Provide feedback

---

Methods

GetValueAtTime

Returns the sampled animated value at the passed time argument.

CompositeValueCurve:GetValueAtTime(time:[number](/docs/luau/numbers)):Variant

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to get the value. |

Returns

Variant

The value of the curve at the passed time.

This method returns the sampled animated value at the passed time
argument. The type of the returned value will match that specified by the
[CurveType](/docs/reference/engine/classes/CompositeValueCurve#CurveType) property.

If any child curve is missing from the children of the curve, the
corresponding value in the returned property will be 0. For example, if
a curve has a [CurveType](/docs/reference/engine/classes/CompositeValueCurve#CurveType) of
[Enum.CompositeValueCurveType.ColorRGB](/docs/reference/engine/enums/CompositeValueCurveType#ColorRGB) but only one [FloatCurve](/docs/reference/engine/classes/FloatCurve)
child named "G", then the returned [FloatCurve](/docs/reference/engine/classes/FloatCurve) will have values
of 0 for "R" and "B", but the "G" value will be sampled from the
child curve.

Provide feedback

---

GetComponentCurves

Returns the child curves with the given names for the
[CurveType](/docs/reference/engine/classes/CompositeValueCurve#CurveType) of this
[CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve).

CompositeValueCurve:GetComponentCurves():Instances

Returns

Instances

This method returns the child curves with the given names for the
[CurveType](/docs/reference/engine/classes/CompositeValueCurve#CurveType) of this
[CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve), in the order given by the list of child
curves outlined at the top of this page. Any curve that does not exist
prior to calling this method will be created and added as a child with the
appropriate name. That new curve will be an empty [FloatCurve](/docs/reference/engine/classes/FloatCurve).

Provide feedback

---