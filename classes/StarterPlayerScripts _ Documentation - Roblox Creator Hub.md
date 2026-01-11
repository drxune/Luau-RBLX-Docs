# StarterPlayerScripts | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StarterPlayerScripts
Scraped: 2026-01-11T02:40:37.945638Z

## Tags
- Not Creatable

## Inherits
- Instance
- StarterPlayerScripts
- Object
- StarterCharacterScripts
- StarterPlayer
- LocalScripts
- PlayerScripts
- Player
- LocalScript
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts)

English

Feedback

Engine Class

StarterPlayerScripts

A container for objects to be copied to a Player's PlayerScripts when they
join a game.

Not Creatable

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts)

[StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts) is a container object located within the
[StarterPlayer](/docs/reference/engine/classes/StarterPlayer) service. It can contain [LocalScripts](/docs/reference/engine/classes/LocalScript)
and other objects to be copied to the [PlayerScripts](/docs/reference/engine/classes/PlayerScripts) container once
when a [Player](/docs/reference/engine/classes/Player) joins the game. For example, if you want to create
special effects on the client when certain conditions are met, you can place a
[LocalScript](/docs/reference/engine/classes/LocalScript) within this container to do that.

When an experience is run, this object will also house the default
multi-platform Roblox control scripts for the camera and character. If
[LocalScripts](/docs/reference/engine/classes/LocalScript) named CameraScript or ControlScript are
placed within this container, they will replace the Roblox defaults for
those scripts respectively. If desired, you can add empty
[LocalScripts](/docs/reference/engine/classes/LocalScript) for each of these to disable them altogether;
this is useful for experiences that do not follow the typical control
paradigms of a Roblox experience.