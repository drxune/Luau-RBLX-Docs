# LogService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LogService
Scraped: 2026-01-11T02:28:55.818387Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- LogService
- LogService.GetLogHistory
- LogService.ClearOutput
- LogService.MessageOut
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [LogService](/docs/reference/engine/classes/LogService)

English

Feedback

Engine Class

LogService

A service that allows you to read outputted text.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [ClearOutput](#ClearOutput)():() |
| [GetLogHistory](#GetLogHistory)():[Array](/docs/luau/tables#arrays) |

Events

|  |
| --- |
| [MessageOut](#MessageOut)(message: [string](/docs/luau/strings),messageType: [Enum.MessageType](/docs/reference/engine/enums/MessageType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Important notes about this service: This service might have unexpected or
unreliable behavior depending on how games and the game engine log things.
Content might also be truncated. Don't rely on contents of events and messages
emitted by this service for any important game logic.

A service that allows you to read outputted text.

---

API Reference

Methods

ClearOutput

Clears the Roblox Studio output window.

LogService:ClearOutput():()

Returns

()

Clears the Roblox Studio output window.

The log history is also cleared, such that
[LogService.GetLogHistory](/docs/reference/engine/classes/LogService#GetLogHistory) will not return any entries from before
the [LogService.ClearOutput](/docs/reference/engine/classes/LogService#ClearOutput) call.

Provide feedback

---

GetLogHistory

Returns a table of tables, each with the message string, message type, and
timestamp of a message that the client displays in the output window.

LogService:GetLogHistory():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Unreliable Behavior This may have changing, unexpected or unreliable
behavior depending on how the game engine logs things. It should not be
relied upon for any important game logic.

Returns a table of tables, each with the message string, message type, and
timestamp of a message that the client displays in the output window.

See also:

* [LogService.MessageOut](/docs/reference/engine/classes/LogService#MessageOut) - An event that fires when text is added
  to the output from the client

Provide feedback

---

Events

MessageOut

Fires when the client outputs text.

LogService.MessageOut(

message:[string](/docs/luau/strings), messageType:[Enum.MessageType](/docs/reference/engine/enums/MessageType)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings) |
| messageType:[Enum.MessageType](/docs/reference/engine/enums/MessageType) |

Fires when the client outputs text.

Code Samples

LogService.MessageOut

Code and output

```
local LogService = game:GetService("LogService")



local messageLabel = Instance.new("Message")



messageLabel.Parent = workspace



local function onMessageOut(message, messageType)



messageLabel.Text = "The message was " .. message .. " and the type was " .. tostring(messageType)



end



LogService.MessageOut:Connect(onMessageOut)
```

Provide feedback

---