# CFrameValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CFrameValue
Scraped: 2026-01-11T02:39:40.158165Z

## Inherits
- ValueBase
- CFrameValue
- Instance
- Object
- CFrameValue.Value
- NumberValue
- StringValue
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [CFrameValue](/docs/reference/engine/classes/CFrameValue)

English

Feedback

Engine Class

![CFrameValue](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/CFrameValue-Dark.webp)CFrameValue

A container object for a single CFrame value.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [CFrame](/docs/reference/engine/datatypes/CFrame)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [CFrame](/docs/reference/engine/datatypes/CFrame)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A container object for a single [CFrame](/docs/reference/engine/datatypes/CFrame) value.

Code Samples

Store the Camera's CFrame

This code sample creates a CFrameValue whose Value is set to the camera's
current CFrame. This CFrame can be later recalled back into the camera's
CFrame.

```
-- Create a CFrame that stores the camera's current position/orientation



local vSnapshot = Instance.new("CFrameValue")



vSnapshot.Value = workspace.CurrentCamera.CFrame



vSnapshot.Name = "Snapshot"



vSnapshot.Parent = workspace



-- Later, we can load the CFrame back into the camera



workspace.CurrentCamera.CFrame = vSnapshot.Value
```

---

API Reference

Properties

Value

Read Parallel

Used to hold a [CFrame](/docs/reference/engine/datatypes/CFrame) value.

CFrameValue.Value:[CFrame](/docs/reference/engine/datatypes/CFrame)

Used to hold a [CFrame](/docs/reference/engine/datatypes/CFrame) value.

Provide feedback

---

Events

Changed

Fired whenever the [CFrameValue.Value](/docs/reference/engine/classes/CFrameValue#Value) of the CFrameValue is
changed.

CFrameValue.Changed(value:[CFrame](/docs/reference/engine/datatypes/CFrame)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[CFrame](/docs/reference/engine/datatypes/CFrame)  The new value after the change. |

Fired whenever the [CFrameValue.Value](/docs/reference/engine/classes/CFrameValue#Value) of the [CFrameValue](/docs/reference/engine/classes/CFrameValue) is
changed. It will run with the new value being stored in the argument
object, instead of a string representing the property being changed.

This event, like other changed events, can be used to track when an
CFrameValue changes and to track the different values that it may change
to.

For instance, this even may be useful in games that rely on CFrameValues
to track game object [CFrame](/docs/reference/engine/datatypes/CFrame) positions and movements.

Equivalent changed events exist for similar objects, such as
[NumberValue](/docs/reference/engine/classes/NumberValue) and [StringValue](/docs/reference/engine/classes/StringValue), depending on what object type
best suits the need.

Code Samples

CFrameValue.Changed

This example prints the CFrameValue's new value each time it changes.

```
local cframeValue = script.Parent.CFrameValue



cframeValue.Changed:Connect(print)



cframeValue.Value = CFrame.new(1, 2, 3)
```

Provide feedback

---

changed

Deprecated

Show details

---