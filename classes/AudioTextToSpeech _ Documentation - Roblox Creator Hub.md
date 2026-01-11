# AudioTextToSpeech | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioTextToSpeech
Scraped: 2026-01-11T02:35:47.427501Z

## Tags
- Not Replicated

## Inherits
- Instance
- AudioTextToSpeech
- Wire
- Object
- Wires
- IsLoaded
- Play()
- Pause()
- TimeLength
- TimePosition
- Looped
- AudioTextToSpeech:GetPropertyChangedSignal()
- IsPlaying
- Looping
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech)

English

Feedback

Engine Class

![AudioTextToSpeech](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioTextToSpeech-Dark.webp)AudioTextToSpeech

Plays text as speech audio.

---

Summary

Properties

|  |
| --- |
| [IsLoaded](#IsLoaded):[boolean](/docs/luau/booleans) |
| [IsPlaying](#IsPlaying):[boolean](/docs/luau/booleans) |
| [Looping](#Looping):[boolean](/docs/luau/booleans) |
| [Pitch](#Pitch):[number](/docs/luau/numbers) |
| [PlaybackSpeed](#PlaybackSpeed):[number](/docs/luau/numbers) |
| [Speed](#Speed):[number](/docs/luau/numbers) |
| [Text](#Text):[string](/docs/luau/strings) |
| [TimeLength](#TimeLength):[number](/docs/luau/numbers) |
| [TimePosition](#TimePosition):[number](/docs/luau/numbers) |
| [VoiceId](#VoiceId):[string](/docs/luau/strings) |
| [Volume](#Volume):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetWaveformAsync](#GetWaveformAsync)(timeRange: [NumberRange](/docs/reference/engine/datatypes/NumberRange),samples: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [LoadAsync](#LoadAsync)():[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) |
| [Pause](#Pause)():() |
| [Play](#Play)():() |
| [Unload](#Unload)():() |

Events

|  |
| --- |
| [Ended](#Ended)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Looped](#Looped)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) is used to play text as speech audio. It provides a
single Output pin which can be connected to other pins via
[Wires](/docs/reference/engine/classes/Wire).

Roblox uses the following formula to throttle requests for this API based on
the number of players in your experience:
max requests per minute per experience = 1 + (6 \* number\_of\_concurrent\_users).
You can purchase additional usage using
[Extended Services](/docs/cloud-services/extended-services).

For a more in-depth look, see
[Text-to-speech](/docs/audio/objects#text-to-speech).

Code Samples

Outputting Text as Speech

```
local audioTextToSpeech: AudioTextToSpeech = Instance.new("AudioTextToSpeech")



audioTextToSpeech.Parent = workspace



audioTextToSpeech.Text = "Hello! Converting text into speech is fun!"



audioTextToSpeech.VoiceId = "1"



local deviceOutput = Instance.new("AudioDeviceOutput")



deviceOutput.Parent = workspace



local wire = Instance.new("Wire")



wire.Parent = workspace



wire.SourceInstance = audioTextToSpeech



wire.TargetInstance = deviceOutput



local count = 0



local connection = nil



connection = audioTextToSpeech.Ended:Connect(function()



audioTextToSpeech.Text = "I can count to " .. count .. " because I am very smart"



audioTextToSpeech.VoiceId = "2"



audioTextToSpeech.TimePosition = 0



audioTextToSpeech:Play()



count += 1



if count > 10 then



connection:Disconnect()



end



end)



audioTextToSpeech:Play()
```

---

API Reference

Properties

IsLoaded

Read Only

Not Replicated

Read Parallel

Denotes whether the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object is loaded, buffered,
and ready to play.

AudioTextToSpeech.IsLoaded:[boolean](/docs/luau/booleans)

Denotes whether the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object is loaded, buffered,
and ready to play. Although uncommon, [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) objects
may have their assets unloaded at runtime if there is extreme memory
pressure, in which case [IsLoaded](/docs/reference/engine/classes/AudioTextToSpeech#IsLoaded) will
become false.

Provide feedback

---

IsPlaying

Roblox Security

Read Parallel

Denotes whether the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object is currently playing.

AudioTextToSpeech.IsPlaying:[boolean](/docs/luau/booleans)

Denotes whether the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object is currently playing.
This property is read-only, but replicates. To play and stop an
[AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object at runtime, use the
[Play()](/docs/reference/engine/classes/AudioTextToSpeech#Play) and
[Pause()](/docs/reference/engine/classes/AudioTextToSpeech#Pause) methods.

Provide feedback

---

Looping

Read Parallel

Controls whether the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object loops.

AudioTextToSpeech.Looping:[boolean](/docs/luau/booleans)

Controls whether the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object loops when exceeding
the end of its [TimeLength](/docs/reference/engine/classes/AudioTextToSpeech#TimeLength).

Provide feedback

---

Pitch

Read Parallel

Controls the pitch of the generated speech audio, which will be
independent of its speed.

AudioTextToSpeech.Pitch:[number](/docs/luau/numbers)

A value in musical semitones. The pitch of the generated speech audio is
shifted from its default value by AudioTextToSpeech.Pitch semitones.
Ranges from -12.0 to 12.0.

Provide feedback

---

PlaybackSpeed

Read Parallel

Controls how quickly the speech audio will be played, which controls its
pitch.

AudioTextToSpeech.PlaybackSpeed:[number](/docs/luau/numbers)

Multiplier controlling how quickly the speech audio will be played,
directly controlling its perceived pitch. Ranges from 0 to 20.

Provide feedback

---

Speed

Read Parallel

Controls the speed of the generated speech audio, which will be
independent of its pitch.

AudioTextToSpeech.Speed:[number](/docs/luau/numbers)

Multiplier controlling the speed of the generated speech audio. Ranges
from 0.5 to 2.0.

Provide feedback

---

Text

Read Parallel

The text to be converted into speech audio by [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech).

AudioTextToSpeech.Text:[string](/docs/luau/strings)

The text to be converted into speech audio by [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech).
The text has a maximum length of 300 characters.

Provide feedback

---

TimeLength

Read Only

Not Replicated

Read Parallel

Denotes the length of the generated speech audio.

AudioTextToSpeech.TimeLength:[number](/docs/luau/numbers)

Denotes the generated speech audio in seconds.

Provide feedback

---

TimePosition

Read Parallel

Tracks the current position of the playhead within the generated speech
audio.

AudioTextToSpeech.TimePosition:[number](/docs/luau/numbers)

Tracks and controls the current position of the playhead within the
generated speech audio, in seconds.

Provide feedback

---

VoiceId

Read Parallel

The voice style to be used by [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech).

AudioTextToSpeech.VoiceId:[string](/docs/luau/strings)

The voice style to be used by[AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech). A list of
available voices and their corresponding VoiceIds can be found in the
[text-to-speech guide](/docs/audio/objects#text-to-speech).

Provide feedback

---

Volume

Read Parallel

Controls how loudly the generated speech audio will be played.

AudioTextToSpeech.Volume:[number](/docs/luau/numbers)

Volume level which is multiplied onto the output audio stream, controlling
how loudly the generated speech audio will be played. Ranges from 0 to 3.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioTextToSpeech:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) has one "Output" pin.

Provide feedback

---

GetWaveformAsync

Yields

AudioTextToSpeech:GetWaveformAsync(

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

LoadAsync

Yields

Generates speech audio.

AudioTextToSpeech:LoadAsync():[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)

Returns

[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)

A blocking call that begins the generation of speech audio based on the
current parameters. It will yield until the speech generation either
completes or fails. Status is returned by an AssetFetchStatus value.

Provide feedback

---

Pause

Pauses the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object wherever its
[TimePosition](/docs/reference/engine/classes/AudioTextToSpeech#TimePosition) is.

AudioTextToSpeech:Pause():()

Returns

()

Pauses the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object wherever its
[TimePosition](/docs/reference/engine/classes/AudioTextToSpeech#TimePosition) is. Replicates from
server to client.

Provide feedback

---

Play

Plays the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) from wherever its
[TimePosition](/docs/reference/engine/classes/AudioTextToSpeech#TimePosition) is.

AudioTextToSpeech:Play():()

Returns

()

Plays the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) from wherever its
[TimePosition](/docs/reference/engine/classes/AudioTextToSpeech#TimePosition) is. Replicates from
server to client.

Provide feedback

---

Unload

Unload the generated speech audio.

AudioTextToSpeech:Unload():()

Returns

()

Frees resources by unloading the generated speech audio.

Provide feedback

---

Events

Ended

Fires when the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object has completed playback and
paused.

AudioTextToSpeech.Ended():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires after the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object has completed playback
and paused. Note this event will not fire for audio with
[Looped](/docs/reference/engine/classes/AudioTextToSpeech#Looped) set to true since it continues
playing upon reaching its end. This event will also not fire when the
audio is paused before playback has completed; for this, use
[AudioTextToSpeech:GetPropertyChangedSignal()](/docs/reference/engine/classes/AudioTextToSpeech#GetPropertyChangedSignal) on the
[IsPlaying](/docs/reference/engine/classes/AudioTextToSpeech#IsPlaying) property.

This event may be used to destroy an [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object when
it has completed playback.

Provide feedback

---

Looped

Fires when the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object loops.

AudioTextToSpeech.Looped():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Event that fires after the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) object loops. This
happens when the audio reaches the end of its content and
[Looping](/docs/reference/engine/classes/AudioTextToSpeech#Looping) is true.

This event does not fire if the audio is looped manually by changing
its [TimePosition](/docs/reference/engine/classes/AudioTextToSpeech#TimePosition).

Provide feedback

---

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) via a [Wire](/docs/reference/engine/classes/Wire).

AudioTextToSpeech.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech) and to some other wirable instance.

Provide feedback

---