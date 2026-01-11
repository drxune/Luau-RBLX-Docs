# RotationCurve | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RotationCurve
Scraped: 2026-01-11T02:27:43.569592Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- RotationCurve
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [RotationCurve](/docs/reference/engine/classes/RotationCurve)

English

Feedback

Engine Class

RotationCurve

Represents a sequence of rotations and the interpolation curve between them.

---

Summary

Properties

|  |
| --- |
| [Length](#Length):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetKeyAtIndex](#GetKeyAtIndex)(index: [number](/docs/luau/numbers)):[RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey) |
| [GetKeyIndicesAtTime](#GetKeyIndicesAtTime)(time: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetKeys](#GetKeys)():[Array](/docs/luau/tables#arrays) |
| [GetValueAtTime](#GetValueAtTime)(time: [number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame)? |
| [InsertKey](#InsertKey)(key: [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey)):[Array](/docs/luau/tables#arrays) |
| [RemoveKeyAtIndex](#RemoveKeyAtIndex)(startingIndex: [number](/docs/luau/numbers),count: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [SetKeys](#SetKeys)(keys: [Array](/docs/luau/tables#arrays)):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This class holds a sorted list of
[RotationCurveKeys](/docs/reference/engine/datatypes/RotationCurveKey) that represent a sequence of
rotations. The shape of the interpolation curve between two keys is determined
by the [RotationCurveKey.Interpolation](/docs/reference/engine/datatypes/RotationCurveKey#Interpolation) type.

---

API Reference

Properties

Length

Read Only

Not Replicated

Read Parallel

Number of rotation keys in this curve.

RotationCurve.Length:[number](/docs/luau/numbers)

Number of rotation keys in this curve.

Provide feedback

---

Methods

GetKeyAtIndex

Returns a copy of a key at a given index.

RotationCurve:GetKeyAtIndex(index:[number](/docs/luau/numbers)):[RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey)

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers) |

Returns

[RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey)

Returns a copy of a key at a given index.

Provide feedback

---

GetKeyIndicesAtTime

Returns the index of the last and first key of a period of time.

RotationCurve:GetKeyIndicesAtTime(time:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

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

Returns a copy of all the keys in the rotation curve as a Luau array of
[RotationCurveKeys](/docs/reference/engine/datatypes/RotationCurveKey).

RotationCurve:GetKeys():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Array of [RotationCurveKeys](/docs/reference/engine/datatypes/RotationCurveKey).

Returns a copy of all the keys in the rotation curve as a Luau array of
[RotationCurveKeys](/docs/reference/engine/datatypes/RotationCurveKey).

Provide feedback

---

GetValueAtTime

Samples the rotation curve at a given time and returns the corresponding
rotation as a [CFrame](/docs/reference/engine/datatypes/CFrame).

RotationCurve:GetValueAtTime(time:[number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame)?

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to sample the curve. |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)?

Value of the curve at the requested time.

Samples the rotation curve at a given time and returns the corresponding
rotation as a [CFrame](/docs/reference/engine/datatypes/CFrame). Empty rotation curves are evaluated as
[CFrame.identity](/docs/reference/engine/datatypes/CFrame#identity).

Provide feedback

---

InsertKey

Adds the key passed as an argument to this curve. If a key at the same
time is found, it will be replaced.

RotationCurve:InsertKey(key:[RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| key:[RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey)  [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey) to insert. |

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

RotationCurve:RemoveKeyAtIndex(

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

Resets this curve's keys using the [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey) array
passed as an argument.

RotationCurve:SetKeys(keys:[Array](/docs/luau/tables#arrays)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| keys:[Array](/docs/luau/tables#arrays)  Array of [RotationCurveKeys](/docs/reference/engine/datatypes/RotationCurveKey). |

Returns

[number](/docs/luau/numbers)

Number of keys inserted.

Resets this curve's keys using the [RotationCurveKey](/docs/reference/engine/datatypes/RotationCurveKey) array
passed as an argument. Keys in the keys array are sorted in ascending
time order before insertion, and keys at duplicated times are removed in a
stable manner.

Returns the number of keys actually inserted. Keys previously stored in
this curve are removed before the keys passed as arguments are added.

Provide feedback

---