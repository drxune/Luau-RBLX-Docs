# EasingStyle | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/EasingStyle
Scraped: 2026-01-11T02:43:36.792045Z

## Inherits
- Tween
1. [Enums](/docs/reference/engine/enums)
2. /
3. [EasingStyle](/docs/reference/engine/enums/EasingStyle)

English

Feedback

Engine Enum

EasingStyle

---

These enum values are passed to [TweenInfo.new()](/docs/reference/engine/datatypes/TweenInfo) to
control the motion of a [Tween](/docs/reference/engine/classes/Tween). The following graphs reflect easing
styles for [Enum.EasingDirection.In](/docs/reference/engine/enums/EasingDirection). For graphs
reflecting [Enum.EasingDirection.Out](/docs/reference/engine/enums/EasingDirection) and
[Enum.EasingDirection.InOut](/docs/reference/engine/enums/EasingDirection), see
[UI Animations](/docs/ui/animation#style).

![Graphs of EasingStyle variations with an 'In' EasingDirection.](https://prod.docsiteassets.roblox.com/assets/engine-api/enums/EasingStyle/Easing-Styles-In.png)

Items

| Name | Value | Summary |
| --- | --- | --- |
| Linear | 0 | Moves at a constant speed. |
| Sine | 1 | Speed is determined by a sine wave for a gentle easing motion. |
| Back | 2 | Slightly overshoots the target, then backs into place. |
| Quad | 3 | Similar to Sine but with a slightly sharper curve based on quadratic interpolation. |
| Quart | 4 | Similar to Cubic but with an even sharper curve based on quartic interpolation. |
| Quint | 5 | Similar to Quart but with an even sharper curve based on quintic interpolation. |
| Bounce | 6 | Bounces backwards multiple times after reaching the target, before eventually settling. |
| Elastic | 7 | Moves as if attached to a rubber band, overshooting the target several times. |
| Exponential | 8 | The sharpest curve based on exponential interpolation. |
| Circular | 9 | Follows a circular arc, such that acceleration is more sudden and deceleration more gradual versus Quint or Exponential. |
| Cubic | 10 | Similar to Quad but with a slightly sharper curve based on cubic interpolation. |