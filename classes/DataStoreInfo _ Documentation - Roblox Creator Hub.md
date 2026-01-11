# DataStoreInfo | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreInfo
Scraped: 2026-01-11T02:30:26.031447Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- DataStoreInfo
- DataStoreListingPages
- DataStoreService:ListDataStoresAsync()
- DataStoreService:GetDataStore()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreInfo](/docs/reference/engine/classes/DataStoreInfo)

English

Feedback

Engine Class

DataStoreInfo

Object describing data store information.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [CreatedTime](#CreatedTime):[number](/docs/luau/numbers) |
| [DataStoreName](#DataStoreName):[string](/docs/luau/strings) |
| [UpdatedTime](#UpdatedTime):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Object describing data store information such as name, created time, and time
last updated. This object is a member of the [DataStoreListingPages](/docs/reference/engine/classes/DataStoreListingPages)
object returned by [DataStoreService:ListDataStoresAsync()](/docs/reference/engine/classes/DataStoreService#ListDataStoresAsync).

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

Indicates when the data store was created in milliseconds since epoch.

DataStoreInfo.CreatedTime:[number](/docs/luau/numbers)

This property indicates when the data store was created in milliseconds
since epoch.

Provide feedback

---

DataStoreName

Read Only

Not Replicated

Read Parallel

The name of the data store.

DataStoreInfo.DataStoreName:[string](/docs/luau/strings)

This property indicates the name of the data store. It is used as a unique
identifier to retrieve a data store instance with
[DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore).

Provide feedback

---

UpdatedTime

Read Only

Not Replicated

Read Parallel

Indicates the last time the data store was updated in milliseconds since
epoch.

DataStoreInfo.UpdatedTime:[number](/docs/luau/numbers)

This property indicates the last time the data store was updated in
milliseconds since epoch.

Provide feedback

---