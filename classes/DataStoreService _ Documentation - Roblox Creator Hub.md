# DataStoreService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStoreService
Scraped: 2026-01-11T02:28:44.452897Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- DataStoreService
- DataStore
- OrderedDataStore
- DataStoreListingPages
- Object
- GlobalDataStore
- Script
- ModuleScript
- DataStoreOptions
- AllScopes
- GetDataStore()
- GlobalDataStore:GetChildren()
- GlobalDataStores
- DataStoreInfo
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataStoreService](/docs/reference/engine/classes/DataStoreService)

English

Feedback

Engine Class

DataStoreService

A game service that gives access to persistent data storage across places in a
game.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetDataStore](#GetDataStore)(name: [string](/docs/luau/strings),scope: [string](/docs/luau/strings),options: [Instance](/docs/reference/engine/datatypes/Instance)):[DataStore](/docs/reference/engine/classes/DataStore) |
| [GetGlobalDataStore](#GetGlobalDataStore)():[DataStore](/docs/reference/engine/classes/DataStore) |
| [GetOrderedDataStore](#GetOrderedDataStore)(name: [string](/docs/luau/strings),scope: [string](/docs/luau/strings)):[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore) |
| [GetRequestBudgetForRequestType](#GetRequestBudgetForRequestType)(requestType: [Enum.DataStoreRequestType](/docs/reference/engine/enums/DataStoreRequestType)):[number](/docs/luau/numbers) |
| [ListDataStoresAsync](#ListDataStoresAsync)(prefix: [string](/docs/luau/strings),pageSize: [number](/docs/luau/numbers),cursor: [string](/docs/luau/strings)):[DataStoreListingPages](/docs/reference/engine/classes/DataStoreListingPages) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

DataStoreService exposes methods for getting [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) and
[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore) objects. Data stores can only be accessed by game
servers, so you can only use [DataStoreService](/docs/reference/engine/classes/DataStoreService) within a [Script](/docs/reference/engine/classes/Script)
or a [ModuleScript](/docs/reference/engine/classes/ModuleScript) that is used by a [Script](/docs/reference/engine/classes/Script).

See [Data stores](/docs/cloud-services/data-stores) for an
in-depth guide on data structure, management, error handling, limits, and
more.

Code Samples

DataStore Budget

This code sample prints the request budget for all data store request types.

```
local DataStoreService = game:GetService("DataStoreService")



for _, enumItem in pairs(Enum.DataStoreRequestType:GetEnumItems()) do



print(enumItem.Name, DataStoreService:GetRequestBudgetForRequestType(enumItem))



end
```

---

API Reference

Methods

GetDataStore

Creates a [DataStore](/docs/reference/engine/classes/DataStore) instance with the provided name and scope.

DataStoreService:GetDataStore(

name:[string](/docs/luau/strings), scope:[string](/docs/luau/strings), options:[Instance](/docs/reference/engine/datatypes/Instance)

):[DataStore](/docs/reference/engine/classes/DataStore)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Name of the data store. |
| scope:[string](/docs/luau/strings) Default Value: "global" (Optional) A string specifying the scope. |
| options:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" (Optional) A [DataStoreOptions](/docs/reference/engine/classes/DataStoreOptions) instance to enable experimental features and v2 API features. |

Returns

[DataStore](/docs/reference/engine/classes/DataStore)

A [DataStore](/docs/reference/engine/classes/DataStore) instance with provided name and optional scope.

This function creates a [DataStore](/docs/reference/engine/classes/DataStore) instance with the provided name
and scope. Subsequent calls to this method with the same name/scope will
return the same object.

Using the scope parameter will restrict operations to that scope by
automatically prepending the scope to keys in all operations done on the
data store. This function also accepts an optional
[DataStoreOptions](/docs/reference/engine/classes/DataStoreOptions) instance which includes options for enabling
[AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes). See
[Versioning, listing, and caching](/docs/cloud-services/data-stores/versioning-listing-and-caching#scopes)
for details on scope.

Provide feedback

---

GetGlobalDataStore

Returns the default data store.

DataStoreService:GetGlobalDataStore():[DataStore](/docs/reference/engine/classes/DataStore)

Returns

[DataStore](/docs/reference/engine/classes/DataStore)

This function returns the default [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore). If you want to
access a specific named data store instead, you should use the
[GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore) function.

Note that the [DataStore](/docs/reference/engine/classes/DataStore) returned by this function always uses the
scope u. See [Data stores](/docs/cloud-services/data-stores)
for details on scope.

Code Samples

Get GlobalDataStore Instance

The following example retrieves a default data store instance which behaves
like a regular [Instance](/docs/reference/engine/classes/Instance). Since a [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) is an
[Instance](/docs/reference/engine/classes/Instance), functions such as [GlobalDataStore:GetChildren()](/docs/reference/engine/classes/GlobalDataStore#GetChildren) will
execute without error.

```
local DataStoreService = game:GetService("DataStoreService")



local GlobalDataStore = DataStoreService:GetGlobalDataStore()



print(GlobalDataStore.Name)
```

Provide feedback

---

GetOrderedDataStore

Get an [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore) given a name and optional scope.

DataStoreService:GetOrderedDataStore(

name:[string](/docs/luau/strings), scope:[string](/docs/luau/strings)

):[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |
| scope:[string](/docs/luau/strings) Default Value: "global" |

Returns

[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore)

This method returns an [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore), similar to the way
[GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore) does with
[GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore). Subsequent calls to this method
with the same name/scope will return the same object.

Code Samples

OrderedDataStore Basics

This code sample demonstrates usage of an OrderedDataStore and pages.

```
local DataStoreService = game:GetService("DataStoreService")



local pointsStore = DataStoreService:GetOrderedDataStore("Points")



local function printTopTenPlayers()



local isAscending = false



local pageSize = 10



local pages = pointsStore:GetSortedAsync(isAscending, pageSize)



local topTen = pages:GetCurrentPage()



-- The data in 'topTen' is stored with the index being the index on the page



-- For each item, 'data.key' is the key in the OrderedDataStore and 'data.value' is the value



for rank, data in ipairs(topTen) do



local name = data.key



local points = data.value



print(name .. " is ranked #" .. rank .. " with " .. points .. "points")



end



-- Potentially load the next page...



--pages:AdvanceToNextPageAsync()



end



-- Create some data



pointsStore:SetAsync("Alex", 55)



pointsStore:SetAsync("Charley", 32)



pointsStore:SetAsync("Sydney", 68)



-- Display the top ten players



printTopTenPlayers()
```

Provide feedback

---

GetRequestBudgetForRequestType

Returns the number of requests that can be made by the given request type.

DataStoreService:GetRequestBudgetForRequestType(requestType:[Enum.DataStoreRequestType](/docs/reference/engine/enums/DataStoreRequestType)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| requestType:[Enum.DataStoreRequestType](/docs/reference/engine/enums/DataStoreRequestType) |

Returns

[number](/docs/luau/numbers)

This function returns the number of data store requests that the current
place can make based on the given [Enum.DataStoreRequestType](/docs/reference/engine/enums/DataStoreRequestType). Any
requests made that exceed this budget are subject to throttling.
Monitoring and adjusting the frequency of data store requests using this
function is recommended.

Code Samples

Print Request Budget

```
local DataStoreService = game:GetService("DataStoreService")



local globalStore = DataStoreService:GetGlobalDataStore()



local function printBudget()



local budget = DataStoreService:GetRequestBudgetForRequestType(Enum.DataStoreRequestType.SetIncrementAsync)



print("Current set/increment budget:", budget)



end



for i = 1, 5 do



local key = "key" .. i



local success, err = pcall(function()



globalStore:SetAsync(key, true)



end)



if success then



printBudget()



else



print(err)



end



end
```

Provide feedback

---

ListDataStoresAsync

Yields

Returns a [DataStoreListingPages](/docs/reference/engine/classes/DataStoreListingPages) object for enumerating through all
of the experience's data stores.

DataStoreService:ListDataStoresAsync(

prefix:[string](/docs/luau/strings), pageSize:[number](/docs/luau/numbers), cursor:[string](/docs/luau/strings)

):[DataStoreListingPages](/docs/reference/engine/classes/DataStoreListingPages)

Parameters

|  |
| --- |
| prefix:[string](/docs/luau/strings)  (Optional) Prefix to enumerate data stores that start with the given prefix. |
| pageSize:[number](/docs/luau/numbers) Default Value: 0 (Optional) Number of items to be returned in each page. If no value is given, the engine sends a default value of 0 to the data store web service, which in turn defaults to 32 items per page. |
| cursor:[string](/docs/luau/strings)  (Optional) Cursor to continue iteration. |

Returns

[DataStoreListingPages](/docs/reference/engine/classes/DataStoreListingPages)

[DataStoreListingPages](/docs/reference/engine/classes/DataStoreListingPages) instance containing
[DataStoreInfo](/docs/reference/engine/classes/DataStoreInfo) instances that provide details such as name,
creation time, and time last updated.

Returns a [DataStoreListingPages](/docs/reference/engine/classes/DataStoreListingPages) object for enumerating through all
of the experience's data stores. It accepts an optional prefix parameter
to only locate data stores whose names start with the provided prefix.

Only data stores containing at least one object will be listed via this
function.

Provide feedback

---