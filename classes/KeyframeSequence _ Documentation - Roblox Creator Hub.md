# KeyframeSequence | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/KeyframeSequence
Scraped: 2026-01-11T02:33:01.419576Z

## Inherits
- AnimationClip
- KeyframeSequence
- Keyframes
- Instance
- Object
- Animation
- Loop
- Priority
- Keyframe
- Time
- AnimationTrack
- KeyframeSequenceProvider:RegisterKeyframeSequence()
- AnimationClipProvider:GetAnimationClipAsync()
- Humanoid
- Instance.Parent
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [AnimationClip](/docs/reference/engine/classes/AnimationClip)
6. /
7. [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence)

English

Feedback

Engine Class

KeyframeSequence

This object stores all of the [Keyframes](/docs/reference/engine/classes/Keyframe) and other data for
the animation.

---

Summary

Properties

|  |
| --- |
| [AuthoredHipHeight](#AuthoredHipHeight):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [AddKeyframe](#AddKeyframe)(keyframe: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [GetKeyframes](#GetKeyframes)():Instances |
| [RemoveKeyframe](#RemoveKeyframe)(keyframe: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

2 inherited from [AnimationClip](/docs/reference/engine/classes/AnimationClip)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) stores all the [Keyframes](/docs/reference/engine/classes/Keyframe) for an
[Animation](/docs/reference/engine/classes/Animation), determines if the animation will
[Loop](/docs/reference/engine/classes/KeyframeSequence#Loop), and determines its
[Priority](/docs/reference/engine/classes/KeyframeSequence#Priority) against other animations. The last
[Keyframe](/docs/reference/engine/classes/Keyframe) in the sequence, meaning the [Keyframe](/docs/reference/engine/classes/Keyframe) with the
highest [Time](/docs/reference/engine/classes/Keyframe#Time) property, determines the length of an
animation.

Although [Priority](/docs/reference/engine/classes/KeyframeSequence#Priority) and
[Loop](/docs/reference/engine/classes/KeyframeSequence#Loop) save the priority and looped animation
settings for the sequence, note that [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) properties can
eventually overwrite these properties at playback time.

If you want to preview an [Animation](/docs/reference/engine/classes/Animation) before uploading it to Roblox, you
can generate a temporary hash ID using
[KeyframeSequenceProvider:RegisterKeyframeSequence()](/docs/reference/engine/classes/KeyframeSequenceProvider#RegisterKeyframeSequence) for localized
animation testing.

#### Obtaining Sequences

In some cases you may wish to download the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence)
corresponding to an existing uploaded [Animation](/docs/reference/engine/classes/Animation). You can use
[AnimationClipProvider:GetAnimationClipAsync()](/docs/reference/engine/classes/AnimationClipProvider#GetAnimationClipAsync) to download an
animation.

Code Samples

Get KeyframeSequence Length

This sample contains a simple function that will get the length of a
KeyframeSequence by finding the Keyframe with the highest Keyframe.Time value.

```
local function getSequenceLength(keyframeSequence)



local length = 0



for _, keyframe in pairs(keyframeSequence:GetKeyframes()) do



if keyframe.Time > length then



length = keyframe.Time



end



end



return length



end



local keyframeSequence = Instance.new("KeyframeSequence")



getSequenceLength(keyframeSequence)
```

KeyframeSequence Instantiation

This sample demonstrates how a basic [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) can be created.

```
-- Create the sequence



local keyframeSequence = Instance.new("KeyframeSequence")



keyframeSequence.Loop = false



keyframeSequence.Priority = Enum.AnimationPriority.Action



--  Create a keyframe



local keyframe = Instance.new("Keyframe")



keyframe.Time = 0



-- Create sample poses



local rootPose = Instance.new("Pose")



rootPose.Name = "HumanoidRootPart"



rootPose.Weight = 0



local lowerTorsoPose = Instance.new("Pose")



lowerTorsoPose.Name = "LowerTorso"



lowerTorsoPose.Weight = 1



-- Set the sequence hierarchy



rootPose:AddSubPose(lowerTorsoPose)



keyframe:AddPose(rootPose)



keyframeSequence:AddKeyframe(keyframe)



-- Parent the sequence



keyframeSequence.Parent = workspace
```

---

API Reference

Properties

AuthoredHipHeight

Hidden

Plugin Security

Read Parallel

Contains the hip height of the [Humanoid](/docs/reference/engine/classes/Humanoid) of the model that was used
to author this [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence).

KeyframeSequence.AuthoredHipHeight:[number](/docs/luau/numbers)

Contains the hip height of the [Humanoid](/docs/reference/engine/classes/Humanoid) of the model that was used
to author this [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence). Default value is 1.35 since
that is the hip height set for a standard R15 character.

Provide feedback

---

Methods

AddKeyframe

Adds a [Keyframe](/docs/reference/engine/classes/Keyframe) to the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) by parenting it to
the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence).

KeyframeSequence:AddKeyframe(keyframe:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| keyframe:[Instance](/docs/reference/engine/datatypes/Instance)  The [Keyframe](/docs/reference/engine/classes/Keyframe) to be added. |

Returns

()

This method adds a [Keyframe](/docs/reference/engine/classes/Keyframe) to the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) by
parenting it to the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence). It is functionally identical
to setting the keyframe's [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to the
[KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence).

Note that this method will not error when called with an instance other
than a [Keyframe](/docs/reference/engine/classes/Keyframe) as the keyframe parameter and will parent it
successfully.

Code Samples

KeyframeSequence Instantiation

This sample demonstrates how a basic [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) can be created.

```
-- Create the sequence



local keyframeSequence = Instance.new("KeyframeSequence")



keyframeSequence.Loop = false



keyframeSequence.Priority = Enum.AnimationPriority.Action



--  Create a keyframe



local keyframe = Instance.new("Keyframe")



keyframe.Time = 0



-- Create sample poses



local rootPose = Instance.new("Pose")



rootPose.Name = "HumanoidRootPart"



rootPose.Weight = 0



local lowerTorsoPose = Instance.new("Pose")



lowerTorsoPose.Name = "LowerTorso"



lowerTorsoPose.Weight = 1



-- Set the sequence hierarchy



rootPose:AddSubPose(lowerTorsoPose)



keyframe:AddPose(rootPose)



keyframeSequence:AddKeyframe(keyframe)



-- Parent the sequence



keyframeSequence.Parent = workspace
```

Provide feedback

---

GetKeyframes

Returns an array that contains all [Keyframes](/docs/reference/engine/classes/Keyframe) contained in
a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence).

KeyframeSequence:GetKeyframes():Instances

Returns

Instances

An array of [Keyframes](/docs/reference/engine/classes/Keyframe).

This method returns an array that contains all [Keyframes](/docs/reference/engine/classes/Keyframe)
that have been added to a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence).

Code Samples

Get KeyframeSequence Length

This sample contains a simple function that will get the length of a
KeyframeSequence by finding the Keyframe with the highest Keyframe.Time value.

```
local function getSequenceLength(keyframeSequence)



local length = 0



for _, keyframe in pairs(keyframeSequence:GetKeyframes()) do



if keyframe.Time > length then



length = keyframe.Time



end



end



return length



end



local keyframeSequence = Instance.new("KeyframeSequence")



getSequenceLength(keyframeSequence)
```

Provide feedback

---

RemoveKeyframe

This method removes a [Keyframe](/docs/reference/engine/classes/Keyframe) from the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence)
by setting its parent to nil.

KeyframeSequence:RemoveKeyframe(keyframe:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| keyframe:[Instance](/docs/reference/engine/datatypes/Instance)  The [Keyframe](/docs/reference/engine/classes/Keyframe) to be removed. |

Returns

()

This method removes a [Keyframe](/docs/reference/engine/classes/Keyframe) from the [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence)
by setting its parent to nil. It is functionally identical to setting
the keyframe's parent to nil.

Note that while this sets the keyframe's parent to nil, it does not
destroy it. Provided another reference to the keyframe remains, it can be
re-parented later.

Also note that this method will not error when called with an
[Instance](/docs/reference/engine/classes/Instance) other than a [Keyframe](/docs/reference/engine/classes/Keyframe) as the keyframe parameter.

Code Samples

KeyframeSequence RemoveKeyframe

This sample adds a [Keyframe](/docs/reference/engine/classes/Keyframe) to a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) before removing it and
adding it again. Note that once a [Keyframe](/docs/reference/engine/classes/Keyframe) is removed, it is not destroyed,
meaning it can be re-added later.

```
local keyframeSequence = Instance.new("KeyframeSequence")



keyframeSequence.Parent = workspace



local keyframe = Instance.new("Keyframe")



keyframeSequence:AddKeyframe(keyframe)



task.wait(2)



keyframeSequence:RemoveKeyframe(keyframe)
```

Provide feedback

---