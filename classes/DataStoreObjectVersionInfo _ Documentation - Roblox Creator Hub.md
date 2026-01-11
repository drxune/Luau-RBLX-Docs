# DataStoreObjectVersionInfo | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreObjectVersionInfo
Scraped: 2026-01-11T02:36:16.944072Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- DataStoreObjectVersionInfo
- Object
- DataStore:GetVersionAsync()
- DataStore:RemoveVersionAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreObjectVersionInfo](/docs/reference/engine/classes/DataStoreObjectVersionInfo)

English

Feedback

Engine Class

DataStoreObjectVersionInfo

An instance describing version information for a key.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [CreatedTime](#CreatedTime):[number](/docs/luau/numbers) |
| [IsDeleted](#IsDeleted):[boolean](/docs/luau/booleans) |
| [Version](#Version):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An instance describing version information for a key, including the version
string, created time, and whether it has been marked as deleted.

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

Indicates when the version was created in milliseconds since epoch.

DataStoreObjectVersionInfo.CreatedTime:[number](/docs/luau/numbers)

This property indicates when the version was created in milliseconds since
epoch.

Provide feedback

---

IsDeleted

Read Only

Not Replicated

Read Parallel

Whether the version has been marked as deleted.

DataStoreObjectVersionInfo.IsDeleted:[boolean](/docs/luau/booleans)

This property describes whether the version has been marked as deleted.
Deleted versions will be permanently deleted after 30 days.

Provide feedback

---

Version

Read Only

Not Replicated

Read Parallel

Uniquely identifies a particular version of the key.

DataStoreObjectVersionInfo.Version:[string](/docs/luau/strings)

This property uniquely identifies a particular version of the key. It can
be passed to [DataStore:GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync) or
[DataStore:RemoveVersionAsync()](/docs/reference/engine/classes/DataStore#RemoveVersionAsync) to get or remove the version
respectively.

Provide feedback

---