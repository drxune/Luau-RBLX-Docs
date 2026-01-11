# ColorCorrectionEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ColorCorrectionEffect
Scraped: 2026-01-11T02:30:39.891085Z

## Inherits
- PostEffect
- ColorCorrectionEffect
- Instance
- Object
- Saturation
- TintColor
- Brightness
- Contrast
- Enabled
- Lighting
- Workspace.CurrentCamera
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PostEffect](/docs/reference/engine/classes/PostEffect)
6. /
7. [ColorCorrectionEffect](/docs/reference/engine/classes/ColorCorrectionEffect)

English

Feedback

Engine Class

ColorCorrectionEffect

Adjusts color-related properties of the rendered world like saturation, tint,
brightness, and contrast.

---

Summary

Properties

|  |
| --- |
| [Brightness](#Brightness):[number](/docs/luau/numbers) |
| [Contrast](#Contrast):[number](/docs/luau/numbers) |
| [Saturation](#Saturation):[number](/docs/luau/numbers) |
| [TintColor](#TintColor):[Color3](/docs/reference/engine/datatypes/Color3) |

Inherited Members

1 inherited from [PostEffect](/docs/reference/engine/classes/PostEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[ColorCorrectionEffect](/docs/reference/engine/classes/ColorCorrectionEffect) can be used to adjust several color-related
properties at once, including
[Saturation](/docs/reference/engine/classes/ColorCorrectionEffect#Saturation),
[TintColor](/docs/reference/engine/classes/ColorCorrectionEffect#TintColor),
[Brightness](/docs/reference/engine/classes/ColorCorrectionEffect#Brightness) and
[Contrast](/docs/reference/engine/classes/ColorCorrectionEffect#Contrast). It's useful for fine-tuning
the visual aesthetic of a world or communicating status effects to the player.
Multiple [ColorCorrectionEffect](/docs/reference/engine/classes/ColorCorrectionEffect) objects can be applied at the same time
and they will compose their effects together.

Like other
[post-processing effects](/docs/environment/post-processing-effects),
[ColorCorrectionEffect](/docs/reference/engine/classes/ColorCorrectionEffect) will only work while
[Enabled](/docs/reference/engine/classes/PostEffect#Enabled) and when parented to [Lighting](/docs/reference/engine/classes/Lighting) or
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). Also, it may render differently depending on
your Studio settings (see Editor Quality Level in
Rendering).

---

API Reference

Properties

Brightness

Read Parallel

Determines by how much the brightness of pixel colors will be shifted.

ColorCorrectionEffect.Brightness:[number](/docs/luau/numbers)

This property determines by how much the colors of pixels will be shifted.
A value of -1 will cause all pixels to be completely black while a value
of 1 will cause them to be white.

Provide feedback

---

Contrast

Read Parallel

Determines the change in separation between the dark and light colors.

ColorCorrectionEffect.Contrast:[number](/docs/luau/numbers)

This property determines the separation between the dark and light colors.
Values less than 0 have reduced contrast while values greater than 0
have increased contrast.

Provide feedback

---

Saturation

Read Parallel

Determines the change in intensity of colors.

ColorCorrectionEffect.Saturation:[number](/docs/luau/numbers)

This property determines the change in intensity of pixel colors. Values
above 1 will cause colors to be more vivid while values below 0 will
make colors more dull, eventually reaching full desaturation at -1.

Provide feedback

---

TintColor

Read Parallel

Determines by how much the RGB channels of pixels are scaled.

ColorCorrectionEffect.TintColor:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines by what factors the RGB channels of pixel colors
are scaled. The effect is multiplicative, so changing this to [255, 0, 0] (red) would cause the green and blue
channels to be multiplied by 0.

Provide feedback

---