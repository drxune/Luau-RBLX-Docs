# AnimationController | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AnimationController
Scraped: 2026-01-11T02:27:24.847827Z

## Inherits
- Instance
- AnimationController
- Humanoid
- Animation
- AnimationTrack
- Object
- Animator
- Motor6Ds
- LoadAnimation()
- Animator:LoadAnimation()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AnimationController](/docs/reference/engine/classes/AnimationController)

English

Feedback

Engine Class

![AnimationController](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AnimationController-Dark.webp)AnimationController

Allows animations to be loaded and applied to a character or model in place of
a [Humanoid](/docs/reference/engine/classes/Humanoid).

---

Summary

Methods

|  |
| --- |
| [GetPlayingAnimationTracks](#GetPlayingAnimationTracks)():[Array](/docs/luau/tables#arrays)  Deprecated |
| [LoadAnimation](#LoadAnimation)(animation: [Animation](/docs/reference/engine/classes/Animation)):[AnimationTrack](/docs/reference/engine/classes/AnimationTrack)  Deprecated |

Events

|  |
| --- |
| [AnimationPlayed](#AnimationPlayed)(animationTrack: [AnimationTrack](/docs/reference/engine/classes/AnimationTrack)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object which allows animations to be loaded and applied to a character or
model in place of a [Humanoid](/docs/reference/engine/classes/Humanoid). Creates an [Animator](/docs/reference/engine/classes/Animator) and loads
animations to update [Motor6Ds](/docs/reference/engine/classes/Motor6D) of said character to react in
the way that is described within the animation asset referenced by an
[Animation](/docs/reference/engine/classes/Animation) object.

Note that the [LoadAnimation()](/docs/reference/engine/classes/AnimationController#LoadAnimation)
method of this class has been deprecated. Instead, you should call
[Animator:LoadAnimation()](/docs/reference/engine/classes/Animator#LoadAnimation) directly from an [Animator](/docs/reference/engine/classes/Animator) which can
be created manually in Studio and directly referenced in scripts. When the
deprecated method is called from an [AnimationController](/docs/reference/engine/classes/AnimationController), the
controller itself does nothing regarding the animation intended to be loaded,
except to automatically generate an [Animator](/docs/reference/engine/classes/Animator), onto which the loading
call and animation ID are transferred. In this way, the
[AnimationController](/docs/reference/engine/classes/AnimationController) can be thought of as nothing more than an empty
shell for a child [Animator](/docs/reference/engine/classes/Animator) object which handles any actual
functionality regarding animations.

Code Samples

Using an AnimationController to animation non-player objects

This code sample demonstrates how an AnimationController can be used in
place of a Humanoid for non player character objects.

A basic rig is loaded using InsertService and the default Humanoid is
replaced with an AnimationController. An AnimationTrack is then created
and played.

```
local InsertService = game:GetService("InsertService")



-- Load a model for demonstration



local npcModel = InsertService:LoadAsset(516159357):GetChildren()[1]



npcModel.Name = "NPC"



npcModel.PrimaryPart.Anchored = true



npcModel:SetPrimaryPartCFrame(CFrame.new(0, 5, 0))



npcModel.Parent = workspace



-- Replace the humanoid with an animationcontroller



local humanoid = npcModel:FindFirstChildOfClass("Humanoid")



humanoid:Destroy()



local animationController = Instance.new("AnimationController")



animationController.Parent = npcModel



-- Create and load an animation



local animation = Instance.new("Animation")



animation.AnimationId = "http://www.roblox.com/asset/?id=507771019" -- Roblox dance emote



local animationTrack = animationController:LoadAnimation(animation)



-- Play the animation



animationTrack:Play()
```

---

API Reference

Methods

GetPlayingAnimationTracks

Deprecated

Show details

---

LoadAnimation

Deprecated

Show details

---

Events

AnimationPlayed

Deprecated

Show details

---