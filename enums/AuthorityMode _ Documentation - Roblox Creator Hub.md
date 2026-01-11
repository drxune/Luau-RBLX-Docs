# AuthorityMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AuthorityMode
Scraped: 2026-01-11T02:46:30.053569Z

## Inherits
- Workspace.AuthorityMode
- BasePart:SetNetworkOwner()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AuthorityMode](/docs/reference/engine/enums/AuthorityMode)

English

Feedback

Engine Enum

AuthorityMode

---

Enum used with [Workspace.AuthorityMode](/docs/reference/engine/classes/Workspace#AuthorityMode).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Server | 0 | Server authority with client side prediction and rollback enabled. |
| Automatic | 1 | Traditional distributed authority model where, for each instance, the engine decides whether the server or a client should be the authority; [BasePart:SetNetworkOwner()](/docs/reference/engine/classes/BasePart#SetNetworkOwner) can be used to influence the decision. |