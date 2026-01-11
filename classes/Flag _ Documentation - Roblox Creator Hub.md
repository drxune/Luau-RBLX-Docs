# Flag | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Flag
Scraped: 2026-01-11T02:30:02.479582Z

## Inherits
- Tool
- Flag
- FlagStand
- BackpackItem
- Model
- PVInstance
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Tool](/docs/reference/engine/classes/Tool)
6. /
7. [Flag](/docs/reference/engine/classes/Flag)

English

Feedback

Engine Class

Flag

Deprecated

The Flag object helps you make 'capture the flag' style games.

The [Flag](/docs/reference/engine/classes/Flag) and [FlagStand](/docs/reference/engine/classes/FlagStand) objects were created to allow
developers to make 'capture the flag' style games quickly. However they have
been deprecated and developers are advised to design their own systems which
will be more flexible and reliable.

---

Summary

Properties

|  |
| --- |
| [TeamColor](#TeamColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |

Inherited Members

16 inherited from [Tool](/docs/reference/engine/classes/Tool)

2 inherited from [BackpackItem](/docs/reference/engine/classes/BackpackItem)

26 inherited from [Model](/docs/reference/engine/classes/Model)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Flag is a unit spawned with a [FlagStand](/docs/reference/engine/classes/FlagStand) object, and will respawn
when captured. When a player touches this object's Handle, which must be a
child of the Flag object, which is a Part named "Handle", the flag will be
added to the player's backpack and will appear in their hand. A player cannot
select other weapons while carrying a flag, and can drop the flag at anytime
by pressing "Backspace" on the keyboard. If the player carrying a flag steps
onto another FlagStand of a different team color, the flag will be removed
from the player's backpack and a point will be added to the user's
leaderstats, if provided. The flag will then regenerate at the originating
flag stand.

---

API Reference

Properties

TeamColor

Deprecated

Show details

---