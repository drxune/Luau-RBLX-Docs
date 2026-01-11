# DebuggerStatus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/DebuggerStatus
Scraped: 2026-01-11T02:43:16.957604Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [DebuggerStatus](/docs/reference/engine/enums/DebuggerStatus)

English

Feedback

Engine Enum

DebuggerStatus

---

Result of a debugger request.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Success | 0 | Request has completed successfully. |
| Timeout | 1 | Timed out while waiting for response. |
| ConnectionLost | 2 | Connection to the debugger was lost. |
| InvalidResponse | 3 | Failed to parse response. |
| InternalError | 4 | Exception encountered while processing response. |
| InvalidState | 5 | The request was not appropriate for the current debugger state. |
| RpcError | 6 | Response was an error. |
| InvalidArgument | 7 | One of the request arguments was invalid. |
| ConnectionClosed | 8 | Connection closed while waiting for response. |