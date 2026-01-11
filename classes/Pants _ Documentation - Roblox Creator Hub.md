# Pants | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Pants
Scraped: 2026-01-11T02:35:20.252869Z

## Inherits
- Clothing
- Pants
- Humanoid
- Instance
- Object
- Shirt
- PantsTemplate
- Clothing.Color3
- Player
- Player.CharacterAppearance
- InsertService:LoadAsset()
- Shirt.ShirtTemplate
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Clothing](/docs/reference/engine/classes/Clothing)
6. /
7. [Pants](/docs/reference/engine/classes/Pants)

English

Feedback

Engine Class

![Pants](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Pants-Dark.webp)Pants

Displays a Pants texture from the Roblox website to display on a
[Humanoid](/docs/reference/engine/classes/Humanoid) rig.

---

Summary

Properties

|  |
| --- |
| [PantsTemplate](#PantsTemplate):ContentId |

Inherited Members

1 inherited from [Clothing](/docs/reference/engine/classes/Clothing)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Pants object displays a pants texture from Roblox on a [Humanoid](/docs/reference/engine/classes/Humanoid)
rig. Pants cover the torso and legs, and will be covered by a [Shirt](/docs/reference/engine/classes/Shirt) on
the torso. To be visible, a Pants must be a sibling of a [Humanoid](/docs/reference/engine/classes/Humanoid)
and have its [PantsTemplate](/docs/reference/engine/classes/Pants#PantsTemplate) property set to an
appropriate texture such as rbxassetid://86896501. The pants texture may be
colorized using the [Clothing.Color3](/docs/reference/engine/classes/Clothing#Color3) property.

Pants are automatically loaded on [Player](/docs/reference/engine/classes/Player) characters if their avatar is
wearing one.

Code Samples

Change Shirt / Pants

This sample includes a simple function to change the texture of the Shirt
and Pants worn by a player's character. If shirt and pants don't exist then
they are created. Note, this should be run every time the character spawns. If
a developer is looking to permanently change a character's appearance to a
preset it is recommended they use [Player.CharacterAppearance](/docs/reference/engine/classes/Player#CharacterAppearance).

```
local Players = game:GetService("Players")



local function replaceClothes(player)



local character = player.Character



if character then



-- look for shirts / pants



local shirt = character:FindFirstChildOfClass("Shirt")



local pants = character:FindFirstChildOfClass("Pants")



-- create shirts / pants if they don't exist



if not shirt then



shirt = Instance.new("Shirt")



shirt.Parent = character



end



if not pants then



pants = Instance.new("Pants")



pants.Parent = character



end



-- reset shirt / pants content ids



shirt.ShirtTemplate = "http://www.roblox.com/asset/?id=83326831"



pants.PantsTemplate = "http://www.roblox.com/asset/?id=10045638"



end



end



for _index, player in ipairs(Players:GetPlayers()) do



replaceClothes(player)



end
```

---

API Reference

Properties

PantsTemplate

Read Parallel

Determines the texture of the [Pants](/docs/reference/engine/classes/Pants).

Pants.PantsTemplate:ContentId

The content ID link pointing to the pants template hosted on Roblox.

This content ID is different than the website URL of the pants. It can be
found by pasting the website URL of the pants into the PantsTemplate
property in Studio. Alternatively, [InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) can
be used to insert the pants into the workspace, for example:

```
local InsertService = game:GetService("InsertService")



local Workspace = game:GetService("Workspace")



local webURL = "https://www.roblox.com/catalog/1804739/Jeans"



local assetId = tonumber(string.match(webURL, "%d+") or 0)  -- Extract the number



local success, model = pcall(function()



return InsertService:LoadAsset(assetId)



end)



if success then



model.Parent = Workspace



end
```

For a [Shirt](/docs/reference/engine/classes/Shirt) object's template, see [Shirt.ShirtTemplate](/docs/reference/engine/classes/Shirt#ShirtTemplate).

Code Samples

Change Shirt / Pants

This sample includes a simple function to change the texture of the Shirt
and Pants worn by a player's character. If shirt and pants don't exist then
they are created. Note, this should be run every time the character spawns. If
a developer is looking to permanently change a character's appearance to a
preset it is recommended they use [Player.CharacterAppearance](/docs/reference/engine/classes/Player#CharacterAppearance).

```
local Players = game:GetService("Players")



local function replaceClothes(player)



local character = player.Character



if character then



-- look for shirts / pants



local shirt = character:FindFirstChildOfClass("Shirt")



local pants = character:FindFirstChildOfClass("Pants")



-- create shirts / pants if they don't exist



if not shirt then



shirt = Instance.new("Shirt")



shirt.Parent = character



end



if not pants then



pants = Instance.new("Pants")



pants.Parent = character



end



-- reset shirt / pants content ids



shirt.ShirtTemplate = "http://www.roblox.com/asset/?id=83326831"



pants.PantsTemplate = "http://www.roblox.com/asset/?id=10045638"



end



end



for _index, player in ipairs(Players:GetPlayers()) do



replaceClothes(player)



end
```

Provide feedback

---