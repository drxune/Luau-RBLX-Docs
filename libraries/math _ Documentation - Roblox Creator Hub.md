# math | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/math
Scraped: 2026-01-11T02:50:02.816537Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [math](/docs/reference/engine/libraries/math)

English

Feedback

Engine Library

math

A library of math functions.

---

Summary

Functions

|  |
| --- |
| [abs](#abs)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [acos](#acos)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [asin](#asin)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [atan](#atan)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [atan2](#atan2)(y: [number](/docs/luau/numbers),x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [ceil](#ceil)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [clamp](#clamp)(x: [number](/docs/luau/numbers),min: [number](/docs/luau/numbers),max: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [cos](#cos)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [cosh](#cosh)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [deg](#deg)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [exp](#exp)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [floor](#floor)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [fmod](#fmod)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [frexp](#frexp)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [ldexp](#ldexp)(x: [number](/docs/luau/numbers),e: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [lerp](#lerp)(a: [number](/docs/luau/numbers),b: [number](/docs/luau/numbers),t: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [log](#log)(x: [number](/docs/luau/numbers),base: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [log10](#log10)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [map](#map)(x: [number](/docs/luau/numbers),inmin: [number](/docs/luau/numbers),inmax: [number](/docs/luau/numbers),outmin: [number](/docs/luau/numbers),outmax: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [max](#max)(x: [number](/docs/luau/numbers),...: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [min](#min)(x: [number](/docs/luau/numbers),...: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [modf](#modf)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [noise](#noise)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [pow](#pow)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [rad](#rad)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [random](#random)(m: [number](/docs/luau/numbers),n: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [randomseed](#randomseed)(x: [number](/docs/luau/numbers)):() |
| [round](#round)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [sign](#sign)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [sin](#sin)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [sinh](#sinh)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [sqrt](#sqrt)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [tan](#tan)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [tanh](#tanh)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |

Properties

|  |
| --- |
| [huge](#huge):[number](/docs/luau/numbers) |
| [pi](#pi):[number](/docs/luau/numbers) |

This library is an interface to the standard C math library, providing all of
its functions inside the [math](/docs/reference/engine/libraries/math) table.

---

API Reference

Functions

abs

Returns the absolute value of x.

math.abs(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the absolute value of x.

Provide feedback

---

acos

Returns the arc cosine of x.

math.acos(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the arc cosine of x.

Provide feedback

---

asin

Returns the arc sine of x.

math.asin(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the arc sine of x.

Provide feedback

---

atan

Returns the arc tangent of x in radians.

math.atan(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the arc tangent of x in radians.

Provide feedback

---

atan2

Returns the arc tangent of y/x (in radians) while using the signs of
both parameters to find the quadrant of the result.

math.atan2(

y:[number](/docs/luau/numbers), x:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| y:[number](/docs/luau/numbers) |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the arc tangent of y/x (in radians) while using the signs of
both parameters to find the quadrant of the result. It also handles
correctly the case of x being zero.

Provide feedback

---

ceil

Returns the smallest integer larger than or equal to x.

math.ceil(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the smallest integer larger than or equal to x.

Provide feedback

---

clamp

Returns a number between min and max, inclusive.

math.clamp(

x:[number](/docs/luau/numbers), min:[number](/docs/luau/numbers), max:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| min:[number](/docs/luau/numbers) |
| max:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns a number between min and max, inclusive.

Provide feedback

---

cos

Returns the cosine of x, assumed to be in radians.

math.cos(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the cosine of x, assumed to be in radians.

Provide feedback

---

cosh

Returns the hyperbolic cosine of x.

math.cosh(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the hyperbolic cosine of x.

Provide feedback

---

deg

Returns the angle x (given in radians) in degrees.

math.deg(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the angle x (given in radians) in degrees.

Provide feedback

---

exp

Returns the value e^x.

math.exp(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the value e^x.

Provide feedback

---

floor

Returns the largest integer smaller than or equal to x.

math.floor(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the largest integer smaller than or equal to x.

Provide feedback

---

fmod

Returns the remainder of the division of x by y that rounds the
quotient towards zero.

math.fmod(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the remainder of the division of x by y that rounds the
quotient towards zero.

Provide feedback

---

frexp

Returns m and e such that x = m\*2^e.

math.frexp(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers)

Returns m and e such that x = m\*2^e. e is an integer and
the absolute value of m is in the range of 0.5 to 1 (inclusive of
0.5 but exclusive of 1), or zero when x is zero.

Provide feedback

---

ldexp

Returns x\*2^e (e should be an integer).

math.ldexp(

x:[number](/docs/luau/numbers), e:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| e:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns x\*2^e (e should be an integer).

Provide feedback

---

lerp

Returns the linear interpolation between a and b.

math.lerp(

a:[number](/docs/luau/numbers), b:[number](/docs/luau/numbers), t:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| a:[number](/docs/luau/numbers)  The starting value. |
| b:[number](/docs/luau/numbers)  The ending value. |
| t:[number](/docs/luau/numbers)  The interpolation factor, typically between 0 and 1. |

Returns

[number](/docs/luau/numbers)

The interpolated value between a and b.

Returns the linear interpolation between a and b based on the factor
t.

This function uses the formula a+(b-a)\*t. t is typically between
0 and 1 but values outside this range are acceptable.

Provide feedback

---

log

Returns the logarithm of x using the given base.

math.log(

x:[number](/docs/luau/numbers), base:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| base:[number](/docs/luau/numbers) Default Value: 2.7182818 The base of the logarithm, the constant e by default. |

Returns

[number](/docs/luau/numbers)

Returns the logarithm of x using the given base, or the mathematical
constant e if no base is provided (natural logarithm).

Provide feedback

---

log10

Returns the base-10 logarithm of x.

math.log10(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the base-10 logarithm of x.

Provide feedback

---

map

Returns the value of x mapped from one range to another.

math.map(

x:[number](/docs/luau/numbers), inmin:[number](/docs/luau/numbers), inmax:[number](/docs/luau/numbers), outmin:[number](/docs/luau/numbers), outmax:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The number to be mapped. |
| inmin:[number](/docs/luau/numbers)  The lower bound of the input range. |
| inmax:[number](/docs/luau/numbers)  The upper bound of the input range. |
| outmin:[number](/docs/luau/numbers)  The lower bound of the output range. |
| outmax:[number](/docs/luau/numbers)  The upper bound of the output range. |

Returns

[number](/docs/luau/numbers)

The value of x mapped to the output range.

Returns a value that represents x mapped linearly from the input range
(inmin to inmax) to the output range (outmin to outmax). This is
achieved by determining the relative position of x within the input
range and applying that ratio to the output range.

Provide feedback

---

max

Returns the maximum value among the numbers passed to the function.

math.max(

x:[number](/docs/luau/numbers), ...:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| ...:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the maximum value among the numbers passed to the function.

Provide feedback

---

min

Returns the minimum value among the numbers passed to the function.

math.min(

x:[number](/docs/luau/numbers), ...:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| ...:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the minimum value among the numbers passed to the function.

Provide feedback

---

modf

Returns two numbers: the integral part of x and the fractional part of
x.

math.modf(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers)

Returns two numbers: the integral part of x and the fractional part of
x.

Provide feedback

---

noise

Returns a Perlin noise value.

math.noise(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) Default Value: 0 |
| z:[number](/docs/luau/numbers) Default Value: 0 |

Returns

[number](/docs/luau/numbers)

Returns a Perlin noise value. The returned value is most often between the
range of -1 to 1 (inclusive) but sometimes may be outside that range;
if the interval is critical to you, use [math.clamp(noise, -1, 1)](/docs/reference/engine/libraries/math#clamp)
on the output.

If you leave arguments out, they will be interpreted as zero, so
[math.noise(1.158)](/docs/reference/engine/libraries/math#noise) is equivalent to
[math.noise(1.158, 0, 0)](/docs/reference/engine/libraries/math#noise) and [math.noise(1.158, 5.723)](/docs/reference/engine/libraries/math#noise)
is equivalent to [math.noise(1.158, 5.723, 0)](/docs/reference/engine/libraries/math#noise).

Note that this function uses a Perlin noise algorithm to assign fixed
values to coordinates. For example, [math.noise(1.158, 5.723)](/docs/reference/engine/libraries/math#noise)
will always return 0.48397532105446 and [math.noise(1.158, 6)](/docs/reference/engine/libraries/math#noise)
will always return 0.15315161645412.

If x, y, and z are all integers, the return value will be 0. For
fractional values of x, y, and z, the return value will gradually
fluctuate between -0.5 and 0.5. For coordinates that are close to each
other, the return values will also be close to each other.

Provide feedback

---

pow

Returns x^y.

math.pow(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns x^y (you can also use the expression x^y to compute this
value).

Provide feedback

---

rad

Returns the angle x (given in degrees) in radians.

math.rad(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the angle x (given in degrees) in radians.

Provide feedback

---

random

Returns a random number within the range provided.

math.random(

m:[number](/docs/luau/numbers), n:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| m:[number](/docs/luau/numbers) Default Value: 0 |
| n:[number](/docs/luau/numbers) Default Value: 1 |

Returns

[number](/docs/luau/numbers)

When called without arguments, returns a uniform pseudo-random real number
in the range of 0 to 1 (inclusive of 0 but exclusive of 1).

When called with an integer number m, returns a uniform pseudo-random
integer in the range of 1 to m, inclusive.

When called with two integer numbers m and n, returns a uniform
pseudo-random integer in the range of m to n, inclusive.

Internally, this uses a 32-bit PCG (Permuted Congruential Generator) which
achieves excellent statistical performance and makes its output hard to
predict.

Provide feedback

---

randomseed

Sets x as the seed for the pseudo-random generator.

math.randomseed(x:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

()

Sets x as the seed for the pseudo-random generator: equal seeds produce
equal sequences of numbers.

Provide feedback

---

round

Returns the integer with the smallest difference between it and the given
number.

math.round(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The value to be rounded. |

Returns

[number](/docs/luau/numbers)

Returns the integer with the smallest difference between it and the given
number. For example, the value 5.8 returns 6.

For values like 0.5 that are equidistant to two integers, the value with
the greater difference between it and zero is chosen. In other words, the
function "rounds away from zero" such that 0.5 rounds to 1 and -0.5
rounds to -1.

Provide feedback

---

sign

Returns -1 if x is less than 0, 0 if x equals 0, or 1 if x
is greater than 0.

math.sign(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns -1 if x is less than 0, 0 if x equals 0, or 1 if x
is greater than 0.

Provide feedback

---

sin

Returns the sine of x, assumed to be in radians.

math.sin(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the sine of x, assumed to be in radians.

Provide feedback

---

sinh

Returns the hyperbolic sine of x.

math.sinh(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the hyperbolic sine of x.

Provide feedback

---

sqrt

Returns the square root of x.

math.sqrt(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the square root of x. You can also use the expression x^0.5
to compute this value.

Provide feedback

---

tan

Returns the tangent of x, assumed to be in radians.

math.tan(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the tangent of x, assumed to be in radians.

Provide feedback

---

tanh

Returns the hyperbolic tangent of x.

math.tanh(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the hyperbolic tangent of x.

Provide feedback

---

Properties

huge

Returns a value larger than or equal to any other numerical value (about
21024).

math.huge:[number](/docs/luau/numbers)

Returns a value larger than or equal to any other numerical value (about
21024). Dividing a positive number by zero yields this same
value.

Provide feedback

---

pi

The value of pi.

math.pi:[number](/docs/luau/numbers)

The value of pi.

Provide feedback

---