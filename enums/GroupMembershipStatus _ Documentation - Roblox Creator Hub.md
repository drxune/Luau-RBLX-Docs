# GroupMembershipStatus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/GroupMembershipStatus
Scraped: 2026-01-11T02:42:38.897804Z

## Inherits
- GroupService:PromptJoinAsync()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [GroupMembershipStatus](/docs/reference/engine/enums/GroupMembershipStatus)

English

Feedback

Engine Enum

GroupMembershipStatus

---

GroupMembershipStatus is an enumeration that represents the result of a
player's interaction with the [GroupService:PromptJoinAsync()](/docs/reference/engine/classes/GroupService#PromptJoinAsync) method.
It conveys the player's group membership status after the prompt.

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | The player chose not to join, cancelled the prompt, or was not eligible to join the group. |
| Joined | 1 | The player successfully joined the group during the prompt. |
| JoinRequestPending | 2 | The player submitted a request to join the group. |
| AlreadyMember | 3 | The player was already a member of the group. |