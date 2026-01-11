# StarterPack | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StarterPack
Scraped: 2026-01-11T02:36:20.300514Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- StarterPack
- Backpack
- LocalScripts
- StarterGear
- Tools
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StarterPack](/docs/reference/engine/classes/StarterPack)

English

Feedback

Engine Class

![StarterPack](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StarterPack-Dark.webp)StarterPack

A service-level container whose contents are copied into each player's
[Backpack](/docs/reference/engine/classes/Backpack) when the player spawns. It is generally used to hold Tools,
but is sometimes used to hold [LocalScripts](/docs/reference/engine/classes/LocalScript) to ensure that
each player gets a copy.

Not Creatable

Service

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A service-level container whose contents are copied into each player's
[Backpack](/docs/reference/engine/classes/Backpack) when the player spawns. It is generally used to hold Tools,
but is sometimes used to hold [LocalScripts](/docs/reference/engine/classes/LocalScript) to ensure that
each player gets a copy.

When a player's character spawns, the contents of the StarterPack and their
[StarterGear](/docs/reference/engine/classes/StarterGear) are copied into their [Backpack](/docs/reference/engine/classes/Backpack). Once a character
dies, the [Backpack](/docs/reference/engine/classes/Backpack) is removed and a new one is created -- populating
it using the contents of [StarterPack](/docs/reference/engine/classes/StarterPack) and [StarterGear](/docs/reference/engine/classes/StarterGear).

The StarterPack is used to determine a set of [Tools](/docs/reference/engine/classes/Tool) that *all*
players will spawn with. If a developer wants to ensure that certain
[Tools](/docs/reference/engine/classes/Tool) are available to specific players, then they will need to
parent the [Tools](/docs/reference/engine/classes/Tool) directly to the player's [Backpack](/docs/reference/engine/classes/Backpack)
instead.

Note: while normally the contents of [StarterPack](/docs/reference/engine/classes/StarterPack) are predefined, the
contents can be changed while the game is running by adding and removing
[Tools](/docs/reference/engine/classes/Tool) accordingly. These updates will pass onto a player's
backpack when they respawn and their backpacks are reloaded. Changes to the
StarterPack should be made by the server.

A tool can be added to the StarterPack using the following code.

```
Tool.Parent = game:GetService("StarterPack")
```

Code Samples

Empty StarterPack

This simple function will remove all Tools from the StarterPack, while leaving
other objects such as LocalScripts in place.

```
local StarterPack = game:GetService("StarterPack")



local function emptyStarterPack()



for _, child in pairs(StarterPack:GetChildren()) do



if child:IsA("Tool") then



child:Destroy()



end



end



end



emptyStarterPack()
```