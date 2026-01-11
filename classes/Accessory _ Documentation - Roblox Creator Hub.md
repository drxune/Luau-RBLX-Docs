# Accessory | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Accessory
Scraped: 2026-01-11T02:35:46.014460Z

## Inherits
- Accoutrement
- Accessory
- Instance
- Object
- Attachment
- Hat
- Weld
- Humanoid:ApplyDescription()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Accoutrement](/docs/reference/engine/classes/Accoutrement)
6. /
7. [Accessory](/docs/reference/engine/classes/Accessory)

English

Feedback

Engine Class

![Accessory](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Accessory-Dark.webp)Accessory

An item that a Character can wear.

---

Summary

Properties

|  |
| --- |
| [AccessoryType](#AccessoryType):[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType) |

Inherited Members

5 inherited from [Accoutrement](/docs/reference/engine/classes/Accoutrement)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Accessory Instance is the parent Instance of all accessories (regardless
of their specific accessory type). It typically has a child Handle with a
child Attachment and a WrapLayer in the case of Layered Clothing.

The Accessory class is the successor to the legacy Hat system. It's
cross-compatible with both the legacy R6 character system and the new R15
character system.

If you insert an [Attachment](/docs/reference/engine/classes/Attachment) into the Accessory's Handle with the same
name as an [Attachment](/docs/reference/engine/classes/Attachment) in one of the character's limbs, they connect
and ignore properties inherited from the [Accoutrement](/docs/reference/engine/classes/Accoutrement) class.
Otherwise, the Accessory functions identically to a [Hat](/docs/reference/engine/classes/Hat).

Note: If there are two matching Attachments, the resulting [Weld](/docs/reference/engine/classes/Weld) is a
child of the Accessory's Handle. This differs from the legacy behavior of Hats
where the Weld is always a child of the Head of the character.

---

API Reference

Properties

AccessoryType

Read Parallel

Specifies the AccessoryType of the Accessory (eg. Hat, Tshirt, Waist).

Accessory.AccessoryType:[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType)

Specifies the AccessoryType of the Accessory. Is
[AccessoryType.Unknown](/docs/reference/engine/enums/AccessoryType) unless you equip the Accessory
through the player spawning process or
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription). If available on the Marketplace, you
can set [Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType) to categorize the Accessory item (for
example, "Hat" or "Face").

Provide feedback

---