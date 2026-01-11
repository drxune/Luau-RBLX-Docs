# MarkerCurve | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MarkerCurve
Scraped: 2026-01-11T02:33:49.055706Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- MarkerCurve
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MarkerCurve](/docs/reference/engine/classes/MarkerCurve)

English

Feedback

Engine Class

MarkerCurve

Represents a list of strings markers in chronological order.

---

Summary

Properties

|  |
| --- |
| [Length](#Length):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetMarkerAtIndex](#GetMarkerAtIndex)(index: [number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetMarkers](#GetMarkers)():[Array](/docs/luau/tables#arrays) |
| [InsertMarkerAtTime](#InsertMarkerAtTime)(time: [number](/docs/luau/numbers),marker: [string](/docs/luau/strings)):[Array](/docs/luau/tables#arrays) |
| [RemoveMarkerAtIndex](#RemoveMarkerAtIndex)(startingIndex: [number](/docs/luau/numbers),count: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The MarkerCurve instance lets you place markers as string values at certain
times on a timeline. The string at each marker cannot exceed 64 characters and
must only contain printable characters.

---

API Reference

Properties

Length

Read Only

Not Replicated

Read Parallel

Returns the number of markers in the MarkerCurve.

MarkerCurve.Length:[number](/docs/luau/numbers)

Returns the number of markers in the MarkerCurve.

Provide feedback

---

Methods

GetMarkerAtIndex

Returns the time and string value of the marker at the provided index.

MarkerCurve:GetMarkerAtIndex(index:[number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers) |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A table containing the time and value of the marker at the provided
index.

Returns the time and string value of the marker at the provided index.

Provide feedback

---

GetMarkers

Returns the time and string value of all markers in the MarkerCurve.

MarkerCurve:GetMarkers():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of tables containing the time and value of all markers in the
MarkerCurve.

Returns the time and string value of all markers in the MarkerCurve.

Provide feedback

---

InsertMarkerAtTime

Inserts a marker with the provided string value at the provided time.

MarkerCurve:InsertMarkerAtTime(

time:[number](/docs/luau/numbers), marker:[string](/docs/luau/strings)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  Time at which the marker should be added. |
| marker:[string](/docs/luau/strings)  String value associated with this marker. |

Returns

[Array](/docs/luau/tables#arrays)

A table containing a boolean and a number. The boolean is true if
the call adds a new marker and false if it modifies an existing
marker at the provided time. The number is the index of the added
marker.

Inserts a marker with the provided string value at the provided time. The
provided string cannot exceed 64 characters and must only contain
printable characters.

Provide feedback

---

RemoveMarkerAtIndex

Remove several markers in the MarkerCurve starting at the provided index.

MarkerCurve:RemoveMarkerAtIndex(

startingIndex:[number](/docs/luau/numbers), count:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| startingIndex:[number](/docs/luau/numbers)  Index of the first marker to be removed in the MarkerCurve. |
| count:[number](/docs/luau/numbers) Default Value: 1 How many markers to remove starting from the startingIndex. |

Returns

[number](/docs/luau/numbers)

How many markers were actually removed (can be less than count if the
MarkerCurve was too few markers).

Remove several markers in the MarkerCurve starting at the provided index.

Provide feedback

---