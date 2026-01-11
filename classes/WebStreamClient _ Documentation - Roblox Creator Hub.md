# WebStreamClient | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WebStreamClient
Scraped: 2026-01-11T02:28:24.093647Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- WebStreamClient
- WebStreamClient.Closed
- WebStreamClient:Close()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [WebStreamClient](/docs/reference/engine/classes/WebStreamClient)

English

Feedback

Engine Class

WebStreamClient

Maintains a streaming connection.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [ConnectionState](#ConnectionState):[Enum.WebStreamClientState](/docs/reference/engine/enums/WebStreamClientState) |

Methods

|  |
| --- |
| [Close](#Close)():() |
| [Send](#Send)(data: [string](/docs/luau/strings)):() |

Events

|  |
| --- |
| [Closed](#Closed)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Error](#Error)(responseStatusCode: [number](/docs/luau/numbers),errorMessage: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MessageReceived](#MessageReceived)(message: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Opened](#Opened)(responseStatusCode: [number](/docs/luau/numbers),headers: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

6 inherited from [Object](/docs/reference/engine/classes/Object)

Maintains a streaming connection. To process stream events as they arrive,
connect callback functions to each event using
[RBXScriptSignal:Connect()](/docs/reference/engine/datatypes/RBXScriptSignal#Connect).

---

API Reference

Properties

ConnectionState

Read Only

Not Replicated

Read Parallel

The current [Enum.WebStreamClientState](/docs/reference/engine/enums/WebStreamClientState) of the client.

WebStreamClient.ConnectionState:[Enum.WebStreamClientState](/docs/reference/engine/enums/WebStreamClientState)

The current [Enum.WebStreamClientState](/docs/reference/engine/enums/WebStreamClientState) of the client.

Provide feedback

---

Methods

Close

Closes the client, aborting the ongoing request.

WebStreamClient:Close():()

Returns

()

Closes the client, aborting the ongoing request. If successful, fires the
[WebStreamClient.Closed](/docs/reference/engine/classes/WebStreamClient#Closed) event.

Provide feedback

---

Send

Enqueues data to be transmitted to the server over the streaming
connection.

WebStreamClient:Send(data:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| data:[string](/docs/luau/strings)  Text string to send to the server. |

Returns

()

Enqueues data to be transmitted to the server over the connection. Only
works on clients created with [Enum.WebStreamClientType.WebSocket](/docs/reference/engine/enums/WebStreamClientType#WebSocket). For
other client types it does nothing.

Provide feedback

---

Events

Closed

WebStreamClient.Closed():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the server closes the connection succesfully or the user calls
[WebStreamClient:Close()](/docs/reference/engine/classes/WebStreamClient#Close)

Provide feedback

---

Error

Fires if an error is received while establishing the connection or during
the connection lifetime.

WebStreamClient.Error(

responseStatusCode:[number](/docs/luau/numbers), errorMessage:[string](/docs/luau/strings)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| responseStatusCode:[number](/docs/luau/numbers)  The standard HTTP error status code (e.g., 404, 500). |
| errorMessage:[string](/docs/luau/strings)  A descriptive message containing details about the error. |

Fires if an error is received while establishing the connection or during
the connection lifetime.

Provide feedback

---

MessageReceived

Fires each time a message is received from the server.

WebStreamClient.MessageReceived(message:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings)  The message data payload received from the server stream. |

Fires each time a message is received from the server. The format differs
based on the [Enum.WebStreamClientType](/docs/reference/engine/enums/WebStreamClientType).

Provide feedback

---

Opened

Fires when the a connection is successfully established between the client
and server, allowing for events to begin streaming.

WebStreamClient.Opened(

responseStatusCode:[number](/docs/luau/numbers), headers:[string](/docs/luau/strings)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| responseStatusCode:[number](/docs/luau/numbers)  The standard HTTP success status code (e.g., 200). |
| headers:[string](/docs/luau/strings)  The raw HTTP response headers from the server. |

Fires when the a connection is successfully established between the client
and server, allowing for events to begin streaming. Provides any response
headers in raw format, which can be used for validation.

Provide feedback

---