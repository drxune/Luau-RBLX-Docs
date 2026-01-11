# NetworkOwnership | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/NetworkOwnership
Scraped: 2026-01-11T02:44:53.830487Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [NetworkOwnership](/docs/reference/engine/enums/NetworkOwnership)

English

Feedback

Engine Enum

NetworkOwnership

---

Defines how to determine which client has ownership of a part for a server
(network).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Automatic | 0 | Network ownership is determined automatically by the server. |
| Manual | 1 | Network ownership is set manually by the developer. |
| OnContact | 2 | The first player to touch a part is given ownership of that part for the server (network). Ownership will not change if another player touches that part unless network ownership has been released by the owner. |