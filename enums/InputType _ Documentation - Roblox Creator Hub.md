# InputType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/InputType
Scraped: 2026-01-11T02:44:45.865993Z

## Inherits
- Part
- Part.BackSurfaceInput
- Part.BottomSurfaceInput
- Part.FrontSurfaceInput
- Part.LeftSurfaceInput
- Part.RightSurfaceInput
- Part.TopSurfaceInput
- BasePart
1. [Enums](/docs/reference/engine/enums)
2. /
3. [InputType](/docs/reference/engine/enums/InputType)

English

Feedback

Engine Enum

InputType

Deprecated

This enum is deprecated as it is used by deprecated methods. It should not be
used in new work.

---

The InputType Enum controls the SurfaceInputs of [Part](/docs/reference/engine/classes/Part). Several
parameters here are left-overs from 2005, before Roblox was a multiplayer
game, and are used by [Part.BackSurfaceInput](/docs/reference/engine/classes/Part#BackSurfaceInput),
[Part.BottomSurfaceInput](/docs/reference/engine/classes/Part#BottomSurfaceInput), [Part.FrontSurfaceInput](/docs/reference/engine/classes/Part#FrontSurfaceInput),
[Part.LeftSurfaceInput](/docs/reference/engine/classes/Part#LeftSurfaceInput), [Part.RightSurfaceInput](/docs/reference/engine/classes/Part#RightSurfaceInput),
[Part.TopSurfaceInput](/docs/reference/engine/classes/Part#TopSurfaceInput).

Items

| Name | Value | Summary |
| --- | --- | --- |
| NoInput | 0 | Behaves like a weld and does nothing. |
| Constant | 12 | Rotate at a constant velocity of [BasePart](/docs/reference/engine/classes/BasePart) ParamB. |
| Sin | 13 | Rotate at a velocity of: ParamA \* math.sin(workspace.DistributedGameTime \* ParamB), where [BasePart](/docs/reference/engine/classes/BasePart) ParamA determines the maximum speed at which the part spins, and [BasePart](/docs/reference/engine/classes/BasePart) ParamB determines how frequently it changes direction. |