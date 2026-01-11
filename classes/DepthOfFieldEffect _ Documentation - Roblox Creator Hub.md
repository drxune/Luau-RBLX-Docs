# DepthOfFieldEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DepthOfFieldEffect
Scraped: 2026-01-11T02:30:20.678163Z

## Inherits
- PostEffect
- DepthOfFieldEffect
- Instance
- Object
- Enabled
- Lighting
- Workspace.CurrentCamera
- FocusDistance
- InFocusRadius
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PostEffect](/docs/reference/engine/classes/PostEffect)
6. /
7. [DepthOfFieldEffect](/docs/reference/engine/classes/DepthOfFieldEffect)

English

Feedback

Engine Class

![DepthOfFieldEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/DepthOfFieldEffect-Dark.webp)DepthOfFieldEffect

Simulates a camera lens by blurring parts of a scene not in focus.

---

Summary

Properties

|  |
| --- |
| [FarIntensity](#FarIntensity):[number](/docs/luau/numbers) |
| [FocusDistance](#FocusDistance):[number](/docs/luau/numbers) |
| [InFocusRadius](#InFocusRadius):[number](/docs/luau/numbers) |
| [NearIntensity](#NearIntensity):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [PostEffect](/docs/reference/engine/classes/PostEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The DepthOfFieldEffect simulates a camera lens by blurring parts of a
scene not in focus. Distant objects can be blurred or this effect can be used
to focus on specific parts of a scene, like an item in an in-game shop.

Like other post-processing effects, DepthOfFieldEffect will only work
while [Enabled](/docs/reference/engine/classes/PostEffect#Enabled) and when parented to [Lighting](/docs/reference/engine/classes/Lighting)
or [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). Also, it may render differently on low-end
devices or depending on your Studio settings (see the Quality Level
settings in Rendering → Performance).

For more details on this effect and others, see
[Post-Processing Effects](/docs/environment/post-processing-effects).

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/DepthOfFieldEffect/Depth-Of-Field-Diagram.svg)

---

API Reference

Properties

FarIntensity

Read Parallel

Intensity of the far field blur.

DepthOfFieldEffect.FarIntensity:[number](/docs/luau/numbers)

Intensity of the far field blur, moving out in distance from the
[FocusDistance](/docs/reference/engine/classes/DepthOfFieldEffect#FocusDistance) point plus
[InFocusRadius](/docs/reference/engine/classes/DepthOfFieldEffect#InFocusRadius) value.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/DepthOfFieldEffect/Depth-Of-Field-Diagram.svg)

Provide feedback

---

FocusDistance

Read Parallel

Distance away from the camera where objects are in focus.

DepthOfFieldEffect.FocusDistance:[number](/docs/luau/numbers)

Controls the distance away from the camera (in studs) where objects are in
focus.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/DepthOfFieldEffect/Depth-Of-Field-Diagram.svg)

Provide feedback

---

InFocusRadius

Read Parallel

Controls the distance away from the
[FocusDistance](/docs/reference/engine/classes/DepthOfFieldEffect#FocusDistance) where no blur is
applied.

DepthOfFieldEffect.InFocusRadius:[number](/docs/luau/numbers)

Controls the distance away from the
[FocusDistance](/docs/reference/engine/classes/DepthOfFieldEffect#FocusDistance) (on both sides)
where no blur is applied. Measured in studs.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/DepthOfFieldEffect/Depth-Of-Field-Diagram.svg)

Provide feedback

---

NearIntensity

Read Parallel

Intensity of the near field blur.

DepthOfFieldEffect.NearIntensity:[number](/docs/luau/numbers)

Intensity of the near field blur, between the camera and the
[FocusDistance](/docs/reference/engine/classes/DepthOfFieldEffect#FocusDistance) point minus
[InFocusRadius](/docs/reference/engine/classes/DepthOfFieldEffect#InFocusRadius) value.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/DepthOfFieldEffect/Depth-Of-Field-Diagram.svg)

Provide feedback

---