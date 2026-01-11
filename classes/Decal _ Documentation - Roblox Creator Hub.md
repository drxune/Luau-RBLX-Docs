# Decal | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Decal
Scraped: 2026-01-11T02:33:17.767268Z

## Tags
- Not Replicated

## Inherits
- FaceInstance
- Decal
- BasePart
- Instance
- Object
- Texture
- Face
- ColorMapContent
- MeshPart.TextureContent
- MeshPart
- SurfaceGui
- ImageLabel
- ImageButton
- Decal.Color3
- TweenService
- Transparency
- LocalPlayer
- LocalTransparencyModifier
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [FaceInstance](/docs/reference/engine/classes/FaceInstance)
6. /
7. [Decal](/docs/reference/engine/classes/Decal)

English

Feedback

Engine Class

![Decal](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Decal-Dark.webp)Decal

Applies an image texture to a face of a parent [BasePart](/docs/reference/engine/classes/BasePart).

---

Summary

Properties

|  |
| --- |
| [Color3](#Color3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ColorMap](#ColorMap):ContentId |
| [ColorMapContent](#ColorMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [MetalnessMap](#MetalnessMap):ContentId |
| [MetalnessMapContent](#MetalnessMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [NormalMap](#NormalMap):ContentId |
| [NormalMapContent](#NormalMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [RoughnessMap](#RoughnessMap):ContentId |
| [RoughnessMapContent](#RoughnessMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [Shiny](#Shiny):[number](/docs/luau/numbers)  Deprecated |
| [Specular](#Specular):[number](/docs/luau/numbers)  Deprecated |
| [Texture](#Texture):ContentId  Deprecated |
| [TextureContent](#TextureContent):[Content](/docs/reference/engine/datatypes/Content)  Deprecated |
| [TexturePack](#TexturePack):ContentId |
| [Transparency](#Transparency):[number](/docs/luau/numbers) |
| [UVOffset](#UVOffset):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [UVScale](#UVScale):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [ZIndex](#ZIndex):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [FaceInstance](/docs/reference/engine/classes/FaceInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Texture](/docs/reference/engine/classes/Texture)

The [Decal](/docs/reference/engine/classes/Decal) object applies an image texture to a face of a parent
[BasePart](/docs/reference/engine/classes/BasePart). The affected face is dependent on the
[Face](/docs/reference/engine/classes/Decal#Face) property, and the size of the decal is dependent on
the size of the face.

The applied image texture is determined by its
[ColorMapContent](/docs/reference/engine/classes/Decal#ColorMapContent) property. For details on how to
upload images, see
[asset management](/docs/projects/assets#asset-management).

For more information, review
[textures and decals](/docs/parts/textures-decals). See also:

* [Texture](/docs/reference/engine/classes/Texture) for repeating surface images.
* [MeshPart.TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) to apply an image texture to a
  [MeshPart](/docs/reference/engine/classes/MeshPart).
* [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) to apply an [ImageLabel](/docs/reference/engine/classes/ImageLabel) or [ImageButton](/docs/reference/engine/classes/ImageButton) to
  an in-experience 3D object.

---

API Reference

Properties

Color3

Read Parallel

The [Color3](/docs/reference/engine/datatypes/Color3) tint of the [Decal](/docs/reference/engine/classes/Decal).

Decal.Color3:[Color3](/docs/reference/engine/datatypes/Color3)

The [Color3](/docs/reference/engine/datatypes/Color3) tint of the [Decal](/docs/reference/engine/classes/Decal). Note that this property
only sets the tint of the decal rather than the color; unless the
image associated with the [Decal](/docs/reference/engine/classes/Decal) was originally pure white, then
the color cannot be freely changed using this property.

Code Samples

Decal Color3

This code sample creates a Decal in the workspace and changes its
[Decal.Color3](/docs/reference/engine/classes/Decal#Color3) property on a loop using [TweenService](/docs/reference/engine/classes/TweenService).

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Size = Vector3.new(10, 10, 1)



part.Position = Vector3.new(0, 5, 0)



part.Anchored = true



part.Transparency = 1



local decal = Instance.new("Decal")



decal.Face = Enum.NormalId.Front



decal.ColorMapContent = "http://www.roblox.com/asset/?id=1145367640"



decal.Parent = part



part.Parent = workspace



local redTween = TweenService:Create(



decal,



TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out),



{ Color3 = Color3.new(1, 0, 0) }



)



local greenTween = TweenService:Create(



decal,



TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out),



{ Color3 = Color3.new(0, 1, 0) }



)



local blueTween = TweenService:Create(



decal,



TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out),



{ Color3 = Color3.new(0, 0, 1) }



)



while true do



redTween:Play()



redTween.Completed:Wait()



greenTween:Play()



greenTween.Completed:Wait()



blueTween:Play()



blueTween.Completed:Wait()



end
```

Provide feedback

---

ColorMap

Not Replicated

Read Parallel

Content ID that determines the color and opacity of the surface.

Decal.ColorMap:ContentId

This property takes a content ID to determine the color and opacity of the
surface. This texture is sometimes called the albedo texture.

Provide feedback

---

ColorMapContent

Not Replicated

Read Parallel

[Content](/docs/reference/engine/datatypes/Content) object that determines the color and opacity of the
surface.

Decal.ColorMapContent:[Content](/docs/reference/engine/datatypes/Content)

This property takes a [Content](/docs/reference/engine/datatypes/Content) object to determine the color and
opacity of the surface. This texture is sometimes called the albedo
texture.

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

Acts as a multiplier for the decal's
[Transparency](/docs/reference/engine/classes/Decal#Transparency) property. The effects are only
visible to the local player.

Decal.LocalTransparencyModifier:[number](/docs/luau/numbers)

Acts as a multiplier for the decal's
[Transparency](/docs/reference/engine/classes/Decal#Transparency) property. The effect is only
visible to the [LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) and will not
replicate to the server.

When this property is set to 1, the [Decal](/docs/reference/engine/classes/Decal) will be completely
invisible regardless of its original transparency. When it is set to 0,
the decal's rendered transparency will match the
[Transparency](/docs/reference/engine/classes/Decal#Transparency) value.

Provide feedback

---

MetalnessMap

Hidden

Plugin Security

Read Parallel

Decal.MetalnessMap:ContentId

Provide feedback

---

MetalnessMapContent

Plugin Security

Read Parallel

Decal.MetalnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

NormalMap

Hidden

Plugin Security

Read Parallel

Decal.NormalMap:ContentId

Provide feedback

---

NormalMapContent

Plugin Security

Read Parallel

Decal.NormalMapContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

RoughnessMap

Hidden

Plugin Security

Read Parallel

Decal.RoughnessMap:ContentId

Provide feedback

---

RoughnessMapContent

Plugin Security

Read Parallel

Decal.RoughnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

Shiny

Deprecated

Show details

---

Specular

Deprecated

Show details

---

Texture

Deprecated

Show details

---

TextureContent

Deprecated

Show details

---

TexturePack

Roblox Security

Read Parallel

Decal.TexturePack:ContentId

Provide feedback

---

Transparency

Read Parallel

Determines the transparency of the [Decal](/docs/reference/engine/classes/Decal).

Decal.Transparency:[number](/docs/luau/numbers)

Determines the transparency of the [Decal](/docs/reference/engine/classes/Decal) with 0 being completely
opaque and 1 completely transparent.

Note that
[LocalTransparencyModifier](/docs/reference/engine/classes/Decal#LocalTransparencyModifier) acts as
a multiplier for this transparency level and should be used when the
transparency of the decal is likely to be changed by another script.

Provide feedback

---

UVOffset

Read Parallel

Shifts the UV coordinates by adding an offset before texture mapping.

Decal.UVOffset:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property controls the UV coordinate translation. The
[X](/docs/reference/engine/datatypes/Vector2#X) value (U offset) and
[Y](/docs/reference/engine/datatypes/Vector2#Y) value (V offset) are added to every
corresponding UV coordinate during texture mapping.

Provide feedback

---

UVScale

Read Parallel

Stretches or compresses the UV coordinates by multiplying a scale factor.

Decal.UVScale:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property controls the scale applied to the horizontal and vertical
coordinates. The [X](/docs/reference/engine/datatypes/Vector2#X) value (U scale) and
[Y](/docs/reference/engine/datatypes/Vector2#Y) value (V scale) are multiplied by every
corresponding UV coordinate during texture mapping.

Provide feedback

---

ZIndex

Read Parallel

Determines the rendering order when multiple decals are assigned the same
face.

Decal.ZIndex:[number](/docs/luau/numbers)

This property determines the order in which decals on the same
[Face](/docs/reference/engine/classes/Decal#Face) of a [BasePart](/docs/reference/engine/classes/BasePart) are rendered. Lower values
are rendered first, so a decal with a higher ZIndex renders on top of
those with a lower ZIndex.

If you're unsure whether you'll need to layer a decal between two
already-existing decals in the future, use larger separations between
ZIndex values such as 10 or 100 to ensure space for future decals
between.

Provide feedback

---