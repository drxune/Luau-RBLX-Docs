# DataStoreKeyInfo | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreKeyInfo
Scraped: 2026-01-11T02:40:58.864994Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- DataStoreKeyInfo
- Object
- GlobalDataStore:GetAsync()
- GlobalDataStore:UpdateAsync()
- GlobalDataStore:IncrementAsync()
- GlobalDataStore:RemoveAsync()
- DataStore:GetVersionAsync()
- DataStore:RemoveVersionAsync()
- UserIds
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo)

English

Feedback

Engine Class

DataStoreKeyInfo

An object specifying information about a particular version of the key.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [CreatedTime](#CreatedTime):[number](/docs/luau/numbers) |
| [UpdatedTime](#UpdatedTime):[number](/docs/luau/numbers) |
| [Version](#Version):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetMetadata](#GetMetadata)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetUserIds](#GetUserIds)():[Array](/docs/luau/tables#arrays) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object describing information about a particular version of the key. This
is returned as the second return value by [GlobalDataStore:GetAsync()](/docs/reference/engine/classes/GlobalDataStore#GetAsync),
[GlobalDataStore:UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync),
[GlobalDataStore:IncrementAsync()](/docs/reference/engine/classes/GlobalDataStore#IncrementAsync),
[GlobalDataStore:RemoveAsync()](/docs/reference/engine/classes/GlobalDataStore#RemoveAsync), and
[DataStore:GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync).

See also:

* [Data Stores](/docs/cloud-services/data-stores), an in-depth
  guide on data structure, management, error handling, etc.

---

API Reference

Properties

CreatedTime

Read Only

Not Replicated

Read Parallel

The date and time the object was created.

DataStoreKeyInfo.CreatedTime:[number](/docs/luau/numbers)

This property indicates the date and time the object was created,
formatted as the number of milliseconds since epoch.

Provide feedback

---

UpdatedTime

Read Only

Not Replicated

Read Parallel

The date and time the object was last updated.

DataStoreKeyInfo.UpdatedTime:[number](/docs/luau/numbers)

This property indicates the date and time the object was last updated,
formatted as the number of milliseconds since epoch.

Provide feedback

---

Version

Read Only

Not Replicated

Read Parallel

Uniquely identifies the version of the object.

DataStoreKeyInfo.Version:[string](/docs/luau/strings)

This property uniquely identifies the version of the object. It can be
passed to [DataStore:GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync) or
[DataStore:RemoveVersionAsync()](/docs/reference/engine/classes/DataStore#RemoveVersionAsync) to get or remove the version
respectively.

Provide feedback

---

Methods

GetMetadata

Returns the metadata associated with the object.

DataStoreKeyInfo:GetMetadata():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Metadata associated with the key.

This function returns the metadata associated with the latest version of
the object.

Provide feedback

---

GetUserIds

An array of [UserIds](/docs/reference/engine/classes/Player#UserId) tagged with a key.

DataStoreKeyInfo:GetUserIds():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of [UserIds](/docs/reference/engine/classes/Player#UserId) associated with the object.

This function returns an array of [UserIds](/docs/reference/engine/classes/Player#UserId) tagged
with the object.

Provide feedback

---