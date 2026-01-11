# NumberSequence | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/NumberSequence
Scraped: 2026-01-11T02:42:01.250140Z

## Inherits
- ParticleEmitter.Size
- Beam.Transparency
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

English

Feedback

Engine Data Type

NumberSequence

A series of floats across a period of time.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(n: [number](/docs/luau/numbers)) |
| [new](#new-n0-n1)(n0: [number](/docs/luau/numbers),n1: [number](/docs/luau/numbers)) |
| [new](#new-Keypoints)(Keypoints: [Array](/docs/luau/tables#arrays)) |

Properties

|  |
| --- |
| [Keypoints](#Keypoints):[Array](/docs/luau/tables#arrays) |

The [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) data type represents a series of number values
from 0 to 1. The number values are expressed using the
[NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint) type. This type is used in properties such
as [ParticleEmitter.Size](/docs/reference/engine/classes/ParticleEmitter#Size) and [Beam.Transparency](/docs/reference/engine/classes/Beam#Transparency) to define a
numerical change over time.

#### Equality

Two [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) objects are equivalent only if the values of
their [NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint) are equivalent, even if both would
result in similar graphs.

#### Evaluation

The [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) type does not have a built-in method for getting
the value at a certain time/point because keypoints can have random envelopes.
However, assuming the envelope values of your keypoints are all 0, you can
use the following function to evaluate at a specific time.

```
local function evalNumberSequence(sequence: NumberSequence, time: number)



-- If time is 0 or 1, return the first or last value respectively



if time == 0 then



return sequence.Keypoints[1].Value



elseif time == 1 then



return sequence.Keypoints[#sequence.Keypoints].Value



end



-- Otherwise, step through each sequential pair of keypoints



for i = 1, #sequence.Keypoints - 1 do



local currKeypoint = sequence.Keypoints[i]



local nextKeypoint = sequence.Keypoints[i + 1]



if time >= currKeypoint.Time and time < nextKeypoint.Time then



-- Calculate how far alpha lies between the points



local alpha = (time - currKeypoint.Time) / (nextKeypoint.Time - currKeypoint.Time)



-- Return the value between the points using alpha



return currKeypoint.Value + (nextKeypoint.Value - currKeypoint.Value) * alpha



end



end



end



local numberSequence = NumberSequence.new{



NumberSequenceKeypoint.new(0, 0),



NumberSequenceKeypoint.new(0.5, 1),



NumberSequenceKeypoint.new(1, 0),



}



print(evalNumberSequence(numberSequence, 0.65))  --> 0.7
```

---

API Reference

Constructors

new

Returns a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) with the start and end values set to the
provided n.

NumberSequence.new(n:[number](/docs/luau/numbers))

Parameters

|  |
| --- |
| n:[number](/docs/luau/numbers) |

Returns a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) with the start and end values set to
the provided n.

```
local numberSequence = NumberSequence.new(n)



-- Equivalent to



local numberSequence = NumberSequence.new{



NumberSequenceKeypoint.new(0, n),



NumberSequenceKeypoint.new(1, n)



}
```

Provide feedback

---

new

Returns a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) of two keypoints with n0 as the start value
and n1 as the end value.

NumberSequence.new(

n0:[number](/docs/luau/numbers), n1:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| n0:[number](/docs/luau/numbers) |
| n1:[number](/docs/luau/numbers) |

Returns a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) of two keypoints with n0 as the start value
and n1 as the end value.

```
local numberSequence = NumberSequence.new(n0, n1)



-- Equivalent to



local numberSequence = NumberSequence.new{



NumberSequenceKeypoint.new(0, n0),



NumberSequenceKeypoint.new(1, n1)



}
```

Provide feedback

---

new

Returns a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) from an array of
[NumberSequenceKeypoints](/docs/reference/engine/datatypes/NumberSequenceKeypoint).

NumberSequence.new(Keypoints:[Array](/docs/luau/tables#arrays))

Parameters

|  |
| --- |
| Keypoints:[Array](/docs/luau/tables#arrays) |

Returns a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) from an array of
[NumberSequenceKeypoints](/docs/reference/engine/datatypes/NumberSequenceKeypoint). The keypoints
must be provided in a non-descending time value order. At least two keypoints must
be provided, and they must have a time value of 0 (first) and 1
(last).

```
local numberSequence = NumberSequence.new{



NumberSequenceKeypoint.new(0, 0),



NumberSequenceKeypoint.new(0.5, 0.5, 0.25),



NumberSequenceKeypoint.new(1, 1)



}
```

Provide feedback

---

Properties

Keypoints

An array of [NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint) values in ascending order.

NumberSequence.Keypoints:[Array](/docs/luau/tables#arrays)

An array containing [NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint) values for the
[NumberSequence](/docs/reference/engine/datatypes/NumberSequence).

Provide feedback

---