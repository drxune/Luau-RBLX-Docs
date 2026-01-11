# DialogChoice | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DialogChoice
Scraped: 2026-01-11T02:31:47.795768Z

## Inherits
- Object
- Instance
- DialogChoice
- DialogChoice.GoodbyeDialog
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DialogChoice](/docs/reference/engine/classes/DialogChoice)

English

Feedback

Engine Class

![DialogChoice](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/DialogChoice-Dark.webp)DialogChoice

Used to craft the further choices available to players who have started a
dialog conversation with an NPC.

---

Summary

Properties

|  |
| --- |
| [GoodbyeChoiceActive](#GoodbyeChoiceActive):[boolean](/docs/luau/booleans) |
| [GoodbyeDialog](#GoodbyeDialog):[string](/docs/luau/strings) |
| [ResponseDialog](#ResponseDialog):[string](/docs/luau/strings) |
| [UserDialog](#UserDialog):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Used to craft the further choices available to players who have started a
dialog conversation with an NPC.

---

API Reference

Properties

GoodbyeChoiceActive

Read Parallel

Toggles whether the goodbye option will be displayed.

DialogChoice.GoodbyeChoiceActive:[boolean](/docs/luau/booleans)

Toggles whether the goodbye option will be displayed. If true, the dialog
will display the content of [DialogChoice.GoodbyeDialog](/docs/reference/engine/classes/DialogChoice#GoodbyeDialog) as the last
option after other dialog choices. Clicking on the goodbye option will
exit the dialog.

Provide feedback

---

GoodbyeDialog

Read Parallel

Sets the sentence that the dialog will show to the player when the chat
ends.

DialogChoice.GoodbyeDialog:[string](/docs/luau/strings)

Sets the sentence that the dialog will show to the player when the chat
ends

Provide feedback

---

ResponseDialog

Read Parallel

Sets what the NPC will say when the player chooses this DialogChoice.

DialogChoice.ResponseDialog:[string](/docs/luau/strings)

Sets what the NPC will say when the player chooses this DialogChoice.

Provide feedback

---

UserDialog

Read Parallel

Sets what the player will say when they choose this DialogChoice.

DialogChoice.UserDialog:[string](/docs/luau/strings)

Sets what the player will say when they choose this DialogChoice.

Provide feedback

---