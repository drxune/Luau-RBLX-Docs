# Dialog | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Dialog
Scraped: 2026-01-11T02:40:28.619336Z

## Inherits
- Object
- Instance
- Dialog
- DialogChoice
- Dialog.GoodbyeDialog
- Player
- LocalScript
- ModuleScript
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Dialog](/docs/reference/engine/classes/Dialog)

English

Feedback

Engine Class

![Dialog](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Dialog-Dark.webp)Dialog

Creates NPC billboard-style dialog bubbles.

---

Summary

Properties

|  |
| --- |
| [BehaviorType](#BehaviorType):[Enum.DialogBehaviorType](/docs/reference/engine/enums/DialogBehaviorType) |
| [ConversationDistance](#ConversationDistance):[number](/docs/luau/numbers) |
| [GoodbyeChoiceActive](#GoodbyeChoiceActive):[boolean](/docs/luau/booleans) |
| [GoodbyeDialog](#GoodbyeDialog):[string](/docs/luau/strings) |
| [InitialPrompt](#InitialPrompt):[string](/docs/luau/strings) |
| [InUse](#InUse):[boolean](/docs/luau/booleans) |
| [Purpose](#Purpose):[Enum.DialogPurpose](/docs/reference/engine/enums/DialogPurpose) |
| [Tone](#Tone):[Enum.DialogTone](/docs/reference/engine/enums/DialogTone) |
| [TriggerDistance](#TriggerDistance):[number](/docs/luau/numbers) |
| [TriggerOffset](#TriggerOffset):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [GetCurrentPlayers](#GetCurrentPlayers)():Instances |

Events

|  |
| --- |
| [DialogChoiceSelected](#DialogChoiceSelected)(player: [Instance](/docs/reference/engine/datatypes/Instance),dialogChoice: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Dialog object allows users to create non-player characters (NPCs) that
players can talk to using a list of choices. The Dialog object can be inserted
into a part such as a Humanoid's head, and then a player will see a speech
bubble above the part that they can click on to start a conversation. The
creator of a place can choose what choices the player can say by inserting
[DialogChoice](/docs/reference/engine/classes/DialogChoice) objects into the dialog.

---

API Reference

Properties

BehaviorType

Read Parallel

Sets whether the Dialog can be used by multiple players at once.

Dialog.BehaviorType:[Enum.DialogBehaviorType](/docs/reference/engine/enums/DialogBehaviorType)

The BehaviorType of a Dialog determines whether multiple players can
interact with a dialog at once. The default value for this property is
SinglePlayer.

#### SinglePlayer

When a Dialog is configured to SinglePlayer, only one player can interact
with it at a time. As soon as a player engages with a dialog, other
players will not be able to initiate the dialog until the first player is
finished.

While a player is engaged with a dialog, the other players will see the
dialog choices of the player who started the dialog, along with the
responses.

#### MultiplePlayers

When a Dialog is set to MultiplePlayers, any player can initiate a dialog
at any time, even if another player has already initiated the dialog.
Unlike SinglePlayer however, Dialogs set to MultiplePlayers will not show
the dialog choices and responses to anyone but the player in the
conversation.

```
local Workspace = game:GetService("Workspace")



local singlePlayerDialog = Instance.new("Dialog")



local singlePlayerPart = Workspace.SinglePlayerPart



singlePlayerDialog.BehaviorType = Enum.DialogBehaviorType.SinglePlayer



singlePlayerDialog.InitialPrompt = "Only one person can interact with me at once."



singlePlayerDialog.Parent = singlePlayerPart



local multiplePlayersDialog = Instance.new("Dialog")



local multiplePlayersPart = Workspace.MultiplePlayersPart



multiplePlayersDialog.BehaviorType = Enum.DialogBehaviorType.MultiplePlayers



multiplePlayersDialog.InitialPrompt = "Any number of players can interact with me at once."



multiplePlayersDialog.Parent = multiplePlayersPart
```

Provide feedback

---

ConversationDistance

Read Parallel

The furthest distance that a player can be from the Dialog's parent to
start a conversation.

Dialog.ConversationDistance:[number](/docs/luau/numbers)

The furthest distance that a player can be from the Dialog's parent to
start a conversation.

Provide feedback

---

GoodbyeChoiceActive

Read Parallel

Toggles whether the goodbye option will be displayed.

Dialog.GoodbyeChoiceActive:[boolean](/docs/luau/booleans)

Toggles whether the goodbye option will be displayed. If true, the dialog
will display the content of [Dialog.GoodbyeDialog](/docs/reference/engine/classes/Dialog#GoodbyeDialog) as the last
option after other dialog choices. Clicking on the goodbye option will
exit the dialog.

Provide feedback

---

GoodbyeDialog

Read Parallel

Sets the sentence that the dialog will show to the player when the chat
ends.

Dialog.GoodbyeDialog:[string](/docs/luau/strings)

Sets the sentence that the dialog will show to the player when the chat
ends

Provide feedback

---

InitialPrompt

Read Parallel

Sets the first sentence that the dialog will show to the player, once a
chat is commenced.

Dialog.InitialPrompt:[string](/docs/luau/strings)

Sets the first sentence that the dialog will show to the player, once a
chat is commenced.

Provide feedback

---

InUse

Read Parallel

If true, this dialog is being used by at least one player.

Dialog.InUse:[boolean](/docs/luau/booleans)

If true, this dialog is being used by at least one player.

Provide feedback

---

Purpose

Read Parallel

Sets the icon that the initial dialog displays.

Dialog.Purpose:[Enum.DialogPurpose](/docs/reference/engine/enums/DialogPurpose)

Sets the icon that the initial dialog displays.

Provide feedback

---

Tone

Read Parallel

Sets the color of the NPC's speech bubble.

Dialog.Tone:[Enum.DialogTone](/docs/reference/engine/enums/DialogTone)

Sets the color of the NPC's speech bubble.

Provide feedback

---

TriggerDistance

Read Parallel

Sets the maximum distance that a dialog can be triggered from.

Dialog.TriggerDistance:[number](/docs/luau/numbers)

Sets the maximum distance that a dialog can be triggered from.

Provide feedback

---

TriggerOffset

Read Parallel

Sets the offset of the dialog relative to the dialog's parent.

Dialog.TriggerOffset:[Vector3](/docs/reference/engine/datatypes/Vector3)

Sets the offset of the dialog relative to the dialog's parent.

Provide feedback

---

Methods

GetCurrentPlayers

Returns a list of players currently using the Dialog.

Dialog:GetCurrentPlayers():Instances

Returns

Instances

The GetCurrentPlayers function of a Dialog will return a list of
[Player](/docs/reference/engine/classes/Player) currently using the Dialog. If there are no players using
the dialog then the returned list will be empty.

Code Samples

Dialog:GetCurrentPlayers

```
local dialog = script.Parent



local function onChoiceSelected(_player, _choice)



local currentPlayers = dialog:GetCurrentPlayers()



print("The current players in the dialog:")



for _, player in ipairs(currentPlayers) do



print(player)



end



end



dialog.DialogChoiceSelected:Connect(onChoiceSelected)
```

Provide feedback

---

Events

DialogChoiceSelected

Fired when a player chooses something to say, through a [Dialog](/docs/reference/engine/classes/Dialog)
instance.

Dialog.DialogChoiceSelected(

player:[Instance](/docs/reference/engine/datatypes/Instance), dialogChoice:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance) |
| dialogChoice:[Instance](/docs/reference/engine/datatypes/Instance) |

Fired when a player chooses something to say, through a [Dialog](/docs/reference/engine/classes/Dialog)
instance.

This event is client-side only and will not fire on the server. It should
be connected to in either a [LocalScript](/docs/reference/engine/classes/LocalScript) or a [ModuleScript](/docs/reference/engine/classes/ModuleScript)
required by a [LocalScript](/docs/reference/engine/classes/LocalScript).

Provide feedback

---