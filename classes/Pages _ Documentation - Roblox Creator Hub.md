# Pages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Pages
Scraped: 2026-01-11T02:38:12.890570Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- Pages
- AudioPages
- BanHistoryPages
- CapturesPages
- CatalogPages
- DataStoreKeyPages
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Pages](/docs/reference/engine/classes/Pages)

English

Feedback

Engine Class

Pages

An abstract class for pages objects.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [IsFinished](#IsFinished):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [AdvanceToNextPageAsync](#AdvanceToNextPageAsync)():() |
| [GetCurrentPage](#GetCurrentPage)():[Array](/docs/luau/tables#arrays) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[AudioPages](/docs/reference/engine/classes/AudioPages), [BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages), [CapturesPages](/docs/reference/engine/classes/CapturesPages), [CatalogPages](/docs/reference/engine/classes/CatalogPages), [DataStoreKeyPages](/docs/reference/engine/classes/DataStoreKeyPages), Show more...

An object which is essentially a table of pages, each of which is a sorted
list of the key/value pairs.

Code Samples

Pages Iterator

When each page in a [Pages](/docs/reference/engine/classes/Pages) object contains a list of multiple items, this
iterator function and its helper may be useful.

```
-- Reformat pages as tables



local function pagesToTable(pages)



local items = {}



while true do



table.insert(items, pages:GetCurrentPage())



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



end



return items



end



local function iterPageItems(pages)



local contents = pagesToTable(pages)



-- Track the current page number starting at 1



local pageNum = 1



-- Get last page number so we don't iterate over it



local lastPageNum = #contents



-- for resumes this coroutine until there's nothing to go through



return coroutine.wrap(function()



-- Loop until page number is greater than last page number



while pageNum <= lastPageNum do



-- Go through all the entries of the current page



for _, item in ipairs(contents[pageNum]) do



-- Pause loop to let developer handle entry and page number



coroutine.yield(item, pageNum)



end



pageNum += 1



end



end)



end



-- Using the iterPageItems function to iterate through the pages of a catalog search



local AvatarEditorService = game:GetService("AvatarEditorService")



local parameters = CatalogSearchParams.new()



parameters.SearchKeyword = "Hair"



local catalogPages = AvatarEditorService:SearchCatalog(parameters)



for item, pageNumber in iterPageItems(catalogPages) do



print(item, pageNumber)



end
```

---

API Reference

Properties

IsFinished

Read Only

Not Replicated

Read Parallel

Whether or not the current page is the last page available.

Pages.IsFinished:[boolean](/docs/luau/booleans)

Whether or not the current page is the last page available.

Provide feedback

---

Methods

AdvanceToNextPageAsync

Yields

Iterates to the next page in the pages object, if possible.

Pages:AdvanceToNextPageAsync():()

Returns

()

Iterates to the next page in the pages object, if possible. The request
limit is the same of the endpoint originally called.

Provide feedback

---

GetCurrentPage

Returns the items on the current page. The keys in the item are determined
by the source of this object.

Pages:GetCurrentPage():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns the items on the current page. The keys in the item are determined
by the source of this object.

Provide feedback

---