# TweenBase | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TweenBase
Scraped: 2026-01-11T02:37:01.969513Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- TweenBase
- Tween
- Tween:Play()
- TweenBase:Play()
- TweenBase:Pause()
- TweenBase:Cancel()
- PlaybackState
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TweenBase](/docs/reference/engine/classes/TweenBase)

English

Feedback

Engine Class

TweenBase

Abstract base class for in-between interpolation handlers. [Tween](/docs/reference/engine/classes/Tween)
inherits from [TweenBase](/docs/reference/engine/classes/TweenBase).

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [PlaybackState](#PlaybackState):[Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState) |

Methods

|  |
| --- |
| [Cancel](#Cancel)():() |
| [Pause](#Pause)():() |
| [Play](#Play)():() |

Events

|  |
| --- |
| [Completed](#Completed)(playbackState: [Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Tween](/docs/reference/engine/classes/Tween)

Abstract base class for in-between interpolation handlers; parent class of
[Tween](/docs/reference/engine/classes/Tween).

---

API Reference

Properties

PlaybackState

Read Only

Not Replicated

Read Parallel

Read-only property that shows the current state for the [Tween](/docs/reference/engine/classes/Tween)
animation.

TweenBase.PlaybackState:[Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState)

Read-only property that shows the current stage for the [Tween](/docs/reference/engine/classes/Tween)
animation. See [Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState) for descriptions of each state. Change
using functions like [Tween:Play()](/docs/reference/engine/classes/Tween#Play).

Code Samples

Tween PlaybackState

In this example a part is rotated by a Tween back and forth several times. The
TweenInfo in this case is configured to make the tween repeat twice after the
first playback and pause between each playback. A function is connected to
when the tween's PlaybackState changes. When run, this function will fire
whenever the tween starts, pauses between playback, and ends.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.Parent = workspace



local goal = {}



goal.Orientation = Vector3.new(0, 90, 0)



local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut, 2, true, 0.5)



local tween = TweenService:Create(part, tweenInfo, goal)



local function onPlaybackChanged()



print("Tween status has changed to:", tween.PlaybackState)



end



local playbackChanged = tween:GetPropertyChangedSignal("PlaybackState")



playbackChanged:Connect(onPlaybackChanged)



tween:Play()
```

Provide feedback

---

Methods

Cancel

Halts playback and resets the tween variables. If you then call
[TweenBase:Play()](/docs/reference/engine/classes/TweenBase#Play), the properties of the tween resume interpolating
towards their destination, but take the full length of the animation to do
so.

TweenBase:Cancel():()

Returns

()

Halts playback of a [Tween](/docs/reference/engine/classes/Tween) and resets the tween variables.

Only resets the tween variables, not the properties being changed by the
tween. If you cancel a tween halfway through its animation, the properties
do not reset to their original values. Differs from
[TweenBase:Pause()](/docs/reference/engine/classes/TweenBase#Pause) in that once resumed, it takes the full duration
of the tween to complete the animation.

Code Samples

Tween Cancel

This sample demonstrates the impact of cancelling a tween.

A part is instanced in the Workspace and a tween is set up to move it along
the Y axis. Mid way through the tween, it is cancelled. It can be observed
here that the part does not return to its original position, but when it is
resumed it takes the full length of the tween (5 seconds) to complete.

This is the key difference TweenBase:Pause() and TweenBase:Cancel().

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.Parent = workspace



local goal = {}



goal.Position = Vector3.new(0, 50, 0)



local tweenInfo = TweenInfo.new(5)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()



task.wait(2.5)



tween:Cancel()



local playTick = tick()



tween:Play()



tween.Completed:Wait()



local timeTaken = tick() - playTick



print("Tween took " .. tostring(timeTaken) .. " secs to complete")



-- The tween will take 5 seconds to complete as the tween variables have been reset by tween:Cancel()
```

Provide feedback

---

Pause

Halts playback of the tween. Doesn't reset its progress variables, meaning
that if you call [TweenBase:Play()](/docs/reference/engine/classes/TweenBase#Play), the tween resumes playback from
the moment it was paused.

TweenBase:Pause():()

Returns

()

Halts playback of the tween. Doesn't reset its progress variables, meaning
that if you call [TweenBase:Play()](/docs/reference/engine/classes/TweenBase#Play), the tween resumes playback from
the moment it was paused.

If you want to reset the progress variables of the tween, use
[TweenBase:Cancel()](/docs/reference/engine/classes/TweenBase#Cancel).

You can only pause tweens that are in the
[PlaybackState](/docs/reference/engine/classes/TweenBase#PlaybackState) of
Enum. PlaybackState.Playing; tweens in other states won't pause. If a
tween is in a different [PlaybackState](/docs/reference/engine/classes/TweenBase#PlaybackState) such
as Enum. PlaybackState.Delayed (as a result of its
[TweenInfo.DelayTime](/docs/reference/engine/datatypes/TweenInfo#DelayTime) being greater than 0), attempting to pause
the tween will fail and the tween will play following its specified delay
time.

Code Samples

Pausing a Tween

This sample demonstrates how the playback of a tween can be paused and
resumed.

A part is instanced in the Workspace and a tween is setup that will move it 50
studs along the X axis. However during playback the tween is briefly paused,
then resumed. To further illustrate this the BrickColor of the part changes
from red to green while it is paused.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.BrickColor = BrickColor.new("Bright green")



part.Parent = workspace



local goal = {}



goal.Position = Vector3.new(50, 10, 0)



local tweenInfo = TweenInfo.new(10, Enum.EasingStyle.Linear)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()



task.wait(3)



part.BrickColor = BrickColor.new("Bright red")



tween:Pause()



task.wait(2)



part.BrickColor = BrickColor.new("Bright green")



tween:Play()
```

Provide feedback

---

Play

Starts playback of a tween. Note that if playback has already started,
calling Play() has no effect unless the tween has finished or is stopped
(either by [TweenBase:Cancel()](/docs/reference/engine/classes/TweenBase#Cancel) or [TweenBase:Pause()](/docs/reference/engine/classes/TweenBase#Pause)).

TweenBase:Play():()

Returns

()

Starts playback of a tween. Note that if playback has already started,
calling Play() has no effect unless the tween has finished or is stopped
(either by [TweenBase:Cancel()](/docs/reference/engine/classes/TweenBase#Cancel) or [TweenBase:Pause()](/docs/reference/engine/classes/TweenBase#Pause)).

Multiple tweens can be played on the same object at the same time, but
they must not animate the same property. If two tweens attempt to modify
the same property, the initial tween is cancelled and overwritten by the
most recent tween (see examples).

Code Samples

Tween Creation

In this example a Tween is created to animate the position and color of a
Part. Because the position and color are part of the same tween, they will
change at the exact same rate and will reach their goal at the same time.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Color = Color3.new(1, 0, 0)



part.Anchored = true



part.Parent = game.Workspace



local goal = {}



goal.Position = Vector3.new(10, 10, 0)



goal.Color = Color3.new(0, 1, 0)



local tweenInfo = TweenInfo.new(5)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()
```

Tween Conflict

This code sample includes a demonstration of tween conflict. A part is
instanced in the Workspace, and two tweens are created that attempt to move
the part in conflicting directions.

When both tweens are played, the first tween is cancelled and overwritten by
the second tween. This can be seen as the part moves along the Y axis as
opposed to the Z axis.

To further demonstrate this, connections have been made for both tweens to the
Tween.Completed event. Upon playing the tweens, the following is printed.

tween1: Enum.PlaybackState.Cancelled tween2: Enum.PlaybackState.Completed

These prints show that the first tween was cancelled (firing the Completed
event) immediately upon the second tween being played. The second tween then
went on to play until completion.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.Parent = game.Workspace



local tweenInfo = TweenInfo.new(5)



-- create two conflicting tweens (both trying to animate part.Position)



local tween1 = TweenService:Create(part, tweenInfo, { Position = Vector3.new(0, 10, 20) })



local tween2 = TweenService:Create(part, tweenInfo, { Position = Vector3.new(0, 30, 0) })



-- listen for their completion status



tween1.Completed:Connect(function(playbackState)



print("tween1: " .. tostring(playbackState))



end)



tween2.Completed:Connect(function(playbackState)



print("tween2: " .. tostring(playbackState))



end)



-- try to play them both



tween1:Play()



tween2:Play()
```

Provide feedback

---

Events

Completed

Fires when the tween finishes playing or when stopped with
[TweenBase:Cancel()](/docs/reference/engine/classes/TweenBase#Cancel).

TweenBase.Completed(playbackState:[Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playbackState:[Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState)  The [Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState) of the tween upon completion. |

Fires when the tween finishes playing or when stopped with
[TweenBase:Cancel()](/docs/reference/engine/classes/TweenBase#Cancel).

Passes the [Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState) of the tween to any connected functions to
give an indication of why the tween ended. Note that calling
[TweenBase:Pause()](/docs/reference/engine/classes/TweenBase#Pause) does not fire the Completed event.

Code Samples

Tween Completed

In this example the walkspeed of any player joining the game will be slowed to
0 over 10 seconds using a Tween. The Completed event is used to reset the
walkspeed after the Tween has finished playing.

```
local Players = game:GetService("Players")



local TweenService = game:GetService("TweenService")



local SLOW_DURATION = 10



local function slowCharacter(humanoid)



local goal = {}



goal.WalkSpeed = 0



local tweenInfo = TweenInfo.new(SLOW_DURATION)



local tweenSpeed = TweenService:Create(humanoid, tweenInfo, goal)



tweenSpeed:Play()



return tweenSpeed



end



local function onCharacterAdded(character)



local humanoid = character:WaitForChild("Humanoid")



local initialSpeed = humanoid.WalkSpeed



local tweenSpeed = slowCharacter(humanoid)



tweenSpeed.Completed:Wait()



humanoid.WalkSpeed = initialSpeed



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterAdded)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Tween Conflict

This code sample includes a demonstration of tween conflict. A part is
instanced in the Workspace, and two tweens are created that attempt to move
the part in conflicting directions.

When both tweens are played, the first tween is cancelled and overwritten by
the second tween. This can be seen as the part moves along the Y axis as
opposed to the Z axis.

To further demonstrate this, connections have been made for both tweens to the
Tween.Completed event. Upon playing the tweens, the following is printed.

tween1: Enum.PlaybackState.Cancelled tween2: Enum.PlaybackState.Completed

These prints show that the first tween was cancelled (firing the Completed
event) immediately upon the second tween being played. The second tween then
went on to play until completion.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.Parent = game.Workspace



local tweenInfo = TweenInfo.new(5)



-- create two conflicting tweens (both trying to animate part.Position)



local tween1 = TweenService:Create(part, tweenInfo, { Position = Vector3.new(0, 10, 20) })



local tween2 = TweenService:Create(part, tweenInfo, { Position = Vector3.new(0, 30, 0) })



-- listen for their completion status



tween1.Completed:Connect(function(playbackState)



print("tween1: " .. tostring(playbackState))



end)



tween2.Completed:Connect(function(playbackState)



print("tween2: " .. tostring(playbackState))



end)



-- try to play them both



tween1:Play()



tween2:Play()
```

Verifying a Tween has Completed

This code sample includes an example of how Tween.Completed can be used to
determine if a Tween has been successfully completed, or cancelled.

In this case a part is instanced and tweened towards 0, 0, 0. Once the tween
has completed, if the final PlaybackState is Completed then the part will
explode. Were the tween to be cancelled prior to completion, the explosion
would not be created.

This method can be used to link tweens to other effects, or even chain several
tweens to play after each other.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 50, 0)



part.Anchored = true



part.Parent = workspace



local goal = {}



goal.Position = Vector3.new(0, 0, 0)



local tweenInfo = TweenInfo.new(3)



local tween = TweenService:Create(part, tweenInfo, goal)



local function onTweenCompleted(playbackState)



if playbackState == Enum.PlaybackState.Completed then



local explosion = Instance.new("Explosion")



explosion.Position = part.Position



explosion.Parent = workspace



part:Destroy()



task.delay(2, function()



if explosion then



explosion:Destroy()



end



end)



end



end



tween.Completed:Connect(onTweenCompleted)



tween:Play()
```

Provide feedback

---