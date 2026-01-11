# Path2D | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Path2D
Scraped: 2026-01-11T02:42:04.522074Z

## Tags
- Not Replicated

## Inherits
- GuiBase
- Path2D
- Instance
- Object
- GuiObject.ZIndex
- GetPositionOnCurveArcLength()
- GetPositionOnCurve()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiBase](/docs/reference/engine/classes/GuiBase)
6. /
7. [Path2D](/docs/reference/engine/classes/Path2D)

English

Feedback

Engine Class

![Path2D](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Path2D-Dark.webp)Path2D

---

Summary

Properties

|  |
| --- |
| [Closed](#Closed):[boolean](/docs/luau/booleans) |
| [Color3](#Color3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [SelectedControlPoint](#SelectedControlPoint):[number](/docs/luau/numbers) |
| [SelectedControlPointData](#SelectedControlPointData):[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) |
| [Thickness](#Thickness):[number](/docs/luau/numbers) |
| [Visible](#Visible):[boolean](/docs/luau/booleans) |
| [ZIndex](#ZIndex):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetBoundingRect](#GetBoundingRect)():[Rect](/docs/reference/engine/datatypes/Rect) |
| [GetControlPoint](#GetControlPoint)(index: [number](/docs/luau/numbers)):[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) |
| [GetControlPoints](#GetControlPoints)():[Array](/docs/luau/tables#arrays) |
| [GetLength](#GetLength)():[number](/docs/luau/numbers) |
| [GetMaxControlPoints](#GetMaxControlPoints)():[number](/docs/luau/numbers) |
| [GetPositionOnCurve](#GetPositionOnCurve)(t: [number](/docs/luau/numbers)):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [GetPositionOnCurveArcLength](#GetPositionOnCurveArcLength)(t: [number](/docs/luau/numbers)):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [GetTangentOnCurve](#GetTangentOnCurve)(t: [number](/docs/luau/numbers)):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [GetTangentOnCurveArcLength](#GetTangentOnCurveArcLength)(t: [number](/docs/luau/numbers)):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [InsertControlPoint](#InsertControlPoint)(index: [number](/docs/luau/numbers),point: [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)):() |
| [RemoveControlPoint](#RemoveControlPoint)(index: [number](/docs/luau/numbers)):() |
| [SetControlPoints](#SetControlPoints)(controlPoints: [Array](/docs/luau/tables#arrays)):() |
| [UpdateControlPoint](#UpdateControlPoint)(index: [number](/docs/luau/numbers),point: [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)):() |

Events

|  |
| --- |
| [ControlPointChanged](#ControlPointChanged)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Properties

Closed

Read Parallel

Connects the first and last control points when enabled.

Path2D.Closed:[boolean](/docs/luau/booleans)

Connects the first and last control points when enabled.

Provide feedback

---

Color3

Read Parallel

Determines the Color of the [Path2D](/docs/reference/engine/classes/Path2D).

Path2D.Color3:[Color3](/docs/reference/engine/datatypes/Color3)

Determines the Color of the [Path2D](/docs/reference/engine/classes/Path2D).

Provide feedback

---

SelectedControlPoint

Not Replicated

Roblox Script Security

Read Parallel

Path2D.SelectedControlPoint:[number](/docs/luau/numbers)

Provide feedback

---

SelectedControlPointData

Not Replicated

Roblox Script Security

Read Parallel

Path2D.SelectedControlPointData:[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)

Provide feedback

---

Thickness

Read Parallel

Determines how thick the [Path2D](/docs/reference/engine/classes/Path2D) path is.

Path2D.Thickness:[number](/docs/luau/numbers)

Determines how thick the [Path2D](/docs/reference/engine/classes/Path2D) path is.

Provide feedback

---

Visible

Read Parallel

Determines if the [Path2D](/docs/reference/engine/classes/Path2D) path is rendered or not.

Path2D.Visible:[boolean](/docs/luau/booleans)

Determines if the [Path2D](/docs/reference/engine/classes/Path2D) path is rendered or not. When false, the
path will not render. However, any modifications to the control points
will update correctly, ensuring that querying data will have the correct
info.

Provide feedback

---

ZIndex

Read Parallel

Determines the order in which a [Path2D](/docs/reference/engine/classes/Path2D) path renders relative to
other GUIs.

Path2D.ZIndex:[number](/docs/luau/numbers)

Determines the order in which a [Path2D](/docs/reference/engine/classes/Path2D) path renders relative to
other GUIs. Works the same as [GuiObject.ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) but does not
interact with layout order in any way.

Provide feedback

---

Methods

GetBoundingRect

Returns the bounding size for the [Path2D](/docs/reference/engine/classes/Path2D).

Path2D:GetBoundingRect():[Rect](/docs/reference/engine/datatypes/Rect)

Returns

[Rect](/docs/reference/engine/datatypes/Rect)

Returns the [Rect](/docs/reference/engine/datatypes/Rect) bounding size for the [Path2D](/docs/reference/engine/classes/Path2D). This is
computed based on the control points and is not modifiable outside of
changing the control point data.

Provide feedback

---

GetControlPoint

Returns the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) for a given index.

Path2D:GetControlPoint(index:[number](/docs/luau/numbers)):[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers) |

Returns

[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)

The control point at the given index.

Returns the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) for a given index. If the index
is out of bounds, this method will throw an error.

Provide feedback

---

GetControlPoints

Returns all the [Path2DControlPoints](/docs/reference/engine/datatypes/Path2DControlPoint) for the
[Path2D](/docs/reference/engine/classes/Path2D).

Path2D:GetControlPoints():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Table of all the [Path2DControlPoints](/docs/reference/engine/datatypes/Path2DControlPoint).

Returns a table of all the
[Path2DControlPoints](/docs/reference/engine/datatypes/Path2DControlPoint) for the [Path2D](/docs/reference/engine/classes/Path2D).

Provide feedback

---

GetLength

Returns the length of the [Path2D](/docs/reference/engine/classes/Path2D).

Path2D:GetLength():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the length of the [Path2D](/docs/reference/engine/classes/Path2D). This function can be expensive
if called too frequently.

Provide feedback

---

GetMaxControlPoints

Returns the maximum allowed number of control points.

Path2D:GetMaxControlPoints():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the maximum allowed number of control points.

Provide feedback

---

GetPositionOnCurve

Returns the position at a given value in parameter space.

Path2D:GetPositionOnCurve(t:[number](/docs/luau/numbers)):[UDim2](/docs/reference/engine/datatypes/UDim2)

Parameters

|  |
| --- |
| t:[number](/docs/luau/numbers)  The value to query the [Path2D](/docs/reference/engine/classes/Path2D) at. |

Returns

[UDim2](/docs/reference/engine/datatypes/UDim2)

The position in parameter space.

Returns the 2D [UDim2](/docs/reference/engine/datatypes/UDim2) position at a given t value between 0
and 1 (inclusive), representing the parameter space result of querying the
spline. The values will be more tightly packed near bends and wider apart
in straighter segments; see
[GetPositionOnCurveArcLength()](/docs/reference/engine/classes/Path2D#GetPositionOnCurveArcLength)
for even spacing results.

Throws an error if the [Path2D](/docs/reference/engine/classes/Path2D) has less than two control points.

Provide feedback

---

GetPositionOnCurveArcLength

Returns the position at a given value in arc length space.

Path2D:GetPositionOnCurveArcLength(t:[number](/docs/luau/numbers)):[UDim2](/docs/reference/engine/datatypes/UDim2)

Parameters

|  |
| --- |
| t:[number](/docs/luau/numbers)  The value to query the Path2D at. |

Returns

[UDim2](/docs/reference/engine/datatypes/UDim2)

The position in arc length space.

Returns the 2D [UDim2](/docs/reference/engine/datatypes/UDim2) position at a given t value between 0
and 1 (inclusive), representing the arc length space result of querying
the spline. The values will be evenly spaced along the spline; see
[GetPositionOnCurve()](/docs/reference/engine/classes/Path2D#GetPositionOnCurve) for parameter
spacing results.

Throws an error if the [Path2D](/docs/reference/engine/classes/Path2D) has less than two control points.

Provide feedback

---

GetTangentOnCurve

Returns the tangent at a given value in parameter space.

Path2D:GetTangentOnCurve(t:[number](/docs/luau/numbers)):[Vector2](/docs/reference/engine/datatypes/Vector2)

Parameters

|  |
| --- |
| t:[number](/docs/luau/numbers)  The value to query the [Path2D](/docs/reference/engine/classes/Path2D) at. |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns the tangent at a given t value in parameter space where t is a
value between 0 and 1 (inclusive). Throws an error if the [Path2D](/docs/reference/engine/classes/Path2D)
has less than two control points.

Provide feedback

---

GetTangentOnCurveArcLength

Returns the tangent at a given value in arc length space.

Path2D:GetTangentOnCurveArcLength(t:[number](/docs/luau/numbers)):[Vector2](/docs/reference/engine/datatypes/Vector2)

Parameters

|  |
| --- |
| t:[number](/docs/luau/numbers)  The value to query the [Path2D](/docs/reference/engine/classes/Path2D) at. |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

The tangent in arc length space.

Returns the tangent at a given t value in arc length space where t is
a value between 0 and 1 (inclusive). Throws an error if the [Path2D](/docs/reference/engine/classes/Path2D)
has less than two control points.

Provide feedback

---

InsertControlPoint

Inserts a new control point at a given index.

Path2D:InsertControlPoint(

index:[number](/docs/luau/numbers), point:[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)

):()

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers)  The index to insert at. |
| point:[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)  The control point to insert. |

Returns

()

Inserts a new [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) at a given index. Throws a
warning if the index is out of bounds or if you're trying to add control
points past the limit of 50.

Provide feedback

---

RemoveControlPoint

Removes a control at the given index.

Path2D:RemoveControlPoint(index:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers)  The index to remove at. |

Returns

()

Removes a control point at the given index. Throws a warning if the index
is out of bounds.

Provide feedback

---

SetControlPoints

Sets all the control points to the specified array, replacing all existing
points with new ones.

Path2D:SetControlPoints(controlPoints:[Array](/docs/luau/tables#arrays)):()

Parameters

|  |
| --- |
| controlPoints:[Array](/docs/luau/tables#arrays)  The new list of control points to set. |

Returns

()

Sets all the control points to the specified array, replacing all existing
points with new ones. Throws a warning if there are more than 50 points in
the controlPoints array.

Provide feedback

---

UpdateControlPoint

Updates a control point at the given index.

Path2D:UpdateControlPoint(

index:[number](/docs/luau/numbers), point:[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)

):()

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers)  The control point index to update. |
| point:[Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) |

Returns

()

Updates the control point at the given index. Throws a warning if the
index is out of range.

Provide feedback

---

Events

ControlPointChanged

Fires any time control points change.

Path2D.ControlPointChanged():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires any time control points change.

Provide feedback

---