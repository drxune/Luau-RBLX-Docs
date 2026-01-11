# TrussPart | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TrussPart
Scraped: 2026-01-11T02:34:13.580573Z

## Tags
- Not Replicated

## Inherits
- BasePart
- TrussPart
- Part
- Style
- PVInstance
- Instance
- Object
- Decals
- Textures
- Transparency
- CanCollide
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BasePart](/docs/reference/engine/classes/BasePart)
6. /
7. [TrussPart](/docs/reference/engine/classes/TrussPart)

English

Feedback

Engine Class

![TrussPart](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TrussPart-Dark.webp)TrussPart

Similar to a [Part](/docs/reference/engine/classes/Part) but with a different visual
[Style](/docs/reference/engine/classes/TrussPart#Style) and the important distinction that default
characters are able to climb it.

---

Summary

Properties

|  |
| --- |
| [Style](#Style):[Enum.Style](/docs/reference/engine/enums/Style) |

Inherited Members

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A TrussPart is similar to a [Part](/docs/reference/engine/classes/Part) but with a different visual
[Style](/docs/reference/engine/classes/TrussPart#Style) and the important distinction that default
characters are able to climb it.

This part type has significantly more restrictive size limitations than other
parts; it must be 2\*2\*n studs where n is a multiple of 2 with a maximum
of 512.

Additionally, this part type does not support styling through the addition of
[Decals](/docs/reference/engine/classes/Decal) or [Textures](/docs/reference/engine/classes/Texture). If you wish to create a
textured and "climbable" [BasePart](/docs/reference/engine/classes/BasePart) but also utilize the climbing
behavior of TrussPart, consider setting the
[Transparency](/docs/reference/engine/classes/BasePart#Transparency) of the TrussPart to 1 to make
it invisible, set [CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) on the
[BasePart](/docs/reference/engine/classes/BasePart) to false, and then align the climbable surface of the
mesh/model with that of the TrussPart.

---

API Reference

Properties

Style

Not Replicated

Read Parallel

Sets what the truss looks like.

TrussPart.Style:[Enum.Style](/docs/reference/engine/enums/Style)

Sets what the truss looks like, from the following options:

* [Enum.Style.AlternatingSupports](/docs/reference/engine/enums/Style#AlternatingSupports)
* [Enum.Style.BridgeStyleSupports](/docs/reference/engine/enums/Style#BridgeStyleSupports)
* [Enum.Style.NoSupports](/docs/reference/engine/enums/Style#NoSupports)

Provide feedback

---