# SharedTableRegistry | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SharedTableRegistry
Scraped: 2026-01-11T02:32:59.604777Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- SharedTableRegistry
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [SharedTableRegistry](/docs/reference/engine/classes/SharedTableRegistry)

English

Feedback

Engine Class

SharedTableRegistry

Provides a global registry of named [SharedTable](/docs/reference/engine/datatypes/SharedTable) objects.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetSharedTable](#GetSharedTable)(name: [string](/docs/luau/strings)):[SharedTable](/docs/reference/engine/datatypes/SharedTable) |
| [SetSharedTable](#SetSharedTable)(name: [string](/docs/luau/strings),st: [SharedTable](/docs/reference/engine/datatypes/SharedTable)?):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Provides a global registry of named [SharedTable](/docs/reference/engine/datatypes/SharedTable) objects. It can be
used to store [SharedTable](/docs/reference/engine/datatypes/SharedTable) objects that are used by multiple
scripts.

---

API Reference

Methods

GetSharedTable

Write Parallel

Gets the registered [SharedTable](/docs/reference/engine/datatypes/SharedTable) with the specified name.

SharedTableRegistry:GetSharedTable(name:[string](/docs/luau/strings)):[SharedTable](/docs/reference/engine/datatypes/SharedTable)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the registered [SharedTable](/docs/reference/engine/datatypes/SharedTable). |

Returns

[SharedTable](/docs/reference/engine/datatypes/SharedTable)

Gets the registered [SharedTable](/docs/reference/engine/datatypes/SharedTable) with the specified name. If no
[SharedTable](/docs/reference/engine/datatypes/SharedTable) with that name exists, a new [SharedTable](/docs/reference/engine/datatypes/SharedTable)
is created with that name and is returned.

```
local SharedTableRegistry = game:GetService("SharedTableRegistry")



local st = SharedTableRegistry:GetSharedTable("MyData")
```

Provide feedback

---

SetSharedTable

Write Parallel

Registers the provided [SharedTable](/docs/reference/engine/datatypes/SharedTable) with the specified name.

SharedTableRegistry:SetSharedTable(

name:[string](/docs/luau/strings), st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)?

):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the registered [SharedTable](/docs/reference/engine/datatypes/SharedTable). |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)?  The [SharedTable](/docs/reference/engine/datatypes/SharedTable) object to register, or nil to unregister any previously registered [SharedTable](/docs/reference/engine/datatypes/SharedTable) object. |

Returns

()

Registers the provided [SharedTable](/docs/reference/engine/datatypes/SharedTable) with the specified name. If
the provided [SharedTable](/docs/reference/engine/datatypes/SharedTable) is nil, any existing
[SharedTable](/docs/reference/engine/datatypes/SharedTable) with the specified name is unregistered.

```
local SharedTableRegistry = game:GetService("SharedTableRegistry")



-- Register a SharedTable with the name "MyData":



local st = SharedTable.new({1, 2, 3})



SharedTableRegistry:SetSharedTable("MyData", st)



-- Unregister the SharedTable with the name "MyData":



SharedTableRegistry:SetSharedTable("MyData", nil)
```

Provide feedback

---