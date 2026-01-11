# AudioChannelSplitter | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioChannelSplitter
Scraped: 2026-01-11T02:39:00.620776Z

## Inherits
- Instance
- AudioChannelSplitter
- Wire
- Object
- Wires
- AudioChannelSplitter.Layout
- Wire.TargetName
- Wire.SourceName
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioChannelSplitter](/docs/reference/engine/classes/AudioChannelSplitter)

English

Feedback

Engine Class

![AudioChannelSplitter](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioChannelSplitter-Dark.webp)AudioChannelSplitter

Splits an audio stream into component channels so that each can be processed
independently.

---

Summary

Properties

|  |
| --- |
| [Layout](#Layout):[Enum.AudioChannelLayout](/docs/reference/engine/enums/AudioChannelLayout) |

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

[AudioChannelSplitter](/docs/reference/engine/classes/AudioChannelSplitter) splits an audio stream into component channels so
that each can be processed independently. It provides one Input pin, one
combined Output pin, as well as the following secondary output pins, all
of which can be connected to/from by [Wires](/docs/reference/engine/classes/Wire): Left, Right,
Center, SurroundLeft, SurroundRight, Sub, BackLeft,
BackRight, TopLeft, TopRight, TopBackLeft, and
TopBackRight.

![Diagram showing position of all potential channels.](https://prod.docsiteassets.roblox.com/assets/engine-api/enums/AudioChannelLayout/Surround_7_1_4.jpg)

Code Samples

Splitting & Mixing Channels

```
local Workspace = game:GetService("Workspace")



local function wireUp(source: Instance, target: Instance, sourceName: string?, targetName: string?)



local wire = Instance.new("Wire", source)



wire.SourceInstance = source



wire.TargetInstance = target



if sourceName then



wire.SourceName = sourceName



end



if targetName then



wire.TargetName = targetName



end



return wire



end



local listener = Instance.new("AudioListener")



listener.Parent = Workspace.CurrentCamera



local output = Instance.new("AudioDeviceOutput")



output.Parent = Workspace



local splitter = Instance.new("AudioChannelSplitter")



splitter.Parent = Workspace



local mixer = Instance.new("AudioChannelMixer")



mixer.Parent = Workspace



-- Send what the listener hears to a splitter and send a mix to the final output



wireUp(listener, splitter)



wireUp(mixer, output)



-- Set up both the splitter and mixer to use a quadrophonic layout



splitter.Layout = Enum.AudioChannelLayout.Quad



mixer.Layout = Enum.AudioChannelLayout.Quad



-- Give each of the four channels its own pitch shifter



local frontLeft = Instance.new("AudioPitchShifter")



frontLeft.Name = "Front Left"



frontLeft.Pitch = 1.25



frontLeft.Parent = Workspace



local backLeft = Instance.new("AudioPitchShifter")



backLeft.Name = "Back Left"



backLeft.Pitch = 0.5



backLeft.Parent = Workspace



local frontRight = Instance.new("AudioPitchShifter")



frontRight.Name = "Front Right"



frontRight.Pitch = 1.5



frontRight.Parent = Workspace



local backRight = Instance.new("AudioPitchShifter")



backRight.Name = "Back Right"



backRight.Pitch = 0.75



backRight.Parent = Workspace



wireUp(splitter, frontLeft, "Left")



wireUp(splitter, backLeft, "BackLeft")



wireUp(splitter, frontRight, "Right")



wireUp(splitter, backRight, "BackRight")



wireUp(frontLeft, mixer, nil, "Left")



wireUp(backLeft, mixer, nil, "BackLeft")



wireUp(frontRight, mixer, nil, "Right")



wireUp(backRight, mixer, nil, "BackRight")



-- Configure a part to emit audio



local part = Instance.new("Part")



part.Shape = Enum.PartType.Ball



part.Size = Vector3.new(4, 4, 4)



part.Material = Enum.Material.SmoothPlastic



part.CastShadow = false



part.Position = Vector3.new(0, 4, -12)



part.Anchored = true



part.Parent = Workspace



local analyzer = Instance.new("AudioAnalyzer")



analyzer.Parent = part



local emitter = Instance.new("AudioEmitter")



emitter.Parent = part



local assetPlayer = Instance.new("AudioPlayer")



assetPlayer.Looping = true



assetPlayer.Asset = "rbxassetid://97799489309320"



assetPlayer.Parent = emitter



wireUp(assetPlayer, emitter)



wireUp(assetPlayer, analyzer)



-- Start playing the audio



assetPlayer:Play()



-- Adjust the part's color as the audio plays



while true do



local peak = math.sqrt(analyzer.PeakLevel)



part.Color = Color3.new(peak, peak, peak)



task.wait()



end
```

---

API Reference

Properties

Layout

Read Parallel

Controls the input channel layout to be split from.

AudioChannelSplitter.Layout:[Enum.AudioChannelLayout](/docs/reference/engine/enums/AudioChannelLayout)

Controls the input channel layout to be split from. When changed, all
audio streams prior to this channel splitter's input may need to be
up-mixed (widened to at least as many channels as the input requires).

The Output pin produces a copy of the stream wired to Input but,
depending on the value of [AudioChannelSplitter.Layout](/docs/reference/engine/classes/AudioChannelSplitter#Layout):

* For [Mono](/docs/reference/engine/enums/AudioChannelLayout#Mono), the Center pin produces an
  audio stream.
* For [Stereo](/docs/reference/engine/enums/AudioChannelLayout#Stereo), the Left and Right
  pins produce audio streams.
* For [Quad](/docs/reference/engine/enums/AudioChannelLayout#Quad), the Left, Right,
  BackLeft, and BackRight pins produce audio streams.
* [Surround\_5](/docs/reference/engine/enums/AudioChannelLayout#Surround_5) is the same as Quad,
  plus Center produces an audio stream.
* [Surround\_5\_1](/docs/reference/engine/enums/AudioChannelLayout#Surround_5_1) is the same as
  Surround\_5, plus Sub produces an audio stream.
* [Surround\_7\_1](/docs/reference/engine/enums/AudioChannelLayout#Surround_7_1) is the same as
  Surround\_5\_1, plus SurroundLeft and SurroundRight produce
  audio streams.
* For [Surround\_7\_1\_4](/docs/reference/engine/enums/AudioChannelLayout#Surround_7_1_4), all
  secondary output pins produce audio streams.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioChannelSplitter:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

Provide feedback

---

GetInputPins

Returns the input pin available for [Wire.TargetName](/docs/reference/engine/classes/Wire#TargetName).

AudioChannelSplitter:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns a table containing one string, "Input", indicating the input pin
available for [Wire.TargetName](/docs/reference/engine/classes/Wire#TargetName).

Provide feedback

---

GetOutputPins

Returns the output pins that can be selected by [Wire.SourceName](/docs/reference/engine/classes/Wire#SourceName).

AudioChannelSplitter:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns a table of strings indicating which output pins are available for
[Wire.SourceName](/docs/reference/engine/classes/Wire#SourceName):

* "Output"
* "Left"
* "Right"
* "Center"
* "SurroundLeft"
* "SurroundRight"
* "BackLeft"
* "BackRight"
* "Sub"
* "TopLeft"
* "TopRight"
* "TopBackLeft"
* "TopBackRight"

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioChannelSplitter](/docs/reference/engine/classes/AudioChannelSplitter) via a [Wire](/docs/reference/engine/classes/Wire).

AudioChannelSplitter.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioChannelSplitter](/docs/reference/engine/classes/AudioChannelSplitter) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioChannelSplitter](/docs/reference/engine/classes/AudioChannelSplitter) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioChannelSplitter](/docs/reference/engine/classes/AudioChannelSplitter) and to some other wirable instance.

Provide feedback

---