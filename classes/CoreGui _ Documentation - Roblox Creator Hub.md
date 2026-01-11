# CoreGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CoreGui
Scraped: 2026-01-11T02:32:42.894801Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- BasePlayerGui
- CoreGui
- Plugins
- GuiObject
- Instance
- Object
- StarterGui:SetCoreGuiEnabled()
- StarterGui:GetCoreGuiEnabled()
- LocalScript
- PlayerGui:SetTopbarTransparency()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui)
6. /
7. [CoreGui](/docs/reference/engine/classes/CoreGui)

English

Feedback

Engine Class

![CoreGui](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/CoreGui-Dark.webp)CoreGui

The CoreGui is a service used to store Guis created in-game by Roblox for the
core user interface found in every game (such as the game menu, the
playerlist, the backpack, etc.). It can also be used by [Plugins](/docs/reference/engine/classes/Plugin)
in Roblox Studio.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [SelectionImageObject](#SelectionImageObject):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [Version](#Version):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The CoreGui is a service used to store Guis created in-game by Roblox for the
core user interface found in every game (such as the game menu, the
playerlist, the backpack, etc.). It can also be used by [Plugins](/docs/reference/engine/classes/Plugin)
in Roblox Studio.

You can use the [StarterGui:SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled) and
[StarterGui:GetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#GetCoreGuiEnabled) methods in a [LocalScript](/docs/reference/engine/classes/LocalScript) to
enable and disable most elements of the CoreGui. You can also use
[PlayerGui:SetTopbarTransparency()](/docs/reference/engine/classes/PlayerGui#SetTopbarTransparency) to set the transparency of the top
bar.

---

API Reference

Properties

SelectionImageObject

Roblox Script Security

Read Parallel

CoreGui.SelectionImageObject:[GuiObject](/docs/reference/engine/classes/GuiObject)

Provide feedback

---

Version

Read Only

Not Replicated

Read Parallel

The current version of the CoreGui. Every time the CoreGui is majorly
changed, this number is increased.

CoreGui.Version:[number](/docs/luau/numbers)

The current version of the CoreGui. Every time the CoreGui is majorly
changed, this number is increased.

Provide feedback

---