# AudioEmitter | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioEmitter
Scraped: 2026-01-11T02:33:35.156301Z

## Inherits
- Object
- Instance
- AudioEmitter
- AudioListener
- Wire
- Wires
- Attachment
- Camera
- PVInstance
- AudioEmitters
- AudioListeners
- SetAngleAttenuation()
- SetDistanceAttenuation()
- AudioInteractionGroup
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioEmitter](/docs/reference/engine/classes/AudioEmitter)

English

Feedback

Engine Class

![AudioEmitter](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioEmitter-Dark.webp)AudioEmitter

Emits audio streams into the world.

---

Summary

Properties

|  |
| --- |
| [AcousticSimulationEnabled](#AcousticSimulationEnabled):[boolean](/docs/luau/booleans) |
| [AngleAttenuation](#AngleAttenuation):BinaryString |
| [AudioInteractionGroup](#AudioInteractionGroup):[string](/docs/luau/strings) |
| [DistanceAttenuation](#DistanceAttenuation):BinaryString |
| [PositionOverride](#PositionOverride):[Instance](/docs/reference/engine/datatypes/Instance) |
| [SimulationFidelity](#SimulationFidelity):[Enum.AudioSimulationFidelity](/docs/reference/engine/enums/AudioSimulationFidelity)  Deprecated |

Methods

|  |
| --- |
| [GetAngleAttenuation](#GetAngleAttenuation)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetAudibilityFor](#GetAudibilityFor)(listener: [AudioListener](/docs/reference/engine/classes/AudioListener)):[number](/docs/luau/numbers) |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetDistanceAttenuation](#GetDistanceAttenuation)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetInteractingListeners](#GetInteractingListeners)():Instances |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |
| [SetAngleAttenuation](#SetAngleAttenuation)(curve: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [SetDistanceAttenuation](#SetDistanceAttenuation)(curve: [Dictionary](/docs/luau/tables#dictionaries)):() |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) emits audio streams into the world. It provides a single
Input pin that can be connected to by one or more [Wires](/docs/reference/engine/classes/Wire). Any
streams wired to an [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) get broadcasted into the world from
the emitter's parent's position. If the parent is an [Attachment](/docs/reference/engine/classes/Attachment),
[Camera](/docs/reference/engine/classes/Camera), or [PVInstance](/docs/reference/engine/classes/PVInstance), the parent's world-position will be
used. If the parent is not one of these classes, the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) is
effectively silent.

[AudioEmitters](/docs/reference/engine/classes/AudioEmitter) are heard by
[AudioListeners](/docs/reference/engine/classes/AudioListener) in order to implement 3D spatialization.

Code Samples

Playing one asset from multiple 3d locations at once

```
local part1: BasePart = workspace.Speakers.Left



local part2: BasePart = workspace.Speakers.Right



local player: AudioPlayer = workspace.AudioPlayer



local leftEmitter = Instance.new("AudioEmitter")



local rightEmitter = Instance.new("AudioEmitter")



local toLeft = Instance.new("Wire")



local toRight = Instance.new("Wire")



leftEmitter.Parent = part1



rightEmitter.Parent = part2



toLeft.Parent = leftEmitter



toLeft.SourceInstance = player



toLeft.TargetInstance = leftEmitter



toRight.Parent = rightEmitter



toRight.SourceInstance = player



toRight.TargetInstance = rightEmitter



player:Play()
```

---

API Reference

Properties

AcousticSimulationEnabled

Read Parallel

AudioEmitter.AcousticSimulationEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

AngleAttenuation

Roblox Security

Read Parallel

Represents how the perceived volume of the emitted sound changes based on
the angle between a [AudioListener](/docs/reference/engine/classes/AudioListener) and the
[LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) associated with the
[AudioEmitter](/docs/reference/engine/classes/AudioEmitter).

AudioEmitter.AngleAttenuation:BinaryString

Represents a volume-over-angle curve that affects how loudly a
[AudioListener](/docs/reference/engine/classes/AudioListener) will hear the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter), based on the
angle between them and the [LookVector](/docs/reference/engine/datatypes/CFrame#LookVector)
associated with the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter).

This property is internal and can't be accessed by scripts; it exists to
support replication. See
[SetAngleAttenuation()](/docs/reference/engine/classes/AudioEmitter#SetAngleAttenuation) for usage
details.

Provide feedback

---

AudioInteractionGroup

Read Parallel

Controls which [AudioListeners](/docs/reference/engine/classes/AudioListener) are capable of hearing
this [AudioEmitter](/docs/reference/engine/classes/AudioEmitter).

AudioEmitter.AudioInteractionGroup:[string](/docs/luau/strings)

If an [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) and an [AudioListener](/docs/reference/engine/classes/AudioListener) share an
interaction group, then the listener is capable of hearing the emitter.

Provide feedback

---

DistanceAttenuation

Roblox Security

Read Parallel

Represents how the perceived volume of the emitted sound changes as the
distance between a [AudioListener](/docs/reference/engine/classes/AudioListener) and the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter)
increases.

AudioEmitter.DistanceAttenuation:BinaryString

Represents a volume-over-distance curve that affects how loudly a
[AudioListener](/docs/reference/engine/classes/AudioListener) will hear the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter), based on the
distance between them.

This property is internal and can't be accessed by scripts; it exists to
support replication. See
[SetDistanceAttenuation()](/docs/reference/engine/classes/AudioEmitter#SetDistanceAttenuation) for
usage details.

Provide feedback

---

PositionOverride

Roblox Security

Read Parallel

AudioEmitter.PositionOverride:[Instance](/docs/reference/engine/datatypes/Instance)

Provide feedback

---

SimulationFidelity

Deprecated

Show details

---

Methods

GetAngleAttenuation

Gets the angle attenuation curve that the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) is using,
or an empty table if it's using the default curve.

AudioEmitter:GetAngleAttenuation():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Table mapping angle to volume, as described above.

Returns a table mapping angle to volume. Keys are numbers between 0 and
180 (inclusive), while values are numbers between 0 and 1
(inclusive) describing how volume attenuates depending on direction. This
method returns an empty table if the default angle attenuation curve is
being used.

Provide feedback

---

GetAudibilityFor

Calculates how audible this emitter is for a particular
[AudioListener](/docs/reference/engine/classes/AudioListener).

AudioEmitter:GetAudibilityFor(listener:[AudioListener](/docs/reference/engine/classes/AudioListener)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| listener:[AudioListener](/docs/reference/engine/classes/AudioListener) |

Returns

[number](/docs/luau/numbers)

Calculates how audible this emitter is for a particular
[AudioListener](/docs/reference/engine/classes/AudioListener). The resulting volume, ranging from 0 to 1,
accounts for distance and angle attenuation on both the emitter and
listener.

Provide feedback

---

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioEmitter:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) has one "Input" pin.

Provide feedback

---

GetDistanceAttenuation

Gets the distance attenuation curve that the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) is
using, or an empty table if it's using the default curve.

AudioEmitter:GetDistanceAttenuation():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Returns a table mapping distance to volume. Keys are numbers greater than
or equal to 0, while values are numbers between 0 and 1 (inclusive)
describing how volume attenuates over distance. This method returns an
empty table if the default distance attenuation curve is being used.

Provide feedback

---

GetInputPins

AudioEmitter:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetInteractingListeners

Lists all [AudioListeners](/docs/reference/engine/classes/AudioListener) that are capable of hearing
this emitter.

AudioEmitter:GetInteractingListeners():Instances

Returns

Instances

Returns an array of [AudioListeners](/docs/reference/engine/classes/AudioListener) that share an
[AudioInteractionGroup](/docs/reference/engine/classes/AudioEmitter#AudioInteractionGroup) with the
emitter.

Provide feedback

---

GetOutputPins

AudioEmitter:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

SetAngleAttenuation

Sets the angle attenuation curve that the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) should use,
or uses a constant curve of volume 1 if none is provided.

AudioEmitter:SetAngleAttenuation(curve:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| curve:[Dictionary](/docs/luau/tables#dictionaries) |

Returns

()

Sets a volume-over-angle curve that affects how loudly a
[AudioListener](/docs/reference/engine/classes/AudioListener) will hear the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter), based on the
angle between them and the [LookVector](/docs/reference/engine/datatypes/CFrame#LookVector)
associated with the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter).

The curve is represented by a table mapping angle keys to volume values.
Keys are expected to be unique numbers between 0 and 180 (inclusive),
while values are expected to be numbers between 0 and 1 (inclusive).
Tables containing up to 400 key-value pairs are supported.

The volume of the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) from the perspective of a
[AudioListener](/docs/reference/engine/classes/AudioListener) at an angle a is determined by linearly
interpolating between the volume levels for the points on the curve whose
angle values are directly above and below a. If there is either no point
below a or no point above a, the volume level of the other point is
chosen. Essentially, the curve is a sequence of points connected by
straight lines, and beyond its left and right endpoints the curve extends
outward at their respective volume levels.

This volume will be multiplied with the volumes from all other attenuation
curves (including the ones on the receiving [AudioListener](/docs/reference/engine/classes/AudioListener)) to
obtain the final audibility.

If the table is empty or nil, the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) defaults to using
an angle attenuation curve with the constant volume value of 1.

Provide feedback

---

SetDistanceAttenuation

Sets the distance attenuation curve that the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) should
use, or uses an inverse rolloff curve if none is provided.

AudioEmitter:SetDistanceAttenuation(curve:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| curve:[Dictionary](/docs/luau/tables#dictionaries) |

Returns

()

Sets a volume-over-distance curve that affects how loudly a
[AudioListener](/docs/reference/engine/classes/AudioListener) will hear the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter), based on the
distance between them.

The curve is represented by a table mapping distance keys to volume
values. Keys are expected to be unique numbers greater than or equal to 0,
while values are expected to be numbers between 0 and 1 (inclusive).
Tables containing up to 400 key-value pairs are supported.

The volume of the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) from the perspective of a
[AudioListener](/docs/reference/engine/classes/AudioListener) at a distance d is determined by linearly
interpolating between the volume levels for the points on the curve whose
distance values are directly above and below d. If there is either no
point below d or no point above d, the volume level of the other point
is chosen. Essentially, the curve is a sequence of points connected by
straight lines, and beyond its left and right endpoints the curve extends
outward infinitely at their respective volume levels.

This volume will be multiplied with the volumes from all other attenuation
curves (including the ones on the receiving [AudioListener](/docs/reference/engine/classes/AudioListener)) to
obtain the final audibility.

If the table is empty or nil, the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) defaults to using
a distance attenuation curve determined by the inverse-square law.

Code Samples

Custom Distance Attenuation

```
local Players = game:GetService("Players")



local emitterPart = Instance.new("Part")



emitterPart.Anchored = true



emitterPart.Position = Vector3.new(0, 0, 0)



emitterPart.Parent = workspace



local emitter: AudioEmitter = Instance.new("AudioEmitter")



emitter.Parent = emitterPart



local curve = {}



curve[10] = 1 -- Within a distance of 10 studs, listeners hear this emitter at full volume



curve[100] = 0.4 -- At a distance of 100 studs, listeners hear this emitter at 40% volume



curve[300] = 0 -- At any distance farther than 300 studs, listeners cannot hear this emitter



emitter:SetDistanceAttenuation(curve)



-- Replicate the rolloff curve from the old voice implementation



-- Default voice without the new audio API uses quadratic rolloff ranging from 7 to 80 studs



local MIN_DISTANCE = 7



local MAX_DISTANCE = 80



local CURVE_STEP_SIZE = 2



local voiceCurve = {}



for i = MIN_DISTANCE, MAX_DISTANCE, CURVE_STEP_SIZE do



voiceCurve[i] = ((i - MIN_DISTANCE) - (MAX_DISTANCE - MIN_DISTANCE)) ^ 2 / (MAX_DISTANCE - MIN_DISTANCE) ^ 2



end



voiceCurve[MAX_DISTANCE] = 0



local function setVoiceCurve(character)



local voiceEmitter: AudioEmitter = character:WaitForChild("AudioEmitter")



voiceEmitter:SetDistanceAttenuation(voiceCurve)



end



for _, player in Players:GetPlayers() do



if player.Character then



setVoiceCurve(player.Character)



end



player.CharacterAdded:Connect(setVoiceCurve)



end
```

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) via a [Wire](/docs/reference/engine/classes/Wire).

AudioEmitter.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) and to some other wirable instance.

Provide feedback

---