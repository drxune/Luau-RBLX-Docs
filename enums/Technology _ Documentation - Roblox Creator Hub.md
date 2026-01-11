# Technology | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/Technology
Scraped: 2026-01-11T02:45:43.241806Z

## Inherits
- Lighting.Technology
- LightingStyle
- PrioritizeLightingQuality
- ColorGradingEffect
1. [Enums](/docs/reference/engine/enums)
2. /
3. [Technology](/docs/reference/engine/enums/Technology)

English

Feedback

Engine Enum

Technology

---

This enum represents the different lighting systems available for rendering
the 3D world. It is used by the [Lighting.Technology](/docs/reference/engine/classes/Lighting#Technology) property.

Note that [Lighting.Technology](/docs/reference/engine/classes/Lighting#Technology) has been superseded by
[LightingStyle](/docs/reference/engine/classes/Lighting#LightingStyle) which determines the artistic
intent behind lighting, and
[PrioritizeLightingQuality](/docs/reference/engine/classes/Lighting#PrioritizeLightingQuality) which
indicates whether you prefer lighting/shading quality or view distance to
scale down first.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Legacy | 0 | Deprecated |
| Voxel | 1 | Uses a 4×4×4 voxel map for light and shadow calculation. |
| Compatibility | 2 | Simulates the removed legacy technology and is now deprecated. To achieve a similar look, use Voxel Lighting and add a [ColorGradingEffect](/docs/reference/engine/classes/ColorGradingEffect) post‑processing effect set to the [Retro](/docs/reference/engine/enums/TonemapperPreset) preset. |
| ShadowMap | 3 | Features shadow mapping that produces more realistic and crisp shadows from sunlight or directional light sources. |
| Future | 4 | Features the most advanced technology for high-fidelity lighting and shadows. |
| Unified | 5 | Deprecated |