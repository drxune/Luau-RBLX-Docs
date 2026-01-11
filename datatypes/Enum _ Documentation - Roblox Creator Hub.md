# Enum | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Enum
Scraped: 2026-01-11T02:41:57.147805Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Enum](/docs/reference/engine/datatypes/Enum)

English

Feedback

Engine Data Type

Enum

A data type that represents an individual enum.

---

Summary

Methods

|  |
| --- |
| [GetEnumItems](#GetEnumItems)():[Array](/docs/luau/tables#arrays) |
| [FromName](#FromName)():[Enum](/docs/reference/engine/datatypes/Enum) | [nil](/docs/luau/nil) |
| [FromValue](#FromValue)():[Enum](/docs/reference/engine/datatypes/Enum) | [nil](/docs/luau/nil) |

The [Enum](/docs/reference/engine/datatypes/Enum) data type represents an individual enum in Roblox. An
individual enum can be indexed through the [Enums](/docs/reference/engine/datatypes/Enums) type, via the name
of the enum itself.

---

API Reference

Methods

GetEnumItems

Returns an array of all [EnumItem](/docs/reference/engine/datatypes/EnumItem) options available for this
enum.

Enum:GetEnumItems():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns an array of all the [EnumItem](/docs/reference/engine/datatypes/EnumItem) options available for this
enum.

Provide feedback

---

FromName

Converts an enum name to an [Enum](/docs/reference/engine/datatypes/Enum).

Enum:FromName():[Enum](/docs/reference/engine/datatypes/Enum) | [nil](/docs/luau/nil)

Returns

[Enum](/docs/reference/engine/datatypes/Enum) | [nil](/docs/luau/nil)

Returns either the converted [Enum](/docs/reference/engine/datatypes/Enum) or nil.

Provide feedback

---

FromValue

Converts an enum value to an [Enum](/docs/reference/engine/datatypes/Enum).

Enum:FromValue():[Enum](/docs/reference/engine/datatypes/Enum) | [nil](/docs/luau/nil)

Returns

[Enum](/docs/reference/engine/datatypes/Enum) | [nil](/docs/luau/nil)

Returns either the converted [Enum](/docs/reference/engine/datatypes/Enum) or nil.

Provide feedback

---