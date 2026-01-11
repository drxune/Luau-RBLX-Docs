# MatchmakingService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MatchmakingService
Scraped: 2026-01-11T02:29:04.343480Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- MatchmakingService
- Object
- InitializeServerAttributesForStudio
- GetServerAttribute
- SetServerAttribute
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MatchmakingService](/docs/reference/engine/classes/MatchmakingService)

English

Feedback

Engine Class

MatchmakingService

The service responsible for managing custom matchmaking data.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetServerAttribute](#GetServerAttribute)(name: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [InitializeServerAttributesForStudio](#InitializeServerAttributesForStudio)(serverAttributes: [Dictionary](/docs/luau/tables#dictionaries)):[Tuple](/docs/luau/tuples) |
| [SetServerAttribute](#SetServerAttribute)(name: [string](/docs/luau/strings),value: Variant):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[MatchmakingService](/docs/reference/engine/classes/MatchmakingService) is responsible for managing custom matchmaking
attributes. Use it to read and write matchmaking data.

---

API Reference

Methods

GetServerAttribute

Retrieves the value of a specific server attribute.

MatchmakingService:GetServerAttribute(name:[string](/docs/luau/strings)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the server attribute. Limited to a maximum of 50 characters. |

Returns

[Tuple](/docs/luau/tuples)

Returns the server attribute value if the attribute is found and if
the error is nil. Otherwise, returns nil for the attribute value
and an error message.

Retrieves the value of a specific server attribute.

Provide feedback

---

InitializeServerAttributesForStudio

Initiates the server attribute schema and its values to test in Studio.

MatchmakingService:InitializeServerAttributesForStudio(serverAttributes:[Dictionary](/docs/luau/tables#dictionaries)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| serverAttributes:[Dictionary](/docs/luau/tables#dictionaries)  An array of attribute name-value pairs. |

Returns

[Tuple](/docs/luau/tuples)

Returns true if the call succeeded. Otherwise, returns false and
an error message.

Initiates the server attribute schema and its values to test in Studio.
This method is optional and has no effect when running outside of Studio.

Provide feedback

---

SetServerAttribute

Assigns a value to a specific server attribute.

MatchmakingService:SetServerAttribute(

name:[string](/docs/luau/strings), value:Variant

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the server attribute. Limited to a maximum of 50 characters. |
| value:Variant  The value of the server attribute. Limited to a maximum of 50 characters. |

Returns

[Tuple](/docs/luau/tuples)

Returns true if the call succeeded. Otherwise, returns false and
an error message.

Assigns a value to a specific server attribute.

Code Samples

MatchmakingService sample

The following code sample:

* Tests the hard-coded Level, Elo, and TrainingMode attributes in Studio with [InitializeServerAttributesForStudio](/docs/reference/engine/classes/MatchmakingService#InitializeServerAttributesForStudio).
* Gets the Level attribute with [GetServerAttribute](/docs/reference/engine/classes/MatchmakingService#GetServerAttribute).
* Updates the player's Level attribute with [SetServerAttribute](/docs/reference/engine/classes/MatchmakingService#SetServerAttribute).

```
```lua title="Server attribute example"



local MatchmakingService = game:GetService("MatchmakingService")



local RunService = game:GetService("RunService")



if RunService:IsStudio() then



-- Sets up initial attributes and schema for testing



MatchmakingService:InitializeServerAttributesForStudio({



Level = "Advanced",



Elo = 123.456,



TrainingMode = true



})



end



-- Retrieves the Level attribute



local currentLevel, errorMessage = MatchmakingService:GetServerAttribute("Level")



if errorMessage then



warn(errorMessage)



else



print("Current level: " .. currentLevel)



end



-- Updates the Level attribute value to Advanced



local success, errorMessage = MatchmakingService:SetServerAttribute("Level", "Advanced")



if not success then



warn("Failed to update server attribute [Level] to [Advanced] due to error: " .. errorMessage)



else



print("Successfully set [Level] to [Advanced]")



end



```
```

Provide feedback

---