# DataStorePages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataStorePages
Scraped: 2026-01-11T02:36:08.393813Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Pages
- DataStorePages
- OrderedDataStore
- Instance
- Object
- GetCurrentPage()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Pages](/docs/reference/engine/classes/Pages)
6. /
7. [DataStorePages](/docs/reference/engine/classes/DataStorePages)

English

Feedback

Engine Class

DataStorePages

A [Pages](/docs/reference/engine/classes/Pages) object that allows iteration through [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore)
key/value pairs.

Not Creatable

Not Replicated

---

Summary

Inherited Members

3 inherited from [Pages](/docs/reference/engine/classes/Pages)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A special type of [Pages](/docs/reference/engine/classes/Pages) object whose pages contain key/value pairs
from an [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). For this object,
[GetCurrentPage()](/docs/reference/engine/classes/Pages#GetCurrentPage) returns an array of tables,
each containing keys named key and value; these reflect the key/value
pair data.

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