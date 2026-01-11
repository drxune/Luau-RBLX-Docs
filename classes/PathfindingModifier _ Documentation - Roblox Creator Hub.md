# PathfindingModifier | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PathfindingModifier
Scraped: 2026-01-11T02:31:01.187593Z

## Inherits
- Instance
- PathfindingModifier
- PathfindingService
- Object
- Part
- PathfindingService:CreatePath()
- collidable
- non-collidable
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PathfindingModifier](/docs/reference/engine/classes/PathfindingModifier)

English

Feedback

Engine Class

![PathfindingModifier](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/PathfindingModifier-Dark.webp)PathfindingModifier

Modifiers used to represent space that has a higher or lower cost to be
traversed when creating paths using the [PathfindingService](/docs/reference/engine/classes/PathfindingService).

---

Summary

Properties

|  |
| --- |
| [Label](#Label):[string](/docs/luau/strings) |
| [PassThrough](#PassThrough):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Pathfinding modifiers can be used to represent space that has a higher or
lower cost to be traversed. When added as a child to a [Part](/docs/reference/engine/classes/Part), it takes
that Part's volume to annotate areas of the navmesh that are inside and on top
of it.

You can include pathfinding modifiers in the
[PathfindingService:CreatePath()](/docs/reference/engine/classes/PathfindingService#CreatePath) parameters and compute smarter paths
across various materials or around defined regions.

Note that when adding a [PathfindingModifier](/docs/reference/engine/classes/PathfindingModifier) to a part, either:

* The part is [collidable](/docs/reference/engine/classes/BasePart#CanCollide) and we are interested in
  modifying pathfinding costs of paths on top of this part, which we call
  area.
* The part is [non-collidable](/docs/reference/engine/classes/BasePart#CanCollide) (and usually
  invisible in game) and we are interested in modifying pathfinding costs of
  paths inside the part, which we call volume.

---

API Reference

Properties

Label

Read Parallel

The name of the navigation area inside or on top of the [Part](/docs/reference/engine/classes/Part)
volume.

PathfindingModifier.Label:[string](/docs/luau/strings)

The name of the navigation area inside or on top of the [Part](/docs/reference/engine/classes/Part)
volume.

For a more detailed overview of [PathfindingService](/docs/reference/engine/classes/PathfindingService) and
[PathfindingModifier](/docs/reference/engine/classes/PathfindingModifier), see
[Character Pathfinding](/docs/characters/pathfinding).

Provide feedback

---

PassThrough

Read Parallel

Determines if the parts enclosed by the modifier are traversable, even if
they would normally be collided with.

PathfindingModifier.PassThrough:[boolean](/docs/luau/booleans)

Determines if the parts enclosed by the modifier are traversable, even if
they would normally be collided with. See
[Character Pathfinding](/docs/characters/pathfinding) for details.

Provide feedback

---