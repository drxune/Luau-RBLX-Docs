# ModelLevelOfDetail | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ModelLevelOfDetail
Scraped: 2026-01-11T02:45:04.522286Z

## Inherits
- Models
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ModelLevelOfDetail](/docs/reference/engine/enums/ModelLevelOfDetail)

English

Feedback

Engine Enum

ModelLevelOfDetail

---

Controls the level of detail for [Models](/docs/reference/engine/classes/Model) in experiences with
instance [streaming](/docs/workspace/streaming) enabled.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Automatic | 0 | Default behavior, currently equivalent to Disabled. |
| StreamingMesh | 1 | A lower resolution "imposter" mesh (colored, coarse mesh that wraps around all child parts of the model) renders outside the streaming radius. |
| Disabled | 2 | A lower resolution mesh will not be displayed. |
| SLIM | 4 | A Scalable Lightweight Interactive Model, or SLIM, model (a composite of all child parts of the model) renders at progressively lower resolutions at distances based on the streaming radius. Greatly improves visual quality over StreamingMesh. |