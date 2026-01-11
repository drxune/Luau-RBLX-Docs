# ImageButton | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ImageButton
Scraped: 2026-01-11T02:34:49.392820Z

## Tags
- Not Replicated

## Inherits
- GuiButton
- ImageButton
- GuiObject
- GuiBase2d
- Instance
- Object
- ImageLabel
- ImageContent
- Decal.Texture
- ImageColor3
- ScaleType
- EditableImage
- ImageRectSize
- ImageRectOffset
- GuiObject.BackgroundTransparency
- BasePart.Transparency
- ImageTransparency
- TextButton
- Image
- TileSize
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiButton](/docs/reference/engine/classes/GuiButton)
6. /
7. [ImageButton](/docs/reference/engine/classes/ImageButton)

English

Feedback

Engine Class

![ImageButton](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ImageButton-Dark.webp)ImageButton

A 2D user interface element that displays an interactive image.

---

Summary

Properties

|  |
| --- |
| [HoverImage](#HoverImage):ContentId |
| [HoverImageContent](#HoverImageContent):[Content](/docs/reference/engine/datatypes/Content) |
| [Image](#Image):ContentId |
| [ImageColor3](#ImageColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ImageContent](#ImageContent):[Content](/docs/reference/engine/datatypes/Content) |
| [ImageRectOffset](#ImageRectOffset):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [ImageRectSize](#ImageRectSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [ImageTransparency](#ImageTransparency):[number](/docs/luau/numbers) |
| [IsLoaded](#IsLoaded):[boolean](/docs/luau/booleans) |
| [PressedImage](#PressedImage):ContentId |
| [PressedImageContent](#PressedImageContent):[Content](/docs/reference/engine/datatypes/Content) |
| [ResampleMode](#ResampleMode):[Enum.ResamplerMode](/docs/reference/engine/enums/ResamplerMode) |
| [ScaleType](#ScaleType):[Enum.ScaleType](/docs/reference/engine/enums/ScaleType) |
| [SliceCenter](#SliceCenter):[Rect](/docs/reference/engine/datatypes/Rect) |
| [SliceScale](#SliceScale):[number](/docs/luau/numbers) |
| [TileSize](#TileSize):[UDim2](/docs/reference/engine/datatypes/UDim2) |

Inherited Members

14 inherited from [GuiButton](/docs/reference/engine/classes/GuiButton)

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An [ImageButton](/docs/reference/engine/classes/ImageButton) behaves similarly to an [ImageLabel](/docs/reference/engine/classes/ImageLabel) in regards
to rendering, with the additional behaviors of a [GuiButton](/docs/reference/engine/classes/GuiButton).

---

API Reference

Properties

HoverImage

Read Parallel

A texture ID that will be used when the [ImageButton](/docs/reference/engine/classes/ImageButton) is being
hovered.

ImageButton.HoverImage:ContentId

A texture ID that will be used when the [ImageButton](/docs/reference/engine/classes/ImageButton) is being
hovered.

Provide feedback

---

HoverImageContent

Read Parallel

The image content that will be used when the [ImageButton](/docs/reference/engine/classes/ImageButton) is being
hovered. Only supports asset URIs.

ImageButton.HoverImageContent:[Content](/docs/reference/engine/datatypes/Content)

An image-type Content that can be set as an [ImageButton](/docs/reference/engine/classes/ImageButton) property.
When the button is hovered, it will render this image. Only asset URIs are
supported for this property.

Provide feedback

---

Image

Read Parallel

The image content displayed by the [ImageButton](/docs/reference/engine/classes/ImageButton) element. Reads and
writes to [ImageContent](/docs/reference/engine/classes/ImageButton#ImageContent).

ImageButton.Image:ContentId

This property is a content-type property that should hold the asset ID of
a decal or image uploaded to Roblox. It functions identically to
[Decal.Texture](/docs/reference/engine/classes/Decal#Texture) with regards to loading the image from Roblox. The
rendered image will be colorized using
[ImageColor3](/docs/reference/engine/classes/ImageButton#ImageColor3).

Note that it is possible to make the image render as tiled, scaled to fit,
or 9-sliced by adjusting the [ScaleType](/docs/reference/engine/classes/ImageButton#ScaleType)
property.

Code Samples

Image Hover Lock

This code sample causes an ImageLabel/ImageButton to display a red padlock.
When the mouse is hovered, it changes to a green unlocked padlock.

```
local imageLabel = script.Parent



-- The images in this example are 64x64



imageLabel.Size = UDim2.new(0, 64, 0, 64)



local function unlock()



imageLabel.Image = "rbxassetid://284402785" -- Unlocked padlock (64x64)



imageLabel.ImageColor3 = Color3.new(0, 0.5, 0) -- Dark green



end



local function lock()



imageLabel.Image = "rbxassetid://284402752" -- Locked padlock (64x64)



imageLabel.ImageColor3 = Color3.new(0.5, 0, 0) -- Dark red



end



-- Connect events; our default state is locked



imageLabel.MouseEnter:Connect(unlock)



imageLabel.MouseLeave:Connect(lock)



lock()
```

Provide feedback

---

ImageColor3

Read Parallel

Determines how a rendered image will be colorized.

ImageButton.ImageColor3:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines how an image is colorized. When set to white, no
colorization occurs. This property is very useful for reusing image
assets: If the source image is completely white with transparency, you can
set the entire color of the image at once with this property.

Code Samples

Image Hover Lock

This code sample causes an ImageLabel/ImageButton to display a red padlock.
When the mouse is hovered, it changes to a green unlocked padlock.

```
local imageLabel = script.Parent



-- The images in this example are 64x64



imageLabel.Size = UDim2.new(0, 64, 0, 64)



local function unlock()



imageLabel.Image = "rbxassetid://284402785" -- Unlocked padlock (64x64)



imageLabel.ImageColor3 = Color3.new(0, 0.5, 0) -- Dark green



end



local function lock()



imageLabel.Image = "rbxassetid://284402752" -- Locked padlock (64x64)



imageLabel.ImageColor3 = Color3.new(0.5, 0, 0) -- Dark red



end



-- Connect events; our default state is locked



imageLabel.MouseEnter:Connect(unlock)



imageLabel.MouseLeave:Connect(lock)



lock()
```

Provide feedback

---

ImageContent

Read Parallel

The image content displayed by the UI element. Supports asset URIs and
[EditableImage](/docs/reference/engine/classes/EditableImage) objects.

ImageButton.ImageContent:[Content](/docs/reference/engine/datatypes/Content)

This property should hold an
[asset URI](/docs/projects/assets#asset-uris) or a reference
to an [EditableImage](/docs/reference/engine/classes/EditableImage) object. The asset URI can reference a decal or
image uploaded to Roblox. It functions identically to
[Decal.Texture](/docs/reference/engine/classes/Decal#Texture) with regards to loading the image.

The rendered image will be colorized using
[ImageColor3](/docs/reference/engine/classes/ImageButton#ImageColor3). It is possible to make the
image render as tiled, scaled to fit, or 9‑sliced by adjusting the
[ScaleType](/docs/reference/engine/classes/ImageButton#ScaleType) property.

Provide feedback

---

ImageRectOffset

Read Parallel

The offset in pixels of the sub-area of an image to be displayed.

ImageButton.ImageRectOffset:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property determines the pixel offset (from the top-left) of the image
area to be displayed, allowing for the partial display of an image in
conjunction with [ImageRectSize](/docs/reference/engine/classes/ImageButton#ImageRectSize).

Code Samples

Image Animation using Spritesheet

This code sample uses ImageRectOffset/ImageRectSize in order to play an
animation of a man throwing a punch

```
-- Place this in an ImageLabel/ImageButton with size 256x256



local imageLabel = script.Parent



-- The following image is 1024x1024 with 12 frames (256x256)



-- The frames play an animation of a man throwing a punch



imageLabel.Image = "rbxassetid://848623155"



imageLabel.ImageRectSize = Vector2.new(256, 256)



-- The order of the frames to be displayed (left-to-right, then top-to-bottom)



local frames = {



Vector2.new(0, 0),



Vector2.new(1, 0),



Vector2.new(2, 0),



Vector2.new(3, 0),



Vector2.new(0, 1),



Vector2.new(1, 1),



Vector2.new(2, 1),



Vector2.new(3, 1),



Vector2.new(0, 2),



Vector2.new(1, 2),



Vector2.new(2, 2),



Vector2.new(3, 2),



}



-- Animate the frames one at a time in a loop



while true do



for _, frame in ipairs(frames) do



imageLabel.ImageRectOffset = frame * imageLabel.ImageRectSize



task.wait(0.1)



end



end
```

Provide feedback

---

ImageRectSize

Read Parallel

Determines the size in pixels of the sub-area of an image to be displayed.

ImageButton.ImageRectSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property determines the pixel size of the image area to be displayed,
allowing for the partial display of an image in conjunction with
[ImageRectOffset](/docs/reference/engine/classes/ImageButton#ImageRectOffset). If either dimension
is set to 0, the entire image is displayed instead.

Code Samples

Image Animation using Spritesheet

This code sample uses ImageRectOffset/ImageRectSize in order to play an
animation of a man throwing a punch

```
-- Place this in an ImageLabel/ImageButton with size 256x256



local imageLabel = script.Parent



-- The following image is 1024x1024 with 12 frames (256x256)



-- The frames play an animation of a man throwing a punch



imageLabel.Image = "rbxassetid://848623155"



imageLabel.ImageRectSize = Vector2.new(256, 256)



-- The order of the frames to be displayed (left-to-right, then top-to-bottom)



local frames = {



Vector2.new(0, 0),



Vector2.new(1, 0),



Vector2.new(2, 0),



Vector2.new(3, 0),



Vector2.new(0, 1),



Vector2.new(1, 1),



Vector2.new(2, 1),



Vector2.new(3, 1),



Vector2.new(0, 2),



Vector2.new(1, 2),



Vector2.new(2, 2),



Vector2.new(3, 2),



}



-- Animate the frames one at a time in a loop



while true do



for _, frame in ipairs(frames) do



imageLabel.ImageRectOffset = frame * imageLabel.ImageRectSize



task.wait(0.1)



end



end
```

Provide feedback

---

ImageTransparency

Read Parallel

Determines the transparency of the rendered image.

ImageButton.ImageTransparency:[number](/docs/luau/numbers)

This property determines the alpha of the element's rendered image. A
value of 0 is completely opaque and a value of 1 is completely
transparent (invisible). This property behaves similarly to
[GuiObject.BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency) or [BasePart.Transparency](/docs/reference/engine/classes/BasePart#Transparency).

If you disable image rendering by setting
[ImageTransparency](/docs/reference/engine/classes/ImageButton#ImageTransparency) to 1, it will
result in a plain rectangle that can be used as a button. However, it may
be better to use a blank [TextButton](/docs/reference/engine/classes/TextButton) instead.

Provide feedback

---

IsLoaded

Read Only

Not Replicated

Read Parallel

Indicates whether the Image has finished loading from the Roblox website.

ImageButton.IsLoaded:[boolean](/docs/luau/booleans)

This property indicates if the [Image](/docs/reference/engine/classes/ImageButton#Image) property
has finished loading from Roblox. Images declined by moderation will never
load.

Code Samples

Image Load Time

This code sample measures how long an ImageLabel or ImageButton takes to load
an image. If the image was already loaded, this will be 0.

```
local imageLabel = script.Parent



local startTime = workspace.DistributedGameTime



-- Wait for the image to load



while not imageLabel.IsLoaded do



task.wait()



end



-- Measure and display how long it took to load



local deltaTime = workspace.DistributedGameTime - startTime



print(("Image loaded in %.3f seconds"):format(deltaTime))
```

Provide feedback

---

PressedImage

Read Parallel

A texture ID that will be used when an [ImageButton](/docs/reference/engine/classes/ImageButton) is being
pressed.

ImageButton.PressedImage:ContentId

A texture ID that can be set as an [ImageButton](/docs/reference/engine/classes/ImageButton) property. When the
button is pressed, it will render this image.

Provide feedback

---

PressedImageContent

Read Parallel

The image content that will be used when an [ImageButton](/docs/reference/engine/classes/ImageButton) is being
pressed. Only supports asset URIs.

ImageButton.PressedImageContent:[Content](/docs/reference/engine/datatypes/Content)

An image-type Content that can be set as an [ImageButton](/docs/reference/engine/classes/ImageButton) property.
When the button is pressed, it will render this image. Only asset URIs are
supported for this property.

Provide feedback

---

ResampleMode

Read Parallel

Selects the image resampling mode for the button.

ImageButton.ResampleMode:[Enum.ResamplerMode](/docs/reference/engine/enums/ResamplerMode)

Determines how the image looks when it is scaled. By default, the image
smooths out the texture when displayed either larger or smaller than its
size in texture memory. In contrast,
[Enum.ResamplerMode.Pixelated](/docs/reference/engine/enums/ResamplerMode#Pixelated) preserves the
sharp edges of the image pixels.

Provide feedback

---

ScaleType

Read Parallel

Determines how an image will scale if displayed in a UI element whose size
differs from the source image.

ImageButton.ScaleType:[Enum.ScaleType](/docs/reference/engine/enums/ScaleType)

This property determines in what way the [Image](/docs/reference/engine/classes/ImageButton#Image)
property is rendered when the UI element's absolute size differs from the
source image's size.

By default, this property is
[Enum.ScaleType.Stretch](/docs/reference/engine/enums/ScaleType#Stretch) which will simply
stretch/compact the image dimensions so it fits the UI element's space
exactly. Since transparent pixels are set to black when uploading to
Roblox, transparent images should apply alpha blending to avoid a blackish
outline around scaled images.

For [Enum.ScaleType.Slice](/docs/reference/engine/enums/ScaleType#Slice), when scaling up, the corners will remain the
source image size. The edges of the image will stretch to the width/height
of the image. Finally, the center of the image will stretch to fill the
center area of the image. To learn more about 9‑sliced images, see
[UI 9‑Slice Design](/docs/ui/9-slice).

For [Enum.ScaleType.Tile](/docs/reference/engine/enums/ScaleType#Tile), the size of each image tile is determined by
the [TileSize](/docs/reference/engine/classes/ImageButton#TileSize) property.

Provide feedback

---

SliceCenter

Read Parallel

Sets the slice boundaries of a 9-sliced image.

ImageButton.SliceCenter:[Rect](/docs/reference/engine/datatypes/Rect)

This property sets the slice boundaries of a 9-sliced image when
[ScaleType](/docs/reference/engine/classes/ImageButton#ScaleType) is set to
[Enum.ScaleType.Slice](/docs/reference/engine/enums/ScaleType#Slice).

To learn more about 9‑sliced images, see
[UI 9‑Slice Design](/docs/ui/9-slice).

Provide feedback

---

SliceScale

Read Parallel

Scales the 9-slice edges by the specified ratio.

ImageButton.SliceScale:[number](/docs/luau/numbers)

Scales the 9-slice edges by the specified ratio. This means that the edges
around the 9‑slice will grow as if you'd uploaded a new version of the
texture upscaled. Defaults to 1.0.

As a multiplier for the borders of a 9-slice, it is useful for reusing one
rounded corner image for multiple radii.

See also [ScaleType](/docs/reference/engine/classes/ImageButton#ScaleType) which determines how an
image will scale if displayed in a UI element whose size differs from the
source image.

Provide feedback

---

TileSize

Read Parallel

Sets the tiling scale of the ImageButton.

ImageButton.TileSize:[UDim2](/docs/reference/engine/datatypes/UDim2)

Sets the tiling size of the [ImageButton](/docs/reference/engine/classes/ImageButton) starting at the upper-left
corner of the image. The default [UDim2](/docs/reference/engine/datatypes/UDim2) values are 1, 0, 1, 0; the scale components of the
[UDim2](/docs/reference/engine/datatypes/UDim2) will scale the tile based on the size of the
[ImageButton](/docs/reference/engine/classes/ImageButton) while the offset components are in raw pixels. For
example, a scale of 0.5 means the tile will be half the size of the
[ImageButton](/docs/reference/engine/classes/ImageButton) in the corresponding axis.

This property is only active if the
[ScaleType](/docs/reference/engine/classes/ImageButton#ScaleType) property is set to
[Enum.ScaleType.Tile](/docs/reference/engine/enums/ScaleType#Tile).

Provide feedback

---