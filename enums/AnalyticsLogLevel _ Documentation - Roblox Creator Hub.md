# AnalyticsLogLevel | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AnalyticsLogLevel
Scraped: 2026-01-11T02:45:33.390147Z

## Inherits
- AnalyticsService.LogEvent
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AnalyticsLogLevel](/docs/reference/engine/enums/AnalyticsLogLevel)

English

Feedback

Engine Enum

AnalyticsLogLevel

---

This enum is used as an argument in [AnalyticsService.LogEvent](/docs/reference/engine/classes/AnalyticsService#LogEvent) to
describe the error severity level.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Trace | 0 | Trace is the noisiest level, rarely (if ever) enabled for a production app. |
| Debug | 1 | Used for debugging. |
| Information | 2 |  |
| Warning | 3 | Used for warning. |
| Error | 4 | When functionality is unavailable or expectations broken. |
| Fatal | 5 | The most critical level, Fatal events demand immediate attention. |