# Animator | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Animator
Scraped: 2026-01-11T02:35:04.577794Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Animator
- Animations
- Animation
- AnimationTrack
- AnimationTracks
- Motor6D.Part1
- DataModel
- BasePart:SetNetworkOwner()
- Workspace
- AnimationClipProvider
- Humanoid:LoadAnimation()
- AnimationController:LoadAnimation()
- Humanoid
- AnimationController
- Player.Character
- AnimationTrack.TimePosition
- Scripts
- LocalScripts
- AnimationTrack:Play()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Animator](/docs/reference/engine/classes/Animator)

English

Feedback

Engine Class

![Animator](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Animator-Dark.webp)Animator

Responsible for the playback and replication of [Animations](/docs/reference/engine/classes/Animation).

---

Summary

Properties

|  |
| --- |
| [EvaluationThrottled](#EvaluationThrottled):[boolean](/docs/luau/booleans) |
| [PreferLodEnabled](#PreferLodEnabled):[boolean](/docs/luau/booleans) |
| [RootMotion](#RootMotion):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [RootMotionWeight](#RootMotionWeight):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [ApplyJointVelocities](#ApplyJointVelocities)(motors: Variant):() |
| [GetPlayingAnimationTracks](#GetPlayingAnimationTracks)():[Array](/docs/luau/tables#arrays) |
| [LoadAnimation](#LoadAnimation)(animation: [Animation](/docs/reference/engine/classes/Animation)):[AnimationTrack](/docs/reference/engine/classes/AnimationTrack) |
| [RegisterEvaluationParallelCallback](#RegisterEvaluationParallelCallback)(callback: [function](/docs/luau/functions)):() |
| [StepAnimations](#StepAnimations)(deltaTime: [number](/docs/luau/numbers)):() |

Events

|  |
| --- |
| [AnimationPlayed](#AnimationPlayed)(animationTrack: [AnimationTrack](/docs/reference/engine/classes/AnimationTrack)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The main class responsible for the playback and replication of
[Animations](/docs/reference/engine/classes/Animation). All replication of playing
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack) is handled through the [Animator](/docs/reference/engine/classes/Animator)
instance.

See also [Animation Editor](/docs/animation/editor) and
[Using Animations](/docs/animation/using) to learn how to create and add
pre-built or custom animations to your game.

---

API Reference

Properties

EvaluationThrottled

Read Only

Not Replicated

Write Parallel

Animator.EvaluationThrottled:[boolean](/docs/luau/booleans)

Provide feedback

---

PreferLodEnabled

Read Parallel

Animator.PreferLodEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

RootMotion

Read Only

Not Replicated

Not Browsable

Write Parallel

Animator.RootMotion:[CFrame](/docs/reference/engine/datatypes/CFrame)

Provide feedback

---

RootMotionWeight

Read Only

Not Replicated

Not Browsable

Write Parallel

Animator.RootMotionWeight:[number](/docs/luau/numbers)

Provide feedback

---

Methods

ApplyJointVelocities

Computes relative velocities between parts and apply them to
[Motor6D.Part1](/docs/reference/engine/classes/Motor6D#Part1). These relative velocity calculations and
assignments happen in the order provided.

Animator:ApplyJointVelocities(motors:Variant):()

Parameters

|  |
| --- |
| motors:Variant |

Returns

()

Given the current set of [AnimationTracks](/docs/reference/engine/classes/AnimationTrack) playing,
and their current times and play speeds, compute relative velocities
between the parts and apply them to Motor6D.Part1 (the part which
[Animator](/docs/reference/engine/classes/Animator) considers the "child" part). These relative velocity
calculations and assignments happen in the order provided.

This method doesn't apply velocities for a given joint if both of the
joint's parts are currently part of the same assembly, for example, if
they are still connected directly or indirectly by Motors or Welds.

This method doesn't disable or remove the joints for you. You must disable
or otherwise remove the rigid joints from the assembly before calling this
method.

The given Motor6Ds are not required to be descendants of the
[DataModel](/docs/reference/engine/classes/DataModel). Removing the joints from the [DataModel](/docs/reference/engine/classes/DataModel) before
calling this method is supported.

Provide feedback

---

GetPlayingAnimationTracks

Returns the list of currently playing
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack).

Animator:GetPlayingAnimationTracks():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns the list of currently playing
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack).

Provide feedback

---

LoadAnimation

Loads an [Animation](/docs/reference/engine/classes/Animation) onto an [Animator](/docs/reference/engine/classes/Animator), returning an
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack).

Animator:LoadAnimation(animation:[Animation](/docs/reference/engine/classes/Animation)):[AnimationTrack](/docs/reference/engine/classes/AnimationTrack)

Parameters

|  |
| --- |
| animation:[Animation](/docs/reference/engine/classes/Animation)  The [Animation](/docs/reference/engine/classes/Animation) to be used. |

Returns

[AnimationTrack](/docs/reference/engine/classes/AnimationTrack)

This function loads the given [Animation](/docs/reference/engine/classes/Animation) onto this
[Animator](/docs/reference/engine/classes/Animator), returning a playable [AnimationTrack](/docs/reference/engine/classes/AnimationTrack). When called
on an [Animator](/docs/reference/engine/classes/Animator) within models that the client has network ownership
of, for example the local player's character or from
[BasePart:SetNetworkOwner()](/docs/reference/engine/classes/BasePart#SetNetworkOwner), this function also loads the animation
for the server as well.

Note that the [Animator](/docs/reference/engine/classes/Animator) must be in the [Workspace](/docs/reference/engine/classes/Workspace) before
making a call to LoadAnimation() or else it will be unable to retrieve
the [AnimationClipProvider](/docs/reference/engine/classes/AnimationClipProvider) service and throw an error.

You should use this function directly instead of the similarly-named
[Humanoid:LoadAnimation()](/docs/reference/engine/classes/Humanoid#LoadAnimation) and
[AnimationController:LoadAnimation()](/docs/reference/engine/classes/AnimationController#LoadAnimation) functions. These are
deprecated proxies of this function which also create an [Animator](/docs/reference/engine/classes/Animator)
if one does not exist; this can cause replication issues if you are not
careful.

#### Loading an Animation on Client or Server

In order for [AnimationTracks](/docs/reference/engine/classes/AnimationTrack) to replicate
correctly, it's important to know when they should be loaded on the client
or on the server:

* If an [Animator](/docs/reference/engine/classes/Animator) is a descendant of a [Humanoid](/docs/reference/engine/classes/Humanoid) or
  [AnimationController](/docs/reference/engine/classes/AnimationController) in a player's [Player.Character](/docs/reference/engine/classes/Player#Character),
  animations started on that player's client will be replicated to the
  server and other clients.
* If the [Animator](/docs/reference/engine/classes/Animator) is not a descendant of a player character,
  its animations must be loaded and started on the server to replicate.

The [Animator](/docs/reference/engine/classes/Animator) object must be initially created on the server and
replicated to clients for animation replication to work at all. If an
[Animator](/docs/reference/engine/classes/Animator) is created locally, then
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack) loaded with that [Animator](/docs/reference/engine/classes/Animator)
will not replicate.

Provide feedback

---

RegisterEvaluationParallelCallback

Animator:RegisterEvaluationParallelCallback(callback:[function](/docs/luau/functions)):()

Parameters

|  |
| --- |
| callback:[function](/docs/luau/functions) |

Returns

()

Provide feedback

---

StepAnimations

Plugin Security

Increments the [AnimationTrack.TimePosition](/docs/reference/engine/classes/AnimationTrack#TimePosition) of all playing
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack) that are loaded onto the
[Animator](/docs/reference/engine/classes/Animator), applying the offsets to the model associated with the
[Animator](/docs/reference/engine/classes/Animator). For use in the command bar or by plugins only.

Animator:StepAnimations(deltaTime:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| deltaTime:[number](/docs/luau/numbers)  The amount of time in seconds animation playback is to be incremented by. |

Returns

()

Increments the [AnimationTrack.TimePosition](/docs/reference/engine/classes/AnimationTrack#TimePosition) of all playing
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack) that are loaded onto the
[Animator](/docs/reference/engine/classes/Animator), applying the offsets to the model associated with the
[Animator](/docs/reference/engine/classes/Animator). For use in the command bar or by plugins only.

The deltaTime parameter determines the number of seconds to increment on
the animation's progress. Typically this function will be called in a loop
to preview the length of an animation (see example).

Note that once animations have stopped playing, the model's joints will
need to be manually reset to their original positions (see example).

This function is used to simulate playback of [Animations](/docs/reference/engine/classes/Animation)
when the game isn't running. This allows animations to be previewed
without the consequences of running the game, such as scripts executing.
If the function is called while the game is running, or by
[Scripts](/docs/reference/engine/classes/Script) or [LocalScripts](/docs/reference/engine/classes/LocalScript), it will return
an error.

Developers designing their own custom animation editors are advised to use
this function to preview animations, as it is the method the official
Roblox Animation Editor plugin uses.

Code Samples

Preview Animation in Studio

This code sample includes a function that can be used to preview an Animation
on a Model in Roblox Studio, without needing to run the game. It utilizes the
Animator.StepAnimations function, which is the same method the official Roblox
Animation Editor uses.

```
local RunService = game:GetService("RunService")



local function studioPreviewAnimation(model, animation)



-- find the AnimationController and Animator



local animationController = model:FindFirstChildOfClass("Humanoid")



or model:FindFirstChildOfClass("AnimationController")



local animator = animationController and animationController:FindFirstChildOfClass("Animator")



if not animationController or not animator then



return



end



-- load the Animation to create an AnimationTrack



local track = animationController:LoadAnimation(animation)



track:Play()



-- preview the animation



local startTime = tick()



while (tick() - startTime) < track.Length do



local step = RunService.Heartbeat:wait()



animator:StepAnimations(step)



end



-- stop the animation



track:Stop(0)



animator:StepAnimations(0)



-- reset the joints



for _, descendant in pairs(model:GetDescendants()) do



if descendant:IsA("Motor6D") then



local joint = descendant



joint.CurrentAngle = 0



joint.Transform = CFrame.new()



end



end



end



local character = script.Parent



local animation = Instance.new("Animation")



animation.AnimationId = "rbxassetid://507765644"



studioPreviewAnimation(character, animation)
```

Provide feedback

---

Events

AnimationPlayed

Fires when the Animator starts playing an AnimationTrack.

Animator.AnimationPlayed(animationTrack:[AnimationTrack](/docs/reference/engine/classes/AnimationTrack)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| animationTrack:[AnimationTrack](/docs/reference/engine/classes/AnimationTrack) |

Fires for all [AnimationTrack:Play()](/docs/reference/engine/classes/AnimationTrack#Play) calls on AnimationTracks
created and owned by the Animator.

Provide feedback

---