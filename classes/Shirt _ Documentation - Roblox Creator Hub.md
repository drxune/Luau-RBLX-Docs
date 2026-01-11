# Shirt | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Shirt
Scraped: 2026-01-11T02:29:45.265654Z

## Inherits
- Clothing
- Shirt
- Humanoid
- Instance
- Object
- Pants
- ShirtTemplate
- Clothing.Color3
- Player
- Player.CharacterAppearance
- InsertService:LoadAsset()
- ShirtGraphic.Graphic
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Clothing](/docs/reference/engine/classes/Clothing)
6. /
7. [Shirt](/docs/reference/engine/classes/Shirt)

English

Feedback

Engine Class

![Shirt](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Shirt-Dark.webp)Shirt

Displays a shirt texture on a [Humanoid](/docs/reference/engine/classes/Humanoid) rig.

---

Summary

Properties

|  |
| --- |
| [ShirtTemplate](#ShirtTemplate):ContentId |

Inherited Members

1 inherited from [Clothing](/docs/reference/engine/classes/Clothing)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Shirt object displays a shirt texture from Roblox on a [Humanoid](/docs/reference/engine/classes/Humanoid)
rig. Shirts cover the torso and arms, and will take priority over a
[Pants](/docs/reference/engine/classes/Pants) on the torso. To be visible, a Shirt must be a sibling of a
[Humanoid](/docs/reference/engine/classes/Humanoid) and have its [ShirtTemplate](/docs/reference/engine/classes/Shirt#ShirtTemplate)
property set to an appropriate texture such as rbxassetid://86896487. The
shirt texture may be colorized using the [Clothing.Color3](/docs/reference/engine/classes/Clothing#Color3) property.

Shirts are automatically loaded on [Player](/docs/reference/engine/classes/Player) characters if their avatar
is wearing one.

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

ShirtTemplate

Read Parallel

Determines the texture of the [Shirt](/docs/reference/engine/classes/Shirt).

Shirt.ShirtTemplate:ContentId

The content ID link pointing to the shirt template hosted on Roblox.

This content ID is different than the website URL of the shirt. It can be
found by pasting the website URL of the shirt into the ShirtTemplate
property in Studio. Alternatively, [InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) can
be used to insert the shirt into the workspace, for example:

```
local InsertService = game:GetService("InsertService")



local Workspace = game:GetService("Workspace")



local webURL = "https://www.roblox.com/catalog/1804747/White-Shirt"



local assetId = tonumber(string.match(webURL, "%d+") or 0)  -- Extract the number



local success, model = pcall(function()



return InsertService:LoadAsset(assetId)



end)



if success then



model.Parent = Workspace



end
```

See also [ShirtGraphic.Graphic](/docs/reference/engine/classes/ShirtGraphic#Graphic) for the image applied to T-shirts.

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