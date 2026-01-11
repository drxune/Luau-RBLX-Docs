# PlayerGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PlayerGui
Scraped: 2026-01-11T02:33:16.572426Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- BasePlayerGui
- PlayerGui
- ScreenGuis
- GuiObject
- Instance
- Object
- ScreenGui
- LocalScript
- Player
- Player.Character
- StarterGui
- Players.CharacterAutoLoads
- Player:LoadCharacter()
- StarterGui.ResetPlayerGuiOnSpawn
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui)
6. /
7. [PlayerGui](/docs/reference/engine/classes/PlayerGui)

English

Feedback

Engine Class

PlayerGui

A container for a player's currently rendered [ScreenGuis](/docs/reference/engine/classes/ScreenGui).

Not Creatable

Player Replicated

---

Summary

Properties

|  |
| --- |
| [CurrentScreenOrientation](#CurrentScreenOrientation):[Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation) |
| [ScreenOrientation](#ScreenOrientation):[Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation) |
| [SelectionImageObject](#SelectionImageObject):[GuiObject](/docs/reference/engine/classes/GuiObject) |

Methods

|  |
| --- |
| [GetTopbarTransparency](#GetTopbarTransparency)():[number](/docs/luau/numbers)  Deprecated |
| [SetTopbarTransparency](#SetTopbarTransparency)(transparency: [number](/docs/luau/numbers)):()  Deprecated |

Events

|  |
| --- |
| [TopbarTransparencyChangedSignal](#TopbarTransparencyChangedSignal)(transparency: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

1 inherited from [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[PlayerGui](/docs/reference/engine/classes/PlayerGui) is a container that holds a player's UI. If a
[ScreenGui](/docs/reference/engine/classes/ScreenGui) is a descendant, then any [GuiObject](/docs/reference/engine/classes/GuiObject) inside of the
[ScreenGui](/docs/reference/engine/classes/ScreenGui) will be drawn to the player's screen. Any
[LocalScript](/docs/reference/engine/classes/LocalScript) will also run if it is inserted into a [PlayerGui](/docs/reference/engine/classes/PlayerGui).

When a player first joins the experience, their [PlayerGui](/docs/reference/engine/classes/PlayerGui) is
automatically inserted into their [Player](/docs/reference/engine/classes/Player) object. When the player's
[Player.Character](/docs/reference/engine/classes/Player#Character) spawns for the first time, all of the contents of
[StarterGui](/docs/reference/engine/classes/StarterGui) are automatically copied into the player's
[PlayerGui](/docs/reference/engine/classes/PlayerGui). Note that if [Players.CharacterAutoLoads](/docs/reference/engine/classes/Players#CharacterAutoLoads) is set to
false, the character will not spawn and [StarterGui](/docs/reference/engine/classes/StarterGui) contents will not
be copied until [Player:LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter) is called. If
[StarterGui.ResetPlayerGuiOnSpawn](/docs/reference/engine/classes/StarterGui#ResetPlayerGuiOnSpawn) is set to true, then every time the
player's character respawns, all of the contents of that player's
[PlayerGui](/docs/reference/engine/classes/PlayerGui) are cleared and replaced with the contents of
[StarterGui](/docs/reference/engine/classes/StarterGui).

If you need to control a player's UI container during playtime, for example to
show/hide a specific [ScreenGui](/docs/reference/engine/classes/ScreenGui) or any of its children, access it as
follows from a [LocalScript](/docs/reference/engine/classes/LocalScript):

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local playerGui = player.PlayerGui
```

---

API Reference

Properties

CurrentScreenOrientation

Read Only

Not Replicated

Read Parallel

Describes the player's current screen orientation.

PlayerGui.CurrentScreenOrientation:[Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation)

Describes the player's current screen orientation.

Provide feedback

---

ScreenOrientation

Read Parallel

Sets the preferred screen orientation mode for this player, if on a mobile
device.

PlayerGui.ScreenOrientation:[Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation)

Sets the preferred screen orientation mode for this player, if on a mobile
device.

Provide feedback

---

SelectionImageObject

Read Parallel

Overrides the default selection adornment used for gamepads.

PlayerGui.SelectionImageObject:[GuiObject](/docs/reference/engine/classes/GuiObject)

Overrides the default selection adornment used for gamepads. For best
results, this should point to a [GuiObject](/docs/reference/engine/classes/GuiObject).

Provide feedback

---

Methods

GetTopbarTransparency

Deprecated

Show details

---

SetTopbarTransparency

Deprecated

Show details

---

Events

TopbarTransparencyChangedSignal

Deprecated

Show details

---