# Ray | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Ray
Scraped: 2026-01-11T02:41:44.986498Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Ray](/docs/reference/engine/datatypes/Ray)

English

Feedback

Engine Data Type

Ray

Represents a line with a starting point that casts infinitely in a specific
direction.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(Origin: [Vector3](/docs/reference/engine/datatypes/Vector3),Direction: [Vector3](/docs/reference/engine/datatypes/Vector3)) |

Properties

|  |
| --- |
| [Unit](#Unit):[Ray](/docs/reference/engine/datatypes/Ray) |
| [Origin](#Origin):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Direction](#Direction):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [ClosestPoint](#ClosestPoint)(point: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Distance](#Distance)(point: [Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers) |

The [Ray](/docs/reference/engine/datatypes/Ray) data type represents a half-line, finite in one direction
but infinite in the other. It can be defined by a 3D point, where the line
originates from, and a direction vector, which is the direction it goes in.

---

API Reference

Constructors

new

Returns a [Ray](/docs/reference/engine/datatypes/Ray) with the given Origin and Direction.

Ray.new(

Origin:[Vector3](/docs/reference/engine/datatypes/Vector3), Direction:[Vector3](/docs/reference/engine/datatypes/Vector3) )

Parameters

|  |
| --- |
| Origin:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| Direction:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns a new [Ray](/docs/reference/engine/datatypes/Ray) with given Origin and Direction.

Provide feedback

---

Properties

Unit

The [Ray](/docs/reference/engine/datatypes/Ray) with a normalized direction (the direction has a
magnitude of 1).

Ray.Unit:[Ray](/docs/reference/engine/datatypes/Ray)

The [Ray](/docs/reference/engine/datatypes/Ray) with a normalized direction (the direction has a
magnitude of 1).

Provide feedback

---

Origin

The position of the origin.

Ray.Origin:[Vector3](/docs/reference/engine/datatypes/Vector3)

The position of the origin.

Provide feedback

---

Direction

The direction vector of the [Ray](/docs/reference/engine/datatypes/Ray).

Ray.Direction:[Vector3](/docs/reference/engine/datatypes/Vector3)

The direction vector of the [Ray](/docs/reference/engine/datatypes/Ray).

Provide feedback

---

Methods

ClosestPoint

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) projected onto the ray so that it is within
the [Ray](/docs/reference/engine/datatypes/Ray) line of sight.

Ray:ClosestPoint(point:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| point:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) projected onto the ray so that it is within
the [Ray](/docs/reference/engine/datatypes/Ray) line of sight.

Note: the [Ray](/docs/reference/engine/datatypes/Ray) must be a unit ray for this method to
behave as expected!

Provide feedback

---

Distance

Returns the distance between the given point and the closest point on the
[Ray](/docs/reference/engine/datatypes/Ray).

Ray:Distance(point:[Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| point:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[number](/docs/luau/numbers)

Returns the distance between the given point and the point on the ray
nearest to the given point ([Ray.ClosestPoint(point)](/docs/reference/engine/datatypes/Ray#ClosestPoint)).

Provide feedback

---