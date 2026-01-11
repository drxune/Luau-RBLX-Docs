# Random | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Random
Scraped: 2026-01-11T02:42:18.651713Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Random](/docs/reference/engine/datatypes/Random)

English

Feedback

Engine Data Type

Random

Generates pseudorandom numbers and directions.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(seed: [number](/docs/luau/numbers)) |

Methods

|  |
| --- |
| [NextInteger](#NextInteger)(min: [number](/docs/luau/numbers),max: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [NextNumber](#NextNumber)():[number](/docs/luau/numbers) |
| [NextNumber](#NextNumber-min-max)(min: [number](/docs/luau/numbers),max: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [Shuffle](#Shuffle)(tb: [table](/docs/luau/tables)):() |
| [NextUnitVector](#NextUnitVector)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Clone](#Clone)():[Random](/docs/reference/engine/datatypes/Random) |

The [Random](/docs/reference/engine/datatypes/Random) data type generates pseudorandom numbers and directions.

---

API Reference

Constructors

new

Returns a new pseudorandom generator using an optional seed.

Random.new(seed:[number](/docs/luau/numbers))

Parameters

|  |
| --- |
| seed:[number](/docs/luau/numbers) |

Returns a new [Random](/docs/reference/engine/datatypes/Random) object. If you don't provide the seed
parameter, [Random](/docs/reference/engine/datatypes/Random) uses a seed from an internal entropy source.

If you provide a seed, it should be within the range [-9007199254740991,
9007199254740991], and [Random](/docs/reference/engine/datatypes/Random) will round it down to the
nearest integer. So seeds of 0, 0.99, and [math.random()](/docs/reference/engine/libraries/math#random) all
produce identical generators. If you need to generate a seed and store it
for later retrieval, use [math.random(max)](/docs/reference/engine/libraries/math#random).

Provide feedback

---

Methods

NextInteger

Returns a pseudorandom integer uniformly distributed over [min, max].

Random:NextInteger(

min:[number](/docs/luau/numbers), max:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| min:[number](/docs/luau/numbers) |
| max:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns a pseudorandom integer uniformly distributed over [min, max].

Provide feedback

---

NextNumber

Returns a pseudorandom number uniformly distributed over [0, 1].

Random:NextNumber():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns a uniform pseudorandom real number in the range of 0 to 1,
inclusive.

Provide feedback

---

NextNumber

Returns a pseudorandom number uniformly distributed over [min, max].

Random:NextNumber(

min:[number](/docs/luau/numbers), max:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| min:[number](/docs/luau/numbers) |
| max:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns a uniform pseudorandom real number in the range of min to max,
inclusive.

Provide feedback

---

Shuffle

Uniformly shuffles a table in-place.

Random:Shuffle(tb:[table](/docs/luau/tables)):()

Parameters

|  |
| --- |
| tb:[table](/docs/luau/tables) |

Returns

()

Uniformly shuffles the array part of tb in-place using NextInteger to
pick indices. If there are any nil "holes" in the array part of the
table, Shuffle throws an error, since shuffling could change the length.

The hash part of tb is ignored. No metamethods of tb are invoked.

The shuffle is defined to be a Fisher-Yates shuffle so the number of
NextInteger calls is guaranteed to be consistent between engine versions
for a given size of table.

Provide feedback

---

NextUnitVector

Returns a unit vector with a pseudorandom direction.

Random:NextUnitVector():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

A unit vector with a pseudorandom direction.

Returns a unit vector with a pseudorandom direction. Vectors returned from
this function are uniformly distributed over the unit sphere.

Provide feedback

---

Clone

Returns a new Random object with the same state as the original.

Random:Clone():[Random](/docs/reference/engine/datatypes/Random)

Returns

[Random](/docs/reference/engine/datatypes/Random)

Returns a new Random object with the same state as the original.

Provide feedback

---