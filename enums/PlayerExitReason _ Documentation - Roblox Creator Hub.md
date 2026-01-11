# PlayerExitReason | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PlayerExitReason
Scraped: 2026-01-11T02:44:22.754717Z

## Inherits
- Players.PlayerRemoving
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PlayerExitReason](/docs/reference/engine/enums/PlayerExitReason)

English

Feedback

Engine Enum

PlayerExitReason

---

Second argument in [Players.PlayerRemoving](/docs/reference/engine/classes/Players#PlayerRemoving). Helps identify whether a
kick was caused by the Roblox platform or the Creator.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Unknown | 0 | Catch-all for all other disconnect reasons. |
| PlatformKick | 1 | User was kicked by Roblox systems, such as being blocked while in a Private Server. |
| CreatorKick | 2 | Creator called Player:Kick() |