# SurfaceType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/SurfaceType
Scraped: 2026-01-11T02:46:24.820443Z

## Inherits
- Part
- HingeConstraint
1. [Enums](/docs/reference/engine/enums)
2. /
3. [SurfaceType](/docs/reference/engine/enums/SurfaceType)

English

Feedback

Engine Enum

SurfaceType

Deprecated

SurfaceType joining is deprecated, leaving only visual changes on the
affected [Part](/docs/reference/engine/classes/Part). It should not be used for future work.

---

Used to determine how a surface should be displayed on a part and how
automatic surface joints should behave.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Smooth | 0 | Adds no details on the surface. |
| Glue | 1 | Adds an "X" pattern across the surface. |
| Weld | 2 | Adds an "X" pattern across the surface. |
| Studs | 3 | Adds square studs across the surface. |
| Inlet | 4 | Adds square holes across the surface where studs would be. |
| Universal | 5 | Adds a checker pattern to the surface using studs and inlets. |
| Hinge | 6 | Adds a yellow hinge to the surface. Parts touching it stick to the surface, allowing for rotations using physics. This should not be used for future work and existing instances should be replaced with a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint). |
| Motor | 7 | Functioned identically to a hinge with the addition of a grey ring. |
| SteppingMotor | 8 | Functioned identically to a motor. It may have functioned differently in the past, but that functionality is non-existent. |
| SmoothNoOutlines | 10 | Previously similar to Smooth with outlines but no longer relevant since outlines have been removed. |