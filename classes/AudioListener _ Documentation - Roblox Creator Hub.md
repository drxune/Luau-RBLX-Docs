# AudioListener | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioListener
Scraped: 2026-01-11T02:28:34.769115Z

## Inherits
- Object
- Instance
- AudioListener
- AudioEmitters
- AudioEmitter
- Wire
- Wires
- Attachment
- Camera
- PVInstance
- SetAngleAttenuation()
- SetDistanceAttenuation()
- AudioInteractionGroup
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioListener](/docs/reference/engine/classes/AudioListener)

English

Feedback

Engine Class

![AudioListener](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioListener-Dark.webp)AudioListener

Records an audio stream from its surrounding
[AudioEmitters](/docs/reference/engine/classes/AudioEmitter) in the 3D world.

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
| [GetAudibilityFor](#GetAudibilityFor)(emitter: [AudioEmitter](/docs/reference/engine/classes/AudioEmitter)):[number](/docs/luau/numbers) |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetDistanceAttenuation](#GetDistanceAttenuation)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetInteractingEmitters](#GetInteractingEmitters)():Instances |
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

[AudioListener](/docs/reference/engine/classes/AudioListener) records an audio stream from its surrounding
[AudioEmitters](/docs/reference/engine/classes/AudioEmitter) in the 3D world. It provides a single
Output pin which can be connected to other pins via [Wires](/docs/reference/engine/classes/Wire). If
the parent is an [Attachment](/docs/reference/engine/classes/Attachment), [Camera](/docs/reference/engine/classes/Camera), or [PVInstance](/docs/reference/engine/classes/PVInstance),
the parent's world [CFrame](/docs/reference/engine/datatypes/CFrame) will be used for listening. If the parent
is not one of these classes, the [AudioListener](/docs/reference/engine/classes/AudioListener) effectively hears
nothing.

Code Samples

Camera Listener

```
local listener = Instance.new("AudioListener")



local output = Instance.new("AudioDeviceOutput")



local wire = Instance.new("Wire")



listener.Parent = workspace.Camera



wire.Parent = listener



output.Parent = wire



wire.SourceInstance = listener



wire.TargetInstance = output
```

---

API Reference

Properties

AcousticSimulationEnabled

Read Parallel

AudioListener.AcousticSimulationEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

AngleAttenuation

Roblox Security

Read Parallel

Represents how the perceived volume of the emitted sound changes based on
the angle between a [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) and the
[LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) associated with the
[AudioListener](/docs/reference/engine/classes/AudioListener).

AudioListener.AngleAttenuation:BinaryString

Represents a volume-over-angle curve that affects how loudly a
[AudioListener](/docs/reference/engine/classes/AudioListener) will hear the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter), based on the
angle between them and the [LookVector](/docs/reference/engine/datatypes/CFrame#LookVector)
associated with the [AudioListener](/docs/reference/engine/classes/AudioListener).

This property is internal and can't be accessed by scripts; it exists to
support replication. See
[SetAngleAttenuation()](/docs/reference/engine/classes/AudioListener#SetAngleAttenuation) for
usage details.

Provide feedback

---

AudioInteractionGroup

Read Parallel

Controls which [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) are audible to this
[AudioListener](/docs/reference/engine/classes/AudioListener).

AudioListener.AudioInteractionGroup:[string](/docs/luau/strings)

Controls which [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) are audible to this
[AudioListener](/docs/reference/engine/classes/AudioListener). Emitters that share an interaction group can be
heard by this Listener.

Provide feedback

---

DistanceAttenuation

Roblox Security

Read Parallel

Represents how the perceived volume of emitted sounds change as the
distance between [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) and the
[AudioListener](/docs/reference/engine/classes/AudioListener) increases.

AudioListener.DistanceAttenuation:BinaryString

Represents a volume-over-distance curve that affects how loudly the
[AudioListener](/docs/reference/engine/classes/AudioListener) hears any [AudioEmitters](/docs/reference/engine/classes/AudioEmitter), based
on the distance between them.

This property is internal and can't be accessed by scripts; it exists to
support replication. See
[SetDistanceAttenuation()](/docs/reference/engine/classes/AudioListener#SetDistanceAttenuation)
for usage details.

Provide feedback

---

PositionOverride

Roblox Security

Read Parallel

AudioListener.PositionOverride:[Instance](/docs/reference/engine/datatypes/Instance)

Provide feedback

---

SimulationFidelity

Deprecated

Show details

---

Methods

GetAngleAttenuation

Gets the angle attenuation curve that the [AudioListener](/docs/reference/engine/classes/AudioListener) is using,
or an empty table if it's using the default curve.

AudioListener:GetAngleAttenuation():[Dictionary](/docs/luau/tables#dictionaries)

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

Calculates how audible an [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) is for this listener

AudioListener:GetAudibilityFor(emitter:[AudioEmitter](/docs/reference/engine/classes/AudioEmitter)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| emitter:[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) |

Returns

[number](/docs/luau/numbers)

Calculates how audible an [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) is for this listener. The
resulting volume, ranging from 0 to 1, accounts for distance and angle
attenuation on both the emitter and listener.

Provide feedback

---

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioListener:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioListener](/docs/reference/engine/classes/AudioListener) has one "Output" pin.

Provide feedback

---

GetDistanceAttenuation

Gets the distance attenuation curve that the [AudioListener](/docs/reference/engine/classes/AudioListener) is
using, or an empty table if it's using the default curve.

AudioListener:GetDistanceAttenuation():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Returns a table mapping distance to volume. Keys are numbers greater than
or equal to 0, while values are numbers between 0 and 1 (inclusive)
describing how volume attenuates over distance. This method returns an
empty table if the default distance attenuation curve is being used.

Provide feedback

---

GetInputPins

AudioListener:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetInteractingEmitters

Lists all [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) that this listener is capable
of hearing.

AudioListener:GetInteractingEmitters():Instances

Returns

Instances

Returns an array of [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) that share an
[AudioInteractionGroup](/docs/reference/engine/classes/AudioListener#AudioInteractionGroup) with the
listener.

Provide feedback

---

GetOutputPins

AudioListener:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

SetAngleAttenuation

Sets the angle attenuation curve that the [AudioListener](/docs/reference/engine/classes/AudioListener) should
use, or uses a constant curve of volume 1 if none is provided.

AudioListener:SetAngleAttenuation(curve:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| curve:[Dictionary](/docs/luau/tables#dictionaries) |

Returns

()

Sets a volume-over-angle curve that affects how loudly a
[AudioListener](/docs/reference/engine/classes/AudioListener) will hear the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter), based on the
angle between them and the [LookVector](/docs/reference/engine/datatypes/CFrame#LookVector)
associated with the [AudioListener](/docs/reference/engine/classes/AudioListener).

The curve is represented by a table mapping angle keys to volume values.
Keys are expected to be unique numbers between 0 and 180 (inclusive),
while values are expected to be numbers between 0 and 1 (inclusive).
Tables containing up to 400 key-value pairs are supported.

The volume of a [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) from the perspective of the
[AudioListener](/docs/reference/engine/classes/AudioListener) at an angle a is determined by linearly
interpolating between the volume levels for the points on the curve whose
angle values are directly above and below a. If there is either no point
below a or no point above a, the volume level of the other point is
chosen. Essentially, the curve is a sequence of points connected by
straight lines, and beyond its left and right endpoints the curve extends
outward at their respective volume levels.

This volume will be multiplied with the volumes from all other attenuation
curves (including the ones on the sending [AudioEmitter](/docs/reference/engine/classes/AudioEmitter)) to obtain
the final audibility.

If the table is empty or nil, the [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) defaults to using
an angle attenuation curve with the constant volume value of 1.

Code Samples

Camera Listener

```
local Workspace = game:GetService("Workspace")



local currentCamera = Workspace.CurrentCamera



local listener = Instance.new("AudioListener")



listener.Parent = currentCamera



local wire = Instance.new("Wire")



wire.Parent = listener



local output = Instance.new("AudioDeviceOutput")



output.Parent = wire



listener:SetAngleAttenuation({



[0] = 1, -- Emitters directly in front of the listener will be full volume



[180] = 0.5 -- Emitters directly behind the listener will be half volume



})



wire.SourceInstance = listener



wire.TargetInstance = output
```

Provide feedback

---

SetDistanceAttenuation

Sets the distance attenuation curve that the [AudioListener](/docs/reference/engine/classes/AudioListener) should
use, or uses an inverse rolloff curve if none is provided.

AudioListener:SetDistanceAttenuation(curve:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| curve:[Dictionary](/docs/luau/tables#dictionaries) |

Returns

()

Sets a volume-over-distance curve that affects how loudly the
[AudioListener](/docs/reference/engine/classes/AudioListener) will hear any [AudioEmitters](/docs/reference/engine/classes/AudioEmitter),
based on the distance between them.

The curve is represented by a table mapping distance keys to volume
values. Keys are expected to be unique numbers greater than or equal to 0,
while values are expected to be numbers between 0 and 1 (inclusive).
Tables containing up to 400 key-value pairs are supported.

The volume of a [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) from the perspective of the
[AudioListener](/docs/reference/engine/classes/AudioListener) at a distance d is determined by linearly
interpolating between the volume levels for the points on the curve whose
distance values are directly above and below d. If there is either no
point below d or no point above d, the volume level of the other point
is chosen. Essentially, the curve is a sequence of points connected by
straight lines, and beyond its left and right endpoints the curve extends
outward infinitely at their respective volume levels.

This volume will be multiplied with the volumes from all other attenuation
curves (including the ones on the sending [AudioEmitter](/docs/reference/engine/classes/AudioEmitter)) to obtain
the final audibility.

If the table is empty or nil, the [AudioListener](/docs/reference/engine/classes/AudioListener) defaults to
applying a constant volume of 1 everywhere.

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioListener](/docs/reference/engine/classes/AudioListener) via a [Wire](/docs/reference/engine/classes/Wire).

AudioListener.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioListener](/docs/reference/engine/classes/AudioListener) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioListener](/docs/reference/engine/classes/AudioListener) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioListener](/docs/reference/engine/classes/AudioListener) and to some other wirable instance.

Provide feedback

---