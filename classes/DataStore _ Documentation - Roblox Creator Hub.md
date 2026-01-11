# DataStore | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStore
Scraped: 2026-01-11T02:33:56.296673Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- GlobalDataStore
- DataStore
- DataStoreKeyPages
- DataStoreVersionPages
- Instance
- Object
- DataStoreOptions.AllScopes
- DataStoreService:GetDataStore()
- DataStoreKeyInfo
- UserIds
- DataStore:ListVersionsAsync()
- GlobalDataStore:SetAsync()
- DataStoreKey
- DataStoreObjectVersionInfo
- GlobalDataStore:RemoveAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore)
6. /
7. [DataStore](/docs/reference/engine/classes/DataStore)

English

Feedback

Engine Class

DataStore

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetVersionAsync](#GetVersionAsync)(key: [string](/docs/luau/strings),version: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [GetVersionAtTimeAsync](#GetVersionAtTimeAsync)(key: [string](/docs/luau/strings),timestamp: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |
| [ListKeysAsync](#ListKeysAsync)(prefix: [string](/docs/luau/strings),pageSize: [number](/docs/luau/numbers),cursor: [string](/docs/luau/strings),excludeDeleted: [boolean](/docs/luau/booleans)):[DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages) |
| [ListVersionsAsync](#ListVersionsAsync)(key: [string](/docs/luau/strings),sortDirection: [Enum.SortDirection](/docs/reference/engine/enums/SortDirection),minDate: [number](/docs/luau/numbers),maxDate: [number](/docs/luau/numbers),pageSize: [number](/docs/luau/numbers)):[DataStoreVersionPages](/docs/reference/engine/classes/DataStoreVersionPages) |
| [RemoveVersionAsync](#RemoveVersionAsync)(key: [string](/docs/luau/strings),version: [string](/docs/luau/strings)):() |

Inherited Members

6 inherited from [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

See [Data stores](/docs/cloud-services/data-stores) for an
in-depth guide on data structure, management, error handling, limits, and
more.

---

API Reference

Methods

GetVersionAsync

Yields

Retrieves the specified key version.

DataStore:GetVersionAsync(

key:[string](/docs/luau/strings), version:[string](/docs/luau/strings)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name for which the version info is requested. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| version:[string](/docs/luau/strings)  Version number of the key for which the version info is requested. |

Returns

[Tuple](/docs/luau/tuples)

The value of the key at the specified version and a
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance that includes the version number,
date and time the version was created, and functions to retrieve
[UserIds](/docs/reference/engine/classes/Player#UserId) and metadata.

This function retrieves the specified key version as well as a
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance. A version identifier can be found
through [DataStore:ListVersionsAsync()](/docs/reference/engine/classes/DataStore#ListVersionsAsync) or alternatively be the
identifier returned by [GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync).

Provide feedback

---

GetVersionAtTimeAsync

Yields

Retrieves the key version that was current at a given time.

DataStore:GetVersionAtTimeAsync(

key:[string](/docs/luau/strings), timestamp:[number](/docs/luau/numbers)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name for which the version info is requested. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| timestamp:[number](/docs/luau/numbers)  Unix timestamp in milliseconds for which the requested version was current. Must be greater than zero. Must not be more than ten minutes in the future. |

Returns

[Tuple](/docs/luau/tuples)

The value of the key that was current at the specified time and a
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance that includes the version number,
date and time the version was created, and functions to retrieve
[UserIds](/docs/reference/engine/classes/Player#UserId) and metadata. nil if no available
version was current at the requested time.

This function retrieves the key version that was current at a given time
as well as a [DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance.

Code Samples

Retrieving DataStore Versions by Time

The following code sample retrieves data store key versions using timestamps.

```
local DataStoreService = game:GetService("DataStoreService")



local dataStore = DataStoreService:GetDataStore("DataStore")



local key = "key-123"



function setData(data)



local success, result = pcall(function()



dataStore:SetAsync(key, data)



end)



if not success then



warn(result)



end



end



function getVersionAtTime(timestamp)



local success, result, keyInfo = pcall(function()



return dataStore:GetVersionAtTimeAsync(key, timestamp.UnixTimestampMillis)



end)



if success then



if result == nil then



print("No version found at time")



else



print(result, keyInfo.Version)



end



else



warn(result)



end



end



-- Previously ran at 2024/12/02 6:00 UTC



setData("version 1")



-- Previously ran at 2024/12/02 9:00 UTC



setData("version 2")



-- Prints "No version found at time"



local time1 = DateTime.fromUniversalTime(2024, 12, 02, 05, 00)



getVersionAtTime(time1)



-- Prints "version 1 <version>"



local time2 = DateTime.fromUniversalTime(2024, 12, 02, 07, 00)



getVersionAtTime(time2)



-- Prints "version 2 <version>"



local time3 = DateTime.fromUniversalTime(2024, 12, 02, 10, 00)



getVersionAtTime(time3)
```

Provide feedback

---

ListKeysAsync

Yields

Returns a [DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages) object for enumerating through keys of
a data store.

DataStore:ListKeysAsync(

prefix:[string](/docs/luau/strings), pageSize:[number](/docs/luau/numbers), cursor:[string](/docs/luau/strings), excludeDeleted:[boolean](/docs/luau/booleans)

):[DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages)

Parameters

|  |
| --- |
| prefix:[string](/docs/luau/strings)  (Optional) Prefix to use for locating keys. |
| pageSize:[number](/docs/luau/numbers) Default Value: 0 (Optional) Number of items to be returned in each page. If no value is given, the engine sends a default value of 0 to the data store web service, which in turn defaults to 50 items per page. |
| cursor:[string](/docs/luau/strings)  (Optional) Cursor to continue iteration. |
| excludeDeleted:[boolean](/docs/luau/booleans) Default Value: false (Optional) Exclude deleted keys from being returned.  When enabled ListKeys will check up to 512 keys. If all checked keys are deleted then it will return an empty list with a cursor to continue iteration. |

Returns

[DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages)

A [DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages) instance that enumerates the keys as
[DataStoreKey](/docs/reference/engine/classes/DataStoreKey) instances.

This function returns a [DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages) object for enumerating
through keys of a data store. It accepts an optional prefix parameter to
only locate keys whose names start with the provided prefix.

If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the
data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), keys will be
returned with all scopes as prefixes.

Provide feedback

---

ListVersionsAsync

Yields

Enumerates all versions of a key.

DataStore:ListVersionsAsync(

key:[string](/docs/luau/strings), sortDirection:[Enum.SortDirection](/docs/reference/engine/enums/SortDirection), minDate:[number](/docs/luau/numbers), maxDate:[number](/docs/luau/numbers), pageSize:[number](/docs/luau/numbers)

):[DataStoreVersionPages](/docs/reference/engine/classes/DataStoreVersionPages)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name for the versions to list. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| sortDirection:[Enum.SortDirection](/docs/reference/engine/enums/SortDirection) Default Value: "Ascending" (Optional) Enum specifying ascending or descending sort order. |
| minDate:[number](/docs/luau/numbers) Default Value: 0 (Optional) Unix timestamp in milliseconds after which the versions should be listed. |
| maxDate:[number](/docs/luau/numbers) Default Value: 0 (Optional) Unix timestamp in milliseconds up to which the versions should be listed. |
| pageSize:[number](/docs/luau/numbers) Default Value: 0 (Optional) Number of items to be returned in each page. If no value is given, the engine sends a default value of 0 to the data store web service, which in turn defaults to 1024 items per page. |

Returns

[DataStoreVersionPages](/docs/reference/engine/classes/DataStoreVersionPages)

A [DataStoreVersionPages](/docs/reference/engine/classes/DataStoreVersionPages) instance that enumerates all the
versions of the key as [DataStoreObjectVersionInfo](/docs/reference/engine/classes/DataStoreObjectVersionInfo) instances.

This function enumerates versions of the specified key in either ascending
or descending order specified by a [Enum.SortDirection](/docs/reference/engine/enums/SortDirection) parameter. It can
optionally filter the returned versions by minimum and maximum timestamp.

Code Samples

Retrieving DataStore Versions With A Date Filter

The following code sample retrieves all versions after a specified starting
time, sorted in ascending order.

```
local DataStoreService = game:GetService("DataStoreService")



local experienceStore = DataStoreService:GetDataStore("PlayerExperience")



local time = DateTime.fromUniversalTime(2020, 10, 09, 01, 42)



local listSuccess, pages = pcall(function()



return experienceStore:ListVersionsAsync("User_1234", nil, time.UnixTimestampMillis)



end)



if listSuccess then



local items = pages:GetCurrentPage()



for key, info in pairs(items) do



print("Key:", key, "; Version:", info.Version, "; Created:", info.CreatedTime, "; Deleted:", info.IsDeleted)



end



end
```

Provide feedback

---

RemoveVersionAsync

Yields

Permanently deletes the specified version of a key.

DataStore:RemoveVersionAsync(

key:[string](/docs/luau/strings), version:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name for which a version is to be removed. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| version:[string](/docs/luau/strings)  Version number of the key to remove. |

Returns

()

This function permanently deletes the specified version of a key. Version
identifiers can be found through [DataStore:ListVersionsAsync()](/docs/reference/engine/classes/DataStore#ListVersionsAsync).

Unlike [GlobalDataStore:RemoveAsync()](/docs/reference/engine/classes/GlobalDataStore#RemoveAsync), this function does not
create a new "tombstone" version and the removed value cannot be retrieved
later.

Provide feedback

---