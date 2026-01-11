# ProximityPromptService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ProximityPromptService
Scraped: 2026-01-11T02:28:24.887925Z

## Tags
- Service

## Inherits
- Instance
- ProximityPromptService
- ProximityPrompt
- Player
- Object
- ProximityPrompts
- KeyboardKeyCode
- HoldDuration
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ProximityPromptService](/docs/reference/engine/classes/ProximityPromptService)

English

Feedback

Engine Class

ProximityPromptService

Allows developers to interact with [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) objects in a global
way.

Service

Not Browsable

---

Summary

Properties

|  |
| --- |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [MaxIndicatorsVisible](#MaxIndicatorsVisible):[number](/docs/luau/numbers) |
| [MaxPromptsVisible](#MaxPromptsVisible):[number](/docs/luau/numbers) |

Events

|  |
| --- |
| [IndicatorHidden](#IndicatorHidden)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [IndicatorShown](#IndicatorShown)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptButtonHoldBegan](#PromptButtonHoldBegan)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt),playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptButtonHoldEnded](#PromptButtonHoldEnded)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt),playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptHidden](#PromptHidden)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptShown](#PromptShown)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt),inputType: [Enum.ProximityPromptInputType](/docs/reference/engine/enums/ProximityPromptInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptTriggered](#PromptTriggered)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt),playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptTriggerEnded](#PromptTriggerEnded)(prompt: [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt),playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

ProximityPromptService allows developers to interact with
[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) objects in a global way. It may be more convenient to
listen to events through this service rather than on individual
[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) objects.

---

API Reference

Properties

Enabled

Read Parallel

Whether [ProximityPrompts](/docs/reference/engine/classes/ProximityPrompt) are enabled, and
therefore shown, in-experience.

ProximityPromptService.Enabled:[boolean](/docs/luau/booleans)

This property determines whether [ProximityPrompts](/docs/reference/engine/classes/ProximityPrompt)
are enabled, and therefore shown, in-experience. When false, no prompts
will be shown.

For example, in a round-based system, you can disable prompts at certain
points in the experience to disable proximity-based interactions:

```
local ProximityPromptService = game:GetService("ProximityPromptService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local enablePrompts = ReplicatedStorage:FindFirstChild("EnablePrompts") -- BindableEvent



-- Connect to the BindableEvent and fire from another script controlling experience logic



enablePrompts.OnServerEvent:Connect(function(enabled)



ProximityPromptService.Enabled = enabled



end)
```

Provide feedback

---

MaxIndicatorsVisible

Read Parallel

ProximityPromptService.MaxIndicatorsVisible:[number](/docs/luau/numbers)

Provide feedback

---

MaxPromptsVisible

Read Parallel

Maximum number of [ProximityPrompts](/docs/reference/engine/classes/ProximityPrompt) that will be
shown to the player.

ProximityPromptService.MaxPromptsVisible:[number](/docs/luau/numbers)

This property indicates the maximum number of
[ProximityPrompts](/docs/reference/engine/classes/ProximityPrompt) that will be shown to the player.

Provide feedback

---

Events

IndicatorHidden

ProximityPromptService.IndicatorHidden(prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) |

Provide feedback

---

IndicatorShown

ProximityPromptService.IndicatorShown(prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) |

Provide feedback

---

PromptButtonHoldBegan

Triggers when the player begins holding down the
[KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode) key/button on a
prompt with a non-zero [HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration).

ProximityPromptService.PromptButtonHoldBegan(

prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt), playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)  The prompt that the player begins interacting with. |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The player who holds the key/button. |

This event triggers when the player begins holding down the
[KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode) key/button on a
prompt with a non-zero [HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration).

Provide feedback

---

PromptButtonHoldEnded

Triggers when the player stops holding down the
[KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode) key/button on a
prompt with a non-zero [HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration).

ProximityPromptService.PromptButtonHoldEnded(

prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt), playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)  The prompt that the player stops interacting with. |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The player who releases the held key/button. |

This event triggers when the player stops holding down the
[KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode) key/button on a
prompt with a non-zero [HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration).

Provide feedback

---

PromptHidden

Triggers client-side when a prompt becomes hidden.

ProximityPromptService.PromptHidden(prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)  The prompt instance that becomes hidden. |

This event triggers client-side in connected local scripts when a prompt
becomes hidden.

Provide feedback

---

PromptShown

Triggers client-side when a prompt becomes visible.

ProximityPromptService.PromptShown(

prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt), inputType:[Enum.ProximityPromptInputType](/docs/reference/engine/enums/ProximityPromptInputType)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)  The prompt instance that becomes visible. |
| inputType:[Enum.ProximityPromptInputType](/docs/reference/engine/enums/ProximityPromptInputType)  The input that triggered the event. |

This event triggers client-side in connected local scripts when a prompt
becomes visible.

Provide feedback

---

PromptTriggered

Triggers when the user interacts with this prompt.

ProximityPromptService.PromptTriggered(

prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt), playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)  The prompt that the player interacts with. |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The interacting player. |

This event triggers when the player completes interaction with a prompt,
either when the [KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode)
key/button is pressed, or after a specified amount of time holding the
key/button if the prompt's
[HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration) is non-zero.

Provide feedback

---

PromptTriggerEnded

Triggers when the player stops holding down the
[KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode) key/button while
triggering a prompt.

ProximityPromptService.PromptTriggerEnded(

prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt), playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| prompt:[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)  The prompt that the player stops interacting with. |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The player that releases the key/button. |

This event triggers when the player stops holding down the
[KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode) key/button while
triggering a prompt. This is intended to allow interactions which require
the player to hold a key/button while something happens in-experience.

Provide feedback

---