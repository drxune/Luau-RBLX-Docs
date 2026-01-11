# VideoPlayer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VideoPlayer
Scraped: 2026-01-11T02:38:27.389467Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- VideoPlayer
- Wire
- VideoDisplay
- VideoContent
- AutoLoadInStudio
- Play()
- Pause()
- TimeLength
- Unload()
- Wires
- TimePosition
- VideoPlayer.VideoContent
- IsLoaded
- LoadAsync()
- Looped
- VideoPlayer:GetPropertyChangedSignal()
- IsPlaying
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [VideoPlayer](/docs/reference/engine/classes/VideoPlayer)

English

Feedback

Engine Class

![VideoPlayer](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/VideoPlayer-Dark.webp)VideoPlayer

Used to play video assets.

Not Browsable

---

Summary

Properties

|  |
| --- |
| [AutoLoadInStudio](#AutoLoadInStudio):[boolean](/docs/luau/booleans) |
| [AutoPlayInStudio](#AutoPlayInStudio):[boolean](/docs/luau/booleans) |
| [IsLoaded](#IsLoaded):[boolean](/docs/luau/booleans) |
| [IsPlaying](#IsPlaying):[boolean](/docs/luau/booleans) |
| [Looping](#Looping):[boolean](/docs/luau/booleans) |
| [PlaybackSpeed](#PlaybackSpeed):[number](/docs/luau/numbers) |
| [Resolution](#Resolution):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [TimeLength](#TimeLength):[number](/docs/luau/numbers) |
| [TimePosition](#TimePosition):[number](/docs/luau/numbers) |
| [VideoContent](#VideoContent):[Content](/docs/reference/engine/datatypes/Content) |
| [Volume](#Volume):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |
| [LoadAsync](#LoadAsync)():[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) |
| [Pause](#Pause)():() |
| [Play](#Play)():() |
| [Unload](#Unload)():() |

Events

|  |
| --- |
| [DidEnd](#DidEnd)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DidLoop](#DidLoop)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PlayFailed](#PlayFailed)(error: [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An instance for playing video assets. It can be connected to a
[VideoDisplay](/docs/reference/engine/classes/VideoDisplay) via a [Wire](/docs/reference/engine/classes/Wire) to show the video and can be connected
to audio instances via a [Wire](/docs/reference/engine/classes/Wire) to play the audio track.

Code Samples

Video Player (Server Side)

```
-- This should be in a "Script" with RunContext set to "Legacy" or "Server"



-- Create what the video is displayed on



local videoScreenPart = Instance.new("Part")



videoScreenPart.Anchored = true



videoScreenPart.Size = Vector3.new(12, 6, 1)



videoScreenPart.CFrame = CFrame.new(0, 5, 0)



videoScreenPart.Parent = workspace



local videoScreenUI = Instance.new("SurfaceGui")



videoScreenUI.Parent = videoScreenPart



local videoDisplay = Instance.new("VideoDisplay")



videoDisplay.Size = UDim2.new(1, 0, 1, 0)



videoDisplay.Parent = videoScreenUI



-- Create where a video asset originates from



local videoSource = Instance.new("VideoPlayer")



videoSource.VideoContent = Content.fromUri("rbxassetid://5608359401")



videoSource.Looping = true



videoSource.Parent = videoScreenPart



-- Create where the video's audio emits from



local speakerPart = Instance.new("Part")



speakerPart.Anchored = true



speakerPart.Parent = workspace



local audioEmitter = Instance.new("AudioEmitter")



audioEmitter.Parent = speakerPart



-- Create and connect wires so that the video visually renders and emits audio



local videoWire = Instance.new("Wire")



videoWire.SourceInstance = videoSource



videoWire.TargetInstance = videoDisplay



videoWire.Parent = videoSource



local audioWire = Instance.new("Wire")



audioWire.SourceInstance = videoSource



audioWire.TargetInstance = audioEmitter



audioWire.Parent = videoSource



-- Play the video



-- Note: Playing a video on the server does not guarantee it is loaded or synced for all clients, playing on the client is preferred



videoSource:Play()
```

Video Player (Client Side)

```
-- This should be in either a "LocalScript" or "Script" with RunContext set to "Client"



-- Same code as above sample until the "Play the video" section



-- Play the video after it has loaded



videoSource:GetPropertyChangedSignal("IsLoaded"):Connect(function()



if videoSource.IsLoaded then



print("Video has loaded, starting playback in 2 seconds.")



wait(2)



videoSource:Play()



end



end)



-- Load the video to have it ready when we need it



videoSource:LoadAsync()



wait(5)



-- Unload the video to save resources



videoSource:Unload()
```

---

API Reference

Properties

AutoLoadInStudio

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

Loads the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) while in Studio
Edit mode.

VideoPlayer.AutoLoadInStudio:[boolean](/docs/luau/booleans)

By default, [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) does not load
while in Studio Edit mode and shows no output when wired to
[VideoDisplay](/docs/reference/engine/classes/VideoDisplay) to reduce studio memory usage. Toggle this option to
load [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) while in Studio Edit
mode.

Provide feedback

---

AutoPlayInStudio

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

Plays the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) while in Studio
Edit mode.

VideoPlayer.AutoPlayInStudio:[boolean](/docs/luau/booleans)

Plays the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) while in Studio
Edit mode. [AutoLoadInStudio](/docs/reference/engine/classes/VideoPlayer#AutoLoadInStudio) must be
on for this option to show.

Provide feedback

---

IsLoaded

Read Only

Not Replicated

Read Parallel

Indicates when the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) has
loaded and is ready to play.

VideoPlayer.IsLoaded:[boolean](/docs/luau/booleans)

This property is true when the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) has loaded and is ready to
play.

Provide feedback

---

IsPlaying

Read Only

Not Replicated

Read Parallel

Denotes whether this [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) is currently playing.

VideoPlayer.IsPlaying:[boolean](/docs/luau/booleans)

Denotes whether this [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) is currently playing. This
property is read-only, but replicates. To play and pause a
[VideoPlayer](/docs/reference/engine/classes/VideoPlayer) at runtime, use the [Play()](/docs/reference/engine/classes/VideoPlayer#Play)
and [Pause()](/docs/reference/engine/classes/VideoPlayer#Pause) methods.

Provide feedback

---

Looping

Read Parallel

Controls whether this [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) loops.

VideoPlayer.Looping:[boolean](/docs/luau/booleans)

Controls whether this [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) loops after reaching the end of
its [TimeLength](/docs/reference/engine/classes/VideoPlayer#TimeLength).

Provide feedback

---

PlaybackSpeed

Read Parallel

Controls the speed at which the video is played.

VideoPlayer.PlaybackSpeed:[number](/docs/luau/numbers)

Multiplier that controls how quickly the video plays, directly controlling
the perceived pitch of the audio track. Ranges from 0 to 1.

Provide feedback

---

Resolution

Read Only

Not Replicated

Read Parallel

Gets the original source resolution of the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) file.

VideoPlayer.Resolution:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property gets the original source resolution of the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) file.

Provide feedback

---

TimeLength

Read Only

Not Replicated

Read Parallel

Indicates the length of the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent)
in seconds.

VideoPlayer.TimeLength:[number](/docs/luau/numbers)

This property indicates the length of the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) in seconds. If the video is
not loaded, this value is 0.

Provide feedback

---

TimePosition

Read Parallel

Indicates the progress in seconds of the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent).

VideoPlayer.TimePosition:[number](/docs/luau/numbers)

This property indicates the progress in seconds of the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent). It can be changed to move
the playback position of the video both before and during playback.

Provide feedback

---

VideoContent

Read Parallel

The asset to be loaded into the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer).

VideoPlayer.VideoContent:[Content](/docs/reference/engine/datatypes/Content)

The content ID of the video file a [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) object is
associated with. To save resources and improve performance, call the
[Unload()](/docs/reference/engine/classes/VideoPlayer#Unload) method to unload the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) when the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer)
is not visible or in use.

Provide feedback

---

Volume

Read Parallel

Controls how loudly the audio track will be played.

VideoPlayer.Volume:[number](/docs/luau/numbers)

Volume level, which is multiplied onto the output audio stream,
controlling how loudly the audio track plays. Ranges from 0 to 3.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

VideoPlayer:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) has one "Output" pin.

Provide feedback

---

GetInputPins

VideoPlayer:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

VideoPlayer:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

LoadAsync

Yields

Loads the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) before it is
played.

VideoPlayer:LoadAsync():[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)

Returns

[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)

[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) is typically only loaded
when [Play()](/docs/reference/engine/classes/VideoPlayer#Play) is called, causing some buffering
delay. This function can preload
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) so that it can be
immediately played when [Play()](/docs/reference/engine/classes/VideoPlayer#Play) is called.
Loading videos can consume a significant amount of device memory.

Provide feedback

---

Pause

Pauses the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) wherever its
[TimePosition](/docs/reference/engine/classes/VideoPlayer#TimePosition) is.

VideoPlayer:Pause():()

Returns

()

Pauses the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) wherever its
[TimePosition](/docs/reference/engine/classes/VideoPlayer#TimePosition) is. Replicates from server
to client.

Provide feedback

---

Play

Plays the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) from wherever its
[TimePosition](/docs/reference/engine/classes/VideoPlayer#TimePosition) is.

VideoPlayer:Play():()

Returns

()

Plays the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) from wherever its
[TimePosition](/docs/reference/engine/classes/VideoPlayer#TimePosition) is. Replicates from server
to client. To save resources and improve performance, call the
[Unload()](/docs/reference/engine/classes/VideoPlayer#Unload) method to unload the
[VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) when the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer)
is not visible or in use.

Provide feedback

---

Unload

Unloads the [VideoPlayer.VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) to save resources.

VideoPlayer:Unload():()

Returns

()

Unloads the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) to save
resources. After calling this method, the
[IsLoaded](/docs/reference/engine/classes/VideoPlayer#IsLoaded) property is false, and the
[TimePosition](/docs/reference/engine/classes/VideoPlayer#TimePosition) resets to 0. To play the
video again, the [LoadAsync()](/docs/reference/engine/classes/VideoPlayer#LoadAsync) or
[Play()](/docs/reference/engine/classes/VideoPlayer#Play) method must be called to reload the
video.

Provide feedback

---

Events

DidEnd

Fires when the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) has completed
playback and stopped.

VideoPlayer.DidEnd():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires after the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) has completed playback and stopped.
Note this event does not fire for videos with
[Looped](/docs/reference/engine/classes/VideoPlayer#Looped) set to true since it continues playing
upon reaching its end. This event also does not fire when the video is
stopped before playback has completed; for this, use
[VideoPlayer:GetPropertyChangedSignal()](/docs/reference/engine/classes/VideoPlayer#GetPropertyChangedSignal) on the
[IsPlaying](/docs/reference/engine/classes/VideoPlayer#IsPlaying) property.

Provide feedback

---

DidLoop

Fires when the [VideoContent](/docs/reference/engine/classes/VideoPlayer#VideoContent) loops.

VideoPlayer.DidLoop():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Event that fires after the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) loops. This happens when
the video reaches the end of its content. This event does not fire if
the video is looped manually by changing its
[TimePosition](/docs/reference/engine/classes/VideoPlayer#TimePosition).

Provide feedback

---

PlayFailed

VideoPlayer.PlayFailed(error:[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| error:[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) |

Provide feedback

---

WiringChanged

Fires when another instance is connected to or disconnected from the
[VideoPlayer](/docs/reference/engine/classes/VideoPlayer) via a [Wire](/docs/reference/engine/classes/Wire).

VideoPlayer.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance was connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [VideoPlayer](/docs/reference/engine/classes/VideoPlayer) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[VideoPlayer](/docs/reference/engine/classes/VideoPlayer) and to some other wirable instance.

Provide feedback

---