# WebStreamClientState | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/WebStreamClientState
Scraped: 2026-01-11T02:44:37.883626Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [WebStreamClientState](/docs/reference/engine/enums/WebStreamClientState)

English

Feedback

Engine Enum

WebStreamClientState

---

WebStreamClientState indicates the current state of a WebStreamClient object.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Connecting | 0 | The client has sent a request to connect with the server and is waiting for a response. |
| Open | 1 | The client is connected to the server, allowing for data to be streamed between the server and client. |
| Error | 2 | An unrecoverable error has occured while setting up the connection orduring the connection lifetime, cutting off the stream. |
| Closed | 3 | The connection has run to completion without issues, either closed naturally by the server or manually by the user. |