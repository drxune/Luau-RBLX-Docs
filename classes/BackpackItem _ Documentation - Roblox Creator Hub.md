# BackpackItem | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BackpackItem
Scraped: 2026-01-11T02:41:05.726031Z

## Tags
- Not Creatable

## Inherits
- Model
- BackpackItem
- PVInstance
- Instance
- Object
- HopperBin
- Tool
- Backpack
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Model](/docs/reference/engine/classes/Model)
6. /
7. [BackpackItem](/docs/reference/engine/classes/BackpackItem)

English

Feedback

Engine Class

BackpackItem

BackpackItem is an abstract class for backpack items such as HopperBins and
Tools.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [TextureContent](#TextureContent):[Content](/docs/reference/engine/datatypes/Content) |
| [TextureId](#TextureId):ContentId |

Inherited Members

26 inherited from [Model](/docs/reference/engine/classes/Model)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[HopperBin](/docs/reference/engine/classes/HopperBin), [Tool](/docs/reference/engine/classes/Tool)

BackpackItem is an abstract class for backpack items such as HopperBins and
Tools.

---

API Reference

Properties

TextureContent

Read Parallel

The texture icon that is displayed for a tool in the player's backpack.
Only supports asset URIs.

BackpackItem.TextureContent:[Content](/docs/reference/engine/datatypes/Content)

The texture icon that is displayed for a tool in the player's backpack.

This property should be set to the content ID of an image uploaded to the
Roblox website. Only asset URIs are supported for this property.

If this property is left blank, the [Backpack](/docs/reference/engine/classes/Backpack) GUI will display the
name of the tool instead.

Provide feedback

---

TextureId

Read Parallel

The texture icon that is displayed for a tool in the player's backpack.

BackpackItem.TextureId:ContentId

The texture icon that is displayed for a tool in the player's backpack.

This property should be set to the content ID of an image uploaded to the
Roblox website.

If this property is left blank, the [Backpack](/docs/reference/engine/classes/Backpack) GUI will display the
name of the tool instead.

Provide feedback

---