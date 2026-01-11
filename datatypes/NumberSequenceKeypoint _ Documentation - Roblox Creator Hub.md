# NumberSequenceKeypoint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/NumberSequenceKeypoint
Scraped: 2026-01-11T02:42:39.156788Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint)

English

Feedback

Engine Data Type

NumberSequenceKeypoint

Represents keypoint within a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) with a particular time,
value, and envelope size.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(time: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)) |
| [new](#new-time-value)(time: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers),envelope: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [Envelope](#Envelope):[number](/docs/luau/numbers) |
| [Time](#Time):[number](/docs/luau/numbers) |
| [Value](#Value):[number](/docs/luau/numbers) |

The [NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint) data type represents keypoints within a
NumberSequence with a particular time, value, and envelope size.

---

API Reference

Constructors

new

Returns a keypoint with the specified time and value.

NumberSequenceKeypoint.new(

time:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers) |
| value:[number](/docs/luau/numbers) |

Returns a keypoint with a specified time and value.

Provide feedback

---

new

Returns a keypoint with the specified time, value, and envelope.

NumberSequenceKeypoint.new(

time:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers), envelope:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers) |
| value:[number](/docs/luau/numbers) |
| envelope:[number](/docs/luau/numbers) |

Returns a keypoint with a specified time, value, and envelope.

Provide feedback

---

Properties

Envelope

The amount of variance allowed from the value.

NumberSequenceKeypoint.Envelope:[number](/docs/luau/numbers)

The amount of variance allowed from the value. A computed value.

Provide feedback

---

Time

The relative time at which the keypoint is positioned.

NumberSequenceKeypoint.Time:[number](/docs/luau/numbers)

The relative time at which the keypoint is positioned.

Provide feedback

---

Value

The base value of the keypoint.

NumberSequenceKeypoint.Value:[number](/docs/luau/numbers)

The base value of this keypoint.

Provide feedback

---