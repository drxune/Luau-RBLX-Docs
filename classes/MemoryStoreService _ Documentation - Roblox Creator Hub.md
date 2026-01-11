# MemoryStoreService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MemoryStoreService
Scraped: 2026-01-11T02:32:19.885859Z

## Tags
- Service

## Inherits
- Instance
- MemoryStoreService
- MemoryStoreHashMap
- MemoryStoreQueue
- MemoryStoreSortedMap
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MemoryStoreService](/docs/reference/engine/classes/MemoryStoreService)

English

Feedback

Engine Class

![MemoryStoreService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/MemoryStoreService-Dark.webp)MemoryStoreService

Exposes methods to access specific primitives within MemoryStore.

Service

---

Summary

Methods

|  |
| --- |
| [GetHashMap](#GetHashMap)(name: [string](/docs/luau/strings)):[MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap) |
| [GetQueue](#GetQueue)(name: [string](/docs/luau/strings),invisibilityTimeout: [number](/docs/luau/numbers)):[MemoryStoreQueue](/docs/reference/engine/classes/MemoryStoreQueue) |
| [GetSortedMap](#GetSortedMap)(name: [string](/docs/luau/strings)):[MemoryStoreSortedMap](/docs/reference/engine/classes/MemoryStoreSortedMap) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A top-level singleton class which exposes methods to access specific
primitives within the MemoryStoreService. Use it for any data that rapidly
changes that other servers can restore, such as global leaderboards,
matchmaking queues, and auction houses.

For a more in-depth look, see
[Memory Stores](/docs/cloud-services/memory-stores). For the
limits and quotas of the service, see
[Limits and Quotas](/docs/cloud-services/memory-stores#limits-and-quotas).

---

API Reference

Methods

GetHashMap

Returns a [MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap) instance for the provided name.

MemoryStoreService:GetHashMap(name:[string](/docs/luau/strings)):[MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the hash map. |

Returns

[MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap)

A [MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap) instance for the provided name.

Returns a [MemoryStoreHashMap](/docs/reference/engine/classes/MemoryStoreHashMap) instance for the provided name. The
name is global within the game, so any place that uses the same name
accesses the same hash map.

Provide feedback

---

GetQueue

Returns a [MemoryStoreQueue](/docs/reference/engine/classes/MemoryStoreQueue) instance for the provided name.

MemoryStoreService:GetQueue(

name:[string](/docs/luau/strings), invisibilityTimeout:[number](/docs/luau/numbers)

):[MemoryStoreQueue](/docs/reference/engine/classes/MemoryStoreQueue)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Name of the queue. |
| invisibilityTimeout:[number](/docs/luau/numbers) Default Value: 30 (Optional) Invisibility timeout, in seconds, for read operations through this queue instance. If not provided, defaults to 30 seconds. |

Returns

[MemoryStoreQueue](/docs/reference/engine/classes/MemoryStoreQueue)

A [MemoryStoreQueue](/docs/reference/engine/classes/MemoryStoreQueue) instance for the provided name.

Returns a [MemoryStoreQueue](/docs/reference/engine/classes/MemoryStoreQueue) instance for the provided name. The
name is global within the game, thus any place that uses the same name
accesses the same queue.

Provide feedback

---

GetSortedMap

Returns a [MemoryStoreSortedMap](/docs/reference/engine/classes/MemoryStoreSortedMap) instance for the provided name.

MemoryStoreService:GetSortedMap(name:[string](/docs/luau/strings)):[MemoryStoreSortedMap](/docs/reference/engine/classes/MemoryStoreSortedMap)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Name of the sorted map. |

Returns

[MemoryStoreSortedMap](/docs/reference/engine/classes/MemoryStoreSortedMap)

A [MemoryStoreSortedMap](/docs/reference/engine/classes/MemoryStoreSortedMap) instance for the provided name.

Returns a [MemoryStoreSortedMap](/docs/reference/engine/classes/MemoryStoreSortedMap) instance for the provided name. The
name is global within the game, so any place that uses the same name
accesses the same sorted map.

Provide feedback

---