# ShirtGraphic | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ShirtGraphic
Scraped: 2026-01-11T02:27:35.050776Z

## Inherits
- CharacterAppearance
- ShirtGraphic
- Instance
- Object
- ImageLabel.ImageColor3
- Clothing.Color3
- Clothing
- InsertService:LoadAsset()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [CharacterAppearance](/docs/reference/engine/classes/CharacterAppearance)
6. /
7. [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic)

English

Feedback

Engine Class

![ShirtGraphic](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ShirtGraphic-Dark.webp)ShirtGraphic

Applies a texture to the front surface of a character's torso, used to display
t-shirts.

---

Summary

Properties

|  |
| --- |
| [Color3](#Color3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Graphic](#Graphic):ContentId |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The ShirtGraphic object applies a texture to the front surface of a
character's torso. It is used to display t-shirts.

---

API Reference

Properties

Color3

Read Parallel

Determines the colorization to be applied to the [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic)
texture.

ShirtGraphic.Color3:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines the colorization to be applied to the
[ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic) texture. It functions similarly to
[ImageLabel.ImageColor3](/docs/reference/engine/classes/ImageLabel#ImageColor3) except that it is applied to
[ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic) textures. This is useful for creating shirt graphics
that have many different color variations but share the same basic look.

See also:

* [Clothing.Color3](/docs/reference/engine/classes/Clothing#Color3) which determines the colorization to be applied
  to the [Clothing](/docs/reference/engine/classes/Clothing) texture

Provide feedback

---

Graphic

Read Parallel

The content ID link pointing to the [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic) texture hosted on
the Roblox website. This property sets the texture associated with a
t-shirt.

ShirtGraphic.Graphic:ContentId

The content ID link pointing to the [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic) texture hosted on
the Roblox website. This property sets the texture associated with a
t-shirt.

#### Finding the ID

This content ID is different than the website URL of the t-shirt. It can
be found by pasting the website URL of the t-shirt into the Graphic
property of the [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic) in Roblox Studio, as Studio will
correct it. Alternatively [InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) can be used to
insert the t-shirt into the workspace, for example:

```
local InsertService = game:GetService("InsertService")



local Workspace = game:GetService("Workspace")



local webURL = "https://www.roblox.com/catalog/2591161/Sword-Fight-on-the-Heights-Ring-of-Fire-T-Shirt"



local assetId = tonumber(string.match(webURL, "%d+") or 0)  -- Extract the number



local success, model = pcall(function()



return InsertService:LoadAsset(assetId)



end)



if success then



model.Parent = Workspace



end
```

Provide feedback

---