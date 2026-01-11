# NumberRange | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/NumberRange
Scraped: 2026-01-11T02:42:23.084791Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [NumberRange](/docs/reference/engine/datatypes/NumberRange)

English

Feedback

Engine Data Type

NumberRange

Represents a range of numbers.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(value: [number](/docs/luau/numbers)) |
| [new](#new-minimum-ma)(minimum: [number](/docs/luau/numbers),maximum: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [Min](#Min):[number](/docs/luau/numbers) |
| [Max](#Max):[number](/docs/luau/numbers) |

The [NumberRange](/docs/reference/engine/datatypes/NumberRange) represents a range of numbers.

NumberRange stores its [NumberRange.Min](/docs/reference/engine/datatypes/NumberRange#Min) and
[NumberRange.Max](/docs/reference/engine/datatypes/NumberRange#Max) values as 32-bit floating-point numbers. Very large
numbers or numbers requiring high decimal precision may lose accuracy.

---

API Reference

Constructors

new

Returns a new [NumberRange](/docs/reference/engine/datatypes/NumberRange) with the minimum and maximum set to the
value.

NumberRange.new(value:[number](/docs/luau/numbers))

Parameters

|  |
| --- |
| value:[number](/docs/luau/numbers) |

Returns a new [NumberRange](/docs/reference/engine/datatypes/NumberRange) with the minimum and maximum set to the
value.

Provide feedback

---

new

Returns a new [NumberRange](/docs/reference/engine/datatypes/NumberRange) with the provided minimum and maximum.

NumberRange.new(

minimum:[number](/docs/luau/numbers), maximum:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| minimum:[number](/docs/luau/numbers) |
| maximum:[number](/docs/luau/numbers) |

Returns a new [NumberRange](/docs/reference/engine/datatypes/NumberRange) with the provided minimum and maximum. The
minimum must be less than or equal to maximum.

Provide feedback

---

Properties

Min

The minimum value of the [NumberRange](/docs/reference/engine/datatypes/NumberRange).

NumberRange.Min:[number](/docs/luau/numbers)

The minimum value of the [NumberRange](/docs/reference/engine/datatypes/NumberRange), always less than or equal
to the maximum.

Provide feedback

---

Max

The maximum value of the [NumberRange](/docs/reference/engine/datatypes/NumberRange).

NumberRange.Max:[number](/docs/luau/numbers)

The maximum value of the [NumberRange](/docs/reference/engine/datatypes/NumberRange), always greater than or
equal to the minimum.

Provide feedback

---