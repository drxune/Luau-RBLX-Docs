# CollisionFidelity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/CollisionFidelity
Scraped: 2026-01-11T02:43:50.826845Z

## Inherits
- MeshPart
- PartOperation
1. [Enums](/docs/reference/engine/enums)
2. /
3. [CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity)

English

Feedback

Engine Enum

CollisionFidelity

---

Determines behavior of the collision hitbox for [MeshPart](/docs/reference/engine/classes/MeshPart) and
[PartOperation](/docs/reference/engine/classes/PartOperation) instances. See
[here](/docs/workspace/collisions#collision-fidelity) for a visual
representation of the various options.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Collision model uses a voxel-based convex-hull decomposition that is relatively fast but may not be highly accurate, especially for holes, doorways, and cavities in general. |
| Hull | 1 | Collision model uses the convex hull of the visual mesh. |
| Box | 2 | Collision model uses a bounding box that encompasses the visual mesh. |
| PreciseConvexDecomposition | 3 | Collison model uses a convex-hull decomposition of the visual mesh which is computed by a variation of an algorithm called HACD. This option is the most accurate representation of collision geometry for complex objects with built-in tolerances to reduce the total number of convex-hulls by compromising on accuracy when justified. |