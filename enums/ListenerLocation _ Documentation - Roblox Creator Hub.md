# ListenerLocation | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ListenerLocation
Scraped: 2026-01-11T02:44:18.260282Z

## Inherits
- SoundService.DefaultListenerLocation
- AudioListener
- VoiceChatService.EnableDefaultVoice
- VoiceChatService.UseAudioApi
- Attachment
- PrimaryPart
- Character
- AudioDeviceOutput
- SoundService
- Wire
- SourceInstance
- TargetInstance
- Workspace.CurrentCamera
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ListenerLocation](/docs/reference/engine/enums/ListenerLocation)

English

Feedback

Engine Enum

ListenerLocation

---

Enum used with [SoundService.DefaultListenerLocation](/docs/reference/engine/classes/SoundService#DefaultListenerLocation) to determine where
an [AudioListener](/docs/reference/engine/classes/AudioListener) is placed by default.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Behavior depends on the value of [VoiceChatService.EnableDefaultVoice](/docs/reference/engine/classes/VoiceChatService#EnableDefaultVoice) and [VoiceChatService.UseAudioApi](/docs/reference/engine/classes/VoiceChatService#UseAudioApi). When using the default voice setup with the audio API, this behaves similarly to Camera. |
| None | 1 | No [AudioListener](/docs/reference/engine/classes/AudioListener) will be created by default, but they can be created separately by scripts. |
| Character | 2 | All of the following, resulting in the world being heard from the position of your character while matching the orientation of your camera.   * An [Attachment](/docs/reference/engine/classes/Attachment) will be created and parented to the   [PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) of the local player's   [Character](/docs/reference/engine/classes/Player#Character) model. * An [AudioListener](/docs/reference/engine/classes/AudioListener) will be created and parented to the   [Attachment](/docs/reference/engine/classes/Attachment). * An [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) will be created and parented to   [SoundService](/docs/reference/engine/classes/SoundService). * A [Wire](/docs/reference/engine/classes/Wire) will be created and parented to the previously-created   [AudioListener](/docs/reference/engine/classes/AudioListener). The wire's   [SourceInstance](/docs/reference/engine/classes/Wire#SourceInstance) will be set to the   previously-created [AudioListener](/docs/reference/engine/classes/AudioListener) and its   [TargetInstance](/docs/reference/engine/classes/Wire#TargetInstance) will be set to the   previously-created [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput). * The previously-created [Attachment](/docs/reference/engine/classes/Attachment) will be updated once per frame   to face the same direction as [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). |
| Camera | 3 | All of the following, resulting in the world being heard from the perspective (postition and orientation) of the camera.   * An [AudioListener](/docs/reference/engine/classes/AudioListener) will be created and parented to   [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). * An [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) will be created and parented to   [SoundService](/docs/reference/engine/classes/SoundService). * A [Wire](/docs/reference/engine/classes/Wire) will be created and parented to the previously-created   [AudioListener](/docs/reference/engine/classes/AudioListener). The wire's   [SourceInstance](/docs/reference/engine/classes/Wire#SourceInstance) will be set to the   previously-created [AudioListener](/docs/reference/engine/classes/AudioListener) and its   [TargetInstance](/docs/reference/engine/classes/Wire#TargetInstance) will be set to the   previously-created [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput). |