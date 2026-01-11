# BreakReason | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/BreakReason
Scraped: 2026-01-11T02:42:55.126194Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [BreakReason](/docs/reference/engine/enums/BreakReason)

English

Feedback

Engine Enum

BreakReason

---

Value for the reason the Class.ScriptDebugger.EncounteredBreak signal fired.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Other | 0 | Pausing for a reason not covered by other values, for example if the user hit "Pause" button. |
| Error | 1 | Pausing on error hit in the code. |
| SpecialBreakpoint | 2 | Pausing on an internal breakpoint set by debugger command: e.g. step over, step into, step out of. |
| UserBreakpoint | 3 | Pausing on a user breakpoint. |