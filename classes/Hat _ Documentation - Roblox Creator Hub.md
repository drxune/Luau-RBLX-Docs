# Hat | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Hat
Scraped: 2026-01-11T02:37:19.952733Z

## Inherits
- Accoutrement
- Hat
- Accessory
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Accoutrement](/docs/reference/engine/classes/Accoutrement)
6. /
7. [Hat](/docs/reference/engine/classes/Hat)

English

Feedback

Engine Class

Hat

Deprecated

This class has been superseded by the [Accessory](/docs/reference/engine/classes/Accessory) class. Do not use it
for new work.

---

Summary

Inherited Members

5 inherited from [Accoutrement](/docs/reference/engine/classes/Accoutrement)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Code Samples

Manually Position Hats

You can use this code to manually position hats on the character:

```
local hat = script.Parent



local character = hat.Parent



hat.Handle.CFrame = character.Head.CFrame * CFrame.new(0, character.Head.Size.Y / 2, 0) * hat.AttachmentPoint:inverse()
```