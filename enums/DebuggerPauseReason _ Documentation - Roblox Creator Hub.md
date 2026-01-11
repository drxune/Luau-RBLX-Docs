# DebuggerPauseReason | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/DebuggerPauseReason
Scraped: 2026-01-11T02:42:51.917473Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [DebuggerPauseReason](/docs/reference/engine/enums/DebuggerPauseReason)

English

Feedback

Engine Enum

DebuggerPauseReason

---

Reason that the DataModel was paused.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Unknown | 0 | Pausing for a reason not covered by other values. |
| Requested | 1 | Pause was requested by user. |
| Breakpoint | 2 | Pausing on a user breakpoint. |
| Exception | 3 | Pausing on error hit in the code. |
| SingleStep | 4 | Pausing on an internal breakpoint set by debugger command: e.g. step over, step into, step out of. |
| Entrypoint | 5 | Pausing at the entry on the script. |