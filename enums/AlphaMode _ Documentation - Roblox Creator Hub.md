# AlphaMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AlphaMode
Scraped: 2026-01-11T02:44:38.878065Z

## Inherits
- SurfaceAppearance.AlphaMode
- SurfaceAppearance.ColorMap
- SurfaceAppearance
- ColorMap
- SurfaceAppearance.Color
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AlphaMode](/docs/reference/engine/enums/AlphaMode)

English

Feedback

Engine Enum

AlphaMode

---

Used by [SurfaceAppearance.AlphaMode](/docs/reference/engine/classes/SurfaceAppearance#AlphaMode) to determine how the alpha channel
of the [SurfaceAppearance.ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) of a [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) is
used.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Overlay | 0 | Overlays the [ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) on top of the underlying part color based on the map's alpha channel. |
| Transparency | 1 | Uses the [ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) alpha channel to control the transparency of the surface. |
| TintMask | 2 | Uses the [ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) alpha channel to control the amount of [SurfaceAppearance.Color](/docs/reference/engine/classes/SurfaceAppearance#Color) tinting. |