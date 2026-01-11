# NetworkClient | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NetworkClient
Scraped: 2026-01-11T02:32:19.522629Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- NetworkPeer
- NetworkClient
- Instance
- Object
- ClientReplicator
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [NetworkPeer](/docs/reference/engine/classes/NetworkPeer)
6. /
7. [NetworkClient](/docs/reference/engine/classes/NetworkClient)

English

Feedback

Engine Class

![NetworkClient](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/NetworkClient-Dark.webp)NetworkClient

Not Creatable

Service

Not Replicated

---

Summary

Events

|  |
| --- |
| [ConnectionAccepted](#ConnectionAccepted)(peer: [string](/docs/luau/strings),replicator: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ConnectionFailed](#ConnectionFailed)(peer: [string](/docs/luau/strings),code: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

1 inherited from [NetworkPeer](/docs/reference/engine/classes/NetworkPeer)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This service is responsible for connecting a client to a server.

---

API Reference

Events

ConnectionAccepted

Fired when the client successfully connects to a server. Returns a string
showing the server's IP and port, and the client's
[ClientReplicator](/docs/reference/engine/classes/ClientReplicator).

NetworkClient.ConnectionAccepted(

peer:[string](/docs/luau/strings), replicator:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| peer:[string](/docs/luau/strings)  The server's IP and port. |
| replicator:[Instance](/docs/reference/engine/datatypes/Instance)  The client's [ClientReplicator](/docs/reference/engine/classes/ClientReplicator). |

Fired when the client successfully connects to a server. Returns a string
showing the server's IP and Port, and the client's
[ClientReplicator](/docs/reference/engine/classes/ClientReplicator).

Provide feedback

---

ConnectionFailed

Fired if the client fails to connect to the server.

NetworkClient.ConnectionFailed(

peer:[string](/docs/luau/strings), code:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| peer:[string](/docs/luau/strings)  The server's IP and port. |
| code:[number](/docs/luau/numbers)  The error code representing why the client failed to connect. |

Fired if the client fails to connect to the server.

Provide feedback

---