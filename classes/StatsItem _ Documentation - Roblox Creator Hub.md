# StatsItem | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StatsItem
Scraped: 2026-01-11T02:35:22.246150Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- StatsItem
- RunningAverageItemDouble
- RunningAverageItemInt
- RunningAverageTimeIntervalItem
- TotalCountTimeIntervalItem
- Stats
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StatsItem](/docs/reference/engine/classes/StatsItem)

English

Feedback

Engine Class

StatsItem

A single performance metric.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [DisplayName](#DisplayName):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetValue](#GetValue)():[number](/docs/luau/numbers) |
| [GetValueString](#GetValueString)():[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[RunningAverageItemDouble](/docs/reference/engine/classes/RunningAverageItemDouble), [RunningAverageItemInt](/docs/reference/engine/classes/RunningAverageItemInt), [RunningAverageTimeIntervalItem](/docs/reference/engine/classes/RunningAverageTimeIntervalItem), [TotalCountTimeIntervalItem](/docs/reference/engine/classes/TotalCountTimeIntervalItem)

A StatsItem is an internal measurement item that is created by the engine to
benchmark many of the backend components of Roblox. It cannot be created using
[Instance.new()](/docs/reference/engine/datatypes/Instance#new), but its value can be read by plugins. They can be
found stored inside of the [Stats](/docs/reference/engine/classes/Stats) service.

---

API Reference

Properties

DisplayName

Hidden

Read Only

Not Replicated

Plugin Security

Read Parallel

StatsItem.DisplayName:[string](/docs/luau/strings)

Provide feedback

---

Methods

GetValue

Plugin Security

Returns the StatsItem's value.

StatsItem:GetValue():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the StatsItem's value.

Provide feedback

---

GetValueString

Plugin Security

Returns the StatsItem's value as a formatted string.

StatsItem:GetValueString():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

Returns the StatsItem's value as a formatted string.

Provide feedback

---