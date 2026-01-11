# TeleportState | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/TeleportState
Scraped: 2026-01-11T02:43:22.253477Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [TeleportState](/docs/reference/engine/enums/TeleportState)

English

Feedback

Engine Enum

TeleportState

---

Determines the current teleportation state of a player.

Items

| Name | Value | Summary |
| --- | --- | --- |
| RequestedFromServer | 0 | The server has requested that the client teleport. |
| Started | 1 | The client has started attempting to teleport. |
| WaitingForServer | 2 | The client is waiting for the server to respond to the teleport request. |
| Failed | 3 | The teleport failed. |
| InProgress | 4 | The teleport is currently in progress. The player usually disconnects and teleports to the destination after this. |