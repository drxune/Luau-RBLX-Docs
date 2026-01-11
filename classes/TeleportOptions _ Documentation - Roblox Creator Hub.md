# TeleportOptions | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TeleportOptions
Scraped: 2026-01-11T02:41:27.351592Z

## Inherits
- Object
- Instance
- TeleportOptions
- TeleportService:TeleportAsync()
- DataModel.JobId
- TeleportOptions.ServerInstanceId
- TeleportOptions:SetTeleportData()
- Player:GetJoinData()
- TeleportService:GetLocalPlayerTeleportData()
- DataModel.PlaceId
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TeleportOptions](/docs/reference/engine/classes/TeleportOptions)

English

Feedback

Engine Class

TeleportOptions

Optional input arguments to the [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync)
function.

---

Summary

Properties

|  |
| --- |
| [ReservedServerAccessCode](#ReservedServerAccessCode):[string](/docs/luau/strings) |
| [ServerInstanceId](#ServerInstanceId):[string](/docs/luau/strings) |
| [ShouldReserveServer](#ShouldReserveServer):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetTeleportData](#GetTeleportData)():Variant |
| [SetTeleportData](#SetTeleportData)(teleportData: Variant):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This class is an optional parameter to the
[TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync) function that allows developers to
provide arguments for the teleport call.

Certain arguments in this class are not compatible with each other and cause
an error when passed to [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync):

* ReservedServerAccessCode + ServerInstanceId
* ShouldReserveServer + ServerInstanceId
* ShouldReserveServer + ReservedServerAccessCode

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

---

API Reference

Properties

ReservedServerAccessCode

Read Parallel

The reserved server access code that indicates the reserved server that
the teleport should be to.

TeleportOptions.ReservedServerAccessCode:[string](/docs/luau/strings)

This property indicates the reserved server access code for the reserved
server that the user(s) should be teleported to.

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

Provide feedback

---

ServerInstanceId

Read Parallel

The [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of the server instance to teleport to.

TeleportOptions.ServerInstanceId:[string](/docs/luau/strings)

This property indicates the [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of the server instance
the user(s) should be teleported to.

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

Provide feedback

---

ShouldReserveServer

Read Parallel

A flag to indicate if a reserved server should be allocated and the
players should then be teleported to this allocation.

TeleportOptions.ShouldReserveServer:[boolean](/docs/luau/booleans)

This property indicates whether the teleport call should create a new
reserved server. When set to true, a reserved server will be created and
the player(s) will be teleported to the new server.

If set to false, the player(s) will be teleported to the public server
with the specified [TeleportOptions.ServerInstanceId](/docs/reference/engine/classes/TeleportOptions#ServerInstanceId) if provided.
When [TeleportOptions.ServerInstanceId](/docs/reference/engine/classes/TeleportOptions#ServerInstanceId) is blank or no matching
server is found, a new public server will be created to teleport the
player(s) to.

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

Provide feedback

---

Methods

GetTeleportData

Returns the teleport data stored in the [TeleportOptions](/docs/reference/engine/classes/TeleportOptions) instance
by [TeleportOptions:SetTeleportData()](/docs/reference/engine/classes/TeleportOptions#SetTeleportData).

TeleportOptions:GetTeleportData():Variant

Returns

Variant

This function returns the teleport data stored in the
[TeleportOptions](/docs/reference/engine/classes/TeleportOptions) instance by
[TeleportOptions:SetTeleportData()](/docs/reference/engine/classes/TeleportOptions#SetTeleportData).

Once a player has teleported, teleport data can be retrieved using the
[Player:GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData) and
[TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData) functions.

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

Provide feedback

---

SetTeleportData

Setter function for data to be passed to the destination place.

TeleportOptions:SetTeleportData(teleportData:Variant):()

Parameters

|  |
| --- |
| teleportData:Variant  Data to be passed to the destination place. |

Returns

()

This is a setter function for data to be passed to the destination place.
On the destination place, this data can be retrieved using
[Player:GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData) or
[TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData).

For example, the following snippet would send the
[DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) and [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) in a dictionary
passing the teleport data in a [TeleportOptions](/docs/reference/engine/classes/TeleportOptions) instance using
[TeleportOptions:SetTeleportData()](/docs/reference/engine/classes/TeleportOptions#SetTeleportData):

```
-- Server



local teleportOptions = Instance.new("TeleportOptions")



local teleportData = {



placeId = game.PlaceId,



jobId = game.JobId



}



teleportOptions:SetTeleportData(teleportData)



TeleportService:TeleportAsync(game.PlaceId, {player}, teleportOptions)
```

This data could then be retrieved upon arrival using the
GetLocalPlayerTeleportData() function as follows:

```
-- Client



local TeleportService = game:GetService("TeleportService")



local teleportData = TeleportService:GetLocalPlayerTeleportData()



if teleportData then



local placeId = teleportData.placeId



local jobId = teleportData.JobId



end
```

If no teleportData was set in the teleportation function this
GetLocalPlayerTeleportData() will return nil.

For more information on how to send and receive user data along with
teleports, see, see
[Teleporting Between Places](/docs/projects/teleport#sending-user-data-along-with-teleports).

Provide feedback

---