# MoverConstraintRootBehaviorMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/MoverConstraintRootBehaviorMode
Scraped: 2026-01-11T02:44:36.700397Z

## Inherits
- Workspace.MoverConstraintRootBehavior
- BodyMover
1. [Enums](/docs/reference/engine/enums)
2. /
3. [MoverConstraintRootBehaviorMode](/docs/reference/engine/enums/MoverConstraintRootBehaviorMode)

English

Feedback

Engine Enum

MoverConstraintRootBehaviorMode

---

Values for [Workspace.MoverConstraintRootBehavior](/docs/reference/engine/classes/Workspace#MoverConstraintRootBehavior). Controls the logic
for selecting the assembly root part when using various
[mover constraints](/docs/physics/mover-constraints).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | The default option for [Workspace.MoverConstraintRootBehavior](/docs/reference/engine/classes/Workspace#MoverConstraintRootBehavior). Currently set to Disabled. |
| Disabled | 1 | The legacy logic will be used for assembly root part selection when a mechanism contains a mover constraint. |
| Enabled | 2 | Improved logic will be used for assembly root part selection when a mechanism contains a mover constraint. This improved logic gives more consistent behavior when compared with other constraints or the deprecated [BodyMover](/docs/reference/engine/classes/BodyMover) classes. |