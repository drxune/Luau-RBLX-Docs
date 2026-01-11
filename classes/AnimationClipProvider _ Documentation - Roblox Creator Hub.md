# AnimationClipProvider | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AnimationClipProvider
Scraped: 2026-01-11T02:28:53.466310Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- AnimationClipProvider
- AnimationClips
- AnimationClip
- Object
- Animation
- KeyframeSequenceProvider
- KeyframeSequence
- CurveAnimation
- InventoryPages
- RegisterAnimationClip()
- AnimationId
- RegisterActiveAnimationClip
- Animation.AnimationId
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AnimationClipProvider](/docs/reference/engine/classes/AnimationClipProvider)

English

Feedback

Engine Class

AnimationClipProvider

Provides functions to load and preview [AnimationClips](/docs/reference/engine/classes/AnimationClip).

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetAnimationClip](#GetAnimationClip)(assetId: ContentId):[AnimationClip](/docs/reference/engine/classes/AnimationClip)  Deprecated |
| [GetAnimationClipAsync](#GetAnimationClipAsync)(assetId: ContentId):[AnimationClip](/docs/reference/engine/classes/AnimationClip) |
| [GetAnimationClipById](#GetAnimationClipById)(assetId: [number](/docs/luau/numbers),useCache: [boolean](/docs/luau/booleans)):[AnimationClip](/docs/reference/engine/classes/AnimationClip)  Deprecated |
| [GetAnimationsAsync](#GetAnimationsAsync)(userId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetAnimations](#GetAnimations)(userId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [GetClipEvaluatorAsync](#GetClipEvaluatorAsync)(assetId: ContentId):ClipEvaluator |
| [RegisterActiveAnimationClip](#RegisterActiveAnimationClip)(animationClip: [AnimationClip](/docs/reference/engine/classes/AnimationClip)):ContentId |
| [RegisterAnimationClip](#RegisterAnimationClip)(animationClip: [AnimationClip](/docs/reference/engine/classes/AnimationClip)):ContentId |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Provides functions to load and preview [AnimationClips](/docs/reference/engine/classes/AnimationClip).
It includes a number of functions that are useful when working with an
[Animation](/docs/reference/engine/classes/Animation).

The [AnimationClipProvider](/docs/reference/engine/classes/AnimationClipProvider) replaces the deprecated
[KeyframeSequenceProvider](/docs/reference/engine/classes/KeyframeSequenceProvider) that was used to download KeyframeSequences
by content ID.

The AnimationClipProvider has a number of uses.

* Download the [AnimationClip](/docs/reference/engine/classes/AnimationClip) associated with an animation content ID
  from the Roblox website, regardless of the underlying type of
  [AnimationClip](/docs/reference/engine/classes/AnimationClip) ([KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) or [CurveAnimation](/docs/reference/engine/classes/CurveAnimation)).
* Generate a temporary ID to locally preview an animation.
* Fetch the content IDs of animations owned by a particular user.

---

API Reference

Methods

GetAnimationClip

Deprecated

Show details

---

GetAnimationClipAsync

Yields

Returns a [AnimationClip](/docs/reference/engine/classes/AnimationClip) based on the specified assetId
asynchronously.

AnimationClipProvider:GetAnimationClipAsync(assetId:ContentId):[AnimationClip](/docs/reference/engine/classes/AnimationClip)

Parameters

|  |
| --- |
| assetId:ContentId  The content ID of the animation. |

Returns

[AnimationClip](/docs/reference/engine/classes/AnimationClip)

The [AnimationClip](/docs/reference/engine/classes/AnimationClip) found.

Fetches an [AnimationClip](/docs/reference/engine/classes/AnimationClip) based on the specified assetId. The
assetId must correspond to an animation asset in Roblox. The function will
yield until the [AnimationClip](/docs/reference/engine/classes/AnimationClip) is loaded from the website and
should be wrapped in a pcall.

Provide feedback

---

GetAnimationClipById

Deprecated

Show details

---

GetAnimationsAsync

Yields

This function returns an [InventoryPages](/docs/reference/engine/classes/InventoryPages) object which can be used
to iterate over animations owned by a specific user.

AnimationClipProvider:GetAnimationsAsync(userId:[number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)

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

Provide feedback

---

GetAnimations

Deprecated

Show details

---

GetClipEvaluatorAsync

Yields

AnimationClipProvider:GetClipEvaluatorAsync(assetId:ContentId):ClipEvaluator

Parameters

|  |
| --- |
| assetId:ContentId |

Returns

ClipEvaluator

Provide feedback

---

RegisterActiveAnimationClip

Generates a temporary asset ID from a [AnimationClip](/docs/reference/engine/classes/AnimationClip) that can be
used for localized testing of an animation.

AnimationClipProvider:RegisterActiveAnimationClip(animationClip:[AnimationClip](/docs/reference/engine/classes/AnimationClip)):ContentId

Parameters

|  |
| --- |
| animationClip:[AnimationClip](/docs/reference/engine/classes/AnimationClip)  The [AnimationClip](/docs/reference/engine/classes/AnimationClip) to be used. |

Returns

ContentId

A temporary asset ID generated for localized animation playback.

Generates a temporary asset ID from a [AnimationClip](/docs/reference/engine/classes/AnimationClip) that can be
used for localized testing of an animation. This performs the same
function as
[RegisterAnimationClip()](/docs/reference/engine/classes/AnimationClipProvider#RegisterAnimationClip)
but generates an active:// URL instead of a hash. The generated ID can
be used as an [AnimationId](/docs/reference/engine/classes/Animation#AnimationId) property for
testing.

The asset ID generated by this function is temporary and cannot be used
outside of Studio. Developers wishing to generate an asset ID that can be
used online should upload the [AnimationClip](/docs/reference/engine/classes/AnimationClip) to Roblox.

Provide feedback

---

RegisterAnimationClip

Generates a temporary asset ID from a [AnimationClip](/docs/reference/engine/classes/AnimationClip) that can be
used for localized testing of an animation. Generates a hash.

AnimationClipProvider:RegisterAnimationClip(animationClip:[AnimationClip](/docs/reference/engine/classes/AnimationClip)):ContentId

Parameters

|  |
| --- |
| animationClip:[AnimationClip](/docs/reference/engine/classes/AnimationClip)  The [AnimationClip](/docs/reference/engine/classes/AnimationClip) to be used. |

Returns

ContentId

A temporary asset ID generated for localized animation playback.

Generates a temporary asset ID from a [AnimationClip](/docs/reference/engine/classes/AnimationClip) that can be
used for localized testing of an animation.

This function performs the same function to
[RegisterActiveAnimationClip](/docs/reference/engine/classes/AnimationClipProvider#RegisterActiveAnimationClip)
yet generates a hash instead of an active:// URL.

The ID generated can be used for the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId)
property to test animations.

The asset ID generated by this function is temporary and cannot be used
outside of Studio. Developers wishing to generate an asset ID that can be
used online should upload the [AnimationClip](/docs/reference/engine/classes/AnimationClip) to Roblox.

Provide feedback

---