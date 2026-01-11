# RBXScriptConnection | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/RBXScriptConnection
Scraped: 2026-01-11T02:41:47.991882Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

English

Feedback

Engine Data Type

RBXScriptConnection

A connection between an [RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) and a function.

---

Summary

Properties

|  |
| --- |
| [Connected](#Connected):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [Disconnect](#Disconnect)():() |

The RBXScriptConnection data type is a special object returned by the
[Connect()](/docs/reference/engine/datatypes/RBXScriptSignal#Connect) method of an event
([RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)). This is used primarily to disconnect a listener
from an [RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal).

```
local part : BasePart = script.Parent



-- Store reference to the RBXScriptConnection so it can be disconnected later



local connection : RBXScriptConnection = part.Touched:Connect(function(otherPart)



print("Hello world!")



end)



-- Wait 15 seconds, then disconnect



task.wait(15)



connection:Disconnect()
```

---

API Reference

Properties

Connected

The state of the RBXScriptConnection.

RBXScriptConnection.Connected:[boolean](/docs/luau/booleans)

Describes whether or not the connection is still alive. This becomes
false if [Disconnect()](/docs/reference/engine/datatypes/RBXScriptConnection#Disconnect) is
called.

Provide feedback

---

Methods

Disconnect

Disconnects the connection from the event.

RBXScriptConnection:Disconnect():()

Returns

()

Disconnects the connection from the event.

Provide feedback

---