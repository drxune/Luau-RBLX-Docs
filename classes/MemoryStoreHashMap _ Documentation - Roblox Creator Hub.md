# MemoryStoreHashMap | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MemoryStoreHashMap
Scraped: 2026-01-11T02:40:32.037279Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- MemoryStoreHashMap
- MemoryStoreService
- MemoryStoreHashMapPages
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap)

English

Feedback

Engine Class

MemoryStoreHashMap

Provides access to a hash map within [MemoryStoreService](/docs/reference/engine/classes/MemoryStoreService).

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetAsync](#GetAsync)(key: [string](/docs/luau/strings)):Variant |
| [ListItemsAsync](#ListItemsAsync)(count: [number](/docs/luau/numbers)):[MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages) |
| [RemoveAsync](#RemoveAsync)(key: [string](/docs/luau/strings)):() |
| [SetAsync](#SetAsync)(key: [string](/docs/luau/strings),value: Variant,expiration: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [UpdateAsync](#UpdateAsync)(key: [string](/docs/luau/strings),transformFunction: [function](/docs/luau/functions),expiration: [number](/docs/luau/numbers)):Variant |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Provides access to a hash map within [MemoryStoreService](/docs/reference/engine/classes/MemoryStoreService). A hash map is
a collection of items where string keys are associated with arbitrary values
(up to the maximum allowed size -- see
[Memory Stores](/docs/cloud-services/memory-stores/hash-map)). The keys
have no ordering guarantees.

---

API Reference

Methods

GetAsync

Yields

Retrieves the value of a key in the hash map.

MemoryStoreHashMap:GetAsync(key:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  The key whose value you want to retrieve. |

Returns

Variant

The value, or nil if the key doesn't exist.

Retrieves the value of a key in the hash map.

Code Samples

Getting data from a MemoryStore Hash Map

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local hashMap = MemoryStoreService:GetHashMap("HashMap1")



local key = "User_1234"



local value = 1000



local expiration = 30



local setSuccess, _ = pcall(function()



return hashMap:SetAsync(key, value, expiration)



end)



if setSuccess then



print("Set succeeded!")



end



local item



local getSuccess, getError = pcall(function()



item = hashMap:GetAsync(key)



end)



if getSuccess then



print(item)



else



warn(getError)



end
```

Provide feedback

---

ListItemsAsync

Yields

Returns a [MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages) object for enumerating through
items in the hash map.

MemoryStoreHashMap:ListItemsAsync(count:[number](/docs/luau/numbers)):[MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages)

Parameters

|  |
| --- |
| count:[number](/docs/luau/numbers)  Maximum possible number of items that can be returned. |

Returns

[MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages)

A [MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages) instance that enumerates the items
as [MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages) instances.

Returns a [MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages) object for enumerating through
items in the hash map. The valid range is 1 to 200 inclusive.

Code Samples

Listing items in a MemoryStore Hash Map

The code below lists all the items in a Memory Store Hash Map.

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local testHashMap = MemoryStoreService:GetHashMap("HashMap1")



local EXPIRATION = 600



local NUM_TEST_ITEMS = 32



local function populateHashMap(hashMap: MemoryStoreHashMap, numItems: number): { [string]: any }



print("Setting HashMap data...")



local createdItems = {}



for index = 1, numItems do



local key = tostring(index) -- HashMap keys must be strings



local value = `{key}_test_value`



local success, result = pcall(hashMap.SetAsync, hashMap, key, value, EXPIRATION)



if success then



createdItems[key] = value



else



warn(`Error setting key {key}: {result}`)



end



end



print("Done setting HashMap data.")



return createdItems



end



local function getItemsFromAllPages(pages: MemoryStoreHashMapPages): { [string]: any }



-- Purely for logging purposes, we track what page number we're on



local currentPageNumber = 1



local retrievedItems = {}



while not pages.IsFinished do



print(`Getting items on page {currentPageNumber}...`)



local items = pages:GetCurrentPage()



for _, entry in pairs(items) do



print(`\t{entry.key}: {entry.value}`)



retrievedItems[entry.key] = entry.value



end



-- Advance pages if there are more pages to read



if not pages.IsFinished then



pages:AdvanceToNextPageAsync()



currentPageNumber += 1



end



end



print("Finished reading all pages")



return retrievedItems



end



local function compareAllItems(retrievedItems: { [string]: any }, expectedItems: { [string]: any }): number



print("Comparing retrieved items to expected items...")



local numMatchingItems = 0



for key, expectedValue in pairs(expectedItems) do



if retrievedItems[key] == expectedValue then



numMatchingItems += 1



else



warn(`Mismatched retrieved value for key {key}: expected {expectedValue}, retrieved {retrievedItems[key]}`)



end



end



print("Comparison complete!")



return numMatchingItems



end



-- Keys added to the hashmap are also added to this expectedItems table.



-- Later, the retrieved hashmap items will be compared against this table of expected items.



local expectedItems = populateHashMap(testHashMap, NUM_TEST_ITEMS)



-- Getting pages can error. In this case, we will let it error and stop program execution,



-- but you may want to pcall it and handle it differently.



print(`Getting HashMap pages with ListItemsAsync...`)



local pages = testHashMap:ListItemsAsync(NUM_TEST_ITEMS)



local retrievedItems = getItemsFromAllPages(pages)



local numMatchingItems = compareAllItems(retrievedItems, expectedItems)



-- If there were no errors setting or getting items, all items should match.



print(`Program complete. {numMatchingItems}/{NUM_TEST_ITEMS} retrieved items matched the expected values.`)
```

Provide feedback

---

RemoveAsync

Yields

Removes an item from the hash map.

MemoryStoreHashMap:RemoveAsync(key:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  The key to remove. |

Returns

()

Removes an item from the hash map.

Code Samples

Removing data from a MemoryStore Hash Map

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local hashMap = MemoryStoreService:GetHashMap("HashMap1")



local key = "User_1234"



local value = 1000



local expiration = 30



local setSuccess, setError = pcall(function()



return hashMap:SetAsync(key, value, expiration)



end)



if not setSuccess then



warn(setError)



end



local removeSuccess, removeError = pcall(function()



hashMap:RemoveAsync(key)



end)



if removeSuccess then



print("Remove succeeded!")



else



warn(removeError)



end
```

Provide feedback

---

SetAsync

Yields

Sets the value of a key in the hash map.

MemoryStoreHashMap:SetAsync(

key:[string](/docs/luau/strings), value:Variant, expiration:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  The key whose value to set. |
| value:Variant  The value to set. |
| expiration:[number](/docs/luau/numbers)  Item expiration in seconds, after which the item is automatically removed from the hash map. The maximum expiration time is 45 days (3,888,000 seconds). |

Returns

[boolean](/docs/luau/booleans)

Sets the value of a key in the hash map, overwriting any existing value.

Code Samples

Adding data to a MemoryStore Hash Map

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local hashMap = MemoryStoreService:GetHashMap("HashMap1")



local key = "User_1234"



local value = 1000



local expiration = 30



local setSuccess, setError = pcall(function()



return hashMap:SetAsync(key, value, expiration)



end)



if setSuccess then



print("Set succeeded!")



else



warn(setError)



end
```

Provide feedback

---

UpdateAsync

Yields

Retrieves the value of a key from a hash map and lets you update it to a
new value.

MemoryStoreHashMap:UpdateAsync(

key:[string](/docs/luau/strings), transformFunction:[function](/docs/luau/functions), expiration:[number](/docs/luau/numbers)

):Variant

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  The key whose value you want to update. |
| transformFunction:[function](/docs/luau/functions)  The transform function, which you provide. This function takes the old value as an input and returns the new value. |
| expiration:[number](/docs/luau/numbers)  Item expiration in seconds, after which the item is automatically removed from the hash map. The maximum expiration time is 45 days (3,888,000 seconds). |

Returns

Variant

The last value returned by the transform function.

Retrieves the value of a key from a hash map and lets you update it to a
new value.

This method accepts a callback function that retrieves the existing key
value and passes it to a transform function, which returns the new value
for the item, with these exceptions:

* If the key does not exist, the old value passed to the function is
  nil.
* If the function returns nil, the update is canceled.

The new value is saved only if the key was not updated (for example, by a
different game server) since the moment it was read. If the value changed
in that time, the transform function is called again with the most recent
item value. This cycle repeats until the value is saved successfully or
the transform function returns nil to abort the operation.

Code Samples

Updating a Memory Store Hash Map

This sample updates the count of some resource in a shared inventory. The use
of MemoryStoreHashMap:UpdateAsync() ensures that all player contributions
make their way into this shared inventory, even if the contributions occur
simultaneously. The function enforces a max resource count of 500.

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local hashMap = MemoryStoreService:GetHashMap("ResourceInventory")



local function contributeResources(itemResource, addedCount)



local success, newResourceCount = pcall(function()



return hashMap:UpdateAsync(itemResource, function(resource)



resource = resource or { count = 0 }



resource.count = resource.count + addedCount



-- ensure we don't exceed the maximum resource count



if resource.count > 500 then



resource.count = 500



end



return resource



end, 1200)



end)



if success then



print(newResourceCount)



end



end



contributeResources("myResource", 50)
```

Provide feedback

---