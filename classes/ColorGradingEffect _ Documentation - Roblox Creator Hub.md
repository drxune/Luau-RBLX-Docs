# ColorGradingEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ColorGradingEffect
Scraped: 2026-01-11T02:38:02.032767Z

## Inherits
- PostEffect
- ColorGradingEffect
- Instance
- Object
- Lighting
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PostEffect](/docs/reference/engine/classes/PostEffect)
6. /
7. [ColorGradingEffect](/docs/reference/engine/classes/ColorGradingEffect)

English

Feedback

Engine Class

ColorGradingEffect

Modifies how color values calculated by the renderer should be converted to
the screen's color range.

---

Summary

Properties

|  |
| --- |
| [TonemapperPreset](#TonemapperPreset):[Enum.TonemapperPreset](/docs/reference/engine/enums/TonemapperPreset) |

Inherited Members

1 inherited from [PostEffect](/docs/reference/engine/classes/PostEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The ColorGradingEffect effect modifies how color values calculated by the
renderer should be converted to the screen's color range, impacting the mood
and appearance of your place.

ColorGradingEffect is expected to be parented to [Lighting](/docs/reference/engine/classes/Lighting) and will
be ignored if parented elsewhere. Multiple instances cannot be combined and
only the most recently parented instance to [Lighting](/docs/reference/engine/classes/Lighting) will be applied.

For more details on this effect and others, see
[Post-Processing Effects](/docs/environment/post-processing-effects).

---

API Reference

Properties

TonemapperPreset

Read Parallel

Specifies which tone mapper preset to use.

ColorGradingEffect.TonemapperPreset:[Enum.TonemapperPreset](/docs/reference/engine/enums/TonemapperPreset)

Specifies which [Enum.TonemapperPreset](/docs/reference/engine/enums/TonemapperPreset) to use.
[Enum.TonemapperPreset.Retro](/docs/reference/engine/enums/TonemapperPreset#Retro) is meant to imitate the look of the pre‑2019
Roblox lighting system.

Provide feedback

---