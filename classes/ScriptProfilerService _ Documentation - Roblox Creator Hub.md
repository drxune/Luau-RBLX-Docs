# ScriptProfilerService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ScriptProfilerService
Scraped: 2026-01-11T02:28:49.985095Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- ScriptProfilerService
- Player
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ScriptProfilerService](/docs/reference/engine/classes/ScriptProfilerService)

English

Feedback

Engine Class

ScriptProfilerService

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [ClientRequestData](#ClientRequestData)(player: [Player](/docs/reference/engine/classes/Player)):() |
| [ClientStart](#ClientStart)(player: [Player](/docs/reference/engine/classes/Player),frequency: [number](/docs/luau/numbers)?):() |
| [ClientStop](#ClientStop)(player: [Player](/docs/reference/engine/classes/Player)):() |
| [DeserializeJSON](#DeserializeJSON)(jsonString: [string](/docs/luau/strings)?):[Dictionary](/docs/luau/tables#dictionaries) |
| [ServerRequestData](#ServerRequestData)():() |
| [ServerStart](#ServerStart)(frequency: [number](/docs/luau/numbers)?):() |
| [ServerStop](#ServerStop)():() |

Events

|  |
| --- |
| [OnNewData](#OnNewData)(player: [Player](/docs/reference/engine/classes/Player),jsonString: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Methods

ClientRequestData

Plugin Security

ScriptProfilerService:ClientRequestData(player:[Player](/docs/reference/engine/classes/Player)):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |

Returns

()

Provide feedback

---

ClientStart

Plugin Security

ScriptProfilerService:ClientStart(

player:[Player](/docs/reference/engine/classes/Player), frequency:[number](/docs/luau/numbers)?

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |
| frequency:[number](/docs/luau/numbers)? |

Returns

()

Provide feedback

---

ClientStop

Plugin Security

ScriptProfilerService:ClientStop(player:[Player](/docs/reference/engine/classes/Player)):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |

Returns

()

Provide feedback

---

DeserializeJSON

Plugin Security

ScriptProfilerService:DeserializeJSON(jsonString:[string](/docs/luau/strings)?):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| jsonString:[string](/docs/luau/strings)? |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Provide feedback

---

ServerRequestData

Plugin Security

ScriptProfilerService:ServerRequestData():()

Returns

()

Provide feedback

---

ServerStart

Plugin Security

ScriptProfilerService:ServerStart(frequency:[number](/docs/luau/numbers)?):()

Parameters

|  |
| --- |
| frequency:[number](/docs/luau/numbers)? |

Returns

()

Provide feedback

---

ServerStop

Plugin Security

ScriptProfilerService:ServerStop():()

Returns

()

Provide feedback

---

Events

OnNewData

Plugin Security

ScriptProfilerService.OnNewData(

player:[Player](/docs/reference/engine/classes/Player), jsonString:[string](/docs/luau/strings)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |
| jsonString:[string](/docs/luau/strings) |

Provide feedback

---