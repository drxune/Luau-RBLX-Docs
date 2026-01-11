# MemoryStoreQueue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MemoryStoreQueue
Scraped: 2026-01-11T02:33:41.753818Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- MemoryStoreQueue
- Object
- MemoryStoreQueue:RemoveAsync()
- MemoryStoreService:GetQueue()
- MemoryStoreQueue:ReadAsync()
- DataStoreService:UpdateAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MemoryStoreQueue](/docs/reference/engine/classes/MemoryStoreQueue)

English

Feedback

Engine Class

MemoryStoreQueue

Provides access to a queue within MemoryStore.

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [AddAsync](#AddAsync)(value: Variant,expiration: [number](/docs/luau/numbers),priority: [number](/docs/luau/numbers)):() |
| [GetSizeAsync](#GetSizeAsync)(excludeInvisible: [boolean](/docs/luau/booleans)):[number](/docs/luau/numbers) |
| [ReadAsync](#ReadAsync)(count: [number](/docs/luau/numbers),allOrNothing: [boolean](/docs/luau/booleans),waitTimeout: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |
| [RemoveAsync](#RemoveAsync)(id: [string](/docs/luau/strings)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Provides access to a queue within MemoryStore. A queue is a data structure
that provides temporary storage for arbitrary items (up to the maximum item
size -- see
[MemoryStore Limits](/docs/cloud-services/memory-stores#limits-and-quotas)).
Each queue item has a numeric priority: MemoryStore retrieves items with
higher priority from the queue first, and it retrieves Items with the same
priority in order of addition.

Items in the queue can optionally be set to expire after a certain amount of
time. Expired items simply disappear from the queue as if they were never
added.

---

API Reference

Methods

AddAsync

Yields

Adds an item to the queue.

MemoryStoreQueue:AddAsync(

value:Variant, expiration:[number](/docs/luau/numbers), priority:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| value:Variant  The value of the item to add to the queue. |
| expiration:[number](/docs/luau/numbers)  Item expiration time, in seconds, after which the item will be automatically removed from the queue. |
| priority:[number](/docs/luau/numbers) Default Value: 0 Item priority. Items with higher priority are retrieved from the queue before items with lower priority. |

Returns

()

Adds an item to the queue.

Provide feedback

---

GetSizeAsync

Yields

Gets the size of the queue.

MemoryStoreQueue:GetSizeAsync(excludeInvisible:[boolean](/docs/luau/booleans)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| excludeInvisible:[boolean](/docs/luau/booleans) Default Value: false Determines whether to exclude invisible items from the size count. |

Returns

[number](/docs/luau/numbers)

Gets the size of the queue.

Provide feedback

---

ReadAsync

Yields

Reads one or more items from the queue.

MemoryStoreQueue:ReadAsync(

count:[number](/docs/luau/numbers), allOrNothing:[boolean](/docs/luau/booleans), waitTimeout:[number](/docs/luau/numbers)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| count:[number](/docs/luau/numbers)  Number of items to read. The maximum allowed value of this parameter is 100. |
| allOrNothing:[boolean](/docs/luau/booleans) Default Value: false Controls the behavior of the method in the case the queue has fewer than count items: if set to false the method returns all available items; if set to true, it returns no items. The default value is false. |
| waitTimeout:[number](/docs/luau/numbers) Default Value: -1 The duration, in seconds, for which the method will wait if the required number of items is not immediately available in the queue. Reads are attempted every two seconds during this period. This parameter can be set to zero to indicate no wait. If this parameter is not provided or set to -1, the method will wait indefinitely. |

Returns

[Tuple](/docs/luau/tuples)

A tuple of two elements. The first element is an array of item values
read from the queue. The second element is a string identifier that
should be passed to [MemoryStoreQueue:RemoveAsync()](/docs/reference/engine/classes/MemoryStoreQueue#RemoveAsync) to
permanently remove these items from the queue.

Reads one or more items from the queue as a single atomic operation.

This method does not automatically delete the returned items from the
queue but makes them invisible to other ReadAsync calls for the period of
the invisibility timeout. The items must be explicitly removed from the
queue with [MemoryStoreQueue:RemoveAsync()](/docs/reference/engine/classes/MemoryStoreQueue#RemoveAsync) before the invisibility
timeout expires. The invisibility timeout defaults to 30 seconds unless a
different value was provided in [MemoryStoreService:GetQueue()](/docs/reference/engine/classes/MemoryStoreService#GetQueue).

Code Samples

Using a MemoryStoreQueue

The following code sample demonstrates using
[MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync) and
[MemoryStoreQueue:RemoveAsync()](/docs/reference/engine/classes/MemoryStoreQueue#RemoveAsync) to reliably read, process, and remove
items from a queue. Though this process can be as complicated as necessary,
this example simply sets a flag in the corresponding data store item, which
guarantees that every item will eventually be processed even if
some of the calls encounter errors or the server crashes:

* If [MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync) fails, no items are retrieved from
  the queue. An item will be picked up for processing during the next iteration
  of the loop.
* If [MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync) succeeds but
  [DataStoreService:UpdateAsync()](/docs/reference/engine/classes/DataStoreService#UpdateAsync) fails, the item stays invisible until
  the queue's invisibility timeout expires, causing the item becoming visible
  again to be returned in a future loop iteration.
* Similarly, if [MemoryStoreQueue:RemoveAsync()](/docs/reference/engine/classes/MemoryStoreQueue#RemoveAsync) fails, the item will
  become visible again in the future and will be processed again.

Depending on where the failure happens, it's possible that an item
will be processed more than once. You should account for that like the
following code sample, in which the end result is the same even if
[DataStoreService:UpdateAsync()](/docs/reference/engine/classes/DataStoreService#UpdateAsync) is invoked multiple times.

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local DataStoreService = game:GetService("DataStoreService")



local queue = MemoryStoreService:GetQueue("PlayerQueue")



local dataStore = DataStoreService:GetDataStore("PlayerStore")



while true do



pcall(function()



-- wait for an item to process



local items, id = queue:ReadAsync(1, false, 30)



-- check if an item was retrieved



if #items > 0 then



-- mark the item as processed



dataStore:UpdateAsync(items[0], function(data)



data = data or {}



data.processed = 1



return data



end)



-- remove the item from the queue



queue:RemoveAsync(id)



end



end)



end
```

Provide feedback

---

RemoveAsync

Yields

Removes an item or items previously read from the queue.

MemoryStoreQueue:RemoveAsync(id:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| id:[string](/docs/luau/strings)  Identifies the items to delete. Use the value returned by [MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync). |

Returns

()

Removes an item or items previously read from the queue. This method uses
the identifier returned by [MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync) to
identify the items to remove. If called after the invisibility timeout has
expired, the call has no effect.

Code Samples

Using a MemoryStoreQueue

The following code sample demonstrates using
[MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync) and
[MemoryStoreQueue:RemoveAsync()](/docs/reference/engine/classes/MemoryStoreQueue#RemoveAsync) to reliably read, process, and remove
items from a queue. Though this process can be as complicated as necessary,
this example simply sets a flag in the corresponding data store item, which
guarantees that every item will eventually be processed even if
some of the calls encounter errors or the server crashes:

* If [MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync) fails, no items are retrieved from
  the queue. An item will be picked up for processing during the next iteration
  of the loop.
* If [MemoryStoreQueue:ReadAsync()](/docs/reference/engine/classes/MemoryStoreQueue#ReadAsync) succeeds but
  [DataStoreService:UpdateAsync()](/docs/reference/engine/classes/DataStoreService#UpdateAsync) fails, the item stays invisible until
  the queue's invisibility timeout expires, causing the item becoming visible
  again to be returned in a future loop iteration.
* Similarly, if [MemoryStoreQueue:RemoveAsync()](/docs/reference/engine/classes/MemoryStoreQueue#RemoveAsync) fails, the item will
  become visible again in the future and will be processed again.

Depending on where the failure happens, it's possible that an item
will be processed more than once. You should account for that like the
following code sample, in which the end result is the same even if
[DataStoreService:UpdateAsync()](/docs/reference/engine/classes/DataStoreService#UpdateAsync) is invoked multiple times.

```
local MemoryStoreService = game:GetService("MemoryStoreService")



local DataStoreService = game:GetService("DataStoreService")



local queue = MemoryStoreService:GetQueue("PlayerQueue")



local dataStore = DataStoreService:GetDataStore("PlayerStore")



while true do



pcall(function()



-- wait for an item to process



local items, id = queue:ReadAsync(1, false, 30)



-- check if an item was retrieved



if #items > 0 then



-- mark the item as processed



dataStore:UpdateAsync(items[0], function(data)



data = data or {}



data.processed = 1



return data



end)



-- remove the item from the queue



queue:RemoveAsync(id)



end



end)



end
```

Provide feedback

---