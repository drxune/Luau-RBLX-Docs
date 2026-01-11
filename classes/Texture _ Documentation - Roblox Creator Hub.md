# Texture | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Texture
Scraped: 2026-01-11T02:40:40.505950Z

## Inherits
- Decal
- Texture
- BasePart
- FaceInstance
- Instance
- Object
- Face
- Decals
- StudsPerTileU
- StudsPerTileV
- ColorMapContent
- MeshPart.TextureContent
- MeshPart
- SurfaceGui
- ImageLabel
- ImageButton
- OffsetStudsV
- OffsetStudsU
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Decal](/docs/reference/engine/classes/Decal)
6. /
7. [Texture](/docs/reference/engine/classes/Texture)

English

Feedback

Engine Class

![Texture](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Texture-Dark.webp)Texture

Applies a repeating image texture to the face of a parent [BasePart](/docs/reference/engine/classes/BasePart).

---

Summary

Properties

|  |
| --- |
| [OffsetStudsU](#OffsetStudsU):[number](/docs/luau/numbers) |
| [OffsetStudsV](#OffsetStudsV):[number](/docs/luau/numbers) |
| [StudsPerTileU](#StudsPerTileU):[number](/docs/luau/numbers) |
| [StudsPerTileV](#StudsPerTileV):[number](/docs/luau/numbers) |

Inherited Members

19 inherited from [Decal](/docs/reference/engine/classes/Decal)

1 inherited from [FaceInstance](/docs/reference/engine/classes/FaceInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [Texture](/docs/reference/engine/classes/Texture) object applies a repeating image texture to the face of a
parent [BasePart](/docs/reference/engine/classes/BasePart). The affected face is dependent on the
[Face](/docs/reference/engine/classes/Texture#Face) property. Unlike [Decals](/docs/reference/engine/classes/Decal), the texture
applied by a [Texture](/docs/reference/engine/classes/Texture) will repeat when the parent [BasePart](/docs/reference/engine/classes/BasePart) is
resized, with the size of the repeating textures determined by the
[StudsPerTileU](/docs/reference/engine/classes/Texture#StudsPerTileU) and
[StudsPerTileV](/docs/reference/engine/classes/Texture#StudsPerTileV) properties.

The applied image texture is determined by its
[ColorMapContent](/docs/reference/engine/classes/Texture#ColorMapContent) property. For details on how
to upload images, see
[asset management](/docs/projects/assets#asset-management).

For more information, review
[textures and decals](/docs/parts/textures-decals). See also:

* [Decal](/docs/reference/engine/classes/Decal) for non-repeating surface images.
* [MeshPart.TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) to apply an image texture to a
  [MeshPart](/docs/reference/engine/classes/MeshPart).
* [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) to apply an [ImageLabel](/docs/reference/engine/classes/ImageLabel) or [ImageButton](/docs/reference/engine/classes/ImageButton) to
  an in-experience 3D object.

---

API Reference

Properties

OffsetStudsU

Read Parallel

Determines the offset in studs of the rendered texture's horizontal
coordinate.

Texture.OffsetStudsU:[number](/docs/luau/numbers)

This property determines how far the rendered texture is offset on the
horizontal axis, in studs, as visualized
[here](/docs/parts/textures-decals#offset-textures).

See also [OffsetStudsV](/docs/reference/engine/classes/Texture#OffsetStudsV).

Provide feedback

---

OffsetStudsV

Read Parallel

Determines the offset in studs of the rendered texture's vertical
coordinate.

Texture.OffsetStudsV:[number](/docs/luau/numbers)

This property determines how far the rendered texture is offset on the
vertical axis, in studs, as visualized
[here](/docs/parts/textures-decals#offset-textures).

See also [OffsetStudsU](/docs/reference/engine/classes/Texture#OffsetStudsU).

Provide feedback

---

StudsPerTileU

Read Parallel

Sets the horizontal size, in studs, of the tiled image applied by the
[Texture](/docs/reference/engine/classes/Texture).

Texture.StudsPerTileU:[number](/docs/luau/numbers)

Sets the horizontal size, in studs, of the tiled image applied by the
[Texture](/docs/reference/engine/classes/Texture).

Larger values for this property will lead to the [Texture](/docs/reference/engine/classes/Texture) appearing
larger, and repeating less frequently. Unlike with [Decals](/docs/reference/engine/classes/Decal),
the size of the repeated image is unaffected by the dimensions of the
[BasePart](/docs/reference/engine/classes/BasePart). Instead, resizing the [BasePart](/docs/reference/engine/classes/BasePart) only increases
the number of times the texture repeats.

Note that this property can be set to very low values, but not zero. Also
note that the horizontal/vertical distinction is relative to the parent
[BasePart](/docs/reference/engine/classes/BasePart) axis; therefore the [Texture](/docs/reference/engine/classes/Texture) will rotate along
with the [BasePart](/docs/reference/engine/classes/BasePart).

See also [StudsPerTileV](/docs/reference/engine/classes/Texture#StudsPerTileV).

Provide feedback

---

StudsPerTileV

Read Parallel

Sets the vertical size, in studs, of the tiled image applied by the
[Texture](/docs/reference/engine/classes/Texture).

Texture.StudsPerTileV:[number](/docs/luau/numbers)

Sets the vertical size, in studs, of the tiled image applied by the
[Texture](/docs/reference/engine/classes/Texture).

Larger values for this property will lead to the [Texture](/docs/reference/engine/classes/Texture) appearing
larger, and repeating less frequently. Unlike with [Decals](/docs/reference/engine/classes/Decal),
the size of the repeated image is unaffected by the dimensions of the
[BasePart](/docs/reference/engine/classes/BasePart). Instead, resizing the [BasePart](/docs/reference/engine/classes/BasePart) only increases
the number of times the texture repeats.

Note that this property can be set to very low values, but not zero. Also
note that the horizontal/vertical distinction is relative to the parent
[BasePart](/docs/reference/engine/classes/BasePart) axis; therefore the [Texture](/docs/reference/engine/classes/Texture) will rotate along
with the [BasePart](/docs/reference/engine/classes/BasePart).

See also [StudsPerTileU](/docs/reference/engine/classes/Texture#StudsPerTileU).

Provide feedback

---