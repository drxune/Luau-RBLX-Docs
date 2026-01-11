# UDim2 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/UDim2
Scraped: 2026-01-11T02:42:02.952613Z

## Inherits
- Size
- Position
- GuiObjects
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [UDim2](/docs/reference/engine/datatypes/UDim2)

English

Feedback

Engine Data Type

UDim2

Represents a two-dimensional value where each dimension is composed of a
relative scale and an absolute offset.

---

Summary

Constructors

|  |
| --- |
| [new](#new)() |
| [new](#new-xScale-xOf)(xScale: [number](/docs/luau/numbers),xOffset: [number](/docs/luau/numbers),yScale: [number](/docs/luau/numbers),yOffset: [number](/docs/luau/numbers)) |
| [new](#new-x-y)(x: [UDim](/docs/reference/engine/datatypes/UDim),y: [UDim](/docs/reference/engine/datatypes/UDim)) |
| [fromScale](#fromScale)(xScale: [number](/docs/luau/numbers),yScale: [number](/docs/luau/numbers)) |
| [fromOffset](#fromOffset)(xOffset: [number](/docs/luau/numbers),yOffset: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [X](#X):[UDim](/docs/reference/engine/datatypes/UDim) |
| [Y](#Y):[UDim](/docs/reference/engine/datatypes/UDim) |
| [Width](#Width):[UDim](/docs/reference/engine/datatypes/UDim) |
| [Height](#Height):[UDim](/docs/reference/engine/datatypes/UDim) |

Methods

|  |
| --- |
| [Lerp](#Lerp)(goal: [UDim2](/docs/reference/engine/datatypes/UDim2),alpha: [number](/docs/luau/numbers)):[UDim2](/docs/reference/engine/datatypes/UDim2) |

Math Operations

|  |
| --- |
| [`UDim2 + UDim2`](#UDim2-+-UDim2) |
| [`UDim2 - UDim2`](#UDim2---UDim2) |

The [UDim2](/docs/reference/engine/datatypes/UDim2) data type represents a two-dimensional value where each
dimension is composed of a relative scale and an absolute offset in pixels. It
is a combination of two [UDim](/docs/reference/engine/datatypes/UDim) data types representing the X and
Y dimensions. The most common usages for [UDim2](/docs/reference/engine/datatypes/UDim2) are setting the
[Size](/docs/reference/engine/classes/GuiObject#Size) and [Position](/docs/reference/engine/classes/GuiObject#Position) of
[GuiObjects](/docs/reference/engine/classes/GuiObject).

```
local guiObject = script.Parent



guiObject.Size = UDim2.new(0, 300, 1, 0)  -- 300 pixels wide; full height of parent



guiObject.Position = UDim2.new(0, 50, 0, 0)  -- 50 pixels from the left
```

---

API Reference

Constructors

new

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) with the coordinates of two zero [UDim](/docs/reference/engine/datatypes/UDim)
components representing each axis.

UDim2.new()

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) with the coordinates of two zero [UDim](/docs/reference/engine/datatypes/UDim)
components representing each axis.

Provide feedback

---

new

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) given the coordinates of the two [UDim](/docs/reference/engine/datatypes/UDim)
components representing each axis.

UDim2.new(

xScale:[number](/docs/luau/numbers), xOffset:[number](/docs/luau/numbers), yScale:[number](/docs/luau/numbers), yOffset:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| xScale:[number](/docs/luau/numbers) Default Value: 0 The X dimension scale. |
| xOffset:[number](/docs/luau/numbers) Default Value: 0 The X dimension offset. |
| yScale:[number](/docs/luau/numbers) Default Value: 0 The Y dimension scale. |
| yOffset:[number](/docs/luau/numbers) Default Value: 0 The Y dimension offset. |

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) given the coordinates of the two [UDim](/docs/reference/engine/datatypes/UDim)
components representing each axis.

Provide feedback

---

new

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) from the given [UDim](/docs/reference/engine/datatypes/UDim) objects representing
the X and Y dimensions, respectively.

UDim2.new(

x:[UDim](/docs/reference/engine/datatypes/UDim), y:[UDim](/docs/reference/engine/datatypes/UDim) )

Parameters

|  |
| --- |
| x:[UDim](/docs/reference/engine/datatypes/UDim) |
| y:[UDim](/docs/reference/engine/datatypes/UDim) |

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) from the given [UDim](/docs/reference/engine/datatypes/UDim) objects representing
the X and Y dimensions, respectively.

Provide feedback

---

fromScale

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) with the given scale components and no offsets.

UDim2.fromScale(

xScale:[number](/docs/luau/numbers), yScale:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| xScale:[number](/docs/luau/numbers) Default Value: 0 |
| yScale:[number](/docs/luau/numbers) Default Value: 0 |

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) with the given scalar coordinates and no offsets.
Equivalent to:

```
UDim2.fromScale(xScale, yScale) == UDim2.new(xScale, 0, yScale, 0)
```

Provide feedback

---

fromOffset

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) with the given offset components and no scaling.

UDim2.fromOffset(

xOffset:[number](/docs/luau/numbers), yOffset:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| xOffset:[number](/docs/luau/numbers) Default Value: 0 |
| yOffset:[number](/docs/luau/numbers) Default Value: 0 |

Returns a new [UDim2](/docs/reference/engine/datatypes/UDim2) with the given offset coordinates and no scaling. Equivalent to:

```
UDim2.fromOffset(xOffset, yOffset) == UDim2.new(0, xOffset, 0, yOffset)
```

Provide feedback

---

Properties

X

The X dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

UDim2.X:[UDim](/docs/reference/engine/datatypes/UDim)

The X dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

Provide feedback

---

Y

The Y dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

UDim2.Y:[UDim](/docs/reference/engine/datatypes/UDim)

The Y dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

Provide feedback

---

Width

The X dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

UDim2.Width:[UDim](/docs/reference/engine/datatypes/UDim)

The X dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

Provide feedback

---

Height

The Y dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

UDim2.Height:[UDim](/docs/reference/engine/datatypes/UDim)

The Y dimension scale and offset of the [UDim2](/docs/reference/engine/datatypes/UDim2).

Provide feedback

---

Methods

Lerp

Returns a [UDim2](/docs/reference/engine/datatypes/UDim2) interpolated linearly between the value and the
given goal.

UDim2:Lerp(

goal:[UDim2](/docs/reference/engine/datatypes/UDim2), alpha:[number](/docs/luau/numbers)

):[UDim2](/docs/reference/engine/datatypes/UDim2)

Parameters

|  |
| --- |
| goal:[UDim2](/docs/reference/engine/datatypes/UDim2) |
| alpha:[number](/docs/luau/numbers) |

Returns

[UDim2](/docs/reference/engine/datatypes/UDim2)

Returns a [UDim2](/docs/reference/engine/datatypes/UDim2) interpolated linearly between this
[UDim2](/docs/reference/engine/datatypes/UDim2) and the given goal. The alpha value should be a
number between 0 and 1.

Provide feedback

---

Math Operations

`UDim2` + `UDim2`

Produces a [UDim2](/docs/reference/engine/datatypes/UDim2) with components that are the sum of the
respective components of the two [UDim2](/docs/reference/engine/datatypes/UDim2) objects.

[UDim2](/docs/reference/engine/datatypes/UDim2) + [UDim2](/docs/reference/engine/datatypes/UDim2) : [UDim2](/docs/reference/engine/datatypes/UDim2)

Produces a [UDim2](/docs/reference/engine/datatypes/UDim2) with components that are the sum of the
respective components of the two [UDim2](/docs/reference/engine/datatypes/UDim2) objects.

Provide feedback

---

`UDim2` - `UDim2`

Produces a [UDim2](/docs/reference/engine/datatypes/UDim2) with components that are the difference of the
respective components of the two [UDim2](/docs/reference/engine/datatypes/UDim2) objects.

[UDim2](/docs/reference/engine/datatypes/UDim2) - [UDim2](/docs/reference/engine/datatypes/UDim2) : [UDim2](/docs/reference/engine/datatypes/UDim2)

Produces a [UDim2](/docs/reference/engine/datatypes/UDim2) with components that are the difference of the
respective components of the two [UDim2](/docs/reference/engine/datatypes/UDim2) objects.

Provide feedback

---