# PredictionStatus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PredictionStatus
Scraped: 2026-01-11T02:46:13.897919Z

## Inherits
- RunService:GetPredictionStatus()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PredictionStatus](/docs/reference/engine/enums/PredictionStatus)

English

Feedback

Engine Enum

PredictionStatus

---

Enum used with [RunService:GetPredictionStatus()](/docs/reference/engine/classes/RunService#GetPredictionStatus) to check the status of
a specific instance.

This prediction status can be used to determine whether any associated scripts
should run. If the status is Authoritative or Predicted, such scripts
should run, since the local node is either the authority for the instance or
is predicting it. If the status is None, such scripts do not need to run.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Authoritative | 0 | This instance is authoritative. |
| Predicted | 1 | This instance is being predicted. |
| None | 2 | The instance will not be resimulated; classic simulation rules apply instead. |