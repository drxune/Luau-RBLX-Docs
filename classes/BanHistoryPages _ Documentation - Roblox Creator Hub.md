# BanHistoryPages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BanHistoryPages
Scraped: 2026-01-11T02:31:20.249457Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Pages
- BanHistoryPages
- Players:GetBanHistoryAsync()
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Pages](/docs/reference/engine/classes/Pages)
6. /
7. [BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages)

English

Feedback

Engine Class

BanHistoryPages

Returned by [Players:GetBanHistoryAsync()](/docs/reference/engine/classes/Players#GetBanHistoryAsync) to view the entire ban and
unban history of any UserId.

Not Creatable

Not Replicated

---

Summary

Inherited Members

3 inherited from [Pages](/docs/reference/engine/classes/Pages)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages) is returned by [Players:GetBanHistoryAsync()](/docs/reference/engine/classes/Players#GetBanHistoryAsync).
This instance allows an experience to view the entire ban and unban history of
any player within the experience's universe.

The items within [BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages) are tables with the following fields:

| Name | Type | Description |
| --- | --- | --- |
| DisplayReason | string | The DisplayReason that was shown to the user |
| PrivateReason | string | The PrivateReason that was sent with this ban. |
| StartTime | string | The time that this ban was applied in ISO 8601 format. |
| Duration | number | The length of the ban in seconds. If it is a permanent ban, it will be -1. |
| Ban | boolean | If the action was a ban, it will be true. If the action was an unban, it will be false. |
| PlaceId | number | The place in which a ban or unban was explicitly updated. This field is -1 if the action was applied on the universe level. |