# EditableImage | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/EditableImage
Scraped: 2026-01-11T02:28:34.995064Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- EditableImage
- EditableMesh
- AssetService:CreateEditableImage()
- AssetService:CreateEditableImageAsync()
- ImageLabel.ImageContent
- MeshPart.TextureContent
- AssetService:PromptCreateAssetAsync()
- DrawImageTransformed()
- Destroy()
- EditableImage:DrawImageTransformed()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [EditableImage](/docs/reference/engine/classes/EditableImage)

English

Feedback

Engine Class

![EditableImage](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/EditableImage-Dark.webp)EditableImage

Instance which allows for the runtime creation and manipulation of images.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Size](#Size):[Vector2](/docs/reference/engine/datatypes/Vector2) |

Methods

|  |
| --- |
| [Destroy](#Destroy)():() |
| [DrawCircle](#DrawCircle)(center: [Vector2](/docs/reference/engine/datatypes/Vector2),radius: [number](/docs/luau/numbers),color: [Color3](/docs/reference/engine/datatypes/Color3),transparency: [number](/docs/luau/numbers),combineType: [Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)):() |
| [DrawImage](#DrawImage)(position: [Vector2](/docs/reference/engine/datatypes/Vector2),image: [EditableImage](/docs/reference/engine/classes/EditableImage),combineType: [Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)):() |
| [DrawImageProjected](#DrawImageProjected)(mesh: [EditableMesh](/docs/reference/engine/classes/EditableMesh),projection: [Dictionary](/docs/luau/tables#dictionaries),brushConfig: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [DrawImageTransformed](#DrawImageTransformed)(position: [Vector2](/docs/reference/engine/datatypes/Vector2),scale: [Vector2](/docs/reference/engine/datatypes/Vector2),rotation: [number](/docs/luau/numbers),image: [EditableImage](/docs/reference/engine/classes/EditableImage),options: [Dictionary](/docs/luau/tables#dictionaries)?):() |
| [DrawLine](#DrawLine)(p1: [Vector2](/docs/reference/engine/datatypes/Vector2),p2: [Vector2](/docs/reference/engine/datatypes/Vector2),color: [Color3](/docs/reference/engine/datatypes/Color3),transparency: [number](/docs/luau/numbers),combineType: [Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)):() |
| [DrawRectangle](#DrawRectangle)(position: [Vector2](/docs/reference/engine/datatypes/Vector2),size: [Vector2](/docs/reference/engine/datatypes/Vector2),color: [Color3](/docs/reference/engine/datatypes/Color3),transparency: [number](/docs/luau/numbers),combineType: [Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)):() |
| [ReadPixelsBuffer](#ReadPixelsBuffer)(position: [Vector2](/docs/reference/engine/datatypes/Vector2),size: [Vector2](/docs/reference/engine/datatypes/Vector2)):[buffer](/docs/reference/engine/libraries/buffer) |
| [WritePixelsBuffer](#WritePixelsBuffer)(position: [Vector2](/docs/reference/engine/datatypes/Vector2),size: [Vector2](/docs/reference/engine/datatypes/Vector2),buffer: [buffer](/docs/reference/engine/libraries/buffer)):() |

Inherited Members

6 inherited from [Object](/docs/reference/engine/classes/Object)

EditableImage allows for the runtime creation and manipulation of images.

To create a blank EditableImage, use
[AssetService:CreateEditableImage()](/docs/reference/engine/classes/AssetService#CreateEditableImage). To create an EditableImage from
an existing image, use [AssetService:CreateEditableImageAsync()](/docs/reference/engine/classes/AssetService#CreateEditableImageAsync).

EditableImage can be used in any [Content](/docs/reference/engine/datatypes/Content) property which takes an
image, such as [ImageLabel.ImageContent](/docs/reference/engine/classes/ImageLabel#ImageContent) or
[MeshPart.TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent). This is done by setting the content property
to [Content.fromObject(editableImage)](/docs/reference/engine/datatypes/Content#fromObject).

The EditableImage coordinate system is relative to the top left of the
image:

* Top-left: (0, 0)
* Bottom-right: (Size.X - 1, Size.Y - 1)

When you use [AssetService:PromptCreateAssetAsync()](/docs/reference/engine/classes/AssetService#PromptCreateAssetAsync) to publish an
object that has a [Content](/docs/reference/engine/datatypes/Content) property which references an
EditableImage, the editable image is published as an image and the property
is set to a new asset ID.

#### Update Limitations

Only a single EditableImage can be updated per frame on the display side.
For example, if you update three EditableImage objects which are currently
being displayed, it will take three frames for all of them to be updated.

#### Enabling for Published Experiences

For security purposes, using EditableImage fails by default for published
experiences. To enable usage, you must be 13+ age verified and ID verified.
After you are verified, open Studio's
[Game Settings](/docs/studio/game-settings), select Security, and
enable the Allow Mesh / Image APIs toggle.

#### Permissions

To prevent misuse, [AssetService:CreateEditableImageAsync()](/docs/reference/engine/classes/AssetService#CreateEditableImageAsync) only allows
you to load and edit image assets:

* That are owned by the creator of the experience (if the experience is owned
  by an individual).
* That are owned by a group (if the experience is owned by the group).
* That are owned by the logged in Studio user (if the place file has not yet
  been saved or published to Roblox).

The APIs throw an error if they are used to load an asset that does not meet
the criteria above.

#### Memory Limits

Editable assets are currently expensive for memory usage. To minimize its
impact on client performance, EditableImage has strict client-side memory
budgets, although the server, Studio, and plugins operate with unlimited
memory. Linking one [EditableImage](/docs/reference/engine/classes/EditableImage) to multiple image-related
[Content](/docs/reference/engine/datatypes/Content) data types (multi-referencing) can help with memory
optimization.

---

API Reference

Properties

Size

Read Only

Not Replicated

Read Parallel

Size of the EditableImage in pixels.

EditableImage.Size:[Vector2](/docs/reference/engine/datatypes/Vector2)

Size of the EditableImage in pixels. The maximum size is
1024×1024. An EditableImage cannot be resized; this property is
read-only. In order to resize or crop an image, create a new
EditableImage and use
[DrawImageTransformed()](/docs/reference/engine/classes/EditableImage#DrawImageTransformed) to
transfer the contents; then call
[Destroy()](/docs/reference/engine/classes/EditableImage#Destroy).

Provide feedback

---

Methods

Destroy

EditableImage:Destroy():()

Returns

()

Destroys the contents of the image, immediately reclaiming used memory.

Provide feedback

---

DrawCircle

Draws a circle at the specified point.

EditableImage:DrawCircle(

center:[Vector2](/docs/reference/engine/datatypes/Vector2), radius:[number](/docs/luau/numbers), color:[Color3](/docs/reference/engine/datatypes/Color3), transparency:[number](/docs/luau/numbers), combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)

):()

Parameters

|  |
| --- |
| center:[Vector2](/docs/reference/engine/datatypes/Vector2)  Center of the circle, relative to the top-left corner of the EditableImage. Positions outside the canvas bounds are allowed. |
| radius:[number](/docs/luau/numbers)  Radius of the circle in pixels. |
| color:[Color3](/docs/reference/engine/datatypes/Color3)  Color of the circle. |
| transparency:[number](/docs/luau/numbers)  Transparency of the circle with 0 being fully opaque and 1 being fully transparent. |
| combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)  How the pixels of the source image are blended with the pixels of the added image. |

Returns

()

Draws a circle at the specified point on the EditableImage. If the
circle is semi-transparent, it will be blended with the pixels behind it
using source over blending.

Provide feedback

---

DrawImage

Draws another EditableImage into this EditableImage at the given
position.

EditableImage:DrawImage(

position:[Vector2](/docs/reference/engine/datatypes/Vector2), image:[EditableImage](/docs/reference/engine/classes/EditableImage), combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)

):()

Parameters

|  |
| --- |
| position:[Vector2](/docs/reference/engine/datatypes/Vector2)  Position at which the top-left corner of the added image will be drawn. |
| image:[EditableImage](/docs/reference/engine/classes/EditableImage)  The EditableImage to draw into this EditableImage. |
| combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)  How the pixels of the source image should be blended with the pixels of the added image. |

Returns

()

Draws another EditableImage into this EditableImage at the given
position. Positions outside the canvas bounds are allowed such that only
part of the new image is drawn.

Provide feedback

---

DrawImageProjected

Projects another EditableImage into an [EditableMesh](/docs/reference/engine/classes/EditableMesh) and stores
the result on this EditableImage.

EditableImage:DrawImageProjected(

mesh:[EditableMesh](/docs/reference/engine/classes/EditableMesh), projection:[Dictionary](/docs/luau/tables#dictionaries), brushConfig:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| mesh:[EditableMesh](/docs/reference/engine/classes/EditableMesh)  The [EditableMesh](/docs/reference/engine/classes/EditableMesh) used to project into. |
| projection:[Dictionary](/docs/luau/tables#dictionaries)  Projection configuration dictionary including the following key-value pairs:   * Direction ([Vector3](/docs/reference/engine/datatypes/Vector3)) where the projector is facing. * Position ([Vector3](/docs/reference/engine/datatypes/Vector3)) as the position in local space with   respect to the mesh. * Size ([Vector3](/docs/reference/engine/datatypes/Vector3)) as the size of the projector. * Up ([Vector3](/docs/reference/engine/datatypes/Vector3)) as the up vector of the projector in local   space with respect to the mesh. |
| brushConfig:[Dictionary](/docs/luau/tables#dictionaries)  Brush configuration dictionary including the following key-value pairs:   * AlphaBlendType ([Enum.ImageAlphaType](/docs/reference/engine/enums/ImageAlphaType)) which determines how this   projection will blend alpha values. * ColorBlendType ([Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)) which determines how this   projection will blend color values. * Decal (EditableImage) as the image used for projection. * FadeAngle (number) as the angle in degrees for the projection   edges to start to fall off. The projection will be fully faded out   at 90 degrees. An angle of 0 means fading starts immediately at 0   degrees and an angle of 90 means no fading but instead a hard edge   at 90 degrees. An angle of 70 degrees would mean the projection   starts to fade at 70 degrees and is fully faded out at 90 degrees. * BlendIntensity (number) as the value between 0 and 1 which   controls how much of the projection is blended into the resulting   image. |

Returns

()

Projects another EditableImage into an [EditableMesh](/docs/reference/engine/classes/EditableMesh) and stores
the result on this EditableImage by using the specified projection and
brush configuration.

Provide feedback

---

DrawImageTransformed

Draws an image into this EditableImage with transformations including
scaling and rotation, placing it at the specified position.

EditableImage:DrawImageTransformed(

position:[Vector2](/docs/reference/engine/datatypes/Vector2), scale:[Vector2](/docs/reference/engine/datatypes/Vector2), rotation:[number](/docs/luau/numbers), image:[EditableImage](/docs/reference/engine/classes/EditableImage), options:[Dictionary](/docs/luau/tables#dictionaries)?

):()

Parameters

|  |
| --- |
| position:[Vector2](/docs/reference/engine/datatypes/Vector2)  Position in pixels where the pivot point of the source image will be placed on this image. |
| scale:[Vector2](/docs/reference/engine/datatypes/Vector2)  Scaling factors for the source image along the X and Y axes. |
| rotation:[number](/docs/luau/numbers)  The rotation angle in degrees, applied around the pivot point of the source image. |
| image:[EditableImage](/docs/reference/engine/classes/EditableImage)  The source EditableImage to be drawn into this image. |
| options:[Dictionary](/docs/luau/tables#dictionaries)?  Optional dictionary for additional configuration:   * CombineType: Specifies how the pixels of the source image blend   with those of the destination. Default is   [Enum.ImageCombineType.AlphaBlend](/docs/reference/engine/enums/ImageCombineType#AlphaBlend). * SamplingMode: Specifies the sampling method (e.g. Default for   bilinear or Pixelated for nearest neighbor). Default is   [Enum.ResamplerMode.Default](/docs/reference/engine/enums/ResamplerMode#Default). * PivotPoint: Specifies the pivot point within the source image for   scaling and rotation. Default is the center of the source image   (i.e. Image.Size / 2). |

Returns

()

This method lets you draw an EditableImage into this EditableImage
with transformations applied, such as scaling and rotation. The position
parameter specifies where the pivot point of the source image will be
placed on this image after transformations. Positions outside the canvas
bounds are allowed such that only part of the new image is drawn.

Code Samples

EditableImage:DrawImageTransformed()

The following code draws a rotated and scaled image onto another.

```
local AssetService = game:GetService("AssetService")



-- Example of drawing a rotated and scaled image onto another EditableImage



local srcImage = AssetService:CreateEditableImage({ Size = Vector2.new(256, 256) })



local dstImage = AssetService:CreateEditableImage({ Size = Vector2.new(512, 512) })



-- Drawing with a rotation of 45 degrees, scaling by 2x, and placing at (100, 100)



dstImage:DrawImageTransformed(



Vector2.new(100, 100), -- Position



Vector2.new(2, 2), -- Scale



45, -- Rotation (degrees)



srcImage, -- Source image



{



CombineType = Enum.ImageCombineType.AlphaBlend, -- Optional, default is AlphaBlend



SamplingMode = Enum.ResamplerMode.Default, -- Optional, default is Default



PivotPoint = srcImage.Size / 2, -- Optional, default is center of the source image



}



)
```

EditableImage:DrawImageTransformed() - Crop

The following code shows how cropping an image can be done using the [EditableImage:DrawImageTransformed()](/docs/reference/engine/classes/EditableImage#DrawImageTransformed) method.

```
local AssetService = game:GetService("AssetService")



-- Source image



local srcImage = AssetService:CreateEditableImageAsync(Content.fromUri(assetUri))



-- Crop area defined by offset and size



local cropOffset = Vector2.new(50, 50)



local cropSize = Vector2.new(100, 100)



-- Destination image with size of the crop area



local dstImage = AssetService:CreateEditableImage({ Size = cropSize })



-- Position (top-left corner)



local position = Vector2.new(0, 0)



-- Scale factors (no scaling)



local scale = Vector2.new(1, 1)



-- Rotation angle (no rotation)



local rotation = 0



-- Draw the source image onto the destination image with adjusted pivot to crop the image



dstImage:DrawImageTransformed(position, scale, rotation, srcImage, {



CombineType = Enum.ImageCombineType.Overwrite,



PivotPoint = cropOffset, -- Set pivot point to cropOffset to start drawing from there



})
```

Provide feedback

---

DrawLine

Draws a line between two provided points.

EditableImage:DrawLine(

p1:[Vector2](/docs/reference/engine/datatypes/Vector2), p2:[Vector2](/docs/reference/engine/datatypes/Vector2), color:[Color3](/docs/reference/engine/datatypes/Color3), transparency:[number](/docs/luau/numbers), combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)

):()

Parameters

|  |
| --- |
| p1:[Vector2](/docs/reference/engine/datatypes/Vector2)  Start point of the line. |
| p2:[Vector2](/docs/reference/engine/datatypes/Vector2)  End point of the line. |
| color:[Color3](/docs/reference/engine/datatypes/Color3)  Color of the line. |
| transparency:[number](/docs/luau/numbers)  Transparency of the line. |
| combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)  How the pixels of the source image are blended with the pixels of the added image. |

Returns

()

Draws an anti-aliased line on the EditableImage one pixel thick between
the two provided points.

Provide feedback

---

DrawRectangle

Draws a rectangle of the given size at the given top-left position.

EditableImage:DrawRectangle(

position:[Vector2](/docs/reference/engine/datatypes/Vector2), size:[Vector2](/docs/reference/engine/datatypes/Vector2), color:[Color3](/docs/reference/engine/datatypes/Color3), transparency:[number](/docs/luau/numbers), combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)

):()

Parameters

|  |
| --- |
| position:[Vector2](/docs/reference/engine/datatypes/Vector2)  Position of the top-left of the rectangle. Unlike other drawing methods, this cannot be outside the canvas bounds of the EditableImage. |
| size:[Vector2](/docs/reference/engine/datatypes/Vector2)  Size of the rectangle to draw, in pixels. |
| color:[Color3](/docs/reference/engine/datatypes/Color3)  Color of the rectangle. |
| transparency:[number](/docs/luau/numbers)  Transparency of the rectangle. |
| combineType:[Enum.ImageCombineType](/docs/reference/engine/enums/ImageCombineType)  How the pixels of the source image are blended with the pixels of the added image. |

Returns

()

Draws a rectangle on the EditableImage of the given size at the given
top-left position.

Provide feedback

---

ReadPixelsBuffer

Write Parallel

Reads a rectangular region of pixels into a buffer.

EditableImage:ReadPixelsBuffer(

position:[Vector2](/docs/reference/engine/datatypes/Vector2), size:[Vector2](/docs/reference/engine/datatypes/Vector2)

):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| position:[Vector2](/docs/reference/engine/datatypes/Vector2)  Top-left corner of the rectangular region of pixels to read. |
| size:[Vector2](/docs/reference/engine/datatypes/Vector2)  Size of the rectangular region of pixels to read. |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

Buffer where each pixel is represented by four bytes (red, green, blue
and alpha respectively). The length of the buffer can be calculated as
Size.X \* Size.Y \* 4 bytes.

Reads a rectangular region of pixels from an EditableImage and returns
it as a buffer. Each number in the buffer is a single byte, with pixels
stored in a sequence of four bytes (red, green, blue, and alpha).

Note that this method uses alpha instead of transparency, unlike the
EditableImage drawing methods.

Code Samples

EditableImage:ReadPixelsBuffer()

The following code reads two pixels from a [EditableImage](/docs/reference/engine/classes/EditableImage) and creates a part with the average color between them.

```
local AssetService = game:GetService("AssetService")



local options = { Size = Vector2.new(32, 32) }



local editableImage = AssetService:CreateEditableImage(options)



local pixelsBuffer = editableImage:ReadPixelsBuffer(Vector2.zero, Vector2.new(2, 1))



local color1 =



Color3.fromRGB(buffer.readu8(pixelsBuffer, 0), buffer.readu8(pixelsBuffer, 1), buffer.readu8(pixelsBuffer, 2))



local transparency1 = (255 - buffer.readu8(pixelsBuffer, 3)) / 255



local color2 =



Color3.fromRGB(buffer.readu8(pixelsBuffer, 4), buffer.readu8(pixelsBuffer, 5), buffer.readu8(pixelsBuffer, 6))



local transparency2 = (255 - buffer.readu8(pixelsBuffer, 7)) / 255



local averageColor = color1:Lerp(color2, 0.5)



local averageTransparency = (transparency1 + transparency2) / 2



local part = Instance.new("Part")



part.Color = averageColor



part.Transparency = averageTransparency



part.Parent = workspace
```

Provide feedback

---

WritePixelsBuffer

Writes a rectangular region of pixels into the image.

EditableImage:WritePixelsBuffer(

position:[Vector2](/docs/reference/engine/datatypes/Vector2), size:[Vector2](/docs/reference/engine/datatypes/Vector2), buffer:[buffer](/docs/reference/engine/libraries/buffer)

):()

Parameters

|  |
| --- |
| position:[Vector2](/docs/reference/engine/datatypes/Vector2)  Top-left corner of the rectangular region to draw the pixels into. |
| size:[Vector2](/docs/reference/engine/datatypes/Vector2)  Size of the rectangular region of pixels to write. |
| buffer:[buffer](/docs/reference/engine/libraries/buffer)  A buffer where each pixel is represented by four bytes (red, green, blue, and alpha respectively). The length of the buffer should be Size.X \* Size.Y \* 4 bytes. |

Returns

()

Writes a rectangular region of pixels to an EditableImage from a buffer.
Each number in the buffer is a single byte, with pixels stored in a
sequence of four bytes (red, green, blue, and alpha).

Note that this method uses alpha instead of transparency, unlike the
EditableImage drawing methods.

Code Samples

EditableImage:WritePixelsBuffer()

The following code reads the pixels of a [EditableImage](/docs/reference/engine/classes/EditableImage) and writes back the inverted color values of those pixels.

```
local AssetService = game:GetService("AssetService")



local options = { Size = Vector2.new(32, 32) }



local editableImage = AssetService:CreateEditableImage(options)



local pixelsBuffer = editableImage:ReadPixelsBuffer(Vector2.zero, editableImage.Size)



for i = 1, editableImage.Size.X * editableImage.Size.Y do



local pixelIndex = (i - 1) * 4



buffer.writeu8(pixelsBuffer, pixelIndex, 255 - buffer.readu8(pixelsBuffer, pixelIndex))



buffer.writeu8(pixelsBuffer, pixelIndex + 1, 255 - buffer.readu8(pixelsBuffer, pixelIndex + 1))



buffer.writeu8(pixelsBuffer, pixelIndex + 2, 255 - buffer.readu8(pixelsBuffer, pixelIndex + 2))



-- Set alpha to 255 to make all pixels fully opaque.



buffer.writeu8(pixelsBuffer, pixelIndex + 3, 255)



end



editableImage:WritePixelsBuffer(Vector2.zero, editableImage.Size, pixelsBuffer)
```

Provide feedback

---