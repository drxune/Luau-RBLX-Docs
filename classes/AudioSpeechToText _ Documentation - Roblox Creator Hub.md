# AudioSpeechToText | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioSpeechToText
Scraped: 2026-01-11T02:34:59.709021Z

## Tags
- Not Replicated

## Inherits
- Instance
- AudioSpeechToText
- Wire
- Object
- Wires
- TextLabel
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText)

English

Feedback

Engine Class

![AudioSpeechToText](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioSpeechToText-Dark.webp)AudioSpeechToText

Converts spoken audio into text.

---

Summary

Properties

|  |
| --- |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Text](#Text):[string](/docs/luau/strings) |
| [VoiceDetected](#VoiceDetected):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) is used to convert speech audio into text. This
class provides a single Input pin that can be connected to other pins via
[Wires](/docs/reference/engine/classes/Wire).

Roblox uses the following formula to throttle requests for this API based on
the number of players in your experience:
max requests per minute per experience = 1 + (5 \* number\_of\_concurrent\_users).

For more information, see
[Speech-to-text](/docs/audio/objects#speech-to-text).

Code Samples

Convert speech to text

On character spawn, adds an [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) instance and
puts its output into a new [TextLabel](/docs/reference/engine/classes/TextLabel).

```
local players = game:GetService("Players")



local function connect(src: Instance, dst: Instance)



local wire = Instance.new("Wire", dst)



wire.SourceInstance = src



wire.TargetInstance = dst



end



local textLabel = nil



local stt = nil



local function onCharacterSpawned(player: Player, character: Model)



local input = Instance.new("AudioDeviceInput", player)



input.Player = player



local audioSpeechToText = Instance.new("AudioSpeechToText", character)



audioSpeechToText.Enabled = true



connect(player.AudioDeviceInput, audioSpeechToText)



local screenGui = Instance.new("ScreenGui", player.PlayerGui)



textLabel = Instance.new("TextLabel", screenGui)



textLabel.Text = "Hello!"



textLabel.Size = UDim2.fromOffset(160,90)



textLabel.Position = UDim2.fromOffset(20,20)



textLabel.BackgroundTransparency = 0



textLabel.FontFace.Weight = Enum.FontWeight.Bold



textLabel.TextColor3 = Color3.new(1,1,1)



textLabel.TextStrokeColor3 = Color3.new(0,0,0)



textLabel.TextStrokeTransparency = 0.5



audioSpeechToText:GetPropertyChangedSignal("Text"):Connect(function()



if audioSpeechToText.Text ~= '' then



print(audioSpeechToText.Text)



textLabel.Text = audioSpeechToText.Text



audioSpeechToText.Text = ''



end



end)



stt = audioSpeechToText



end



local function onPlayerAdded(player: Player)



if player.Character then



onCharacterSpawned(player, player.Character)



end



player.CharacterAdded:Connect(function()



onCharacterSpawned(player, player.Character)



end)



end



players.PlayerAdded:Connect(onPlayerAdded)



for _, player in players:GetPlayers() do



onPlayerAdded(player)



end



local vad = false



while true do



wait(0.1)



if stt and textLabel then



if(stt.VoiceDetected ~= vad) then



vad = stt.VoiceDetected



print(vad)



if(vad) then



textLabel.BackgroundColor3 = Color3.new(0.7,0,0)



else



textLabel.BackgroundColor3 = Color3.new(0,0,0)



end



end



end



end
```

---

API Reference

Properties

Enabled

Read Parallel

Whether the [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) object is enabled for processing
input audio into text.

AudioSpeechToText.Enabled:[boolean](/docs/luau/booleans)

Whether the [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) object is enabled for processing
input audio into text.

Provide feedback

---

Text

Read Parallel

The text resulting from the conversion of speech audio.

AudioSpeechToText.Text:[string](/docs/luau/strings)

The text resulting from the conversion of speech audio.

Provide feedback

---

VoiceDetected

Read Only

Not Replicated

Read Parallel

Whether the [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) object is detecting speech in the
incoming audio signal.

AudioSpeechToText.VoiceDetected:[boolean](/docs/luau/booleans)

Whether the [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) object is detecting speech in the
incoming audio signal. [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) records the speech audio
until it ceases or until a maximum amount of 10 seconds has been recorded.
Then it converts the recorded audio into text.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioSpeechToText:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) has one input pin.

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) via a [Wire](/docs/reference/engine/classes/Wire).

AudioSpeechToText.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText) and to some other wirable instance.

Provide feedback

---