# RaycastResult | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/RaycastResult
Scraped: 2026-01-11T02:41:50.673102Z

## Inherits
- BasePart
- WorldRoot:Raycast()
- Terrain
- BasePart.Material
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [RaycastResult](/docs/reference/engine/datatypes/RaycastResult)

English

Feedback

Engine Data Type

RaycastResult

Stores results from a raycast operation.

---

Summary

Properties

|  |
| --- |
| [Distance](#Distance):[number](/docs/luau/numbers) |
| [Instance](#Instance):[BasePart](/docs/reference/engine/classes/BasePart) |
| [Material](#Material):[Enum.Material](/docs/reference/engine/enums/Material) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Normal](#Normal):[Vector3](/docs/reference/engine/datatypes/Vector3) |

The [RaycastResult](/docs/reference/engine/datatypes/RaycastResult) data type stores the result of a successful
raycasting operation performed by [WorldRoot:Raycast()](/docs/reference/engine/classes/WorldRoot#Raycast). It contains the
properties listed below.

This object should not be confused with the similarly-named
[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) which is used to perform a raycast.

---

API Reference

Properties

Distance

The distance between the ray origin and the intersection point.

RaycastResult.Distance:[number](/docs/luau/numbers)

The distance between the ray origin and the intersection point.

Provide feedback

---

Instance

The [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell that the ray intersected.

RaycastResult.Instance:[BasePart](/docs/reference/engine/classes/BasePart)

The [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell that the ray intersected.

Provide feedback

---

Material

The [Enum.Material](/docs/reference/engine/enums/Material) at the intersection point.

RaycastResult.Material:[Enum.Material](/docs/reference/engine/enums/Material)

The [Enum.Material](/docs/reference/engine/enums/Material) at the intersection point. For normal parts this is
the [BasePart.Material](/docs/reference/engine/classes/BasePart#Material); for [Terrain](/docs/reference/engine/classes/Terrain) this can vary depending
on terrain data.

Provide feedback

---

Position

The world space point at which the intersection occurred.

RaycastResult.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

The world space point at which the intersection occurred, usually a point
directly on the surface of the [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell.

Provide feedback

---

Normal

The normal vector of the intersected face.

RaycastResult.Normal:[Vector3](/docs/reference/engine/datatypes/Vector3)

The normal vector of the intersected face.

Provide feedback

---