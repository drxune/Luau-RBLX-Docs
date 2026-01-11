# AudioFilter | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioFilter
Scraped: 2026-01-11T02:40:26.337492Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- AudioFilter
- Wire
- Wires
- FilterType
- Gain
- Q
- Frequency
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioFilter](/docs/reference/engine/classes/AudioFilter)

English

Feedback

Engine Class

![AudioFilter](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioFilter-Dark.webp)AudioFilter

Adjusts the frequency content of audio streams.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Editor](#Editor):[boolean](/docs/luau/booleans) |
| [FilterType](#FilterType):[Enum.AudioFilterType](/docs/reference/engine/enums/AudioFilterType) |
| [Frequency](#Frequency):[number](/docs/luau/numbers) |
| [Gain](#Gain):[number](/docs/luau/numbers) |
| [Q](#Q):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetGainAt](#GetGainAt)(frequency: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioFilter](/docs/reference/engine/classes/AudioFilter) adjusts the frequency content of audio streams. It
provides one Input pin and one Output pin which can be connected
to/from by [Wires](/docs/reference/engine/classes/Wire). [AudioFilter](/docs/reference/engine/classes/AudioFilter) uses its
[FilterType](/docs/reference/engine/classes/AudioFilter#FilterType), [Gain](/docs/reference/engine/classes/AudioFilter#Gain), and
[Q](/docs/reference/engine/classes/AudioFilter#Q) properties to determine what to do around a particular
cutoff [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency).

Code Samples

Emitter Filtering

An AudioFilter can be used to change the frequency content of audio streams.
In this example, an AudioFilter is used to make the AudioEmitter
output more muffled when there's a wall between it and the AudioListener.

```
-- This assumes the workspace contains a Part with an AudioEmitter and an AudioPlayer, and the camera has an AudioListener



local RunService = game:GetService("RunService")



local part: BasePart = workspace.Part



local camera: Camera = workspace.CurrentCamera



local audioPlayer: AudioPlayer = part.AudioPlayer



local audioEmitter: AudioEmitter = part.AudioEmitter



local audioListener: AudioListener = camera.AudioListener



local raycastParams = RaycastParams.new()



raycastParams.FilterDescendantsInstances = { audioEmitter.Parent }



raycastParams.FilterType = Enum.RaycastFilterType.Exclude



-- Create a new AudioFilter



local filter: AudioFilter = Instance.new("AudioFilter")



filter.FilterType = Enum.AudioFilterType.Lowpass12dB



filter.Frequency = 22000



filter.Q = math.sqrt(2) / 2 -- This Q value produces a flat lowpass for the 12dB slope type



filter.Parent = part



-- Put the AudioFilter between the player and the emitter



local function wireTo(source: Instance, target: Instance): Wire



local wire = Instance.new("Wire")



wire.SourceInstance = source



wire.TargetInstance = target



wire.Parent = target



end



wireTo(audioPlayer, filter)



wireTo(filter, audioEmitter)



-- Update the filter based on the positions of the emitter and listener



RunService.Heartbeat:Connect(function()



local emitterPos: Vector3 = part.Position



local listenerPos: Vector3 = camera.CFrame.Position



local raycastResult = workspace:Raycast(emitterPos, (listenerPos - emitterPos), raycastParams)



filter.Frequency = if raycastResult then 500 else 22000



end)
```

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioFilter.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

Editor

Not Replicated

Roblox Script Security

Read Parallel

AudioFilter.Editor:[boolean](/docs/luau/booleans)

Provide feedback

---

FilterType

Read Parallel

The curve type of the band represented by the filter.

AudioFilter.FilterType:[Enum.AudioFilterType](/docs/reference/engine/enums/AudioFilterType)

The type of frequency response curve that will be used to filter the audio
signal. Each type of curve affects the frequency content of the audio in
different ways.

Provide feedback

---

Frequency

Read Parallel

The central frequency that the filter acts around.

AudioFilter.Frequency:[number](/docs/luau/numbers)

The central frequency in hertz of the curve represented by the filter.
Generally, adjusting this value up or down corresponds to a horizontal
shift in the overall frequency curve. Ranges from 20 to 22000.

Provide feedback

---

Gain

Read Parallel

For peaking and shelving filters, controls volume increase or reduction.

AudioFilter.Gain:[number](/docs/luau/numbers)

The gain value in decibels used to determine the volume level of the curve
represented by the filter. Only applies when the
[FilterType](/docs/reference/engine/classes/AudioFilter) is Peak, LowShelf, or HighShelf.
Ranges from -30 to 30.

Provide feedback

---

Q

Read Parallel

For peaking, lowpass, highpass, bandpass, and notch filters, controls the
selectiveness or resonance.

AudioFilter.Q:[number](/docs/luau/numbers)

The quality value used to determine the slope or resonance of the curve
represented by the filter. Only applies when the
[FilterType](/docs/reference/engine/classes/AudioFilter) is Peak, Lowpass[x]dB, Highpass[x]dB,
Bandpass, or Notch. Ranges from 0.1 to 10.

For [FilterType](/docs/reference/engine/classes/AudioFilter) values of
[Lowpass12dB](/docs/reference/engine/enums/AudioFilterType#Lowpass12dB) and
[Highpass12dB](/docs/reference/engine/enums/AudioFilterType#Highpass12dB), a Q value of
sqrt(2) / 2, or 0.707, corresponds to a flat filter at a 12dB/octave
slope.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioFilter:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioFilter](/docs/reference/engine/classes/AudioFilter) has one "Input" pin and one "Output" pin.

Provide feedback

---

GetGainAt

Returns the magnitude response of the filter at the given frequency.

AudioFilter:GetGainAt(frequency:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| frequency:[number](/docs/luau/numbers)  The frequency, in hertz, to sample. |

Returns

[number](/docs/luau/numbers)

The gain value, in decibels, at the given frequency.

Returns the gain value, in decibels, of the frequency response curve
represented by the filter at the given frequency, in hertz. This can be
used to sample the exact shape of the filter in key places or as a whole.

Provide feedback

---

GetInputPins

AudioFilter:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioFilter:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioFilter](/docs/reference/engine/classes/AudioFilter) via a [Wire](/docs/reference/engine/classes/Wire).

AudioFilter.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioFilter](/docs/reference/engine/classes/AudioFilter) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioFilter](/docs/reference/engine/classes/AudioFilter) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioFilter](/docs/reference/engine/classes/AudioFilter) and to some other wirable instance.

Provide feedback

---