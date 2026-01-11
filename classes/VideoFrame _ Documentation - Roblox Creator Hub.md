# VideoFrame | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VideoFrame
Scraped: 2026-01-11T02:41:34.717320Z

## Tags
- Not Replicated

## Inherits
- GuiObject
- VideoFrame
- Frame
- GuiBase2d
- Instance
- Object
- SurfaceGui
- BasePart
- BasePart.Position
- Camera
- VideoFrame.Video
- VideoFrame:Play()
- VideoFrame:Pause()
- VideoFrame.Playing
- VideoFrame.TimePosition
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiObject](/docs/reference/engine/classes/GuiObject)
6. /
7. [VideoFrame](/docs/reference/engine/classes/VideoFrame)

English

Feedback

Engine Class

![VideoFrame](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/VideoFrame-Dark.webp)VideoFrame

A GUI object that renders a rectangle, like a [Frame](/docs/reference/engine/classes/Frame) does, with a
moving video image.

---

Summary

Properties

|  |
| --- |
| [IsLoaded](#IsLoaded):[boolean](/docs/luau/booleans) |
| [Looped](#Looped):[boolean](/docs/luau/booleans) |
| [Playing](#Playing):[boolean](/docs/luau/booleans) |
| [Resolution](#Resolution):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [TimeLength](#TimeLength):[number](/docs/luau/numbers) |
| [TimePosition](#TimePosition):[number](/docs/luau/numbers) |
| [Video](#Video):ContentId |
| [VideoContent](#VideoContent):[Content](/docs/reference/engine/datatypes/Content) |
| [Volume](#Volume):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Pause](#Pause)():() |
| [Play](#Play)():() |

Events

|  |
| --- |
| [DidLoop](#DidLoop)(video: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Ended](#Ended)(video: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Loaded](#Loaded)(video: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Paused](#Paused)(video: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Played](#Played)(video: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A VideoFrame renders a rectangle, like a [Frame](/docs/reference/engine/classes/Frame) does, with a moving
video image. The video must be from a file uploaded to the Roblox website.

The video is scaled to fit the entirety of the rectangle, but looks best when
displayed at its native resolution.

2D and 3D Sound
---------------

A VideoFrame placed underneath [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) on a [BasePart](/docs/reference/engine/classes/BasePart) will
emit its sound from that part's [BasePart.Position](/docs/reference/engine/classes/BasePart#Position).

A VideoFrame exhibits the Doppler effect, meaning its frequency and pitch
varies with the relative motion of whatever part it is attached to.

The volume of the VideoFrame will be determined by the distance between the
client's sound listener (by default the [Camera](/docs/reference/engine/classes/Camera) position) and the
position of the VideoFrame's part.

A VideoFrame is considered "global" if it is not placed underneath
SurfaceGui on a BasePart. In this case, the sound will play at the same volume
throughout the entire place.

Code Samples

Creating and Playing a Video

The code sample below demonstrates how to create and play a VideoFrame with
some valid asset ID after the video has loaded.

```
local screenPart = Instance.new("Part")



screenPart.Parent = workspace



local surfaceGui = Instance.new("SurfaceGui")



surfaceGui.Parent = screenPart



local videoFrame = Instance.new("VideoFrame")



videoFrame.Parent = surfaceGui



videoFrame.Looped = true



videoFrame.Video = "rbxassetid://" -- add an asset ID to this



while not videoFrame.IsLoaded do



task.wait()



end



videoFrame:Play()
```

---

API Reference

Properties

IsLoaded

Read Only

Not Replicated

Read Parallel

Indicates when the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) has loaded from Roblox servers
and is ready to play.

VideoFrame.IsLoaded:[boolean](/docs/luau/booleans)

This property will be true when the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) has loaded
from Roblox servers and is ready to play.

Provide feedback

---

Looped

Read Parallel

Sets whether or not the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) repeats once it has
finished when it is playing.

VideoFrame.Looped:[boolean](/docs/luau/booleans)

This property sets whether or not the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) repeats
once it has finished when it is playing.

Provide feedback

---

Playing

Not Replicated

Read Parallel

Indicates whether the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is currently playing. It
can be set to start or pause playback.

VideoFrame.Playing:[boolean](/docs/luau/booleans)

This property indicates whether the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is currently
playing. It can be set to start or pause playback as an alternative to the
[VideoFrame:Play()](/docs/reference/engine/classes/VideoFrame#Play) and [VideoFrame:Pause()](/docs/reference/engine/classes/VideoFrame#Pause) functions.

Provide feedback

---

Resolution

Read Only

Not Replicated

Read Parallel

Gets the original source resolution of the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) file.

VideoFrame.Resolution:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property gets the original source resolution of the
[VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) file.

Provide feedback

---

TimeLength

Read Only

Not Replicated

Read Parallel

Indicates the length of the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) in seconds.

VideoFrame.TimeLength:[number](/docs/luau/numbers)

This property indicates the length of the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) in
seconds. If the video is not loaded, this value will be 0.

Provide feedback

---

TimePosition

Not Replicated

Read Parallel

Indicates the progress in seconds of the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video).

VideoFrame.TimePosition:[number](/docs/luau/numbers)

This property indicates the progress in seconds of the
[VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video). It can be changed to move the playback position
of the video both before and during playback.

Provide feedback

---

Video

Read Parallel

The content ID of the video file a [VideoFrame](/docs/reference/engine/classes/VideoFrame) object is associated
with.

VideoFrame.Video:ContentId

The content ID of the video file a [VideoFrame](/docs/reference/engine/classes/VideoFrame) object is associated
with. To save resources and improve performance, set this property to ""
when the [VideoFrame](/docs/reference/engine/classes/VideoFrame) is not visible or in use.

Code Samples

Creating and Playing a Video

The code sample below demonstrates how to create and play a VideoFrame with
some valid asset ID after the video has loaded.

```
local screenPart = Instance.new("Part")



screenPart.Parent = workspace



local surfaceGui = Instance.new("SurfaceGui")



surfaceGui.Parent = screenPart



local videoFrame = Instance.new("VideoFrame")



videoFrame.Parent = surfaceGui



videoFrame.Looped = true



videoFrame.Video = "rbxassetid://" -- add an asset ID to this



while not videoFrame.IsLoaded do



task.wait()



end



videoFrame:Play()
```

Provide feedback

---

VideoContent

Read Parallel

VideoFrame.VideoContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

Volume

Read Parallel

Indicates how loud the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is currently playing back.

VideoFrame.Volume:[number](/docs/luau/numbers)

This property determines how loud the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) plays back.
It can be set to a number between 0 and 100.

Provide feedback

---

Methods

Pause

Sets [VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to false, pausing playback if the
[VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is playing.

VideoFrame:Pause():()

Returns

()

Sets [VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to false, pausing playback if the
[VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is playing.

As [VideoFrame.TimePosition](/docs/reference/engine/classes/VideoFrame#TimePosition) is not reset, when the video is resumed
it will continue from its previous position.

Provide feedback

---

Play

Sets [VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to true, playing the
[VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) from the current [VideoFrame.TimePosition](/docs/reference/engine/classes/VideoFrame#TimePosition).

VideoFrame:Play():()

Returns

()

Sets [VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to true, playing the
[VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) from the current [VideoFrame.TimePosition](/docs/reference/engine/classes/VideoFrame#TimePosition).
To save resources and improve performance, set the
[VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) property to "" when the [VideoFrame](/docs/reference/engine/classes/VideoFrame) is
not visible or in use.

Code Samples

Creating and Playing a Video

The code sample below demonstrates how to create and play a VideoFrame with
some valid asset ID after the video has loaded.

```
local screenPart = Instance.new("Part")



screenPart.Parent = workspace



local surfaceGui = Instance.new("SurfaceGui")



surfaceGui.Parent = screenPart



local videoFrame = Instance.new("VideoFrame")



videoFrame.Parent = surfaceGui



videoFrame.Looped = true



videoFrame.Video = "rbxassetid://" -- add an asset ID to this



while not videoFrame.IsLoaded do



task.wait()



end



videoFrame:Play()
```

Provide feedback

---

Events

DidLoop

Fires whenever the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) loops.

VideoFrame.DidLoop(video:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| video:[string](/docs/luau/strings)  The content ID of the video that looped. |

An event that fires whenever the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) loops. Returns
the content ID of the video.

Provide feedback

---

Ended

Fires when the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) has completed playback and
stopped.

VideoFrame.Ended(video:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| video:[string](/docs/luau/strings)  The content ID of the paused that ended. |

This event fires when the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) has completed playback
and stopped.

Provide feedback

---

Loaded

Fires when the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is loaded.

VideoFrame.Loaded(video:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| video:[string](/docs/luau/strings)  The content ID of the loaded video. |

This event fires when the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is loaded.

Provide feedback

---

Paused

This event fires whenever the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is paused using
[VideoFrame:Pause()](/docs/reference/engine/classes/VideoFrame#Pause) or by setting [VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to
false.

VideoFrame.Paused(video:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| video:[string](/docs/luau/strings)  The content ID of the paused video. |

This event fires whenever the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is paused using
[VideoFrame:Pause()](/docs/reference/engine/classes/VideoFrame#Pause) or by setting [VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to
false.

Provide feedback

---

Played

Fires whenever the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is played using the
[VideoFrame:Play()](/docs/reference/engine/classes/VideoFrame#Play) function or by setting
[VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to true.

VideoFrame.Played(video:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| video:[string](/docs/luau/strings)  The content ID of the played video. |

This event fires whenever the [VideoFrame.Video](/docs/reference/engine/classes/VideoFrame#Video) is played using the
[VideoFrame:Play()](/docs/reference/engine/classes/VideoFrame#Play) function or by setting
[VideoFrame.Playing](/docs/reference/engine/classes/VideoFrame#Playing) to true.

Provide feedback

---