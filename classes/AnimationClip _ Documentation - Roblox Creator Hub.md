# AnimationClip | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AnimationClip
Scraped: 2026-01-11T02:38:32.255093Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- AnimationClip
- CurveAnimation
- KeyframeSequence
- Animation
- AnimationTrack
- AnimationId
- AnimationTrack.Looped
- Keyframe
- AnimationTrack.Priority
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AnimationClip](/docs/reference/engine/classes/AnimationClip)

English

Feedback

Engine Class

AnimationClip

Represents all types of animation data that the Roblox animation system can
consume.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Loop](#Loop):[boolean](/docs/luau/booleans) |
| [Priority](#Priority):[Enum.AnimationPriority](/docs/reference/engine/enums/AnimationPriority) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[CurveAnimation](/docs/reference/engine/classes/CurveAnimation), [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence)

The non-creatable [AnimationClip](/docs/reference/engine/classes/AnimationClip) instance type represents abstract
animation data that can be fed to the Roblox animation system.
[KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) and [CurveAnimation](/docs/reference/engine/classes/CurveAnimation) are two current instance
types that inherit from [AnimationClip](/docs/reference/engine/classes/AnimationClip).

There are different ways to represent animation data. To simplify the use of
Roblox's animation system, all such representations are their own instance
types but inherit from the [AnimationClip](/docs/reference/engine/classes/AnimationClip) instance. Animation clips
published to Roblox via the [Animation Editor](/docs/animation/editor)
can be loaded into the Roblox Engine using an [Animation](/docs/reference/engine/classes/Animation) instance.

---

API Reference

Properties

Loop

Read Parallel

Determines whether the animation stored in this [AnimationClip](/docs/reference/engine/classes/AnimationClip) is
intended to loop.

AnimationClip.Loop:[boolean](/docs/luau/booleans)

Determines whether the animation stored in this [AnimationClip](/docs/reference/engine/classes/AnimationClip) is
intended to loop. When set to true, the animation will continuously repeat
each time it finishes.

Note that [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) instances internally load an
[AnimationClip](/docs/reference/engine/classes/AnimationClip) when an [Animation](/docs/reference/engine/classes/Animation) is requested via its
[AnimationId](/docs/reference/engine/classes/Animation#AnimationId), and the
[AnimationTrack.Looped](/docs/reference/engine/classes/AnimationTrack#Looped) property will default to the original
[AnimationClip](/docs/reference/engine/classes/AnimationClip) value. Note also that this value can be overwritten.

Provide feedback

---

Priority

Read Parallel

Determines which clip takes priority when multiple animations are playing
simultaneously.

AnimationClip.Priority:[Enum.AnimationPriority](/docs/reference/engine/enums/AnimationPriority)

Determines which clip takes priority when multiple animations are playing
simultaneously. Multiple playing animations look to this property to
figure out which [Keyframe](/docs/reference/engine/classes/Keyframe) poses should be played over one another.

Note that [AnimationTrack](/docs/reference/engine/classes/AnimationTrack) instances internally load an
[AnimationClip](/docs/reference/engine/classes/AnimationClip) when an [Animation](/docs/reference/engine/classes/Animation) is requested via its
[AnimationId](/docs/reference/engine/classes/Animation#AnimationId), and the
[AnimationTrack.Priority](/docs/reference/engine/classes/AnimationTrack#Priority) property will default to the original
[AnimationClip](/docs/reference/engine/classes/AnimationClip) value. Note also that this value can be overwritten.

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