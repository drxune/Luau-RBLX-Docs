# GenerationService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GenerationService
Scraped: 2026-01-11T02:30:09.195762Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- GenerationService
- Player
- MeshPart
- Object
- GenerateMeshAsync()
- LoadGeneratedMeshAsync()
- Model
- EditableMesh
- RemoteEvent
- ReplicatedStorage
- Part
- Workspace
- TextButton
- LocalScript
- StarterPlayerScripts
- GenerationService:GenerateMeshAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [GenerationService](/docs/reference/engine/classes/GenerationService)

English

Feedback

Engine Class

GenerationService

Service that allows developers to generate 3D objects from text prompts.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [GenerateMeshAsync](#GenerateMeshAsync)(inputs: [Dictionary](/docs/luau/tables#dictionaries),player: [Player](/docs/reference/engine/classes/Player),options: [Dictionary](/docs/luau/tables#dictionaries),intermediateResultCallback: [function](/docs/luau/functions)?):[Tuple](/docs/luau/tuples) |
| [GenerateModelAsync](#GenerateModelAsync)(inputs: [Dictionary](/docs/luau/tables#dictionaries),schema: [Dictionary](/docs/luau/tables#dictionaries),options: [Dictionary](/docs/luau/tables#dictionaries)?):[Tuple](/docs/luau/tuples) |
| [LoadGeneratedMeshAsync](#LoadGeneratedMeshAsync)(generationId: [string](/docs/luau/strings)):[MeshPart](/docs/reference/engine/classes/MeshPart) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

GenerationService enables you to generate 3D objects from text prompts using
Roblox's Cube 3D foundation model. This enables the generation of objects like
environmental props in-experience.

You can control the output by providing an optional [Vector3](/docs/reference/engine/datatypes/Vector3) to the
SuggestedSize parameter. Rather than simply rescaling the result, this
parameter guides the model during the creation process, influencing it to
create a mesh that attempts to match the proportions and size of your
specified bounding box.

Mesh generation is a two step process:

1. [GenerateMeshAsync()](/docs/reference/engine/classes/GenerationService#GenerateMeshAsync) starts
   the mesh generation process using a text prompt and other required
   parameters. It returns a unique identifier (generation ID) that can be used
   to retrieve the future result.
2. [LoadGeneratedMeshAsync()](/docs/reference/engine/classes/GenerationService#LoadGeneratedMeshAsync)
   loads the generated mesh into the experience. The mesh is returned as a
   [MeshPart](/docs/reference/engine/classes/MeshPart) or [Model](/docs/reference/engine/classes/Model).

Currently, GenerationService only supports the following usage:

* [GenerateMeshAsync()](/docs/reference/engine/classes/GenerationService#GenerateMeshAsync) must be
  called from server scripts.
* [LoadGeneratedMeshAsync()](/docs/reference/engine/classes/GenerationService#LoadGeneratedMeshAsync)
  must be called from client scripts.

As a result, when a mesh generation request originates from a client, the
client must send a signal to the server to initiate generation. Once the
server determines that generation is complete, it should notify the
appropriate client to call
[LoadGeneratedMeshAsync()](/docs/reference/engine/classes/GenerationService#LoadGeneratedMeshAsync)
and retrieve the mesh. Note that since the generated mesh is loaded with
[EditableMesh](/docs/reference/engine/classes/EditableMesh) content and only on the client, it is not replicated to
any other clients.

See
[this demo experience](https://www.roblox.com/games/108838517877898/SuggestedSize-Generation-Template)
for a more detailed example including usage of the SuggestedSize option
(click the ⋯ button and Edit in Studio).

Code Samples

Server-Side Mesh Generation

This setup includes server-side functionality to handle mesh
generation requests from clients.

```
local GenerationService = game:GetService("GenerationService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



-- Create a RemoteEvent for client-server communication



local generationEvent = Instance.new("RemoteEvent")



generationEvent.Name = "GenerationEvent"



generationEvent.Parent = ReplicatedStorage



-- Create a RemoteEvent to send generation results back to clients



local generationResultEvent = Instance.new("RemoteEvent")



generationResultEvent.Name = "GenerationResultEvent"



generationResultEvent.Parent = ReplicatedStorage



-- Handle mesh generation requests from clients



generationEvent.OnServerEvent:Connect(function(player, prompt)



print("Generating mesh for player", player.Name, "with prompt:", prompt)



-- Generate the mesh on the server



local success, generationId, contextId = pcall(function()



return GenerationService:GenerateMeshAsync(



{ ["Prompt"] = prompt },



player,



{},



function(intermediateType, intermediateGenerationId, intermediateContextId)



-- Send intermediate result to the requesting client



generationResultEvent:FireClient(



player,



intermediateGenerationId,



true -- isIntermediate



)



end



)



end)



if success then



-- Send the final generation ID to the client



generationResultEvent:FireClient(player, generationId, false)



print("Successfully generated mesh with ID:", generationId)



else



generationResultEvent:FireClient(player, nil, false)



warn("Failed to generate mesh:", generationId)



end



end)
```

Client-Side Mesh Generation

The following example adds client-side functionality to request
mesh generation from the server and display the results. This code assumes that
the two [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instances created by the server-side example
(GenerationEvent and GenerationResultEvent) exist inside
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage).

```
local GenerationService = game:GetService("GenerationService")



local Players = game:GetService("Players")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



-- Reference to RemoteEvent instances created in server-side script



local generationEvent = ReplicatedStorage:WaitForChild("GenerationEvent")



local generationResultEvent = ReplicatedStorage:WaitForChild("GenerationResultEvent")



local player = Players.LocalPlayer



-- Store generated meshes



local generatedMeshes = {}



-- Function to request mesh generation



local function requestMeshGeneration(prompt)



print("Requesting mesh generation for prompt:", prompt)



generationEvent:FireServer(prompt)



end



-- Handle generation results from the server



generationResultEvent.OnClientEvent:Connect(function(generationId, isIntermediate)



if not generationId then



warn("Generation failed")



return



end



print(isIntermediate and "Loading intermediate result..." or "Loading final result...")



-- Use generation ID generated on the server to retrieve and load the mesh



local mesh = GenerationService:LoadGeneratedMeshAsync(generationId)



if mesh then



-- Clean up previous mesh if it exists



if generatedMeshes[isIntermediate and "intermediate" or "final"] then



generatedMeshes[isIntermediate and "intermediate" or "final"]:Destroy()



end



mesh.Parent = workspace



-- Position the mesh in front of the player



local character = player.Character



if character and character:FindFirstChild("HumanoidRootPart") then



local rootPart = character.HumanoidRootPart



mesh:PivotTo(rootPart.CFrame * CFrame.new(0, 0, -10))



end



-- Store the mesh for cleanup



generatedMeshes[isIntermediate and "intermediate" or "final"] = mesh



print(isIntermediate and "Loaded intermediate result" or "Loaded final result")



else



warn("Failed to load mesh")



end



end)



-- Example usage



requestMeshGeneration("toy robot")
```

Server-Side Mesh Generation With Suggested Size

This server-side script gets the size from a [Part](/docs/reference/engine/classes/Part) in the
[Workspace](/docs/reference/engine/classes/Workspace) named SizeBox and tells the client when the model is ready.

```
local GenerationService = game:GetService("GenerationService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local Workspace = game:GetService("Workspace")



-- Create a RemoteEvent for client-server communication



local generationEvent = Instance.new("RemoteEvent")



generationEvent.Name = "GenerationEvent"



generationEvent.Parent = ReplicatedStorage



-- Create a RemoteEvent to send generation results back to clients



local generationResultEvent = Instance.new("RemoteEvent")



generationResultEvent.Name = "GenerationResultEvent"



generationResultEvent.Parent = ReplicatedStorage



local sizeBox = Workspace:WaitForChild("SizeBox")



generationEvent.OnServerEvent:Connect(function(player, prompt)



-- Get the size from the part



local boundingBoxSize = sizeBox.Size



print("Server received request; using SuggestedSize:", boundingBoxSize)



-- Run the generation in a separate thread



task.spawn(function()



local success, generationId = pcall(function()



return GenerationService:GenerateMeshAsync(



{ ["Prompt"] = prompt },



player,



{ ["SuggestedSize"] = boundingBoxSize } -- Use the size from the box



)



end)



if success and generationId then



print("Server generation complete; sending ID to client:", generationId)



-- Tell the client it's ready and provide the position for the new model



generationResultEvent:FireClient(player, generationId, sizeBox.CFrame)



else



warn("Server generation failed:", generationId)



end



end)



end)
```

Button-Triggered Mesh Generation With Suggested Size

The following example sends the generation request to the server
via a parent [TextButton](/docs/reference/engine/classes/TextButton). This code assumes there's a [Part](/docs/reference/engine/classes/Part) named
SizeBox in the [Workspace](/docs/reference/engine/classes/Workspace). It also assumes that the [RemoteEvent](/docs/reference/engine/classes/RemoteEvent)
instance created by the server-side example (GenerationEvent) exists inside
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage).

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



-- Reference to RemoteEvent instance created in server-side script



local generationEvent = ReplicatedStorage:WaitForChild("GenerationEvent")



local button = script.Parent



local PROMPT = "cabinet"



button.Activated:Connect(function()



local prompt = PROMPT



print("Client requesting generation with prompt:", prompt)



generationEvent:FireServer(prompt)



end)
```

Client-Side Mesh Generation With Suggested Size

The following code, placed in a [LocalScript](/docs/reference/engine/classes/LocalScript) in
[StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts), listens for the server's signal and loads the
model. This example assumes there's a [Part](/docs/reference/engine/classes/Part) named SizeBox in the
[Workspace](/docs/reference/engine/classes/Workspace). It also assumes that the [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instance created
by the server-side example (GenerationEvent) exists inside
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage).

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local GenerationService = game:GetService("GenerationService")



local Workspace = game:GetService("Workspace")



local sizeBox = Workspace:WaitForChild("SizeBox")



-- Reference to RemoteEvent instance created in server-side script



local generationEvent = ReplicatedStorage:WaitForChild("GenerationEvent")



generationEvent.OnClientEvent:Connect(function(generationId, targetCFrame)



print("Client received signal to load model with ID:", generationId)



local success, result = pcall(function()



return GenerationService:LoadGeneratedMeshAsync(generationId)



end)



if success and result then



result.Parent = Workspace



result:PivotTo(targetCFrame)



print("Client successfully loaded and placed model")



-- Make the box a transparent, non-collidable container



sizeBox.CanCollide = false



sizeBox.Transparency = 0.85



else



warn("Client failed to load model:", result)



end



end)
```

---

API Reference

Methods

GenerateMeshAsync

Yields

Starts the generation of a new 3D mesh from a text prompt and returns
unique IDs used to track and retrieve the result.

GenerationService:GenerateMeshAsync(

inputs:[Dictionary](/docs/luau/tables#dictionaries), player:[Player](/docs/reference/engine/classes/Player), options:[Dictionary](/docs/luau/tables#dictionaries), intermediateResultCallback:[function](/docs/luau/functions)?

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| inputs:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary containing the mesh generation prompts. Currently, the only supported key is the Prompt (string) that describes the mesh to generate. |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) requesting the generation. |
| options:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary for additional generation options to influence the result. The following key is supported: - SuggestedSize — Optional [Vector3](/docs/reference/engine/datatypes/Vector3) representing a size guide for the generated asset. The service will attempt to create a model with a size and proportion similar to the provided [Vector3](/docs/reference/engine/datatypes/Vector3). This does not guarantee the final output size. |
| intermediateResultCallback:[function](/docs/luau/functions)?  A callback function triggered with intermediate generation results. Useful for retrieving early mesh versions before textures are applied. |

Returns

[Tuple](/docs/luau/tuples)

A tuple of the generation ID (a unique ID returned for each invocation
of GenerateMeshAsync()) and context ID (not currently used).

Starts the generation of a new 3D mesh from a text prompt and returns
unique IDs used to track and retrieve the result. You can optionally
receive intermediate results, such as the untextured mesh, by providing an
intermediateResultCallback function. After the generation is complete,
use
[LoadGeneratedMeshAsync()](/docs/reference/engine/classes/GenerationService#LoadGeneratedMeshAsync)
to load and display the generated mesh.

Error Codes

| Error | Description | Recommended developer action |
| --- | --- | --- |
| Rate limit exceeded | The maximum number of mesh generations has been exceeded for the minute. | Wait until the rate limit resets. |
| Moderation failed | The mesh generation was flagged for moderation. | Review and modify the prompt to ensure it adheres to Roblox's moderation guidelines. |
| Internal server error | An unexpected issue occurred on the server. | Retry the request later or check server status for issues. |
| Character limit exceeded | The input prompt length for this generation request exceeded the limit. | Reduce the number of characters in the Prompt string of the input dictionary. |
| Service overloaded | The service is overloaded. | Retry the request later. |
| Size dimensions must all be greater than 0 | Invalid size provided. | Change the size to above 0. |

Provide feedback

---

GenerateModelAsync

Yields

GenerationService:GenerateModelAsync(

inputs:[Dictionary](/docs/luau/tables#dictionaries), schema:[Dictionary](/docs/luau/tables#dictionaries), options:[Dictionary](/docs/luau/tables#dictionaries)?

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| inputs:[Dictionary](/docs/luau/tables#dictionaries) |
| schema:[Dictionary](/docs/luau/tables#dictionaries) |
| options:[Dictionary](/docs/luau/tables#dictionaries)? |

Returns

[Tuple](/docs/luau/tuples)

Provide feedback

---

LoadGeneratedMeshAsync

Yields

Retrieves and loads a mesh generated by
[GenerationService:GenerateMeshAsync()](/docs/reference/engine/classes/GenerationService#GenerateMeshAsync) using the provided
generationId.

GenerationService:LoadGeneratedMeshAsync(generationId:[string](/docs/luau/strings)):[MeshPart](/docs/reference/engine/classes/MeshPart)

Parameters

|  |
| --- |
| generationId:[string](/docs/luau/strings)  The unique ID returned by [GenerateMeshAsync()](/docs/reference/engine/classes/GenerationService#GenerateMeshAsync). Identifies the mesh to load. |

Returns

[MeshPart](/docs/reference/engine/classes/MeshPart)

The generated asset, returned as a [Model](/docs/reference/engine/classes/Model) with a single
[MeshPart](/docs/reference/engine/classes/MeshPart) containing an [EditableMesh](/docs/reference/engine/classes/EditableMesh).

Retrieves and loads a mesh generated by
[GenerateMeshAsync()](/docs/reference/engine/classes/GenerationService#GenerateMeshAsync) using
the provided generationId. The mesh can be returned as a
[MeshPart](/docs/reference/engine/classes/MeshPart) or [Model](/docs/reference/engine/classes/Model). Because editable meshes are not
replicated, the loaded mesh is not replicated to any other clients and can
only be loaded once per generationId.

Provide feedback

---