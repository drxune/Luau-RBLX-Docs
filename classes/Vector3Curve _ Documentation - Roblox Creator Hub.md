# Vector3Curve | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Vector3Curve
Scraped: 2026-01-11T02:38:55.907867Z

## Inherits
- Object
- Instance
- Vector3Curve
- FloatCurve
- Vector3Curve:X()
- Vector3Curve:Y()
- Vector3Curve:Z()
- Vector3Curve:GetValueAtTime()
- FloatCurves
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Vector3Curve](/docs/reference/engine/classes/Vector3Curve)

English

Feedback

Engine Class

Vector3Curve

Represents a 3D vector curve, grouping three [FloatCurve](/docs/reference/engine/classes/FloatCurve) instances.

---

Summary

Methods

|  |
| --- |
| [GetValueAtTime](#GetValueAtTime)(time: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [X](#X)():[FloatCurve](/docs/reference/engine/classes/FloatCurve) |
| [Y](#Y)():[FloatCurve](/docs/reference/engine/classes/FloatCurve) |
| [Z](#Z)():[FloatCurve](/docs/reference/engine/classes/FloatCurve) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Represents a 3D vector curve, grouping three [FloatCurve](/docs/reference/engine/classes/FloatCurve) instances.
Each child [FloatCurve](/docs/reference/engine/classes/FloatCurve) can be accessed via the
[Vector3Curve:X()](/docs/reference/engine/classes/Vector3Curve#X), [Vector3Curve:Y()](/docs/reference/engine/classes/Vector3Curve#Y), and
[Vector3Curve:Z()](/docs/reference/engine/classes/Vector3Curve#Z) methods. The three axes can be sampled simultaneously
via the method [Vector3Curve:GetValueAtTime()](/docs/reference/engine/classes/Vector3Curve#GetValueAtTime).

Code Samples

Creating a Vector3Curve

```
--- Vector3Curve



local function createVector3Curve()



local vectorCurve = Instance.new("Vector3Curve")



local curveX = vectorCurve:X() -- creates and returns a FloatCurve animating the X channel



local curveY = vectorCurve:Y() -- creates and returns a FloatCurve animating the Y channel



-- Not setting the Z channel will leave the Z channel not animated.



-- A missing curve or a curve with no keys don't participate in the animation



local key = FloatCurveKey.new(0, 1) -- creates a key at time 0 and with value 1



curveX:InsertKey(key)



curveY:InsertKey(key)



local key2 = FloatCurveKey.new(1, 2) -- creates a key at time 1 and with value 2



curveX:InsertKey(key2)



curveY:InsertKey(key2)



return vectorCurve



end



local function testVector3Curve()



local curve = createVector3Curve()



-- sampling the curve at a given time (returns a vector3)



print(curve:GetValueAtTime(0)) -- returns 1, 1, void



print(curve:GetValueAtTime(0.5)) -- returns 1.5, 1.5, void (result of cubic interpolation with auto tangents)



curve:X():RemoveKeyAtIndex(1)



curve:X():RemoveKeyAtIndex(1)



print(curve:X().Length) -- number of keys = 0



print(curve:GetValueAtTime(0.5)) -- returns void, 1.5, void



end



testVector3Curve()
```

---

API Reference

Methods

GetValueAtTime

Returns the three [FloatCurves](/docs/reference/engine/classes/FloatCurve) (X, Y, Z) at the passed
time argument.

Vector3Curve:GetValueAtTime(time:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to get the value. |

Returns

[Array](/docs/luau/tables#arrays)

The three [FloatCurves](/docs/reference/engine/classes/FloatCurve) (X, Y, Z) at the passed time
argument.

Returns the three [FloatCurves](/docs/reference/engine/classes/FloatCurve) (X, Y, Z) at the passed
time argument as an array of three numbers. If a channel curve is missing
or no key is found in the curve, the channel is evaluated as nil.

Provide feedback

---

X

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the X channel (the first child
instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named X).

Vector3Curve:X():[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns

[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the X channel (the first child
instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named X). If none is found, an empty
[FloatCurve](/docs/reference/engine/classes/FloatCurve) is created.

Provide feedback

---

Y

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Y channel (the first child
instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named Y).

Vector3Curve:Y():[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns

[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Y channel (the first child
instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named Y). If none is found, an empty
[FloatCurve](/docs/reference/engine/classes/FloatCurve) is created.

Provide feedback

---

Z

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Z channel (the first child
instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named Z).

Vector3Curve:Z():[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns

[FloatCurve](/docs/reference/engine/classes/FloatCurve)

Returns the [FloatCurve](/docs/reference/engine/classes/FloatCurve) controlling the Z channel (the first child
instance of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named Z). If none is found, an empty
[FloatCurve](/docs/reference/engine/classes/FloatCurve) is created.

Provide feedback

---