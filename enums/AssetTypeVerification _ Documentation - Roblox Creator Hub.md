# AssetTypeVerification | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AssetTypeVerification
Scraped: 2026-01-11T02:44:15.600846Z

## Inherits
- Humanoid:ApplyDescription()
- Players:CreateHumanoidModelFromDescription()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)

English

Feedback

Engine Enum

AssetTypeVerification

---

Determines the asset type verification mode used when calling
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription) or
[Players:CreateHumanoidModelFromDescription()](/docs/reference/engine/classes/Players#CreateHumanoidModelFromDescription). This verification mode
determines if the method will load models or not. Loading models can be
insecure if it's possible for malicious users to trick your game into loading
unexpected models that you own which may include malicious scripts. You should
set this to Always unless you want to load non-catalog assets.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 1 | Use the default behavior for asset type verification. |
| ClientOnly | 2 | Only verify asset types on the client. Asset type verification can not be turned off on the client. |
| Always | 3 | Always verify the asset types to be loaded and disallow loading models. |