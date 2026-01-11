# ScriptContext | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ScriptContext
Scraped: 2026-01-11T02:30:49.756498Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- ScriptContext
- BaseScript
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ScriptContext](/docs/reference/engine/classes/ScriptContext)

English

Feedback

Engine Class

ScriptContext

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [SetTimeout](#SetTimeout)(seconds: [number](/docs/luau/numbers)):() |

Events

|  |
| --- |
| [Error](#Error)(message: [string](/docs/luau/strings),stackTrace: [string](/docs/luau/strings),script: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This service controls all [BaseScript](/docs/reference/engine/classes/BaseScript) objects. Most of the properties
and methods of this service are locked for internal use.

---

API Reference

Methods

SetTimeout

Plugin Security

Limits how long a script is allowed to run without yielding.

ScriptContext:SetTimeout(seconds:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| seconds:[number](/docs/luau/numbers) |

Returns

()

Limits how long a script is allowed to run without yielding.

Provide feedback

---

Events

Error

Fired when an error occurs.

ScriptContext.Error(

message:[string](/docs/luau/strings), stackTrace:[string](/docs/luau/strings), script:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings) |
| stackTrace:[string](/docs/luau/strings) |
| script:[Instance](/docs/reference/engine/datatypes/Instance) |

Fired when an error occurs.

Code Samples

ScriptContext.Error

When an error occurs, this example prints the name of the script that errored,
the reason it errored, and a trace of the error.

```
local ScriptContext = game:GetService("ScriptContext")



local function onError(message, trace, script)



print(script:GetFullName(), "errored!")



print("Reason:", message)



print("Trace:", trace)



end



ScriptContext.Error:Connect(onError)



-- Somewhere, in another script



error("Error occurred!")
```

Provide feedback

---