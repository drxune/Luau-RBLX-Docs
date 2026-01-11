# Backpack | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Backpack
Scraped: 2026-01-11T02:36:38.670388Z

## Inherits
- Object
- Instance
- Backpack
- Tool
- Tools
- Scripts
- LocalScripts
- StarterPack
- StarterGear
- StarterGui:SetCoreGuiEnabled()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Backpack](/docs/reference/engine/classes/Backpack)

English

Feedback

Engine Class

![Backpack](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Backpack-Dark.webp)Backpack

A container object that holds a player's inventory. Any [Tool](/docs/reference/engine/classes/Tool) in a
player's Backpack will be displayed in their inventory at the bottom of their
screen.

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A container object that holds a player's inventory. Any [Tool](/docs/reference/engine/classes/Tool) in a
player's Backpack will be displayed in their inventory at the bottom of their
screen. Selecting [Tools](/docs/reference/engine/classes/Tool) from the inventory will equip the
[Tool](/docs/reference/engine/classes/Tool), moving it from the Backpack to the player's character.

The Backpack can also store [Scripts](/docs/reference/engine/classes/Script) and
[LocalScripts](/docs/reference/engine/classes/LocalScript), which run when placed in a player's
Backpack.

When a player's character spawns, the contents of the [StarterPack](/docs/reference/engine/classes/StarterPack) and
their [StarterGear](/docs/reference/engine/classes/StarterGear) are copied into their Backpack. Once a character
dies, the Backpack is removed and a new one will be created -- populating it
with the contents of [StarterPack](/docs/reference/engine/classes/StarterPack) and [StarterGear](/docs/reference/engine/classes/StarterGear).

Roblox provides an interface for a player to access their backpack and
inventory by default at the bottom of the screen. If a developer wishes to
disable the default Roblox backpack GUI and replace it with their own, they
may do so using [StarterGui:SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled).

The Backpack can be accessed from both the client and the server.

```
local Players = game:GetService("Players")



-- Accessing Backpack from a Server Script:



local backpack = Players.PlayerName.Backpack



-- Accessing Backpack from a LocalScript:



local backpack = Players.LocalPlayer.Backpack
```

Code Samples

Backpack Give Tool

This sample includes a simple function demonstrating how a Tool can be given
to a Player by parenting it to their Backpack.

```
local Players = game:GetService("Players")



local function onCharacterAdded(character)



local player = Players:GetPlayerFromCharacter(character)



local tool = Instance.new("Tool")



local backpack = player:FindFirstChildOfClass("Backpack")



tool.Parent = backpack



end



local function onPlayerAdded(player)



if player.Character then



onCharacterAdded(player.Character)



end



player.CharacterAdded:Connect(onCharacterAdded)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```