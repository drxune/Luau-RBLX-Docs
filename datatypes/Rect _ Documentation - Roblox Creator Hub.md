# Rect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Rect
Scraped: 2026-01-11T02:42:26.683089Z

## Inherits
- ImageLabel.SliceCenter
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Rect](/docs/reference/engine/datatypes/Rect)

English

Feedback

Engine Data Type

Rect

A value that represents a two-dimensional rectangle.

---

Summary

Constructors

|  |
| --- |
| [new](#new)() |
| [new](#new-min-max)(min: [Vector2](/docs/reference/engine/datatypes/Vector2),max: [Vector2](/docs/reference/engine/datatypes/Vector2)) |
| [new](#new-minX-minY)(minX: [number](/docs/luau/numbers),minY: [number](/docs/luau/numbers),maxX: [number](/docs/luau/numbers),maxY: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [Width](#Width):[number](/docs/luau/numbers) |
| [Height](#Height):[number](/docs/luau/numbers) |
| [Min](#Min):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Max](#Max):[Vector2](/docs/reference/engine/datatypes/Vector2) |

Rect describes a rectangle on a 2D plane. It is constructed using two
corners, either two [Vector2](/docs/reference/engine/datatypes/Vector2) positions or four numbers:

```
local rect1 = Rect.new(Vector2.new(10, 10), Vector2.new(80, 80))



local rect2 = Rect.new(10, 10, 80, 80)
```

This data type is used in the [ImageLabel.SliceCenter](/docs/reference/engine/classes/ImageLabel#SliceCenter) property which
determines the center area of a scaled image.

---

API Reference

Constructors

new

Returns a new Rect with zero [Vector2](/docs/reference/engine/datatypes/Vector2) positions.

Rect.new()

Constructs a new Rect with two zero [Vector2](/docs/reference/engine/datatypes/Vector2) positions.

Provide feedback

---

new

Returns a new Rect from the given [Vector2](/docs/reference/engine/datatypes/Vector2) positions.

Rect.new(

min:[Vector2](/docs/reference/engine/datatypes/Vector2), max:[Vector2](/docs/reference/engine/datatypes/Vector2) )

Parameters

|  |
| --- |
| min:[Vector2](/docs/reference/engine/datatypes/Vector2) |
| max:[Vector2](/docs/reference/engine/datatypes/Vector2) |

Constructs a new Rect given two [Vector2](/docs/reference/engine/datatypes/Vector2) positions: min as
the top-left corner and max as the bottom-right corner.

Provide feedback

---

new

Returns a new Rect using the first and last two arguments as
coordinates for corners.

Rect.new(

minX:[number](/docs/luau/numbers), minY:[number](/docs/luau/numbers), maxX:[number](/docs/luau/numbers), maxY:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| minX:[number](/docs/luau/numbers) |
| minY:[number](/docs/luau/numbers) |
| maxX:[number](/docs/luau/numbers) |
| maxY:[number](/docs/luau/numbers) |

Constructs a new Rect using minX and minY as coordinates for the
top-left corner, and maxX and maxY as coordinates for the bottom-right
corner.

Provide feedback

---

Properties

Width

The width of the Rect.

Rect.Width:[number](/docs/luau/numbers)

The width of the Rect in pixels.

Provide feedback

---

Height

The height of the Rect.

Rect.Height:[number](/docs/luau/numbers)

The height of the Rect in pixels.

Provide feedback

---

Min

The coordinates of the top-left corner.

Rect.Min:[Vector2](/docs/reference/engine/datatypes/Vector2)

The top-left corner.

Provide feedback

---

Max

The coordinates of the bottom-right corner.

Rect.Max:[Vector2](/docs/reference/engine/datatypes/Vector2)

The bottom-right corner.

Provide feedback

---