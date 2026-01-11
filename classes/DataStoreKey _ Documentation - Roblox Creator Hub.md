# DataStoreKey | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreKey
Scraped: 2026-01-11T02:39:07.444706Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- DataStoreKey
- DataStoreKeyPages
- DataStoreKey.KeyName
- DataStore:ListKeysAsync()
- GlobalDataStore:GetAsync()
- GlobalDataStore:SetAsync()
- DataStoreOptions.AllScopes
- DataStoreService:GetDataStore()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreKey](/docs/reference/engine/classes/DataStoreKey)

English

Feedback

Engine Class

DataStoreKey

Object representing a key on a [DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages) object.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [KeyName](#KeyName):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Object representing a key on a [DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages) object. It contains
the key name as [DataStoreKey.KeyName](/docs/reference/engine/classes/DataStoreKey#KeyName). This object is a member of the
[DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages) object returned by
[DataStore:ListKeysAsync()](/docs/reference/engine/classes/DataStore#ListKeysAsync).

See also:

* [Data Stores](/docs/cloud-services/data-stores), an in-depth
  guide on data structure, management, error handling, etc.

---

API Reference

Properties

KeyName

Read Only

Not Replicated

Read Parallel

The name of the key.

DataStoreKey.KeyName:[string](/docs/luau/strings)

This property indicates the name of the key. This name can then be used in
other operations such as [GlobalDataStore:GetAsync()](/docs/reference/engine/classes/GlobalDataStore#GetAsync) and
[GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync).

If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the
data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), the name will
include its scope as a prefix.

Provide feedback

---