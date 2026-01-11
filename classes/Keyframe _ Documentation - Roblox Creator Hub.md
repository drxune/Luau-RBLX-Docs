# Keyframe | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Keyframe
Scraped: 2026-01-11T02:29:58.507518Z

## Inherits
- Object
- Instance
- Keyframe
- Poses
- Model
- Keyframes
- KeyframeSequences
- Script
- KeyframeSequence
- Pose
- BaseParts
- Keyframe.Time
- KeyframeMarker
- Instance.Parent
- AnimationTrack:GetMarkerReachedSignal()
- Keyframe:RemoveMarker()
- Keyframe:GetMarkers()
- Keyframe:AddMarker()
- parenting
- KeyframeMarkers
- instances
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Keyframe](/docs/reference/engine/classes/Keyframe)

English

Feedback

Engine Class

Keyframe

A Keyframe holds the [Poses](/docs/reference/engine/classes/Pose) applied to joints in a [Model](/docs/reference/engine/classes/Model)
at a given point of time in an animation. [Keyframes](/docs/reference/engine/classes/Keyframe) are
interpolated between during animation playback.

---

Summary

Properties

|  |
| --- |
| [Time](#Time):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [AddMarker](#AddMarker)(marker: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [AddPose](#AddPose)(pose: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [GetMarkers](#GetMarkers)():Instances |
| [GetPoses](#GetPoses)():Instances |
| [RemoveMarker](#RemoveMarker)(marker: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [RemovePose](#RemovePose)(pose: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A Keyframe holds the [Poses](/docs/reference/engine/classes/Pose) applied to joints in a [Model](/docs/reference/engine/classes/Model)
at a given point of time in an animation. [Keyframes](/docs/reference/engine/classes/Keyframe) are
interpolated between during animation playback.

Note, in most cases developers do not need to manipulate
[KeyframeSequences](/docs/reference/engine/classes/KeyframeSequence) as the animation editor covers most
animation functionality. However, in some cases a developer may wish to
generate an animation from a [Script](/docs/reference/engine/classes/Script) or build their own plugin.

Structure
---------

Keyframes are held within a [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) and contain [Pose](/docs/reference/engine/classes/Pose)
objects. The poses are named in accordance with the [BaseParts](/docs/reference/engine/classes/BasePart)
they correspond to and are structured in terms of joint hierarchy. This means
each [Pose](/docs/reference/engine/classes/Pose) is parented to the [Pose](/docs/reference/engine/classes/Pose) corresponding to the part it
is attached to.

Note, as [Poses](/docs/reference/engine/classes/Pose) are named in accordance with the
[BaseParts](/docs/reference/engine/classes/BasePart) they correspond to, animations require distinct
part names to play correctly.

Interpolation
-------------

During animation playback the poses in different keyframes are interpolated
between. This allows a smooth animation to be created without needing to
define every frame. Note, the style of interpolation is determined in the
[Pose](/docs/reference/engine/classes/Pose) object. The Keyframe object merely holds the [Poses](/docs/reference/engine/classes/Pose)
at a defined point of time in the animation ([Keyframe.Time](/docs/reference/engine/classes/Keyframe#Time)).

Code Samples

Keyframe Generate Poses

This sample includes a function that will generate a 'blank' keyframe
containing blank poses for all of the model's connected parts in the correct
hierarchical order.

```
local function generateKeyframe(model)



if not model.PrimaryPart then



warn("No primary part set")



return



end



local rootPart = model.PrimaryPart:GetRootPart()



if not rootPart then



warn("Root part not found")



return



end



local partsAdded = {}



partsAdded[rootPart] = true



local function addPoses(part, parentPose)



-- get all of the joints attached to the part



for _, joint in pairs(part:GetJoints()) do



-- we're only interested in Motor6Ds



if joint:IsA("Motor6D") then



-- find the connected part



local connectedPart = nil



if joint.Part0 == part then



connectedPart = joint.Part1



elseif joint.Part1 == part then



connectedPart = joint.Part0



end



if connectedPart then



-- make sure we haven't already added this part



if not partsAdded[connectedPart] then



partsAdded[connectedPart] = true



-- create a pose



local pose = Instance.new("Pose")



pose.Name = connectedPart.Name



parentPose:AddSubPose(pose)



-- recurse



addPoses(connectedPart, pose)



end



end



end



end



end



local keyframe = Instance.new("Keyframe")



-- populate the keyframe



local rootPose = Instance.new("Pose")



rootPose.Name = rootPart.Name



addPoses(rootPart, rootPose)



keyframe:AddPose(rootPose)



return keyframe



end



local character = script.Parent



local keyframe = generateKeyframe(character)



print(keyframe)
```

---

API Reference

Properties

Time

Read Parallel

The [Keyframe](/docs/reference/engine/classes/Keyframe) time position (in seconds) in an animation. This
determines the time at which the [Poses](/docs/reference/engine/classes/Pose) inside the keyframe
will be shown.

Keyframe.Time:[number](/docs/luau/numbers)

This property gives the [Keyframe](/docs/reference/engine/classes/Keyframe) time position (in seconds) in an
animation. This determines the time at which the [Poses](/docs/reference/engine/classes/Pose) inside
the keyframe will be shown.

Note the [Keyframe](/docs/reference/engine/classes/Keyframe) with the highest time value in a
[KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) is used to determine the length of the animation.

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

Methods

AddMarker

Adds a [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) to the [Keyframe](/docs/reference/engine/classes/Keyframe) by parenting it to
the keyframe.

Keyframe:AddMarker(marker:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| marker:[Instance](/docs/reference/engine/datatypes/Instance)  The [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) being parented to the [Keyframe](/docs/reference/engine/classes/Keyframe). |

Returns

()

This function adds a [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) to the [Keyframe](/docs/reference/engine/classes/Keyframe) by
parenting it to the keyframe. It is functionally identical to setting the
marker's [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to the Keyframe.

Note, this function will not error when an instance other than a
KeyframeMarker is given as the parameter and will parent it successfully.

#### More about Keyframes

[Keyframe](/docs/reference/engine/classes/Keyframe) names do not need to be unique. For example, if an
Animation has three keyframes named "Particles" the connected event
returned by [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal) will fire each
time one of these keyframes is reached.

[Keyframe](/docs/reference/engine/classes/Keyframe) names can be set in the Roblox Animation Editor when
creating or editing an animation. They cannot however be set by a
[Script](/docs/reference/engine/classes/Script) on an existing animation prior to playing it.

See also:

* [Keyframe:RemoveMarker()](/docs/reference/engine/classes/Keyframe#RemoveMarker)
* [Keyframe:GetMarkers()](/docs/reference/engine/classes/Keyframe#GetMarkers)
* [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal)

Code Samples

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

AddPose

Adds a [Pose](/docs/reference/engine/classes/Pose) to the [Keyframe](/docs/reference/engine/classes/Keyframe) by parenting it to the
keyframe.

Keyframe:AddPose(pose:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| pose:[Instance](/docs/reference/engine/datatypes/Instance)  The [Pose](/docs/reference/engine/classes/Pose) to be added. |

Returns

()

This function adds a [Pose](/docs/reference/engine/classes/Pose) to the [Keyframe](/docs/reference/engine/classes/Keyframe) by parenting it
to the keyframe. It is functionally identical to setting the pose's
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to the keyframe.

Note, this function will not error when an instance other than a
[Pose](/docs/reference/engine/classes/Pose) is given as the pose parameter and will parent it
successfully.

Code Samples

Keyframe Generate Poses

This sample includes a function that will generate a 'blank' keyframe
containing blank poses for all of the model's connected parts in the correct
hierarchical order.

```
local function generateKeyframe(model)



if not model.PrimaryPart then



warn("No primary part set")



return



end



local rootPart = model.PrimaryPart:GetRootPart()



if not rootPart then



warn("Root part not found")



return



end



local partsAdded = {}



partsAdded[rootPart] = true



local function addPoses(part, parentPose)



-- get all of the joints attached to the part



for _, joint in pairs(part:GetJoints()) do



-- we're only interested in Motor6Ds



if joint:IsA("Motor6D") then



-- find the connected part



local connectedPart = nil



if joint.Part0 == part then



connectedPart = joint.Part1



elseif joint.Part1 == part then



connectedPart = joint.Part0



end



if connectedPart then



-- make sure we haven't already added this part



if not partsAdded[connectedPart] then



partsAdded[connectedPart] = true



-- create a pose



local pose = Instance.new("Pose")



pose.Name = connectedPart.Name



parentPose:AddSubPose(pose)



-- recurse



addPoses(connectedPart, pose)



end



end



end



end



end



local keyframe = Instance.new("Keyframe")



-- populate the keyframe



local rootPose = Instance.new("Pose")



rootPose.Name = rootPart.Name



addPoses(rootPart, rootPose)



keyframe:AddPose(rootPose)



return keyframe



end



local character = script.Parent



local keyframe = generateKeyframe(character)



print(keyframe)
```

Keyframe Add/Remove Pose

This sample demonstrates quickly the Keyframe.AddPose, Keyframe.RemovePose and
Pose.AddSubPose and Pose.RemoveSubPose functions. Note these are functionally
equivalent to parenting and un-parenting the poses.

```
local keyframe = Instance.new("Keyframe")



keyframe.Parent = workspace



local pose = Instance.new("Pose")



pose.EasingStyle = Enum.PoseEasingStyle.Cubic



pose.EasingDirection = Enum.PoseEasingDirection.Out



local pose2 = Instance.new("Pose")



pose2.EasingStyle = Enum.PoseEasingStyle.Cubic



pose2.EasingDirection = Enum.PoseEasingDirection.Out



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



keyframe:RemovePose(pose) -- pose.Parent = nil



task.wait(2)



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



pose:AddSubPose(pose2) -- pose2.Parent = pose



task.wait(2)



pose:RemoveSubPose(pose2) -- pose2.Parent = nil
```

Provide feedback

---

GetMarkers

Returns an array containing all KeyframeMarkers that have been added to
the [Keyframe](/docs/reference/engine/classes/Keyframe).

Keyframe:GetMarkers():Instances

Returns

Instances

An array containing all [KeyframeMarkers](/docs/reference/engine/classes/KeyframeMarker) that
have been added to the [Keyframe](/docs/reference/engine/classes/Keyframe).

This function returns an array containing all
[KeyframeMarkers](/docs/reference/engine/classes/KeyframeMarker) that have been added to the
[Keyframe](/docs/reference/engine/classes/Keyframe). Note, this function will only return
[instances](/docs/reference/engine/classes/Instance) of type KeyframeMarker.

#### More about Keyframes

[Keyframe](/docs/reference/engine/classes/Keyframe) names do not need to be unique. For example, if an
Animation has three keyframes named "Particles" the connected event
returned by [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal) will fire each
time one of these keyframes is reached.

[Keyframe](/docs/reference/engine/classes/Keyframe) names can be set in the Roblox Animation Editor when
creating or editing an animation. They cannot however be set by a
[Script](/docs/reference/engine/classes/Script) on an existing animation prior to playing it.

See also:

* [Keyframe:AddMarker()](/docs/reference/engine/classes/Keyframe#AddMarker)
* [Keyframe:RemoveMarker()](/docs/reference/engine/classes/Keyframe#RemoveMarker)
* [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal)

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

Provide feedback

---

GetPoses

Returns an array containing all [Poses](/docs/reference/engine/classes/Pose) that have been added to
a [Keyframe](/docs/reference/engine/classes/Keyframe).

Keyframe:GetPoses():Instances

Returns

Instances

An array of [Poses](/docs/reference/engine/classes/Pose).

This function returns an array containing all [Poses](/docs/reference/engine/classes/Pose) that have
been added to a [Keyframe](/docs/reference/engine/classes/Keyframe).

Code Samples

Keyframe Reset Poses

This code sample includes a function to reset the CFrame of the Poses in a
Keyframe.

```
local function resetPoses(parent)



-- both functions are equivalent to GetChildren



local poses = parent:IsA("Keyframe") and parent:GetPoses() or parent:IsA("Pose") and parent:GetSubPoses()



for _, pose in pairs(poses) do



if pose:IsA("Pose") then



pose.CFrame = CFrame.new()



-- recurse



resetPoses(pose)



end



end



end
```

Provide feedback

---

RemoveMarker

Removes a [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) from the [Keyframe](/docs/reference/engine/classes/Keyframe) by settings its
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to nil.

Keyframe:RemoveMarker(marker:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| marker:[Instance](/docs/reference/engine/datatypes/Instance)  The marker being removed from the [Keyframe](/docs/reference/engine/classes/Keyframe). |

Returns

()

This function removes a [KeyframeMarker](/docs/reference/engine/classes/KeyframeMarker) from the [Keyframe](/docs/reference/engine/classes/Keyframe)
by settings its [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to nil.

The KeyframeMarker's [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) is set to nil but it is not
destroyed. This means, provided the marker is referenced it can be
re-parented later.

Note, this function will not error when an instance other than a
KeyframeMarker is given as the parameter.

#### More about Keyframes

[Keyframe](/docs/reference/engine/classes/Keyframe) names do not need to be unique. For example, if an
Animation has three keyframes named "Particles" the connected event
returned by [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal) will fire each
time one of these keyframes is reached.

[Keyframe](/docs/reference/engine/classes/Keyframe) names can be set in the Roblox Animation Editor when
creating or editing an animation. They cannot however be set by a
[Script](/docs/reference/engine/classes/Script) on an existing animation prior to playing it.

See also:

* [Keyframe:AddMarker()](/docs/reference/engine/classes/Keyframe#AddMarker)
* [Keyframe:GetMarkers()](/docs/reference/engine/classes/Keyframe#GetMarkers)
* [AnimationTrack:GetMarkerReachedSignal()](/docs/reference/engine/classes/AnimationTrack#GetMarkerReachedSignal)

Code Samples

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

RemovePose

Removes a [Pose](/docs/reference/engine/classes/Pose) from the [Keyframe](/docs/reference/engine/classes/Keyframe) by setting its
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to nil.

Keyframe:RemovePose(pose:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| pose:[Instance](/docs/reference/engine/datatypes/Instance)  The [Pose](/docs/reference/engine/classes/Pose) to be removed. |

Returns

()

This function removes a [Pose](/docs/reference/engine/classes/Pose) from the [Keyframe](/docs/reference/engine/classes/Keyframe) by setting
its [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to nil without destroying it. This means the
provided the pose is referenced and it can be re-parented later.

Note, this function will not error when an instance other than a
[Pose](/docs/reference/engine/classes/Pose) is given as the pose parameter.

Code Samples

Keyframe Add/Remove Pose

This sample demonstrates quickly the Keyframe.AddPose, Keyframe.RemovePose and
Pose.AddSubPose and Pose.RemoveSubPose functions. Note these are functionally
equivalent to parenting and un-parenting the poses.

```
local keyframe = Instance.new("Keyframe")



keyframe.Parent = workspace



local pose = Instance.new("Pose")



pose.EasingStyle = Enum.PoseEasingStyle.Cubic



pose.EasingDirection = Enum.PoseEasingDirection.Out



local pose2 = Instance.new("Pose")



pose2.EasingStyle = Enum.PoseEasingStyle.Cubic



pose2.EasingDirection = Enum.PoseEasingDirection.Out



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



keyframe:RemovePose(pose) -- pose.Parent = nil



task.wait(2)



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



pose:AddSubPose(pose2) -- pose2.Parent = pose



task.wait(2)



pose:RemoveSubPose(pose2) -- pose2.Parent = nil
```

Provide feedback

---