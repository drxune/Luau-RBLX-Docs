# WrapTarget | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WrapTarget
Scraped: 2026-01-11T02:35:00.088188Z

## Tags
- Not Replicated

## Inherits
- BaseWrap
- WrapTarget
- Instance
- Object
- WrapTarget.DebugMode
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BaseWrap](/docs/reference/engine/classes/BaseWrap)
6. /
7. [WrapTarget](/docs/reference/engine/classes/WrapTarget)

English

Feedback

Engine Class

![WrapTarget](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/WrapTarget-Dark.webp)WrapTarget

The WrapTarget object defines a target. A target is the 3D body with only an
outer surface, or an Outer Cage.

---

Summary

Properties

|  |
| --- |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [DebugMode](#DebugMode):[Enum.WrapTargetDebugMode](/docs/reference/engine/enums/WrapTargetDebugMode) |
| [Stiffness](#Stiffness):[number](/docs/luau/numbers) |

Inherited Members

7 inherited from [BaseWrap](/docs/reference/engine/classes/BaseWrap)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The WrapTarget object defines a target. A target is the 3D body with only an
outer surface, or an Outer Cage.

This target, often an Avatar, is what 3D accessories (using WrapLayer) will be
applied to, allowing multiple accessories items to naturally layer over the
source target.

---

API Reference

Properties

Color

Not Replicated

Not Scriptable

Read Parallel

Sets color used for the debug rendering. See [WrapTarget.DebugMode](/docs/reference/engine/classes/WrapTarget#DebugMode).

WrapTarget.Color:[Color3](/docs/reference/engine/datatypes/Color3)

Sets color used for the debug rendering. See [WrapTarget.DebugMode](/docs/reference/engine/classes/WrapTarget#DebugMode)

Provide feedback

---

DebugMode

Not Replicated

Not Scriptable

Read Parallel

Allows switching between different debugging visualization modes for cage
meshes.

WrapTarget.DebugMode:[Enum.WrapTargetDebugMode](/docs/reference/engine/enums/WrapTargetDebugMode)

Allows switching between different debugging visualization modes for cage
meshes.

Provide feedback

---

Stiffness

Plugin Security

Read Parallel

Defines how much the body mesh can be compressed by clothing.

WrapTarget.Stiffness:[number](/docs/luau/numbers)

Defines how much the body mesh can be compressed by clothing. Super tight
clothing may lead to an intersection between the clothing mesh and body
mesh. To solve this visual artifact, the deformer can compress the body
mesh slightly to solve possible intersections.

Valid range is 0 to 1. A value of 0 will compress the body mesh as much as
necessary to ensure that the intersections are eliminated (visible body
parts might look a little bit deformed). A value of 1 will prevent the
body mesh from being compressed (may lead to visible intersections or
Z-fighting). A value of 0.9 (default) is a reasonable default that solves
most of the intersections without introducing any significant body
deformation.

Provide feedback

---