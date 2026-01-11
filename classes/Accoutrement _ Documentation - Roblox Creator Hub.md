# Accoutrement | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Accoutrement
Scraped: 2026-01-11T02:27:46.352099Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Accoutrement
- Accessory
- Hat
- part
- AttachmentPos
- Right
- Forward
- Up
- GetRootPart()
- GetMass()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Accoutrement](/docs/reference/engine/classes/Accoutrement)

English

Feedback

Engine Class

Accoutrement

An object that can attach to a player's character.

---

Summary

Properties

|  |
| --- |
| [AttachmentForward](#AttachmentForward):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [AttachmentPoint](#AttachmentPoint):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [AttachmentPos](#AttachmentPos):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [AttachmentRight](#AttachmentRight):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [AttachmentUp](#AttachmentUp):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Accessory](/docs/reference/engine/classes/Accessory), [Hat](/docs/reference/engine/classes/Hat)

An Accoutrement welds its child [part](/docs/reference/engine/classes/Part) called "Handle" to the
player's character. You can change the position and rotation of the Handle
part using the [AttachmentPos](/docs/reference/engine/classes/Accoutrement#AttachmentPos),
[Right](/docs/reference/engine/classes/Accoutrement#AttachmentRight),
[Forward](/docs/reference/engine/classes/Accoutrement#AttachmentForward), and
[Up](/docs/reference/engine/classes/Accoutrement#AttachmentUp) properties.

Parts descending from an accoutrement are massless when attach to other parts
(e.g. with a Weld) as long as they are not the root part of the assembly that
[GetRootPart()](/docs/reference/engine/classes/BasePart#GetRootPart) returns.
[GetMass()](/docs/reference/engine/classes/BasePart#GetMass) returns 0 for parts in this case, and it
doesn't add to the total mass or rotational inertia of the Assembly.

This doesn't apply to a part descending from an accoutrement when an
accoutrement welds to another part that is massless or one if its parts
otherwise becomes root. This also doesn't apply for the root part, and it has
mass like a normal part.

---

API Reference

Properties

AttachmentForward

Hidden

Not Replicated

Read Parallel

Sets the offset position of the object on the Player.

Accoutrement.AttachmentForward:[Vector3](/docs/reference/engine/datatypes/Vector3)

Sets the offset position of the object on the Player.

Provide feedback

---

AttachmentPoint

Read Parallel

The exact CFrame of the Accoutrement.

Accoutrement.AttachmentPoint:[CFrame](/docs/reference/engine/datatypes/CFrame)

The exact CFrame of the Accoutrement.

Provide feedback

---

AttachmentPos

Hidden

Not Replicated

Read Parallel

Sets the position of the object on the Player.

Accoutrement.AttachmentPos:[Vector3](/docs/reference/engine/datatypes/Vector3)

Sets the position of the object on the Player.

Provide feedback

---

AttachmentRight

Hidden

Not Replicated

Read Parallel

Sets the offset position of the object on the Player.

Accoutrement.AttachmentRight:[Vector3](/docs/reference/engine/datatypes/Vector3)

Sets the offset position of the object on the Player.

Provide feedback

---

AttachmentUp

Hidden

Not Replicated

Read Parallel

Sets the offset position of the object on the Player.

Accoutrement.AttachmentUp:[Vector3](/docs/reference/engine/datatypes/Vector3)

Sets the offset position of the object on the Player.

Provide feedback

---