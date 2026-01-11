# VoiceChatService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VoiceChatService
Scraped: 2026-01-11T02:27:55.831953Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- VoiceChatService
- Object
- AudioDeviceInput
- AudioEmitter
- EnableDefaultVoice
- UseAudioApi
- AudioEmitters
- Player
- Player.Character
- AudioListener
- Workspace.CurrentCamera
- VoiceChatService.EnableDefaultVoice
- Player.UserId
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [VoiceChatService](/docs/reference/engine/classes/VoiceChatService)

English

Feedback

Engine Class

![VoiceChatService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/VoiceChatService-Dark.webp)VoiceChatService

VoiceChatService is responsible for voice chat's high-level functionality.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [DefaultDistanceAttenuation](#DefaultDistanceAttenuation):[Enum.VoiceChatDistanceAttenuationType](/docs/reference/engine/enums/VoiceChatDistanceAttenuationType) |
| [EnableDefaultVoice](#EnableDefaultVoice):[boolean](/docs/luau/booleans) |
| [UseAudioApi](#UseAudioApi):[Enum.AudioApiRollout](/docs/reference/engine/enums/AudioApiRollout) |

Methods

|  |
| --- |
| [IsVoiceEnabledForUserIdAsync](#IsVoiceEnabledForUserIdAsync)(userId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

VoiceChatService is responsible for voice chat's high-level functionality.
This mostly consists of configuration options, and functions that are not
specifically-controlled by more-specific instances.

---

API Reference

Properties

DefaultDistanceAttenuation

Plugin Security

Read Parallel

Determines which distance attenuation curve the default voice chat setup
uses when [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) and [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) objects are
generated.

VoiceChatService.DefaultDistanceAttenuation:[Enum.VoiceChatDistanceAttenuationType](/docs/reference/engine/enums/VoiceChatDistanceAttenuationType)

This property controls the default distance attenuation curve assigned to
any generated [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) instances in the default voice chat
setup.

This property only has an effect if
[EnableDefaultVoice](/docs/reference/engine/classes/VoiceChatService#EnableDefaultVoice) and
[UseAudioApi](/docs/reference/engine/classes/VoiceChatService#UseAudioApi) are both enabled, since
no [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) are otherwise generated.

Provide feedback

---

EnableDefaultVoice

Plugin Security

Read Parallel

Controls whether each voice-eligible player can be heard as though they
were speaking through their character.

VoiceChatService.EnableDefaultVoice:[boolean](/docs/luau/booleans)

When enabled, each voice-eligible player can be heard as though they were
speaking through their character. The implementation details of the voice
setup depend on [UseAudioApi](/docs/reference/engine/classes/VoiceChatService#UseAudioApi).

When [UseAudioApi](/docs/reference/engine/classes/VoiceChatService#UseAudioApi) is
[Enabled](/docs/reference/engine/enums/AudioApiRollout), disabling this property disables the
default setup, but [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) will still work. Conversely,
when [UseAudioApi](/docs/reference/engine/classes/VoiceChatService#UseAudioApi) is
[Disabled](/docs/reference/engine/enums/AudioApiRollout), disabling the default voice setup
effectively disables voice chat altogether.

Provide feedback

---

UseAudioApi

Plugin Security

Read Parallel

Controls whether voice chat is represented and controlled by
[AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) objects.

VoiceChatService.UseAudioApi:[Enum.AudioApiRollout](/docs/reference/engine/enums/AudioApiRollout)

If [Enabled](/docs/reference/engine/enums/AudioApiRollout), the voice chat setup is represented and
controlled by [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) objects. More specifically:

* An [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) will be created and parented to each
  voice-eligible [Player](/docs/reference/engine/classes/Player).
* An [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) will be created and parented to each
  voice-eligible player's [Player.Character](/docs/reference/engine/classes/Player#Character).
* An [AudioListener](/docs/reference/engine/classes/AudioListener) will be created and parented to
  [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera).

You can disable the default setup by setting
[VoiceChatService.EnableDefaultVoice](/docs/reference/engine/classes/VoiceChatService#EnableDefaultVoice) to false.

If [Disabled](/docs/reference/engine/enums/AudioApiRollout), the voice chat setup is done through
an internal-only system.

Currently, setting this to [Automatic](/docs/reference/engine/enums/AudioApiRollout) has the same
meaning as [Disabled](/docs/reference/engine/enums/AudioApiRollout). However, in the future,
[Automatic](/docs/reference/engine/enums/AudioApiRollout) will become
[Enabled](/docs/reference/engine/enums/AudioApiRollout), so that new experiences can achieve
greater customization over voice.

Provide feedback

---

Methods

IsVoiceEnabledForUserIdAsync

Yields

Returns whether or not the given user has voice enabled.

VoiceChatService:IsVoiceEnabledForUserIdAsync(userId:[number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) to check. |

Returns

[boolean](/docs/luau/booleans)

If that user has voice enabled.

Returns whether or not the given user has voice enabled. On the
client-side, this can only be used to check the voice status of the local
player. On the server-side, this can only check the voice status for
players in that server.

This function can throw an error if the HTTP call fails.

```
local Players = game:GetService("Players")



local VoiceChatService = game:GetService("VoiceChatService")



local localPlayer = Players.LocalPlayer



local success, enabled = pcall(function()



return VoiceChatService:IsVoiceEnabledForUserIdAsync(localPlayer.UserId)



end)



if success and enabled then



print("Voice chat enabled!")



end
```

Provide feedback

---