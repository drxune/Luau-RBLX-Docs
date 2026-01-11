# ColorSequence | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/ColorSequence
Scraped: 2026-01-11T02:42:38.341893Z

## Inherits
- ParticleEmitter
- Trail
- Beam
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [ColorSequence](/docs/reference/engine/datatypes/ColorSequence)

English

Feedback

Engine Data Type

ColorSequence

A gradient of color values comprised of
[ColorSequenceKeypoints](/docs/reference/engine/datatypes/ColorSequenceKeypoint).

---

Summary

Constructors

|  |
| --- |
| [new](#new)(c: [Color3](/docs/reference/engine/datatypes/Color3)) |
| [new](#new-c0-c1)(c0: [Color3](/docs/reference/engine/datatypes/Color3),c1: [Color3](/docs/reference/engine/datatypes/Color3)) |
| [new](#new-keypoints)(keypoints: [Array](/docs/luau/tables#arrays)) |

Properties

|  |
| --- |
| [Keypoints](#Keypoints):[Array](/docs/luau/tables#arrays) |

The [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) data type represents a gradient of color values
from 0 to 1. The color values are expressed using the
[ColorSequenceKeypoint](/docs/reference/engine/datatypes/ColorSequenceKeypoint) type. This type is used in various properties
of [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter), [Trail](/docs/reference/engine/classes/Trail), [Beam](/docs/reference/engine/classes/Beam), and other objects
that use color gradients.

#### Equality

Two [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) objects are equivalent only if the values of
their [ColorSequenceKeypoint](/docs/reference/engine/datatypes/ColorSequenceKeypoint) are equivalent, even if both would
result in similar gradients.

#### Evaluation

The [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) type does not have a built-in method for getting
the value at a certain time/point. However, you can use the following function
to evaluate at a specific time.

```
local function evalColorSequence(sequence: ColorSequence, time: number)



-- If time is 0 or 1, return the first or last value respectively



if time == 0 then



return sequence.Keypoints[1].Value



elseif time == 1 then



return sequence.Keypoints[#sequence.Keypoints].Value



end



-- Otherwise, step through each sequential pair of keypoints



for i = 1, #sequence.Keypoints - 1 do



local thisKeypoint = sequence.Keypoints[i]



local nextKeypoint = sequence.Keypoints[i + 1]



if time >= thisKeypoint.Time and time < nextKeypoint.Time then



-- Calculate how far alpha lies between the points



local alpha = (time - thisKeypoint.Time) / (nextKeypoint.Time - thisKeypoint.Time)



-- Evaluate the real value between the points using alpha



return Color3.new(



(nextKeypoint.Value.R - thisKeypoint.Value.R) * alpha + thisKeypoint.Value.R,



(nextKeypoint.Value.G - thisKeypoint.Value.G) * alpha + thisKeypoint.Value.G,



(nextKeypoint.Value.B - thisKeypoint.Value.B) * alpha + thisKeypoint.Value.B



)



end



end



end



local colorSequence = ColorSequence.new{



ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 0, 0)),



ColorSequenceKeypoint.new(0.5, Color3.fromRGB(0, 190, 200)),



ColorSequenceKeypoint.new(1, Color3.fromRGB(190, 0, 255))



}



print(evalColorSequence(colorSequence, 0.75))  --> 0.372549, 0.372549, 0.892157
```

---

API Reference

Constructors

new

Returns a new [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) that is entirely the specified color.

ColorSequence.new(c:[Color3](/docs/reference/engine/datatypes/Color3))

Parameters

|  |
| --- |
| c:[Color3](/docs/reference/engine/datatypes/Color3) |

Returns a sequence of two keypoints with c for both the start and end
values.

```
local colorSequence = ColorSequence.new(c)



-- Equivalent to



local colorSequence = ColorSequence.new{



ColorSequenceKeypoint.new(0, c),



ColorSequenceKeypoint.new(1, c)



}
```

Provide feedback

---

new

Returns a new [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) with c0 as the start value and c1 as the
end value.

ColorSequence.new(

c0:[Color3](/docs/reference/engine/datatypes/Color3), c1:[Color3](/docs/reference/engine/datatypes/Color3) )

Parameters

|  |
| --- |
| c0:[Color3](/docs/reference/engine/datatypes/Color3) |
| c1:[Color3](/docs/reference/engine/datatypes/Color3) |

Returns a new [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) with c0 as the start value and c1 as the
end value.

```
local colorSequence = ColorSequence.new(c0, c1)



-- Equivalent to



local colorSequence = ColorSequence.new{



ColorSequenceKeypoint.new(0, c0),



ColorSequenceKeypoint.new(1, c1)



}
```

Provide feedback

---

new

Returns a new [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) from an array of
[ColorSequenceKeypoints](/docs/reference/engine/datatypes/ColorSequenceKeypoint).

ColorSequence.new(keypoints:[Array](/docs/luau/tables#arrays))

Parameters

|  |
| --- |
| keypoints:[Array](/docs/luau/tables#arrays) |

Returns a new [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) from an array of
[ColorSequenceKeypoints](/docs/reference/engine/datatypes/ColorSequenceKeypoint). The keypoints
must be in a non-descending time value order. At least two keypoints must
be provided, and they must have a time value of 0 (first) and 1
(last).

```
local red = Color3.fromRGB(255, 0, 0)



local cyan = Color3.fromRGB(0, 190, 200)



local purple = Color3.fromRGB(190, 0, 255)



local colorSequence = ColorSequence.new{



ColorSequenceKeypoint.new(0, red),



ColorSequenceKeypoint.new(0.5, cyan),



ColorSequenceKeypoint.new(1, purple)



}
```

Provide feedback

---

Properties

Keypoints

An array of [ColorSequenceKeypoint](/docs/reference/engine/datatypes/ColorSequenceKeypoint) values in ascending order.

ColorSequence.Keypoints:[Array](/docs/luau/tables#arrays)

An array containing [ColorSequenceKeypoint](/docs/reference/engine/datatypes/ColorSequenceKeypoint) values for the
[ColorSequence](/docs/reference/engine/datatypes/ColorSequence).

Provide feedback

---