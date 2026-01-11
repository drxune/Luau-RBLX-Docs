# TriangleMeshPart | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TriangleMeshPart
Scraped: 2026-01-11T02:36:17.487542Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- BasePart
- TriangleMeshPart
- PVInstance
- Instance
- Object
- MeshPart
- PartOperation
- CollisionFidelity
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BasePart](/docs/reference/engine/classes/BasePart)
6. /
7. [TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart)

English

Feedback

Engine Class

TriangleMeshPart

Abstract intermediate class that manages physical geometry properties for
PartOperations and MeshParts.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [CollisionFidelity](#CollisionFidelity):[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity) |
| [FluidFidelity](#FluidFidelity):[Enum.FluidFidelity](/docs/reference/engine/enums/FluidFidelity) |
| [MeshSize](#MeshSize):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[MeshPart](/docs/reference/engine/classes/MeshPart), [PartOperation](/docs/reference/engine/classes/PartOperation)

TriangleMeshPart is an abstract intermediate class from which [MeshPart](/docs/reference/engine/classes/MeshPart)
and [PartOperation](/docs/reference/engine/classes/PartOperation) inherit. It was created to consolidate the
management of physical geometry properties between the two sub-classes. It
implements the read-only
[CollisionFidelity](/docs/reference/engine/classes/TriangleMeshPart#CollisionFidelity).

---

API Reference

Properties

CollisionFidelity

Not Replicated

Plugin Security

Read Parallel

Determines the level of detail the part's physics will adhere to its mesh.

TriangleMeshPart.CollisionFidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity)

This property determines how the collision model of the
[TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart) relates to the actual geometry of the mesh. This
property cannot be read or manipulated by scripts during runtime.

See [here](/docs/workspace/collisions#collision-fidelity) for a
visual representation of the various options.

Provide feedback

---

FluidFidelity

Not Replicated

Plugin Security

Read Parallel

Determines the geometric representation used to compute aerodynamic forces
and torques.

TriangleMeshPart.FluidFidelity:[Enum.FluidFidelity](/docs/reference/engine/enums/FluidFidelity)

Determines the geometric representation used to compute aerodynamic forces
and torques.

Provide feedback

---

MeshSize

Read Only

Not Replicated

Read Parallel

TriangleMeshPart.MeshSize:[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---