# BloomEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BloomEffect
Scraped: 2026-01-11T02:40:38.793694Z

## Inherits
- PostEffect
- BloomEffect
- Instance
- Object
- Material
- Sky
- Enabled
- Lighting
- Workspace.CurrentCamera
- Threshold
- BlurEffect.Size
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PostEffect](/docs/reference/engine/classes/PostEffect)
6. /
7. [BloomEffect](/docs/reference/engine/classes/BloomEffect)

English

Feedback

Engine Class

![BloomEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BloomEffect-Dark.webp)BloomEffect

Simulates the camera viewing a very bright light.

---

Summary

Properties

|  |
| --- |
| [Intensity](#Intensity):[number](/docs/luau/numbers) |
| [Size](#Size):[number](/docs/luau/numbers) |
| [Threshold](#Threshold):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [PostEffect](/docs/reference/engine/classes/PostEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BloomEffect simulates the camera viewing a very bright light. It
causes brighter colors to glow, similar to applying the neon
[Material](/docs/reference/engine/classes/BasePart#Material) to everything, including the [Sky](/docs/reference/engine/classes/Sky).
Multiple BloomEffect objects can be applied at once and they will compose
their effects together.

Like other post-processing effects, BloomEffect will only work while
[Enabled](/docs/reference/engine/classes/PostEffect#Enabled) and when parented to [Lighting](/docs/reference/engine/classes/Lighting) or
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). Also, it may render differently depending on
your Studio settings (see the Quality Level settings in Rendering
→ Performance).

For more details on this effect and others, see
[Post-Processing Effects](/docs/environment/post-processing-effects).

---

API Reference

Properties

Intensity

Read Parallel

Determines the additive blending intensity.

BloomEffect.Intensity:[number](/docs/luau/numbers)

Intensity determines how intensely the colors that bloom (determined by
the [Threshold](/docs/reference/engine/classes/BloomEffect#Threshold)) will additively blend with
themselves. Higher values will produce brighter colors.

Provide feedback

---

Size

Read Parallel

Determines the radius of the bloom in pixels.

BloomEffect.Size:[number](/docs/luau/numbers)

Size determines the radius of the bloom effect in pixels in a similar
manner to [BlurEffect.Size](/docs/reference/engine/classes/BlurEffect#Size). Larger values create a wider bloom
effect, and a value of 0 will disable the bleed (but not the color
adjustment).

Provide feedback

---

Threshold

Read Parallel

Determines how bright a color must be before it blooms.

BloomEffect.Threshold:[number](/docs/luau/numbers)

Threshold determines how bright a color can be before it blooms. If set to
1, only pure white colors will bloom. If set to 0, all colors will bloom.

Provide feedback

---