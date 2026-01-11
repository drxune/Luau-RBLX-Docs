# NetworkServer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NetworkServer
Scraped: 2026-01-11T02:40:03.497174Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- NetworkPeer
- NetworkServer
- Instance
- Object
- NetworkReplicator
- NetworkPeer:SetOutgoingKBPSLimit()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [NetworkPeer](/docs/reference/engine/classes/NetworkPeer)
6. /
7. [NetworkServer](/docs/reference/engine/classes/NetworkServer)

English

Feedback

Engine Class

NetworkServer

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [EncryptStringForPlayerId](#EncryptStringForPlayerId)(toEncrypt: [string](/docs/luau/strings),playerId: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |

Inherited Members

1 inherited from [NetworkPeer](/docs/reference/engine/classes/NetworkPeer)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [NetworkServer](/docs/reference/engine/classes/NetworkServer) stores all the [NetworkReplicator](/docs/reference/engine/classes/NetworkReplicator) in the game
and handles all connections. [NetworkPeer:SetOutgoingKBPSLimit()](/docs/reference/engine/classes/NetworkPeer#SetOutgoingKBPSLimit) can be
used to imitate latency while using Start Server.

---

API Reference

Methods

EncryptStringForPlayerId

NetworkServer:EncryptStringForPlayerId(

toEncrypt:[string](/docs/luau/strings), playerId:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| toEncrypt:[string](/docs/luau/strings) |
| playerId:[number](/docs/luau/numbers) |

Returns

[string](/docs/luau/strings)

Provide feedback

---