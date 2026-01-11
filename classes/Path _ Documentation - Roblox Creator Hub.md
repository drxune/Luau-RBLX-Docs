# Path | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Path
Scraped: 2026-01-11T02:41:19.172558Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- Path
- PathfindingService:CreatePath()
- Path:ComputeAsync()
- CreatePath()
- ComputeAsync()
- Path.Status
- GetWaypoints()
- Path.Blocked
- Path:GetWaypoints()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Path](/docs/reference/engine/classes/Path)

English

Feedback

Engine Class

Path

Stores the result of paths created by [PathfindingService:CreatePath()](/docs/reference/engine/classes/PathfindingService#CreatePath).

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [Status](#Status):[Enum.PathStatus](/docs/reference/engine/enums/PathStatus) |

Methods

|  |
| --- |
| [CheckOcclusionAsync](#CheckOcclusionAsync)(start: [number](/docs/luau/numbers)):[number](/docs/luau/numbers)  Deprecated |
| [ComputeAsync](#ComputeAsync)(start: [Vector3](/docs/reference/engine/datatypes/Vector3),finish: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [GetPointCoordinates](#GetPointCoordinates)():[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetWaypoints](#GetWaypoints)():[Array](/docs/luau/tables#arrays) |

Events

|  |
| --- |
| [Blocked](#Blocked)(blockedWaypointIdx: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Unblocked](#Unblocked)(unblockedWaypointIdx: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Path objects store the result of paths created by
[PathfindingService:CreatePath()](/docs/reference/engine/classes/PathfindingService#CreatePath).

Once a path object is created, you can call [Path:ComputeAsync()](/docs/reference/engine/classes/Path#ComputeAsync) with a
starting point and ending point. This will attempt to compute a valid path for
a character to move along, based on default or custom parameters passed to
[CreatePath()](/docs/reference/engine/classes/PathfindingService#CreatePath). If
[ComputeAsync()](/docs/reference/engine/classes/Path#ComputeAsync) successfully finds a path, the
[Path](/docs/reference/engine/classes/Path) object will have a [Path.Status](/docs/reference/engine/classes/Path#Status) value of
[Enum.PathStatus.Success](/docs/reference/engine/enums/PathStatus#Success). Otherwise the status will be
[Enum.PathStatus.NoPath](/docs/reference/engine/enums/PathStatus#NoPath) which can occur if there are obstacles between the
two points (and no way around) or if the points are inside of solid objects.

In addition to [ComputeAsync()](/docs/reference/engine/classes/Path#ComputeAsync), [Path](/docs/reference/engine/classes/Path)
objects have the [GetWaypoints()](/docs/reference/engine/classes/Path#GetWaypoints) method which
returns a list of waypoints representing the points a character should follow
in sequence to get from the beginning to the end of the path.

Finally, [Path](/docs/reference/engine/classes/Path) objects can be connected to the [Path.Blocked](/docs/reference/engine/classes/Path#Blocked)
event. This event will fire if, at any time during the path's existence, the
path is blocked. Note that this can occur behind a character moving along
the path, not just in front of it.

---

API Reference

Properties

Status

Read Only

Not Replicated

Read Parallel

The success of the generated [Path](/docs/reference/engine/classes/Path).

Path.Status:[Enum.PathStatus](/docs/reference/engine/enums/PathStatus)

The success of the generated [Path](/docs/reference/engine/classes/Path).

Provide feedback

---

Methods

CheckOcclusionAsync

Deprecated

Show details

---

ComputeAsync

Yields

Computes a [Path](/docs/reference/engine/classes/Path) from a start position to an end position.

Path:ComputeAsync(

start:[Vector3](/docs/reference/engine/datatypes/Vector3), finish:[Vector3](/docs/reference/engine/datatypes/Vector3)

):()

Parameters

|  |
| --- |
| start:[Vector3](/docs/reference/engine/datatypes/Vector3)  The world position where the computed path begins. |
| finish:[Vector3](/docs/reference/engine/datatypes/Vector3)  The world position where the computed path finishes. |

Returns

()

This function computes a [Path](/docs/reference/engine/classes/Path) from a start position to an end
position. This function is not automatically called when a path is created
and must be invoked each time the path needs to be updated.

Once the Path is computed, it will have a series of waypoints that, when
followed, can lead a character along the path. These points are gathered
with the [Path:GetWaypoints()](/docs/reference/engine/classes/Path#GetWaypoints) function.

Code Samples

Using the Pathfinding Service

The code sample below explores how to move an NPC along a more complex path or
around obstacles. This is known as pathfinding.

```
local PathfindingService = game:GetService("PathfindingService")



local agentParams = {



AgentRadius = 2.0,



AgentHeight = 5.0,



AgentCanJump = false,



}



local currentWaypointIdx = 1



local path = PathfindingService:CreatePath(agentParams)



local humanoidRootPart = script.Parent:FindFirstChild("HumanoidRootPart")



local targetPosition = Vector3.new(50, 0, 50)



path:ComputeAsync(humanoidRootPart.Position, targetPosition)



-- When the path is blocked...



local function OnPathBlocked(blockedWaypointIdx)



-- Check if the obstacle is further down the path



if blockedWaypointIdx > currentWaypointIdx then



-- Recompute the path



path:ComputeAsync(humanoidRootPart.Position, targetPosition)



if path.Status == Enum.PathStatus.Success then



-- Retrieve update waypoint list with path:GetWaypoints()



-- and Continue walking towards target



else



-- Error, path not found



end



end



end



path.Blocked:Connect(OnPathBlocked)
```

Provide feedback

---

GetPointCoordinates

Deprecated

Show details

---

GetWaypoints

Returns an array of points in the path.

Path:GetWaypoints():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of [PathWaypoints](/docs/reference/engine/datatypes/PathWaypoint) ordered from path
start to path end.

This function returns an array of all the
[PathWaypoints](/docs/reference/engine/datatypes/PathWaypoint) in a [Path](/docs/reference/engine/classes/Path), as computed by
[Path:ComputeAsync()](/docs/reference/engine/classes/Path#ComputeAsync).

Each waypoint in the array specifies a [Vector3](/docs/reference/engine/datatypes/Vector3) position and
[action](/docs/reference/engine/enums/PathWaypointAction) to take when this PathWaypoint is
reached. The array is arranged in the order of waypoints from the path
start to path end.

If a path could not be computed, this function will return an empty array.

Code Samples

Get Path Waypoints

The example below demonstrates how to create a Path and it's
[PathWaypoints](/docs/reference/engine/datatypes/PathWaypoint) using the PathService.

It tries to [Path:ComputeAsync()](/docs/reference/engine/classes/Path#ComputeAsync) a path between two [Vector3](/docs/reference/engine/datatypes/Vector3)
positions, from pathStart to pathEnd. If a path is successfully created,
indicated by it's [Enum.PathStatus](/docs/reference/engine/enums/PathStatus), the code block gets an array of its
waypoints using [Path:GetWaypoints()](/docs/reference/engine/classes/Path#GetWaypoints). Then, it loops through the array
and prints each waypoint's position.

```
local PathfindingService = game:GetService("PathfindingService")



local path = PathfindingService:CreatePath()



local PATH_START = Vector3.new(0, 1, 0)



local PATH_END = Vector3.new(100, 1, 25)



path:ComputeAsync(PATH_START, PATH_END)



if path.Status == Enum.PathStatus.Success then



local waypoints = path:GetWaypoints()



for _, waypoint in pairs(waypoints) do



print(waypoint.Position)



end



end
```

Provide feedback

---

Events

Blocked

Fires when the computed path becomes blocked.

Path.Blocked(blockedWaypointIdx:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| blockedWaypointIdx:[number](/docs/luau/numbers) |

Fires when the computed path becomes blocked. Note that paths may become
blocked somewhere behind the agent, such as a pile of rubble falling
on a path as the agent runs away. See
[Handling Blocked Paths](/docs/characters/pathfinding#handling-blocked-paths)
for details on checking the forward waypoint progress of an agent along a
path.

Provide feedback

---

Unblocked

Fires when a computed path that was blocked becomes unblocked.

Path.Unblocked(unblockedWaypointIdx:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| unblockedWaypointIdx:[number](/docs/luau/numbers) |

Fires when a computed path that was blocked becomes unblocked. Note that a
blocked path may become unblocked somewhere behind the agent,
effectively making reaction to this event unnecessary. See
[Handling Blocked Paths](/docs/characters/pathfinding#handling-blocked-paths)
for details on checking the forward waypoint progress of an agent along a
path.

Provide feedback

---