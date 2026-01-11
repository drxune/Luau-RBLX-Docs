# Vector2 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Vector2
Scraped: 2026-01-11T02:43:29.521957Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Vector2](/docs/reference/engine/datatypes/Vector2)

English

Feedback

Engine Data Type

Vector2

Represents a 2D value with direction and magnitude.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [zero](#zero):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [one](#one):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [xAxis](#xAxis):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [yAxis](#yAxis):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [X](#X):[number](/docs/luau/numbers) |
| [Y](#Y):[number](/docs/luau/numbers) |
| [Magnitude](#Magnitude):[number](/docs/luau/numbers) |
| [Unit](#Unit):[Vector2](/docs/reference/engine/datatypes/Vector2) |

Methods

|  |
| --- |
| [Cross](#Cross)(other: [Vector2](/docs/reference/engine/datatypes/Vector2)):[number](/docs/luau/numbers) |
| [Abs](#Abs)():[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Ceil](#Ceil)():[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Floor](#Floor)():[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Sign](#Sign)():[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Angle](#Angle)(other: [Vector2](/docs/reference/engine/datatypes/Vector2),isSigned: [boolean](/docs/luau/booleans)):[number](/docs/luau/numbers) |
| [Dot](#Dot)(v: [Vector2](/docs/reference/engine/datatypes/Vector2)):[number](/docs/luau/numbers) |
| [Lerp](#Lerp)(v: [Vector2](/docs/reference/engine/datatypes/Vector2),alpha: [number](/docs/luau/numbers)):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Max](#Max)(others...: [Tuple](/docs/luau/tuples)):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Min](#Min)(others...: [Tuple](/docs/luau/tuples)):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [FuzzyEq](#FuzzyEq)(other: [Vector2](/docs/reference/engine/datatypes/Vector2),epsilon: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |

Math Operations

|  |
| --- |
| [`Vector2 + Vector2`](#Vector2-+-Vector2) |
| [`Vector2 - Vector2`](#Vector2---Vector2) |
| [`Vector2 * Vector2`](#Vector2-*-Vector2) |
| [`Vector2 / Vector2`](#Vector2-_-Vector2) |
| [`Vector2 * number`](#Vector2-*-number) |
| [`Vector2 / number`](#Vector2-_-number) |

The [Vector2](/docs/reference/engine/datatypes/Vector2) data type represents a 2D value with direction and
magnitude. Some applications include GUI elements and 2D mouse positions.

#### Math Operations

The following math operations are valid for the [Vector2](/docs/reference/engine/datatypes/Vector2) data type:

| Operation | Description |
| --- | --- |
| [Vector2](/docs/reference/engine/datatypes/Vector2) + [Vector2](/docs/reference/engine/datatypes/Vector2) | Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second added to the corresponding component of the first. |
| [Vector2](/docs/reference/engine/datatypes/Vector2) - [Vector2](/docs/reference/engine/datatypes/Vector2) | Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second subtracted from the corresponding component of the first. |
| [Vector2](/docs/reference/engine/datatypes/Vector2) \* [Vector2](/docs/reference/engine/datatypes/Vector2) | Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second multiplied by the corresponding component of the first. |
| [Vector2](/docs/reference/engine/datatypes/Vector2) / [Vector2](/docs/reference/engine/datatypes/Vector2) | Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the first divided by the corresponding component of the second. |
| [Vector2](/docs/reference/engine/datatypes/Vector2) \* number | Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component multiplied by the number. |
| [Vector2](/docs/reference/engine/datatypes/Vector2) / number | Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component divided by the number. |

---

API Reference

Constructors

new

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) from the given x and y components.

Vector2.new(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) from the given x and y components.

Provide feedback

---

Properties

zero

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a magnitude of zero.

Vector2.zero:[Vector2](/docs/reference/engine/datatypes/Vector2)

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a magnitude of zero.

This API member is a constant, and must be accessed through the
[Vector2](/docs/reference/engine/datatypes/Vector2) global as opposed to an individual [Vector2](/docs/reference/engine/datatypes/Vector2)
object.

```
print(Vector2.zero)  --> 0, 0
```

Provide feedback

---

one

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a value of 1 on every axis.

Vector2.one:[Vector2](/docs/reference/engine/datatypes/Vector2)

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a value of 1 on every axis.

This API member is a constant, and must be accessed through the
[Vector2](/docs/reference/engine/datatypes/Vector2) global as opposed to an individual [Vector2](/docs/reference/engine/datatypes/Vector2)
object.

```
print(Vector2.one)  --> 1, 1
```

Provide feedback

---

xAxis

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a value of 1 on the X axis.

Vector2.xAxis:[Vector2](/docs/reference/engine/datatypes/Vector2)

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a value of 1 on the X axis.

This API member is a constant, and must be accessed through the
[Vector2](/docs/reference/engine/datatypes/Vector2) global as opposed to an individual [Vector2](/docs/reference/engine/datatypes/Vector2)
object.

```
print(Vector2.xAxis)  --> 1, 0
```

Provide feedback

---

yAxis

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a value of 1 on the y axis.

Vector2.yAxis:[Vector2](/docs/reference/engine/datatypes/Vector2)

A [Vector2](/docs/reference/engine/datatypes/Vector2) with a value of 1 on the Y axis.

This API member is a constant, and must be accessed through the
[Vector2](/docs/reference/engine/datatypes/Vector2) global as opposed to an individual [Vector2](/docs/reference/engine/datatypes/Vector2)
object.

```
print(Vector2.yAxis)  --> 0, 1
```

Provide feedback

---

X

The x-coordinate of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Vector2.X:[number](/docs/luau/numbers)

The x-coordinate of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Provide feedback

---

Y

The y-coordinate of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Vector2.Y:[number](/docs/luau/numbers)

The y-coordinate of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Provide feedback

---

Magnitude

The length of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Vector2.Magnitude:[number](/docs/luau/numbers)

The length of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Provide feedback

---

Unit

A normalized copy of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Vector2.Unit:[Vector2](/docs/reference/engine/datatypes/Vector2)

A normalized copy of the [Vector2](/docs/reference/engine/datatypes/Vector2).

Provide feedback

---

Methods

Cross

Returns the cross product of the two vectors.

Vector2:Cross(other:[Vector2](/docs/reference/engine/datatypes/Vector2)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| other:[Vector2](/docs/reference/engine/datatypes/Vector2) |

Returns

[number](/docs/luau/numbers)

Returns the cross product of the two vectors.

Provide feedback

---

Abs

Returns a new vector from the absolute values of the original's
components.

Vector2:Abs():[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns a new vector from the absolute values of the original's
components. For example, a vector of (-2, 4) returns a vector of
(2, 4).

Provide feedback

---

Ceil

Returns a new vector from the ceiling of the original's components.

Vector2:Ceil():[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns a new vector from the ceiling of the original's components. For
example, a vector of (-2.6, 5.1) returns a vector of (-2, 6).

Provide feedback

---

Floor

Returns a new vector from the floor of the original's components.

Vector2:Floor():[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns a new vector from the floor of the original's components. For
example, a vector of (-2.6, 5.1) returns a vector of (-3, 5).

Provide feedback

---

Sign

Returns a new vector from the sign (-1, 0, or 1) of the original's
components.

Vector2:Sign():[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns a new vector from the sign (-1, 0, or 1) of the original's
components. For example, a vector of (-2.6, 5.1) returns a vector of
(-1, 1).

Provide feedback

---

Angle

Returns the angle in radians between the two vectors.

Vector2:Angle(

other:[Vector2](/docs/reference/engine/datatypes/Vector2), isSigned:[boolean](/docs/luau/booleans)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| other:[Vector2](/docs/reference/engine/datatypes/Vector2) |
| isSigned:[boolean](/docs/luau/booleans) Default Value: false |

Returns

[number](/docs/luau/numbers)

Returns the angle in radians between the two vectors. Specify true for
the optional isSigned boolean if you want a signed angle. By default,
the method returns the absolute value. Signed angles are a negative when
going clockwise. Values are in the range [0, pi] for absolute angles and
[-pi, pi] for signed angles.

Provide feedback

---

Dot

Returns a scalar dot product of the two vectors.

Vector2:Dot(v:[Vector2](/docs/reference/engine/datatypes/Vector2)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| v:[Vector2](/docs/reference/engine/datatypes/Vector2) |

Returns

[number](/docs/luau/numbers)

Returns a scalar dot product of the two vectors.

Provide feedback

---

Lerp

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) linearly interpolated between this
[Vector2](/docs/reference/engine/datatypes/Vector2) and the given goal by the given alpha.

Vector2:Lerp(

v:[Vector2](/docs/reference/engine/datatypes/Vector2), alpha:[number](/docs/luau/numbers)

):[Vector2](/docs/reference/engine/datatypes/Vector2)

Parameters

|  |
| --- |
| v:[Vector2](/docs/reference/engine/datatypes/Vector2) |
| alpha:[number](/docs/luau/numbers) |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) linearly interpolated between this
[Vector2](/docs/reference/engine/datatypes/Vector2) and the given goal by the given alpha.

Provide feedback

---

Max

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component as the highest among the
respective components of the provided [Vector2](/docs/reference/engine/datatypes/Vector2) objects.

Vector2:Max(others...:[Tuple](/docs/luau/tuples)):[Vector2](/docs/reference/engine/datatypes/Vector2)

Parameters

|  |
| --- |
| others...:[Tuple](/docs/luau/tuples) |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component as the highest among the
respective components of the provided [Vector2](/docs/reference/engine/datatypes/Vector2) objects.

```
local a = Vector2.new(1, 2)



local b = Vector2.new(2, 1)



print(a:Max(b)) -- Vector2.new(2, 2)
```

Provide feedback

---

Min

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component as the lowest among the
respective components of the provided [Vector2](/docs/reference/engine/datatypes/Vector2) objects.

Vector2:Min(others...:[Tuple](/docs/luau/tuples)):[Vector2](/docs/reference/engine/datatypes/Vector2)

Parameters

|  |
| --- |
| others...:[Tuple](/docs/luau/tuples) |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component as the lowest among the
respective components of the provided [Vector2](/docs/reference/engine/datatypes/Vector2) objects.

```
local a = Vector2.new(1, 2)



local b = Vector2.new(2, 1)



print(a:Min(b)) -- Vector2.new(1, 1)
```

Provide feedback

---

FuzzyEq

Returns true if the X and Y components of the other [Vector2](/docs/reference/engine/datatypes/Vector2)
are within epsilon units of each corresponding component of this
[Vector2](/docs/reference/engine/datatypes/Vector2).

Vector2:FuzzyEq(

other:[Vector2](/docs/reference/engine/datatypes/Vector2), epsilon:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| other:[Vector2](/docs/reference/engine/datatypes/Vector2) |
| epsilon:[number](/docs/luau/numbers) Default Value: 0.00001 (1e-5) |

Returns

[boolean](/docs/luau/booleans)

Returns true if the X and Y components of the other [Vector2](/docs/reference/engine/datatypes/Vector2)
are within epsilon units of each corresponding component of this
[Vector2](/docs/reference/engine/datatypes/Vector2).

Provide feedback

---

Math Operations

`Vector2` + `Vector2`

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second added to
the corresponding component of the first.

[Vector2](/docs/reference/engine/datatypes/Vector2) + [Vector2](/docs/reference/engine/datatypes/Vector2) : [Vector2](/docs/reference/engine/datatypes/Vector2)

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second added to
the corresponding component of the first.

Provide feedback

---

`Vector2` - `Vector2`

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second subtracted
from the corresponding component of the first.

[Vector2](/docs/reference/engine/datatypes/Vector2) - [Vector2](/docs/reference/engine/datatypes/Vector2) : [Vector2](/docs/reference/engine/datatypes/Vector2)

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second subtracted
from the corresponding component of the first.

Provide feedback

---

`Vector2` \* `Vector2`

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second multiplied
by the corresponding component of the first.

[Vector2](/docs/reference/engine/datatypes/Vector2) \* [Vector2](/docs/reference/engine/datatypes/Vector2) : [Vector2](/docs/reference/engine/datatypes/Vector2)

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the second multiplied
by the corresponding component of the first.

Provide feedback

---

`Vector2` / `Vector2`

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the first divided by
the corresponding component of the second.

[Vector2](/docs/reference/engine/datatypes/Vector2) / [Vector2](/docs/reference/engine/datatypes/Vector2) : [Vector2](/docs/reference/engine/datatypes/Vector2)

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component of the first divided by
the corresponding component of the second.

Provide feedback

---

`Vector2` \* `number`

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component multiplied by the
number.

[Vector2](/docs/reference/engine/datatypes/Vector2) \* [number](/docs/luau/numbers) : [Vector2](/docs/reference/engine/datatypes/Vector2)

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component multiplied by the
number.

Provide feedback

---

`Vector2` / `number`

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component divided by the number.

[Vector2](/docs/reference/engine/datatypes/Vector2) / [number](/docs/luau/numbers) : [Vector2](/docs/reference/engine/datatypes/Vector2)

Produces a [Vector2](/docs/reference/engine/datatypes/Vector2) with each component divided by the number.

Provide feedback

---