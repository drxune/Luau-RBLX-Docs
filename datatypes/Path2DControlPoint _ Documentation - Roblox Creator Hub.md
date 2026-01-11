# Path2DControlPoint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Path2DControlPoint
Scraped: 2026-01-11T02:41:57.045246Z

## Inherits
- Path2D
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint)

English

Feedback

Engine Data Type

Path2DControlPoint

Stores the info for a single control point used with the [Path2D](/docs/reference/engine/classes/Path2D)
instance.

---

Summary

Constructors

|  |
| --- |
| [new](#new)() |
| [new](#new-Position)(Position: [UDim2](/docs/reference/engine/datatypes/UDim2)) |
| [new](#new-Position-L)(Position: [UDim2](/docs/reference/engine/datatypes/UDim2),Left Tangent: [UDim2](/docs/reference/engine/datatypes/UDim2),Right Tangent: [UDim2](/docs/reference/engine/datatypes/UDim2)) |

Properties

|  |
| --- |
| [Position](#Position):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [LeftTangent](#LeftTangent):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [RightTangent](#RightTangent):[UDim2](/docs/reference/engine/datatypes/UDim2) |

The Path2DControlPoint data type represents a single control point used
with the [Path2D](/docs/reference/engine/classes/Path2D) instance.

---

API Reference

Constructors

new

Returns an empty [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Path2DControlPoint.new()

Returns an empty [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Provide feedback

---

new

Returns a [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) with only the position set.

Path2DControlPoint.new(Position:[UDim2](/docs/reference/engine/datatypes/UDim2))

Parameters

|  |
| --- |
| Position:[UDim2](/docs/reference/engine/datatypes/UDim2)  The [UDim2](/docs/reference/engine/datatypes/UDim2) position of the control point. |

Returns a [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) with the position set. This
constructor will set the tangents to default [UDim2](/docs/reference/engine/datatypes/UDim2) values.

Provide feedback

---

new

Returns a [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) with the position, left
tangent, and right tangent set.

Path2DControlPoint.new(

Position:[UDim2](/docs/reference/engine/datatypes/UDim2), Left Tangent:[UDim2](/docs/reference/engine/datatypes/UDim2), Right Tangent:[UDim2](/docs/reference/engine/datatypes/UDim2) )

Parameters

|  |
| --- |
| Position:[UDim2](/docs/reference/engine/datatypes/UDim2)  The [UDim2](/docs/reference/engine/datatypes/UDim2) position of the control point. |
| Left Tangent:[UDim2](/docs/reference/engine/datatypes/UDim2)  The [UDim2](/docs/reference/engine/datatypes/UDim2) left tangent of the control point. |
| Right Tangent:[UDim2](/docs/reference/engine/datatypes/UDim2)  The [UDim2](/docs/reference/engine/datatypes/UDim2) right tangent of the control point. |

Returns a [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint) with the position, left
tangent, and right tangent set.

Provide feedback

---

Properties

Position

The position of the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Path2DControlPoint.Position:[UDim2](/docs/reference/engine/datatypes/UDim2)

The position of the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Provide feedback

---

LeftTangent

The left tangent of the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Path2DControlPoint.LeftTangent:[UDim2](/docs/reference/engine/datatypes/UDim2)

The left tangent of the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Provide feedback

---

RightTangent

The right tangent of the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Path2DControlPoint.RightTangent:[UDim2](/docs/reference/engine/datatypes/UDim2)

The right tangent of the [Path2DControlPoint](/docs/reference/engine/datatypes/Path2DControlPoint).

Provide feedback

---