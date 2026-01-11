# DragDetectorPermissionPolicy | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/DragDetectorPermissionPolicy
Scraped: 2026-01-11T02:45:04.413519Z

## Inherits
- DragDetector
- PermissionPolicy
- DragDetector:SetPermissionPolicyFunction()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [DragDetectorPermissionPolicy](/docs/reference/engine/enums/DragDetectorPermissionPolicy)

English

Feedback

Engine Enum

DragDetectorPermissionPolicy

---

Used to control the permission level for which players can interact with a
[DragDetector](/docs/reference/engine/classes/DragDetector) through its
[PermissionPolicy](/docs/reference/engine/classes/DragDetector#PermissionPolicy) property.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Nobody | 0 | No players can interact with the [DragDetector](/docs/reference/engine/classes/DragDetector). |
| Everybody | 1 | All players can interact with the [DragDetector](/docs/reference/engine/classes/DragDetector). |
| Scriptable | 2 | Invokes the function registered via [DragDetector:SetPermissionPolicyFunction()](/docs/reference/engine/classes/DragDetector#SetPermissionPolicyFunction), enabling/disabling the detector based on whether the function returns true or false. |