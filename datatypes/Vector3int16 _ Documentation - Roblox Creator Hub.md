# Vector3int16 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Vector3int16
Scraped: 2026-01-11T02:42:24.520359Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Vector3int16](/docs/reference/engine/datatypes/Vector3int16)

English

Feedback

Engine Data Type

Vector3int16

A Vector3 with signed 16-bit integers for components.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [X](#X):[number](/docs/luau/numbers) |
| [Y](#Y):[number](/docs/luau/numbers) |
| [Z](#Z):[number](/docs/luau/numbers) |

Math Operations

|  |
| --- |
| [`Vector3int16 + Vector3int16`](#Vector3int16-+-Vector3int16) |
| [`Vector3int16 - Vector3int16`](#Vector3int16---Vector3int16) |
| [`Vector3int16 * Vector3int16`](#Vector3int16-*-Vector3int16) |
| [`Vector3int16 / Vector3int16`](#Vector3int16-_-Vector3int16) |
| [`Vector3int16 * number`](#Vector3int16-*-number) |
| [`Vector3int16 / number`](#Vector3int16-_-number) |

The [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) data type represents a vector in 3D space with a
signed 16-bit integer for its components. It is similar to
[Vector3](/docs/reference/engine/datatypes/Vector3) in that it allows for the same arithmetic operations, but
it lacks commonly used vector functions.

[Vector3int16](/docs/reference/engine/datatypes/Vector3int16) should not be confused with:

* [Vector3](/docs/reference/engine/datatypes/Vector3), a more precise and complete implementation for 3D
  vectors.
* [Vector2int16](/docs/reference/engine/datatypes/Vector2int16), a similar implementation for 2D vectors.

For each component:

* The lower bound is -215, or -32,768.
* The upper bound is 215 − 1, or 32,767.

#### Converting to Vector3

To convert a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) to a [Vector3](/docs/reference/engine/datatypes/Vector3), construct a
[Vector3](/docs/reference/engine/datatypes/Vector3) by passing each component of the
[Vector3int16](/docs/reference/engine/datatypes/Vector3int16) to [Vector3.new()](/docs/reference/engine/datatypes/Vector3#new):

```
local vector3int16 = Vector3int16.new(1, 2, 3)



local vector3 = Vector3.new(vector3int16.X, vector3int16.Y, vector3int16.Z)



print(vector3)  --> 1, 2, 3
```

Do not pass an entire [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) to [Vector3.new()](/docs/reference/engine/datatypes/Vector3#new),
as the constructor interprets a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) as a 0 within its
parameters without producing an error. This can lead to silent logic
errors if you do something like:

```
local vector3int16 = Vector3int16.new(1, 2, 3)



local vector3 = Vector3.new(vector3int16)



print(vector3)  --> 0, 0, 0
```

#### Math Operations

The following math operations are valid for the [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) data
type. For all operations, be mindful of the bounds associated with signed
16-bit integers, described earlier.

| Operation | Description |
| --- | --- |
| [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) + [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) | Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the sum of the operands' respective components. |
| [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) - [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) | Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the difference of the operands' respective components. |
| [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) \* [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) | Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the product of the operands' respective components. |
| [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) / [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) | Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the quotient of the operands' respective components. The results of the division are rounded down. |
| [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) \* number | Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the product of the respective [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) components and the number (factor). This operation is commutative. |
| [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) / number | Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the quotient of the respective [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) components and the number (divisor). The results of the division are rounded toward zero. |

---

API Reference

Constructors

new

Returns a new [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) from the given x, y, and z components.

Vector3int16.new(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |
| z:[number](/docs/luau/numbers) |

Returns a new [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) from the given x, y and z components.
Non-integer components are rounded down.

The components must fall within the range [-215,
215). If outside this range, integer
overflow may occur. For
example, providing 32,768 (equal to 215) as a component
overflows the 16-bit integer, and so the component will be -32,768 (equal
to -215) instead.

Provide feedback

---

Properties

X

The x-coordinate of the [Vector3int16](/docs/reference/engine/datatypes/Vector3int16).

Vector3int16.X:[number](/docs/luau/numbers)

The x-coordinate of the [Vector3int16](/docs/reference/engine/datatypes/Vector3int16), also accessible in its
lower-case variant.

Provide feedback

---

Y

The y-coordinate of the [Vector3int16](/docs/reference/engine/datatypes/Vector3int16).

Vector3int16.Y:[number](/docs/luau/numbers)

The y-coordinate of the [Vector3int16](/docs/reference/engine/datatypes/Vector3int16), also accessible in its
lower-case variant.

Provide feedback

---

Z

The z-coordinate of the [Vector3int16](/docs/reference/engine/datatypes/Vector3int16).

Vector3int16.Z:[number](/docs/luau/numbers)

The z-coordinate of the [Vector3int16](/docs/reference/engine/datatypes/Vector3int16), also accessible in its
lower-case variant.

Provide feedback

---

Math Operations

`Vector3int16` + `Vector3int16`

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the sum of the
operands' respective components.

Vector3int16 + Vector3int16 : Vector3int16

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the sum of the
operands' respective components. Be mindful of the bounds associated with
signed 16-bit integers, described earlier.

Provide feedback

---

`Vector3int16` - `Vector3int16`

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the difference of
the operands' respective components.

Vector3int16 - Vector3int16 : Vector3int16

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the difference of
the operands' respective components. Be mindful of the bounds associated
with signed 16-bit integers, described earlier.

Provide feedback

---

`Vector3int16` \* `Vector3int16`

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the product of the
operands' respective components.

Vector3int16 \* Vector3int16 : Vector3int16

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the product of the
operands' respective components. Be mindful of the bounds associated with
signed 16-bit integers, described earlier.

Provide feedback

---

`Vector3int16` / `Vector3int16`

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the quotient of
the operands' respective components. The results of the division are
rounded down.

Vector3int16 / Vector3int16 : Vector3int16

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the quotient of
the operands' respective components. The results of the division are
rounded down. Be mindful of the bounds associated with signed 16-bit
integers, described earlier.

Provide feedback

---

`Vector3int16` \* `number`

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the product of the
respective [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) components and the number (factor).
This operation is commutative.

Vector3int16 \* [number](/docs/luau/numbers) : Vector3int16

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the product of the
respective [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) components and the number (factor).
This operation is commutative. Be mindful of the bounds associated with
signed 16-bit integers, described earlier.

Provide feedback

---

`Vector3int16` / `number`

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the quotient of
the respective [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) components and the number
(divisor). The results of the division are rounded toward zero.

Vector3int16 / [number](/docs/luau/numbers) : Vector3int16

Produces a [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) whose components are the quotient of
the respective [Vector3int16](/docs/reference/engine/datatypes/Vector3int16) components and the number
(divisor). The results of the division are rounded toward zero. Be mindful
of the bounds associated with signed 16-bit integers, described earlier.

Provide feedback

---