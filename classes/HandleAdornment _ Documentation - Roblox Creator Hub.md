# HandleAdornment | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HandleAdornment
Scraped: 2026-01-11T02:30:23.120359Z

## Tags
- Not Creatable

## Inherits
- PVAdornment
- HandleAdornment
- GuiBase3d
- Instance
- Object
- BoxHandleAdornment
- ConeHandleAdornment
- CylinderHandleAdornment
- ImageHandleAdornment
- LineHandleAdornment
- PlayerGui
- CoreGui
- ZIndex
- AlwaysOnTop
- PVAdornment.Adornee
- SizeRelativeOffset
- BasePart.Size
- Adornee
- GuiObjects
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PVAdornment](/docs/reference/engine/classes/PVAdornment)
6. /
7. [HandleAdornment](/docs/reference/engine/classes/HandleAdornment)

English

Feedback

Engine Class

HandleAdornment

An abstract class inherited by 3D handle adornments.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [AdornCullingMode](#AdornCullingMode):[Enum.AdornCullingMode](/docs/reference/engine/enums/AdornCullingMode) |
| [AlwaysOnTop](#AlwaysOnTop):[boolean](/docs/luau/booleans) |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [SizeRelativeOffset](#SizeRelativeOffset):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ZIndex](#ZIndex):[number](/docs/luau/numbers) |

Events

|  |
| --- |
| [MouseButton1Down](#MouseButton1Down)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton1Up](#MouseButton1Up)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseEnter](#MouseEnter)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseLeave](#MouseLeave)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

1 inherited from [PVAdornment](/docs/reference/engine/classes/PVAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[BoxHandleAdornment](/docs/reference/engine/classes/BoxHandleAdornment), [ConeHandleAdornment](/docs/reference/engine/classes/ConeHandleAdornment), [CylinderHandleAdornment](/docs/reference/engine/classes/CylinderHandleAdornment), [ImageHandleAdornment](/docs/reference/engine/classes/ImageHandleAdornment), [LineHandleAdornment](/docs/reference/engine/classes/LineHandleAdornment), Show more...

HandleAdornment is an abstract class inherited by 3D handle adornments. If
parented to a player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) or the [CoreGui](/docs/reference/engine/classes/CoreGui), handles can
listen to input events for purposes such as making dragger tools.

---

API Reference

Properties

AdornCullingMode

Read Parallel

Determines whether to automatically cull the adornment.

HandleAdornment.AdornCullingMode:[Enum.AdornCullingMode](/docs/reference/engine/enums/AdornCullingMode)

This property determines whether to automatically cull the adornment based
on distance from the camera.

Provide feedback

---

AlwaysOnTop

Read Parallel

Forces this adornment to render on top of all 3D objects in the workspace.

HandleAdornment.AlwaysOnTop:[boolean](/docs/luau/booleans)

If true, forces this adornment to render on top of all 3D objects in the
workspace. As an exception, setting [ZIndex](/docs/reference/engine/classes/HandleAdornment#ZIndex)
to -1 will override an [AlwaysOnTop](/docs/reference/engine/classes/HandleAdornment#AlwaysOnTop)
value of true and cause the adornment to appear either in front of or
behind other adornments and objects based on their relative position in
the 3D space.

Provide feedback

---

CFrame

Read Parallel

The position and rotation of the object relative to its
[PVAdornment.Adornee](/docs/reference/engine/classes/PVAdornment#Adornee).

HandleAdornment.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

[CFrame](/docs/reference/engine/datatypes/CFrame) position and rotation relative to its
[PVAdornment.Adornee](/docs/reference/engine/classes/PVAdornment#Adornee), applied after any translations due to
[SizeRelativeOffset](/docs/reference/engine/classes/HandleAdornment#SizeRelativeOffset).

Provide feedback

---

SizeRelativeOffset

Read Parallel

The positional offset of the adornment based on the adornee's
[BasePart.Size](/docs/reference/engine/classes/BasePart#Size).

HandleAdornment.SizeRelativeOffset:[Vector3](/docs/reference/engine/datatypes/Vector3)

By default, an adornment draws in the center of its
[Adornee](/docs/reference/engine/classes/HandleAdornment#Adornee), but this property shifts the
adornment's relative position based on the adornee's
[BasePart.Size](/docs/reference/engine/classes/BasePart#Size).

Note that the units of
[SizeRelativeOffset](/docs/reference/engine/classes/HandleAdornment#SizeRelativeOffset) are a
scale based on the size of the adornee itself, such that a value of
1 will move the adornment to the corresponding edge of the adornee. For
example, a value of [Vector3.new(0, 1, 0)](/docs/reference/engine/datatypes/Vector3#new) will shift the
adornment to the exact top of its adornee.

Provide feedback

---

ZIndex

Read Parallel

Determines the draw order of this [HandleAdornment](/docs/reference/engine/classes/HandleAdornment) when
[AlwaysOnTop](/docs/reference/engine/classes/HandleAdornment#AlwaysOnTop) is true.

HandleAdornment.ZIndex:[number](/docs/luau/numbers)

Only applies if [AlwaysOnTop](/docs/reference/engine/classes/HandleAdornment#AlwaysOnTop) is true
and determines the draw order of this [HandleAdornment](/docs/reference/engine/classes/HandleAdornment) relative to
other adornments. It does not relate to the
[ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) property for [GuiObjects](/docs/reference/engine/classes/GuiObject).

Valid values are from -1 to 10 with higher values drawing on top (in
front) of lesser values. This drawing order will be respected even if an
adornment is in front of or behind another adornment in the 3D space.

As an exception, setting [ZIndex](/docs/reference/engine/classes/HandleAdornment#ZIndex) to -1 or
[AlwaysOnTop](/docs/reference/engine/classes/HandleAdornment#AlwaysOnTop) to false will cause the
adornment to appear either in front of or behind other adornments and
objects based on their relative position in the 3D space.

Provide feedback

---

Events

MouseButton1Down

Fires when a player presses down on their left mouse button while hovering
over the adornment.

HandleAdornment.MouseButton1Down():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when a player presses down their left mouse button while
hovering over the adornment. Only fires if the adornment is parented to a
player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) or the [CoreGui](/docs/reference/engine/classes/CoreGui).

Provide feedback

---

MouseButton1Up

Fires when a player releases their left mouse button while hovering over
the adornment.

HandleAdornment.MouseButton1Up():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when a player releases their left mouse button while
hovering over the adornment. Only fires if the adornment is parented to a
player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) or the [CoreGui](/docs/reference/engine/classes/CoreGui).

Provide feedback

---

MouseEnter

Fires when a player moves their mouse over the adornment.

HandleAdornment.MouseEnter():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when a player moves their mouse over the adornment. Only
fires if the adornment is parented to a player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) or the
[CoreGui](/docs/reference/engine/classes/CoreGui).

Provide feedback

---

MouseLeave

Fires when a player moves their mouse out of the adornment.

HandleAdornment.MouseLeave():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when a player moves their mouse out of the adornment.
Only fires if the adornment is parented to a player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) or
the [CoreGui](/docs/reference/engine/classes/CoreGui).

Provide feedback

---