# AdGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AdGui
Scraped: 2026-01-11T02:40:00.204919Z

## Tags
- Not Replicated

## Inherits
- SurfaceGuiBase
- AdGui
- LayerCollector
- GuiBase2d
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SurfaceGuiBase](/docs/reference/engine/classes/SurfaceGuiBase)
6. /
7. [AdGui](/docs/reference/engine/classes/AdGui)

English

Feedback

Engine Class

![AdGui](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AdGui-Dark.webp)AdGui

---

Summary

Properties

|  |
| --- |
| [AdShape](#AdShape):[Enum.AdShape](/docs/reference/engine/enums/AdShape) |
| [EnableVideoAds](#EnableVideoAds):[boolean](/docs/luau/booleans) |
| [FallbackImage](#FallbackImage):ContentId |
| [Status](#Status):[Enum.AdUnitStatus](/docs/reference/engine/enums/AdUnitStatus) |

Callbacks

|  |
| --- |
| [OnAdEvent](#OnAdEvent)(eventInfo: [Dictionary](/docs/luau/tables#dictionaries)):[boolean](/docs/luau/booleans) |

Inherited Members

3 inherited from [SurfaceGuiBase](/docs/reference/engine/classes/SurfaceGuiBase)

4 inherited from [LayerCollector](/docs/reference/engine/classes/LayerCollector)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Properties

AdShape

Read Parallel

AdGui.AdShape:[Enum.AdShape](/docs/reference/engine/enums/AdShape)

Provide feedback

---

EnableVideoAds

Read Parallel

Enables the AdGui to serve video ads.

AdGui.EnableVideoAds:[boolean](/docs/luau/booleans)

The property enables the AdGui to serve video ads.

Provide feedback

---

FallbackImage

Read Parallel

AdGui.FallbackImage:ContentId

Provide feedback

---

Status

Read Only

Not Replicated

Read Parallel

AdGui.Status:[Enum.AdUnitStatus](/docs/reference/engine/enums/AdUnitStatus)

Provide feedback

---

Callbacks

OnAdEvent

Used to react to the AdGui events.

AdGui.OnAdEvent(eventInfo:[Dictionary](/docs/luau/tables#dictionaries)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| eventInfo:[Dictionary](/docs/luau/tables#dictionaries)  Options table for the method:   * PlayerId – The user ID of the player related to the ad event. * AdEventType – A [Enum.AdEventType](/docs/reference/engine/enums/AdEventType) enum value describing the AdGui   events. |

Returns

[boolean](/docs/luau/booleans)

Whether the callback has successfully reacted to the event.

The callback function used to react to the AdGui events.

Provide feedback

---