# StyleDerive | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StyleDerive
Scraped: 2026-01-11T02:41:32.444593Z

## Inherits
- Object
- Instance
- StyleDerive
- StyleSheet
- StyleRules
- Priority
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StyleDerive](/docs/reference/engine/classes/StyleDerive)

English

Feedback

Engine Class

![StyleDerive](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StyleDerive-Dark.webp)StyleDerive

When parented to a [StyleSheet](/docs/reference/engine/classes/StyleSheet), references another [StyleSheet](/docs/reference/engine/classes/StyleSheet)
from which the parent inherits [StyleRules](/docs/reference/engine/classes/StyleRule) and token
definitions.

---

Summary

Properties

|  |
| --- |
| [Priority](#Priority):[number](/docs/luau/numbers) |
| [StyleSheet](#StyleSheet):[StyleSheet](/docs/reference/engine/classes/StyleSheet) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

When parented to a [StyleSheet](/docs/reference/engine/classes/StyleSheet), references another [StyleSheet](/docs/reference/engine/classes/StyleSheet)
from which the parent inherits [StyleRules](/docs/reference/engine/classes/StyleRule) and token
definitions. Multiple StyleDerive instances can exist under a
[StyleSheet](/docs/reference/engine/classes/StyleSheet) and you can order them by
[Priority](/docs/reference/engine/classes/StyleDerive#Priority).

---

API Reference

Properties

Priority

Read Parallel

A number that determines how style properties inherited through this
StyleDerive apply relative to the same properties inherited through
other StyleDerives.

StyleDerive.Priority:[number](/docs/luau/numbers)

A number that determines how style properties inherited through this
StyleDerive apply relative to the same properties inherited through
other StyleDerives. Higher priority takes precedence over lower; for
example, if a StyleDerive with a priority of 10 points to a sheet
StyleSheetA, its [StyleRules](/docs/reference/engine/classes/StyleRule) and tokens will take
precedence over the same [StyleRules](/docs/reference/engine/classes/StyleRule) and tokens inherited
through lower-priority StyleDerives.

Provide feedback

---

StyleSheet

Read Parallel

The [StyleSheet](/docs/reference/engine/classes/StyleSheet) from which the parent [StyleSheet](/docs/reference/engine/classes/StyleSheet) inherits
[StyleRules](/docs/reference/engine/classes/StyleRule) and token definitions.

StyleDerive.StyleSheet:[StyleSheet](/docs/reference/engine/classes/StyleSheet)

The [StyleSheet](/docs/reference/engine/classes/StyleSheet) from which the parent [StyleSheet](/docs/reference/engine/classes/StyleSheet) inherits
[StyleRules](/docs/reference/engine/classes/StyleRule) and token definitions.

Provide feedback

---