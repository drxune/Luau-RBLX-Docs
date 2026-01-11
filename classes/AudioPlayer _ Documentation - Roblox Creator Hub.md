# AudioPlayer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioPlayer
Scraped: 2026-01-11T02:30:24.834531Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- AudioPlayer
- Wire
- Wires
- AutoLoad
- IsReady
- Asset
- DataModel
- AudioPlayers
- Play()
- Stop()
- TimeLength
- LoopRegion
- PlaybackRegion
- TimePosition
- Looped
- AudioPlayer:GetPropertyChangedSignal()
- IsPlaying
- Looping
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioPlayer](/docs/reference/engine/classes/AudioPlayer)

English

Feedback

Engine Class

![AudioPlayer](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioPlayer-Dark.webp)AudioPlayer

Used to play audio assets.

---

Summary

Properties

|  |
| --- |
| [Asset](#Asset):ContentId |
| [AssetId](#AssetId):[string](/docs/luau/strings)  Deprecated |
| [AudioContent](#AudioContent):[Content](/docs/reference/engine/datatypes/Content) |
| [AutoLoad](#AutoLoad):[boolean](/docs/luau/booleans) |
| [AutoPlay](#AutoPlay):[boolean](/docs/luau/booleans) |
| [IsMutedForCapture](#IsMutedForCapture):[boolean](/docs/luau/booleans) |
| [IsPlaying](#IsPlaying):[boolean](/docs/luau/booleans) |
| [IsReady](#IsReady):[boolean](/docs/luau/booleans) |
| [Looping](#Looping):[boolean](/docs/luau/booleans) |
| [LoopRegion](#LoopRegion):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [PlaybackRegion](#PlaybackRegion):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [PlaybackSpeed](#PlaybackSpeed):[number](/docs/luau/numbers) |
| [TimeLength](#TimeLength):[number](/docs/luau/numbers) |
| [TimePosition](#TimePosition):[number](/docs/luau/numbers) |
| [Volume](#Volume):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |
| [GetWaveformAsync](#GetWaveformAsync)(timeRange: [NumberRange](/docs/reference/engine/datatypes/NumberRange),samples: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [Play](#Play)():() |
| [Stop](#Stop)():() |

Events

|  |
| --- |
| [Ended](#Ended)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Looped](#Looped)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioPlayer](/docs/reference/engine/classes/AudioPlayer) is used to play audio assets. It provides a single
Output pin which can be connected to other pins via [Wires](/docs/reference/engine/classes/Wire).

Code Samples

Outputting Audio to Device

```
local audioPlayer: AudioPlayer = Instance.new("AudioPlayer")



audioPlayer.Parent = workspace



audioPlayer.AssetId = "rbxassetid://9112854440"



local deviceOutput = Instance.new("AudioDeviceOutput")



deviceOutput.Parent = workspace



local wire = Instance.new("Wire")



wire.Parent = workspace



wire.SourceInstance = audioPlayer



wire.TargetInstance = deviceOutput



audioPlayer:Play()
```

---

API Reference

Properties

Asset

Read Parallel

The asset to be loaded into the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer).

AudioPlayer.Asset:ContentId

The asset to be loaded into the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer). If
[AutoLoad](/docs/reference/engine/classes/AudioPlayer#AutoLoad) is true, the asset loads
immediately once this property is assigned. When loading is complete,
[IsReady](/docs/reference/engine/classes/AudioPlayer#IsReady) becomes true.

Provide feedback

---

AssetId

Deprecated

Show details

---

AudioContent

Read Parallel

AudioPlayer.AudioContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

AutoLoad

Read Parallel

Controls whether [Asset](/docs/reference/engine/classes/AudioPlayer#Asset) loads automatically once
assigned.

AudioPlayer.AutoLoad:[boolean](/docs/luau/booleans)

Controls whether [Asset](/docs/reference/engine/classes/AudioPlayer#Asset) loads automatically once
assigned. If false, the asset will load upon the first attempt to play.

Provide feedback

---

AutoPlay

Read Parallel

Denotes whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) starts playing as soon as it
spawns in for the first time.

AudioPlayer.AutoPlay:[boolean](/docs/luau/booleans)

Denotes whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) starts playing as soon as it
enters the [DataModel](/docs/reference/engine/classes/DataModel) for the first time. This only applies to
[AudioPlayers](/docs/reference/engine/classes/AudioPlayer) that are created or deserialized locally,
and does not apply to [AudioPlayers](/docs/reference/engine/classes/AudioPlayer) generated via
replication. This property is primarily used at edit time in Studio to
have an [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) begin when entering a play session.

Provide feedback

---

IsMutedForCapture

Roblox Script Security

Read Parallel

AudioPlayer.IsMutedForCapture:[boolean](/docs/luau/booleans)

Provide feedback

---

IsPlaying

Roblox Security

Read Parallel

Denotes whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) is currently playing.

AudioPlayer.IsPlaying:[boolean](/docs/luau/booleans)

Denotes whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) is currently playing. This
property is read-only, but replicates. To play and stop an
[AudioPlayer](/docs/reference/engine/classes/AudioPlayer) at runtime, use the [Play()](/docs/reference/engine/classes/AudioPlayer#Play)
and [Stop()](/docs/reference/engine/classes/AudioPlayer#Stop) methods.

Provide feedback

---

IsReady

Read Only

Not Replicated

Read Parallel

Denotes whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) is loaded, buffered, and ready to
play.

AudioPlayer.IsReady:[boolean](/docs/luau/booleans)

Denotes whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) is loaded, buffered, and ready to
play. Although uncommon, [AudioPlayers](/docs/reference/engine/classes/AudioPlayer) may have their
assets unloaded at runtime if there is extreme memory pressure, in which
case [IsReady](/docs/reference/engine/classes/AudioPlayer#IsReady) will become false.

Provide feedback

---

Looping

Read Parallel

Controls whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) loops.

AudioPlayer.Looping:[boolean](/docs/luau/booleans)

Controls whether this [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) loops when exceeding the end of
its [TimeLength](/docs/reference/engine/classes/AudioPlayer#TimeLength),
[LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion), or
[PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion).

Provide feedback

---

LoopRegion

Read Parallel

A range, in seconds, denoting a desired loop start and loop end within the
[PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) of this
[AudioPlayer](/docs/reference/engine/classes/AudioPlayer).

AudioPlayer.LoopRegion:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

A range, in seconds, denoting a desired loop start and loop end within the
[PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) of this
[AudioPlayer](/docs/reference/engine/classes/AudioPlayer).

If the [LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) minimum is greater
than the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) minimum, the
loop starts from the [LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) minimum.

If the [LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) minimum is less than
the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) minimum, the loop
starts from the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) minimum.

If the [LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) maximum is greater
than the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) maximum, the
loop ends at the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion)
maximum.

If the [LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) maximum is less than
the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) maximum, the loop
ends at exactly the [LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) maximum.

If the [LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) minimum equals the
[LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) maximum, the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer)
uses the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) property
instead.

Provide feedback

---

PlaybackRegion

Read Parallel

Range in seconds denoting a desired start time (minimum) and stop time
(maximum) within the [TimeLength](/docs/reference/engine/classes/AudioPlayer#TimeLength).

AudioPlayer.PlaybackRegion:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

Range in seconds denoting a desired start time (minimum) and stop time
(maximum) within the [TimeLength](/docs/reference/engine/classes/AudioPlayer#TimeLength).

If the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) minimum is
greater than 0, the sound begins playing from the
[PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) minimum time.

If the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) minimum is
less than 0, the sound begins playing from 0.

If the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) maximum is
greater than the [TimeLength](/docs/reference/engine/classes/AudioPlayer#TimeLength), the sound
stops at [TimeLength](/docs/reference/engine/classes/AudioPlayer#TimeLength).

If the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) maximum is
less than the [TimeLength](/docs/reference/engine/classes/AudioPlayer#TimeLength), the sound
stops at exactly the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion)
maximum.

If the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) minimum
equals the [PlaybackRegion](/docs/reference/engine/classes/AudioPlayer#PlaybackRegion) maximum,
the sound plays in its entirety.

Provide feedback

---

PlaybackSpeed

Read Parallel

Controls how quickly the asset will be played, which controls its pitch.

AudioPlayer.PlaybackSpeed:[number](/docs/luau/numbers)

Multiplier controlling how quickly the asset will be played, directly
controlling its perceived pitch. Ranges from 0 to 20.

Provide feedback

---

TimeLength

Read Only

Not Replicated

Read Parallel

Denotes the length of the loaded asset.

AudioPlayer.TimeLength:[number](/docs/luau/numbers)

Denotes the length of the loaded [Asset](/docs/reference/engine/classes/AudioPlayer#Asset) in
seconds.

Provide feedback

---

TimePosition

Read Parallel

Tracks the current position of the playhead within the asset.

AudioPlayer.TimePosition:[number](/docs/luau/numbers)

Tracks and controls the current position of the playhead within the
[Asset](/docs/reference/engine/classes/AudioPlayer#Asset), in seconds.

Provide feedback

---

Volume

Read Parallel

Controls how loudly the asset will be played.

AudioPlayer.Volume:[number](/docs/luau/numbers)

Volume level which is multiplied onto the output audio stream, controlling
how loudly the asset will be played. Ranges from 0 to 3.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioPlayer:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) has one "Output" pin.

Provide feedback

---

GetInputPins

AudioPlayer:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioPlayer:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetWaveformAsync

Yields

AudioPlayer:GetWaveformAsync(

timeRange:[NumberRange](/docs/reference/engine/datatypes/NumberRange), samples:[number](/docs/luau/numbers)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| timeRange:[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| samples:[number](/docs/luau/numbers) |

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Play

Plays the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) from wherever its
[TimePosition](/docs/reference/engine/classes/AudioPlayer#TimePosition) is.

AudioPlayer:Play():()

Returns

()

Plays the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) from wherever its
[TimePosition](/docs/reference/engine/classes/AudioPlayer#TimePosition) is. Replicates from server
to client.

Provide feedback

---

Stop

Stops the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) wherever its
[TimePosition](/docs/reference/engine/classes/AudioPlayer#TimePosition) is.

AudioPlayer:Stop():()

Returns

()

Stops the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) wherever its
[TimePosition](/docs/reference/engine/classes/AudioPlayer#TimePosition) is. Replicates from server
to client.

Provide feedback

---

Events

Ended

Fires when the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) has completed playback and stopped.

AudioPlayer.Ended():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires after the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) has completed playback and stopped.
Note this event will not fire for audio with
[Looped](/docs/reference/engine/classes/AudioPlayer#Looped) set to true since it continues playing
upon reaching its end. This event will also not fire when the audio is
stopped before playback has completed; for this, use
[AudioPlayer:GetPropertyChangedSignal()](/docs/reference/engine/classes/AudioPlayer#GetPropertyChangedSignal) on the
[IsPlaying](/docs/reference/engine/classes/AudioPlayer#IsPlaying) property.

This event is often used to destroy an [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) when it has
completed playback.

Provide feedback

---

Looped

Fires when the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) loops.

AudioPlayer.Looped():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Event that fires after the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) loops. This happens when
the audio reaches the end of its content (or the end of the
[LoopRegion](/docs/reference/engine/classes/AudioPlayer#LoopRegion) if it is active) and
[Looping](/docs/reference/engine/classes/AudioPlayer#Looping) is true.

This event does not fire if the audio is looped manually by changing
its [TimePosition](/docs/reference/engine/classes/AudioPlayer#TimePosition).

Provide feedback

---

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioPlayer](/docs/reference/engine/classes/AudioPlayer) via a [Wire](/docs/reference/engine/classes/Wire).

AudioPlayer.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioPlayer](/docs/reference/engine/classes/AudioPlayer) and to some other wirable instance.

Provide feedback

---