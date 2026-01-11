# OrderedDataStore | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/OrderedDataStore
Scraped: 2026-01-11T02:27:57.044791Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- GlobalDataStore
- OrderedDataStore
- DataStorePages
- Instance
- Object
- GetSortedAsync()
- DataStoreKeyInfo
- DataStore
- SetAsync()
- IncrementAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore)
6. /
7. [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore)

English

Feedback

Engine Class

OrderedDataStore

A GlobalDataStore that also allows for ordered data store entries.

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetSortedAsync](#GetSortedAsync)(ascending: [boolean](/docs/luau/booleans),pagesize: [number](/docs/luau/numbers),minValue: Variant,maxValue: Variant):[DataStorePages](/docs/reference/engine/classes/DataStorePages) |

Inherited Members

6 inherited from [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A OrderedDataStore is essentially a [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) with the
exception that stored values must be integers. It exposes a method
[GetSortedAsync()](/docs/reference/engine/classes/OrderedDataStore#GetSortedAsync) which allows
inspection of the entries in sorted order using a [DataStorePages](/docs/reference/engine/classes/DataStorePages)
object.

Ordered data stores do not support versioning and metadata, so
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) is always nil for keys in an
[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). If you need versioning and metadata support, use a
[DataStore](/docs/reference/engine/classes/DataStore).

Ordered data stores do not support the optional userIds parameter for
[SetAsync()](/docs/reference/engine/classes/OrderedDataStore#SetAsync) or
[IncrementAsync()](/docs/reference/engine/classes/OrderedDataStore#IncrementAsync).

See [Data stores](/docs/cloud-services/data-stores) for an
overview on how to use ordered data stores.

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

---

API Reference

Methods

GetSortedAsync

Yields

Returns a [DataStorePages](/docs/reference/engine/classes/DataStorePages) object.

OrderedDataStore:GetSortedAsync(

ascending:[boolean](/docs/luau/booleans), pagesize:[number](/docs/luau/numbers), minValue:Variant, maxValue:Variant

):[DataStorePages](/docs/reference/engine/classes/DataStorePages)

Parameters

|  |
| --- |
| ascending:[boolean](/docs/luau/booleans)  A boolean indicating whether the returned data pages are in ascending order. |
| pagesize:[number](/docs/luau/numbers)  The length of each page. By default is 50. The max allowed value is 100. |
| minValue:Variant  Optional parameter. If set, data pages with a value less than minValue will be excluded. |
| maxValue:Variant  Optional parameter. If set, data pages with a value greater than maxValue will be excluded. |

Returns

[DataStorePages](/docs/reference/engine/classes/DataStorePages)

A sorted [DataStorePages](/docs/reference/engine/classes/DataStorePages) object based on the provided
arguments.

Returns a [DataStorePages](/docs/reference/engine/classes/DataStorePages) object. The sort order is determined by
ascending, the length of each page by pageSize, and
minValue/maxValue are optional parameters which filter the
results.

See
[Error codes and limits](/docs/cloud-services/data-stores/error-codes-and-limits)
for request limits and descriptions of the error codes.

Provide feedback

---