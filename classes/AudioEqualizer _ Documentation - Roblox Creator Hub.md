# AudioEqualizer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioEqualizer
Scraped: 2026-01-11T02:33:31.681485Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- AudioEqualizer
- Wire
- Wires
- MidGain
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer)

English

Feedback

Engine Class

![AudioEqualizer](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioEqualizer-Dark.webp)AudioEqualizer

Adjusts the frequency content of audio streams.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Editor](#Editor):[boolean](/docs/luau/booleans) |
| [HighGain](#HighGain):[number](/docs/luau/numbers) |
| [LowGain](#LowGain):[number](/docs/luau/numbers) |
| [MidGain](#MidGain):[number](/docs/luau/numbers) |
| [MidRange](#MidRange):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |

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

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer) adjusts the frequency content of audio streams. It
provides one Input pin and one Output pin which can be connected
to/from by [Wires](/docs/reference/engine/classes/Wire). [AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer) has 3 frequency bands
whose gain values can be controlled, and the crossover points between bands
can be moved.

Code Samples

Listener Equalization

An AudioEqualizer can be used to change the frequency content of audio streams.
This can be done before emission, or after listening,
and can be used to implement your own, custom RollOff logic!
In this example, we use an AudioEqualizer to make an AudioPlayer's high frequencies
more muffled as the AudioListener looks away from the AudioEmitter.
We also reduce both the low and high frequencies as the listener gets further away.

```
local function wireUp(source: Instance, target: Instance): Wire



local wire = Instance.new("Wire")



wire.Parent = target



wire.SourceInstance = source



wire.TargetInstance = target



return wire



end



local function getCFrameFrom(inst: Instance): CFrame?



local parent = inst.Parent



if not parent then



return nil



elseif parent:IsA("Model") then



return parent.WorldPivot



elseif parent:IsA("BasePart") then



return parent.CFrame



elseif parent:IsA("Attachment") then



return parent.WorldCFrame



elseif parent:IsA("Camera") then



return parent.CFrame



else



return nil



end



end



local function rescale(value: number, oldRange: NumberRange, newRange: NumberRange): number



local clamped = math.clamp(value, oldRange.Min, oldRange.Max)



local normalized = clamped - oldRange.Min / (oldRange.Max - oldRange.Min)



return normalized * (newRange.Max - newRange.Min) + newRange.Min



end



local assetPlayer = Instance.new("AudioPlayer")



assetPlayer.AssetId = "rbxassetid://142376088"



assetPlayer.Parent = workspace



local equalizer = Instance.new("AudioEqualizer")



equalizer.MidRange = NumberRange.new(400, 3000)



equalizer.Parent = workspace



local emitterPart = Instance.new("Part")



emitterPart.Anchored = true



emitterPart.Position = Vector3.new(0, 5, 0)



emitterPart.Parent = workspace



local emitter = Instance.new("AudioEmitter")



emitter.Parent = emitterPart



local listener = Instance.new("AudioListener")



listener.Parent = workspace.CurrentCamera



local output = Instance.new("AudioDeviceOutput")



output.Parent = workspace



wireUp(assetPlayer, equalizer)



wireUp(equalizer, emitter)



wireUp(listener, output)



assetPlayer.Looping = true



assetPlayer:Play()



while true do



local emitterFrame = getCFrameFrom(emitter)



local listenerFrame = getCFrameFrom(listener)



if emitterFrame and listenerFrame then



local towardEmitter = emitterFrame.Position - listenerFrame.Position



local look = towardEmitter.Unit:Dot(listenerFrame.LookVector) -- ranges from [-1, 1]



look = rescale(look, NumberRange.new(-1, 1), NumberRange.new(-20, 0))



local distance = math.max(towardEmitter.Magnitude, 1)



local rolloff = 1 / distance -- ranges from [0, 1]



rolloff = rescale(rolloff, NumberRange.new(0, 1), NumberRange.new(-10, 10))



equalizer.HighGain = look + rolloff



equalizer.LowGain = rolloff



end



task.wait()



end
```

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioEqualizer.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

Editor

Not Replicated

Roblox Script Security

Read Parallel

AudioEqualizer.Editor:[boolean](/docs/luau/booleans)

Provide feedback

---

HighGain

Read Parallel

Gain value to be applied to the frequency content of the highest band in
the equalizer.

AudioEqualizer.HighGain:[number](/docs/luau/numbers)

Gain value, in decibels, to be applied to the frequency content of the
highest band in the equalizer. Ranges from -80 to 10.

Provide feedback

---

LowGain

Read Parallel

Gain value to be applied to the frequency content of the lowest band in
the equalizer.

AudioEqualizer.LowGain:[number](/docs/luau/numbers)

Gain value, in decibels, to be applied to the frequency content of the
lowest band in the equalizer. Ranges from -80 to 10.

Provide feedback

---

MidGain

Read Parallel

Gain value to be applied to the frequency content of the middle band in
the equalizer.

AudioEqualizer.MidGain:[number](/docs/luau/numbers)

Gain value, in decibels, to be applied to the frequency content of the
middle band in the equalizer. Ranges from -80 to 10.

Provide feedback

---

MidRange

Read Parallel

The frequency range of the band influenced by
[MidGain](/docs/reference/engine/classes/AudioEqualizer#MidGain).

AudioEqualizer.MidRange:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

The frequency range in hertz of the band influenced by
[MidGain](/docs/reference/engine/classes/AudioEqualizer#MidGain). The lower value of the range
determines the crossover frequency between the low and mid bands. The
higher value of the range determines the crossover frequency between the
mid and high bands. Both crossover frequencies range from 200 to 20,000.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioEqualizer:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer) has one "Input" pin and one "Output" pin.

Provide feedback

---

GetInputPins

AudioEqualizer:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioEqualizer:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer) via a [Wire](/docs/reference/engine/classes/Wire).

AudioEqualizer.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer) and to some other wirable instance.

Provide feedback

---