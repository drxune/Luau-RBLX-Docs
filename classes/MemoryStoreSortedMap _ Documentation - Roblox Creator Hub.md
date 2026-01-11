# MemoryStoreSortedMap | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MemoryStoreSortedMap
Scraped: 2026-01-11T02:30:34.606319Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- MemoryStoreSortedMap
- MemoryStoreService
- Object
- MemoryStoreSortedMap:GetRangeAsync()
- MemoryStoreSortedMap:UpdateAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MemoryStoreSortedMap](/docs/reference/engine/classes/MemoryStoreSortedMap)

English

Feedback

Engine Class

MemoryStoreSortedMap

Provides access to a sorted map within [MemoryStoreService](/docs/reference/engine/classes/MemoryStoreService).

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetAsync](#GetAsync)(key: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [GetRangeAsync](#GetRangeAsync)(direction: [Enum.SortDirection](/docs/reference/engine/enums/SortDirection),count: [number](/docs/luau/numbers),exclusiveLowerBound: Variant,exclusiveUpperBound: Variant):[Array](/docs/luau/tables#arrays) |
| [GetSizeAsync](#GetSizeAsync)():[number](/docs/luau/numbers) |
| [RemoveAsync](#RemoveAsync)(key: [string](/docs/luau/strings)):() |
| [SetAsync](#SetAsync)(key: [string](/docs/luau/strings),value: Variant,expiration: [number](/docs/luau/numbers),sortKey: Variant):[boolean](/docs/luau/booleans) |
| [UpdateAsync](#UpdateAsync)(key: [string](/docs/luau/strings),transformFunction: [function](/docs/luau/functions),expiration: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Provides access to a sorted map within [MemoryStoreService](/docs/reference/engine/classes/MemoryStoreService). A sorted
map is a collection of items where string keys are associated with arbitrary
values (up to the maximum allowed size -- see
[Memory Stores](/docs/cloud-services/memory-stores/sorted-map)). Each
item can also have an optional sort key, which can be a number or a string. In
the ordering of items, the sort key, if provided, takes precedence over the
key. Items with numeric sort keys are sorted before items with string sort
keys, which are sorted before items with no sort key. Items with the same sort
key and items with no sort key are arranged in alphabetical order by key.

---

API Reference

Methods

GetAsync

Yields

Retrieves the value and sort key of a key in the sorted map.

MemoryStoreSortedMap:GetAsync(key:[string](/docs/luau/strings)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key whose value and sort key to retrieve. |

Returns

[Tuple](/docs/luau/tuples)

A tuple of two values:

* Key value, or nil if there's no item with the specified key.
* Sort key, or nil if there's no sort key associated with the
  specified key.

Retrieves the value and sort key of a key in the sorted map.

Provide feedback

---

GetRangeAsync

Yields

Retrieves items within a sorted range of keys and sort keys.

MemoryStoreSortedMap:GetRangeAsync(

direction:[Enum.SortDirection](/docs/reference/engine/enums/SortDirection), count:[number](/docs/luau/numbers), exclusiveLowerBound:Variant, exclusiveUpperBound:Variant

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| direction:[Enum.SortDirection](/docs/reference/engine/enums/SortDirection)  Sort direction, ascending or descending. |
| count:[number](/docs/luau/numbers)  The number of items to retrieve; the maximum allowed value for this parameter is 200. |
| exclusiveLowerBound:Variant  (Optional) Lower bound, exclusive, for the returned keys. This is provided as a table where one or both of key and sort key can be specified: { key: string, sortKey: Variant } . |
| exclusiveUpperBound:Variant  (Optional) Upper bound, exclusive, for the returned keys. This is provided as a table where one or both of key and sort key can be specified: { key: string, sortKey: Variant } . |

Returns

[Array](/docs/luau/tables#arrays)

Item keys, values and sort keys in the requested range.

Gets items within a sorted range of keys and sort keys.

Code Samples

Retrieving MemoryStore Keys

The code below prints all keys in a sorted map in alphabetical order with the
help of the [MemoryStoreSortedMap:GetRangeAsync()](/docs/reference/engine/classes/MemoryStoreSortedMap#GetRangeAsync) method.

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local myMap = MemoryStoreService:GetSortedMap("MySortedMap")



function printAllKeys(map)



-- the initial lower bound is nil which means to start from the very first item



local exclusiveLowerBound = nil



-- this loop continues until the end of the map is reached



while true do



-- get up to a hundred items starting from the current lower bound



local items = map:GetRangeAsync(Enum.SortDirection.Ascending, 100, exclusiveLowerBound)



for _, item in ipairs(items) do



print(item.key)



print(item.sortKey)



end



-- if the call returned less than a hundred items it means we've reached the end of the map



if #items < 100 then



break



end



-- the last retrieved key is the exclusive lower bound for the next iteration



exclusiveLowerBound = {}



exclusiveLowerBound["key"] = items[#items].key



exclusiveLowerBound["sortKey"] = items[#items].sortKey



end



end



printAllKeys(myMap)
```

Provide feedback

---

GetSizeAsync

Yields

Gets the size of the sorted map.

MemoryStoreSortedMap:GetSizeAsync():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Gets the size of the sorted map.

Provide feedback

---

RemoveAsync

Yields

Removes the provided key from the sorted map.

MemoryStoreSortedMap:RemoveAsync(key:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key to remove. |

Returns

()

Removes the provided key from the sorted map.

Provide feedback

---

SetAsync

Yields

Sets the value of a key.

MemoryStoreSortedMap:SetAsync(

key:[string](/docs/luau/strings), value:Variant, expiration:[number](/docs/luau/numbers), sortKey:Variant

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key whose value to set. |
| value:Variant  Key value to set. |
| expiration:[number](/docs/luau/numbers)  Item expiration, in seconds. The item is automatically removed from the sorted map once the expiration duration is reached. The maximum expiration time is 45 days (3,888,000 seconds). |
| sortKey:Variant  (Optional) Sort key to set for this key. Accepted types are a number (integer or decimal) or a string. |

Returns

[boolean](/docs/luau/booleans)

Sets the value and sort key of the key overwriting any existing key value
and sort key.

Provide feedback

---

UpdateAsync

Yields

Retrieves the value and sort key of a key from a sorted map and updates it
with a new value and sort key.

MemoryStoreSortedMap:UpdateAsync(

key:[string](/docs/luau/strings), transformFunction:[function](/docs/luau/functions), expiration:[number](/docs/luau/numbers)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key whose value to update. |
| transformFunction:[function](/docs/luau/functions)  A function which you need to provide. The function takes the key's old value and old sort key as input and returns the new value and new sort key. |
| expiration:[number](/docs/luau/numbers)  Item expiration time, in seconds, after which the item will be automatically removed from the sorted map. The maximum expiration time is 45 days (3,888,000 seconds). |

Returns

[Tuple](/docs/luau/tuples)

The return value is a tuple of the last value and sort key returned by
the transform function.

Retrieves the value and sort key of a key from a sorted map and lets you
update it to a new value and sort key via a callback function.

This method accepts a callback function that transforms the old value and
old sort key into the updated value and updated sort key as required. The
method retrieves the existing key value and sort key and passes it to the
transform function which returns the new value and sort key for the item,
with these exceptions:

* If the key does not exist, the old value and old sort key passed to the
  function will be nil.
* If the function returns nil, the update is canceled.

The new value and new sort key is saved only if the key was not updated
(e.g. by a different game server) since the moment it was read. If the
value or sort key did change, the transform function is invoked again with
the most recent item value and sort key. This cycle repeats until the
value and sort key are saved successfully or the transform function
returns nil to abort the operation.

Code Samples

Updating a MemoryStore Sorted Map

The code below updates the score in a leaderboard for a player in a game.
The score is calculated as kills / deaths. The use of
[MemoryStoreSortedMap:UpdateAsync()](/docs/reference/engine/classes/MemoryStoreSortedMap#UpdateAsync) ensures that the kills and deaths
are updated for the most recent values even if multiple game servers update
the same item simultaneously. A player's kills and deaths are monotonically
increasing values and can hence only increase in value in a session.

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local map = MemoryStoreService:GetSortedMap("Leaderboard")



local Players = game:GetService("Players")



function updateLeaderboard(itemKey, killsToAdd, deathsToAdd)



local success, newStats, newScore = pcall(function()



return map:UpdateAsync(itemKey, function(playerStats, playerScore)



playerStats = playerStats or { kills = 0, deaths = 0 }



playerStats.kills += killsToAdd



playerStats.deaths += deathsToAdd



if playerStats then



-- `playerScore` is the sortKey being used to sort items in the map



playerScore = playerStats.kills / math.max(playerStats.deaths, 1)



return playerStats, playerScore



end



return nil



end, 30)



end)



end



-- Add one kill to all players



for i, player in pairs(Players:GetPlayers()) do



updateLeaderboard(player.UserId, 1, 0)



end



-- Add 5 kills and 1 death to player with userId 12345



updateLeaderboard(12345, 5, 1)
```

Provide feedback

---