# ContentSourceType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ContentSourceType
Scraped: 2026-01-11T02:45:43.225093Z

## Inherits
- Object
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ContentSourceType](/docs/reference/engine/enums/ContentSourceType)

English

Feedback

Engine Enum

ContentSourceType

---

The source type of [Content](/docs/reference/engine/datatypes/Content) value. Indicates which properties of a
[Content](/docs/reference/engine/datatypes/Content) contain the referenced content.

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | Empty value with no source type. Does not reference any content or hold any non‑nil value. |
| Uri | 1 | An [asset URI](/docs/projects/assets#asset-uris) string value contained in [Content.Uri](/docs/reference/engine/datatypes/Content#Uri). |
| Object | 2 | A non-nil [Object](/docs/reference/engine/classes/Object) reference contained in [Content.Object](/docs/reference/engine/datatypes/Content#Object). |
| Opaque | 3 | A non-nil Opaque reference contained in [Content.Opaque](/docs/reference/engine/datatypes/Content#Opaque). |