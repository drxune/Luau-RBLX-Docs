# Vector2int16 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Vector2int16
Scraped: 2026-01-11T02:42:04.342190Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Vector2int16](/docs/reference/engine/datatypes/Vector2int16)

English

Feedback

Engine Data Type

Vector2int16

Represents a Vector2 with signed 16-bit integers for components.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [X](#X):[number](/docs/luau/numbers) |
| [Y](#Y):[number](/docs/luau/numbers) |

Math Operations

|  |
| --- |
| [`Vector2int16 + Vector2int16`](#Vector2int16-+-Vector2int16) |
| [`Vector2int16 - Vector2int16`](#Vector2int16---Vector2int16) |
| [`Vector2int16 * Vector2int16`](#Vector2int16-*-Vector2int16) |
| [`Vector2int16 / Vector2int16`](#Vector2int16-_-Vector2int16) |
| [`Vector2int16 * number`](#Vector2int16-*-number) |
| [`Vector2int16 / number`](#Vector2int16-_-number) |

The [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) data type represents a vector in 2D space with a
signed 16-bit integer for its components. It is similar to
[Vector2](/docs/reference/engine/datatypes/Vector2) in that it allows for the same arithmetic operations, but
it lacks commonly used vector functions.

[Vector2int16](/docs/reference/engine/datatypes/Vector2int16) should not be confused with:

* [Vector2](/docs/reference/engine/datatypes/Vector2), a more precise and complete implementation for 2D
  vectors.
* [Vector3int16](/docs/reference/engine/datatypes/Vector3int16), a similar implementation for 3D vectors.

For each component:

* The lower bound is -215, or -32,768.
* The upper bound is 215 − 1, or 32,767.

#### Converting to Vector2

To convert a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) to a [Vector2](/docs/reference/engine/datatypes/Vector2), construct a
[Vector2](/docs/reference/engine/datatypes/Vector2) by passing each component of the
[Vector2int16](/docs/reference/engine/datatypes/Vector2int16) to [Vector2.new()](/docs/reference/engine/datatypes/Vector2#new):

```
local vector2int16 = Vector2int16.new(1, 2)



local vector2 = Vector2.new(vector2int16.X, vector2int16.Y)



print(vector2)  --> 1, 2
```

Do not pass an entire [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) to [Vector2.new()](/docs/reference/engine/datatypes/Vector2#new),
as the constructor interprets a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) as a 0 within its
parameters without producing an error. This can lead to silent logic
errors if you do something like:

```
local vector2int16 = Vector2int16.new(1, 2)



local vector2 = Vector2.new(vector2int16)



print(vector2)  --> 0, 0
```

#### Math Operations

The following math operations are valid for the [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) data
type. For all operations, be mindful of the bounds associated with signed
16-bit integers, described earlier.

| Operation | Description |
| --- | --- |
| [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) + [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) | Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the sum of the operands' respective components. |
| [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) - [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) | Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the difference of the operands' respective components. |
| [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) \* [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) | Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the product of the operands' respective components. |
| [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) / [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) | Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the quotient of the operands' respective components. The results of the division are rounded down. |
| [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) \* number | Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the product of the respective [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) components and the number (factor). This operation is commutative. |
| [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) / number | Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the quotient of the respective [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) components and the number (divisor). The results of the division are rounded toward zero. |

---

API Reference

Constructors

new

Returns a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) from the given x and y components.

Vector2int16.new(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |

Returns a new [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) given the x and y components. Non-integer
components are rounded down.

The components must fall within the range [-215,
215). If outside this range, integer
overflow may occur. For
example, providing 32,768 (equal to 215) as a component
overflows the 16-bit integer, and so the component is -32,768 (equal
to -215) instead.

Provide feedback

---

Properties

X

The x-coordinate of the [Vector2int16](/docs/reference/engine/datatypes/Vector2int16).

Vector2int16.X:[number](/docs/luau/numbers)

The x-coordinate of the [Vector2int16](/docs/reference/engine/datatypes/Vector2int16), also accessible in its
lower-case variant.

Provide feedback

---

Y

The y-coordinate of the [Vector2int16](/docs/reference/engine/datatypes/Vector2int16).

Vector2int16.Y:[number](/docs/luau/numbers)

The y-coordinate of the [Vector2int16](/docs/reference/engine/datatypes/Vector2int16), also accessible in its
lower-case variant.

Provide feedback

---

Math Operations

`Vector2int16` + `Vector2int16`

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the sum of the
operands' respective components.

Vector2int16 + Vector2int16 : Vector2int16

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the sum of the
operands' respective components. Be mindful of the bounds associated with
signed 16-bit integers, described earlier.

Provide feedback

---

`Vector2int16` - `Vector2int16`

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the difference of
the operands' respective components.

Vector2int16 - Vector2int16 : Vector2int16

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the difference of
the operands' respective components. Be mindful of the bounds associated
with signed 16-bit integers, described earlier.

Provide feedback

---

`Vector2int16` \* `Vector2int16`

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the product of the
operands' respective components.

Vector2int16 \* Vector2int16 : Vector2int16

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the product of the
operands' respective components. Be mindful of the bounds associated with
signed 16-bit integers, described earlier.

Provide feedback

---

`Vector2int16` / `Vector2int16`

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the quotient of
the operands' respective components.

Vector2int16 / Vector2int16 : Vector2int16

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the quotient of
the operands' respective components. The results of the division are
rounded down. Be mindful of the bounds associated with signed 16-bit
integers, described earlier.

Provide feedback

---

`Vector2int16` \* `number`

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the product of the
respective [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) components and the number (factor).

Vector2int16 \* [number](/docs/luau/numbers) : Vector2int16

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the product of the
respective [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) components and the number (factor).
This operation is commutative. Be mindful of the bounds associated with
signed 16-bit integers, described earlier.

Provide feedback

---

`Vector2int16` / `number`

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the quotient of
the respective [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) components and the number
(divisor).

Vector2int16 / [number](/docs/luau/numbers) : Vector2int16

Produces a [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) whose components are the quotient of
the respective [Vector2int16](/docs/reference/engine/datatypes/Vector2int16) components and the number
(divisor). The results of the division are rounded toward zero. Be mindful
of the bounds associated with signed 16-bit integers, described earlier.

Provide feedback

---