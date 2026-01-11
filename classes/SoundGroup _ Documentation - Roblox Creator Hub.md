# SoundGroup | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SoundGroup
Scraped: 2026-01-11T02:32:33.307002Z

## Inherits
- Object
- Instance
- SoundGroup
- Sounds
- Volume
- Sound
- SoundEffects
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [SoundGroup](/docs/reference/engine/classes/SoundGroup)

English

Feedback

Engine Class

![SoundGroup](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SoundGroup-Dark.webp)SoundGroup

A [SoundGroup](/docs/reference/engine/classes/SoundGroup) is used to manage the volume and sound effects on
multiple [Sounds](/docs/reference/engine/classes/Sound) at once. [Sounds](/docs/reference/engine/classes/Sound) in the SoundGroup
will have their volume and effects adjusted by the SoundGroup.

---

Summary

Properties

|  |
| --- |
| [Volume](#Volume):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [SoundGroup](/docs/reference/engine/classes/SoundGroup) is used to manage the volume and effects on multiple
[Sounds](/docs/reference/engine/classes/Sound) at once. Every sound in the sound group will have its
volume adjusted by the group's [Volume](/docs/reference/engine/classes/SoundGroup#Volume) property which
acts as a multiplier, meaning a [Sound](/docs/reference/engine/classes/Sound) with volume 0.5 assigned to a
[SoundGroup](/docs/reference/engine/classes/SoundGroup) with a volume of 0.5 will have an effective volume of
0.25.

If the [SoundGroup](/docs/reference/engine/classes/SoundGroup) has any [SoundEffects](/docs/reference/engine/classes/SoundEffect) as
children, those effects will be applied to all of the [Sounds](/docs/reference/engine/classes/Sound) in
the group.

Note that a [Sound](/docs/reference/engine/classes/Sound) must be added to a [SoundGroup](/docs/reference/engine/classes/SoundGroup) by setting its
[SoundGroup](/docs/reference/engine/classes/Sound#SoundGroup) property, not by simply parenting the
[Sound](/docs/reference/engine/classes/Sound) to the [SoundGroup](/docs/reference/engine/classes/SoundGroup). A [Sound](/docs/reference/engine/classes/Sound) can only belong to
one [SoundGroup](/docs/reference/engine/classes/SoundGroup) at a time, although you can nest groups as outlined
[here](/docs/sound/groups#nesting-soundgroups).

See [Sound Groups](/docs/sound/groups) for further details on working
with the [SoundGroup](/docs/reference/engine/classes/SoundGroup) class.

---

API Reference

Properties

Volume

Read Parallel

The volume multiplier applied to [Sounds](/docs/reference/engine/classes/Sound) that are in the
[SoundGroup](/docs/reference/engine/classes/SoundGroup).

SoundGroup.Volume:[number](/docs/luau/numbers)

The volume multiplier applied to [Sounds](/docs/reference/engine/classes/Sound) which belong to the
[SoundGroup](/docs/reference/engine/classes/SoundGroup). Value can range from 0 to 10.

Code Samples

SoundGroups

This sample demonstrates how a SoundGroup can be used to change the volume of
its associated Sounds and apply SoundEffects.

In this example a Sound is instanced in the Workspace and assigned to a new
SoundGroup. The Sound is played and during playback the volume is changed via
the SoundGroup and a SoundEffect is added.

```
local SoundService = game:GetService("SoundService")



-- create a sound group



local soundGroup = Instance.new("SoundGroup")



soundGroup.Parent = SoundService



-- create a sound



local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



sound.Looped = true



sound.PlaybackSpeed = 2



sound.SoundGroup = soundGroup



sound.Parent = workspace



-- play the sound



sound:Play()



task.wait(10)



-- change the volume



soundGroup.Volume = 0.1



task.wait(3)



-- return the volume



soundGroup.Volume = 0.5



task.wait(4)



-- add a sound effect



local reverb = Instance.new("ReverbSoundEffect")



reverb.Parent = soundGroup
```

Provide feedback

---