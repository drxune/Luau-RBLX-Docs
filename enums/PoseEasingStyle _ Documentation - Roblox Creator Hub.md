# PoseEasingStyle | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PoseEasingStyle
Scraped: 2026-01-11T02:44:45.093334Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PoseEasingStyle](/docs/reference/engine/enums/PoseEasingStyle)

English

Feedback

Engine Enum

PoseEasingStyle

---

Items

| Name | Value | Summary |
| --- | --- | --- |
| Linear | 0 | Poses interpolate linearly between key frames. |
| Constant | 1 | Poses do not interpolate but snap to the key frame indicated by the [Enum.PoseEasingDirection](/docs/reference/engine/enums/PoseEasingDirection). |
| Elastic | 2 | Pose interpolation will overshoot like it is elastic. |
| Cubic | 3 | Deprecated - Use [Enum.PoseEasingStyle.CubicV2](/docs/reference/engine/enums/PoseEasingStyle#CubicV2). Pose interpolation is a cubic curve between keyframes based on the [Enum.PoseEasingDirection](/docs/reference/engine/enums/PoseEasingDirection). |
| Bounce | 4 | Pose interpolation produces a bounce like effect between key frames. |
| CubicV2 | 5 | Pose interpolation is a cubic curve between keyframes based on [Enum.PoseEasingDirection](/docs/reference/engine/enums/PoseEasingDirection). |