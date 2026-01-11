# PostEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PostEffect
Scraped: 2026-01-11T02:30:11.759271Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- PostEffect
- BloomEffect
- BlurEffect
- ColorCorrectionEffect
- ColorGradingEffect
- DepthOfFieldEffect
- GuiObjects
- Lighting
- Workspace.CurrentCamera
- QualityLevel
- EditQualityLevel
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PostEffect](/docs/reference/engine/classes/PostEffect)

English

Feedback

Engine Class

PostEffect

Abstract base class for post-processing effects.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[BloomEffect](/docs/reference/engine/classes/BloomEffect), [BlurEffect](/docs/reference/engine/classes/BlurEffect), [ColorCorrectionEffect](/docs/reference/engine/classes/ColorCorrectionEffect), [ColorGradingEffect](/docs/reference/engine/classes/ColorGradingEffect), [DepthOfFieldEffect](/docs/reference/engine/classes/DepthOfFieldEffect), Show more...

PostEffect is an abstract base class for post-processing effects, such as
[BloomEffect](/docs/reference/engine/classes/BloomEffect) and [ColorCorrectionEffect](/docs/reference/engine/classes/ColorCorrectionEffect). They change how the
world looks after it has been rendered. They do not affect
[GuiObjects](/docs/reference/engine/classes/GuiObject). Objects of this kind should be parented to the
[Lighting](/docs/reference/engine/classes/Lighting) or the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) in order to work.

It should also be noted that some post-processing effects will work
differently or not at all when Roblox is set to a low
[QualityLevel](/docs/reference/engine/classes/RenderSettings#QualityLevel) (or
[EditQualityLevel](/docs/reference/engine/classes/RenderSettings#EditQualityLevel) in Studio). On some
low-end devices, faster rendering algorithms may be used. By default, these
quality settings are set to Automatic, so if you aren't seeing post-processing
effects you should check Roblox's settings under the "Rendering" section. It
may be necessary to override the automatic behavior temporarily in order to
preview post-processing effects.

---

API Reference

Properties

Enabled

Read Parallel

Toggles whether or not the PostEffect is enabled.

PostEffect.Enabled:[boolean](/docs/luau/booleans)

Toggles whether or not the PostEffect is enabled.

Provide feedback

---