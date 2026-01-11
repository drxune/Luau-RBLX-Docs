# ArcHandles | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ArcHandles
Scraped: 2026-01-11T02:27:41.944940Z

## Inherits
- HandlesBase
- ArcHandles
- Adornee
- PartAdornment
- GuiBase3d
- Instance
- Object
- PlayerGui
- CoreGui
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [HandlesBase](/docs/reference/engine/classes/HandlesBase)
6. /
7. [ArcHandles](/docs/reference/engine/classes/ArcHandles)

English

Feedback

Engine Class

![ArcHandles](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ArcHandles-Dark.webp)ArcHandles

The [ArcHandles](/docs/reference/engine/classes/ArcHandles) object places 3D arc handles around any 3D object that
its [Adornee](/docs/reference/engine/classes/PartAdornment#Adornee) is set to.

---

Summary

Properties

|  |
| --- |
| [Axes](#Axes):[Axes](/docs/reference/engine/datatypes/Axes) |

Events

|  |
| --- |
| [MouseButton1Down](#MouseButton1Down)(axis: [Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton1Up](#MouseButton1Up)(axis: [Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseDrag](#MouseDrag)(axis: [Enum.Axis](/docs/reference/engine/enums/Axis),relativeAngle: [number](/docs/luau/numbers),deltaRadius: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseEnter](#MouseEnter)(axis: [Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseLeave](#MouseLeave)(axis: [Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

1 inherited from [PartAdornment](/docs/reference/engine/classes/PartAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The ArcHandles object places 3D arc handles around any 3D object that its
[Adornee](/docs/reference/engine/classes/PartAdornment#Adornee) is set to. For handles to be
interactive, it must be parented to a player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) or the
[CoreGui](/docs/reference/engine/classes/CoreGui).

![ArcHandles example](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/ArcHandles/ArcHandles-Example.jpg)

---

API Reference

Properties

Axes

Read Parallel

Sets the current Axes ArcHandles will show.

ArcHandles.Axes:[Axes](/docs/reference/engine/datatypes/Axes)

Sets the current Axes ArcHandles will show.

Provide feedback

---

Events

MouseButton1Down

Fired when the left mouse button goes down on one of the GUI handles.

ArcHandles.MouseButton1Down(axis:[Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| axis:[Enum.Axis](/docs/reference/engine/enums/Axis) |

Fired when the left mouse button goes down on one of the GUI handles.

Provide feedback

---

MouseButton1Up

Fired when the left mouse button is released on one of the GUI handles.

ArcHandles.MouseButton1Up(axis:[Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| axis:[Enum.Axis](/docs/reference/engine/enums/Axis) |

Fired when the left mouse button is released on one of the GUI handles.

Provide feedback

---

MouseDrag

Fired when the mouse moves while the MouseButton1Down event has fired, but
the left mouse button has not been released yet.

ArcHandles.MouseDrag(

axis:[Enum.Axis](/docs/reference/engine/enums/Axis), relativeAngle:[number](/docs/luau/numbers), deltaRadius:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| axis:[Enum.Axis](/docs/reference/engine/enums/Axis) |
| relativeAngle:[number](/docs/luau/numbers) |
| deltaRadius:[number](/docs/luau/numbers) |

Fired when the mouse moves while the MouseButton1Down event has fired, but
the left mouse button has not been released yet.

Provide feedback

---

MouseEnter

Fired when a mouse "enters" the GUI handle.

ArcHandles.MouseEnter(axis:[Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| axis:[Enum.Axis](/docs/reference/engine/enums/Axis) |

Fired when a mouse "enters" the GUI handle.

Provide feedback

---

MouseLeave

Fired when the mouse leaves the GUI handle.

ArcHandles.MouseLeave(axis:[Enum.Axis](/docs/reference/engine/enums/Axis)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| axis:[Enum.Axis](/docs/reference/engine/enums/Axis) |

Fired when the mouse leaves the GUI handle.

Provide feedback

---