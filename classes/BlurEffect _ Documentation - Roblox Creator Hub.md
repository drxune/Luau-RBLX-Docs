# BlurEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BlurEffect
Scraped: 2026-01-11T02:39:10.238175Z

## Inherits
- PostEffect
- BlurEffect
- Instance
- Object
- BlurEffect.Size
- Size
- Enabled
- Lighting
- Workspace.CurrentCamera
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PostEffect](/docs/reference/engine/classes/PostEffect)
6. /
7. [BlurEffect](/docs/reference/engine/classes/BlurEffect)

English

Feedback

Engine Class

![BlurEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BlurEffect-Dark.webp)BlurEffect

Applies a blur to the entire game world.

---

Summary

Properties

|  |
| --- |
| [Size](#Size):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [PostEffect](/docs/reference/engine/classes/PostEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BlurEffect applies a Gaussian blur to the entire rendered game world.
The strength of the blur is controlled by the [BlurEffect.Size](/docs/reference/engine/classes/BlurEffect#Size). Only
one BlurEffect can be applied at once (the instance with the greatest
[Size](/docs/reference/engine/classes/BlurEffect#Size) takes priority).

Like other post-processing effects, BlurEffect will only work while
[Enabled](/docs/reference/engine/classes/PostEffect#Enabled) and when parented to [Lighting](/docs/reference/engine/classes/Lighting) or
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). Also, it may render differently on low-end
devices and/or depending on your Studio settings (see the Quality Level
settings in Rendering → Performance).

For more details on this effect and others, see
[Post-Processing Effects](/docs/environment/post-processing-effects).

---

API Reference

Properties

Size

Read Parallel

Determines the blur radius.

BlurEffect.Size:[number](/docs/luau/numbers)

Size controls the blur radius, measured in pixels. The larger the size,
the blurrier the screen will become.

Provide feedback

---