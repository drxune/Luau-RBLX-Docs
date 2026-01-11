# HumanoidStateType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/HumanoidStateType
Scraped: 2026-01-11T02:46:23.722112Z

## Inherits
- Humanoid
- Humanoid:GetState()
- Humanoid:ChangeState()
- Humanoid.StateChanged
- LocalScript
- Humanoid.Jump
- Terrain
- Humanoid.PlatformStand
- TrussPart
- Humanoid.Sit
1. [Enums](/docs/reference/engine/enums)
2. /
3. [HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)

English

Feedback

Engine Enum

HumanoidStateType

---

Identifies, reads and sets the physics control state of a [Humanoid](/docs/reference/engine/classes/Humanoid).
[Humanoid:GetState()](/docs/reference/engine/classes/Humanoid#GetState) and [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState) methods, as
well as the [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged) event currently use this Enum.

Some states only allow manual setting, and allow a developer to make the
Humanoid relinquish control of its character.

When altering the Humanoid of a player, this should be done from a
[LocalScript](/docs/reference/engine/classes/LocalScript) ran by that player on their local client. Certain states
only work when set by the owner process (client or server). (Dead for example)

Items

| Name | Value | Summary |
| --- | --- | --- |
| FallingDown | 0 | The Humanoid has been tripped, and will attempt to get up in a few moments. |
| Ragdoll | 1 | (Deprecated) The Humanoid has been hit by a fast moving object (uncontrolled falling). *The Humanoid can recover from this.* This state has to be set and unset manually using [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState). |
| GettingUp | 2 | The Humanoid is getting back on their feet after FallingDown or Ragdoll. |
| Jumping | 3 | The Humanoid just jumped. (Check [Humanoid.Jump](/docs/reference/engine/classes/Humanoid#Jump)). This state lasts only briefly. This state normally transitions into either Landed, if on the ground, or Freefall, if still in the air. |
| Swimming | 4 | The Humanoid is currently swimming in [Terrain](/docs/reference/engine/classes/Terrain) water. |
| Freefall | 5 | The Humanoid is currently freefalling (jumped from a height or fell off a ledge). |
| Flying | 6 | When set, the Humanoid won't be animated, as with the [Humanoid.PlatformStand](/docs/reference/engine/classes/Humanoid#PlatformStand) property. This state lasts as long as the player flies. |
| Landed | 7 | The Humanoid touched the ground after a Freefall. This state lasts only briefly. |
| Running | 8 | Currently running while on the ground. |
| RunningNoPhysics | 10 | (Deprecated) Currently running and not near other physical objects. |
| StrafingNoPhysics | 11 | Not currently used with default Humanoid. Cannot be set with [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState). |
| Climbing | 12 | The Humanoid is climbing (e.g. up a [TrussPart](/docs/reference/engine/classes/TrussPart) or ladder). |
| Seated | 13 | The Humanoid is currently sitting in a Seat or VehicleSeat. Check the [Humanoid.Sit](/docs/reference/engine/classes/Humanoid#Sit) property. |
| PlatformStanding | 14 | The Humanoid is platformstanding. Check the [Humanoid.PlatformStand](/docs/reference/engine/classes/Humanoid#PlatformStand) property. |
| Dead | 15 | The Humanoid died. Changing a Humanoid's state to this state will kill it. |
| Physics | 16 | The Humanoid doesn't apply any force on its own and will not automatically transition to any other state. This state has to be set and unset manually using [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState). |
| None | 18 | Unusable placeholder in case an unknown state gets triggered internally. |