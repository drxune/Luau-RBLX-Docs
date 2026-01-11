# SurfaceGuiBase | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SurfaceGuiBase
Scraped: 2026-01-11T02:28:40.853759Z

## Tags
- Not Creatable

## Inherits
- LayerCollector
- SurfaceGuiBase
- GuiBase2d
- Instance
- Object
- AdGui
- SurfaceGui
- Adornee
- ClickDetector
- DragDetector
- ImageButtons
- TextButtons
- PlayerGui
- SurfaceGui.Adorneee
- CanQuery
- BasePart
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [LayerCollector](/docs/reference/engine/classes/LayerCollector)
6. /
7. [SurfaceGuiBase](/docs/reference/engine/classes/SurfaceGuiBase)

English

Feedback

Engine Class

SurfaceGuiBase

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Active](#Active):[boolean](/docs/luau/booleans) |
| [Adornee](#Adornee):[Instance](/docs/reference/engine/datatypes/Instance) |
| [Face](#Face):[Enum.NormalId](/docs/reference/engine/enums/NormalId) |

Inherited Members

4 inherited from [LayerCollector](/docs/reference/engine/classes/LayerCollector)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[AdGui](/docs/reference/engine/classes/AdGui), [SurfaceGui](/docs/reference/engine/classes/SurfaceGui)

---

API Reference

Properties

Active

Read Parallel

SurfaceGuiBase.Active:[boolean](/docs/luau/booleans)

This property determines whether the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) will sink input,
for example if the parent or [Adornee](/docs/reference/engine/classes/SurfaceGuiBase#Adornee) part
contains a [ClickDetector](/docs/reference/engine/classes/ClickDetector) class like [DragDetector](/docs/reference/engine/classes/DragDetector).

Note that interactive UI elements like [ImageButtons](/docs/reference/engine/classes/ImageButton)
and [TextButtons](/docs/reference/engine/classes/TextButton) inside a [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) will only
receive user input if they are parented to the [PlayerGui](/docs/reference/engine/classes/PlayerGui) (the
[SurfaceGui.Adorneee](/docs/reference/engine/classes/SurfaceGui#Adorneee) property can be used to target a part in the
3D world while the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) itself remains in the
[PlayerGui](/docs/reference/engine/classes/PlayerGui)). Additionally, the part's
[CanQuery](/docs/reference/engine/classes/BasePart#CanQuery) property must be true for the
interactive UI element to receive input.

Provide feedback

---

Adornee

Read Parallel

[BasePart](/docs/reference/engine/classes/BasePart) on which to apply the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui), overriding the
default parent association.

SurfaceGuiBase.Adornee:[Instance](/docs/reference/engine/datatypes/Instance)

[BasePart](/docs/reference/engine/classes/BasePart) on which to apply the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui), overriding the
default parent association.

Provide feedback

---

Face

Read Parallel

[Enum.NormalId](/docs/reference/engine/enums/NormalId) face upon which to apply the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui).

SurfaceGuiBase.Face:[Enum.NormalId](/docs/reference/engine/enums/NormalId)

[Enum.NormalId](/docs/reference/engine/enums/NormalId) face of the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) parent (or its
[Adornee](/docs/reference/engine/classes/SurfaceGuiBase#Adornee)) upon which to apply the
[SurfaceGui](/docs/reference/engine/classes/SurfaceGui).

Provide feedback

---