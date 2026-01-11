# ImageLabel | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ImageLabel
Scraped: 2026-01-11T02:33:20.092734Z

## Tags
- Not Replicated

## Inherits
- GuiLabel
- ImageLabel
- GuiObject
- GuiBase2d
- Instance
- Object
- Frame
- ImageColor3
- ImageTransparency
- GuiObject.BackgroundTransparency
- ScaleType
- TileSize
- SliceCenter
- ImageRectOffset
- ImageRectSize
- ImageContent
- Decal.Texture
- EditableImage
- ImageButton.ImageColor3
- ImageButton.ScaleType
- ImageLabel.Image
- SliceScale
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiLabel](/docs/reference/engine/classes/GuiLabel)
6. /
7. [ImageLabel](/docs/reference/engine/classes/ImageLabel)

English

Feedback

Engine Class

![ImageLabel](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ImageLabel-Dark.webp)ImageLabel

A 2D user interface element that displays a single non-interactive image.

---

Summary

Properties

|  |
| --- |
| [Image](#Image):ContentId |
| [ImageColor3](#ImageColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ImageContent](#ImageContent):[Content](/docs/reference/engine/datatypes/Content) |
| [ImageRectOffset](#ImageRectOffset):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [ImageRectSize](#ImageRectSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [ImageTransparency](#ImageTransparency):[number](/docs/luau/numbers) |
| [IsLoaded](#IsLoaded):[boolean](/docs/luau/booleans) |
| [ResampleMode](#ResampleMode):[Enum.ResamplerMode](/docs/reference/engine/enums/ResamplerMode) |
| [ScaleType](#ScaleType):[Enum.ScaleType](/docs/reference/engine/enums/ScaleType) |
| [SliceCenter](#SliceCenter):[Rect](/docs/reference/engine/datatypes/Rect) |
| [SliceScale](#SliceScale):[number](/docs/luau/numbers) |
| [TileSize](#TileSize):[UDim2](/docs/reference/engine/datatypes/UDim2) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An [ImageLabel](/docs/reference/engine/classes/ImageLabel) renders a rectangle, like a [Frame](/docs/reference/engine/classes/Frame) does, with an
image asset. The display of the image can be manipulated through the
[ImageColor3](/docs/reference/engine/classes/ImageLabel#ImageColor3) and
[ImageTransparency](/docs/reference/engine/classes/ImageLabel#ImageTransparency) properties. To display
only the image and hide the rectangle, set
[GuiObject.BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency) to 1.

Advanced [ImageLabel](/docs/reference/engine/classes/ImageLabel) usage includes:

* Tiled images can be created by setting
  [ScaleType](/docs/reference/engine/classes/ImageLabel#ScaleType) to [Enum.ScaleType.Tile](/docs/reference/engine/enums/ScaleType#Tile), then
  [TileSize](/docs/reference/engine/classes/ImageLabel#TileSize) to the size of rendered tiles.
* 9-slice images can be created by setting
  [ScaleType](/docs/reference/engine/classes/ImageLabel#ScaleType) to [Enum.ScaleType.Slice](/docs/reference/engine/enums/ScaleType#Slice), then
  [SliceCenter](/docs/reference/engine/classes/ImageLabel#SliceCenter) to the center area of the 9‑slice
  image.
* Sprite sheets can be implemented through the use of
  [ImageRectOffset](/docs/reference/engine/classes/ImageLabel#ImageRectOffset) and
  [ImageRectSize](/docs/reference/engine/classes/ImageLabel#ImageRectSize). Packing multiple images into
  one and using this property can make your experience's image assets load
  much quicker, especially if you use many small icons in your GUIs.

---

API Reference

Properties

Image

Read Parallel

The image content displayed by the UI element. Reads and writes to
[ImageContent](/docs/reference/engine/classes/ImageLabel#ImageContent).

ImageLabel.Image:ContentId

This property is a content-type property that should hold the asset ID of
a decal or image uploaded to Roblox. It functions identically to
[Decal.Texture](/docs/reference/engine/classes/Decal#Texture) with regards to loading the image from Roblox. The
rendered image can be modified using
[ImageColor3](/docs/reference/engine/classes/ImageLabel#ImageColor3) and
[ImageTransparency](/docs/reference/engine/classes/ImageLabel#ImageTransparency).

Provide feedback

---

ImageColor3

Read Parallel

Determines how a rendered image will be colorized.

ImageLabel.ImageColor3:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines how an image is colorized. When set to white, no
colorization occurs. This property is very useful for reusing image
assets; if the source image is completely white with transparency, you can
set the entire color of the image at once with this property.

Provide feedback

---

ImageContent

Read Parallel

The image content displayed by the UI element. Supports
[asset URIs](/docs/projects/assets#asset-uris) and
[EditableImage](/docs/reference/engine/classes/EditableImage) objects.

ImageLabel.ImageContent:[Content](/docs/reference/engine/datatypes/Content)

This property should hold an
[asset URI](/docs/projects/assets#asset-uris) or a reference
to an [EditableImage](/docs/reference/engine/classes/EditableImage) object.

The asset URI can reference a decal or image uploaded to Roblox. It
functions identically to [Decal.Texture](/docs/reference/engine/classes/Decal#Texture) with regards to loading the
image.

The rendered image will be colorized using
[ImageButton.ImageColor3](/docs/reference/engine/classes/ImageButton#ImageColor3). It is possible to make the image render
as tiled, scaled to fit, or 9-sliced, by adjusting the
[ImageButton.ScaleType](/docs/reference/engine/classes/ImageButton#ScaleType) property.

Provide feedback

---

ImageRectOffset

Read Parallel

The offset in pixels of the sub-area of an image to be displayed.

ImageLabel.ImageRectOffset:[Vector2](/docs/reference/engine/datatypes/Vector2)

Allows the partial display of an image in conjunction with
[ImageRectSize](/docs/reference/engine/classes/ImageLabel#ImageRectSize). This property determines
the pixel offset (from the top-left) of the image area to be displayed.

Provide feedback

---

ImageRectSize

Read Parallel

Determines the size in pixels of the sub-area of an image to be displayed.

ImageLabel.ImageRectSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

Allows the partial display of an image in conjunction with
[ImageRectOffset](/docs/reference/engine/classes/ImageLabel#ImageRectOffset). This property
determines the pixel size of the image area to be displayed. If either
dimension is set to 0, the entire image is displayed instead.

Provide feedback

---

ImageTransparency

Read Parallel

Determines the transparency of the rendered image.

ImageLabel.ImageTransparency:[number](/docs/luau/numbers)

This property determines the alpha of a UI element's rendered image. A
value of 0 is completely opaque and a value of 1 is completely
transparent (invisible).

Code Samples

Oscillate ImageTransparency

This code sample oscillates the ImageTransparency of an ImageLabel/ImageButton
from 0 to 1 using a sine wave.

```
local RunService = game:GetService("RunService")



local imageLabel = script.Parent



local function onRenderStep()



-- Oscillate ImageTransparency from 0 to 1 using a sine wave



imageLabel.ImageTransparency = math.sin(workspace.DistributedGameTime * math.pi) * 0.5 + 0.5



end



RunService.RenderStepped:Connect(onRenderStep)
```

Provide feedback

---

IsLoaded

Read Only

Not Replicated

Read Parallel

Indicates whether the image has finished loading from Roblox.

ImageLabel.IsLoaded:[boolean](/docs/luau/booleans)

This property indicates if the [ImageLabel.Image](/docs/reference/engine/classes/ImageLabel#Image) property has
finished loading from Roblox. Images declined by moderation will never
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

ResampleMode

Read Parallel

Selects the image resampling mode for the label.

ImageLabel.ResampleMode:[Enum.ResamplerMode](/docs/reference/engine/enums/ResamplerMode)

Determines how the image looks when it is scaled. By default, the image
smooths out texturing when displayed on the screen larger or smaller than
its size in texture memory. When set to
[Enum.ResamplerMode.Pixelated](/docs/reference/engine/enums/ResamplerMode#Pixelated), the image
preserves the sharp edges of pixels.

Provide feedback

---

ScaleType

Read Parallel

Determines how an image will scale if displayed in a UI element whose size
differs from the source image.

ImageLabel.ScaleType:[Enum.ScaleType](/docs/reference/engine/enums/ScaleType)

This property determines in what way an [ImageLabel.Image](/docs/reference/engine/classes/ImageLabel#Image) is
rendered when the UI element's absolute size differs from the source
image's size.

By default, this property is [Enum.ScaleType.Stretch](/docs/reference/engine/enums/ScaleType#Stretch) which will simply
stretch/compact the image dimensions so it fits the UI element's space
exactly. Since transparent pixels are set to black when uploading to
Roblox, transparent images should apply alpha blending to avoid a blackish
outline around scaled images.

For [Enum.ScaleType.Slice](/docs/reference/engine/enums/ScaleType#Slice), the [SliceCenter](/docs/reference/engine/classes/ImageLabel#SliceCenter)
property will be revealed in the
[Properties](/docs/studio/properties) window. This is for nine-slice
UI: when scaling up, the corners will remain the source image size. The
edges of the image will stretch to the width/height of the image. Finally,
the center of the image will stretch to fill the center area of the image.

Finally, for [Enum.ScaleType.Tile](/docs/reference/engine/enums/ScaleType#Tile), the
[TileSize](/docs/reference/engine/classes/ImageLabel#TileSize) property will be revealed in the
[Properties](/docs/studio/properties) window. This is for tiled
images, where the size of each image tile is determined by the
[TileSize](/docs/reference/engine/classes/ImageLabel#TileSize) property.

Provide feedback

---

SliceCenter

Read Parallel

Sets the slice boundaries of a 9-sliced image.

ImageLabel.SliceCenter:[Rect](/docs/reference/engine/datatypes/Rect)

This property sets the slice boundaries of a 9-sliced image when
[ScaleType](/docs/reference/engine/classes/ImageLabel#ScaleType) is set to
[Enum.ScaleType.Slice](/docs/reference/engine/enums/ScaleType#Slice). Please note that this
property is only visible in the
[Properties](/docs/studio/properties) window under this condition.

To learn more about 9-slice images, see
[UI 9 Slice Design](/docs/ui/9-slice).

Provide feedback

---

SliceScale

Read Parallel

Scales the 9-slice edges by the specified ratio.

ImageLabel.SliceScale:[number](/docs/luau/numbers)

Scales the 9-slice edges by the specified ratio. This means that the edges
around the 9-slice will grow as if you'd uploaded a new version of the
texture upscaled. Defaults to 1.0.

See also [ScaleType](/docs/reference/engine/classes/ImageLabel#ScaleType),
[SliceCenter](/docs/reference/engine/classes/ImageLabel#SliceCenter), and
[SliceScale](/docs/reference/engine/classes/ImageLabel#SliceScale).

Provide feedback

---

TileSize

Read Parallel

Sets the tiling size of the [ImageLabel](/docs/reference/engine/classes/ImageLabel).

ImageLabel.TileSize:[UDim2](/docs/reference/engine/datatypes/UDim2)

This property sets the tiling size of the [ImageLabel](/docs/reference/engine/classes/ImageLabel) with a
default of
[UDim2.new(1, 0, 1, 0)](/docs/reference/engine/datatypes/UDim2#new). Tiling
starts at the top-left corner of the image. This property is only active
if the [ScaleType](/docs/reference/engine/classes/ImageLabel#ScaleType) for the [ImageLabel](/docs/reference/engine/classes/ImageLabel)
is set to [Enum.ScaleType.Tile](/docs/reference/engine/enums/ScaleType#Tile).

Code Samples

Image ScaleType Demo

This code sample demonstrates the different ScaleType options - Stretch, Tile
and Slice. It does this by resizing an ImageLabel/ImageButton in a circle.

```
local imageLabel = script.Parent



-- Set the source image to be a 64x64 padlock



imageLabel.Image = "rbxassetid://284402752"



imageLabel.BackgroundTransparency = 0



imageLabel.BackgroundColor3 = Color3.new(1, 1, 1) -- White



imageLabel.ImageColor3 = Color3.new(0, 0, 0) -- Black



local function resizeInACircle()



for theta = 0, 2, 0.02 do



imageLabel.Size =



UDim2.new(0, 100 + math.cos(theta * 2 * math.pi) * 50, 0, 100 + math.sin(theta * 2 * math.pi) * 50)



task.wait()



end



end



while true do



-- Stretch simply stretches the source image to fit



-- the UI element's space



imageLabel.ScaleType = Enum.ScaleType.Stretch



resizeInACircle()



-- Tile will render the source image multiple times



-- enough to fill the UI element's space



imageLabel.ScaleType = Enum.ScaleType.Tile



imageLabel.TileSize = UDim2.new(0, 64, 0, 64)



resizeInACircle()



-- Slice will turn the image into a nine-slice UI.



imageLabel.ScaleType = Enum.ScaleType.Slice



imageLabel.SliceCenter = Rect.new(30, 30, 34, 34)



resizeInACircle()



end
```

Provide feedback

---