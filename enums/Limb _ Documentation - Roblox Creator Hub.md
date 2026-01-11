# Limb | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/Limb
Scraped: 2026-01-11T02:43:51.047610Z

## Inherits
- Humanoid:GetLimb()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [Limb](/docs/reference/engine/enums/Limb)

English

Feedback

Engine Enum

Limb

---

Describes which limb a particular Instance belongs to (assuming the Instance
is part of a Humanoid). Passing an Instance to the Humanoid:GetLimb() function
will return the Limb for the Instance.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Head | 0 | If the limb is a part of the Humanoid's Head. |
| Torso | 1 | If the limb is a part of the Humanoid's Torso. This includes UpperTorso and LowerTorso for R15 rigs. |
| LeftArm | 2 | If the limb is a part of the Humanoid's Left Arm. This includes UpperLeftArm, LowerLeftArm, and LeftHand for R15 rigs. |
| RightArm | 3 | If the limb is a part of the Humanoid's Right Arm. This includes UpperRightArm, LowerRightArm and RightHand for R15 rigs. |
| LeftLeg | 4 | If the limb is a part of the Humanoid's Left Leg. This includes UpperLeftLeg, LowerLeftLeg and LeftFoot for R15 rigs. |
| RightLeg | 5 | If the limb is a part of the Humanoid's Right Leg. This includes UpperRightLeg, LowerRightLeg, and RightFoot for R15 rigs. |
| Unknown | 6 | If a part is not a limb (e.g. running the [Humanoid:GetLimb()](/docs/reference/engine/classes/Humanoid#GetLimb) function and passing it an accessory which is a sibling of the Humanoid will return this value). |