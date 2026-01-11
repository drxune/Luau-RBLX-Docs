# FloatCurve | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/FloatCurve
Scraped: 2026-01-11T02:41:32.913512Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- FloatCurve
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [FloatCurve](/docs/reference/engine/classes/FloatCurve)

English

Feedback

Engine Class

FloatCurve

A sorted list of time-value pairs that define a curve. Used to animate a
single numerical value.

---

Summary

Properties

|  |
| --- |
| [Length](#Length):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetKeyAtIndex](#GetKeyAtIndex)(index: [number](/docs/luau/numbers)):[FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey) |
| [GetKeyIndicesAtTime](#GetKeyIndicesAtTime)(time: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetKeys](#GetKeys)():[Array](/docs/luau/tables#arrays) |
| [GetValueAtTime](#GetValueAtTime)(time: [number](/docs/luau/numbers)):[number](/docs/luau/numbers)? |
| [InsertKey](#InsertKey)(key: [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey)):[Array](/docs/luau/tables#arrays) |
| [RemoveKeyAtIndex](#RemoveKeyAtIndex)(startingIndex: [number](/docs/luau/numbers),count: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [SetKeys](#SetKeys)(keys: [Array](/docs/luau/tables#arrays)):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An instance representing a 1D float curve encoded via a sorted list of
[FloatCurveKeys](/docs/reference/engine/datatypes/FloatCurveKey). The shape of the interpolation curve
between two keys is determined by the [FloatCurveKey.Interpolation](/docs/reference/engine/datatypes/FloatCurveKey#Interpolation)
type.

---

API Reference

Properties

Length

Read Only

Not Replicated

Read Parallel

Number of keys in the float curve.

FloatCurve.Length:[number](/docs/luau/numbers)

Number of keys in the float curve.

Provide feedback

---

Methods

GetKeyAtIndex

Returns a copy of a key at a given index.

FloatCurve:GetKeyAtIndex(index:[number](/docs/luau/numbers)):[FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey)

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers) |

Returns

[FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey)

Returns a copy of a key at a given index.

Provide feedback

---

GetKeyIndicesAtTime

Returns the index of the last and first key of a period of time.

FloatCurve:GetKeyIndicesAtTime(time:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers) |

Returns

[Array](/docs/luau/tables#arrays)

The first item in the returned array is the index of the last key with
time less than or equal to time (or the lesser of either 1 or the curve
length if no key was found). The second item in the returned array is the
index of the first key with time greater than or equal to time (or the
curve length if no key was found satisfying the inequality).

Provide feedback

---

GetKeys

Returns a copy of all the keys in the FloatCurve as a Luau array of
[FloatCurveKeys](/docs/reference/engine/datatypes/FloatCurveKey).

FloatCurve:GetKeys():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Array of [FloatCurveKeys](/docs/reference/engine/datatypes/FloatCurveKey).

Returns a copy of all the keys in the FloatCurve as a Luau array of
[FloatCurveKeys](/docs/reference/engine/datatypes/FloatCurveKey).

Provide feedback

---

GetValueAtTime

Samples the float curve at a given time passed as argument.

FloatCurve:GetValueAtTime(time:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)?

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to sample the curve. |

Returns

[number](/docs/luau/numbers)?

Value of the curve at the requested time.

Samples the float curve at a given time passed as argument.

Provide feedback

---

InsertKey

Adds the key passed as an argument to this curve. If a key at the same
time is found, it will be replaced.

FloatCurve:InsertKey(key:[FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| key:[FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey)  [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey) to insert. |

Returns

[Array](/docs/luau/tables#arrays)

(see description) .

Adds the key passed as an argument to this curve. If a key at the same
time is found, it will be replaced. In the returned array, the first value
is true if a key was added or false if a previous key was replaced;
the second value is the index at which the marker was added.

Provide feedback

---

RemoveKeyAtIndex

Removes a given number of keys starting from a given index.

FloatCurve:RemoveKeyAtIndex(

startingIndex:[number](/docs/luau/numbers), count:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| startingIndex:[number](/docs/luau/numbers)  Starting index from which to remove keys. |
| count:[number](/docs/luau/numbers) Default Value: 1 Number of keys to remove. |

Returns

[number](/docs/luau/numbers)

Number of keys removed.

Removes a given number (count) of keys starting from the startingIndex
index and returns the number of keys that were removed.

Provide feedback

---

SetKeys

Resets this curve's keys using the [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey) array passed
as an argument.

FloatCurve:SetKeys(keys:[Array](/docs/luau/tables#arrays)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| keys:[Array](/docs/luau/tables#arrays)  Array of [FloatCurveKeys](/docs/reference/engine/datatypes/FloatCurveKey). |

Returns

[number](/docs/luau/numbers)

Number of keys inserted.

Resets this curve's keys using the [FloatCurveKey](/docs/reference/engine/datatypes/FloatCurveKey) array passed
as an argument. Keys in the keys array are sorted in ascending time
order before insertion, and keys at duplicated times are removed in a
stable manner.

Returns the number of keys actually inserted. Keys previously stored in
this curve are removed before the keys passed as arguments are added.

Provide feedback

---