# NetworkPeer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NetworkPeer
Scraped: 2026-01-11T02:31:01.724406Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- NetworkPeer
- NetworkClient
- NetworkServer
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [NetworkPeer](/docs/reference/engine/classes/NetworkPeer)

English

Feedback

Engine Class

NetworkPeer

The NetworkPeer object is the most basic class of the network objects.

Not Creatable

Not Browsable

---

Summary

Methods

|  |
| --- |
| [SetOutgoingKBPSLimit](#SetOutgoingKBPSLimit)(limit: [number](/docs/luau/numbers)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[NetworkClient](/docs/reference/engine/classes/NetworkClient), [NetworkServer](/docs/reference/engine/classes/NetworkServer)

The NetworkPeer object is the most basic class of the network objects.

---

API Reference

Methods

SetOutgoingKBPSLimit

Plugin Security

Sets the maximum outgoing bandwidth that Roblox can use.

NetworkPeer:SetOutgoingKBPSLimit(limit:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| limit:[number](/docs/luau/numbers) |

Returns

()

Sets the maximum outgoing bandwidth that Roblox can use.

Code Samples

NetworkPeer:SetOutgoingKBPSLimit

The following code, when ran from the command bar or a plugin, would limit
bandwidth to 1KBPS.

```
local NetworkClient = game:GetService("NetworkClient")



NetworkClient:SetOutgoingKBPSLimit(1)
```

Provide feedback

---