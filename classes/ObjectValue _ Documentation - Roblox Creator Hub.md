# ObjectValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ObjectValue
Scraped: 2026-01-11T02:40:22.460323Z

## Inherits
- ValueBase
- ObjectValue
- Instance
- Object
- Model.PrimaryPart
- Value
- ObjectValue.Value
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [ObjectValue](/docs/reference/engine/classes/ObjectValue)

English

Feedback

Engine Class

ObjectValue

A container object for a reference to another instance.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[Instance](/docs/reference/engine/datatypes/Instance) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Stores a single reference to another object. If this object is duplicated
within Studio and the value refers to an object also being copied, then the
new ObjectValue points to the copied object instead of the original.
Otherwise, the same value is kept. Copying and pasting this object clears the
value field.

You can set the value within Studio like other reference-type fields (such as
[Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart)): click the field within the Properties window, then
click the object you wish to set it to within the game view or Explorer
window. You can clear the field (set it to nil) by clicking the X that
appears when you click the field.

Like all [ValueBase](/docs/reference/engine/classes/ValueBase) objects, this single value is stored in the
[Value](/docs/reference/engine/classes/ObjectValue#Value) property. The Changed event fires with the
new value being stored in the object, instead of a string representing the
property being changed.

If [streaming](/docs/workspace/streaming) is enabled, the Value
property is nil until the referenced object streams in, at which point the
Changed event fires.

Code Samples

ObjectValue Example

This code sample creates an ObjectValue in the Workspace which holds a
reference to an object in the workspace named "Baseplate".

```
local objectValue = Instance.new("ObjectValue")



objectValue.Name = "MyBaseplateReference"



objectValue.Value = workspace:FindFirstChild("Baseplate")



objectValue.Parent = workspace
```

---

API Reference

Properties

Value

Read Parallel

Holds a reference to an instance.

ObjectValue.Value:[Instance](/docs/reference/engine/datatypes/Instance)

Holds a reference to an instance.

Provide feedback

---

Events

Changed

Fires whenever the [ObjectValue.Value](/docs/reference/engine/classes/ObjectValue#Value) is changed.

ObjectValue.Changed(value:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[Instance](/docs/reference/engine/datatypes/Instance)  The new value after the change. |

Fires whenever the [ObjectValue.Value](/docs/reference/engine/classes/ObjectValue#Value) changes. It runs with the new
value being stored in the argument object, instead of a string
representing the property being changed.

Listening for the Changed signal can be useful in games that use
ObjectValues to track game state, such as an RPG targeting system.

Code Samples

ObjectValue Changed

This example prints the path to the newly reference instance when
the [Value](/docs/reference/engine/classes/ObjectValue#Value) property is changed.

```
local objectValue = script.Parent.ObjectValue



local part = script.Parent.Part



local function printObject(object)



print(object:GetFullName())



end



objectValue.Changed:Connect(printObject)



objectValue.Value = part
```

Provide feedback

---

changed

Deprecated

Show details

---