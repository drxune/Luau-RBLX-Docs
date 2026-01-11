# AssetFetchStatus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AssetFetchStatus
Scraped: 2026-01-11T02:43:47.700062Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)

English

Feedback

Engine Enum

AssetFetchStatus

---

Items

| Name | Value | Summary |
| --- | --- | --- |
| Success | 0 | The asset loaded successfully. |
| Failure | 1 | The asset failed to load successfully. Subsequent attempts are likely to fail; there may be something wrong with the [Content](/docs/reference/engine/datatypes/Content) string. |
| None | 2 | The engine has no information about this asset. The engine never tried to load it. |
| Loading | 3 | The engine is in the middle of trying to load this asset. |
| TimedOut | 4 | The engine tried to load this asset but timed out. Future attempts to load may succeed. |