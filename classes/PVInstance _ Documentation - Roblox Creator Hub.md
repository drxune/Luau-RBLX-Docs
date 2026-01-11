# PVInstance | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PVInstance
Scraped: 2026-01-11T02:34:06.697083Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- PVInstance
- BasePart
- Camera
- Model
- PVInstance:PivotTo()
- Models
- BaseParts
- PVInstances
- PVInstance:GetPivot()
- Model.WorldPivot
- Object.Changed
- Position
- Orientation
- PivotTo
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PVInstance](/docs/reference/engine/classes/PVInstance)

English

Feedback

Engine Class

PVInstance

Abstract class for all objects that have a physical location in the world.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [Origin](#Origin):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Pivot Offset](#Pivot-Offset):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Methods

|  |
| --- |
| [GetPivot](#GetPivot)():[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [PivotTo](#PivotTo)(targetCFrame: [CFrame](/docs/reference/engine/datatypes/CFrame)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[BasePart](/docs/reference/engine/classes/BasePart), [Camera](/docs/reference/engine/classes/Camera), [Model](/docs/reference/engine/classes/Model)

A [PVInstance](/docs/reference/engine/classes/PVInstance) is an abstract class that cannot be created. It is the
base for all objects that have a physical location in the world.

---

API Reference

Properties

Origin

Not Replicated

Not Scriptable

Read Parallel

PVInstance.Origin:[CFrame](/docs/reference/engine/datatypes/CFrame)

Provide feedback

---

Pivot Offset

Not Replicated

Not Scriptable

Read Parallel

PVInstance.Pivot Offset:[CFrame](/docs/reference/engine/datatypes/CFrame)

Provide feedback

---

Methods

GetPivot

Write Parallel

Gets the pivot of a [PVInstance](/docs/reference/engine/classes/PVInstance).

PVInstance:GetPivot():[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

This function gets the pivot of a [PVInstance](/docs/reference/engine/classes/PVInstance). This is often used
with [PVInstance:PivotTo()](/docs/reference/engine/classes/PVInstance#PivotTo) to move a model.

[Models](/docs/reference/engine/classes/Model) and [BaseParts](/docs/reference/engine/classes/BasePart) are both
[PVInstances](/docs/reference/engine/classes/PVInstance) ("Position Velocity Instances") and so both
have this function.

Code Samples

Simple Character Teleportation

This code sample is a simple teleport script that moves your character
10 studs forwards in the direction you're currently facing when you press
the F key. It does so by getting the current pivot with
[PVInstance:GetPivot()](/docs/reference/engine/classes/PVInstance#GetPivot) and calling PVInstance|PivotTo to move the
character forwards.

```
-- This code should be placed in a LocalScript under StarterPlayerScripts



local Players = game:GetService("Players")



local ContextActionService = game:GetService("ContextActionService")



local player = Players.LocalPlayer



local function doTeleport(_actionName, inputState, _inputObject)



local character = player.Character



if character and character.Parent and inputState == Enum.UserInputState.Begin then



-- Move the character 10 studs forwards in the direction they're facing



local currentPivot = character:GetPivot()



character:PivotTo(currentPivot * CFrame.new(0, 0, -10))



end



end



ContextActionService:BindAction("Teleport", doTeleport, true, Enum.KeyCode.F)
```

Provide feedback

---

PivotTo

Transforms the [PVInstance](/docs/reference/engine/classes/PVInstance) along with all of its descendant
[PVInstances](/docs/reference/engine/classes/PVInstance) such that the pivot is now located at the
specified [CFrame](/docs/reference/engine/datatypes/CFrame).

PVInstance:PivotTo(targetCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)):()

Parameters

|  |
| --- |
| targetCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)  The [CFrame](/docs/reference/engine/datatypes/CFrame) that the [PVInstance](/docs/reference/engine/classes/PVInstance) pivot should equal after moving it. |

Returns

()

Transforms the [PVInstance](/docs/reference/engine/classes/PVInstance) along with all of its descendant
[PVInstances](/docs/reference/engine/classes/PVInstance) such that the pivot is now located at the
specified [CFrame](/docs/reference/engine/datatypes/CFrame). This is the primary function that should be
used to move [Models](/docs/reference/engine/classes/Model) via scripting.

[BaseParts](/docs/reference/engine/classes/BasePart) are moved in this way by having their
[CFrame](/docs/reference/engine/datatypes/CFrame) transformed by the necessary offset.
[Models](/docs/reference/engine/classes/Model) are moved in this way by having their
[Model.WorldPivot](/docs/reference/engine/classes/Model#WorldPivot) transformed by the necessary offset.

Note that for efficiency purposes, [Object.Changed](/docs/reference/engine/classes/Object#Changed) events are not
fired for [Position](/docs/reference/engine/classes/BasePart#Position) and
[Orientation](/docs/reference/engine/classes/BasePart#Orientation) of [BaseParts](/docs/reference/engine/classes/BasePart)
moved in this way; they are only fired for [CFrame](/docs/reference/engine/datatypes/CFrame).

When calling [PivotTo](/docs/reference/engine/classes/PVInstance#PivotTo) on [Models](/docs/reference/engine/classes/Model),
the offsets of the descendant parts and models are cached, such that
subsequent calls to [PivotTo](/docs/reference/engine/classes/PVInstance#PivotTo) on the same model
do not accumulate floating point drift between the parts making up the
model.

[Models](/docs/reference/engine/classes/Model) and [BaseParts](/docs/reference/engine/classes/BasePart) are both
[PVInstances](/docs/reference/engine/classes/PVInstance) ("Position Velocity Instances") and so both
have this function.

Code Samples

Simple Character Teleportation

This code sample is a simple teleport script that moves your character
10 studs forwards in the direction you're currently facing when you press
the F key. It does so by getting the current pivot with
[PVInstance:GetPivot()](/docs/reference/engine/classes/PVInstance#GetPivot) and calling PVInstance|PivotTo to move the
character forwards.

```
-- This code should be placed in a LocalScript under StarterPlayerScripts



local Players = game:GetService("Players")



local ContextActionService = game:GetService("ContextActionService")



local player = Players.LocalPlayer



local function doTeleport(_actionName, inputState, _inputObject)



local character = player.Character



if character and character.Parent and inputState == Enum.UserInputState.Begin then



-- Move the character 10 studs forwards in the direction they're facing



local currentPivot = character:GetPivot()



character:PivotTo(currentPivot * CFrame.new(0, 0, -10))



end



end



ContextActionService:BindAction("Teleport", doTeleport, true, Enum.KeyCode.F)
```

Provide feedback

---