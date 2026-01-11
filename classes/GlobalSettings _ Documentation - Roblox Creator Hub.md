# GlobalSettings | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GlobalSettings
Scraped: 2026-01-11T02:38:59.210780Z

## Tags
- Not Creatable

## Inherits
- GenericSettings
- GlobalSettings
- ServiceProvider
- Instance
- Object
- DebugSettings
- GameSettings
- LuaSettings
- NetworkSettings
- PhysicsSettings
- RenderSettings
- Studio
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GenericSettings](/docs/reference/engine/classes/GenericSettings)
6. /
7. [GlobalSettings](/docs/reference/engine/classes/GlobalSettings)

English

Feedback

Engine Class

GlobalSettings

Collection of menu settings for Roblox Studio.

Not Creatable

Not Browsable

---

Summary

Methods

|  |
| --- |
| [GetFFlag](#GetFFlag)(name: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [GetFVariable](#GetFVariable)(name: [string](/docs/luau/strings)):[string](/docs/luau/strings) |

Inherited Members

7 inherited from [ServiceProvider](/docs/reference/engine/classes/ServiceProvider)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The base object used for Roblox Studio's settings menu. Can be accessed by
using the settings() function.

Settings classes under the GlobalSettings
-----------------------------------------

* [DebugSettings](/docs/reference/engine/classes/DebugSettings)
* [GameSettings](/docs/reference/engine/classes/GameSettings)
* [LuaSettings](/docs/reference/engine/classes/LuaSettings)
* [NetworkSettings](/docs/reference/engine/classes/NetworkSettings)
* [PhysicsSettings](/docs/reference/engine/classes/PhysicsSettings)
* [RenderSettings](/docs/reference/engine/classes/RenderSettings)
* [Studio](/docs/reference/engine/classes/Studio)

---

API Reference

Methods

GetFFlag

Returns the value of an FFlag if it exists.

GlobalSettings:GetFFlag(name:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

Returns the value of an FFlag if it exists.

Provide feedback

---

GetFVariable

Returns the value of an FVariable, if it exists.

GlobalSettings:GetFVariable(name:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

[string](/docs/luau/strings)

Returns the value of an FVariable, if it exists.

Provide feedback

---