# CanvasGroup | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CanvasGroup
Scraped: 2026-01-11T02:28:36.436438Z

## Inherits
- GuiObject
- CanvasGroup
- GuiBase2d
- Instance
- Object
- UICorner
- UIGradient
- GuiObject.ClipsDescendants
- LayerCollector
- LayerCollector.ZIndexBehavior
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiObject](/docs/reference/engine/classes/GuiObject)
6. /
7. [CanvasGroup](/docs/reference/engine/classes/CanvasGroup)

English

Feedback

Engine Class

![CanvasGroup](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/CanvasGroup-Dark.webp)CanvasGroup

Blends descendants as a group with color/transparency.

---

Summary

Properties

|  |
| --- |
| [GroupColor3](#GroupColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [GroupTransparency](#GroupTransparency):[number](/docs/luau/numbers) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

CanvasGroup renders descendants as a group with color and transparency applied
to the render result. GuiEffect ([UICorner](/docs/reference/engine/classes/UICorner) and [UIGradient](/docs/reference/engine/classes/UIGradient))
under CanvasGroup will also apply to the whole group. CanvasGroup always has
[GuiObject.ClipsDescendants](/docs/reference/engine/classes/GuiObject#ClipsDescendants) set to true and all descendants will render
within CanvasGroup's viewport.

### Important notes:

* Descendants of CanvasGroup will be rendered as a flattened texture only when
  the ancestor [LayerCollector](/docs/reference/engine/classes/LayerCollector) has its
  [LayerCollector.ZIndexBehavior](/docs/reference/engine/classes/LayerCollector#ZIndexBehavior) set to [Enum.ZIndexBehavior.Sibling](/docs/reference/engine/enums/ZIndexBehavior#Sibling).
* CanvasGroup consumes extra texture memory. The quality of the texture and
  total memory usage is limited by the [Enum.QualityLevel](/docs/reference/engine/enums/QualityLevel) of the client. When
  exceeding the memory cap, CanvasGroup will render as a blank texture.
* We recommend using CanvasGroup with static sizes, otherwise a new texture
  would need to be created to accommodate new sizes.

---

API Reference

Properties

GroupColor3

Read Parallel

Color tint that applies to all descendants.

CanvasGroup.GroupColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color tint that applies to all descendants.

Provide feedback

---

GroupTransparency

Read Parallel

Transparency that applies to all descendants.

CanvasGroup.GroupTransparency:[number](/docs/luau/numbers)

Transparency that applies to all descendants.

Provide feedback

---