# VideoDisplay | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VideoDisplay
Scraped: 2026-01-11T02:35:50.545149Z

## Inherits
- GuiObject
- VideoDisplay
- VideoPlayer
- Wire
- GuiBase2d
- Instance
- Object
- ImageLabel
- VideoRectSize
- VideoRectOffset
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiObject](/docs/reference/engine/classes/GuiObject)
6. /
7. [VideoDisplay](/docs/reference/engine/classes/VideoDisplay)

English

Feedback

Engine Class

![VideoDisplay](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/VideoDisplay-Dark.webp)VideoDisplay

A GUI object that displays video content from a connected [VideoPlayer](/docs/reference/engine/classes/VideoPlayer).

Not Browsable

---

Summary

Properties

|  |
| --- |
| [ResampleMode](#ResampleMode):[Enum.ResamplerMode](/docs/reference/engine/enums/ResamplerMode) |
| [ScaleType](#ScaleType):[Enum.ScaleType](/docs/reference/engine/enums/ScaleType) |
| [TileSize](#TileSize):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [VideoColor3](#VideoColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [VideoRectOffset](#VideoRectOffset):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [VideoRectSize](#VideoRectSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [VideoTransparency](#VideoTransparency):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [VideoDisplay](/docs/reference/engine/classes/VideoDisplay) is a GUI object that displays video content from a
[VideoPlayer](/docs/reference/engine/classes/VideoPlayer) connected via a [Wire](/docs/reference/engine/classes/Wire). It functions similarly to a
[ImageLabel](/docs/reference/engine/classes/ImageLabel) but is designed for video playback.

---

API Reference

Properties

ResampleMode

Read Parallel

Selects the texture resampling mode for the [VideoDisplay](/docs/reference/engine/classes/VideoDisplay).

VideoDisplay.ResampleMode:[Enum.ResamplerMode](/docs/reference/engine/enums/ResamplerMode)

Determines how the video looks when it is scaled. By default, the video
smooths out texturing when displayed on the screen larger or smaller than
its size in texture memory. When set to
[Enum.ResamplerMode.Pixelated](/docs/reference/engine/enums/ResamplerMode#Pixelated), the video
preserves the sharp edges of pixels.

Provide feedback

---

ScaleType

Read Parallel

Determines how a video will scale if displayed in a UI element whose
aspect ratio differs from the source video.

VideoDisplay.ScaleType:[Enum.ScaleType](/docs/reference/engine/enums/ScaleType)

Determines how a video texture is rendered when the UI element's aspect
ratio differs from the source video's aspect ratio.

By default, this property is [Enum.ScaleType.Stretch](/docs/reference/engine/enums/ScaleType#Stretch) which will simply
stretch/compact the video texture dimensions so it fits the UI element's
space exactly.

Provide feedback

---

TileSize

Read Parallel

VideoDisplay.TileSize:[UDim2](/docs/reference/engine/datatypes/UDim2)

Provide feedback

---

VideoColor3

Read Parallel

Determines how a rendered video will be colorized.

VideoDisplay.VideoColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Determines how a video is colorized. When set to white, no colorization
occurs. This property is useful for reusing video assets.

Provide feedback

---

VideoRectOffset

Read Parallel

The offset in pixels of the sub-area of a video to be displayed.

VideoDisplay.VideoRectOffset:[Vector2](/docs/reference/engine/datatypes/Vector2)

Allows the partial display of a video in conjunction with
[VideoRectSize](/docs/reference/engine/classes/VideoDisplay#VideoRectSize). This property determines
the pixel offset (from the top-left) of the video area to be displayed.

Provide feedback

---

VideoRectSize

Read Parallel

Determines the size in pixels of the sub-area of a video to be displayed.

VideoDisplay.VideoRectSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

Allows the partial display of a video in conjunction with
[VideoRectOffset](/docs/reference/engine/classes/VideoDisplay#VideoRectOffset). This property
determines the pixel size of the video area to be displayed. If either
dimension is set to 0, the entire video is displayed instead.

Provide feedback

---

VideoTransparency

Read Parallel

Determines the transparency of the rendered video.

VideoDisplay.VideoTransparency:[number](/docs/luau/numbers)

Determines the alpha of a UI element's rendered video texture. A value of
0 is completely opaque, and a value of 1 is completely transparent
(invisible).

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

VideoDisplay:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [VideoDisplay](/docs/reference/engine/classes/VideoDisplay) has one "Input" pin.

Provide feedback

---

GetInputPins

VideoDisplay:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

VideoDisplay:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[VideoDisplay](/docs/reference/engine/classes/VideoDisplay) via a [Wire](/docs/reference/engine/classes/Wire).

VideoDisplay.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [VideoDisplay](/docs/reference/engine/classes/VideoDisplay) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [VideoDisplay](/docs/reference/engine/classes/VideoDisplay) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected, and that
[Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[VideoDisplay](/docs/reference/engine/classes/VideoDisplay) and to some other wirable instance.

Provide feedback

---