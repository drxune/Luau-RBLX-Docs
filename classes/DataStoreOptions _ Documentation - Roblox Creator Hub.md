# DataStoreOptions | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreOptions
Scraped: 2026-01-11T02:31:35.659428Z

## Tags
- Not Replicated

## Inherits
- Instance
- DataStoreOptions
- DataStoreService:GetDataStore()
- Object
- GlobalDataStore
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreOptions](/docs/reference/engine/classes/DataStoreOptions)

English

Feedback

Engine Class

DataStoreOptions

Object used to provide additional parameters to
[DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore).

Not Replicated

---

Summary

Properties

|  |
| --- |
| [AllScopes](#AllScopes):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [SetExperimentalFeatures](#SetExperimentalFeatures)(experimentalFeatures: [Dictionary](/docs/luau/tables#dictionaries)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Any object containing additional parameters that are used by
[DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore).

---

API Reference

Properties

AllScopes

Read Parallel

Whether the [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) should work with all scopes.

DataStoreOptions.AllScopes:[boolean](/docs/luau/booleans)

This property specifies whether the [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) should work
with all scopes.

Provide feedback

---

Methods

SetExperimentalFeatures

DataStoreOptions:SetExperimentalFeatures(experimentalFeatures:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| experimentalFeatures:[Dictionary](/docs/luau/tables#dictionaries)  Luau table in key = value format where the key is the experimental feature name and the value is a boolean which specifies whether to enable. |

Returns

()

This function currently has no effect.

Provide feedback

---