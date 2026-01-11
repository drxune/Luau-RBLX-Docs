# PathfindingService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PathfindingService
Scraped: 2026-01-11T02:34:12.039213Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- PathfindingService
- Path
- Object
- TrussParts
- PathfindingModifiers
- PathfindingService:CreatePath()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PathfindingService](/docs/reference/engine/classes/PathfindingService)

English

Feedback

Engine Class

![PathfindingService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/PathfindingService-Dark.webp)PathfindingService

Used to find logical paths between two points.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [EmptyCutoff](#EmptyCutoff):[number](/docs/luau/numbers)  Deprecated |

Methods

|  |
| --- |
| [ComputeRawPathAsync](#ComputeRawPathAsync)(start: [Vector3](/docs/reference/engine/datatypes/Vector3),finish: [Vector3](/docs/reference/engine/datatypes/Vector3),maxDistance: [number](/docs/luau/numbers)):[Path](/docs/reference/engine/classes/Path)  Deprecated |
| [ComputeSmoothPathAsync](#ComputeSmoothPathAsync)(start: [Vector3](/docs/reference/engine/datatypes/Vector3),finish: [Vector3](/docs/reference/engine/datatypes/Vector3),maxDistance: [number](/docs/luau/numbers)):[Path](/docs/reference/engine/classes/Path)  Deprecated |
| [CreatePath](#CreatePath)(agentParameters: [Dictionary](/docs/luau/tables#dictionaries)):[Path](/docs/reference/engine/classes/Path) |
| [FindPathAsync](#FindPathAsync)(start: [Vector3](/docs/reference/engine/datatypes/Vector3),finish: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Path](/docs/reference/engine/classes/Path)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

PathfindingService is used to find logical paths between two points,
ensuring that characters can move between the points without running into
walls or other obstacles. By default, the shortest path is calculated, but you
can implement pathfinding modifiers to compute smarter paths across various
materials, around defined regions, or through obstacles.

See [Character Pathfinding](/docs/characters/pathfinding) for usage
details.

---

API Reference

Properties

EmptyCutoff

Deprecated

Show details

---

Methods

ComputeRawPathAsync

Deprecated

Show details

---

ComputeSmoothPathAsync

Deprecated

Show details

---

CreatePath

PathfindingService:CreatePath(agentParameters:[Dictionary](/docs/luau/tables#dictionaries)):[Path](/docs/reference/engine/classes/Path)

Parameters

|  |
| --- |
| agentParameters:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Luau table which lets you fine-tune the path for the size of the agent (the humanoid that will move along the path). See above for valid keys, types, and descriptions. |

Returns

[Path](/docs/reference/engine/classes/Path)

A [Path](/docs/reference/engine/classes/Path) object.

Creates a [Path](/docs/reference/engine/classes/Path) object based on various agent parameters. Valid
keys and values in the agentParameters table are as follows:

| Key | Type | Default | Description |
| --- | --- | --- | --- |
| **AgentRadius** | integer | 2 | Determines the minimum amount of horizontal space required for empty space to be considered traversable. |
| **AgentHeight** | integer | 5 | Determines the minimum amount of vertical space required for empty space to be considered traversable. |
| **AgentCanJump** | boolean | true | Determines whether jumping during pathfinding is allowed. |
| **AgentCanClimb** | boolean | false | Determines whether climbing [TrussParts](/docs/reference/engine/classes/TrussPart) during pathfinding is allowed. |
| **WaypointSpacing** | number | 4 | Determines the spacing between intermediate waypoints in path. |
| **Costs** | table | {} | Table of materials or defined [PathfindingModifiers](/docs/reference/engine/classes/PathfindingModifier) and their "cost" for traversal. Useful for making the agent prefer certain materials/regions over others. See [here](/docs/characters/pathfinding#pathfinding-modifiers) for details. |

Code Samples

Creating a Path with Pathfinding Service

Demonstrates creating a path using [PathfindingService:CreatePath()](/docs/reference/engine/classes/PathfindingService#CreatePath)

'PathOptions' represents a Model with three paths made of different materials.
When creating the path we define a large 'Cost' for two of the three paths materials.
This will ensure the path created steers towards the path with the material of the lowest 'Cost'.

Once the path is created, small parts are created at each waypoint to visualize the path.

```
local Workspace = game:GetService("Workspace")



local PathfindingService = game:GetService("PathfindingService")



-- This model contains a start, end and three paths between the player can walk on: Snow, Metal and LeafyGrass



local PathOptionsModel = script.Parent.PathOptions



local startPosition = PathOptionsModel.Start.Position



local finishPosition = PathOptionsModel.End.Position



-- Create a path that avoids Snow and Metal materials



-- This will ensure the path created avoids the Snow and Metal paths and guides



-- the user towards the LeafyGrass path



local path = PathfindingService:CreatePath({



AgentRadius = 3,



AgentHeight = 6,



AgentCanJump = false,



Costs = {



Snow = math.huge,



Metal = math.huge,



},



})



-- Compute the path



local success, errorMessage = pcall(function()



path:ComputeAsync(startPosition, finishPosition)



end)



-- Confirm the computation was successful



if success and path.Status == Enum.PathStatus.Success then



-- For each waypoint, create a part to visualize the path



for _, waypoint in path:GetWaypoints() do



local part = Instance.new("Part")



part.Position = waypoint.Position



part.Size = Vector3.new(0.5, 0.5, 0.5)



part.Color = Color3.new(1, 0, 1)



part.Anchored = true



part.CanCollide = false



part.Parent = Workspace



end



else



print(`Path unable to be computed, error: {errorMessage}`)



end
```

Provide feedback

---

FindPathAsync

Deprecated

Show details

---