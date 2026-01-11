# CloseReason | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/CloseReason
Scraped: 2026-01-11T02:46:36.947688Z

## Inherits
- BindToClose()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [CloseReason](/docs/reference/engine/enums/CloseReason)

English

Feedback

Engine Enum

CloseReason

---

Specifies the reason for the experience server shutdown. This enum value is
the first parameter passed to functions bound by
[BindToClose()](/docs/reference/engine/classes/DataModel#BindToClose).

The DeveloperShutdown value must always be passed to functions bound by
[BindToClose()](/docs/reference/engine/classes/DataModel#BindToClose) when they're called in Studio.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Unknown | 0 | The server shut down for an unknown reason. |
| RobloxMaintenance | 1 | The server shut down for maintenance. |
| DeveloperShutdown | 2 | The experience developer has shut down the server, or functions bound by [BindToClose()](/docs/reference/engine/classes/DataModel#BindToClose) have been called inside Studio. |
| DeveloperUpdate | 3 | The experience developer has migrated the server to a new place version. |
| ServerEmpty | 4 | The last player has left and the experience is empty. |
| OutOfMemory | 5 | The experience has hit the memory limit for the game server. |