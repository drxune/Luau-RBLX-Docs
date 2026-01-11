# vector | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/vector
Scraped: 2026-01-11T02:49:37.953986Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [vector](/docs/reference/engine/libraries/vector)

English

Feedback

Engine Library

vector

A library of vector functions.

---

Summary

Functions

|  |
| --- |
| [create](#create)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)):[vector](/docs/reference/engine/libraries/vector) |
| [magnitude](#magnitude)(vec: [vector](/docs/reference/engine/libraries/vector)):[number](/docs/luau/numbers) |
| [normalize](#normalize)(vec: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [cross](#cross)(vec1: [vector](/docs/reference/engine/libraries/vector),vec2: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [dot](#dot)(vec1: [vector](/docs/reference/engine/libraries/vector),vec2: [vector](/docs/reference/engine/libraries/vector)):[number](/docs/luau/numbers) |
| [angle](#angle)(vec1: [vector](/docs/reference/engine/libraries/vector),vec2: [vector](/docs/reference/engine/libraries/vector),axis: [vector](/docs/reference/engine/libraries/vector)?):[number](/docs/luau/numbers) |
| [floor](#floor)(vec: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [ceil](#ceil)(vec: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [abs](#abs)(vec: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [sign](#sign)(vec: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [clamp](#clamp)(vec: [vector](/docs/reference/engine/libraries/vector),min: [vector](/docs/reference/engine/libraries/vector),max: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [lerp](#lerp)(vec1: [vector](/docs/reference/engine/libraries/vector),vec2: [vector](/docs/reference/engine/libraries/vector),alpha: [number](/docs/luau/numbers)):[vector](/docs/reference/engine/libraries/vector) |
| [max](#max)(...: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |
| [min](#min)(...: [vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector) |

Properties

|  |
| --- |
| [zero](#zero):[vector](/docs/reference/engine/libraries/vector) |
| [one](#one):[vector](/docs/reference/engine/libraries/vector) |

This library implements functionality for the vector type in addition to the
built-in primitive operator support. It uses vectors with three components
(x, y, and z).

Individual vector components can be accessed using the fields x or X, y
or Y, z or Z. Since vector values are immutable, writing to individual
components is not supported.

---

API Reference

Functions

create

Creates a new vector with the given component values.

vector.create(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers)

):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |
| z:[number](/docs/luau/numbers) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Creates a new vector with the given component values.

Provide feedback

---

magnitude

Calculates the magnitude of a given vector.

vector.magnitude(vec:[vector](/docs/reference/engine/libraries/vector)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| vec:[vector](/docs/reference/engine/libraries/vector) |

Returns

[number](/docs/luau/numbers)

Calculates the magnitude of a given vector.

Provide feedback

---

normalize

Computes the normalized version (unit vector) of a given vector.

vector.normalize(vec:[vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Computes the normalized version (unit vector) of a given vector.

Provide feedback

---

cross

Computes the cross product of two vectors.

vector.cross(

vec1:[vector](/docs/reference/engine/libraries/vector), vec2:[vector](/docs/reference/engine/libraries/vector)

):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec1:[vector](/docs/reference/engine/libraries/vector) |
| vec2:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Computes the cross product of two vectors.

Provide feedback

---

dot

Computes the dot product of two vectors.

vector.dot(

vec1:[vector](/docs/reference/engine/libraries/vector), vec2:[vector](/docs/reference/engine/libraries/vector)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| vec1:[vector](/docs/reference/engine/libraries/vector) |
| vec2:[vector](/docs/reference/engine/libraries/vector) |

Returns

[number](/docs/luau/numbers)

Computes the dot product of two vectors.

Provide feedback

---

angle

Computes the angle between two vectors in radians.

vector.angle(

vec1:[vector](/docs/reference/engine/libraries/vector), vec2:[vector](/docs/reference/engine/libraries/vector), axis:[vector](/docs/reference/engine/libraries/vector)?

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| vec1:[vector](/docs/reference/engine/libraries/vector) |
| vec2:[vector](/docs/reference/engine/libraries/vector) |
| axis:[vector](/docs/reference/engine/libraries/vector)? |

Returns

[number](/docs/luau/numbers)

Computes the angle between two vectors in radians. The axis, if specified,
is used to determine the sign of the angle.

Provide feedback

---

floor

Applies [math.floor()](/docs/reference/engine/libraries/math#floor) to every component of the input vector.

vector.floor(vec:[vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Applies [math.floor()](/docs/reference/engine/libraries/math#floor) to every component of the input vector.

Provide feedback

---

ceil

Applies [math.ceil()](/docs/reference/engine/libraries/math#ceil) to every component of the input vector.

vector.ceil(vec:[vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Applies [math.ceil()](/docs/reference/engine/libraries/math#ceil) to every component of the input vector.

Provide feedback

---

abs

Applies [math.abs()](/docs/reference/engine/libraries/math#abs) to every component of the input vector.

vector.abs(vec:[vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Applies [math.abs()](/docs/reference/engine/libraries/math#abs) to every component of the input vector.

Provide feedback

---

sign

Applies [math.sign()](/docs/reference/engine/libraries/math#sign) to every component of the input vector.

vector.sign(vec:[vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Applies [math.sign()](/docs/reference/engine/libraries/math#sign) to every component of the input vector.

Provide feedback

---

clamp

Applies [math.clamp()](/docs/reference/engine/libraries/math#clamp) to every component of the input vector.

vector.clamp(

vec:[vector](/docs/reference/engine/libraries/vector), min:[vector](/docs/reference/engine/libraries/vector), max:[vector](/docs/reference/engine/libraries/vector)

):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec:[vector](/docs/reference/engine/libraries/vector) |
| min:[vector](/docs/reference/engine/libraries/vector) |
| max:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Applies [math.clamp()](/docs/reference/engine/libraries/math#clamp) to every component of the input vector.

Provide feedback

---

lerp

Returns a vector linearly interpolated between two vectors by a fractional
alpha.

vector.lerp(

vec1:[vector](/docs/reference/engine/libraries/vector), vec2:[vector](/docs/reference/engine/libraries/vector), alpha:[number](/docs/luau/numbers)

):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| vec1:[vector](/docs/reference/engine/libraries/vector) |
| vec2:[vector](/docs/reference/engine/libraries/vector) |
| alpha:[number](/docs/luau/numbers) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Returns a vector linearly interpolated between two vectors (vec1,
vec2) by the fraction alpha. Note that alpha is not limited to
the range [0, 1].

Provide feedback

---

max

Applies [math.max()](/docs/reference/engine/libraries/math#max) to the corresponding components of the input
vectors.

vector.max(...:[vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| ...:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Applies [math.max()](/docs/reference/engine/libraries/math#max) to the corresponding components of the input
vectors.

Provide feedback

---

min

Applies [math.min()](/docs/reference/engine/libraries/math#min) to the corresponding components of the input
vectors.

vector.min(...:[vector](/docs/reference/engine/libraries/vector)):[vector](/docs/reference/engine/libraries/vector)

Parameters

|  |
| --- |
| ...:[vector](/docs/reference/engine/libraries/vector) |

Returns

[vector](/docs/reference/engine/libraries/vector)

Applies [math.min()](/docs/reference/engine/libraries/math#min) to the corresponding components of the input
vectors.

Provide feedback

---

Properties

zero

Constant vector with all components set to 0.

vector.zero:[vector](/docs/reference/engine/libraries/vector)

Constant vector with all components set to 0.

Provide feedback

---

one

Constant vector with all components set to 1.

vector.one:[vector](/docs/reference/engine/libraries/vector)

Constant vector with all components set to 1.

Provide feedback

---