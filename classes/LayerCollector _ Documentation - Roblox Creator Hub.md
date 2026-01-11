# LayerCollector | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LayerCollector
Scraped: 2026-01-11T02:31:19.099381Z

## Tags
- Not Creatable

## Inherits
- GuiBase2d
- LayerCollector
- GuiObjects
- Instance
- Object
- BillboardGui
- PluginGui
- ScreenGui
- SurfaceGuiBase
- GuiObject
- PlayerGui
- StarterGui
- GuiObject.ZIndex
- ZIndex
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)
6. /
7. [LayerCollector](/docs/reference/engine/classes/LayerCollector)

English

Feedback

Engine Class

LayerCollector

The base class of 2D UI containers which render [GuiObjects](/docs/reference/engine/classes/GuiObject)
in layers.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [ResetOnSpawn](#ResetOnSpawn):[boolean](/docs/luau/booleans) |
| [ZIndexBehavior](#ZIndexBehavior):[Enum.ZIndexBehavior](/docs/reference/engine/enums/ZIndexBehavior) |

Methods

|  |
| --- |
| [GetLayoutNodeTree](#GetLayoutNodeTree)():[Dictionary](/docs/luau/tables#dictionaries)  Deprecated |

Inherited Members

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[BillboardGui](/docs/reference/engine/classes/BillboardGui), [PluginGui](/docs/reference/engine/classes/PluginGui), [ScreenGui](/docs/reference/engine/classes/ScreenGui), [SurfaceGuiBase](/docs/reference/engine/classes/SurfaceGuiBase)

LayerCollector is the base class of 2D UI containers which render
[GuiObject](/docs/reference/engine/classes/GuiObject) descendants, such as [ScreenGui](/docs/reference/engine/classes/ScreenGui).

For performance improvements, the appearance of a [LayerCollector](/docs/reference/engine/classes/LayerCollector) is
cached until one of the following events occurs:

* A descendant is added to or removed from it.
* A property of a descendant changes.
* A property of the [LayerCollector](/docs/reference/engine/classes/LayerCollector) itself changes.

---

API Reference

Properties

Enabled

Read Parallel

Toggles the visibility of this [LayerCollector](/docs/reference/engine/classes/LayerCollector).

LayerCollector.Enabled:[boolean](/docs/luau/booleans)

Toggles the visibility of this [LayerCollector](/docs/reference/engine/classes/LayerCollector). When false, the
UI contents will not render, process user input, or update in response to
changes.

Provide feedback

---

ResetOnSpawn

Read Parallel

Determines if the [LayerCollector](/docs/reference/engine/classes/LayerCollector) resets (deletes itself and
re-clones into the player's [PlayerGui](/docs/reference/engine/classes/PlayerGui)) every time the player's
character respawns.

LayerCollector.ResetOnSpawn:[boolean](/docs/luau/booleans)

When set to false and this [LayerCollector](/docs/reference/engine/classes/LayerCollector) is a direct child of
[StarterGui](/docs/reference/engine/classes/StarterGui), it will only be cloned into each player's
[PlayerGui](/docs/reference/engine/classes/PlayerGui) once and it will not be deleted when the player's
character respawns.

When set to true (default), or if this [LayerCollector](/docs/reference/engine/classes/LayerCollector) is an
indirect descendant of [StarterGui](/docs/reference/engine/classes/StarterGui), it will be cloned into each
player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) when their character respawns, and it will
delete itself when the player's character respawns again.

Provide feedback

---

ZIndexBehavior

Read Parallel

Controls how [GuiObject.ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) behaves on all descendants of this
[LayerCollector](/docs/reference/engine/classes/LayerCollector).

LayerCollector.ZIndexBehavior:[Enum.ZIndexBehavior](/docs/reference/engine/enums/ZIndexBehavior)

Controls how [GuiObject.ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) behaves on all descendants of this
[LayerCollector](/docs/reference/engine/classes/LayerCollector).

With [Enum.ZIndexBehavior.Sibling](/docs/reference/engine/enums/ZIndexBehavior#Sibling) (default), children always render above
their parents, and the [ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) is used to decide
the order in which children of a single UI object will render over each
other.

[Enum.ZIndexBehavior.Global](/docs/reference/engine/enums/ZIndexBehavior#Global) sorts all descendants according to the
[ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex), then breaks ties using the hierarchy
order. As a result, descendants of a [GuiObject](/docs/reference/engine/classes/GuiObject) need to have a
[ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) value that's at least as high as the
parent, or they will render underneath their parent.

Provide feedback

---

Methods

GetLayoutNodeTree

Deprecated

Show details

---