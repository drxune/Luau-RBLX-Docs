# Sound | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Sound
Scraped: 2026-01-11T02:37:42.197345Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Sound
- BasePart
- Attachment
- SoundGroup
- BasePart.Position
- Attachment.WorldPosition
- Camera
- RollOffMode
- Sound.IsPlaying
- Loaded
- Pause()
- Stop()
- IsPaused
- IsPlaying
- Play()
- DidLoop
- PlaybackRegion
- LoopRegion.Min
- PlaybackRegion.Min
- LoopRegion.Max
- PlaybackRegion.Max
- TimeLength
- Sound.TimeLength
- LoopRegion
- Playing
- TimePosition
- PlayOnRemove
- Sounds
- RollOffMaxDistance
- RollOffMinDistance
- PlaybackSpeed
- Looped
- Volume
- SoundGroup.Volume
- Resume()
- SoundId
- Stopped
- IsLoaded
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Sound](/docs/reference/engine/classes/Sound)

English

Feedback

Engine Class

![Sound](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Sound-Dark.webp)Sound

An object that emits sound. This object can be placed within a
[BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) to emit a sound from a particular
position within a place or world, or it can be attached elsewhere to play the
sound at a constant volume throughout the entire place.

---

Summary

Properties

|  |
| --- |
| [AudioContent](#AudioContent):[Content](/docs/reference/engine/datatypes/Content) |
| [ChannelCount](#ChannelCount):[number](/docs/luau/numbers) |
| [EmitterSize](#EmitterSize):[number](/docs/luau/numbers)  Deprecated |
| [IsLoaded](#IsLoaded):[boolean](/docs/luau/booleans) |
| [IsMutedForCapture](#IsMutedForCapture):[boolean](/docs/luau/booleans) |
| [IsPaused](#IsPaused):[boolean](/docs/luau/booleans) |
| [IsPlaying](#IsPlaying):[boolean](/docs/luau/booleans) |
| [isPlaying](#isPlaying):[boolean](/docs/luau/booleans)  Deprecated |
| [Looped](#Looped):[boolean](/docs/luau/booleans) |
| [LoopRegion](#LoopRegion):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [MaxDistance](#MaxDistance):[number](/docs/luau/numbers)  Deprecated |
| [MinDistance](#MinDistance):[number](/docs/luau/numbers)  Deprecated |
| [Pitch](#Pitch):[number](/docs/luau/numbers)  Deprecated |
| [PlaybackLoudness](#PlaybackLoudness):[number](/docs/luau/numbers) |
| [PlaybackRegion](#PlaybackRegion):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [PlaybackRegionsEnabled](#PlaybackRegionsEnabled):[boolean](/docs/luau/booleans) |
| [PlaybackSpeed](#PlaybackSpeed):[number](/docs/luau/numbers) |
| [Playing](#Playing):[boolean](/docs/luau/booleans) |
| [PlayOnRemove](#PlayOnRemove):[boolean](/docs/luau/booleans) |
| [RollOffMaxDistance](#RollOffMaxDistance):[number](/docs/luau/numbers) |
| [RollOffMinDistance](#RollOffMinDistance):[number](/docs/luau/numbers) |
| [RollOffMode](#RollOffMode):[Enum.RollOffMode](/docs/reference/engine/enums/RollOffMode) |
| [SoundGroup](#SoundGroup):[SoundGroup](/docs/reference/engine/classes/SoundGroup) |
| [SoundId](#SoundId):ContentId |
| [TimeLength](#TimeLength):[number](/docs/luau/numbers) |
| [TimePosition](#TimePosition):[number](/docs/luau/numbers) |
| [Volume](#Volume):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Pause](#Pause)():() |
| [pause](#pause)():()  Deprecated |
| [Play](#Play)():() |
| [play](#play)():()  Deprecated |
| [Resume](#Resume)():() |
| [Stop](#Stop)():() |
| [stop](#stop)():()  Deprecated |

Events

|  |
| --- |
| [DidLoop](#DidLoop)(soundId: [string](/docs/luau/strings),numOfTimesLooped: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Ended](#Ended)(soundId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Loaded](#Loaded)(soundId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Paused](#Paused)(soundId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Played](#Played)(soundId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Resumed](#Resumed)(soundId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Stopped](#Stopped)(soundId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[Sound](/docs/reference/engine/classes/Sound) is an object that emits sound. When placed in a [BasePart](/docs/reference/engine/classes/BasePart)
or an [Attachment](/docs/reference/engine/classes/Attachment), this object will emit its sound from that part's
[BasePart.Position](/docs/reference/engine/classes/BasePart#Position) or the attachment's
[Attachment.WorldPosition](/docs/reference/engine/classes/Attachment#WorldPosition). In this placement, a [Sound](/docs/reference/engine/classes/Sound) exhibits
the Doppler effect, meaning its frequency and pitch varies with the relative
motion of whatever attachment or part it is attached to. Additionally, its
volume will be determined by the distance between the client's sound listener
(by default the [Camera](/docs/reference/engine/classes/Camera) position) and the position of the sound's
parent. For more information, see [RollOffMode](/docs/reference/engine/classes/Sound#RollOffMode).

A sound is considered "global" if it is not parented to a [BasePart](/docs/reference/engine/classes/BasePart)
or an [Attachment](/docs/reference/engine/classes/Attachment). In this case, the sound will play at the same volume
throughout the entire place.

Code Samples

Music Playing Part

The code in this sample demonstrates how a sound parented to a Part or
Attachment will play locally and experience volume drop off the further the
player's camera is away from the part.

A part is instanced, and a sound is instanced and parented to the part. A
click detector is set up on the part that will check if the sound is playing,
using [Sound.IsPlaying](/docs/reference/engine/classes/Sound#IsPlaying) and play or stop the sound depending.

```
local part = Instance.new("Part")



part.Anchored = true



part.Position = Vector3.new(0, 3, 0)



part.BrickColor = BrickColor.new("Bright red")



part.Name = "MusicBox"



part.Parent = workspace



-- create a sound



local sound = Instance.new("Sound", part)



sound.SoundId = "rbxassetid://9120386436"



sound.EmitterSize = 5 -- decrease the emitter size (for earlier volume drop off)



sound.Looped = true



sound.Parent = part



local clickDetector = Instance.new("ClickDetector")



clickDetector.Parent = part



-- toggle the sound playing / not playing



clickDetector.MouseClick:Connect(function()



if not sound.IsPlaying then



part.BrickColor = BrickColor.new("Bright green")



sound:Play()



else



part.BrickColor = BrickColor.new("Bright red")



sound:Stop()



end



end)
```

---

API Reference

Properties

AudioContent

Read Parallel

Sound.AudioContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

ChannelCount

Read Only

Not Replicated

Not Browsable

Roblox Script Security

Read Parallel

Sound.ChannelCount:[number](/docs/luau/numbers)

Provide feedback

---

EmitterSize

Deprecated

Show details

---

IsLoaded

Read Only

Not Replicated

Read Parallel

This property is true when the [Sound](/docs/reference/engine/classes/Sound) has loaded from Roblox
servers and is ready to play.

Sound.IsLoaded:[boolean](/docs/luau/booleans)

This property is true when the [Sound](/docs/reference/engine/classes/Sound) has loaded from Roblox
servers and is ready to play. You can use this property and the
[Loaded](/docs/reference/engine/classes/Sound#Loaded) event to verify a sound has loaded before
playing it.

Code Samples

Load Sound

This simple function will verify a Sound has loaded by checking the
Sound.IsLoaded property. If Sound.IsLoaded is false it will wait for the
Loaded event before resuming.

It is important to check Sound.IsLoaded before connecting to the Sound.Loaded
event, as if the sound has already loaded the Sound.Loaded event will not fire
and the function will yield indefinitely.

```
local sound = script.Parent.Sound



if not sound.IsLoaded then



sound.Loaded:Wait()



end



print("The sound has loaded!")
```

Provide feedback

---

IsMutedForCapture

Roblox Script Security

Read Parallel

Sound.IsMutedForCapture:[boolean](/docs/luau/booleans)

Provide feedback

---

IsPaused

Hidden

Read Only

Not Replicated

Read Parallel

Read-only property which returns true when the [Sound](/docs/reference/engine/classes/Sound) is not
playing.

Sound.IsPaused:[boolean](/docs/luau/booleans)

This read-only property returns true when the [Sound](/docs/reference/engine/classes/Sound) is not
playing. Note that it can return true if a sound has been paused using
[Pause()](/docs/reference/engine/classes/Sound#Pause), if it has been stopped using
[Stop()](/docs/reference/engine/classes/Sound#Stop), or the sound has never been played.

As [IsPaused](/docs/reference/engine/classes/Sound#IsPaused) is read-only, it cannot be used to stop
the sound; [Stop()](/docs/reference/engine/classes/Sound#Stop) or [Pause()](/docs/reference/engine/classes/Sound#Pause)
should be used instead.

Code Samples

Sound IsPlaying and SoundIsPaused

This code sample contains demonstrates when the Sound.IsPlaying and
Sound.IsPaused properties will be true or false.

A sound is instanced in the Workspace and the Sound.IsLoaded property is
checked to ensure it has loaded, if it has not the Sound.Loaded event is used
to yield the script until the sound has.

As the sound is played, paused and stopped the Sound.IsPlaying and
Sound.IsPaused properties are printed to demonstrate how they respond to each
of these functions. Note Sound.IsPaused will always be true if even if the
sound has been stopped rather than paused.

```
local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



sound.Looped = true



sound.Parent = workspace



if not sound.isLoaded then



sound.Loaded:Wait()



end



sound:Play()



print(sound.IsPlaying, sound.IsPaused) -- true, false



task.wait(2)



sound:Pause()



print(sound.IsPlaying, sound.IsPaused) -- false, true



task.wait(2)



sound:Play()



print(sound.IsPlaying, sound.IsPaused) -- true, false



task.wait(2)



sound:Stop()



print(sound.IsPlaying, sound.IsPaused) -- false, true
```

Provide feedback

---

IsPlaying

Hidden

Read Only

Not Replicated

Read Parallel

Read-only property which returns true when the [Sound](/docs/reference/engine/classes/Sound) is playing.

Sound.IsPlaying:[boolean](/docs/luau/booleans)

This read-only property returns true when the [Sound](/docs/reference/engine/classes/Sound) is playing.

As [IsPlaying](/docs/reference/engine/classes/Sound#IsPlaying) is read-only, it cannot be used to
play the sound; [Play()](/docs/reference/engine/classes/Sound#Play) should be used instead.

Code Samples

Sound IsPlaying and SoundIsPaused

This code sample contains demonstrates when the Sound.IsPlaying and
Sound.IsPaused properties will be true or false.

A sound is instanced in the Workspace and the Sound.IsLoaded property is
checked to ensure it has loaded, if it has not the Sound.Loaded event is used
to yield the script until the sound has.

As the sound is played, paused and stopped the Sound.IsPlaying and
Sound.IsPaused properties are printed to demonstrate how they respond to each
of these functions. Note Sound.IsPaused will always be true if even if the
sound has been stopped rather than paused.

```
local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



sound.Looped = true



sound.Parent = workspace



if not sound.isLoaded then



sound.Loaded:Wait()



end



sound:Play()



print(sound.IsPlaying, sound.IsPaused) -- true, false



task.wait(2)



sound:Pause()



print(sound.IsPlaying, sound.IsPaused) -- false, true



task.wait(2)



sound:Play()



print(sound.IsPlaying, sound.IsPaused) -- true, false



task.wait(2)



sound:Stop()



print(sound.IsPlaying, sound.IsPaused) -- false, true
```

Provide feedback

---

isPlaying

Deprecated

Show details

---

Looped

Read Parallel

Sets whether or not the [Sound](/docs/reference/engine/classes/Sound) repeats once it has finished
playing.

Sound.Looped:[boolean](/docs/luau/booleans)

This sets whether or not the [Sound](/docs/reference/engine/classes/Sound) repeats once it has finished
playing. Looped sounds are suitable for a range of applications including
music and background ambient sounds.

The [DidLoop](/docs/reference/engine/classes/Sound#DidLoop) event can be used to track the number of
times as sound has looped.

Code Samples

Loop a Number of Times

This code sample includes a function that will play a sound and allow it to
loop for a given number of times before stopping it.

```
local function loopNTimes(sound, numberOfLoops)



if not sound.IsPlaying then



sound.Looped = true



local connection = nil



connection = sound.DidLoop:Connect(function(_soundId, numOfTimesLooped)



print(numOfTimesLooped)



if numOfTimesLooped >= numberOfLoops then



-- disconnect the connection



connection:Disconnect()



-- stop the sound



sound:Stop()



end



end)



sound:Play()



end



end



local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://0"



loopNTimes(sound, 5)
```

Provide feedback

---

LoopRegion

Read Parallel

A range denoting a desired loop start and loop end within the
[PlaybackRegion](/docs/reference/engine/classes/Sound#PlaybackRegion), in seconds.

Sound.LoopRegion:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

A range denoting a desired loop start and loop end within the
[PlaybackRegion](/docs/reference/engine/classes/Sound#PlaybackRegion), in seconds.

* If [LoopRegion.Min](/docs/reference/engine/classes/Sound#LoopRegion) >
  [PlaybackRegion.Min](/docs/reference/engine/classes/Sound#PlaybackRegion), the loop starts from
  [LoopRegion.Min](/docs/reference/engine/classes/Sound#LoopRegion).
* If [LoopRegion.Min](/docs/reference/engine/classes/Sound#LoopRegion) <
  [PlaybackRegion.Min](/docs/reference/engine/classes/Sound#PlaybackRegion), the loop starts from
  [PlaybackRegion.Min](/docs/reference/engine/classes/Sound#PlaybackRegion).
* If [LoopRegion.Max](/docs/reference/engine/classes/Sound#LoopRegion) >
  [PlaybackRegion.Max](/docs/reference/engine/classes/Sound#PlaybackRegion), the loop starts at
  [PlaybackRegion.Max](/docs/reference/engine/classes/Sound#PlaybackRegion).
* If [LoopRegion.Max](/docs/reference/engine/classes/Sound#LoopRegion) <
  [PlaybackRegion.Max](/docs/reference/engine/classes/Sound#PlaybackRegion), the loop starts at
  exactly that time.
* If [LoopRegion.Min](/docs/reference/engine/classes/Sound#LoopRegion) ==
  [LoopRegion.Max](/docs/reference/engine/classes/Sound#LoopRegion), the [Sound](/docs/reference/engine/classes/Sound) uses the
  [PlaybackRegion](/docs/reference/engine/classes/Sound#PlaybackRegion) property instead.

Provide feedback

---

MaxDistance

Deprecated

Show details

---

MinDistance

Deprecated

Show details

---

Pitch

Deprecated

Show details

---

PlaybackLoudness

Read Only

Not Replicated

Read Parallel

A number between 0 and 1000 indicating how loud the [Sound](/docs/reference/engine/classes/Sound) is
currently playing back.

Sound.PlaybackLoudness:[number](/docs/luau/numbers)

A number between 0 and 1000 indicating how loud the [Sound](/docs/reference/engine/classes/Sound) is
currently playing back. This property reflects the amplitude of the
sound's playback in the instance of time it is read.

Code Samples

Volume Amplitude Bar

In this sample Sound.PlaybackLoudness is used to create an amplitude bar that
shows the amplitude of a sound playing.

This code sample should be placed in StarterPlayerScripts.

A simple GUI is created, a frame holding that bar and a frame containing the
bar. A Sound is then played and the size of the bar is set to reflect the
Sound.PlaybackLoudness on a loop.

```
-- to be placed in StarterPlayer > StarterPlayerScripts



local Players = game:GetService("Players")



-- wait for local player PlayerGui



local LocalPlayer = Players.LocalPlayer



local playerGui = LocalPlayer:WaitForChild("PlayerGui")



-- create a ScreenGui



local screenGui = Instance.new("ScreenGui")



screenGui.Parent = playerGui



-- create a holder for our bar



local frame = Instance.new("Frame")



frame.AnchorPoint = Vector2.new(0.5, 0.5)



frame.Position = UDim2.new(0.5, 0, 0.5, 0)



frame.Size = UDim2.new(0.3, 0, 0.05, 0)



frame.Parent = screenGui



-- create a bar



local bar = Instance.new("Frame")



bar.Position = UDim2.new(0, 0, 0, 0)



bar.Size = UDim2.new(1, 0, 1, 0)



bar.BackgroundColor3 = Color3.new(0, 1, 0)



bar.Parent = frame



-- create a sound



local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



sound.Looped = true



sound.Parent = screenGui



sound:Play()



-- define a max loudness



local maxLoudness = 30



-- animate the amplitude bar



while true do



local amplitude = math.clamp(sound.PlaybackLoudness / maxLoudness, 0, 1)



bar.Size = UDim2.new(amplitude, 0, 1, 0)



wait(0.05)



end
```

Provide feedback

---

PlaybackRegion

Read Parallel

A range denoting a desired start and stop time within the
[TimeLength](/docs/reference/engine/classes/Sound#TimeLength), in seconds.

Sound.PlaybackRegion:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

A range denoting a desired start and stop time within the
[TimeLength](/docs/reference/engine/classes/Sound#TimeLength), in seconds.

* If [PlaybackRegion.Min](/docs/reference/engine/classes/Sound#PlaybackRegion) > 0, the sound
  begins to play from the [PlaybackRegion.Min](/docs/reference/engine/classes/Sound#PlaybackRegion)
  time.
* If [PlaybackRegion.Min](/docs/reference/engine/classes/Sound#PlaybackRegion) < 0, the sound
  begins to play from 0.
* If [PlaybackRegion.Max](/docs/reference/engine/classes/Sound#PlaybackRegion) >
  [Sound.TimeLength](/docs/reference/engine/classes/Sound#TimeLength), the sound stops at [Sound.TimeLength](/docs/reference/engine/classes/Sound#TimeLength).
* If [PlaybackRegion.Max](/docs/reference/engine/classes/Sound#PlaybackRegion) <
  [Sound.TimeLength](/docs/reference/engine/classes/Sound#TimeLength), the sound stops at exactly that time.
* If [PlaybackRegion.Min](/docs/reference/engine/classes/Sound#PlaybackRegion) ==
  [PlaybackRegion.Max](/docs/reference/engine/classes/Sound#PlaybackRegion), this property is
  inactive.

Provide feedback

---

PlaybackRegionsEnabled

Read Parallel

If true, this property gives your [Sound](/docs/reference/engine/classes/Sound) access to the
[PlaybackRegion](/docs/reference/engine/classes/Sound#PlaybackRegion) and
[LoopRegion](/docs/reference/engine/classes/Sound#LoopRegion) properties which can more-accurately
control its playback.

Sound.PlaybackRegionsEnabled:[boolean](/docs/luau/booleans)

If true, this property gives your [Sound](/docs/reference/engine/classes/Sound) access to the
[PlaybackRegion](/docs/reference/engine/classes/Sound#PlaybackRegion) and
[LoopRegion](/docs/reference/engine/classes/Sound#LoopRegion) properties which can more-accurately
control its playback.

Provide feedback

---

PlaybackSpeed

Not Replicated

Read Parallel

Determines the speed at which a [Sound](/docs/reference/engine/classes/Sound) will play, with higher
values causing the sound to play faster and at a higher pitch.

Sound.PlaybackSpeed:[number](/docs/luau/numbers)

Determines the speed at which a [Sound](/docs/reference/engine/classes/Sound) will play, with higher
values causing the sound to play faster and at a higher pitch.

Code Samples

Sound PlaybackSpeed

In this example a Sound is played in the Workspace. The PlaybackSpeed property
is increased and decreased at intervals to demonstrate its impact on the
playback of the Sound.

```
local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



sound.Looped = true



sound.Parent = workspace



sound:Play()



task.wait(10)



sound.PlaybackSpeed = 3 -- 3x faster



task.wait(5)



sound.PlaybackSpeed = 0.5 -- 2x slower



task.wait(5)



sound.PlaybackSpeed = 1 -- default
```

Provide feedback

---

Playing

Not Replicated

Read Parallel

Indicates whether the [Sound](/docs/reference/engine/classes/Sound) is currently playing.

Sound.Playing:[boolean](/docs/luau/booleans)

Indicates whether the [Sound](/docs/reference/engine/classes/Sound) is currently playing. This can be
toggled, and this property will always replicate.

In Studio's [Properties](/docs/studio/properties) window, while in
Edit mode, toggling [Playing](/docs/reference/engine/classes/Sound#Playing) to true does not
begin playing the sound, but the sound will begin playing during runtime.

This property should not be confused with
[IsPlaying](/docs/reference/engine/classes/Sound#IsPlaying) which is a read-only property.

Note that when [Playing](/docs/reference/engine/classes/Sound#Playing) is set to false, the
[TimePosition](/docs/reference/engine/classes/Sound#TimePosition) property of the sound will not
reset, meaning that when [Playing](/docs/reference/engine/classes/Sound#Playing) is set to true
again, the audio will continue from the time position it was at when it
was stopped. However, if the [Play()](/docs/reference/engine/classes/Sound#Play) function is used
to resume the sound, the time position will reset to 0.

Code Samples

Sound Playing

This sample demonstrates how the Sound.Playing property can be used to start
and stop playback of a sound.

A sound is instanced in the Workspace and playback is started by setting
Sound.Playing to true. After ten seconds the playback is stopped by setting
Sound.Playing to false. When the playback is again resumed using Sound.Playing
it resumes at the previous Sound.TimePosition it was stopped at. This is
demonstrated by printing the TimePosition property immediately after resuming
the sound.

```
local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



sound.Looped = true



sound.Parent = workspace



print("playing sound")



sound.Playing = true



task.wait(10)



print("stopping sound")



sound.Playing = false



task.wait(5)



sound.Playing = true



local timePosition = sound.TimePosition



print("resumed at time position: " .. tostring(timePosition)) -- c. 10 seconds
```

Provide feedback

---

PlayOnRemove

Read Parallel

When true, the [Sound](/docs/reference/engine/classes/Sound) will play when it is removed from the
experience.

Sound.PlayOnRemove:[boolean](/docs/luau/booleans)

When true, the [Sound](/docs/reference/engine/classes/Sound) will play when it is removed from the
experience by parenting the [Sound](/docs/reference/engine/classes/Sound) or one if its ancestors to
nil. This means all of the following will cause the sound to play when
[PlayOnRemove](/docs/reference/engine/classes/Sound#PlayOnRemove) is true:

* sound:Destroy()
* sound.Parent = nil
* sound.Parent.Parent = nil

Provide feedback

---

RollOffMaxDistance

Read Parallel

The maximum distance, in studs, a client's listener can be from the
sound's origin and still hear it. Only applies to [Sounds](/docs/reference/engine/classes/Sound)
parented to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment).

Sound.RollOffMaxDistance:[number](/docs/luau/numbers)

The maximum distance, in studs, a client's listener can be from the
sound's origin and still hear it. Only applies to [Sounds](/docs/reference/engine/classes/Sound)
parented to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment).

How [RollOffMaxDistance](/docs/reference/engine/classes/Sound#RollOffMaxDistance) impacts the
attenuation of a sound (manner in which it fades out) is dependent on the
[RollOffMode](/docs/reference/engine/classes/Sound#RollOffMode) property.

Provide feedback

---

RollOffMinDistance

Read Parallel

The minimum distance, in studs, at which a [Sound](/docs/reference/engine/classes/Sound) which is parented
to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) will begin to attenuate
(decrease in volume).

Sound.RollOffMinDistance:[number](/docs/luau/numbers)

The minimum distance, in studs, at which a [Sound](/docs/reference/engine/classes/Sound) which is parented
to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) will begin to attenuate
(decrease in volume).

How [RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance) impacts the
attenuation of a sound (manner in which it fades out) is dependent on the
[RollOffMode](/docs/reference/engine/classes/Sound#RollOffMode) property.

Provide feedback

---

RollOffMode

Read Parallel

Controls how the volume of a [Sound](/docs/reference/engine/classes/Sound) which is parented to a
[BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) attenuates (fades out) as the
distance between the listener and parent changes.

Sound.RollOffMode:[Enum.RollOffMode](/docs/reference/engine/enums/RollOffMode)

This property controls how the volume of a [Sound](/docs/reference/engine/classes/Sound) which is parented
to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) attenuates (fades out) as the
distance between the listener and parent changes.

For details on the different modes, see [Enum.RollOffMode](/docs/reference/engine/enums/RollOffMode).

Provide feedback

---

SoundGroup

Read Parallel

The [SoundGroup](/docs/reference/engine/classes/SoundGroup) that is linked to this [Sound](/docs/reference/engine/classes/Sound).

Sound.SoundGroup:[SoundGroup](/docs/reference/engine/classes/SoundGroup)

The [SoundGroup](/docs/reference/engine/classes/SoundGroup) that is linked to this [Sound](/docs/reference/engine/classes/Sound).

Provide feedback

---

SoundId

Read Parallel

Content ID of the sound file to associate with the [Sound](/docs/reference/engine/classes/Sound).

Sound.SoundId:ContentId

This property is the content ID of the sound file to associate with the
[Sound](/docs/reference/engine/classes/Sound). See [Audio Assets](/docs/audio/assets) for more
information.

Provide feedback

---

TimeLength

Read Only

Not Replicated

Read Parallel

The length of the [Sound](/docs/reference/engine/classes/Sound) in seconds.

Sound.TimeLength:[number](/docs/luau/numbers)

The length of the [Sound](/docs/reference/engine/classes/Sound) in seconds. If the [Sound](/docs/reference/engine/classes/Sound) is not
loaded, this value will be 0.

This property is often used in conjunction with
[PlaybackSpeed](/docs/reference/engine/classes/Sound#PlaybackSpeed) to adjust the speed of a sound
so that it lasts for a specific duration.

Code Samples

Play a Sound for a Specific Duration

This code sample includes a simple function that uses Sound.TimeLength and
Sound.PlaybackSpeed to play a sound that'll take the given duration to
complete. It achieves this by setting the PlaybackSpeed of the sound to be
equal to the TimeLength of the sound divided by the desired duration.

Note that as TimeLength is equal to 0 when the sound has not loaded, the
function will yield while it loads the sound.

```
local function playForDuration(sound, duration)



if not sound.IsLoaded then



sound.Loaded:wait()



end



local speed = sound.TimeLength / duration



sound.PlaybackSpeed = speed



sound:Play()



end



local sound = script.Parent



playForDuration(sound, 5)
```

Provide feedback

---

TimePosition

Not Replicated

Read Parallel

Progress of the [Sound](/docs/reference/engine/classes/Sound) in seconds. Can be changed to move the
playback position of the [Sound](/docs/reference/engine/classes/Sound) both before and during playback.

Sound.TimePosition:[number](/docs/luau/numbers)

This property reflects the progress of the [Sound](/docs/reference/engine/classes/Sound) in seconds. It
can be changed to move the playback position of the sound both before and
during playback.

As a [Sound](/docs/reference/engine/classes/Sound) is played, [TimePosition](/docs/reference/engine/classes/Sound#TimePosition)
increases at a rate of [PlaybackSpeed](/docs/reference/engine/classes/Sound#PlaybackSpeed) per
second. Once [TimePosition](/docs/reference/engine/classes/Sound#TimePosition) reaches
[TimeLength](/docs/reference/engine/classes/Sound#TimeLength), the sound will stop unless it is
[Looped](/docs/reference/engine/classes/Sound#Looped).

Note that setting [TimePosition](/docs/reference/engine/classes/Sound#TimePosition) to a value
greater than the length in a looped track will not cause it to wrap
around. If that behavior is desired, consider the following code snippet:

```
local newPosition = 1.5



if newPosition >= sound.TimeLength then



newPosition = newPosition - sound.TimeLength



end



sound.TimePosition = newPosition
```

Code Samples

Sound TimePosition

This sample demonstrates how Sound.TimePosition can be used to jump to
particular points in an audio file both before and during Sound playback.

A Sound is created in the Workspace and set to start at 30 seconds in. During
playback, it jumps forwards to 100 seconds and then back to the start (0
seconds).

```
local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



sound.Parent = workspace



sound.TimePosition = 30



sound:Play()



task.wait(5)



sound.TimePosition = 100



task.wait(5)



sound.TimePosition = 0
```

Provide feedback

---

Volume

Read Parallel

The volume of the [Sound](/docs/reference/engine/classes/Sound).

Sound.Volume:[number](/docs/luau/numbers)

The volume of the [Sound](/docs/reference/engine/classes/Sound). Can be set between 0 and 10 and
defaults to 0.5.

Note that if the [Sound](/docs/reference/engine/classes/Sound) is a member of a [SoundGroup](/docs/reference/engine/classes/SoundGroup), its
playback volume (but not its [Volume](/docs/reference/engine/classes/Sound#Volume) property) will be
influenced by the group's [SoundGroup.Volume](/docs/reference/engine/classes/SoundGroup#Volume) property.

Provide feedback

---

Methods

Pause

Pauses playback of the [Sound](/docs/reference/engine/classes/Sound) if it is playing.

Sound:Pause():()

Returns

()

This method pauses playback of the [Sound](/docs/reference/engine/classes/Sound) if it is playing, setting
[Playing](/docs/reference/engine/classes/Sound#Playing) to false. Unlike
[Stop()](/docs/reference/engine/classes/Sound#Stop), it does not reset
[TimePosition](/docs/reference/engine/classes/Sound#TimePosition), meaning the sound can be resumed
using [Resume()](/docs/reference/engine/classes/Sound#Resume).

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---

pause

Deprecated

Show details

---

Play

Plays the [Sound](/docs/reference/engine/classes/Sound).

Sound:Play():()

Returns

()

This method plays the [Sound](/docs/reference/engine/classes/Sound) and sets
[TimePosition](/docs/reference/engine/classes/Sound#TimePosition) to the last value set by a script
(or 0 if it has not been set), then sets [Playing](/docs/reference/engine/classes/Sound#Playing)
to true.

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---

play

Deprecated

Show details

---

Resume

Resumes the [Sound](/docs/reference/engine/classes/Sound).

Sound:Resume():()

Returns

()

This method resumes the [Sound](/docs/reference/engine/classes/Sound) and sets
[Playing](/docs/reference/engine/classes/Sound#Playing) to true. Does not alter
[TimePosition](/docs/reference/engine/classes/Sound#TimePosition) and thus can be used to resume
playback of a sound paused through [Pause()](/docs/reference/engine/classes/Sound#Pause).

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---

Stop

Stops the [Sound](/docs/reference/engine/classes/Sound).

Sound:Stop():()

Returns

()

This method stops the [Sound](/docs/reference/engine/classes/Sound) and sets [Playing](/docs/reference/engine/classes/Sound#Playing)
to false, then sets [TimePosition](/docs/reference/engine/classes/Sound#TimePosition) to 0.

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---

stop

Deprecated

Show details

---

Events

DidLoop

Fires whenever the [Sound](/docs/reference/engine/classes/Sound) loops.

Sound.DidLoop(

soundId:[string](/docs/luau/strings), numOfTimesLooped:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| soundId:[string](/docs/luau/strings)  The [SoundId](/docs/reference/engine/classes/Sound#SoundId) of the [Sound](/docs/reference/engine/classes/Sound) that looped. |
| numOfTimesLooped:[number](/docs/luau/numbers)  The number of times the [Sound](/docs/reference/engine/classes/Sound) has looped. |

Fires whenever the [Sound](/docs/reference/engine/classes/Sound) loops. Returns soundId and
numOfTimesLooped, giving the content ID of the sound and the number of
times looped respectively.

When the [Sound](/docs/reference/engine/classes/Sound) is stopped through [Stop()](/docs/reference/engine/classes/Sound#Stop), the
looped counter resets meaning the next [DidLoop](/docs/reference/engine/classes/Sound#DidLoop) event
will return 1 for numOfTimesLooped.

Code Samples

Loop a Number of Times

This code sample includes a function that will play a sound and allow it to
loop for a given number of times before stopping it.

```
local function loopNTimes(sound, numberOfLoops)



if not sound.IsPlaying then



sound.Looped = true



local connection = nil



connection = sound.DidLoop:Connect(function(_soundId, numOfTimesLooped)



print(numOfTimesLooped)



if numOfTimesLooped >= numberOfLoops then



-- disconnect the connection



connection:Disconnect()



-- stop the sound



sound:Stop()



end



end)



sound:Play()



end



end



local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://0"



loopNTimes(sound, 5)
```

Provide feedback

---

Ended

Fires when the [Sound](/docs/reference/engine/classes/Sound) has completed playback and stopped.

Sound.Ended(soundId:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| soundId:[string](/docs/luau/strings)  The [SoundId](/docs/reference/engine/classes/Sound#SoundId) of the [Sound](/docs/reference/engine/classes/Sound) that has ended. |

Fires when the [Sound](/docs/reference/engine/classes/Sound) has completed playback and stopped. This
event is often used to destroy a sound when it has completed playback:

```
sound:Play()



sound.Ended:Wait()



sound:Destroy()
```

Note that this event will not fire for sounds with
[Looped](/docs/reference/engine/classes/Sound#Looped) set to true, as they continue playing upon
reaching their end. This event will also not fire when the sound is
stopped before playback has completed; for this use the
[Stopped](/docs/reference/engine/classes/Sound#Stopped) event.

Provide feedback

---

Loaded

Fires when the [Sound](/docs/reference/engine/classes/Sound) is loaded.

Sound.Loaded(soundId:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| soundId:[string](/docs/luau/strings)  The [SoundId](/docs/reference/engine/classes/Sound#SoundId) of the [Sound](/docs/reference/engine/classes/Sound) that loaded. |

Fires when the [Sound](/docs/reference/engine/classes/Sound) is loaded.

As this event only fires at the time the sound is loaded, it's recommended
to check the sound's [IsLoaded](/docs/reference/engine/classes/Sound#IsLoaded) property prior to
connecting to this event.

Code Samples

Load Sound

This simple function will verify a Sound has loaded by checking the
Sound.IsLoaded property. If Sound.IsLoaded is false it will wait for the
Loaded event before resuming.

It is important to check Sound.IsLoaded before connecting to the Sound.Loaded
event, as if the sound has already loaded the Sound.Loaded event will not fire
and the function will yield indefinitely.

```
local sound = script.Parent.Sound



if not sound.IsLoaded then



sound.Loaded:Wait()



end



print("The sound has loaded!")
```

Provide feedback

---

Paused

Fires whenever the [Sound](/docs/reference/engine/classes/Sound) is paused using
[Pause()](/docs/reference/engine/classes/Sound#Pause).

Sound.Paused(soundId:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| soundId:[string](/docs/luau/strings)  The [SoundId](/docs/reference/engine/classes/Sound#SoundId) of the [Sound](/docs/reference/engine/classes/Sound) that was paused. |

Fires whenever the [Sound](/docs/reference/engine/classes/Sound) is paused using
[Pause()](/docs/reference/engine/classes/Sound#Pause).

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---

Played

Fires whenever the [Sound](/docs/reference/engine/classes/Sound) is played using
[Play()](/docs/reference/engine/classes/Sound#Play).

Sound.Played(soundId:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| soundId:[string](/docs/luau/strings)  The [SoundId](/docs/reference/engine/classes/Sound#SoundId) of the [Sound](/docs/reference/engine/classes/Sound) that was played. |

Fires whenever the [Sound](/docs/reference/engine/classes/Sound) is played using
[Play()](/docs/reference/engine/classes/Sound#Play). This event will not fire if the
[Sound](/docs/reference/engine/classes/Sound) is played due to [PlayOnRemove](/docs/reference/engine/classes/Sound#PlayOnRemove)
being set to true and the sound being destroyed.

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---

Resumed

Fires when the [Sound](/docs/reference/engine/classes/Sound) is resumed using
[Resume()](/docs/reference/engine/classes/Sound#Resume).

Sound.Resumed(soundId:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| soundId:[string](/docs/luau/strings)  The [SoundId](/docs/reference/engine/classes/Sound#SoundId) of the [Sound](/docs/reference/engine/classes/Sound) being resumed. |

Fires when the [Sound](/docs/reference/engine/classes/Sound) is resumed using
[Resume()](/docs/reference/engine/classes/Sound#Resume).

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---

Stopped

Fires when the [Sound](/docs/reference/engine/classes/Sound) is stopped through using
[Stop()](/docs/reference/engine/classes/Sound#Stop).

Sound.Stopped(soundId:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| soundId:[string](/docs/luau/strings)  The [SoundId](/docs/reference/engine/classes/Sound#SoundId) of the [Sound](/docs/reference/engine/classes/Sound) that stopped. |

Fires when the [Sound](/docs/reference/engine/classes/Sound) is stopped through using
[Stop()](/docs/reference/engine/classes/Sound#Stop). Destroying a sound while it is playing will
not cause this event to fire.

Code Samples

Sound Functions

This sample gives a simple demonstration of what each of the Sound functions
(Sound.Play, Sound.Stop, Sound.Pause and Sound.Resume) do to Sound.Playing and
Sound.TimePosition.

```
-- create a sound



local sound = Instance.new("Sound", game.Workspace)



sound.SoundId = "rbxassetid://9120386436"



if not sound.IsLoaded then



sound.Loaded:Wait()



end



-- listen for events



sound.Played:Connect(function(_soundId)



print("Sound.Played event")



end)



sound.Paused:Connect(function(_soundId)



print("Sound.Paused event")



end)



sound.Resumed:Connect(function(_soundId)



print("Sound.Resumed event")



end)



sound.Stopped:Connect(function(_soundId)



print("Sound.Stopped event")



end)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0



task.wait(10)



sound:Pause()



print("pause", sound.Playing, sound.TimePosition) -- pause false 10



task.wait(3)



sound:Resume()



print("play", sound.Playing, sound.TimePosition) -- play true 10



task.wait(3)



sound:Stop()



print("stop", sound.Playing, sound.TimePosition) -- stop false 0



task.wait(3)



sound:Play()



print("play", sound.Playing, sound.TimePosition) -- play true 0
```

Provide feedback

---