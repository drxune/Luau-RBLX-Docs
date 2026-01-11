# TweenInfo | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/TweenInfo
Scraped: 2026-01-11T02:41:38.427848Z

## Inherits
- Tweens
- TweenService:Create()
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [TweenInfo](/docs/reference/engine/datatypes/TweenInfo)

English

Feedback

Engine Data Type

TweenInfo

Stores parameters for [Tweens](/docs/reference/engine/classes/Tween).

---

Summary

Constructors

|  |
| --- |
| [new](#new)(time: [number](/docs/luau/numbers),easingStyle: [Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle),easingDirection: [Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection),repeatCount: [number](/docs/luau/numbers),reverses: [boolean](/docs/luau/booleans),delayTime: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [EasingDirection](#EasingDirection):[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection) |
| [Time](#Time):[number](/docs/luau/numbers) |
| [DelayTime](#DelayTime):[number](/docs/luau/numbers) |
| [RepeatCount](#RepeatCount):[number](/docs/luau/numbers) |
| [EasingStyle](#EasingStyle):[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle) |
| [Reverses](#Reverses):[boolean](/docs/luau/booleans) |

The [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) data type stores parameters for
[TweenService:Create()](/docs/reference/engine/classes/TweenService#Create) to specify the behavior of the tween. The
properties of a [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) cannot be written to after its creation.

---

API Reference

Constructors

new

Creates a new [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) from the provided parameters.

TweenInfo.new(

time:[number](/docs/luau/numbers), easingStyle:[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle), easingDirection:[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection), repeatCount:[number](/docs/luau/numbers), reverses:[boolean](/docs/luau/booleans), delayTime:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers) Default Value: 1 Duration for the tween, in seconds. |
| easingStyle:[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle) Default Value: Enum.EasingStyle.Quad Easing style for the tween. |
| easingDirection:[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection) Default Value: Enum.EasingDirection.Out The direction in which the tween executes. |
| repeatCount:[number](/docs/luau/numbers) Default Value: 0 Number of times the tween should repeat. -1 repeats indefinitely. |
| reverses:[boolean](/docs/luau/booleans) Default Value: false Whether the tween should reverse to the starting values once it reaches its targets. |
| delayTime:[number](/docs/luau/numbers) Default Value: 0 Time of delay until the tween begins, in seconds. |

Creates a new [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) from the provided parameters.

Provide feedback

---

Properties

EasingDirection

The direction in which the tween executes.

TweenInfo.EasingDirection:[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection)

The direction in which the tween executes.

Provide feedback

---

Time

Duration of the tween, in seconds.

TweenInfo.Time:[number](/docs/luau/numbers)

Duration of the tween, in seconds.

Provide feedback

---

DelayTime

Time of delay until the tween begins, in seconds.

TweenInfo.DelayTime:[number](/docs/luau/numbers)

Time of delay until the tween begins, in seconds.

Provide feedback

---

RepeatCount

Number of times the tween repeats.

TweenInfo.RepeatCount:[number](/docs/luau/numbers)

Number of times the tween repeats. -1 indicates indefinite repetition.

Provide feedback

---

EasingStyle

The style in which the tween executes.

TweenInfo.EasingStyle:[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle)

The style in which the tween executes.

Provide feedback

---

Reverses

Whether or not the tween interpolates in reverse tween once the initial
tween completes.

TweenInfo.Reverses:[boolean](/docs/luau/booleans)

Whether or not the tween interpolates in reverse tween once the initial
tween completes.

Provide feedback

---