# SunRaysEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SunRaysEffect
Scraped: 2026-01-11T02:28:00.738913Z

## Inherits
- PostEffect
- SunRaysEffect
- Instance
- Object
- Workspace.CurrentCamera
- Enabled
- Lighting
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PostEffect](/docs/reference/engine/classes/PostEffect)
6. /
7. [SunRaysEffect](/docs/reference/engine/classes/SunRaysEffect)

English

Feedback

Engine Class

![SunRaysEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SunRaysEffect-Dark.webp)SunRaysEffect

Renders dynamic rays from the sun.

---

Summary

Properties

|  |
| --- |
| [Intensity](#Intensity):[number](/docs/luau/numbers) |
| [Spread](#Spread):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [PostEffect](/docs/reference/engine/classes/PostEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The SunRaysEffect renders a halo of light around sun. The halo is
shaped/blocked by world objects between the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera)
and the sun.

Like other post-processing effects, SunRaysEffect will only work while
[Enabled](/docs/reference/engine/classes/PostEffect#Enabled) and when parented to [Lighting](/docs/reference/engine/classes/Lighting) or
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). Also, it may not render on low-end devices,
and it may render differently depending on your Studio settings (see the
Quality Level settings in Rendering → Performance).

For more details on this effect and others, see
[Post-Processing Effects](/docs/environment/post-processing-effects).

---

API Reference

Properties

Intensity

Read Parallel

Determines the opacity of the sun rays.

SunRaysEffect.Intensity:[number](/docs/luau/numbers)

Intensity determines the opacity of the sun rays. Values closer to 0 are
less visible, while values closer to 1 become more visible.

Provide feedback

---

Spread

Read Parallel

Determines how wide the sun rays will spread out.

SunRaysEffect.Spread:[number](/docs/luau/numbers)

Spread determines how wide the sun rays will spread across the sky. Its
value should be set between 0 and 1 as values outside that range have
undefined behavior.

Provide feedback

---