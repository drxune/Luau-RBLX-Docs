# PoseEasingDirection | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PoseEasingDirection
Scraped: 2026-01-11T02:42:54.535302Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PoseEasingDirection](/docs/reference/engine/enums/PoseEasingDirection)

English

Feedback

Engine Enum

PoseEasingDirection

---

When a Pose has an EasingStyle which is not symmetric, the EasingDirection
determines if the curve is applied from previous keyframe to next, next
keyframe to previous, or in both directions by using two copies of the curve
back to back. For the symmetric Linear and Constant EasingStyles, this
property has no effect. For legacy compatibility reasons, the use of In and
Out are backwards from how these terms are used by most other animation tools
and by TweenService.

Items

| Name | Value | Summary |
| --- | --- | --- |
| In | 0 | The EasingStyle curve is reversed, with the easing becoming linear as it approaches the next keyframe. |
| Out | 1 | EasingStyle curves are applied in the forward direction, from the current keyframe to the next. |
| InOut | 2 | Two easing curves are applied back-to-back with the linear ends of the curves meeting in the middle. |