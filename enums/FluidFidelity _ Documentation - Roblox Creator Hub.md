# FluidFidelity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/FluidFidelity
Scraped: 2026-01-11T02:44:44.923012Z

## Inherits
- MeshPart
- PartOperation
- TriangleMeshPart.CollisionFidelity
1. [Enums](/docs/reference/engine/enums)
2. /
3. [FluidFidelity](/docs/reference/engine/enums/FluidFidelity)

English

Feedback

Engine Enum

FluidFidelity

---

Determines the geometric representation used to compute aerodynamic forces and
torques for [MeshPart](/docs/reference/engine/classes/MeshPart) and [PartOperation](/docs/reference/engine/classes/PartOperation) instances.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Automatic | 0 | Let the physics engine select the geometric representation for aerodynamic force and torque calculations. |
| UseCollisionGeometry | 1 | Use the current collision geometry specified by [TriangleMeshPart.CollisionFidelity](/docs/reference/engine/classes/TriangleMeshPart#CollisionFidelity) for aerodynamic force and torque calculations . |
| UsePreciseGeometry | 2 | Force the engine to compute aerodynamic forces and torques using a more precise geometry representation based on the original mesh. This option may increase join and replication time if used on a large scale. |