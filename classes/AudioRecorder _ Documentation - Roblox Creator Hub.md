# AudioRecorder | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioRecorder
Scraped: 2026-01-11T02:38:11.477157Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- AudioRecorder
- Wire
- AudioPlayer
- AudioDeviceInput
- GetUnrecordableInstancesAsync()
- Clear()
- CanRecordAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioRecorder](/docs/reference/engine/classes/AudioRecorder)

English

Feedback

Engine Class

![AudioRecorder](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioRecorder-Dark.webp)AudioRecorder

Records audio streams in-experience.

Not Browsable

---

Summary

Properties

|  |
| --- |
| [IsRecording](#IsRecording):[boolean](/docs/luau/booleans) |
| [TimeLength](#TimeLength):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [CanRecordAsync](#CanRecordAsync)():[boolean](/docs/luau/booleans) |
| [Clear](#Clear)():() |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |
| [GetTemporaryContent](#GetTemporaryContent)():[Content](/docs/reference/engine/datatypes/Content) |
| [GetUnrecordableInstancesAsync](#GetUnrecordableInstancesAsync)():Instances |
| [RecordAsync](#RecordAsync)():() |
| [Stop](#Stop)():() |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This API is in development and is not available yet.

AudioRecorder records audio streams in-experience with a fixed time limit of
60 seconds. The results can be loaded into an [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) for
playback.

At this time, [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) cannot be recorded. The
[GetUnrecordableInstancesAsync()](/docs/reference/engine/classes/AudioRecorder#GetUnrecordableInstancesAsync)
method can be used to check specifically which instances aren't recordable.

Code Samples

Audio Recorder

```
local Workspace = game:GetService("Workspace")



local audioRecorder = Instance.new("AudioRecorder")



audioRecorder.Parent = Workspace



local audioPlayer = Instance.new("AudioPlayer")



audioPlayer.Asset = "rbxassetid://5829815715"



audioPlayer.Volume = 0.8



audioPlayer.Parent = Workspace



-- Wire AudioPlayer into the AudioRecorder



local wire1 = Instance.new("Wire")



wire1.SourceInstance = audioPlayer



wire1.TargetInstance = audioRecorder



wire1.Parent = audioRecorder



-- There is no exact way to determine when audio buffer enters in to trigger the recording properly



-- Recording will have pre-head empty silence compared to the original asset



audioPlayer:Play()



audioRecorder:RecordAsync() -- Start recording the AudioPlayer



print("Recording...")



task.wait(5)



audioRecorder:Stop() -- Stop recording



print("Stopped recording!")



audioPlayer:Stop()



audioPlayer.TimePosition = 0



-- Create output to listen the results



local audioOutput = Instance.new("AudioDeviceOutput")



audioOutput.Parent = Workspace



local wire2 = Instance.new("Wire")



wire2.SourceInstance = audioPlayer



wire2.TargetInstance = audioOutput



wire2.Parent = audioOutput



-- Get the recorded content and play it in the AudioPlayer



local resultUri = audioRecorder:GetTemporaryContent().Uri



audioPlayer.Asset = resultUri



if not audioPlayer.IsReady then



audioPlayer:GetPropertyChangedSignal("IsReady"):Wait()



end



audioPlayer:Play()
```

---

API Reference

Properties

IsRecording

Roblox Security

Read Parallel

AudioRecorder.IsRecording:[boolean](/docs/luau/booleans)

Returns whether the AudioRecorder is currently recording.

Provide feedback

---

TimeLength

Read Only

Not Replicated

Read Parallel

AudioRecorder.TimeLength:[number](/docs/luau/numbers)

Returns the current length of the recording in seconds.

Provide feedback

---

Methods

CanRecordAsync

Yields

AudioRecorder:CanRecordAsync():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Returns whether the AudioRecorder can currently record. For instance,
this will return false if the current recording data has reached the
recording time limit. To clear the recording, use
[Clear()](/docs/reference/engine/classes/AudioRecorder#Clear).

Provide feedback

---

Clear

AudioRecorder:Clear():()

Returns

()

Clears out the recording from the AudioRecorder.

Provide feedback

---

GetConnectedWires

AudioRecorder:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Provide feedback

---

GetInputPins

AudioRecorder:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioRecorder:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetTemporaryContent

AudioRecorder:GetTemporaryContent():[Content](/docs/reference/engine/datatypes/Content)

Returns

[Content](/docs/reference/engine/datatypes/Content)

Returns recorded content that can be played back with [AudioPlayer](/docs/reference/engine/classes/AudioPlayer).
The content retrieved from this method is only valid in the current
session.

Provide feedback

---

GetUnrecordableInstancesAsync

Yields

AudioRecorder:GetUnrecordableInstancesAsync():Instances

Returns

Instances

Traverses the audio graph, starting from this recorder's inputs, to find
unrecordable instances. Currently, [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) is not
recordable.

Provide feedback

---

RecordAsync

Yields

AudioRecorder:RecordAsync():()

Returns

()

If [CanRecordAsync()](/docs/reference/engine/classes/AudioRecorder#CanRecordAsync) returns true,
recording begins. If recording cannot begin, this method produces an
error.

Provide feedback

---

Stop

AudioRecorder:Stop():()

Returns

()

Stops recording.

Provide feedback

---

Events

WiringChanged

AudioRecorder.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans) |
| pin:[string](/docs/luau/strings) |
| wire:[Wire](/docs/reference/engine/classes/Wire) |
| instance:[Instance](/docs/reference/engine/datatypes/Instance) |

Provide feedback

---