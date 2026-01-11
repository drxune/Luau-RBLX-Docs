# Highlight | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Highlight
Scraped: 2026-01-11T02:37:26.597647Z

## Inherits
- Object
- Instance
- Highlight
- Enabled
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Highlight](/docs/reference/engine/classes/Highlight)

English

Feedback

Engine Class

![Highlight](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Highlight-Dark.webp)Highlight

A visual effect which you can use to call attention to a specific object
within an experience.

---

Summary

Properties

|  |
| --- |
| [Adornee](#Adornee):[Instance](/docs/reference/engine/datatypes/Instance) |
| [DepthMode](#DepthMode):[Enum.HighlightDepthMode](/docs/reference/engine/enums/HighlightDepthMode) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [FillColor](#FillColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [FillTransparency](#FillTransparency):[number](/docs/luau/numbers) |
| [OutlineColor](#OutlineColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [OutlineTransparency](#OutlineTransparency):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [Highlight](/docs/reference/engine/classes/Highlight) instance is a visual effect which you can use to call
attention to a specific object within an experience. Every highlight effect
has a silhouette outline that surrounds the object and a solid overlay
interior that displays over the object. You can customize both of these
components independently to modify the highlight's visual appearance.

|  |  |  |
| --- | --- | --- |
| Base object | White outline, 50% red interior | Yellow outline, black interior |

Useful applications of the highlight effect include:

* Providing visual feedback that an object is important and/or interactable.
* Making distant objects visible through objects that are closer to the user.
* Indicating the current position and status of other characters.

#### Limitations

As a performance limit, Studio only displays 255 simultaneous
[Highlight](/docs/reference/engine/classes/Highlight) instances on the client at a time. If you exceed this limit,
the additional instances are silently ignored. Note that while a
[Highlight](/docs/reference/engine/classes/Highlight) with [Enabled](/docs/reference/engine/classes/Highlight#Enabled) set to false
doesn't display, it still takes one of the 255 available slots, so if you plan
to permanently disable a [Highlight](/docs/reference/engine/classes/Highlight) instance, it's best to delete it
rather than disable it.

---

API Reference

Properties

Adornee

Read Parallel

The [Instance](/docs/reference/engine/classes/Instance) that the [Highlight](/docs/reference/engine/classes/Highlight) is applied to.

Highlight.Adornee:[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) for which to apply the [Highlight](/docs/reference/engine/classes/Highlight), used to
apply the effect to an [Instance](/docs/reference/engine/classes/Instance) outside of a child/parent
relationship.

Provide feedback

---

DepthMode

Read Parallel

Controls how the [Highlight](/docs/reference/engine/classes/Highlight) effect displays with respect to other
objects in the world.

Highlight.DepthMode:[Enum.HighlightDepthMode](/docs/reference/engine/enums/HighlightDepthMode)

Controls how the [Highlight](/docs/reference/engine/classes/Highlight) effect displays with respect to other
objects in the world. You can set this property to one of the following
options:

* [AlwaysOnTop](/docs/reference/engine/enums/HighlightDepthMode#AlwaysOnTop) — Allows the highlight
  to display regardless if there are objects between the camera and the
  highlighted object. This means the viewer is always able to see the
  highlight regardless of what is between the highlighted object and the
  camera.
* [Occluded](/docs/reference/engine/enums/HighlightDepthMode#Occluded) — Hides the highlight if
  there are objects between the camera and the highlighted object. This
  means the viewer is only able to see the object if there are no
  obstructing objects between the highlighted object and the camera's
  view.

|  |  |
| --- | --- |
| DepthMode = AlwaysOnTop | DepthMode = Occluded |

Provide feedback

---

Enabled

Read Parallel

Sets whether or not the highlight is enabled.

Highlight.Enabled:[boolean](/docs/luau/booleans)

Sets whether or not the highlight is enabled. This does not impact
performance, but disabled [Highlight](/docs/reference/engine/classes/Highlight) instances will still take one
of the 255 available slots. If you plan to permanently disable a
[Highlight](/docs/reference/engine/classes/Highlight) instance, it's best to delete it rather than disable it.

Provide feedback

---

FillColor

Read Parallel

Sets the [Color3](/docs/reference/engine/datatypes/Color3) value of the highlight's interior.

Highlight.FillColor:[Color3](/docs/reference/engine/datatypes/Color3)

Sets the [Color3](/docs/reference/engine/datatypes/Color3) value of the highlight's interior.

|  |  |  |
| --- | --- | --- |
| FillColor = [255, 100, 50] | FillColor = [0, 255, 125] | FillColor = [75, 150, 255] |

Provide feedback

---

FillTransparency

Read Parallel

Sets the transparency of the highlight's interior.

Highlight.FillTransparency:[number](/docs/luau/numbers)

Sets the visibility of the highlight's interior to any value between the
default value of 0 (opaque) and 1 (invisible). You can use this
property to determine how much of the object's existing color you want
viewers to see.

|  |  |  |
| --- | --- | --- |
| FillTransparency = 0 | FillTransparency = 0.5 | FillTransparency = 1 |

Provide feedback

---

OutlineColor

Read Parallel

Sets the [Color3](/docs/reference/engine/datatypes/Color3) value of the highlight's outline.

Highlight.OutlineColor:[Color3](/docs/reference/engine/datatypes/Color3)

Sets the [Color3](/docs/reference/engine/datatypes/Color3) value of the highlight's outline.

|  |  |  |
| --- | --- | --- |
| OutlineColor = [255, 100, 50] | OutlineColor = [0, 255, 125] | OutlineColor = [75, 150, 255] |

Provide feedback

---

OutlineTransparency

Read Parallel

Sets the transparency of the highlight's outline.

Highlight.OutlineTransparency:[number](/docs/luau/numbers)

Sets the visibility of the highlight's outline to a value between 0
(opaque) and 1 (transparent).

|  |  |  |
| --- | --- | --- |
| OutlineTransparency = 0 | OutlineTransparency = 1 |  |

Provide feedback

---