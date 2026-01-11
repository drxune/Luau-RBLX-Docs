# PermissionLevelShown | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PermissionLevelShown
Scraped: 2026-01-11T02:44:14.894803Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PermissionLevelShown](/docs/reference/engine/enums/PermissionLevelShown)

English

Feedback

Engine Enum

PermissionLevelShown

---

Used to set the highest permission level that APIs have to have in order to be
shown in the Object Browser.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Game | 0 | Member must have no security permissions in order to be shown. |
| RobloxGame | 1 | Member must have security permissions less than or equal to RobloxPlaceSecurity to be shown. |
| RobloxScript | 2 | Member must have security permissions less than or equal to RobloxScriptSecurity to be shown. |
| Studio | 3 | Member must have security permissions less than or equal to LocalUserSecurity to be shown. |
| Roblox | 4 | Member is shown no matter what security it has. |