# WorldRoot | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WorldRoot
Scraped: 2026-01-11T02:33:37.804986Z

## Tags
- Not Creatable

## Inherits
- Model
- WorldRoot
- BasePart
- PVInstance
- Instance
- Object
- Workspace
- WorldModel
- parts
- WorldRoot:ArePartsTouchingOthers()
- Terrain
- WorldRoot:Raycast()
- WorldRoot:GetPartsInPart()
- BaseParts
- Changed
- Position
- Orientation
- CFrame
- WorldRoot:GetPartBoundsInBox()
- MeshParts
- BasePart.CanCollide
- BasePart.CanQuery
- WorldRoot:GetPartBoundsInRadius()
- BasePart:GetTouchingParts()
- constraints
- plugins
- RunService.RenderStepped
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Model](/docs/reference/engine/classes/Model)
6. /
7. [WorldRoot](/docs/reference/engine/classes/WorldRoot)

English

Feedback

Engine Class

WorldRoot

Base class for handling physics simulation and 3D spatial queries.

Not Creatable

---

Summary

Methods

|  |
| --- |
| [ArePartsTouchingOthers](#ArePartsTouchingOthers)(partList: Instances,overlapIgnored: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [Blockcast](#Blockcast)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),size: [Vector3](/docs/reference/engine/datatypes/Vector3),direction: [Vector3](/docs/reference/engine/datatypes/Vector3),params: [RaycastParams](/docs/reference/engine/datatypes/RaycastParams)):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)? |
| [BulkMoveTo](#BulkMoveTo)(partList: Instances,cframeList: [Array](/docs/luau/tables#arrays),eventMode: [Enum.BulkMoveMode](/docs/reference/engine/enums/BulkMoveMode)):() |
| [FindPartOnRay](#FindPartOnRay)(ray: [Ray](/docs/reference/engine/datatypes/Ray),ignoreDescendantsInstance: [Instance](/docs/reference/engine/datatypes/Instance),terrainCellsAreCubes: [boolean](/docs/luau/booleans),ignoreWater: [boolean](/docs/luau/booleans)):[Tuple](/docs/luau/tuples)  Deprecated |
| [findPartOnRay](#findPartOnRay)(ray: [Ray](/docs/reference/engine/datatypes/Ray),ignoreDescendantsInstance: [Instance](/docs/reference/engine/datatypes/Instance),terrainCellsAreCubes: [boolean](/docs/luau/booleans),ignoreWater: [boolean](/docs/luau/booleans)):[Tuple](/docs/luau/tuples)  Deprecated |
| [FindPartOnRayWithIgnoreList](#FindPartOnRayWithIgnoreList)(ray: [Ray](/docs/reference/engine/datatypes/Ray),ignoreDescendantsTable: Instances,terrainCellsAreCubes: [boolean](/docs/luau/booleans),ignoreWater: [boolean](/docs/luau/booleans)):[Tuple](/docs/luau/tuples)  Deprecated |
| [FindPartOnRayWithWhitelist](#FindPartOnRayWithWhitelist)(ray: [Ray](/docs/reference/engine/datatypes/Ray),whitelistDescendantsTable: Instances,ignoreWater: [boolean](/docs/luau/booleans)):[Tuple](/docs/luau/tuples)  Deprecated |
| [FindPartsInRegion3](#FindPartsInRegion3)(region: [Region3](/docs/reference/engine/datatypes/Region3),ignoreDescendantsInstance: [Instance](/docs/reference/engine/datatypes/Instance),maxParts: [number](/docs/luau/numbers)):Instances  Deprecated |
| [findPartsInRegion3](#findPartsInRegion3)(region: [Region3](/docs/reference/engine/datatypes/Region3),ignoreDescendantsInstance: [Instance](/docs/reference/engine/datatypes/Instance),maxParts: [number](/docs/luau/numbers)):Instances  Deprecated |
| [FindPartsInRegion3WithIgnoreList](#FindPartsInRegion3WithIgnoreList)(region: [Region3](/docs/reference/engine/datatypes/Region3),ignoreDescendantsTable: Instances,maxParts: [number](/docs/luau/numbers)):Instances  Deprecated |
| [FindPartsInRegion3WithWhiteList](#FindPartsInRegion3WithWhiteList)(region: [Region3](/docs/reference/engine/datatypes/Region3),whitelistDescendantsTable: Instances,maxParts: [number](/docs/luau/numbers)):Instances  Deprecated |
| [GetPartBoundsInBox](#GetPartBoundsInBox)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),size: [Vector3](/docs/reference/engine/datatypes/Vector3),overlapParams: [OverlapParams](/docs/reference/engine/datatypes/OverlapParams)):Instances |
| [GetPartBoundsInRadius](#GetPartBoundsInRadius)(position: [Vector3](/docs/reference/engine/datatypes/Vector3),radius: [number](/docs/luau/numbers),overlapParams: [OverlapParams](/docs/reference/engine/datatypes/OverlapParams)):Instances |
| [GetPartsInPart](#GetPartsInPart)(part: [BasePart](/docs/reference/engine/classes/BasePart),overlapParams: [OverlapParams](/docs/reference/engine/datatypes/OverlapParams)):Instances |
| [IKMoveTo](#IKMoveTo)(part: [BasePart](/docs/reference/engine/classes/BasePart),target: [CFrame](/docs/reference/engine/datatypes/CFrame),translateStiffness: [number](/docs/luau/numbers),rotateStiffness: [number](/docs/luau/numbers),collisionsMode: [Enum.IKCollisionsMode](/docs/reference/engine/enums/IKCollisionsMode)):() |
| [IsRegion3Empty](#IsRegion3Empty)(region: [Region3](/docs/reference/engine/datatypes/Region3),ignoreDescendentsInstance: [Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans)  Deprecated |
| [IsRegion3EmptyWithIgnoreList](#IsRegion3EmptyWithIgnoreList)(region: [Region3](/docs/reference/engine/datatypes/Region3),ignoreDescendentsTable: Instances):[boolean](/docs/luau/booleans)  Deprecated |
| [Raycast](#Raycast)(origin: [Vector3](/docs/reference/engine/datatypes/Vector3),direction: [Vector3](/docs/reference/engine/datatypes/Vector3),raycastParams: [RaycastParams](/docs/reference/engine/datatypes/RaycastParams)):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)? |
| [Shapecast](#Shapecast)(part: [BasePart](/docs/reference/engine/classes/BasePart),direction: [Vector3](/docs/reference/engine/datatypes/Vector3),params: [RaycastParams](/docs/reference/engine/datatypes/RaycastParams)):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)? |
| [Spherecast](#Spherecast)(position: [Vector3](/docs/reference/engine/datatypes/Vector3),radius: [number](/docs/luau/numbers),direction: [Vector3](/docs/reference/engine/datatypes/Vector3),params: [RaycastParams](/docs/reference/engine/datatypes/RaycastParams)):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)? |
| [StepPhysics](#StepPhysics)(dt: [number](/docs/luau/numbers),parts: Instances):() |

Inherited Members

26 inherited from [Model](/docs/reference/engine/classes/Model)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Workspace](/docs/reference/engine/classes/Workspace), [WorldModel](/docs/reference/engine/classes/WorldModel)

This base class provides an API for any instance intended for handling 3D
spatial queries and simulation, such as [Workspace](/docs/reference/engine/classes/Workspace) and
[WorldModel](/docs/reference/engine/classes/WorldModel).

---

API Reference

Methods

ArePartsTouchingOthers

Returns true if any of the given [BasePart](/docs/reference/engine/classes/BasePart) are touching any other
parts.

WorldRoot:ArePartsTouchingOthers(

partList:Instances, overlapIgnored:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| partList:Instances  A list of parts checks to see if any parts in the list are touching any parts not in the list. |
| overlapIgnored:[number](/docs/luau/numbers) Default Value: 0.000199999995 The part overlap threshold in studs that is ignored before parts are considered to be touching. |

Returns

[boolean](/docs/luau/booleans)

True if and only if any of the [parts](/docs/reference/engine/classes/Part) in partList are
touching any other parts (parts not in the partList). False if no
parts are passed.

ArePartsTouchingOthers returns true if at least one of the given
[BasePart](/docs/reference/engine/classes/BasePart) are touching any other parts. Two parts are considered
"touching" if they are within the distance threshold, overlapIgnored.

If no parts are provided, false is returned.

Code Samples

Checking for Touching Parts

The code block below demonstrates how to use
[WorldRoot:ArePartsTouchingOthers()](/docs/reference/engine/classes/WorldRoot#ArePartsTouchingOthers) to check if parts in a list are
touching any parts in the workspace not in the list.

First the script creates two square parts that overlap 1 stud, Part1 and
Part2. Then, it prints the value returned by ArePartsTouchingOthers() when
Part1 is passed in partList at three different overlap values: 0, 0.999,
and 1. The first two times ArePartsTouchingOthers() is called return false
because the overlap values are less than the distance that Part1 and Part2
overlap. The third call returns true because the overlap value is equal to
the distance that the parts overlap.

```
local part1 = Instance.new("Part")



part1.Name = "Part1"



part1.Anchored = true



part1.Transparency = 0.5



part1.Color = Color3.fromRGB(185, 100, 38)



part1.Size = Vector3.new(2, 2, 2)



part1.Position = Vector3.new(0, 4, 0)



part1.Parent = workspace



local part2 = Instance.new("Part")



part2.Name = "Part2"



part2.Anchored = true



part2.Transparency = 0.5



part2.Color = Color3.fromRGB(200, 10, 0)



part2.Size = Vector3.new(2, 2, 2)



part2.Position = Vector3.new(0, 5, 0)



part2.Parent = workspace



local partList = { part1 }



print(workspace:ArePartsTouchingOthers(partList, 0)) -- True



print(workspace:ArePartsTouchingOthers(partList, 0.999)) -- True



print(workspace:ArePartsTouchingOthers(partList, 1)) -- False
```

Provide feedback

---

Blockcast

Write Parallel

Casts a block shape in a given direction and returns a
[RaycastResult](/docs/reference/engine/datatypes/RaycastResult) if the shape hits a [BasePart](/docs/reference/engine/classes/BasePart) or
[Terrain](/docs/reference/engine/classes/Terrain) cell.

WorldRoot:Blockcast(

cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), size:[Vector3](/docs/reference/engine/datatypes/Vector3), direction:[Vector3](/docs/reference/engine/datatypes/Vector3), params:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams)

):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Parameters

|  |
| --- |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  The initial position and rotation of the cast block shape. |
| size:[Vector3](/docs/reference/engine/datatypes/Vector3)  The size of the cast block shape in studs. The maximum size is 512 studs. |
| direction:[Vector3](/docs/reference/engine/datatypes/Vector3)  Direction of the shapecast, with the magnitude representing the maximum distance the shape can travel. The maximum distance is 1024 studs. |
| params:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) Default Value: "RaycastParams{IgnoreWater=false, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" |

Returns

[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Contains the result of the shapecast operation, or nil if no
eligible [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell was hit.

Casts a block shape in a given direction and returns the first collision
with a [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell. This is analogous to how
[WorldRoot:Raycast()](/docs/reference/engine/classes/WorldRoot#Raycast) casts a linear ray in a direction to find a
collision, but it uses a 3D shape instead of a ray.

Unlike [WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart), this method does not detect
[BaseParts](/docs/reference/engine/classes/BasePart) that initially intersect the shape.

If a hit is detected, a [RaycastResult](/docs/reference/engine/datatypes/RaycastResult) is returned containing
the hit information. The [Distance](/docs/reference/engine/datatypes/RaycastResult#Distance)
property represents the distance the shape has to travel to find a hit,
and the [Position](/docs/reference/engine/datatypes/RaycastResult#Position) property represents the
intersection point that causes the hit.

This method throws an error if it is passed invalid [CFrame](/docs/reference/engine/datatypes/CFrame),
size, or direction inputs.

Code Samples

Blockcasting

Casts a block and returns the first collision with a [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain). Prints the properties of the RaycastResult if a result was hit.

```
local Workspace = game:GetService("Workspace")



local function castBlock()



-- The initial position and rotation of the cast block shape



local originCFrame = CFrame.new(Vector3.new(0, 50, 0))



-- The size of the cast block shape



local size = Vector3.new(6, 3, 9)



-- The direction the block is cast in



local direction = -Vector3.yAxis



-- The maximum distance of the cast



local distance = 50



-- Cast the block and create a visualization of it



local raycastResult = Workspace:Blockcast(originCFrame, size, direction * distance)



if raycastResult then



-- Print all properties of the RaycastResult if it exists



print(`Block intersected with: {raycastResult.Instance:GetFullName()}`)



print(`Intersection position: {raycastResult.Position}`)



print(`Distance between block's initial position and result: {raycastResult.Distance}`)



print(`The normal vector of the intersected face: {raycastResult.Normal}`)



print(`Material hit: {raycastResult.Material.Name}`)



else



print("Nothing was hit")



end



end



-- Continually cast a block every 2 seconds



while true do



castBlock()



task.wait(2)



end
```

Provide feedback

---

BulkMoveTo

Moves a table of [BaseParts](/docs/reference/engine/classes/BasePart) to a table of
[CFrames](/docs/reference/engine/datatypes/CFrame).

WorldRoot:BulkMoveTo(

partList:Instances, cframeList:[Array](/docs/luau/tables#arrays), eventMode:[Enum.BulkMoveMode](/docs/reference/engine/enums/BulkMoveMode)

):()

Parameters

|  |
| --- |
| partList:Instances |
| cframeList:[Array](/docs/luau/tables#arrays) |
| eventMode:[Enum.BulkMoveMode](/docs/reference/engine/enums/BulkMoveMode) Default Value: "FireAllEvents" |

Returns

()

This function moves a table of [BaseParts](/docs/reference/engine/classes/BasePart) to a table of
[CFrames](/docs/reference/engine/datatypes/CFrame) without necessarily firing the default property
[Changed](/docs/reference/engine/classes/Object#Changed) events. This provides a very fast way to
move large numbers of parts, as you don't have to pay the cost of separate
property sets for each individual part.

The third argument allows you to further optimize the movement operation.
By default, the [Changed](/docs/reference/engine/classes/Object#Changed) event of each part fires
for [Position](/docs/reference/engine/classes/BasePart#Position),
[Orientation](/docs/reference/engine/classes/BasePart#Orientation), and
[CFrame](/docs/reference/engine/classes/BasePart#CFrame). However, if you specify
[FireCFrameChanged](/docs/reference/engine/enums/BulkMoveMode) as the third argument, only the
[Changed](/docs/reference/engine/classes/Object#Changed) event for the
[CFrame](/docs/reference/engine/classes/BasePart#CFrame) property will fire.

Note that you should only use this function if you're sure that part
movement is a bottleneck in your code. Simply setting the
[CFrame](/docs/reference/engine/classes/BasePart#CFrame) property of individual parts and welded
models is fast enough in the majority of cases.

Provide feedback

---

FindPartOnRay

Deprecated

Show details

---

findPartOnRay

Deprecated

Show details

---

FindPartOnRayWithIgnoreList

Deprecated

Show details

---

FindPartOnRayWithWhitelist

Deprecated

Show details

---

FindPartsInRegion3

Deprecated

Show details

---

findPartsInRegion3

Deprecated

Show details

---

FindPartsInRegion3WithIgnoreList

Deprecated

Show details

---

FindPartsInRegion3WithWhiteList

Deprecated

Show details

---

GetPartBoundsInBox

Write Parallel

Returns an array of parts whose bounding boxes overlap a given box.

WorldRoot:GetPartBoundsInBox(

cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), size:[Vector3](/docs/reference/engine/datatypes/Vector3), overlapParams:[OverlapParams](/docs/reference/engine/datatypes/OverlapParams)

):Instances

Parameters

|  |
| --- |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  The location of the center of the given box volume to be queried. |
| size:[Vector3](/docs/reference/engine/datatypes/Vector3)  The size of the given box volume to be queried. |
| overlapParams:[OverlapParams](/docs/reference/engine/datatypes/OverlapParams) Default Value: "OverlapParams{MaxParts=0, Tolerance=0, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" Contains reusable portions of the spatial query parameters. |

Returns

Instances

An array of [BaseParts](/docs/reference/engine/classes/BasePart) which matched the spatial
query.

[WorldRoot:GetPartBoundsInBox()](/docs/reference/engine/classes/WorldRoot#GetPartBoundsInBox) returns an array of parts whose
bounding boxes overlap a box whose volume is described using the given
center ([CFrame](/docs/reference/engine/datatypes/CFrame)) and size ([Vector3](/docs/reference/engine/datatypes/Vector3)).

As emphasized, this spatial query method efficiently considers the volume
of parts' bounding boxes rather than their actual occupied volume. This
may be important when considering cylinders, spheres, unions, and
[MeshParts](/docs/reference/engine/classes/MeshPart) which have non-block shapes. For cases where
accuracy especially matters, use [WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart)
instead, or further filter the results of this method yourself.

This method uses a [OverlapParams](/docs/reference/engine/datatypes/OverlapParams) object to describe reusable
portions of the spatial query, such as an inclusion or exclusion list, the
maximum number of parts to query, what
[collision group](/docs/workspace/collisions#collision-filtering) to
use, and whether the query favors an intersected part's
[BasePart.CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) value over its [BasePart.CanQuery](/docs/reference/engine/classes/BasePart#CanQuery)
value.

Provide feedback

---

GetPartBoundsInRadius

Write Parallel

Returns an array of parts whose bounding boxes overlap a given sphere.

WorldRoot:GetPartBoundsInRadius(

position:[Vector3](/docs/reference/engine/datatypes/Vector3), radius:[number](/docs/luau/numbers), overlapParams:[OverlapParams](/docs/reference/engine/datatypes/OverlapParams)

):Instances

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3)  The location of the center of the given sphere volume to be queried. |
| radius:[number](/docs/luau/numbers)  The radius of the given sphere volume to be queried. |
| overlapParams:[OverlapParams](/docs/reference/engine/datatypes/OverlapParams) Default Value: "OverlapParams{MaxParts=0, Tolerance=0, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" Contains reusable portions of the spatial query parameters. |

Returns

Instances

An array of [BaseParts](/docs/reference/engine/classes/BasePart) which matched the spatial
query.

[WorldRoot:GetPartBoundsInRadius()](/docs/reference/engine/classes/WorldRoot#GetPartBoundsInRadius) returns an array of parts whose
bounding boxes overlap a sphere whose volume is described using the
given center ([Vector3](/docs/reference/engine/datatypes/Vector3)) and radius (number).

As emphasized, this spatial query method efficiently considers the volume
of parts' bounding boxes rather than their actual occupied volume. This
may be important when considering cylinders, spheres, unions, and
[MeshParts](/docs/reference/engine/classes/MeshPart) which have non-block shapes. For cases where
accuracy especially matters, use [WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart)
instead, or further filter the results of this method yourself.

This method uses a [OverlapParams](/docs/reference/engine/datatypes/OverlapParams) object to describe reusable
portions of the spatial query, such as an inclusion or exclusion list, the
maximum number of parts to query, what
[collision group](/docs/workspace/collisions#collision-filtering) to
use, and whether the query favors an intersected part's
[BasePart.CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) value over its [BasePart.CanQuery](/docs/reference/engine/classes/BasePart#CanQuery)
value.

Provide feedback

---

GetPartsInPart

Write Parallel

Returns an array of parts whose occupied space is shared with the given
part.

WorldRoot:GetPartsInPart(

part:[BasePart](/docs/reference/engine/classes/BasePart), overlapParams:[OverlapParams](/docs/reference/engine/datatypes/OverlapParams)

):Instances

Parameters

|  |
| --- |
| part:[BasePart](/docs/reference/engine/classes/BasePart)  The part whose volume is to be checked against other parts. |
| overlapParams:[OverlapParams](/docs/reference/engine/datatypes/OverlapParams) Default Value: "OverlapParams{MaxParts=0, Tolerance=0, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" Contains reusable portions of the spatial query parameters. |

Returns

Instances

An array of [BaseParts](/docs/reference/engine/classes/BasePart) which matched the spatial
query.

[WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart) returns an array of parts whose
occupied space is shared with the given part (which must exist in the same
[WorldRoot](/docs/reference/engine/classes/WorldRoot) as the parts to be queried). This method can be used in
place of [BasePart:GetTouchingParts()](/docs/reference/engine/classes/BasePart#GetTouchingParts) and is generally a better
choice.

As noted, this spatial query method considers the exact volume
occupied by the given part using a full geometric collision check. As an
example, a concave/hollow part won't match queried parts within it unless
they actually overlap/touch such a part. For simpler volumes, consider
using [WorldRoot:GetPartBoundsInBox()](/docs/reference/engine/classes/WorldRoot#GetPartBoundsInBox) or
[WorldRoot:GetPartBoundsInRadius()](/docs/reference/engine/classes/WorldRoot#GetPartBoundsInRadius), as they are less accurate but
perform more efficiently.

This method uses a [OverlapParams](/docs/reference/engine/datatypes/OverlapParams) object to describe reusable
portions of the spatial query, such as an inclusion or exclusion list, the
maximum number of parts to query, what
[collision group](/docs/workspace/collisions#collision-filtering) to
use, and whether the query favors an intersected part's
[BasePart.CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) value over its [BasePart.CanQuery](/docs/reference/engine/classes/BasePart#CanQuery)
value.

Provide feedback

---

IKMoveTo

Plugin Security

Moves the specified part to the specified location via inverse kinematics
rather than moving it there directly, to ensure any joints, constraints,
or collisions that part is participating in remain physically satisfied.

WorldRoot:IKMoveTo(

part:[BasePart](/docs/reference/engine/classes/BasePart), target:[CFrame](/docs/reference/engine/datatypes/CFrame), translateStiffness:[number](/docs/luau/numbers), rotateStiffness:[number](/docs/luau/numbers), collisionsMode:[Enum.IKCollisionsMode](/docs/reference/engine/enums/IKCollisionsMode)

):()

Parameters

|  |
| --- |
| part:[BasePart](/docs/reference/engine/classes/BasePart)  The part being moved. |
| target:[CFrame](/docs/reference/engine/datatypes/CFrame)  The location to move the specified part. |
| translateStiffness:[number](/docs/luau/numbers) Default Value: 0.5 A number between 0 and 1 specifying how aggressively to match the part's position to the position part of the target [CFrame](/docs/reference/engine/datatypes/CFrame). |
| rotateStiffness:[number](/docs/luau/numbers) Default Value: 0.5 A number between 0 and 1 specifying how aggressively to match the part's rotation to the rotation part of the target [CFrame](/docs/reference/engine/datatypes/CFrame). |
| collisionsMode:[Enum.IKCollisionsMode](/docs/reference/engine/enums/IKCollisionsMode) Default Value: "OtherMechanismsAnchored" Allows you to specify what objects should be effected by the physical resolution. |

Returns

()

This function moves the specified part to the specified location via
[inverse kinematics](https://en.wikipedia.org/wiki/Inverse_kinematics)
rather than moving it there directly, to ensure any joints,
[constraints](/docs/reference/engine/classes/Constraint), or collisions that part is participating
in remain physically satisfied. Currently this function is only available
in Studio to [plugins](/docs/reference/engine/classes/Plugin), as it currently conflicts with the
physics of a running game.

Translate stiffness is a number between 0 and 1 specifying how
aggressively to match the part's position to the position part of the
target CFrame. Rotate stiffness is a number between 0 and 1 specifying
how aggressively to match the part's rotation to the rotation part of the
target CFrame.

For example:

* If translate stiffness and rotate stiffness are both equal to 1, then
  the part will be moved exactly to the target CFrame regardless of what
  physical constraints there are on it.
* If translate stiffness and rotate stiffness are both equal to 0.5, then
  the part will try to move to exactly the target CFrame, but may be
  pushed out of the way by physical constraints on it.
* If translate stiffness and rotate stiffness are both equal to 0, then
  the target CFrame will be ignored and physical constraints will be
  solved for the object at the position where it was.

Provide feedback

---

IsRegion3Empty

Deprecated

Show details

---

IsRegion3EmptyWithIgnoreList

Deprecated

Show details

---

Raycast

Write Parallel

Casts a ray using an origin, direction, and optional
[RaycastParams](/docs/reference/engine/datatypes/RaycastParams), then returns a [RaycastResult](/docs/reference/engine/datatypes/RaycastResult) if an
eligible object or terrain intersects the ray.

WorldRoot:Raycast(

origin:[Vector3](/docs/reference/engine/datatypes/Vector3), direction:[Vector3](/docs/reference/engine/datatypes/Vector3), raycastParams:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams)

):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Parameters

|  |
| --- |
| origin:[Vector3](/docs/reference/engine/datatypes/Vector3)  The origin point of the ray. |
| direction:[Vector3](/docs/reference/engine/datatypes/Vector3)  The directional vector of the ray. Note that the length of this vector matters, as parts/terrain further away than its length will not be tested. |
| raycastParams:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) Default Value: "RaycastParams{IgnoreWater=false, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" An object used to specify hit eligibility in the raycast operation. If not provided, default values are used where all parts are considered and [Terrain](/docs/reference/engine/classes/Terrain) water is not ignored. |

Returns

[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Contains the results of a raycast operation, or nil if no eligible
[BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell was hit.

Casts a ray using an origin, direction, and optional
[RaycastParams](/docs/reference/engine/datatypes/RaycastParams). If it finds an eligible [BasePart](/docs/reference/engine/classes/BasePart) or
[Terrain](/docs/reference/engine/classes/Terrain) cell, a [RaycastResult](/docs/reference/engine/datatypes/RaycastResult) is returned containing
the results of the operation. If no [RaycastParams](/docs/reference/engine/datatypes/RaycastParams) object is
provided, the defaults are used (all parts are considered and
[Terrain](/docs/reference/engine/classes/Terrain) water is not ignored).

Note that the length (magnitude) of the directional vector is important,
as objects/terrain further away than its length will not be tested. If
you're using a [CFrame](/docs/reference/engine/datatypes/CFrame) to help create the ray components,
consider using [CFrame.LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) as the directional vector and
multiply it by the desired length as shown in the example below. The
maximum length of the direction vector is 15,000 studs.

This method does not use a [Ray](/docs/reference/engine/datatypes/Ray) object, but its origin and
direction components can be borrowed from [Ray.Origin](/docs/reference/engine/datatypes/Ray#Origin) and
[Ray.Direction](/docs/reference/engine/datatypes/Ray#Direction).

Code Samples

Raycasting

Casts a ray and returns the first collision with a [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain). Prints the properties of the RaycastResult if a result was hit.

```
local Workspace = game:GetService("Workspace")



local function castRay()



-- The origin point of the ray



local originPosition = Vector3.new(0, 50, 0)



-- The direction the ray is cast in



local direction = -Vector3.yAxis



-- The maximum distance of the ray



local distance = 50



-- Cast the ray and create a visualization of it



local raycastResult = Workspace:Raycast(originPosition, direction * distance)



if raycastResult then



-- Print all properties of the RaycastResult if it exists



print(`Ray intersected with: {raycastResult.Instance:GetFullName()}`)



print(`Intersection position: {raycastResult.Position}`)



print(`Distance between ray origin and result: {raycastResult.Distance}`)



print(`The normal vector of the intersected face: {raycastResult.Normal}`)



print(`Material hit: {raycastResult.Material.Name}`)



else



print("Nothing was hit")



end



end



-- Continually cast a ray every 2 seconds



while true do



castRay()



task.wait(2)



end
```

Provide feedback

---

Shapecast

WorldRoot:Shapecast(

part:[BasePart](/docs/reference/engine/classes/BasePart), direction:[Vector3](/docs/reference/engine/datatypes/Vector3), params:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams)

):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Parameters

|  |
| --- |
| part:[BasePart](/docs/reference/engine/classes/BasePart) |
| direction:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| params:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) Default Value: "RaycastParams{IgnoreWater=false, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" |

Returns

[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Provide feedback

---

Spherecast

Write Parallel

Casts a spherical shape in a given direction and returns a
[RaycastResult](/docs/reference/engine/datatypes/RaycastResult) if the shape hits a [BasePart](/docs/reference/engine/classes/BasePart) or
[Terrain](/docs/reference/engine/classes/Terrain) cell.

WorldRoot:Spherecast(

position:[Vector3](/docs/reference/engine/datatypes/Vector3), radius:[number](/docs/luau/numbers), direction:[Vector3](/docs/reference/engine/datatypes/Vector3), params:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams)

):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3)  The initial position of the cast spherical shape. |
| radius:[number](/docs/luau/numbers)  The radius of the cast spherical shape in studs. The maximum radius is 256 studs. |
| direction:[Vector3](/docs/reference/engine/datatypes/Vector3)  Direction of the shapecast, with the magnitude representing the maximum distance the shape can travel. The maximum distance is 1024 studs. |
| params:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) Default Value: "RaycastParams{IgnoreWater=false, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" |

Returns

[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Contains the result of the shapecast operation, or nil if no
eligible [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell was hit.

Casts a spherical shape in a given direction and returns the first
collision with a [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain) cell. This is
analogous to how [WorldRoot:Raycast()](/docs/reference/engine/classes/WorldRoot#Raycast) casts a linear ray in a
direction to find a collision, but it uses a 3D shape instead of a ray.

Unlike [WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart), this method does not detect
[BaseParts](/docs/reference/engine/classes/BasePart) that initially intersect the shape.

If a hit is detected, a [RaycastResult](/docs/reference/engine/datatypes/RaycastResult) is returned containing
the hit information. The [Distance](/docs/reference/engine/datatypes/RaycastResult#Distance)
property represents the distance the shape has to travel to find a hit,
and the [Position](/docs/reference/engine/datatypes/RaycastResult#Position) property represents the
intersection point that causes the hit.

This method throws an error if it is passed invalid radius or direction
inputs.

Code Samples

Spherecasting

Casts a sphere and returns the first collision with a [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain). Prints the properties of the RaycastResult if a result was hit.

```
local Workspace = game:GetService("Workspace")



local function castSphere()



-- The initial position of the cast spherical shape



local originPosition = Vector3.new(0, 50, 0)



-- The radius of the cast spherical shape in studs



local radius = 10



-- The direction the sphere is cast in



local direction = -Vector3.yAxis



-- The maximum distance of the cast



local distance = 50



-- Cast the sphere and create a visualization of it



local raycastResult = Workspace:Spherecast(originPosition, radius, direction * distance)



if raycastResult then



-- Print all properties of the RaycastResult if it exists



print(`Sphere intersected with: {raycastResult.Instance:GetFullName()}`)



print(`Intersection position: {raycastResult.Position}`)



print(`Distance between sphere's initial position and result: {raycastResult.Distance}`)



print(`The normal vector of the intersected face: {raycastResult.Normal}`)



print(`Material hit: {raycastResult.Material.Name}`)



else



print("Nothing was hit")



end



end



-- Continually cast a sphere every 2 seconds



while true do



castSphere()



task.wait(2)



end
```

Provide feedback

---

StepPhysics

Plugin Security

Advances the simulation for parts in the world forward based on a
specified time increment and an optional set of
[BaseParts](/docs/reference/engine/classes/BasePart).

WorldRoot:StepPhysics(

dt:[number](/docs/luau/numbers), parts:Instances

):()

Parameters

|  |
| --- |
| dt:[number](/docs/luau/numbers)  The amount of time that will be simulated. This argument must be a positive number. Larger values will increase the runtime of this function. |
| parts:Instances Default Value: "{}" Optional array of parts that will be simulated. This set must contain instances that are of type [BasePart](/docs/reference/engine/classes/BasePart); any other types will be ignored. |

Returns

()

Advances the simulation for parts in the world forward based on a
specified time increment and an optional set of [BasePart](/docs/reference/engine/classes/BasePart). When a
set of parts is specified, only these parts will be simulated and all
other parts in the world will be treated as anchored. When this argument
is left out, all parts in the world will be included in the simulation.
The specified time increment can be any positive number, with larger
values increasing the runtime of the function. Depending on the value of
the time increment, the physics system may subdivide it into multiple
individual steps to maintain the accuracy and stability of the simulation.
Even if the function performs multiple substeps, the results of the
simulation will only be seen once the function completes. To visualize the
individual steps of a simulation, the function can be called once per
RenderStep via the [RunService.RenderStepped](/docs/reference/engine/classes/RunService#RenderStepped) event.

Code Samples

StepPhysics

Simulates the parts in the workspace for a fixed period of time by calling the StepPhysics function once per frame until a specified time has elaspsed.

```
local RunService = game:GetService("RunService")



-- Optional array of parts to simulate; otherwise all parts will be simulated



local partsToSimulate = {



workspace.Part,



}



local function simulateParts(duration)



local time = 0.0



local stepJob



stepJob = RunService.RenderStepped:Connect(function(dt)



if time + dt > duration then



dt = duration - time



end



workspace:StepPhysics(dt, partsToSimulate)



time = time + dt



if time >= duration then



stepJob:Disconnect()



end



end)



end



-- Simulate workspace parts for 5 seconds, stepping the parts once per frame



simulateParts(5.0)
```

Provide feedback

---