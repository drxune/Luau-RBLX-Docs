# Vector3 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Vector3
Scraped: 2026-01-11T02:43:02.507358Z

## Inherits
- Position
- Rotation
- Size
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Vector3](/docs/reference/engine/datatypes/Vector3)

English

Feedback

Engine Data Type

Vector3

Represents a 3D value with a direction and magnitude.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)) |
| [FromNormalId](#FromNormalId)(normal: [Enum.NormalId](/docs/reference/engine/enums/NormalId)) |
| [FromAxis](#FromAxis)(axis: [Enum.Axis](/docs/reference/engine/enums/Axis)) |

Properties

|  |
| --- |
| [zero](#zero):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [one](#one):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [xAxis](#xAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [yAxis](#yAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [zAxis](#zAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [X](#X):[number](/docs/luau/numbers) |
| [Y](#Y):[number](/docs/luau/numbers) |
| [Z](#Z):[number](/docs/luau/numbers) |
| [Magnitude](#Magnitude):[number](/docs/luau/numbers) |
| [Unit](#Unit):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [Abs](#Abs)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Ceil](#Ceil)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Floor](#Floor)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Sign](#Sign)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Cross](#Cross)(other: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Angle](#Angle)(other: [Vector3](/docs/reference/engine/datatypes/Vector3),axis: [Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers) |
| [Dot](#Dot)(other: [Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers) |
| [FuzzyEq](#FuzzyEq)(other: [Vector3](/docs/reference/engine/datatypes/Vector3),epsilon: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [Lerp](#Lerp)(goal: [Vector3](/docs/reference/engine/datatypes/Vector3),alpha: [number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Max](#Max)(vector: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Min](#Min)(vector: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Math Operations

|  |
| --- |
| [`Vector3 + Vector3`](#Vector3-+-Vector3) |
| [`Vector3 - Vector3`](#Vector3---Vector3) |
| [`Vector3 * Vector3`](#Vector3-*-Vector3) |
| [`Vector3 / Vector3`](#Vector3-_-Vector3) |
| [`Vector3 // Vector3`](#Vector3-__-Vector3) |
| [`Vector3 * number`](#Vector3-*-number) |
| [`Vector3 / number`](#Vector3-_-number) |
| [`Vector3 // number`](#Vector3-__-number) |

The [Vector3](/docs/reference/engine/datatypes/Vector3) data type represents a vector in 3D space, typically
used as a point in 3D space or the dimensions of a rectangular prism.
[Vector3](/docs/reference/engine/datatypes/Vector3) supports basic component-based arithmetic operations (sum,
difference, product, and quotient) and these operations can be applied on the
left or right hand side to either another [Vector3](/docs/reference/engine/datatypes/Vector3) or a number. It
also features methods for common vector operations, such as
[Cross()](/docs/reference/engine/datatypes/Vector3#Cross) and [Dot()](/docs/reference/engine/datatypes/Vector3#Dot).

Alternatively to [Vector3](/docs/reference/engine/datatypes/Vector3), consider using the methods and properties
of the [vector](/docs/reference/engine/libraries/vector) library.

Some example usages of [Vector3](/docs/reference/engine/datatypes/Vector3) are the
[Position](/docs/reference/engine/classes/BasePart#Position), [Rotation](/docs/reference/engine/classes/BasePart#Rotation), and
[Size](/docs/reference/engine/classes/BasePart#Size) of parts, for example:

```
local Workspace = game:GetService("Workspace")



local part = Workspace.Part



part.Position = part.Position + Vector3.new(5, 2, 10) -- Move part by (5, 2, 10)
```

[Vector3](/docs/reference/engine/datatypes/Vector3) is also commonly used when constructing more complex 3D
data types such as [CFrame](/docs/reference/engine/datatypes/CFrame). Many of these data types' methods will
use a [Vector3](/docs/reference/engine/datatypes/Vector3) within their parameters, such as
[CFrame:PointToObjectSpace()](/docs/reference/engine/datatypes/CFrame#PointToObjectSpace).

---

API Reference

Constructors

new

Returns a new [Vector3](/docs/reference/engine/datatypes/Vector3) from the given x, y, and z components.

Vector3.new(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) Default Value: 0 |
| y:[number](/docs/luau/numbers) Default Value: 0 |
| z:[number](/docs/luau/numbers) Default Value: 0 |

Returns a new [Vector3](/docs/reference/engine/datatypes/Vector3) using the given x, y, and z components.

Provide feedback

---

FromNormalId

Returns a new [Vector3](/docs/reference/engine/datatypes/Vector3) in the given direction.

Vector3.FromNormalId(normal:[Enum.NormalId](/docs/reference/engine/enums/NormalId))

Parameters

|  |
| --- |
| normal:[Enum.NormalId](/docs/reference/engine/enums/NormalId) |

Returns a new [Vector3](/docs/reference/engine/datatypes/Vector3) in the given direction.

Provide feedback

---

FromAxis

Returns a new [Vector3](/docs/reference/engine/datatypes/Vector3) for the given axis.

Vector3.FromAxis(axis:[Enum.Axis](/docs/reference/engine/enums/Axis))

Parameters

|  |
| --- |
| axis:[Enum.Axis](/docs/reference/engine/enums/Axis) |

Returns a new [Vector3](/docs/reference/engine/datatypes/Vector3) for the given axis.

Provide feedback

---

Properties

zero

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a magnitude of 0.

Vector3.zero:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a magnitude of 0.

This API member is a constant, and must be accessed through the
[Vector3](/docs/reference/engine/datatypes/Vector3) global as opposed to an individual [Vector3](/docs/reference/engine/datatypes/Vector3)
object.

```
print(Vector3.zero) --> 0, 0, 0
```

Provide feedback

---

one

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on every axis.

Vector3.one:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on every axis.

This API member is a constant, and must be accessed through the
[Vector3](/docs/reference/engine/datatypes/Vector3) global as opposed to an individual [Vector3](/docs/reference/engine/datatypes/Vector3)
object.

```
print(Vector3.one)  --> 1, 1, 1
```

Provide feedback

---

xAxis

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on the X axis.

Vector3.xAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on the X axis.

This API member is a constant, and must be accessed through the
[Vector3](/docs/reference/engine/datatypes/Vector3) global as opposed to an individual [Vector3](/docs/reference/engine/datatypes/Vector3)
object.

```
print(Vector3.xAxis)  --> 1, 0, 0
```

Provide feedback

---

yAxis

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on the Y axis.

Vector3.yAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on the Y axis.

This API member is a constant, and must be accessed through the
[Vector3](/docs/reference/engine/datatypes/Vector3) global as opposed to an individual [Vector3](/docs/reference/engine/datatypes/Vector3)
object.

```
print(Vector3.yAxis)  --> 0, 1, 0
```

Provide feedback

---

zAxis

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on the Z axis.

Vector3.zAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) with a value of 1 on the Z axis.

This API member is a constant, and must be accessed through the
[Vector3](/docs/reference/engine/datatypes/Vector3) global as opposed to an individual [Vector3](/docs/reference/engine/datatypes/Vector3)
object.

```
print(Vector3.zAxis)  --> 0, 0, 1
```

Provide feedback

---

X

The X coordinate of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Vector3.X:[number](/docs/luau/numbers)

The X coordinate of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

Y

The Y coordinate of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Vector3.Y:[number](/docs/luau/numbers)

The Y coordinate of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

Z

The Z coordinate of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Vector3.Z:[number](/docs/luau/numbers)

The Z coordinate of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

Magnitude

The length of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Vector3.Magnitude:[number](/docs/luau/numbers)

The length of the [Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

Unit

A normalized copy of the [Vector3](/docs/reference/engine/datatypes/Vector3) - one that has the same
direction as the original but a magnitude of 1.

Vector3.Unit:[Vector3](/docs/reference/engine/datatypes/Vector3)

A normalized copy of the [Vector3](/docs/reference/engine/datatypes/Vector3) - one that has the same
direction as the original but a magnitude of 1.

Provide feedback

---

Methods

Abs

Returns a new vector from the absolute values of the original's
components.

Vector3:Abs():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a new vector from the absolute values of the original's
components. For example, a vector of (-2, 4, -6) returns a vector of
(2, 4, 6).

Provide feedback

---

Ceil

Returns a new vector from the ceiling of the original's components.

Vector3:Ceil():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a new vector from the ceiling of the original's components. For
example, a vector of (-2.6, 5.1, 8.8) returns a vector of (-2, 6, 9).

Provide feedback

---

Floor

Returns a new vector from the floor of the original's components.

Vector3:Floor():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a new vector from the floor of the original's components. For
example, a vector of (-2.6, 5.1, 8.8) returns a vector of (-3, 5, 8).

Provide feedback

---

Sign

Returns a new vector from the sign (-1, 0, or 1) of the original's
components.

Vector3:Sign():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a new vector from the sign (-1, 0, or 1) of the original's
components. For example, a vector of (-2.6, 5.1, 0) returns a vector of
(-1, 1, 0).

Provide feedback

---

Cross

Returns the cross product of the two vectors.

Vector3:Cross(other:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| other:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the cross product of the two vectors.

Provide feedback

---

Angle

Returns the angle in radians between the two vectors. If you provide an
axis, it determines the sign of the angle.

Vector3:Angle(

other:[Vector3](/docs/reference/engine/datatypes/Vector3), axis:[Vector3](/docs/reference/engine/datatypes/Vector3)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| other:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| axis:[Vector3](/docs/reference/engine/datatypes/Vector3) Default Value: nil |

Returns

[number](/docs/luau/numbers)

Returns the angle in radians between the two vectors. If you provide an
axis, it determines the sign of the angle.

Provide feedback

---

Dot

Returns a scalar dot product of the two vectors.

Vector3:Dot(other:[Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| other:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[number](/docs/luau/numbers)

Returns a scalar dot product of the two vectors.

Provide feedback

---

FuzzyEq

Returns true if the difference between the squared magnitude of the two
vectors is within epsilon. epsilon is scaled relative to the
magnitude, rather than an absolute epsilon.

Vector3:FuzzyEq(

other:[Vector3](/docs/reference/engine/datatypes/Vector3), epsilon:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| other:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| epsilon:[number](/docs/luau/numbers) Default Value: 0.00001 aka 1e-5 |

Returns

[boolean](/docs/luau/booleans)

Returns true if the difference between the squared magnitude of the two
vectors is within epsilon. epsilon is scaled relative to the
magnitude, rather than an absolute epsilon.

Provide feedback

---

Lerp

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) linearly interpolated between this
[Vector3](/docs/reference/engine/datatypes/Vector3) and the given goal by the given alpha.

Vector3:Lerp(

goal:[Vector3](/docs/reference/engine/datatypes/Vector3), alpha:[number](/docs/luau/numbers)

):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| goal:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| alpha:[number](/docs/luau/numbers) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) linearly interpolated between this
[Vector3](/docs/reference/engine/datatypes/Vector3) and the given goal [Vector3](/docs/reference/engine/datatypes/Vector3) by the fraction
alpha. Note that alpha is not limited to the range [0, 1].

Provide feedback

---

Max

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) with each component as the highest among the
respective components of both provided [Vector3](/docs/reference/engine/datatypes/Vector3) objects.

Vector3:Max(vector:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| vector:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) with each component as the highest among the
respective components of both provided [Vector3](/docs/reference/engine/datatypes/Vector3) objects.

```
local a = Vector3.new(1, 2, 1)



local b = Vector3.new(2, 1, 2)



print(a:Max(b))  --> Vector3.new(2, 2, 2)
```

Provide feedback

---

Min

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) with each component as the lowest among the
respective components of both provided [Vector3](/docs/reference/engine/datatypes/Vector3) objects.

Vector3:Min(vector:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| vector:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) with each component as the lowest among the
respective components of both provided [Vector3](/docs/reference/engine/datatypes/Vector3) objects.

```
local a = Vector3.new(1, 2, 1)



local b = Vector3.new(2, 1, 2)



print(a:Min(b))  --> Vector3.new(1, 1, 1)
```

Provide feedback

---

Math Operations

`Vector3` + `Vector3`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by adding each component of the first vector
to the corresponding component of the second.

[Vector3](/docs/reference/engine/datatypes/Vector3) + [Vector3](/docs/reference/engine/datatypes/Vector3) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by adding each component of the first vector
to the corresponding component of the second.

Provide feedback

---

`Vector3` - `Vector3`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by subtracting each component of the second
vector from the corresponding component of the first.

[Vector3](/docs/reference/engine/datatypes/Vector3) - [Vector3](/docs/reference/engine/datatypes/Vector3) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by subtracting each component of the second
vector from the corresponding component of the first.

Provide feedback

---

`Vector3` \* `Vector3`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by multiplying each component of the first
vector by the corresponding component of the second.

[Vector3](/docs/reference/engine/datatypes/Vector3) \* [Vector3](/docs/reference/engine/datatypes/Vector3) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by multiplying each component of the first
vector by the corresponding component of the second.

Provide feedback

---

`Vector3` / `Vector3`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by dividing each component of the first
vector by the corresponding component of the second.

[Vector3](/docs/reference/engine/datatypes/Vector3) / [Vector3](/docs/reference/engine/datatypes/Vector3) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by dividing each component of the first
vector by the corresponding component of the second.

Provide feedback

---

`Vector3` // `Vector3`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by floor dividing each component of the
first vector by the corresponding component of the second.

[Vector3](/docs/reference/engine/datatypes/Vector3) // [Vector3](/docs/reference/engine/datatypes/Vector3) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by floor dividing each component of the
first vector by the corresponding component of the second.

Provide feedback

---

`Vector3` \* `number`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by multiplying each component of the
provided vector by the number.

[Vector3](/docs/reference/engine/datatypes/Vector3) \* [number](/docs/luau/numbers) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by multiplying each component of the
provided vector by the number.

Provide feedback

---

`Vector3` / `number`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by dividing each component of the provided
vector by the number.

[Vector3](/docs/reference/engine/datatypes/Vector3) / [number](/docs/luau/numbers) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by dividing each component of the provided
vector by the number.

Provide feedback

---

`Vector3` // `number`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by floor dividing each component of the
provided vector by the number.

[Vector3](/docs/reference/engine/datatypes/Vector3) // [number](/docs/luau/numbers) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) by floor dividing each component of the
provided vector by the number.

Provide feedback

---