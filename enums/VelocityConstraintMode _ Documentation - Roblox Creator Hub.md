# VelocityConstraintMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/VelocityConstraintMode
Scraped: 2026-01-11T02:42:48.926132Z

## Inherits
- RelativeTo
- Attachment0
- Attachment1
1. [Enums](/docs/reference/engine/enums)
2. /
3. [VelocityConstraintMode](/docs/reference/engine/enums/VelocityConstraintMode)

English

Feedback

Engine Enum

VelocityConstraintMode

---

The velocity constraint mode sets how the attachment velocity is constrained.
The velocity can be constrained to a line, a plane or a vector. See each mode
for more details.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Line | 0 | The velocity component in the direction of the line is constrained to the specified value. The line direction is based on the [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) property:   * [Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo) - The line direction is the   primary axis of [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). * [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo) - The line direction is the   primary axis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1). * [World](/docs/reference/engine/enums/ActuatorRelativeTo) - The line direction must be specified. |
| Plane | 1 | The velocity components in the plane are constrained to the specified values. The plane tangents are based on the [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) property:   * [Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo) - The plane tangents are the two   axes of [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). * [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo) - The plane tangents are the two   axes of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1). * [World](/docs/reference/engine/enums/ActuatorRelativeTo) - The two plane tangents must be   specified |
| Vector | 2 | The velocity components must be equal to the vector components specified. The coordinate system of the vector is based on the [RelativeTo](/docs/reference/engine/classes/LinearVelocity#RelativeTo) property:   * [Attachment0](/docs/reference/engine/enums/ActuatorRelativeTo) - The vector components are in the   coordinate system defined by the axes of   [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). * [Attachment1](/docs/reference/engine/enums/ActuatorRelativeTo) - The vector components are in the   coordinate system defined by the axes of   [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1). * [World](/docs/reference/engine/enums/ActuatorRelativeTo) - The coordinate system is in the world   and the vector components must be specified. |