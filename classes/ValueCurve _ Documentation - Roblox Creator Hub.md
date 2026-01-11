# ValueCurve | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ValueCurve
Scraped: 2026-01-11T02:35:12.612411Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- ValueCurve
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ValueCurve](/docs/reference/engine/classes/ValueCurve)

English

Feedback

Engine Class

ValueCurve

A sorted list of time-value pairs that define a curve. Used to animate a any
type of value.

---

Summary

Properties

|  |
| --- |
| [Length](#Length):[number](/docs/luau/numbers) |
| [ValueType](#ValueType):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetKeyAtIndex](#GetKeyAtIndex)(index: [number](/docs/luau/numbers)):[ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey) |
| [GetKeyIndicesAtTime](#GetKeyIndicesAtTime)(time: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetKeys](#GetKeys)():[Array](/docs/luau/tables#arrays) |
| [GetValueAtTime](#GetValueAtTime)(time: [number](/docs/luau/numbers)):Variant? |
| [InsertKey](#InsertKey)(key: [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey)):[Array](/docs/luau/tables#arrays) |
| [InsertKeyValue](#InsertKeyValue)(time: [number](/docs/luau/numbers),value: Variant,Interpolation: [Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)):[Array](/docs/luau/tables#arrays) |
| [RemoveKeyAtIndex](#RemoveKeyAtIndex)(startingIndex: [number](/docs/luau/numbers),count: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [SetKeys](#SetKeys)(keys: [Array](/docs/luau/tables#arrays)):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An instance representing a 1D value curve encoded via a sorted list of
[ValueCurveKeys](/docs/reference/engine/datatypes/ValueCurveKey). The shape of the interpolation curve
between two keys is determined by the [ValueCurveKey.Interpolation](/docs/reference/engine/datatypes/ValueCurveKey#Interpolation)
type.

Not all value types (for example, strings and other non-numerical types) may
perform [Linear](/docs/reference/engine/enums/KeyInterpolationMode#Linear) or
[Cubic](/docs/reference/engine/enums/KeyInterpolationMode#Cubic) interpolation. These types will revert
to [Constant](/docs/reference/engine/enums/KeyInterpolationMode#Constant) interpolation if necessary.

---

API Reference

Properties

Length

Read Only

Not Replicated

Read Parallel

Number of keys in the value curve.

ValueCurve.Length:[number](/docs/luau/numbers)

Number of keys in the value curve.

Provide feedback

---

ValueType

Read Only

Not Replicated

Read Parallel

Read-only value indicating the type held in this curve.

ValueCurve.ValueType:[string](/docs/luau/strings)

Read-only value indicating the type held in this curve, or the string
"Nil" if there are no keys.

Provide feedback

---

Methods

GetKeyAtIndex

Returns a copy of a key at a given index.

ValueCurve:GetKeyAtIndex(index:[number](/docs/luau/numbers)):[ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey)

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers)  The index in the existing set of keys held by this [ValueCurve](/docs/reference/engine/classes/ValueCurve). |

Returns

[ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey)

Returns a copy of a key at a given index.

Provide feedback

---

GetKeyIndicesAtTime

Returns the index of the last and first key of a period of time.

ValueCurve:GetKeyIndicesAtTime(time:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  A time during the animation. Inputs will be clamped between 0 and the time of the last key held by this [ValueCurve](/docs/reference/engine/classes/ValueCurve). |

Returns

[Array](/docs/luau/tables#arrays)

The first item in the returned array is the index of the last key with
time less than or equal to time (or the lesser of either 1 or the
curve length if no key was found). The second item in the returned array
is the index of the first key with time greater than or equal to time
(or the curve length if no key was found satisfying the inequality).

Provide feedback

---

GetKeys

Returns a copy of all the keys in the ValueCurve as a Luau array of
[ValueCurveKeys](/docs/reference/engine/datatypes/ValueCurveKey).

ValueCurve:GetKeys():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Array of [ValueCurveKeys](/docs/reference/engine/datatypes/ValueCurveKey).

Returns a copy of all the keys in the [ValueCurve](/docs/reference/engine/classes/ValueCurve) as a Luau array
of [ValueCurveKeys](/docs/reference/engine/datatypes/ValueCurveKey).

Provide feedback

---

GetValueAtTime

Samples the value curve at a given time passed as argument.

ValueCurve:GetValueAtTime(time:[number](/docs/luau/numbers)):Variant?

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to sample the curve. |

Returns

Variant?

Value of the curve at the requested time.

Samples the value curve at a given time passed as argument.

Provide feedback

---

InsertKey

Adds the key passed as an argument to this curve. If a key at the same
time is found, it will be replaced.

ValueCurve:InsertKey(key:[ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| key:[ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey)  [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey) to insert. |

Returns

[Array](/docs/luau/tables#arrays)

(see description)

Adds the key passed as an argument to this curve. If a key at the same
time is found, it will be replaced. In the returned array, the first value
is true if a key was added or false if a previous key was replaced;
the second value is the index at which the marker was added.

If there are not yet any keys, then the key may be added. If keys exist,
the type of the value must match those of existing keys; otherwise a
message is printed and {false, -1} is returned.

Provide feedback

---

InsertKeyValue

Creates a key for the given value and inserts it at the given time. If a
key at the same time is found, it will be replaced.

ValueCurve:InsertKeyValue(

time:[number](/docs/luau/numbers), value:Variant, Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which to insert the new [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey). - type: number |
| value:Variant  Value of the inserted [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey). - type: any |
| Interpolation:[Enum.KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)  Interpolation mode of the inserted [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey). - type: KeyInterpolationMode |

Returns

[Array](/docs/luau/tables#arrays)

(see description)

Creates a [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey) from the given arguments and inserts it
in this curve. If a key at the same time is found, it will be replaced. In
the returned array, the first value is true if a key was added or
false if a previous key was replaced; the second value is the index at
which the marker was added.

If there are not yet any keys, then the key may be added. If keys exist,
the type of the value must match those of existing keys; otherwise a
message is printed and {false, -1} is returned.

Provide feedback

---

RemoveKeyAtIndex

Removes a given number of keys starting from a given index.

ValueCurve:RemoveKeyAtIndex(

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

Resets this curve's keys using the [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey) array passed
as an argument.

ValueCurve:SetKeys(keys:[Array](/docs/luau/tables#arrays)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| keys:[Array](/docs/luau/tables#arrays)  Array of [ValueCurveKeys](/docs/reference/engine/datatypes/ValueCurveKey). |

Returns

[number](/docs/luau/numbers)

Number of keys inserted.

Resets this curve's keys using the [ValueCurveKey](/docs/reference/engine/datatypes/ValueCurveKey) array passed
as an argument. Keys in the keys array are sorted in ascending time
order before insertion, and keys at duplicated times are removed in a
stable manner.

Returns the number of keys actually inserted. Keys previously stored in
this curve are removed before the keys passed as arguments are added.

The keys must all contain values of the same type. And that type must
match any existing keys. Otherwise a message is printed, the keys are not
added, and 0 is returned.

Provide feedback

---