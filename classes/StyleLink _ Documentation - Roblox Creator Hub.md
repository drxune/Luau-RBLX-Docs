# StyleLink | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StyleLink
Scraped: 2026-01-11T02:31:23.402623Z

## Inherits
- Object
- Instance
- StyleLink
- StyleSheet
- ScreenGui
- GuiObjects
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StyleLink](/docs/reference/engine/classes/StyleLink)

English

Feedback

Engine Class

![StyleLink](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StyleLink-Dark.webp)StyleLink

Links a [StyleSheet](/docs/reference/engine/classes/StyleSheet) to the instance tree whose root is the parent of
the StyleLink.

---

Summary

Properties

|  |
| --- |
| [StyleSheet](#StyleSheet):[StyleSheet](/docs/reference/engine/classes/StyleSheet) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Links a [StyleSheet](/docs/reference/engine/classes/StyleSheet) to the instance tree whose root is the parent of
the StyleLink. For example, placing a StyleLink under a [ScreenGui](/docs/reference/engine/classes/ScreenGui)
applies the referenced [StyleSheet](/docs/reference/engine/classes/StyleSheet) to both the [ScreenGui](/docs/reference/engine/classes/ScreenGui) and
all of the [GuiObjects](/docs/reference/engine/classes/GuiObject) within it. Only one [StyleSheet](/docs/reference/engine/classes/StyleSheet)
can apply to a given tree.

![](https://prod.docsiteassets.roblox.com/assets/studio/explorer/StyleLink-Propagation.png)

---

API Reference

Properties

StyleSheet

Read Parallel

The [StyleSheet](/docs/reference/engine/classes/StyleSheet) to link to the parent such that the parent's
descendants are styled accordingly.

StyleLink.StyleSheet:[StyleSheet](/docs/reference/engine/classes/StyleSheet)

The [StyleSheet](/docs/reference/engine/classes/StyleSheet) to link to the parent such that the parent's
descendants are styled accordingly.

Provide feedback

---