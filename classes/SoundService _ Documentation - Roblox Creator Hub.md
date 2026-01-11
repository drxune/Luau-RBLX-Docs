# SoundService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SoundService
Scraped: 2026-01-11T02:34:44.109671Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- SoundService
- Sounds
- AudioPlayers
- AudioEmitters
- SoundGroups
- SoundService.AmbientReverb
- AudioListeners
- AcousticSimulationEnabled
- AmbientReverb
- AudioReverb
- AudioListener
- AudioDeviceOutput
- AudioListener.InteractionGroup
- Sound
- BasePart
- Attachment
- DistanceFactor
- SoundService.DistanceFactor
- AudioPlayer
- AudioEmitter
- SoundService.DopplerScale
- LocalScript
- Play()
- Sound.RollOffMinDistance
- RolloffScale
- Sound.RollOffMaxDistance
- SoundService.RolloffScale
- AudioEmitter:SetDistanceAttenuation()
- Part
- Attachments
- MeshParts
- CurrentCamera
- SetListener()
- Workspace.CurrentCamera
- Sound.Volume
- Sound.TimePosition
- Sound.PlaybackSpeed
- Sound.Looped
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [SoundService](/docs/reference/engine/classes/SoundService)

English

Feedback

Engine Class

![SoundService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SoundService-Dark.webp)SoundService

A service that determines various aspects of how the audio engine works. Most
of its properties affect how [Sounds](/docs/reference/engine/classes/Sound) play in the experience.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [AcousticSimulationEnabled](#AcousticSimulationEnabled):[boolean](/docs/luau/booleans) |
| [AmbientReverb](#AmbientReverb):[Enum.ReverbType](/docs/reference/engine/enums/ReverbType) |
| [CharacterSoundsUseNewApi](#CharacterSoundsUseNewApi):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [DefaultListenerLocation](#DefaultListenerLocation):[Enum.ListenerLocation](/docs/reference/engine/enums/ListenerLocation) |
| [DistanceFactor](#DistanceFactor):[number](/docs/luau/numbers) |
| [DopplerScale](#DopplerScale):[number](/docs/luau/numbers) |
| [RespectFilteringEnabled](#RespectFilteringEnabled):[boolean](/docs/luau/booleans) |
| [RolloffScale](#RolloffScale):[number](/docs/luau/numbers) |
| [VolumetricAudio](#VolumetricAudio):[Enum.VolumetricAudio](/docs/reference/engine/enums/VolumetricAudio) |

Methods

|  |
| --- |
| [GetListener](#GetListener)():[Tuple](/docs/luau/tuples) |
| [OpenAttenuationCurveEditor](#OpenAttenuationCurveEditor)(selectedCurveObjects: Instances):() |
| [OpenDirectionalCurveEditor](#OpenDirectionalCurveEditor)(selectedCurveObjects: Instances):() |
| [PlayLocalSound](#PlayLocalSound)(sound: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [SetListener](#SetListener)(listenerType: [Enum.ListenerType](/docs/reference/engine/enums/ListenerType),listener: [Tuple](/docs/luau/tuples)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A service that determines various aspects of how the audio engine works. Most
of its properties affect how [Sounds](/docs/reference/engine/classes/Sound) play in the experience,
while others affect the behavior of instances in the advanced audio system
such as [AudioPlayers](/docs/reference/engine/classes/AudioPlayer) and
[AudioEmitters](/docs/reference/engine/classes/AudioEmitter).

[SoundService](/docs/reference/engine/classes/SoundService) is also often used to store
[SoundGroups](/docs/reference/engine/classes/SoundGroup), although this is not mandatory for groups to
work.

Code Samples

Dynamic Reverb System

The code in this sample, when ran from a LocalScript, will change the
[SoundService.AmbientReverb](/docs/reference/engine/classes/SoundService#AmbientReverb) property of SoundService when the player
is inside a BasePart tagged using CollectionService.

To add or remove tags and reverb types, change the entries in the 'reverbTags'
table.

```
local Players = game:GetService("Players")



local CollectionService = game:GetService("CollectionService")



local SoundService = game:GetService("SoundService")



local localPlayer = Players.LocalPlayer



local reverbTags = {



["reverb_Cave"] = Enum.ReverbType.Cave,



}



-- collect parts and group them by tag



local parts = {}



for reverbTag, reverbType in pairs(reverbTags) do



for _, part in pairs(CollectionService:GetTagged(reverbTag)) do



parts[part] = reverbType



end



end



-- function to check if a position is within a part's extents



local function positionInPart(part, position)



local extents = part.Size / 2



local offset = part.CFrame:PointToObjectSpace(position)



return offset.x < extents.x and offset.y < extents.y and offset.z < extents.z



end



local reverbType = SoundService.AmbientReverb



while true do



task.wait()



if not localPlayer then



return



end



local character = localPlayer.Character



-- default to no reverb



local newReverbType = Enum.ReverbType.NoReverb



if character and character.PrimaryPart then



local position = character.PrimaryPart.Position



-- go through all the indexed parts



for part, type in pairs(parts) do



-- see if the character is within them



if positionInPart(part, position) then



-- if so, pick that reverb type



newReverbType = type



break



end



end



end



-- set the reverb type if it has changed



if newReverbType ~= reverbType then



SoundService.AmbientReverb = newReverbType



reverbType = newReverbType



end



end
```

---

API Reference

Properties

AcousticSimulationEnabled

Read Parallel

Determines whether acoustic simulation is enabled globally in the advanced
audio system.

SoundService.AcousticSimulationEnabled:[boolean](/docs/luau/booleans)

Determines at a global level whether sound from
[AudioEmitters](/docs/reference/engine/classes/AudioEmitter) and
[AudioListeners](/docs/reference/engine/classes/AudioListener) should automatically implement
features of acoustic simulation, such as occlusion (being muffled through
walls), diffraction (bending around corners), and reverberation (echoing
off of walls).

If set to false, these instances will not simulate these features,
regardless of their individual
[AcousticSimulationEnabled](/docs/reference/engine/classes/AudioEmitter#AcousticSimulationEnabled)
settings.

Provide feedback

---

AmbientReverb

Read Parallel

The ambient sound environment preset applied to all [Sounds](/docs/reference/engine/classes/Sound).

SoundService.AmbientReverb:[Enum.ReverbType](/docs/reference/engine/enums/ReverbType)

A reverb preset that should be applied to all [Sounds](/docs/reference/engine/classes/Sound) in the
experience.

Each [Enum.ReverbType](/docs/reference/engine/enums/ReverbType) option for this property corresponds to a preset
available in the FMOD sound engine. For example, when
[AmbientReverb](/docs/reference/engine/classes/SoundService#AmbientReverb) is set to
[Enum.ReverbType.Hangar](/docs/reference/engine/enums/ReverbType#Hangar), [Sounds](/docs/reference/engine/classes/Sound) will have reverb applied to
simulate being in a large enclosed space.

Note that this only affects [Sounds](/docs/reference/engine/classes/Sound) and not instances in
the advanced audio system such as [AudioPlayers](/docs/reference/engine/classes/AudioPlayer) and
[AudioEmitters](/docs/reference/engine/classes/AudioEmitter). See [AudioReverb](/docs/reference/engine/classes/AudioReverb) for a way to
apply reverb in that system.

Provide feedback

---

CharacterSoundsUseNewApi

Plugin Security

Read Parallel

Determines whether the default character sounds will use instances in the
advanced audio system vs. [Sounds](/docs/reference/engine/classes/Sound).

SoundService.CharacterSoundsUseNewApi:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

Determines which set of instances core scripts will use to create default
character sounds. If set to [Enum.RolloutState.Enabled](/docs/reference/engine/enums/RolloutState#Enabled), it will use
instances in the advanced audio system such as
[AudioPlayers](/docs/reference/engine/classes/AudioPlayer) and [AudioEmitters](/docs/reference/engine/classes/AudioEmitter).
If set to [Enum.RolloutState.Disabled](/docs/reference/engine/enums/RolloutState#Disabled), it will use instances in the
legacy sound system such as [Sounds](/docs/reference/engine/classes/Sound).

Provide feedback

---

DefaultListenerLocation

Plugin Security

Read Parallel

Determines where (if anywhere) to place an [AudioListener](/docs/reference/engine/classes/AudioListener) by
default.

SoundService.DefaultListenerLocation:[Enum.ListenerLocation](/docs/reference/engine/enums/ListenerLocation)

Determines where to place an [AudioListener](/docs/reference/engine/classes/AudioListener) by default. The
[AudioListener](/docs/reference/engine/classes/AudioListener) will automatically be wired to a
[AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) and will have an empty
[AudioListener.InteractionGroup](/docs/reference/engine/classes/AudioListener#InteractionGroup) set.

See [Enum.ListenerLocation](/docs/reference/engine/enums/ListenerLocation) for detailed descriptions of each option.

Provide feedback

---

DistanceFactor

Read Parallel

The number of studs to be considered a meter by [SoundService](/docs/reference/engine/classes/SoundService) when
simulating the Doppler effect for [Sounds](/docs/reference/engine/classes/Sound).

SoundService.DistanceFactor:[number](/docs/luau/numbers)

The number of studs to be considered a meter by [SoundService](/docs/reference/engine/classes/SoundService) when
simulating the Doppler effect for [Sounds](/docs/reference/engine/classes/Sound). This impacts any
[Sound](/docs/reference/engine/classes/Sound) parented to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment).

By default, this property is 3.33, meaning that a meter is considered
3.33 studs for the purposes of simulating the Doppler effect. The greater
the [DistanceFactor](/docs/reference/engine/classes/SoundService#DistanceFactor), the faster the
listener has to travel relative to [Sounds](/docs/reference/engine/classes/Sound) in order to
experience the same Doppler shift.

It's recommended that you only change this property if the objects in your
experience are scaled differently from what they represent. For example,
if your character is meant to be very small (but is normal-sized in the
engine), you may want to increase [SoundService.DistanceFactor](/docs/reference/engine/classes/SoundService#DistanceFactor).

Note that this does not impact the behavior of instances in the advanced
audio system, such as [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) or [AudioEmitter](/docs/reference/engine/classes/AudioEmitter).

Provide feedback

---

DopplerScale

Read Parallel

Degree to which the pitch of a [Sound](/docs/reference/engine/classes/Sound) varies due to the Doppler
effect.

SoundService.DopplerScale:[number](/docs/luau/numbers)

This property determines the degree to which the pitch of a [Sound](/docs/reference/engine/classes/Sound)
varies due to the Doppler effect. This impacts any [Sound](/docs/reference/engine/classes/Sound) parented
to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment).

The Doppler effect is a phenomenon whereby the pitch of a sound changes as
the source and observer of the sound move further away or closer together,
which is stronger the more quickly they are moving. Increasing
[SoundService.DopplerScale](/docs/reference/engine/classes/SoundService#DopplerScale) exaggerates the impact of this effect,
whereas decreasing it minimizes it. By default, the value of this property
is 1.

Note that this does not impact the behavior of instances in the advanced
audio system, such as [AudioPlayer](/docs/reference/engine/classes/AudioPlayer) or [AudioEmitter](/docs/reference/engine/classes/AudioEmitter).

Provide feedback

---

RespectFilteringEnabled

Read Parallel

Sets whether [Sound](/docs/reference/engine/classes/Sound) playback from a client will replicate to the
server.

SoundService.RespectFilteringEnabled:[boolean](/docs/luau/booleans)

This property determines whether [Sound](/docs/reference/engine/classes/Sound) playback is replicated from
the client to the server, and therefore from the server. In other words,
when a [LocalScript](/docs/reference/engine/classes/LocalScript) calls [Play()](/docs/reference/engine/classes/Sound#Play) and this
property is true, the sound will only play on the respective client. If
this property is false, other clients will also hear the sound.

Default is true, meaning filtering is enabled.

Provide feedback

---

RolloffScale

Read Parallel

Determines how fast the volume of a [Sound](/docs/reference/engine/classes/Sound) attenuates beyond its
[Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance).

SoundService.RolloffScale:[number](/docs/luau/numbers)

Determines how fast the volume of a spatialized [Sound](/docs/reference/engine/classes/Sound) attenuates.
This impacts any [Sound](/docs/reference/engine/classes/Sound) parented to a [BasePart](/docs/reference/engine/classes/BasePart) or
[Attachment](/docs/reference/engine/classes/Attachment).

A higher [RolloffScale](/docs/reference/engine/classes/SoundService#RolloffScale) means the volume
of a [Sound](/docs/reference/engine/classes/Sound) will attenuate more rapidly as the distance between the
listener and the [Sound](/docs/reference/engine/classes/Sound) grows. More precisely, the volume of
the [Sound](/docs/reference/engine/classes/Sound) will still start attenuating at a distance equal to
[Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance), but the attenuation curve will be
steeper or more gradual based on the value of
[RolloffScale](/docs/reference/engine/classes/SoundService#RolloffScale). Note that the
[Sound](/docs/reference/engine/classes/Sound) will still be inaudible past its the
[Sound.RollOffMaxDistance](/docs/reference/engine/classes/Sound#RollOffMaxDistance) regardless of the value of
[SoundService.RolloffScale](/docs/reference/engine/classes/SoundService#RolloffScale).

Note that this property does not affect the behavior of instances in the
advanced audio system, such as [AudioEmitter](/docs/reference/engine/classes/AudioEmitter). See
[AudioEmitter:SetDistanceAttenuation()](/docs/reference/engine/classes/AudioEmitter#SetDistanceAttenuation) for a way to apply custom
attenuation in that system.

Provide feedback

---

VolumetricAudio

Not Scriptable

Read Parallel

Determines whether certain spatialized [Sounds](/docs/reference/engine/classes/Sound) emit
volumetrically, throughout the space of their parent object.

SoundService.VolumetricAudio:[Enum.VolumetricAudio](/docs/reference/engine/enums/VolumetricAudio)

Determines whether any [Sounds](/docs/reference/engine/classes/Sound) parented to a [Part](/docs/reference/engine/classes/Part)
emit volumetrically. If set to [Enum.VolumetricAudio.Enabled](/docs/reference/engine/enums/VolumetricAudio#Enabled), the
[Sound](/docs/reference/engine/classes/Sound) will simulate being emitted from every point in the interior
of the [Part](/docs/reference/engine/classes/Part). If set to [Enum.VolumetricAudio.Disabled](/docs/reference/engine/enums/VolumetricAudio#Disabled), the
[Sound](/docs/reference/engine/classes/Sound) will only emit from a single point in the center of the
[Part](/docs/reference/engine/classes/Part).

Note that this does not impact [Sounds](/docs/reference/engine/classes/Sound) parented to other
objects, such as [Attachments](/docs/reference/engine/classes/Attachment) or
[MeshParts](/docs/reference/engine/classes/MeshPart). This also does not impact the behavior of
instances in the advanced audio system such as [AudioEmitter](/docs/reference/engine/classes/AudioEmitter).

Provide feedback

---

Methods

GetListener

Returns the current listener type used by [Sounds](/docs/reference/engine/classes/Sound), as well as
what that listener is currently set to.

SoundService:GetListener():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

A table containing two results. The first result is the listener's
[Enum.ListenerType](/docs/reference/engine/enums/ListenerType) and the second result is dependent on that type:

| Listener Type | Description |
| --- | --- |
| [Enum.ListenerType.Camera](/docs/reference/engine/enums/ListenerType#Camera) | Does not return a listener object as [CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) is always used. |
| [Enum.ListenerType.CFrame](/docs/reference/engine/enums/ListenerType#CFrame) | Returns the [CFrame](/docs/reference/engine/datatypes/CFrame) used in [SetListener()](/docs/reference/engine/classes/SoundService#SetListener). |
| [Enum.ListenerType.ObjectPosition](/docs/reference/engine/enums/ListenerType#ObjectPosition) | Returns the [BasePart](/docs/reference/engine/classes/BasePart) used in [SetListener()](/docs/reference/engine/classes/SoundService#SetListener). |
| [Enum.ListenerType.ObjectCFrame](/docs/reference/engine/enums/ListenerType#ObjectCFrame) | Returns the [BasePart](/docs/reference/engine/classes/BasePart) used in [SetListener()](/docs/reference/engine/classes/SoundService#SetListener). |

Returns the current listener type used by [Sounds](/docs/reference/engine/classes/Sound) and what
object or position that listener is currently set to. This is the point
from which [Sound](/docs/reference/engine/classes/Sound) audio in the experience is heard by the player.
By default, the listener is set to [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). The
listener can be changed using
[SetListener()](/docs/reference/engine/classes/SoundService#SetListener).

Note that this does not affect the listener location when using the
advanced audio system. See [AudioListener](/docs/reference/engine/classes/AudioListener) for a way to set the
listener location in that system.

Provide feedback

---

OpenAttenuationCurveEditor

Plugin Security

Opens the attenuation curve editor in Studio for the provided
[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) or [AudioListener](/docs/reference/engine/classes/AudioListener) instances.

SoundService:OpenAttenuationCurveEditor(selectedCurveObjects:Instances):()

Parameters

|  |
| --- |
| selectedCurveObjects:Instances  A list of [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) or [AudioListeners](/docs/reference/engine/classes/AudioListener). |

Returns

()

Opens the attenuation curve editor in Studio for the provided
[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) or [AudioListener](/docs/reference/engine/classes/AudioListener) instances.

Provide feedback

---

OpenDirectionalCurveEditor

Plugin Security

Opens the directional curve editor in Studio for the provided
[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) or [AudioListener](/docs/reference/engine/classes/AudioListener) instances.

SoundService:OpenDirectionalCurveEditor(selectedCurveObjects:Instances):()

Parameters

|  |
| --- |
| selectedCurveObjects:Instances  A list of [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) or [AudioListeners](/docs/reference/engine/classes/AudioListener). |

Returns

()

Opens the directional curve editor in Studio for the provided
[AudioEmitter](/docs/reference/engine/classes/AudioEmitter) or [AudioListener](/docs/reference/engine/classes/AudioListener) instances.

Provide feedback

---

PlayLocalSound

Plays a copy of a [Sound](/docs/reference/engine/classes/Sound) locally, such that it will only be heard
by the client calling this method.

SoundService:PlayLocalSound(sound:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| sound:[Instance](/docs/reference/engine/datatypes/Instance)  The [Sound](/docs/reference/engine/classes/Sound) to be played. |

Returns

()

Plays a copy of a [Sound](/docs/reference/engine/classes/Sound) locally. The [Sound](/docs/reference/engine/classes/Sound) will only be
heard by the client calling this method, regardless of where it's parented
to.

Some properties of the [Sound](/docs/reference/engine/classes/Sound) will be carried over into the copy.
These include its [Sound.Volume](/docs/reference/engine/classes/Sound#Volume), [Sound.TimePosition](/docs/reference/engine/classes/Sound#TimePosition),
[Sound.PlaybackSpeed](/docs/reference/engine/classes/Sound#PlaybackSpeed), and any spatialization and effects that are
applied to it, including through [SoundGroups](/docs/reference/engine/classes/Sound#SoundGroup).
Properties that do not affect the copy include [Sound.Looped](/docs/reference/engine/classes/Sound#Looped) and
[SoundService.AmbientReverb](/docs/reference/engine/classes/SoundService#AmbientReverb).

Provide feedback

---

SetListener

Sets the listener used by [Sounds](/docs/reference/engine/classes/Sound).

SoundService:SetListener(

listenerType:[Enum.ListenerType](/docs/reference/engine/enums/ListenerType), listener:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| listenerType:[Enum.ListenerType](/docs/reference/engine/enums/ListenerType)  The [Enum.ListenerType](/docs/reference/engine/enums/ListenerType) of the listener. |
| listener:[Tuple](/docs/luau/tuples)  Dependent on the [Enum.ListenerType](/docs/reference/engine/enums/ListenerType). Use a [BasePart](/docs/reference/engine/classes/BasePart) for [Enum.ListenerType.ObjectPosition](/docs/reference/engine/enums/ListenerType#ObjectPosition) or [Enum.ListenerType.ObjectCFrame](/docs/reference/engine/enums/ListenerType#ObjectCFrame), a [CFrame](/docs/reference/engine/datatypes/CFrame) for [Enum.ListenerType.CFrame](/docs/reference/engine/enums/ListenerType#CFrame), or nil for [Enum.ListenerType.Camera](/docs/reference/engine/enums/ListenerType#Camera). |

Returns

()

Sets the listener type for any [Sounds](/docs/reference/engine/classes/Sound) in the experience,
which defines the point from which [Sound](/docs/reference/engine/classes/Sound) audio in the experience
is heard by the player. For [Sounds](/docs/reference/engine/classes/Sound) parented to a
[BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment), the listener influences the volume
and left/right balance of a playing sound. By default, this listener is
set to [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera).

Note that this does not affect the listener location when using the
advanced audio system. See [AudioListener](/docs/reference/engine/classes/AudioListener) for a way to set the
listener location in that system.

Provide feedback

---