# MemoryStoreHashMapPages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MemoryStoreHashMapPages
Scraped: 2026-01-11T02:38:46.177397Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Pages
- MemoryStoreHashMapPages
- MemoryStoreHashMap
- Instance
- Object
- Pages:GetCurrentPage()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Pages](/docs/reference/engine/classes/Pages)
6. /
7. [MemoryStoreHashMapPages](/docs/reference/engine/classes/MemoryStoreHashMapPages)

English

Feedback

Engine Class

MemoryStoreHashMapPages

A special type of [Pages](/docs/reference/engine/classes/Pages) object whose pages contain key-value pairs
from a [MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap).

Not Creatable

Not Replicated

---

Summary

Inherited Members

3 inherited from [Pages](/docs/reference/engine/classes/Pages)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A special type of [Pages](/docs/reference/engine/classes/Pages) object whose pages contain key-value pairs
from a [MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap). [Pages:GetCurrentPage()](/docs/reference/engine/classes/Pages#GetCurrentPage) can be used
to retrieve an array of tables, each containing a key and value; these reflect
the key-value pair data.

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