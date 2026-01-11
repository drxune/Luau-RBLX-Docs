# PlayerViewService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PlayerViewService
Scraped: 2026-01-11T02:27:42.074798Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- PlayerViewService
- Player
- Object
- PlayerViewService:GetDeviceCameraCFrame()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PlayerViewService](/docs/reference/engine/classes/PlayerViewService)

English

Feedback

Engine Class

PlayerViewService

Provides a way to get additional information about a player's view.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetDeviceCameraCFrame](#GetDeviceCameraCFrame)(player: [Player](/docs/reference/engine/classes/Player)):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[PlayerViewService](/docs/reference/engine/classes/PlayerViewService) provides a way to get additional information about a
player's view.

---

API Reference

Methods

GetDeviceCameraCFrame

Returns a world space [CFrame](/docs/reference/engine/datatypes/CFrame) looking at the player's character.

PlayerViewService:GetDeviceCameraCFrame(player:[Player](/docs/reference/engine/classes/Player)):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) Default Value: "nil" The player for which to get the device camera [CFrame](/docs/reference/engine/datatypes/CFrame). |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

The world space [CFrame](/docs/reference/engine/datatypes/CFrame) looking at the player's character,
or a [CFrame.identity](/docs/reference/engine/datatypes/CFrame#identity) (see description).

Returns a world space [CFrame](/docs/reference/engine/datatypes/CFrame) looking at the player's character,
such that setting the current camera's [CFrame](/docs/reference/engine/datatypes/CFrame) will view that
character from the perspective of their device.

This method leverages the device's camera and it only functions on mobile
devices. If no information is available, for example the user is not on a
mobile device or they don't have their camera turned on, this method
returns a [CFrame.identity](/docs/reference/engine/datatypes/CFrame#identity).

See [Roblox Connect](/docs/resources/roblox-connect) for a sample
implementation of this method.

Code Samples

PlayerViewService:GetDeviceCameraCFrame()

Updates the local player's camera by using [PlayerViewService:GetDeviceCameraCFrame()](/docs/reference/engine/classes/PlayerViewService#GetDeviceCameraCFrame). This method returns a world space [CFrame](/docs/reference/engine/datatypes/CFrame) looking at the player's character, such that setting the current camera's [CFrame](/docs/reference/engine/datatypes/CFrame) will view that character from the perspective of their device.

```
local PlayerViewService = game:GetService("PlayerViewService")



local RunService = game:GetService("RunService")



local Workspace = game:GetService("Workspace")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local camera = Workspace.CurrentCamera



local function updatePictureInPictureCamera()



camera.CFrame = PlayerViewService:GetDeviceCameraCFrame(player)



end



RunService:BindToRenderStep(



"PictureInPictureCamera",



Enum.RenderPriority.Camera.Value + 1,



updatePictureInPictureCamera



)
```

Provide feedback

---