# UIPageLayout | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIPageLayout
Scraped: 2026-01-11T02:32:32.094049Z

## Tags
- Not Replicated

## Inherits
- UIGridStyleLayout
- UIPageLayout
- GuiObject
- Instance
- Object
- UIPageLayout.CurrentPage
- UIPageLayout:JumpTo()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)
6. /
7. [UIPageLayout](/docs/reference/engine/classes/UIPageLayout)

English

Feedback

Engine Class

![UIPageLayout](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIPageLayout-Dark.webp)UIPageLayout

---

Summary

Properties

|  |
| --- |
| [Animated](#Animated):[boolean](/docs/luau/booleans) |
| [Circular](#Circular):[boolean](/docs/luau/booleans) |
| [CurrentPage](#CurrentPage):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [EasingDirection](#EasingDirection):[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection) |
| [EasingStyle](#EasingStyle):[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle) |
| [GamepadInputEnabled](#GamepadInputEnabled):[boolean](/docs/luau/booleans) |
| [Padding](#Padding):[UDim](/docs/reference/engine/datatypes/UDim) |
| [ScrollWheelInputEnabled](#ScrollWheelInputEnabled):[boolean](/docs/luau/booleans) |
| [TouchInputEnabled](#TouchInputEnabled):[boolean](/docs/luau/booleans) |
| [TweenTime](#TweenTime):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [JumpTo](#JumpTo)(page: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [JumpToIndex](#JumpToIndex)(index: [number](/docs/luau/numbers)):() |
| [Next](#Next)():() |
| [Previous](#Previous)():() |

Events

|  |
| --- |
| [PageEnter](#PageEnter)(page: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PageLeave](#PageLeave)(page: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Stopped](#Stopped)(currentPage: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

7 inherited from [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Creates a paged viewing window, like the home screen of a mobile device. You
can use a UIPageLayout by parenting it to a GuiObject. The UIPageLayout will
then apply itself to all of its GuiObject siblings.

---

API Reference

Properties

Animated

Read Parallel

Whether or not to animate transitions between pages.

UIPageLayout.Animated:[boolean](/docs/luau/booleans)

Whether or not to animate transitions between pages.

Provide feedback

---

Circular

Read Parallel

Whether or not the page layout wraps around at the ends.

UIPageLayout.Circular:[boolean](/docs/luau/booleans)

Whether or not the page layout wraps around at the ends.

Provide feedback

---

CurrentPage

Read Only

Not Replicated

Read Parallel

The page that is either currently being displayed or is the target of the
current animation.

UIPageLayout.CurrentPage:[GuiObject](/docs/reference/engine/classes/GuiObject)

The page that is either currently being displayed or is the target of the
current animation.

Provide feedback

---

EasingDirection

Read Parallel

The easing direction to use when performing an animation.

UIPageLayout.EasingDirection:[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection)

The easing direction to use when performing an animation.

Provide feedback

---

EasingStyle

Read Parallel

The easing style to use when performing an animation.

UIPageLayout.EasingStyle:[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle)

The easing style to use when performing an animation.

Provide feedback

---

GamepadInputEnabled

Read Parallel

Controls the overrides of NextSelection{Up, Down, Left, Right}. Defaults
to true.

UIPageLayout.GamepadInputEnabled:[boolean](/docs/luau/booleans)

Controls the overrides of NextSelection{Up,Down,Left,Right}. Defaults to
true.

Provide feedback

---

Padding

Read Parallel

Determines the amount that pages are separated from each other by.

UIPageLayout.Padding:[UDim](/docs/reference/engine/datatypes/UDim)

Determines the amount that pages are separated from each other by. Can be
set either using scale (Percentage of parent's size in the current
direction) or offset (a static spacing value, similar to pixel size).

Provide feedback

---

ScrollWheelInputEnabled

Read Parallel

Controls the use of scroll wheel, in case that it is intended for
something else. Defaults to true.

UIPageLayout.ScrollWheelInputEnabled:[boolean](/docs/luau/booleans)

Controls the use of scroll wheel, in case that it is intended for
something else. Defaults to true.

Provide feedback

---

TouchInputEnabled

Read Parallel

Controls touch scrolling, in case this is a non-interactive layout.
Defaults to true.

UIPageLayout.TouchInputEnabled:[boolean](/docs/luau/booleans)

Controls touch scrolling, in case this is a non-interactive layout.
Defaults to true.

Provide feedback

---

TweenTime

Read Parallel

The length of the animation.

UIPageLayout.TweenTime:[number](/docs/luau/numbers)

The length of the animation.

Provide feedback

---

Methods

JumpTo

If the page is in the UIPageLayout, then it sets
[UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) to it and animates to it. If the circular
layout is enabled, it will take the shortest path to this page.

UIPageLayout:JumpTo(page:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| page:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

If the page is in the UIPageLayout, then it sets
[UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) to it and animates to it. If the circular
layout is enabled, it will take the shortest path to this page.

Provide feedback

---

JumpToIndex

If the index is >= 0 and less than the size of the layout, this method
acts like [UIPageLayout:JumpTo()](/docs/reference/engine/classes/UIPageLayout#JumpTo). If it's out of bounds and
circular is set, it will animate the full distance between the in-bounds
index of [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) and the new index.

UIPageLayout:JumpToIndex(index:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers) |

Returns

()

If the index is >= 0 and less than the size of the layout, this method
acts like [UIPageLayout:JumpTo()](/docs/reference/engine/classes/UIPageLayout#JumpTo). If it's out of bounds and
circular is set, it will animate the full distance between the in-bounds
index of [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) and the new index.

Provide feedback

---

Next

Sets [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) to the page after the current page
and animates to it, or does nothing if there isn't a next page.

UIPageLayout:Next():()

Returns

()

Sets [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) to the page after the current page
and animates to it, or does nothing if there isn't a next page.

Provide feedback

---

Previous

Sets [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) to the page before the current page
and animates to it, or does nothing if there isn't a previous page.

UIPageLayout:Previous():()

Returns

()

Sets [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) to the page before the current page
and animates to it, or does nothing if there isn't a previous page.

Provide feedback

---

Events

PageEnter

Fires when a page comes into view, and is going to be rendered.

UIPageLayout.PageEnter(page:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| page:[Instance](/docs/reference/engine/datatypes/Instance) |

Fires when a page comes into view, and is going to be rendered.

Provide feedback

---

PageLeave

Fires when a page leaves view, and will not be rendered.

UIPageLayout.PageLeave(page:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| page:[Instance](/docs/reference/engine/datatypes/Instance) |

Fires when a page leaves view, and will not be rendered.

Provide feedback

---

Stopped

Fires when an animation to [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) is completed
without being canceled, and the view stops scrolling.

UIPageLayout.Stopped(currentPage:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| currentPage:[Instance](/docs/reference/engine/datatypes/Instance) |

Fires when an animation to [UIPageLayout.CurrentPage](/docs/reference/engine/classes/UIPageLayout#CurrentPage) is completed
without being canceled, and the view stops scrolling.

Provide feedback

---