# KeyframeSequenceProvider | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/KeyframeSequenceProvider
Scraped: 2026-01-11T02:35:09.945659Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- KeyframeSequenceProvider
- KeyframeSequence
- AnimationClip
- AnimationClipProvider
- Object
- KeyframeSequences
- Animations
- Poses
- Animation.AnimationId
- Animation
- InventoryPages
- KeyframeSequenceProvider:GetAnimations()
- KeyframeSequenceProvider:GetKeyframeSequenceAsync()
- KeyframeSequenceProvider:RegisterKeyframeSequence()
- KeyframeSequenceProvider:RegisterActiveKeyframeSequence()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [KeyframeSequenceProvider](/docs/reference/engine/classes/KeyframeSequenceProvider)

English

Feedback

Engine Class

KeyframeSequenceProvider

Deprecated

Provides functions to load and preview [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence).

Not Creatable

Service

Not Replicated

This service is deprecated and does not support the newer
[AnimationClip](/docs/reference/engine/classes/AnimationClip). It's recommended to use [AnimationClipProvider](/docs/reference/engine/classes/AnimationClipProvider)
instead.

---

Summary

Methods

|  |
| --- |
| [GetAnimationsAsync](#GetAnimationsAsync)(userId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetAnimations](#GetAnimations)(userId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [GetKeyframeSequence](#GetKeyframeSequence)(assetId: ContentId):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [GetKeyframeSequenceAsync](#GetKeyframeSequenceAsync)(assetId: ContentId):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetKeyframeSequenceById](#GetKeyframeSequenceById)(assetId: [number](/docs/luau/numbers),useCache: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [RegisterActiveKeyframeSequence](#RegisterActiveKeyframeSequence)(keyframeSequence: [Instance](/docs/reference/engine/datatypes/Instance)):ContentId |
| [RegisterKeyframeSequence](#RegisterKeyframeSequence)(keyframeSequence: [Instance](/docs/reference/engine/datatypes/Instance)):ContentId |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The KeyframeSequenceProvider service provides functions to load and
preview [KeyframeSequences](/docs/reference/engine/classes/KeyframeSequence). It includes a number of
functions that are useful when working with [Animations](/docs/reference/engine/classes/Animation).

A [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) stores a series of [Poses](/docs/reference/engine/classes/Pose) that encode
the hierarchy and motion of an animation. The animation data Roblox uses in
the playback of an animation, referenced by the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId)
property, can be constructed from a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence).
[KeyframeSequences](/docs/reference/engine/classes/KeyframeSequence) are usually created by the Roblox
[Animation Editor](/docs/animation/editor) but can be created through
other plugins or even manually.

Code Samples

Create temporary animation

This code sample contains a simple function to generate an [Animation](/docs/reference/engine/classes/Animation) with a
generated hash ID to preview a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) locally.

```
local KeyframeSequenceProvider = game:GetService("KeyframeSequenceProvider")



local function createPreviewAnimation(keyframeSequence)



local hashId = KeyframeSequenceProvider:RegisterKeyframeSequence(keyframeSequence)



local Animation = Instance.new("Animation")



Animation.AnimationId = hashId



return Animation



end



local keyframeSequence = Instance.new("KeyframeSequence")



local animation = createPreviewAnimation(keyframeSequence)



print(animation)
```

---

API Reference

Methods

GetAnimationsAsync

Yields

This function returns an [InventoryPages](/docs/reference/engine/classes/InventoryPages) object which can be used
to iterate over animations owned by a specific user.

KeyframeSequenceProvider:GetAnimationsAsync(userId:[number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The user ID of the user. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

An [InventoryPages](/docs/reference/engine/classes/InventoryPages) of animations.

This function returns an [InventoryPages](/docs/reference/engine/classes/InventoryPages) object which can be used
to iterate over animations owned by a specific user.

This function has a number of potential uses, such as allowing users to
browse and import animations into a custom animation plugin.

Code Samples

KeyframeSequenceProvider GetAnimations

This code sample includes a demonstration of how the content IDs of animations
belonging to a player can be downloaded using
[KeyframeSequenceProvider:GetAnimations()](/docs/reference/engine/classes/KeyframeSequenceProvider#GetAnimations). To run this code be sure to
change the *USER\_ID* variable to the ID of the user whose animations you want
to download.

```
local KeyframeSequenceProvider = game:GetService("KeyframeSequenceProvider")



local USER_ID = 0 -- Insert your UserId here



local function extractPages(pagesObject)



local array = {}



while true do



local thisPage = pagesObject:GetCurrentPage()



for _, v in pairs(thisPage) do



table.insert(array, v)



end



if pagesObject.IsFinished then



break



end



pagesObject:AdvanceToNextPageAsync()



end



return array



end



local inventoryPages = KeyframeSequenceProvider:GetAnimations(USER_ID)



local animationIds = extractPages(inventoryPages)



for _, id in pairs(animationIds) do



print(id)



end



print("total: ", #animationIds)
```

Provide feedback

---

GetAnimations

Deprecated

Show details

---

GetKeyframeSequence

Deprecated

Show details

---

GetKeyframeSequenceAsync

Yields

Returns a KeyframeSequence based on the specified assetId asynchronously.

KeyframeSequenceProvider:GetKeyframeSequenceAsync(assetId:ContentId):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| assetId:ContentId  The content ID of the animation. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) found.

GetKeyframeSequenceAsync returns a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) based on the
specified assetId. The assetId must correspond to an animation. The
function will yield until the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) is loaded from the
website. Because this is a webcall it should wrapped in a pcall.

Code Samples

Getting an animation's KeyframeSequence

Demonstrates getting an animation's KeyframeSequence using [KeyframeSequenceProvider:GetKeyframeSequenceAsync()](/docs/reference/engine/classes/KeyframeSequenceProvider#GetKeyframeSequenceAsync) and printing the time of each keyframe.

```
local KeyframeSequenceProvider = game:GetService("KeyframeSequenceProvider")



local ANIMATION_ID = "rbxassetid://507771019"



-- Get the keyframe sequence for the asset



local keyframeSequence



local success, err = pcall(function()



keyframeSequence = KeyframeSequenceProvider:GetKeyframeSequenceAsync(ANIMATION_ID)



end)



if success then



-- Iterate over each keyframe and print its time value



local keyframeTable = keyframeSequence:GetKeyframes()



for key, value in keyframeTable do



print(`The time of keyframe number {key} is: {value.Time}`)



end



else



print(`Error getting KeyframeSequence: {err}`)



end
```

Provide feedback

---

GetKeyframeSequenceById

Deprecated

Show details

---

RegisterActiveKeyframeSequence

Generates a temporary asset ID from a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) that can be
used for localized testing of an animation. Generates an *active://* URL.

KeyframeSequenceProvider:RegisterActiveKeyframeSequence(keyframeSequence:[Instance](/docs/reference/engine/datatypes/Instance)):ContentId

Parameters

|  |
| --- |
| keyframeSequence:[Instance](/docs/reference/engine/datatypes/Instance)  The [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) to be used. |

Returns

ContentId

A temporary asset ID generated for localized animation playback.

Generates a temporary asset ID from a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) that can be
used for localized testing of an animation.

This function performs the same function to
[KeyframeSequenceProvider:RegisterKeyframeSequence()](/docs/reference/engine/classes/KeyframeSequenceProvider#RegisterKeyframeSequence) however this
function generates an *active://* URL instead of a hash.

The ID generated can be used in an [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) property
for testing.

The asset ID generated by this function is temporary and cannot be used
outside of Studio. Developers wishing to generate an asset ID that can be
used online should upload the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) to Roblox.

Code Samples

Create temporary animation

This code sample contains a simple function to generate an [Animation](/docs/reference/engine/classes/Animation) with a
generated hash ID to preview a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) locally.

```
local KeyframeSequenceProvider = game:GetService("KeyframeSequenceProvider")



local function createPreviewAnimation(keyframeSequence)



local hashId = KeyframeSequenceProvider:RegisterKeyframeSequence(keyframeSequence)



local Animation = Instance.new("Animation")



Animation.AnimationId = hashId



return Animation



end



local keyframeSequence = Instance.new("KeyframeSequence")



local animation = createPreviewAnimation(keyframeSequence)



print(animation)
```

Provide feedback

---

RegisterKeyframeSequence

Generates a temporary asset ID from a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) that can be
used for localized testing of an animation. Generates a hash.

KeyframeSequenceProvider:RegisterKeyframeSequence(keyframeSequence:[Instance](/docs/reference/engine/datatypes/Instance)):ContentId

Parameters

|  |
| --- |
| keyframeSequence:[Instance](/docs/reference/engine/datatypes/Instance)  The [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) to be used. |

Returns

ContentId

A temporary asset ID generated for localized animation playback.

Generates a temporary asset ID from a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) that can be
used for localized testing of an animation.

This function performs the same function to
[KeyframeSequenceProvider:RegisterActiveKeyframeSequence()](/docs/reference/engine/classes/KeyframeSequenceProvider#RegisterActiveKeyframeSequence) however
this function generates a hash instead of an *active://* URL.

The ID generated can be used for the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId)
property to test animations.

The asset ID generated by this function is temporary and cannot be used
outside of Studio. Developers wishing to generate an asset ID that can be
used online should upload the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) to Roblox.

Code Samples

KeyframeSequenceProvider:RegisterKeyframeSequence

```
local KeyframeSequenceProvider = game:GetService("KeyframeSequenceProvider")



local asset = KeyframeSequenceProvider:RegisterKeyframeSequence(workspace.KeyframeSequence)



local animation = Instance.new("Animation")



animation.Name = "TestAnimation"



animation.AnimationId = asset



animation.Parent = workspace
```

Provide feedback

---