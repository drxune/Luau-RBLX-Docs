# BuoyancySensor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BuoyancySensor
Scraped: 2026-01-11T02:27:26.511950Z

## Inherits
- SensorBase
- BuoyancySensor
- BasePart
- Terrain
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SensorBase](/docs/reference/engine/classes/SensorBase)
6. /
7. [BuoyancySensor](/docs/reference/engine/classes/BuoyancySensor)

English

Feedback

Engine Class

BuoyancySensor

A [SensorBase](/docs/reference/engine/classes/SensorBase) that outputs data about how its [BasePart](/docs/reference/engine/classes/BasePart) is
interacting with [Terrain](/docs/reference/engine/classes/Terrain) water.

---

Summary

Properties

|  |
| --- |
| [FullySubmerged](#FullySubmerged):[boolean](/docs/luau/booleans) |
| [TouchingSurface](#TouchingSurface):[boolean](/docs/luau/booleans) |

Inherited Members

3 inherited from [SensorBase](/docs/reference/engine/classes/SensorBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [SensorBase](/docs/reference/engine/classes/SensorBase) that outputs data about how its [BasePart](/docs/reference/engine/classes/BasePart) is
interacting with [Terrain](/docs/reference/engine/classes/Terrain) water, allowing you to determine if the part
is or is not in water.

---

API Reference

Properties

FullySubmerged

Read Parallel

True when the entirety of the [BasePart](/docs/reference/engine/classes/BasePart) is submerged in
[Terrain](/docs/reference/engine/classes/Terrain) water with at least one voxel of water above it.

BuoyancySensor.FullySubmerged:[boolean](/docs/luau/booleans)

This property is true when the entirety of the [BasePart](/docs/reference/engine/classes/BasePart) is
submerged in [Terrain](/docs/reference/engine/classes/Terrain) water with at least one voxel of water above
it.

Provide feedback

---

TouchingSurface

Read Parallel

True when any position on the [BasePart](/docs/reference/engine/classes/BasePart) is touching [Terrain](/docs/reference/engine/classes/Terrain)
water.

BuoyancySensor.TouchingSurface:[boolean](/docs/luau/booleans)

This property is true when any position on the [BasePart](/docs/reference/engine/classes/BasePart) is
touching [Terrain](/docs/reference/engine/classes/Terrain) water. The detection measurements are not exact
and may use the bounding box of the part instead of its exact geometry.

Provide feedback

---