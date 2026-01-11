# TeleportAsyncResult | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TeleportAsyncResult
Scraped: 2026-01-11T02:31:57.632744Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- TeleportAsyncResult
- Object
- DataModel.PrivateServerId
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TeleportAsyncResult](/docs/reference/engine/classes/TeleportAsyncResult)

English

Feedback

Engine Class

TeleportAsyncResult

The return structure of the TeleportAsync function call.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [PrivateServerId](#PrivateServerId):[string](/docs/luau/strings) |
| [ReservedServerAccessCode](#ReservedServerAccessCode):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This class is an instance that is returned by the TeleportAsync function
with information about the teleport.

---

API Reference

Properties

PrivateServerId

Read Only

Not Replicated

Read Parallel

The private server ID of the reserved server that the players are being
teleported to.

TeleportAsyncResult.PrivateServerId:[string](/docs/luau/strings)

The private server ID of the reserved server that the players are being
teleported to. This field is populated only if the teleport is to a
reserved server.

This field is not the same as the private server ID of the server that
initiated the teleport, please see: [DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId)

See also:

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

Provide feedback

---

ReservedServerAccessCode

Read Only

Not Replicated

Read Parallel

The access code of the reserved server that the players are being
teleported to.

TeleportAsyncResult.ReservedServerAccessCode:[string](/docs/luau/strings)

The access code of the reserved server that the players are being
teleported to. This field is populated only if the teleport is to a
reserved server. This allows developers to perform subsequent teleports to
this same reserved server.

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

Provide feedback

---