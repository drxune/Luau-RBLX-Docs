# FluidForces | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/FluidForces
Scraped: 2026-01-11T02:44:45.419929Z

## Inherits
- Workspace.FluidForces
- BaseParts
- EnableFluidForces
1. [Enums](/docs/reference/engine/enums)
2. /
3. [FluidForces](/docs/reference/engine/enums/FluidForces)

English

Feedback

Engine Enum

FluidForces

---

Used as an enum value for [Workspace.FluidForces](/docs/reference/engine/classes/Workspace#FluidForces) to control the
enablement of aerodynamic forces on parts and assemblies in the workspace.
Note that this enum is not applicable in scripting and
[Workspace.FluidForces](/docs/reference/engine/classes/Workspace#FluidForces) must be toggled in Studio.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Aerodynamic forces will not be calculated on any [BaseParts](/docs/reference/engine/classes/BasePart). |
| Experimental | 1 | Aerodynamic forces will be calculated on [BaseParts](/docs/reference/engine/classes/BasePart) with [EnableFluidForces](/docs/reference/engine/classes/BasePart#EnableFluidForces) set to true. During the beta phase, the behavior of the aerodynamic force model may change as the model improves. |