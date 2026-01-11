# Handles | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Handles
Scraped: 2026-01-11T02:34:24.769544Z

## Inherits
- HandlesBase
- Handles
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
7. [Handles](/docs/reference/engine/classes/Handles)

English

Feedback

Engine Class

![Handles](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Handles-Dark.webp)Handles

Places 3D handles around any object that its [Adornee](/docs/reference/engine/classes/Handles#Adornee)
is set to.

---

Summary

Properties

|  |
| --- |
| [Faces](#Faces):[Faces](/docs/reference/engine/datatypes/Faces) |
| [Style](#Style):[Enum.HandlesStyle](/docs/reference/engine/enums/HandlesStyle) |

Events

|  |
| --- |
| [MouseButton1Down](#MouseButton1Down)(face: [Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton1Up](#MouseButton1Up)(face: [Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseDrag](#MouseDrag)(face: [Enum.NormalId](/docs/reference/engine/enums/NormalId),distance: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseEnter](#MouseEnter)(face: [Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseLeave](#MouseLeave)(face: [Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

1 inherited from [PartAdornment](/docs/reference/engine/classes/PartAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Handles object places 3D handles around any object that its
[Adornee](/docs/reference/engine/classes/Handles#Adornee) is set to; this property must be set to a 3D
object for the handles to appear. The color can be changed and the shape of
the handles can be set to either arrows or spheres.

For handles to be interactive, they must be parented to a player's
[PlayerGui](/docs/reference/engine/classes/PlayerGui) or the [CoreGui](/docs/reference/engine/classes/CoreGui).

---

API Reference

Properties

Faces

Read Parallel

Sets which sides the GUI handles will appear.

Handles.Faces:[Faces](/docs/reference/engine/datatypes/Faces)

Sets which sides the GUI handles will appear.

Provide feedback

---

Style

Read Parallel

Sets the GUI style of the handles.

Handles.Style:[Enum.HandlesStyle](/docs/reference/engine/enums/HandlesStyle)

Sets the GUI style of the handles. Currently there are only two types:
[Resize](/docs/reference/engine/enums/HandlesStyle) and [Movement](/docs/reference/engine/enums/HandlesStyle).

Provide feedback

---

Events

MouseButton1Down

Fired when the left mouse button goes down on one of the GUI handles.

Handles.MouseButton1Down(face:[Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| face:[Enum.NormalId](/docs/reference/engine/enums/NormalId) |

Fired when the left mouse button goes down on one of the GUI handles.

Provide feedback

---

MouseButton1Up

Fired when the left mouse button is released on one of the GUI handles.

Handles.MouseButton1Up(face:[Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| face:[Enum.NormalId](/docs/reference/engine/enums/NormalId) |

Fired when the left mouse button is released on one of the GUI handles.

Provide feedback

---

MouseDrag

Fired when the mouse moves while the MouseButton1Down event has fired, but
the left mouse button has not been released yet.

Handles.MouseDrag(

face:[Enum.NormalId](/docs/reference/engine/enums/NormalId), distance:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| face:[Enum.NormalId](/docs/reference/engine/enums/NormalId) |
| distance:[number](/docs/luau/numbers) |

Fired when the mouse moves while the MouseButton1Down event has fired, but
the left mouse button has not been released yet.

Provide feedback

---

MouseEnter

Fired when a mouse "enters" the GUI handle.

Handles.MouseEnter(face:[Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| face:[Enum.NormalId](/docs/reference/engine/enums/NormalId) |

Fired when a mouse "enters" the GUI handle.

Provide feedback

---

MouseLeave

Fired when the mouse leaves the GUI handle.

Handles.MouseLeave(face:[Enum.NormalId](/docs/reference/engine/enums/NormalId)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| face:[Enum.NormalId](/docs/reference/engine/enums/NormalId) |

Fired when the mouse leaves the GUI handle.

Provide feedback

---