# WorldModel | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WorldModel
Scraped: 2026-01-11T02:41:21.980944Z

## Inherits
- WorldRoot
- WorldModel
- ViewportFrame
- Model
- PVInstance
- Instance
- Object
- BaseParts
- Humanoid
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [WorldRoot](/docs/reference/engine/classes/WorldRoot)
6. /
7. [WorldModel](/docs/reference/engine/classes/WorldModel)

English

Feedback

Engine Class

![WorldModel](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/WorldModel-Dark.webp)WorldModel

Extends limited physics for its children on to a parent [ViewportFrame](/docs/reference/engine/classes/ViewportFrame).

---

Summary

Inherited Members

21 inherited from [WorldRoot](/docs/reference/engine/classes/WorldRoot)

26 inherited from [Model](/docs/reference/engine/classes/Model)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

When parented to a [ViewportFrame](/docs/reference/engine/classes/ViewportFrame), WorldModel extends limited physics
for its children on to that [ViewportFrame](/docs/reference/engine/classes/ViewportFrame). For example,
[BaseParts](/docs/reference/engine/classes/BasePart) that are parented to the WorldModel can be
animated and spatially queried (for example by raycasts) but those parts are
not simulated. Furthermore, you can put [Humanoid](/docs/reference/engine/classes/Humanoid) characters in the
WorldModel and their joints will be set up correctly for animation.

To avoid possible performance issues, make sure to only create WorldModels
when you want to show them and to delete WorldModels that are currently not
in use.