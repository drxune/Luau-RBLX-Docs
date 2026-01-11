# KeyframeMarker | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/KeyframeMarker
Scraped: 2026-01-11T02:30:02.781126Z

## Inherits
- Instance
- KeyframeMarker
- Keyframe
- Object
- Keyframe:AddMarker()
- Keyframe:RemoveMarker()
- Keyframe:GetMarkers()
- AnimationTrack.GetKeyframeMarkerReached
- KeyframeMarker.Value
- Keyframe.Name
- AnimationTrack:GetMarkerReachedSignal()
- Poses
- Model
- AnimationTrack
- Humanoid
- AnimationController
- Animation
- Animation.AnimationId
- AnimationTrack:Play()
- parenting
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker)

English

Feedback

Engine Class

KeyframeMarker

An instance meant to represent an event that will eventually be fired when a
[Keyframe](/docs/reference/engine/classes/Keyframe) is hit.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A KeyframeMarker is an instance meant to represent an event that will
eventually be fired when a [Keyframe](/docs/reference/engine/classes/Keyframe) is hit.

Using a KeyframeMarker
----------------------

KeyframeMarkers should always be parented to a Keyframe via setting the parent
directly or using the [Keyframe:AddMarker()](/docs/reference/engine/classes/Keyframe#AddMarker) function of Keyframe.
KeyframeMarkers can also be removed directly or using the
[Keyframe:RemoveMarker()](/docs/reference/engine/classes/Keyframe#RemoveMarker) function, and polled to check which markers
are attached to a specific Keyframe using [Keyframe:GetMarkers()](/docs/reference/engine/classes/Keyframe#GetMarkers).

Whenever a Keyframe is detected as an animation is running, there will be an
event fired for each KeyframeMarker that is parented to the Keyframe. These
events are identifiable by the name of the KeyframeMarker. You can retrieve
and listen to these events using the
[AnimationTrack.GetKeyframeMarkerReached](/docs/reference/engine/classes/AnimationTrack#GetKeyframeMarkerReached) function. Optionally, you may
set the [KeyframeMarker.Value](/docs/reference/engine/classes/KeyframeMarker#Value) property of the KeyframeMarker in order
to pass along a value with the event being fired.

It inherits the [Keyframe.Name](/docs/reference/engine/classes/Instance#Name) property from
[Instance](/docs/reference/engine/classes/Instance) and behaves identically. Names are used for identification
and do not need to be unique. When multiple KeyframeMarker instances with
the same name are attached to a [Keyframe](/docs/reference/engine/classes/Keyframe), events such as the one
returned by [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal) will fire for
every marker.

See also:

* [Keyframe](/docs/reference/engine/classes/Keyframe), holds the [Poses](/docs/reference/engine/classes/Pose) applied to joints in a
  [Model](/docs/reference/engine/classes/Model) at a given point of time in an animation
* [AnimationTrack](/docs/reference/engine/classes/AnimationTrack), controls the playback of an animation on a
  [Humanoid](/docs/reference/engine/classes/Humanoid) or [AnimationController](/docs/reference/engine/classes/AnimationController)
* [Animation](/docs/reference/engine/classes/Animation), holds a reference to animation data required to play
  custom animations on characters or other models using the Roblox animation
  system

Code Samples

Get Keyframe Markers Attached to a Keyframe

This example demonstrates the [Keyframe:AddMarker()](/docs/reference/engine/classes/Keyframe#AddMarker) and
[Keyframe:GetMarkers()](/docs/reference/engine/classes/Keyframe#GetMarkers) functions. After adding two markers, *marker1*
and *marker2* to the keyframe, this example gets and prints the names of the
added markers.

```
local keyframe = Instance.new("Keyframe")



keyframe.Parent = workspace



local marker1 = Instance.new("KeyframeMarker")



marker1.Name = "FootStep"



marker1.Value = 100



local marker2 = Instance.new("KeyframeMarker")



marker2.Name = "Wave"



marker2.Value = 100



keyframe:AddMarker(marker1) --marker.Parent = keyframe



keyframe:AddMarker(marker2) --marker.Parent = keyframe



local markers = keyframe:GetMarkers()



for _, marker in pairs(markers) do



print(marker.Name)



end
```

Listening to Keyframe Markers

This LocalScript code waits for the local player's Humanoid object to
load, then it creates a new Animation instance with the proper
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId). The animation is then loaded onto the humanoid,
creating an AnimationTrack, and the track is played with
[AnimationTrack:Play()](/docs/reference/engine/classes/AnimationTrack#Play). Following that, the
[AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal) function detects when the
"KickEnd" marker is hit.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.Character:Wait()



local humanoid = character:WaitForChild("Humanoid")



-- Create new "Animation" instance



local kickAnimation = Instance.new("Animation")



-- Set its "AnimationId" to the corresponding animation asset ID



kickAnimation.AnimationId = "rbxassetid://2515090838"



-- Load animation onto the humanoid



local kickAnimationTrack = humanoid:LoadAnimation(kickAnimation)



-- Play animation track



kickAnimationTrack:Play()



-- If a named event was defined for the animation, connect it to "GetMarkerReachedSignal()"



kickAnimationTrack:GetMarkerReachedSignal("KickEnd"):Connect(function(paramString)



print(paramString)



end)
```

---

API Reference

Properties

Value

Read Parallel

A value that is specified for a [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker).

KeyframeMarker.Value:[string](/docs/luau/strings)

A value that is specified for a [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker). Whenever the
signal created from [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal) gets
fired, this value will be passed into the connected function.

See also:

* [Keyframe](/docs/reference/engine/classes/Keyframe), holds the [Poses](/docs/reference/engine/classes/Pose) applied to joints in a
  [Model](/docs/reference/engine/classes/Model) at a given point of time in an animation
* [AnimationTrack](/docs/reference/engine/classes/AnimationTrack), controls the playback of an animation on a
  [Humanoid](/docs/reference/engine/classes/Humanoid) or [AnimationController](/docs/reference/engine/classes/AnimationController)

Code Samples

Get Keyframe Markers Attached to a Keyframe

This example demonstrates the [Keyframe:AddMarker()](/docs/reference/engine/classes/Keyframe#AddMarker) and
[Keyframe:GetMarkers()](/docs/reference/engine/classes/Keyframe#GetMarkers) functions. After adding two markers, *marker1*
and *marker2* to the keyframe, this example gets and prints the names of the
added markers.

```
local keyframe = Instance.new("Keyframe")



keyframe.Parent = workspace



local marker1 = Instance.new("KeyframeMarker")



marker1.Name = "FootStep"



marker1.Value = 100



local marker2 = Instance.new("KeyframeMarker")



marker2.Name = "Wave"



marker2.Value = 100



keyframe:AddMarker(marker1) --marker.Parent = keyframe



keyframe:AddMarker(marker2) --marker.Parent = keyframe



local markers = keyframe:GetMarkers()



for _, marker in pairs(markers) do



print(marker.Name)



end
```

Add Marker/Remove Marker

This example demonstrates the [Keyframe:AddMarker()](/docs/reference/engine/classes/Keyframe#AddMarker) and
[Keyframe:RemoveMarker()](/docs/reference/engine/classes/Keyframe#RemoveMarker) functions. Note these are functionally
equivalent to [parenting](/docs/reference/engine/classes/Instance#Parent) and un-parenting the markers.

```
local keyframe = Instance.new("Keyframe")



keyframe.Parent = workspace



local marker = Instance.new("KeyframeMarker")



marker.Name = "FootStep"



marker.Value = 100



keyframe:AddMarker(marker) --marker.Parent = keyframe



task.wait(2)



keyframe:RemoveMarker(marker) --marker.Parent = nil
```

Provide feedback

---