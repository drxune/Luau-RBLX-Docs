# WebStreamClientType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/WebStreamClientType
Scraped: 2026-01-11T02:46:11.229311Z

## Inherits
- WebStreamClient
1. [Enums](/docs/reference/engine/enums)
2. /
3. [WebStreamClientType](/docs/reference/engine/enums/WebStreamClientType)

English

Feedback

Engine Enum

WebStreamClientType

---

Specifies what type of streaming to use when creating a
[WebStreamClient](/docs/reference/engine/classes/WebStreamClient).

Items

| Name | Value | Summary |
| --- | --- | --- |
| SSE | 0 | Traditional Server-Sent Events (SSE) client. Requires text/event-stream to be returned in the Content-Type header. Messages in the stream will follow the [event stream format](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events#event_stream_format). |
| RawStream | 1 | General purpose HTTP streaming client. It can connect to any server that provides streaming data transfer (e.g. [chunked encoding](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Transfer-Encoding)). It provides no guarantees about the stream format. |
| WebSocket | 2 | [WebSocket](https://en.wikipedia.org/wiki/WebSocket) client that provides a bidirectional communication channel over a TCP connection. |