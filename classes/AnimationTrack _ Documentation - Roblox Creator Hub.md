# AnimationTrack | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AnimationTrack
Scraped: 2026-01-11T02:40:49.201767Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- AnimationTrack
- Animator
- Animation
- Animator:LoadAnimation()
- Humanoid
- AnimationTracks
- Animator:GetPlayingAnimationTracks()
- AnimationTrack.Speed
- AnimationTrack.Length
- Keyframe
- Poses
- AnimationTrack:AdjustSpeed()
- AnimationTrack.WeightCurrent
- AnimationTrack.WeightTarget
- AnimationTrack:Play()
- AnimationTrack:Stop()
- AnimationTrack:AdjustWeight()
- AnimationTrack.Priority
- KeyframeMarker
- animation
- AnimationTrack.KeyframeReached
- AnimationController
- Model
- Keyframe:AddMarker()
- Keyframe:RemoveMarker()
- Keyframe:GetMarkers()
- Animation.AnimationId
- AnimationTrack:GetMarkerReachedSignal()
- Keyframes
- AnimationTrack.TimePosition
- Motor6Ds
- Motor.MaxVelocity
- AnimationTrack.Ended
- Instances
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AnimationTrack](/docs/reference/engine/classes/AnimationTrack)

English

Feedback

Engine Class

AnimationTrack

Controls the playback of an animation on an [Animator](/docs/reference/engine/classes/Animator).

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Animation](#Animation):[Animation](/docs/reference/engine/classes/Animation) |
| [IsPlaying](#IsPlaying):[boolean](/docs/luau/booleans) |
| [Length](#Length):[number](/docs/luau/numbers) |
| [Looped](#Looped):[boolean](/docs/luau/booleans) |
| [Priority](#Priority):[Enum.AnimationPriority](/docs/reference/engine/enums/AnimationPriority) |
| [Speed](#Speed):[number](/docs/luau/numbers) |
| [TimePosition](#TimePosition):[number](/docs/luau/numbers) |
| [WeightCurrent](#WeightCurrent):[number](/docs/luau/numbers) |
| [WeightTarget](#WeightTarget):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [AdjustSpeed](#AdjustSpeed)(speed: [number](/docs/luau/numbers)):() |
| [AdjustWeight](#AdjustWeight)(weight: [number](/docs/luau/numbers),fadeTime: [number](/docs/luau/numbers)):() |
| [GetMarkerReachedSignal](#GetMarkerReachedSignal)(name: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GetParameter](#GetParameter)(key: [string](/docs/luau/strings)):Variant |
| [GetParameterDefaults](#GetParameterDefaults)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetTargetInstance](#GetTargetInstance)(name: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetTargetNames](#GetTargetNames)():[Array](/docs/luau/tables#arrays) |
| [GetTimeOfKeyframe](#GetTimeOfKeyframe)(keyframeName: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [Play](#Play)(fadeTime: [number](/docs/luau/numbers),weight: [number](/docs/luau/numbers),speed: [number](/docs/luau/numbers)):() |
| [SetParameter](#SetParameter)(key: [string](/docs/luau/strings),value: Variant):() |
| [SetTargetInstance](#SetTargetInstance)(name: [string](/docs/luau/strings),target: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [Stop](#Stop)(fadeTime: [number](/docs/luau/numbers)):() |

Events

|  |
| --- |
| [DidLoop](#DidLoop)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Ended](#Ended)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [KeyframeReached](#KeyframeReached)(keyframeName: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [Stopped](#Stopped)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Controls the playback of an animation on an [Animator](/docs/reference/engine/classes/Animator). This object
cannot be created, instead it is returned by the
[Animator:LoadAnimation()](/docs/reference/engine/classes/Animator#LoadAnimation) method.

---

API Reference

Properties

Animation

Read Only

Not Replicated

Read Parallel

The [Animation](/docs/reference/engine/classes/Animation) object that was used to create this
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

AnimationTrack.Animation:[Animation](/docs/reference/engine/classes/Animation)

The [Animation](/docs/reference/engine/classes/Animation) object that was used to create this
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack). To create an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack), you must load
an [Animation](/docs/reference/engine/classes/Animation) object onto an [Animator](/docs/reference/engine/classes/Animator) using the
[Animator:LoadAnimation()](/docs/reference/engine/classes/Animator#LoadAnimation) method.

Code Samples

Listen For New Animations

The following code sample prints the name of an animation whenever an
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack) plays on a [Humanoid](/docs/reference/engine/classes/Humanoid). This script can be placed
in a model with a [Humanoid](/docs/reference/engine/classes/Humanoid) child.

```
local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



animator.AnimationPlayed:Connect(function(animationTrack)



local animationName = animationTrack.Animation.Name



print("Animation playing " .. animationName)



end)
```

Provide feedback

---

IsPlaying

Read Only

Not Replicated

Read Parallel

A read-only property that returns true when the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) is
playing.

AnimationTrack.IsPlaying:[boolean](/docs/luau/booleans)

A read-only property that returns true when the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) is
playing.

This property can be used to check if an animation is already playing
before playing it (as that would cause it to restart). If you want to
obtain all playing [AnimationTracks](/docs/reference/engine/classes/AnimationTrack) on an
[Animator](/docs/reference/engine/classes/Animator) or a [Humanoid](/docs/reference/engine/classes/Humanoid), they should use
[Animator:GetPlayingAnimationTracks()](/docs/reference/engine/classes/Animator#GetPlayingAnimationTracks)

Code Samples

AnimationTrack IsPlaying

This code sample includes a simple function that will play an AnimationTrack
if it is not playing, or otherwise adjust its speed and weight to match the
new parameters given.

```
local function playOrAdjust(animationTrack, fadeTime, weight, speed)



if not animationTrack.IsPlaying then



animationTrack:Play(fadeTime, weight, speed)



else



animationTrack:AdjustSpeed(speed)



animationTrack:AdjustWeight(weight, fadeTime)



end



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



playOrAdjust(animationTrack, 1, 0.6, 1)
```

Provide feedback

---

Length

Read Only

Not Replicated

Read Parallel

A read-only property that returns the length (in seconds) of an
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack). This will return 0 until the animation has fully
loaded and thus may not be immediately available.

AnimationTrack.Length:[number](/docs/luau/numbers)

A read-only property that returns the length (in seconds) of an
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack). This will return 0 until the animation has fully
loaded and thus may not be immediately available.

When the [AnimationTrack.Speed](/docs/reference/engine/classes/AnimationTrack#Speed) of an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) is
equal to 1, the animation will take [AnimationTrack.Length](/docs/reference/engine/classes/AnimationTrack#Length) (in
seconds) to complete.

Code Samples

Playing Animation for a Specific Duration

The following function will play an AnimationTrack for a specific duration.
This is done by changing the speed of the animation to the length of the
animation divided by the desired playback duration. This could be used in
situations where a developer wants to play a standard animation for different
duration (for example, recharging different abilities).

```
local function playAnimationForDuration(animationTrack, duration)



local speed = animationTrack.Length / duration



animationTrack:Play()



animationTrack:AdjustSpeed(speed)



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765000"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



playAnimationForDuration(animationTrack, 3)
```

Provide feedback

---

Looped

Read Parallel

Sets whether the animation will repeat after finishing. If it is changed
while playing the result will take effect after the animation finishes.

AnimationTrack.Looped:[boolean](/docs/luau/booleans)

This property sets whether the animation will repeat after finishing. If
it is changed while playing the result will take effect after the
animation finishes.

This property defaults to how it was set in the
[Animation Editor](/docs/animation/editor). However, this property
can be changed, allowing control over the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) while it
is running. This property also correctly handles animations played in
reverse (negative [AnimationTrack.Speed](/docs/reference/engine/classes/AnimationTrack#Speed)). After the first keyframe
is reached, it will restart at the last keyframe.

Code Samples

Animation Looping

The animation in this example normally loops. After the player and the
animation are loaded the animation is played in a non-looped fashion then in a
looped fashion.

```
local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



while not localPlayer.Character do



task.wait()



end



local character = localPlayer.Character



local humanoid = character:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507770453"



local animationTrack = animator:LoadAnimation(animation)



animationTrack.Looped = false



task.wait(3)



animationTrack:Play()



task.wait(4)



animationTrack.Looped = true



animationTrack:Play()
```

Play AnimationTrack for a Number of Loops

The function in this code sample will play an AnimationTrack on a loop, for a
specific number of loops, before stopping the animation.

In some cases the developer may want to stop a looped animation after a
certain number of loops have completed, rather than after a certain amount of
time. This is where the DidLoop event can be used.

```
local function playForNumberLoops(animationTrack, number)



animationTrack.Looped = true



animationTrack:Play()



local numberOfLoops = 0



local connection = nil



connection = animationTrack.DidLoop:Connect(function()



numberOfLoops = numberOfLoops + 1



print("loop: ", numberOfLoops)



if numberOfLoops >= number then



animationTrack:Stop()



connection:Disconnect() -- it's important to disconnect connections when they are no longer needed



end



end)



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



playForNumberLoops(animationTrack, 5)
```

Provide feedback

---

Priority

Read Parallel

Sets the priority of an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack). Depending on what this is
set to, playing multiple animations at once will look to this property to
figure out which [Keyframe](/docs/reference/engine/classes/Keyframe) [Poses](/docs/reference/engine/classes/Pose) should be played over
one another.

AnimationTrack.Priority:[Enum.AnimationPriority](/docs/reference/engine/enums/AnimationPriority)

This property sets the priority of an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack). Depending on
what this is set to, playing multiple animations at once will look to this
property to figure out which [Keyframe](/docs/reference/engine/classes/Keyframe) poses should be played over
one another. It uses [Enum.AnimationPriority](/docs/reference/engine/enums/AnimationPriority) which has 7 priority levels:

1. [Action4](/docs/reference/engine/enums/AnimationPriority) (highest priority)
2. [Action3](/docs/reference/engine/enums/AnimationPriority)
3. [Action2](/docs/reference/engine/enums/AnimationPriority)
4. [Action](/docs/reference/engine/enums/AnimationPriority)
5. [Movement](/docs/reference/engine/enums/AnimationPriority)
6. [Idle](/docs/reference/engine/enums/AnimationPriority)
7. [Core](/docs/reference/engine/enums/AnimationPriority) (lowest priority)

Properly set animation priorities, either through the
[Animation Editor](/docs/animation/editor) or through this property,
allow multiple animations to be played without them clashing. Where two
playing animations direct the target to move the same limb in different
ways, the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) with the highest priority will show. If
both animations have the same priority, the weights of the tracks will be
used to combine the animations.

Provide feedback

---

Speed

Read Only

Not Replicated

Read Parallel

Read-only property that gives the current playback speed of the
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

AnimationTrack.Speed:[number](/docs/luau/numbers)

This read-only property gives the current playback speed of the
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack). When equal to 1, the amount of time an animation
takes to complete is equal to [AnimationTrack.Length](/docs/reference/engine/classes/AnimationTrack#Length), in seconds.

If the speed is adjusted through [AnimationTrack:AdjustSpeed()](/docs/reference/engine/classes/AnimationTrack#AdjustSpeed), the
actual time it will take a track to play can be computed by dividing the
length by the speed. Speed is a unitless quantity.

Code Samples

Animation Speed

In this example a player and an animation is loaded. The Length of an
AnimationTrack determines how long the track would take to play if the speed
is at 1. If the speed is adjusted, then the actual time it will take a track
to play can be computed by dividing the length by the speed.

```
local ContentProvider = game:GetService("ContentProvider")



local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



while not localPlayer.Character do



task.wait()



end



local character = localPlayer.Character



local humanoid = character:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507770453"



ContentProvider:PreloadAsync({ animation })



local animationTrack = animator:LoadAnimation(animation)



local normalSpeedTime = animationTrack.Length / animationTrack.Speed



animationTrack:AdjustSpeed(3)



local fastSpeedTime = animationTrack.Length / animationTrack.Speed



print("At normal speed the animation will play for", normalSpeedTime, "seconds")



print("At 3x speed the animation will play for", fastSpeedTime, "seconds")
```

Playing Animation for a Specific Duration

The following function will play an AnimationTrack for a specific duration.
This is done by changing the speed of the animation to the length of the
animation divided by the desired playback duration. This could be used in
situations where a developer wants to play a standard animation for different
duration (for example, recharging different abilities).

```
local function playAnimationForDuration(animationTrack, duration)



local speed = animationTrack.Length / duration



animationTrack:Play()



animationTrack:AdjustSpeed(speed)



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765000"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



playAnimationForDuration(animationTrack, 3)
```

Provide feedback

---

TimePosition

Not Replicated

Read Parallel

Returns the position in time in seconds that an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) is
through playing its source animation. Can be set to make the track jump to
a specific moment in the animation.

AnimationTrack.TimePosition:[number](/docs/luau/numbers)

Returns the position in time in seconds that an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) is
through playing its source animation. Can be set to make the track jump to
a specific moment in the animation, but the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) must be
playing to do so. It can also be used in combination with
[AnimationTrack:AdjustSpeed()](/docs/reference/engine/classes/AnimationTrack#AdjustSpeed) to freeze the animation at a desired
point by setting speed to 0.

Code Samples

Freeze Animation at Position

The following code sample includes two functions that demonstrate how
AdjustSpeed and TimePosition can be used to freeze an animation at a
particular point.

The first function freezes an animation at a particular point in time (defined
in seconds). The second freezes at it at a percentage (between 0 or 100) by
multiplying the percentage by the track length.

As TimePosition can not be used when an AnimationTrack is not playing, the
functions check to make sure the animation is playing before proceeding.

```
function freezeAnimationAtTime(animationTrack, timePosition)



if not animationTrack.IsPlaying then



-- Play the animation if it is not playing



animationTrack:Play()



end



-- Set the speed to 0 to freeze the animation



animationTrack:AdjustSpeed(0)



-- Jump to the desired TimePosition



animationTrack.TimePosition = timePosition



end



function freezeAnimationAtPercent(animationTrack, percentagePosition)



if not animationTrack.IsPlaying then



-- Play the animation if it is not playing



animationTrack:Play()



end



-- Set the speed to 0 to freeze the animation



animationTrack:AdjustSpeed(0)



-- Jump to the desired TimePosition



animationTrack.TimePosition = (percentagePosition / 100) * animationTrack.Length



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



freezeAnimationAtTime(animationTrack, 0.5)



freezeAnimationAtPercent(animationTrack, 50)
```

Provide feedback

---

WeightCurrent

Read Only

Not Replicated

Read Parallel

Read-only property that gives the current weight of the
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

AnimationTrack.WeightCurrent:[number](/docs/luau/numbers)

When weight is set in an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) it does not change
instantaneously but moves from [AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) to
[AnimationTrack.WeightTarget](/docs/reference/engine/classes/AnimationTrack#WeightTarget). The time it takes to do this is
determined by the fadeTime parameter given when the animation is played,
or the weight is adjusted.

[AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) can be checked against
[AnimationTrack.WeightTarget](/docs/reference/engine/classes/AnimationTrack#WeightTarget) to see if the desired weight has been
reached. Note that these values should not be checked for equality with
the == operator, as both of these values are floats. To see if
[AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) has reached the target weight, it is
recommended to see if the distance between those values is sufficiently
small.

Code Samples

WeightCurrent and WeightTarget

This code sample loads two animations onto the local player's Humanoid and
demonstrates how the fadeTime paramater in AnimationTrack.Play determines how
long it takes for an AnimationTrack's WeightCurrent to reach it's
WeightTarget.

As WeightCurrent and WeightTarget are floats the == operator cannot be used to
compare, instead it is more appropriate to check that the difference between
them is sufficiently small to assume the weight fade has completed.

```
local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



while not localPlayer.Character do



task.wait()



end



local character = localPlayer.Character



local humanoid = character:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animation1 = Instance.new("Animation")



animation1.AnimationId = "rbxassetid://507770453"



local animation2 = Instance.new("Animation")



animation2.AnimationId = "rbxassetid://507771019"



task.wait(3) -- arbitrary wait time to allow the character to fall into place



local animationTrack1 = animator:LoadAnimation(animation1)



local animationTrack2 = animator:LoadAnimation(animation2)



animationTrack1.Priority = Enum.AnimationPriority.Movement



animationTrack2.Priority = Enum.AnimationPriority.Action



animationTrack1:Play(0.1, 5, 1)



animationTrack2:Play(10, 3, 1)



local done = false



while not done and task.wait(0.1) do



if math.abs(animationTrack2.WeightCurrent - animationTrack2.WeightTarget) < 0.001 then



print("got there")



done = true



end



end
```

Provide feedback

---

WeightTarget

Read Only

Not Replicated

Read Parallel

Read-only property that gives the current weight of the
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

AnimationTrack.WeightTarget:[number](/docs/luau/numbers)

This read-only property gives the current weight of the
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack). It has a default value of 1 and is set when
[AnimationTrack:Play()](/docs/reference/engine/classes/AnimationTrack#Play), [AnimationTrack:Stop()](/docs/reference/engine/classes/AnimationTrack#Stop) or
[AnimationTrack:AdjustWeight()](/docs/reference/engine/classes/AnimationTrack#AdjustWeight) is called. When weight is set in an
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack) it does not change instantaneously but moves from
[AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) to
[AnimationTrack.WeightTarget](/docs/reference/engine/classes/AnimationTrack#WeightTarget). The time it takes to do this is
determined by the fadeTime parameter given when the animation is played,
or the weight is adjusted.

[AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) can be checked against
[AnimationTrack.WeightTarget](/docs/reference/engine/classes/AnimationTrack#WeightTarget) to see if the desired weight has been
reached. Note that these values should not be checked for equality with
the == operator, as both of these values are floats. To see if
[AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) has reached the target weight, it is
recommended to see if the distance between those values is sufficiently
small.

Code Samples

WeightCurrent and WeightTarget

This code sample loads two animations onto the local player's Humanoid and
demonstrates how the fadeTime paramater in AnimationTrack.Play determines how
long it takes for an AnimationTrack's WeightCurrent to reach it's
WeightTarget.

As WeightCurrent and WeightTarget are floats the == operator cannot be used to
compare, instead it is more appropriate to check that the difference between
them is sufficiently small to assume the weight fade has completed.

```
local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



while not localPlayer.Character do



task.wait()



end



local character = localPlayer.Character



local humanoid = character:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animation1 = Instance.new("Animation")



animation1.AnimationId = "rbxassetid://507770453"



local animation2 = Instance.new("Animation")



animation2.AnimationId = "rbxassetid://507771019"



task.wait(3) -- arbitrary wait time to allow the character to fall into place



local animationTrack1 = animator:LoadAnimation(animation1)



local animationTrack2 = animator:LoadAnimation(animation2)



animationTrack1.Priority = Enum.AnimationPriority.Movement



animationTrack2.Priority = Enum.AnimationPriority.Action



animationTrack1:Play(0.1, 5, 1)



animationTrack2:Play(10, 3, 1)



local done = false



while not done and task.wait(0.1) do



if math.abs(animationTrack2.WeightCurrent - animationTrack2.WeightTarget) < 0.001 then



print("got there")



done = true



end



end
```

Provide feedback

---

Methods

AdjustSpeed

Changes the [AnimationTrack.Speed](/docs/reference/engine/classes/AnimationTrack#Speed) of an animation. A positive value
for speed plays the animation forward, a negative one plays it backwards,
and 0 pauses it.

AnimationTrack:AdjustSpeed(speed:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| speed:[number](/docs/luau/numbers) Default Value: 1 The playback speed the animation is to be changed to. |

Returns

()

This method changes the [AnimationTrack.Speed](/docs/reference/engine/classes/AnimationTrack#Speed) of an animation. A
positive value for speed plays the animation forward, a negative one plays
it backwards, and 0 pauses it.

A track's initial speed is set as a parameter in
[AnimationTrack:Play()](/docs/reference/engine/classes/AnimationTrack#Play). However a track's
[AnimationTrack.Speed](/docs/reference/engine/classes/AnimationTrack#Speed) can be changed during playback using this
method. When speed is equal to 1, the amount of time an animation takes
to complete is equal to [AnimationTrack.Length](/docs/reference/engine/classes/AnimationTrack#Length) (in seconds).

When is adjusted, then the actual time it will take a track to play can be
computed by dividing the length by the speed. [AnimationTrack.Speed](/docs/reference/engine/classes/AnimationTrack#Speed)
is a unitless quantity.

Code Samples

Playing Animation for a Specific Duration

The following function will play an AnimationTrack for a specific duration.
This is done by changing the speed of the animation to the length of the
animation divided by the desired playback duration. This could be used in
situations where a developer wants to play a standard animation for different
duration (for example, recharging different abilities).

```
local function playAnimationForDuration(animationTrack, duration)



local speed = animationTrack.Length / duration



animationTrack:Play()



animationTrack:AdjustSpeed(speed)



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765000"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



playAnimationForDuration(animationTrack, 3)
```

Animation Speed

In this example a player and an animation is loaded. The Length of an
AnimationTrack determines how long the track would take to play if the speed
is at 1. If the speed is adjusted, then the actual time it will take a track
to play can be computed by dividing the length by the speed.

```
local ContentProvider = game:GetService("ContentProvider")



local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



while not localPlayer.Character do



task.wait()



end



local character = localPlayer.Character



local humanoid = character:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507770453"



ContentProvider:PreloadAsync({ animation })



local animationTrack = animator:LoadAnimation(animation)



local normalSpeedTime = animationTrack.Length / animationTrack.Speed



animationTrack:AdjustSpeed(3)



local fastSpeedTime = animationTrack.Length / animationTrack.Speed



print("At normal speed the animation will play for", normalSpeedTime, "seconds")



print("At 3x speed the animation will play for", fastSpeedTime, "seconds")
```

Provide feedback

---

AdjustWeight

Changes the weight of an animation, with the optional fadeTime parameter
determining how long it takes for [AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) to
reach [AnimationTrack.WeightTarget](/docs/reference/engine/classes/AnimationTrack#WeightTarget).

AnimationTrack:AdjustWeight(

weight:[number](/docs/luau/numbers), fadeTime:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| weight:[number](/docs/luau/numbers) Default Value: 1 The weight the animation is to be changed to. |
| fadeTime:[number](/docs/luau/numbers) Default Value: 0.100000001 The duration of time that the animation will fade between the old weight and the new weight for. |

Returns

()

Changes the weight of an animation, with the optional fadeTime parameter
determining how long it takes for [AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) to
reach [AnimationTrack.WeightTarget](/docs/reference/engine/classes/AnimationTrack#WeightTarget).

When weight is set in an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) it does not change
instantaneously but moves from [AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) to
[AnimationTrack.WeightTarget](/docs/reference/engine/classes/AnimationTrack#WeightTarget). The time it takes to do this is
determined by the fadeTime parameter given when the animation is played,
or the weight is adjusted.

The animation weighting system is used to determine how
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack) playing at the same priority are
blended together. The default weight is 1, and no movement will be
visible on an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) with a weight of 0. The pose that
is shown at any point in time is determined by the weighted average of all
the [Poses](/docs/reference/engine/classes/Pose) and the [AnimationTrack.WeightCurrent](/docs/reference/engine/classes/AnimationTrack#WeightCurrent) of
each [AnimationTrack](/docs/reference/engine/classes/AnimationTrack). See below for an example of animation
blending in practice. In most cases blending animations is not required
and using [AnimationTrack.Priority](/docs/reference/engine/classes/AnimationTrack#Priority) is more suitable.

Code Samples

AnimationTrack Change Weight

This code sample includes a function that changes the weight of an
AnimationTrack and yields until the weight has changed to the new target
weight.

The purpose of this sample is to demonstrate how the fadeTime parameter of
AnimationTrack.AdjustWeight works. In most cases, if a developer wishes to
yield over the fadeTime it is recommended they use wait(fadeTime).

```
local function changeWeight(animationTrack, weight, fadeTime)



animationTrack:AdjustWeight(weight, fadeTime)



local startTime = tick()



while math.abs(animationTrack.WeightCurrent - weight) > 0.001 do



task.wait()



end



print("Time taken to change weight " .. tostring(tick() - startTime))



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



changeWeight(animationTrack, 0.6, 1)
```

Provide feedback

---

GetMarkerReachedSignal

Returns an [RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) (event) that fires when a specified
[KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) has been hit in an [animation](/docs/reference/engine/classes/Animation).

AnimationTrack:GetMarkerReachedSignal(name:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) the signal is being created for. Not to be confused with the name of the [Keyframe](/docs/reference/engine/classes/Keyframe). |

Returns

[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

The signal created and fired when the animation reaches the created
[KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker).

This method returns an [RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) (event) similar to the
[AnimationTrack.KeyframeReached](/docs/reference/engine/classes/AnimationTrack#KeyframeReached) event, except it only fires when a
specified [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) has been hit in an
[animation](/docs/reference/engine/classes/Animation). The difference allows for greater control of
when the event will fire.

To learn more about using this method, see
[here](/docs/animation/events).

#### See Also

* [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker)
* [AnimationTrack](/docs/reference/engine/classes/AnimationTrack), controls the playback of an animation on a
  [Humanoid](/docs/reference/engine/classes/Humanoid) or [AnimationController](/docs/reference/engine/classes/AnimationController)
* [Keyframe](/docs/reference/engine/classes/Keyframe), holds the [Poses](/docs/reference/engine/classes/Pose) applied to joints in a
  [Model](/docs/reference/engine/classes/Model) at a given point of time in an animation
* [Keyframe:AddMarker()](/docs/reference/engine/classes/Keyframe#AddMarker)
* [Keyframe:RemoveMarker()](/docs/reference/engine/classes/Keyframe#RemoveMarker)
* [Keyframe:GetMarkers()](/docs/reference/engine/classes/Keyframe#GetMarkers)

Code Samples

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

Provide feedback

---

GetParameter

AnimationTrack:GetParameter(key:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |

Returns

Variant

Provide feedback

---

GetParameterDefaults

AnimationTrack:GetParameterDefaults():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Provide feedback

---

GetTargetInstance

AnimationTrack:GetTargetInstance(name:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Provide feedback

---

GetTargetNames

AnimationTrack:GetTargetNames():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetTimeOfKeyframe

Returns the time position of the first [Keyframe](/docs/reference/engine/classes/Keyframe) of the given name
in an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

AnimationTrack:GetTimeOfKeyframe(keyframeName:[string](/docs/luau/strings)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| keyframeName:[string](/docs/luau/strings)  The name associated with the [Keyframe](/docs/reference/engine/classes/Keyframe) to be found. |

Returns

[number](/docs/luau/numbers)

The time, in seconds, the [Keyframe](/docs/reference/engine/classes/Keyframe) occurs at normal playback
speed.

Returns the time position of the first [Keyframe](/docs/reference/engine/classes/Keyframe) of the given name
in an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack). If multiple [Keyframes](/docs/reference/engine/classes/Keyframe) share
the same name, it will return the earliest one in the animation.

This method will return an error if it is uses with an invalid keyframe
name (one that does not exist for example) or if the underlying
[Animation](/docs/reference/engine/classes/Animation) has not yet loaded. To address this make sure only
correct keyframe names are used and the animation has loaded before
calling this method.

To check if the animation has loaded, verify that the
[AnimationTrack.Length](/docs/reference/engine/classes/AnimationTrack#Length) is greater than zero.

Code Samples

Jump To Keyframe

This sample includes a function that will jump to the first keyframe of a
specified name in an AnimationTrack.

As AnimationTrack.TimePosition cannot be set while the animation is not
playing the function first checks to see if the animation is playing.

This sample will only work once an Animation has loaded.

```
local function jumpToKeyframe(animationTrack, keyframeName)



local timePosition = animationTrack:GetTimeOfKeyframe(keyframeName)



if not animationTrack.IsPlaying then



animationTrack:Play()



end



animationTrack.TimePosition = timePosition



end



local ANIMATION_ID = 0



local KEYFRAME_NAME = "Test"



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://" .. ANIMATION_ID



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



jumpToKeyframe(animationTrack, KEYFRAME_NAME)
```

Provide feedback

---

Play

Plays the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack). Once called an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack)
will play with the specified fadeTime, weight and speed.

AnimationTrack:Play(

fadeTime:[number](/docs/luau/numbers), weight:[number](/docs/luau/numbers), speed:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| fadeTime:[number](/docs/luau/numbers) Default Value: 0.100000001 The duration of time that the animation's weight should be faded in for. |
| weight:[number](/docs/luau/numbers) Default Value: 1 The weight the animation is to be played at. |
| speed:[number](/docs/luau/numbers) Default Value: 1 The playback speed of the animation. |

Returns

()

When [AnimationTrack:Play()](/docs/reference/engine/classes/AnimationTrack#Play) is called the track's animation will
begin playing and the weight of the animation will increase from 0 to
the specified weight (defaults to 1) over the specified fadeTime.

The speed the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) will play at is determined by the
speed parameter (defaults to 1). When the speed is equal to 1 the
number of seconds the track will take to complete is equal to the track's
[AnimationTrack.Length](/docs/reference/engine/classes/AnimationTrack#Length) property. For example, a speed of 2 will
cause the track to play twice as fast.

The weight and speed of the animation can also be changed after the
animation has begun playing by using the
[AnimationTrack:AdjustWeight()](/docs/reference/engine/classes/AnimationTrack#AdjustWeight) and
[AnimationTrack:AdjustSpeed()](/docs/reference/engine/classes/AnimationTrack#AdjustSpeed) methods.

If you want to start the animation at a specific point using
[AnimationTrack.TimePosition](/docs/reference/engine/classes/AnimationTrack#TimePosition), it's important the animation is
played before this is done.

Code Samples

Playing Animation for a Specific Duration

The following function will play an AnimationTrack for a specific duration.
This is done by changing the speed of the animation to the length of the
animation divided by the desired playback duration. This could be used in
situations where a developer wants to play a standard animation for different
duration (for example, recharging different abilities).

```
local function playAnimationForDuration(animationTrack, duration)



local speed = animationTrack.Length / duration



animationTrack:Play()



animationTrack:AdjustSpeed(speed)



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765000"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



playAnimationForDuration(animationTrack, 3)
```

Freeze Animation at Position

The following code sample includes two functions that demonstrate how
AdjustSpeed and TimePosition can be used to freeze an animation at a
particular point.

The first function freezes an animation at a particular point in time (defined
in seconds). The second freezes at it at a percentage (between 0 or 100) by
multiplying the percentage by the track length.

As TimePosition can not be used when an AnimationTrack is not playing, the
functions check to make sure the animation is playing before proceeding.

```
function freezeAnimationAtTime(animationTrack, timePosition)



if not animationTrack.IsPlaying then



-- Play the animation if it is not playing



animationTrack:Play()



end



-- Set the speed to 0 to freeze the animation



animationTrack:AdjustSpeed(0)



-- Jump to the desired TimePosition



animationTrack.TimePosition = timePosition



end



function freezeAnimationAtPercent(animationTrack, percentagePosition)



if not animationTrack.IsPlaying then



-- Play the animation if it is not playing



animationTrack:Play()



end



-- Set the speed to 0 to freeze the animation



animationTrack:AdjustSpeed(0)



-- Jump to the desired TimePosition



animationTrack.TimePosition = (percentagePosition / 100) * animationTrack.Length



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



freezeAnimationAtTime(animationTrack, 0.5)



freezeAnimationAtPercent(animationTrack, 50)
```

Provide feedback

---

SetParameter

AnimationTrack:SetParameter(

key:[string](/docs/luau/strings), value:Variant

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| value:Variant |

Returns

()

Provide feedback

---

SetTargetInstance

AnimationTrack:SetTargetInstance(

name:[string](/docs/luau/strings), target:[Instance](/docs/reference/engine/datatypes/Instance)

):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |
| target:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

Provide feedback

---

Stop

Stops the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

AnimationTrack:Stop(fadeTime:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| fadeTime:[number](/docs/luau/numbers) Default Value: 0.100000001 The time, in seconds, for which animation weight is to be faded out over. |

Returns

()

Stops the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack). Once called, the weight of the animation
will move towards zero over a length of time specified by the optional
fadeTime parameter. For example, if Stop() is called with a fadeTime
of 2, it will take two seconds for the weight of the track to reach zero
and its effects completely end. Please note this will be the case
regardless of the initial weight of the animation.

It is not recommended to use a fadeTime of 0 in an attempt to override
this effect and end the animation immediately for [Motor6Ds](/docs/reference/engine/classes/Motor6D)
that have their [Motor.MaxVelocity](/docs/reference/engine/classes/Motor#MaxVelocity) set to zero, as this causes the
joints to freeze in place. If it must end immediately, ensure the
[Motor.MaxVelocity](/docs/reference/engine/classes/Motor#MaxVelocity) of [Motor6Ds](/docs/reference/engine/classes/Motor6D) in your rig are high
enough for them to snap properly.

Code Samples

AnimationTrack Stop

This code sample includes a function that stops an AnimationTrack with a
specific fadeTime, and yields until the fade is completed and the weight of
the AnimationTrack is equal to zero.

The purpose of this sample is to demonstrate how the fadeTime parameter of
AnimationTrack.Stop works. In most cases, if a developer wishes to yield over
the fadeTime it is recommended they use wait(fadeTime).

```
local function fadeOut(animationTrack, fadeTime)



animationTrack:Stop(fadeTime)



local startTime = tick()



while animationTrack.WeightCurrent > 0 do



task.wait()



end



local timeTaken = tick() - startTime



print("Time taken for weight to reset: " .. tostring(timeTaken))



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



animationTrack:Play()



fadeOut(animationTrack, 1)
```

Provide feedback

---

Events

DidLoop

Fires when an [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) loops on the next update following
the end of the previous animation loop.

AnimationTrack.DidLoop():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires whenever a looped [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) completes a
loop, on the next update.

Currently it may also fire at the exact end of a non looped animation
track but this behavior should not be relied upon.

Code Samples

Play AnimationTrack for a Number of Loops

The function in this code sample will play an AnimationTrack on a loop, for a
specific number of loops, before stopping the animation.

In some cases the developer may want to stop a looped animation after a
certain number of loops have completed, rather than after a certain amount of
time. This is where the DidLoop event can be used.

```
local function playForNumberLoops(animationTrack, number)



animationTrack.Looped = true



animationTrack:Play()



local numberOfLoops = 0



local connection = nil



connection = animationTrack.DidLoop:Connect(function()



numberOfLoops = numberOfLoops + 1



print("loop: ", numberOfLoops)



if numberOfLoops >= number then



animationTrack:Stop()



connection:Disconnect() -- it's important to disconnect connections when they are no longer needed



end



end)



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



playForNumberLoops(animationTrack, 5)
```

Provide feedback

---

Ended

Fires when the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) is completely done moving anything
in the world.

AnimationTrack.Ended():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) is completely done moving anything
in the world, meaning the animation has finished playing, the "fade out"
is finished, and the subject is in a neutral pose.

You can use this to take action when the animation track's subject is back
in a neutral pose that's unaffected by the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) or to
clean up the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

Code Samples

AnimationTrack Ended

The function in this code sample plays an animationTrack and yields until
it has stopped and ended, printing at each step along the way.

```
local InsertService = game:GetService("InsertService")



local Players = game:GetService("Players")



-- Create an NPC model to animate.



local npcModel = Players:CreateHumanoidModelFromUserId(129687796)



npcModel.Name = "JoeNPC"



npcModel.Parent = workspace



npcModel:MoveTo(Vector3.new(0, 15, 4))



local humanoid = npcModel:WaitForChild("Humanoid")



-- Load an animation.



local animationModel = InsertService:LoadAsset(2510238627)



local animation = animationModel:FindFirstChildWhichIsA("Animation", true)



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



-- Connect to Stopped event. This fires when animation stops of



-- it's own accord, or we explicitly call Stop.



animationTrack.Stopped:Connect(function()



print("Animation stopped")



end)



-- Connect to Ended event. This fires when when animation is completely



-- finished affecting the world. In this case it will fire 3 seconds



-- after we call animationTrack:Stop because we pass in a 3



-- second fadeOut.



animationTrack.Ended:Connect(function()



print("Animation ended")



animationTrack:Destroy()



end)



-- Run, give it a bit to play, then stop.



print("Calling Play")



animationTrack:Play()



task.wait(10)



print("Calling Stop")



animationTrack:Stop(3)
```

Provide feedback

---

KeyframeReached

Deprecated

Show details

---

Stopped

Fires when the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) finishes playing. The AnimationTrack
might still animate the subject while the animation "fades out". To catch
when the AnimationTrack is completely done moving anything in the world,
use the [AnimationTrack.Ended](/docs/reference/engine/classes/AnimationTrack#Ended) event.

AnimationTrack.Stopped():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires whenever the [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) finishes playing.

This event has a number of uses. It can be used to wait until an
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack) has stopped before continuing (for example, if
chaining a series of animations to play after each other). It can also be
used to clean up any [Instances](/docs/reference/engine/classes/Instance) created during the
animation playback.

Code Samples

AnimationTrack Stopped

The function in this code sample will play an animationTrack and yield until
it has stopped, before printing.

```
local function yieldPlayAnimation(animationTrack, fadeTime, weight, speed)



animationTrack:Play(fadeTime, weight, speed)



animationTrack.Stopped:Wait()



print("Animation has stopped")



end



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



local humanoid = script.Parent:WaitForChild("Humanoid")



local animator = humanoid:WaitForChild("Animator")



local animationTrack = animator:LoadAnimation(animation)



yieldPlayAnimation(animationTrack, 1, 0.6, 1)
```

Provide feedback

---