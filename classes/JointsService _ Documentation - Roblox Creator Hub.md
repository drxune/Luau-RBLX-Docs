# JointsService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/JointsService
Scraped: 2026-01-11T02:38:01.940923Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- JointsService
- JointsService:ShowPermissibleJoints()
- JointsService:SetJoinAfterMoveTarget()
- JointsService:SetJoinAfterMoveInstance()
- BasePart
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [JointsService](/docs/reference/engine/classes/JointsService)

English

Feedback

Engine Class

JointsService

Deprecated

A service that stores joints created by surface connections.

Not Creatable

Service

This service has been deprecated in favor of
[constraints](/docs/physics/mechanical-constraints) which should be used
for surface connections instead

---

Summary

Methods

|  |
| --- |
| [ClearJoinAfterMoveJoints](#ClearJoinAfterMoveJoints)():() |
| [CreateJoinAfterMoveJoints](#CreateJoinAfterMoveJoints)():() |
| [SetJoinAfterMoveInstance](#SetJoinAfterMoveInstance)(joinInstance: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [SetJoinAfterMoveTarget](#SetJoinAfterMoveTarget)(joinTarget: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [ShowPermissibleJoints](#ShowPermissibleJoints)():() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The JointsService is a service that stores joints created by surface
connections. It also has API available for visualizing surface to surface
contact, and joining surfaces together.

---

API Reference

Methods

ClearJoinAfterMoveJoints

Will remove any 'create joints' that were made visible via the
[JointsService:ShowPermissibleJoints()](/docs/reference/engine/classes/JointsService#ShowPermissibleJoints) method.

JointsService:ClearJoinAfterMoveJoints():()

Returns

()

Will remove any 'create joints' that were made visible via the
[JointsService:ShowPermissibleJoints()](/docs/reference/engine/classes/JointsService#ShowPermissibleJoints) method.

Provide feedback

---

CreateJoinAfterMoveJoints

Updates all visible joints for the parts assigned by the
[JointsService:SetJoinAfterMoveTarget()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveTarget) and
[JointsService:SetJoinAfterMoveInstance()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveInstance) methods.

JointsService:CreateJoinAfterMoveJoints():()

Returns

()

Updates all visible joints for the parts assigned by the
[JointsService:SetJoinAfterMoveTarget()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveTarget) and
[JointsService:SetJoinAfterMoveInstance()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveInstance) methods.

Provide feedback

---

SetJoinAfterMoveInstance

Sets the PVInstance that will be connected with the target PVInstance
specified by [JointsService:SetJoinAfterMoveTarget()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveTarget).

JointsService:SetJoinAfterMoveInstance(joinInstance:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| joinInstance:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

Sets the PVInstance that will be connected with the target PVInstance
specified by [JointsService:SetJoinAfterMoveTarget()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveTarget).

Provide feedback

---

SetJoinAfterMoveTarget

Sets the PVInstance that will be connected with the PVInstance specified
by [JointsService:SetJoinAfterMoveInstance()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveInstance).

JointsService:SetJoinAfterMoveTarget(joinTarget:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| joinTarget:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

Sets the PVInstance that will be connected with the PVInstance specified
by [JointsService:SetJoinAfterMoveInstance()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveInstance).

Provide feedback

---

ShowPermissibleJoints

When used it will visibly display a potential surface connection between
the two [BasePart](/docs/reference/engine/classes/BasePart), which were set with
[JointsService:SetJoinAfterMoveTarget()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveTarget) and
[JointsService:SetJoinAfterMoveInstance()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveInstance).

JointsService:ShowPermissibleJoints():()

Returns

()

When used it will visibly display a potential surface connection between
the two [BasePart](/docs/reference/engine/classes/BasePart), which were set with
[JointsService:SetJoinAfterMoveTarget()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveTarget) and
[JointsService:SetJoinAfterMoveInstance()](/docs/reference/engine/classes/JointsService#SetJoinAfterMoveInstance).

Provide feedback

---