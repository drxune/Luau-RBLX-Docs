# DataStoreSetOptions | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreSetOptions
Scraped: 2026-01-11T02:36:38.495445Z

## Tags
- Not Replicated

## Inherits
- Instance
- DataStoreSetOptions
- GlobalDataStore:SetAsync()
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions)

English

Feedback

Engine Class

DataStoreSetOptions

Specifies additional parameters for a [GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) call.

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
[GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) call.

See also:

* [Data Stores](/docs/cloud-services/data-stores), an in-depth
  guide on data structure, management, error handling, etc.

---

API Reference

Methods

GetMetadata

Gets the custom metadata set with this [DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions)
instance.

DataStoreSetOptions:GetMetadata():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Metadata associated with this [DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions) instance.

This function gets custom metadata associated with this
[DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions) instance.

Provide feedback

---

SetMetadata

Sets custom metadata to be associated with the key.

DataStoreSetOptions:SetMetadata(attributes:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| attributes:[Dictionary](/docs/luau/tables#dictionaries)  Metadata values to set for the key. |

Returns

()

This function sets custom metadata used by
[GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) to associate metadata with a key.
Metadata should be in key-value pair form.

Provide feedback

---