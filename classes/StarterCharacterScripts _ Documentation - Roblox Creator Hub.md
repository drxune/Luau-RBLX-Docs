# StarterCharacterScripts | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StarterCharacterScripts
Scraped: 2026-01-11T02:32:45.967832Z

## Tags
- Not Creatable

## Inherits
- StarterPlayerScripts
- StarterCharacterScripts
- Instance
- Object
- Player.Character
- LocalScript
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts)
6. /
7. [StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts)

English

Feedback

Engine Class

![StarterCharacterScripts](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StarterCharacterScripts-Dark.webp)StarterCharacterScripts

Stores instances to be parented to a player's character when it spawns.

Not Creatable

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts) container stores scripts to be parented to
a player's [Player.Character](/docs/reference/engine/classes/Player#Character) when it spawns. Unlike scripts stored in
the [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts) folder, these scripts will not persist when
the character respawns.

If a [LocalScript](/docs/reference/engine/classes/LocalScript) named Animate, Sound, or Health is placed in
this container, it will replace the default script that manages character
animations, character sounds, and character health regeneration respectively.