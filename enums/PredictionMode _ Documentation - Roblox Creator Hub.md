# PredictionMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PredictionMode
Scraped: 2026-01-11T02:43:13.890730Z

## Inherits
- RunService:SetPredictionMode()
- BaseParts
- Humanoid
- BasePart
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PredictionMode](/docs/reference/engine/enums/PredictionMode)

English

Feedback

Engine Enum

PredictionMode

---

Enum used with [RunService:SetPredictionMode()](/docs/reference/engine/classes/RunService#SetPredictionMode) to define the prediction
mode for the instance.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Automatic | 0 | The engine will automatically decide if this instance should be predicted or not. Currently, only [BaseParts](/docs/reference/engine/classes/BasePart) near the local player character's [Humanoid](/docs/reference/engine/classes/Humanoid) will be predicted within a dynamic radius that grows and shrinks based on the device's capability to handle the simulation load. |
| On | 1 | The instance will be predicted. Mismatches in the attributes of this instance between the client and server will cause a rollback and resimulation. If the instance is a [BasePart](/docs/reference/engine/classes/BasePart), its physics properties will be predicted ahead of the replicated authoritative server state. |
| Off | 2 | The instance will not be predicted. Regular network ownership semantics apply. |