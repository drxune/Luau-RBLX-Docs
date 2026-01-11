# UDim | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/UDim
Scraped: 2026-01-11T02:42:31.947653Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [UDim](/docs/reference/engine/datatypes/UDim)

English

Feedback

Engine Data Type

UDim

Represents a one-dimensional value with two components, a relative scale and
an absolute offset.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(Scale: [number](/docs/luau/numbers),Offset: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [Scale](#Scale):[number](/docs/luau/numbers) |
| [Offset](#Offset):[number](/docs/luau/numbers) |

Math Operations

|  |
| --- |
| [`UDim + UDim`](#UDim-+-UDim) |
| [`UDim - UDim`](#UDim---UDim) |

The [UDim](/docs/reference/engine/datatypes/UDim) data type represents a one-dimensional value with two
components, a relative scale and an absolute offset in pixels.

---

API Reference

Constructors

new

Returns a [UDim](/docs/reference/engine/datatypes/UDim) from the given components.

UDim.new(

Scale:[number](/docs/luau/numbers), Offset:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| Scale:[number](/docs/luau/numbers) |
| Offset:[number](/docs/luau/numbers) |

Returns a [UDim](/docs/reference/engine/datatypes/UDim) from the given components.

Provide feedback

---

Properties

Scale

The relative scale component of the [UDim](/docs/reference/engine/datatypes/UDim).

UDim.Scale:[number](/docs/luau/numbers)

The relative scale component of the [UDim](/docs/reference/engine/datatypes/UDim).

Provide feedback

---

Offset

The absolute offset component of the [UDim](/docs/reference/engine/datatypes/UDim).

UDim.Offset:[number](/docs/luau/numbers)

The absolute offset component of the [UDim](/docs/reference/engine/datatypes/UDim) in pixels.

Provide feedback

---

Math Operations

`UDim` + `UDim`

Produces a [UDim](/docs/reference/engine/datatypes/UDim) representing the sum of the two [UDim](/docs/reference/engine/datatypes/UDim)
values.

UDim + UDim : UDim

Produces a [UDim](/docs/reference/engine/datatypes/UDim) representing the sum of the two [UDim](/docs/reference/engine/datatypes/UDim)
values.

Provide feedback

---

`UDim` - `UDim`

Produces a [UDim](/docs/reference/engine/datatypes/UDim) representing the difference between the two
[UDim](/docs/reference/engine/datatypes/UDim) values.

UDim - UDim : UDim

Produces a [UDim](/docs/reference/engine/datatypes/UDim) representing the difference between the two
[UDim](/docs/reference/engine/datatypes/UDim) values.

Provide feedback

---