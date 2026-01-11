# PhysicsSteppingMethod | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PhysicsSteppingMethod
Scraped: 2026-01-11T02:43:23.402273Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PhysicsSteppingMethod](/docs/reference/engine/enums/PhysicsSteppingMethod)

English

Feedback

Engine Enum

PhysicsSteppingMethod

---

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | The current default is Adaptive. |
| Fixed | 1 | All simulated assemblies inside the workspace will advance forward at 240 Hz. This option is best for optimal stability and simulation accuracy. |
| Adaptive | 2 | The engine attempts to assign optimal simulation rates for individual assemblies of either 240 Hz, 120 Hz, or 60 Hz. This setting is optimized for performance. |