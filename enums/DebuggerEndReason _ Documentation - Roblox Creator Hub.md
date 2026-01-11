# DebuggerEndReason | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/DebuggerEndReason
Scraped: 2026-01-11T02:45:18.383413Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [DebuggerEndReason](/docs/reference/engine/enums/DebuggerEndReason)

English

Feedback

Engine Enum

DebuggerEndReason

---

Reason for the end of the debugger session.

Items

| Name | Value | Summary |
| --- | --- | --- |
| ClientRequest | 0 | Client requested connection termination. |
| Timeout | 1 | Connection timed out. |
| InvalidHost | 2 | Invalid host:port combination. |
| Disconnected | 3 | Connection was lost. |
| ServerShutdown | 4 | Server terminated the connection because it shut down. |
| ServerProtocolMismatch | 5 | Server has wrong version of protocol. |
| ConfigurationFailed | 6 | Got a failure response when trying to configure the server. |
| RpcError | 7 | An error occurred in the RPC layer. |