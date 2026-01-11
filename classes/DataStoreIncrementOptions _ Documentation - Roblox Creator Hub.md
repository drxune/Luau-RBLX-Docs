# DataStoreIncrementOptions | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreIncrementOptions
Scraped: 2026-01-11T02:28:20.226647Z

## Tags
- Not Replicated

## Inherits
- Instance
- DataStoreIncrementOptions
- GlobalDataStore:IncrementAsync()
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions)

English

Feedback

Engine Class

DataStoreIncrementOptions

Specifies additional parameters for a [GlobalDataStore:IncrementAsync()](/docs/reference/engine/classes/GlobalDataStore#IncrementAsync)
call.

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetMetadata](#GetMetadata)():[Dictionary](/docs/luau/tables#dictionaries) |
| [SetMetadata](#SetMetadata)(attributes: [Dictionary](/docs/luau/tables#dictionaries)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object that specifies additional parameters for a
[GlobalDataStore:IncrementAsync()](/docs/reference/engine/classes/GlobalDataStore#IncrementAsync) call.

See also:

* [Data Stores](/docs/cloud-services/data-stores), an in-depth
  guide on data structure, management, error handling, etc.

---

API Reference

Methods

GetMetadata

Gets the custom metadata set with this [DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions)
instance.

DataStoreIncrementOptions:GetMetadata():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Metadata associated with this [DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions)
instance.

This function gets custom metadata associated with this
[DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions) instance.

Provide feedback

---

SetMetadata

Sets custom metadata to be associated with the key.

DataStoreIncrementOptions:SetMetadata(attributes:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| attributes:[Dictionary](/docs/luau/tables#dictionaries)  Metadata values to set for the key. |

Returns

()

This function sets custom metadata used by
[GlobalDataStore:IncrementAsync()](/docs/reference/engine/classes/GlobalDataStore#IncrementAsync) to associate metadata with a key.
Metadata should be in key-value pair form.

Provide feedback

---