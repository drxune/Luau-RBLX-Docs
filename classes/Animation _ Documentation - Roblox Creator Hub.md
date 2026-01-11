# Animation | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Animation
Scraped: 2026-01-11T02:31:44.098111Z

## Inherits
- Object
- Instance
- Animation
- AnimationController
- AnimationId
- AnimationTracks
- Animator
- Humanoid
- Player.Character
- AnimationTrack
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Animation](/docs/reference/engine/classes/Animation)

English

Feedback

Engine Class

![Animation](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Animation-Dark.webp)Animation

References an animation asset which can be loaded by an
[AnimationController](/docs/reference/engine/classes/AnimationController).

---

Summary

Properties

|  |
| --- |
| [AnimationId](#AnimationId):ContentId |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object that references an animation asset
([AnimationId](/docs/reference/engine/classes/Animation#AnimationId)) which can be loaded by an
[AnimationController](/docs/reference/engine/classes/AnimationController).

#### Loading an Animation on Client or Server

In order for [AnimationTracks](/docs/reference/engine/classes/AnimationTrack) to replicate correctly,
it's important to know when they should be loaded on the client or on the
server:

* If an [Animator](/docs/reference/engine/classes/Animator) is a descendant of a [Humanoid](/docs/reference/engine/classes/Humanoid) or
  [AnimationController](/docs/reference/engine/classes/AnimationController) in a player's [Player.Character](/docs/reference/engine/classes/Player#Character),
  animations started on that player's client will be replicated to the server
  and other clients.
* If the [Animator](/docs/reference/engine/classes/Animator) is not a descendant of a player character, its
  animations must be loaded and started on the server to replicate.

The [Animator](/docs/reference/engine/classes/Animator) object must be initially created on the server and
replicated to clients for animation replication to work at all. If an
[Animator](/docs/reference/engine/classes/Animator) is created locally, then
[AnimationTracks](/docs/reference/engine/classes/AnimationTrack) loaded with that [Animator](/docs/reference/engine/classes/Animator) will
not replicate.

See also [Animation Editor](/docs/animation/editor) and
[Using Animations](/docs/animation/using) to learn how to create and add
pre-built or custom animations to your game.

---

API Reference

Properties

AnimationId

Read Parallel

Asset ID of the animation an [Animation](/docs/reference/engine/classes/Animation) object is referencing.

Animation.AnimationId:ContentId

This property is the asset ID of the animation an [Animation](/docs/reference/engine/classes/Animation) object
is referencing. Once an animation has been created and uploaded to Roblox,
the ID can be copied from the
[Creator Dashboard](https://create.roblox.com/dashboard/creations?activeTab=Animation).

Note that the animation will need to be loaded onto an
[AnimationTrack](/docs/reference/engine/classes/AnimationTrack) in order to play it.

Provide feedback

---