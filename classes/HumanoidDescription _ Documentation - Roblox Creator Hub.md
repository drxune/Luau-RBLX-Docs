# HumanoidDescription | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HumanoidDescription
Scraped: 2026-01-11T02:35:51.663175Z

## Tags
- Not Replicated

## Inherits
- Instance
- HumanoidDescription
- Object
- Humanoid
- applied
- Shirt
- Pants
- ShirtGraphic
- Accessories
- Animations
- BodyColors
- Players:GetHumanoidDescriptionFromUserId()
- Players:GetHumanoidDescriptionFromOutfitId()
- Players:CreateHumanoidModelFromDescription()
- HumanoidDescription:SetAccessories()
- HumanoidDescription:GetAccessories()
- FaceAccessory
- FrontAccessory
- HairAccessory
- HatAccessory
- NeckAccessory
- ShouldersAccessory
- WaistAccessory
- Humanoid:ApplyDescription()
- NumberValue
- ProportionScale
- WidthScale
- HeightScale
- DepthScale
- HeadScale
- Animation.AnimationId
- state
- FallAnimation
- IdleAnimation
- JumpAnimation
- RunAnimation
- SwimAnimation
- WalkAnimation
- BodyTypeScale
- Decal
- GraphicTShirt
- Head
- Accessory
- BackAccessory
- Face
- ClimbAnimation
- Graphic
- TorsoColor
- Torso
- RightArm
- LeftArm
- RightLeg
- LeftLeg
- HeadColor
- BodyColors.HeadColor3
- BodyColors.HeadColor
- LeftArmColor
- RightArmColor
- LeftLegColor
- RightLegColor
- BodyColors.LeftArmColor3
- BodyColors.LeftArmColor
- BodyColors.LeftLegColor3
- BodyColors.LeftLegColor
- PantsTemplate
- BodyColors.RightArmColor3
- BodyColors.RightArmColor
- BodyColors.RightLegColor3
- BodyColors.RightLegColor
- ShirtTemplate
- BodyColors.TorsoColor3
- BodyColors.TorsoColor
- RemoveEmote
- EmotesChanged
- GetEmotes
- SetEmotes
- added
- set
- AddEmote
- SetEquippedEmotes
- EquippedEmotesChanged
- GetEquippedEmotes
- removed
- HumanoidDescription:SetEmotes()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

English

Feedback

Engine Class

![HumanoidDescription](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/HumanoidDescription-Dark.webp)HumanoidDescription

Describes the appearance of a Humanoid character including body parts,
accessories, colors, scales, animations, and emotes.

---

Summary

Properties

|  |
| --- |
| [AccessoryBlob](#AccessoryBlob):[string](/docs/luau/strings) |
| [BackAccessory](#BackAccessory):[string](/docs/luau/strings) |
| [BodyTypeScale](#BodyTypeScale):[number](/docs/luau/numbers) |
| [ClimbAnimation](#ClimbAnimation):[number](/docs/luau/numbers) |
| [DepthScale](#DepthScale):[number](/docs/luau/numbers) |
| [Face](#Face):[number](/docs/luau/numbers) |
| [FaceAccessory](#FaceAccessory):[string](/docs/luau/strings) |
| [FallAnimation](#FallAnimation):[number](/docs/luau/numbers) |
| [FrontAccessory](#FrontAccessory):[string](/docs/luau/strings) |
| [GraphicTShirt](#GraphicTShirt):[number](/docs/luau/numbers) |
| [HairAccessory](#HairAccessory):[string](/docs/luau/strings) |
| [HatAccessory](#HatAccessory):[string](/docs/luau/strings) |
| [Head](#Head):[number](/docs/luau/numbers) |
| [HeadColor](#HeadColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [HeadScale](#HeadScale):[number](/docs/luau/numbers) |
| [HeightScale](#HeightScale):[number](/docs/luau/numbers) |
| [IdleAnimation](#IdleAnimation):[number](/docs/luau/numbers) |
| [JumpAnimation](#JumpAnimation):[number](/docs/luau/numbers) |
| [LeftArm](#LeftArm):[number](/docs/luau/numbers) |
| [LeftArmColor](#LeftArmColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [LeftLeg](#LeftLeg):[number](/docs/luau/numbers) |
| [LeftLegColor](#LeftLegColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [MoodAnimation](#MoodAnimation):[number](/docs/luau/numbers) |
| [NeckAccessory](#NeckAccessory):[string](/docs/luau/strings) |
| [Pants](#Pants):[number](/docs/luau/numbers) |
| [ProportionScale](#ProportionScale):[number](/docs/luau/numbers) |
| [RightArm](#RightArm):[number](/docs/luau/numbers) |
| [RightArmColor](#RightArmColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [RightLeg](#RightLeg):[number](/docs/luau/numbers) |
| [RightLegColor](#RightLegColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [RunAnimation](#RunAnimation):[number](/docs/luau/numbers) |
| [Shirt](#Shirt):[number](/docs/luau/numbers) |
| [ShouldersAccessory](#ShouldersAccessory):[string](/docs/luau/strings) |
| [SwimAnimation](#SwimAnimation):[number](/docs/luau/numbers) |
| [Torso](#Torso):[number](/docs/luau/numbers) |
| [TorsoColor](#TorsoColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [WaistAccessory](#WaistAccessory):[string](/docs/luau/strings) |
| [WalkAnimation](#WalkAnimation):[number](/docs/luau/numbers) |
| [WidthScale](#WidthScale):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [AddEmote](#AddEmote)(name: [string](/docs/luau/strings),assetId: [number](/docs/luau/numbers)):() |
| [GetAccessories](#GetAccessories)(includeRigidAccessories: [boolean](/docs/luau/booleans)):[Array](/docs/luau/tables#arrays) |
| [GetEmotes](#GetEmotes)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetEquippedEmotes](#GetEquippedEmotes)():[Array](/docs/luau/tables#arrays) |
| [RemoveEmote](#RemoveEmote)(name: [string](/docs/luau/strings)):() |
| [SetAccessories](#SetAccessories)(accessories: [Array](/docs/luau/tables#arrays),includeRigidAccessories: [boolean](/docs/luau/booleans)):() |
| [SetEmotes](#SetEmotes)(emotes: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [SetEquippedEmotes](#SetEquippedEmotes)(equippedEmotes: [Array](/docs/luau/tables#arrays)):() |

Events

|  |
| --- |
| [EmotesChanged](#EmotesChanged)(newEmotes: [Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [EquippedEmotesChanged](#EquippedEmotesChanged)(newEquippedEmotes: [Array](/docs/luau/tables#arrays)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

HumanoidDescription is an object that stores a description of a
[Humanoid](/docs/reference/engine/classes/Humanoid) for R6 and R15 rigs. It can be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) in order to set a rig's scaling,
clothing ([Shirt](/docs/reference/engine/classes/Shirt), [Pants](/docs/reference/engine/classes/Pants), [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic)),
[Accessories](/docs/reference/engine/classes/Accessory), [Animations](/docs/reference/engine/classes/Animation) and
[BodyColors](/docs/reference/engine/classes/BodyColors).

You can get a HumanoidDescription by using the following functions:

* [Players:GetHumanoidDescriptionFromUserId()](/docs/reference/engine/classes/Players#GetHumanoidDescriptionFromUserId), for an outfit currently
  being worn by a user on Roblox.
* [Players:GetHumanoidDescriptionFromOutfitId()](/docs/reference/engine/classes/Players#GetHumanoidDescriptionFromOutfitId), for an outfit created
  by a user on Roblox.
* You can create a Humanoid rig model from a HumanoidDescription through
  [Players:CreateHumanoidModelFromDescription()](/docs/reference/engine/classes/Players#CreateHumanoidModelFromDescription).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

---

API Reference

Properties

AccessoryBlob

Not Replicated

Not Scriptable

Read Parallel

A JSON formatted array of Layered clothing where each table in the entry
in the array describes an accessory's AssetId, AccessoryType, Order, and
(optionally) Puffiness as key-value pairs.

HumanoidDescription.AccessoryBlob:[string](/docs/luau/strings)

A JSON formatted array of Layered clothing where each table in the entry
in the array describes an accessory's AssetId, AccessoryType, Order, and
(optionally) Puffiness as key-value pairs. This can be edited in the
properties windows for the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

To make changes from Luau (which is recommended over editing the JSON
directly), use [HumanoidDescription:SetAccessories()](/docs/reference/engine/classes/HumanoidDescription#SetAccessories) and
[HumanoidDescription:GetAccessories()](/docs/reference/engine/classes/HumanoidDescription#GetAccessories). These methods can also be
enabled to work with rigid accessories by setting IncludeRigidAccessories
parameters to true.

Provide feedback

---

BackAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
back (such as capes).

HumanoidDescription.BackAccessory:[string](/docs/luau/strings)

BackAccessory is a comma-separated list of asset IDs that determine
what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription). The list cannot contain
duplicates.

An error is thrown if you try to apply a new description which shares any
assets with the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory),
  [FrontAccessory](/docs/reference/engine/classes/HumanoidDescription#FrontAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory),
  [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [NeckAccessory](/docs/reference/engine/classes/HumanoidDescription#NeckAccessory),
  [ShouldersAccessory](/docs/reference/engine/classes/HumanoidDescription#ShouldersAccessory) and
  [WaistAccessory](/docs/reference/engine/classes/HumanoidDescription#WaistAccessory), which are
  similar properties that apply accessories like this one

Provide feedback

---

BodyTypeScale

Read Parallel

Determines the factor by which the shape of a [Humanoid](/docs/reference/engine/classes/Humanoid) is
interpolated from the standard R15 body shape (0) to a taller and more
slender body type (1).

HumanoidDescription.BodyTypeScale:[number](/docs/luau/numbers)

BodyTypeScale determines the factor by which the shape of a
[Humanoid](/docs/reference/engine/classes/Humanoid) is interpolated from the standard R15 body shape (0) to a
taller and more slender body type (1). Values outside the range of 0 to 1
are clamped. When the description is applied through
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription), this value maps to a
BodyTypeScale [NumberValue](/docs/reference/engine/classes/NumberValue) within the [Humanoid](/docs/reference/engine/classes/Humanoid).

Note that when the value of this property is 0, the
[ProportionScale](/docs/reference/engine/classes/HumanoidDescription#ProportionScale) property has
no effect.

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [ProportionScale](/docs/reference/engine/classes/HumanoidDescription#ProportionScale), which also
  affects rig proportions when this property is non-zero
* [WidthScale](/docs/reference/engine/classes/HumanoidDescription#HeightScale),
  [HeightScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale) and
  [DepthScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale), which provide finer
  control over the dimensions of a rig
* [HeadScale](/docs/reference/engine/classes/HumanoidDescription#HeadScale), which provides specific
  control over the scale of the rig's head

Provide feedback

---

ClimbAnimation

Read Parallel

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), this determines the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to
play when its [state](/docs/reference/engine/classes/Humanoid#GetState) is
[Climbing](/docs/reference/engine/enums/HumanoidStateType).

HumanoidDescription.ClimbAnimation:[number](/docs/luau/numbers)

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), ClimbAnimation determines the
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to play when its
[state](/docs/reference/engine/classes/Humanoid#GetState) is [Climbing](/docs/reference/engine/enums/HumanoidStateType).

See also:

* [FallAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [IdleAnimation](/docs/reference/engine/classes/HumanoidDescription#IdleAnimation),
  [JumpAnimation](/docs/reference/engine/classes/HumanoidDescription#JumpAnimation),
  [RunAnimation](/docs/reference/engine/classes/HumanoidDescription#RunAnimation),
  [SwimAnimation](/docs/reference/engine/classes/HumanoidDescription#SwimAnimation) and
  [WalkAnimation](/docs/reference/engine/classes/HumanoidDescription#WalkAnimation), which are
  similar properties that determine animations to play on the rig

Provide feedback

---

DepthScale

Read Parallel

Determines by what factor the depth (back-to-front distance) of a
[Humanoid](/docs/reference/engine/classes/Humanoid) is scaled.

HumanoidDescription.DepthScale:[number](/docs/luau/numbers)

DepthScale determines by what factor the depth (back-to-front
distance) of a [Humanoid](/docs/reference/engine/classes/Humanoid) is scaled, as well as all accessories not
attached to its head. When the description is applied through
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription), this value maps to a
BodyDepthScale [NumberValue](/docs/reference/engine/classes/NumberValue) within the Humanoid.

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BodyTypeScale](/docs/reference/engine/classes/HumanoidDescription#BodyTypeScale) and
  [ProportionScale](/docs/reference/engine/classes/HumanoidDescription#ProportionScale), which can
  provide more realistic rig proportions
* [WidthScale](/docs/reference/engine/classes/HumanoidDescription#HeightScale) and
  [HeightScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale)

Provide feedback

---

Face

Read Parallel

Determines the asset ID of the Face to be applied to the [Humanoid](/docs/reference/engine/classes/Humanoid).

HumanoidDescription.Face:[number](/docs/luau/numbers)

Face determines the asset ID of the Face to be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a [Humanoid](/docs/reference/engine/classes/Humanoid). The
type of the asset ID provided must be for a Face type asset and not a
Decal or Image type asset.

The actual face texture is rendered using a [Decal](/docs/reference/engine/classes/Decal) in the Head
named "face" or "Face".

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [GraphicTShirt](/docs/reference/engine/classes/HumanoidDescription#GraphicTShirt),
  [Shirt](/docs/reference/engine/classes/HumanoidDescription#Shirt) and
  [Pants](/docs/reference/engine/classes/HumanoidDescription#Pants), which also apply textures to a
  rig
* [Head](/docs/reference/engine/classes/HumanoidDescription#Head), which can change the mesh of the
  head
* [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory), which can apply
  one or more [Accessory](/docs/reference/engine/classes/Accessory) objects to the face

Provide feedback

---

FaceAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to the
front of its face (such as glasses).

HumanoidDescription.FaceAccessory:[string](/docs/luau/strings)

FaceAccessory is a comma-separated list of asset IDs that determine
what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to the
front of its face (such as glasses). The list does not contain duplicates.

An error is thrown if you try to apply a new description which shares any
assets with the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BackAccessory](/docs/reference/engine/classes/HumanoidDescription#BackAccessory),
  [FrontAccessory](/docs/reference/engine/classes/HumanoidDescription#FrontAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory),
  [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [NeckAccessory](/docs/reference/engine/classes/HumanoidDescription#NeckAccessory),
  [ShouldersAccessory](/docs/reference/engine/classes/HumanoidDescription#ShouldersAccessory) and
  [WaistAccessory](/docs/reference/engine/classes/HumanoidDescription#WaistAccessory), which are
  similar properties that apply accessories like this one
* [Face](/docs/reference/engine/classes/HumanoidDescription#Face), a property that determines what
  Face texture is used on the head

Provide feedback

---

FallAnimation

Read Parallel

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), this determines the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to
play when its [state](/docs/reference/engine/classes/Humanoid#GetState) is
[Freefall](/docs/reference/engine/enums/HumanoidStateType).

HumanoidDescription.FallAnimation:[number](/docs/luau/numbers)

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), FallAnimation determines the
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to play when its
[state](/docs/reference/engine/classes/Humanoid#GetState) is [Freefall](/docs/reference/engine/enums/HumanoidStateType).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [ClimbAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [IdleAnimation](/docs/reference/engine/classes/HumanoidDescription#IdleAnimation),
  [JumpAnimation](/docs/reference/engine/classes/HumanoidDescription#JumpAnimation),
  [RunAnimation](/docs/reference/engine/classes/HumanoidDescription#RunAnimation),
  [SwimAnimation](/docs/reference/engine/classes/HumanoidDescription#SwimAnimation) and
  [WalkAnimation](/docs/reference/engine/classes/HumanoidDescription#WalkAnimation), which are
  similar properties that determine animations to play on the rig

Provide feedback

---

FrontAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to
front of its torso (such as medals or ties).

HumanoidDescription.FrontAccessory:[string](/docs/luau/strings)

FrontAccessory is a comma-separated list of asset IDs that determine
what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to
front of its torso (such as medals or ties). The list does not contain
duplicates.

An error is thrown if you try to apply a new description which shares any
assets with the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BackAccessory](/docs/reference/engine/classes/HumanoidDescription#BackAccessory),
  [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory),
  [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [NeckAccessory](/docs/reference/engine/classes/HumanoidDescription#NeckAccessory),
  [ShouldersAccessory](/docs/reference/engine/classes/HumanoidDescription#ShouldersAccessory) and
  [WaistAccessory](/docs/reference/engine/classes/HumanoidDescription#WaistAccessory), which are
  similar properties that apply accessories like this one

Provide feedback

---

GraphicTShirt

Read Parallel

Determines the [Graphic](/docs/reference/engine/classes/ShirtGraphic#Graphic) used by a
[ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic).

HumanoidDescription.GraphicTShirt:[number](/docs/luau/numbers)

GraphicTShirt determines the [Graphic](/docs/reference/engine/classes/ShirtGraphic#Graphic) used
by a [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic) instance when
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription) is called on a [Humanoid](/docs/reference/engine/classes/Humanoid). The
asset type must be for a T‑Shirt, not a Decal or Image.

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Shirt](/docs/reference/engine/classes/HumanoidDescription#Shirt), which can provide the same
  functionality in addition to providing textures for the entire torso and
  arms
* [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor), which can change the
  color of the torso underneath the t-shirt texture

Provide feedback

---

HairAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
head resembling hair.

HumanoidDescription.HairAccessory:[string](/docs/luau/strings)

HairAccessory is a comma-separated list of asset IDs that determine
what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
head resembling hair. The list does not contain duplicates.

An error is thrown if you try to apply a new description which shares any
assets with the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BackAccessory](/docs/reference/engine/classes/HumanoidDescription#BackAccessory),
  [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory),
  [FrontAccessory](/docs/reference/engine/classes/HumanoidDescription#FrontAccessory),
  [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [NeckAccessory](/docs/reference/engine/classes/HumanoidDescription#NeckAccessory),
  [ShouldersAccessory](/docs/reference/engine/classes/HumanoidDescription#ShouldersAccessory) and
  [WaistAccessory](/docs/reference/engine/classes/HumanoidDescription#WaistAccessory), which are
  similar properties that apply accessories like this one

Provide feedback

---

HatAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
head.

HumanoidDescription.HatAccessory:[string](/docs/luau/strings)

HatAccessory is a comma-separated list of asset IDs that determine
what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
head. The list does not contain duplicates.

An error is thrown if you try to apply a new description which shares any
assets with the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BackAccessory](/docs/reference/engine/classes/HumanoidDescription#BackAccessory),
  [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory),
  [FrontAccessory](/docs/reference/engine/classes/HumanoidDescription#FrontAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory),
  [NeckAccessory](/docs/reference/engine/classes/HumanoidDescription#NeckAccessory),
  [ShouldersAccessory](/docs/reference/engine/classes/HumanoidDescription#ShouldersAccessory) and
  [WaistAccessory](/docs/reference/engine/classes/HumanoidDescription#WaistAccessory), which are
  similar properties that apply accessories like this one

Provide feedback

---

Head

Not Replicated

Read Parallel

Determines the asset ID of the Head to be applied to the [Humanoid](/docs/reference/engine/classes/Humanoid).

HumanoidDescription.Head:[number](/docs/luau/numbers)

Head determines the asset ID of the Head to be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a [Humanoid](/docs/reference/engine/classes/Humanoid).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Torso](/docs/reference/engine/classes/HumanoidDescription#Torso),
  [RightArm](/docs/reference/engine/classes/HumanoidDescription#RightArm),
  [LeftArm](/docs/reference/engine/classes/HumanoidDescription#LeftArm),
  [RightLeg](/docs/reference/engine/classes/HumanoidDescription#RightLeg) and
  [LeftLeg](/docs/reference/engine/classes/HumanoidDescription#LeftLeg), which are similar
  properties that also control body part
* [HeadColor](/docs/reference/engine/classes/HumanoidDescription#HeadColor), which controls the
  color of this limb
* [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory) and
  [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory), which all can
  apply [Accessory](/docs/reference/engine/classes/Accessory) objects which are joined to the head

Provide feedback

---

HeadColor

Not Replicated

Read Parallel

Determines the [BodyColors.HeadColor3](/docs/reference/engine/classes/BodyColors#HeadColor3) and
[BodyColors.HeadColor](/docs/reference/engine/classes/BodyColors#HeadColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription).

HumanoidDescription.HeadColor:[Color3](/docs/reference/engine/datatypes/Color3)

HeadColor determines the [BodyColors.HeadColor3](/docs/reference/engine/classes/BodyColors#HeadColor3) and
[BodyColors.HeadColor](/docs/reference/engine/classes/BodyColors#HeadColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [LeftArmColor](/docs/reference/engine/classes/HumanoidDescription#LeftArmColor),
  [RightArmColor](/docs/reference/engine/classes/HumanoidDescription#RightArmColor),
  [LeftLegColor](/docs/reference/engine/classes/HumanoidDescription#LeftLegColor), and
  [RightLegColor](/docs/reference/engine/classes/HumanoidDescription#RightLegColor), which are
  similar properties that also control body colors
* [Head](/docs/reference/engine/classes/HumanoidDescription#Head), which controls the mesh used for
  the head
* [Face](/docs/reference/engine/classes/HumanoidDescription#Face), which applies a texture to the
  front of the head

Provide feedback

---

HeadScale

Read Parallel

Determines by what factor the Head object of a [Humanoid](/docs/reference/engine/classes/Humanoid) is
scaled, as well as any accessories attached to it.

HumanoidDescription.HeadScale:[number](/docs/luau/numbers)

HeadScale determines by what factor the Head object of a
[Humanoid](/docs/reference/engine/classes/Humanoid) is scaled, as well as any accessories attached to it
(such as those specified by
[HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory) and
[HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory)). When the
description is applied through [Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription), this
value maps to a HeadScale [NumberValue](/docs/reference/engine/classes/NumberValue) within the
[Humanoid](/docs/reference/engine/classes/Humanoid).

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BodyTypeScale](/docs/reference/engine/classes/HumanoidDescription#BodyTypeScale) and
  [ProportionScale](/docs/reference/engine/classes/HumanoidDescription#ProportionScale), which can
  provide realistic rig proportions
* [WidthScale](/docs/reference/engine/classes/HumanoidDescription#HeightScale),
  [HeightScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale) and
  [DepthScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale), which provide finer
  control over other dimensions of a rig

Provide feedback

---

HeightScale

Read Parallel

Determines by what factor the height (top-to-bottom distance) of a
[Humanoid](/docs/reference/engine/classes/Humanoid) is scaled, as well as all accessories not attached to its
head.

HumanoidDescription.HeightScale:[number](/docs/luau/numbers)

HeightScale determines by what factor the height (top-to-bottom
distance) of a [Humanoid](/docs/reference/engine/classes/Humanoid) is scaled, as well as all accessories not
attached to its head. When the description is applied through
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription), this value maps to a
BodyHeightScale [NumberValue](/docs/reference/engine/classes/NumberValue) within the [Humanoid](/docs/reference/engine/classes/Humanoid).

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BodyTypeScale](/docs/reference/engine/classes/HumanoidDescription#BodyTypeScale) and
  [ProportionScale](/docs/reference/engine/classes/HumanoidDescription#ProportionScale), which can
  provide more realistic rig proportions
* [WidthScale](/docs/reference/engine/classes/HumanoidDescription#HeightScale) and
  [DepthScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale)

Provide feedback

---

IdleAnimation

Read Parallel

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), this determines the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to
play when its [state](/docs/reference/engine/classes/Humanoid#GetState) is
[Running](/docs/reference/engine/enums/HumanoidStateType) at a speed near zero.

HumanoidDescription.IdleAnimation:[number](/docs/luau/numbers)

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), IdleAnimation determines the
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to play when its
[state](/docs/reference/engine/classes/Humanoid#GetState) is [Running](/docs/reference/engine/enums/HumanoidStateType) at a
speed near zero.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [ClimbAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [FallAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [JumpAnimation](/docs/reference/engine/classes/HumanoidDescription#JumpAnimation),
  [RunAnimation](/docs/reference/engine/classes/HumanoidDescription#RunAnimation),
  [SwimAnimation](/docs/reference/engine/classes/HumanoidDescription#SwimAnimation) and
  [WalkAnimation](/docs/reference/engine/classes/HumanoidDescription#WalkAnimation), which are
  similar properties that determine animations to play on the rig

Provide feedback

---

JumpAnimation

Read Parallel

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), this determines the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to
play when its [state](/docs/reference/engine/classes/Humanoid#GetState) is
[Jumping](/docs/reference/engine/enums/HumanoidStateType).

HumanoidDescription.JumpAnimation:[number](/docs/luau/numbers)

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), JumpAnimation determines the
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to play when its
[state](/docs/reference/engine/classes/Humanoid#GetState) is [Jumping](/docs/reference/engine/enums/HumanoidStateType).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [ClimbAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [FallAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [IdleAnimation](/docs/reference/engine/classes/HumanoidDescription#IdleAnimation),
  [RunAnimation](/docs/reference/engine/classes/HumanoidDescription#RunAnimation),
  [SwimAnimation](/docs/reference/engine/classes/HumanoidDescription#SwimAnimation) and
  [WalkAnimation](/docs/reference/engine/classes/HumanoidDescription#WalkAnimation), which are
  similar properties that determine animations to play on the rig

Provide feedback

---

LeftArm

Not Replicated

Read Parallel

Determines the asset ID of the LeftArm to be applied to the
[Humanoid](/docs/reference/engine/classes/Humanoid).

HumanoidDescription.LeftArm:[number](/docs/luau/numbers)

LeftArm determines the asset ID of the LeftArm to be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a [Humanoid](/docs/reference/engine/classes/Humanoid).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Head](/docs/reference/engine/classes/HumanoidDescription#Head),
  [Torso](/docs/reference/engine/classes/HumanoidDescription#Torso),
  [RightArm](/docs/reference/engine/classes/HumanoidDescription#RightArm),
  [RightLeg](/docs/reference/engine/classes/HumanoidDescription#RightLeg) and
  [LeftLeg](/docs/reference/engine/classes/HumanoidDescription#LeftLeg), which are similar
  properties that also control body part
* [LeftArmColor](/docs/reference/engine/classes/HumanoidDescription#LeftArmColor), which controls
  the color of this limb

Provide feedback

---

LeftArmColor

Not Replicated

Read Parallel

Determines the [BodyColors.LeftArmColor3](/docs/reference/engine/classes/BodyColors#LeftArmColor3) and
[BodyColors.LeftArmColor](/docs/reference/engine/classes/BodyColors#LeftArmColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when applied.

HumanoidDescription.LeftArmColor:[Color3](/docs/reference/engine/datatypes/Color3)

LeftArmColor determines the [BodyColors.LeftArmColor3](/docs/reference/engine/classes/BodyColors#LeftArmColor3) and
[BodyColors.LeftArmColor](/docs/reference/engine/classes/BodyColors#LeftArmColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when the description
is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription). For R15 and Rthro rigs,
this property controls both the upper, lower, and hand parts of the left
arm.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [HeadColor](/docs/reference/engine/classes/HumanoidDescription#HeadColor),
  [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [RightArmColor](/docs/reference/engine/classes/HumanoidDescription#RightArmColor),
  [LeftLegColor](/docs/reference/engine/classes/HumanoidDescription#LeftLegColor), and
  [RightLegColor](/docs/reference/engine/classes/HumanoidDescription#RightLegColor), which are
  similar properties that also control body colors
* [LeftArm](/docs/reference/engine/classes/HumanoidDescription#LeftArm), which controls the mesh
  used for this limb
* [Shirt](/docs/reference/engine/classes/HumanoidDescription#Shirt), which can apply a texture to
  this limb

Provide feedback

---

LeftLeg

Not Replicated

Read Parallel

Determines the asset ID of the LeftLeg to be applied to the
[Humanoid](/docs/reference/engine/classes/Humanoid).

HumanoidDescription.LeftLeg:[number](/docs/luau/numbers)

LeftLeg determines the asset ID of the LeftLeg to be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a [Humanoid](/docs/reference/engine/classes/Humanoid).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Head](/docs/reference/engine/classes/HumanoidDescription#Head),
  [Torso](/docs/reference/engine/classes/HumanoidDescription#Torso),
  [RightArm](/docs/reference/engine/classes/HumanoidDescription#RightArm),
  [LeftArm](/docs/reference/engine/classes/HumanoidDescription#LeftArm), and
  [RightLeg](/docs/reference/engine/classes/HumanoidDescription#RightLeg), which are similar
  properties that also control body part
* [LeftLegColor](/docs/reference/engine/classes/HumanoidDescription#LeftLegColor), which controls
  the color of this limb

Provide feedback

---

LeftLegColor

Not Replicated

Read Parallel

Determines the [BodyColors.LeftLegColor3](/docs/reference/engine/classes/BodyColors#LeftLegColor3) and
[BodyColors.LeftLegColor](/docs/reference/engine/classes/BodyColors#LeftLegColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when applied.

HumanoidDescription.LeftLegColor:[Color3](/docs/reference/engine/datatypes/Color3)

LeftLegColor determines the [BodyColors.LeftLegColor3](/docs/reference/engine/classes/BodyColors#LeftLegColor3) and
[BodyColors.LeftLegColor](/docs/reference/engine/classes/BodyColors#LeftLegColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when the description
is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription). For R15 and Rthro rigs,
this property controls both the upper, lower, and foot parts of the left
leg.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [HeadColor](/docs/reference/engine/classes/HumanoidDescription#HeadColor),
  [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [LeftArmColor](/docs/reference/engine/classes/HumanoidDescription#LeftArmColor),
  [RightArmColor](/docs/reference/engine/classes/HumanoidDescription#RightArmColor), and
  [RightLegColor](/docs/reference/engine/classes/HumanoidDescription#RightLegColor), which are
  similar properties that also control body colors
* [LeftLeg](/docs/reference/engine/classes/HumanoidDescription#LeftLeg), which controls the mesh
  used for this limb
* [Pants](/docs/reference/engine/classes/HumanoidDescription#Pants), which can apply a texture to
  this limb

Provide feedback

---

MoodAnimation

Read Parallel

HumanoidDescription.MoodAnimation:[number](/docs/luau/numbers)

Provide feedback

---

NeckAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
neck (such as scarves or necklaces).

HumanoidDescription.NeckAccessory:[string](/docs/luau/strings)

NeckAccessory is a comma-separated list of asset IDs that determine
what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
neck (such as scarves or necklaces). The list does not contain duplicates.

Any accessory can used in this property, even if it is meant to go in a
different accessory spot. For example, an accessory meant to go on your
back (such as a cape) could be included in
[HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory). An error is
thrown if you try to apply a new description which shares any assets with
the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BackAccessory](/docs/reference/engine/classes/HumanoidDescription#BackAccessory),
  [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory),
  [FrontAccessory](/docs/reference/engine/classes/HumanoidDescription#FrontAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory),
  [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [ShouldersAccessory](/docs/reference/engine/classes/HumanoidDescription#ShouldersAccessory) and
  [WaistAccessory](/docs/reference/engine/classes/HumanoidDescription#WaistAccessory), which are
  similar properties that apply accessories like this one

Provide feedback

---

Pants

Read Parallel

Determines the [PantsTemplate](/docs/reference/engine/classes/Pants#PantsTemplate) used by a
[Pants](/docs/reference/engine/classes/Pants) instance.

HumanoidDescription.Pants:[number](/docs/luau/numbers)

Pants determines the [PantsTemplate](/docs/reference/engine/classes/Pants#PantsTemplate) used by
a [Pants](/docs/reference/engine/classes/Pants) instance when [Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription) is
called on a [Humanoid](/docs/reference/engine/classes/Humanoid). The asset type must be for Pants, not a
Decal or Image.

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Shirt](/docs/reference/engine/classes/HumanoidDescription#Shirt), a similar property which
  applies to a [Shirt](/docs/reference/engine/classes/Shirt) object
* [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [LeftLegColor](/docs/reference/engine/classes/HumanoidDescription#LeftLegColor) and
  [RightLegColor](/docs/reference/engine/classes/HumanoidDescription#RightLegColor), which can
  change the color of the body parts underneath the pants texture

Provide feedback

---

ProportionScale

Read Parallel

Determines how wide (0) or narrow (1) a [Humanoid](/docs/reference/engine/classes/Humanoid) rig is.

HumanoidDescription.ProportionScale:[number](/docs/luau/numbers)

ProportionScale determines how wide (0) or narrow (1) a
[Humanoid](/docs/reference/engine/classes/Humanoid) rig is. Values outside the range of 0 to 1 are clamped.
When the description is applied through
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription), this value maps to a
BodyProportionScale [NumberValue](/docs/reference/engine/classes/NumberValue) within the [Humanoid](/docs/reference/engine/classes/Humanoid).

Note that when the value of
[BodyTypeScale](/docs/reference/engine/classes/HumanoidDescription#BodyTypeScale) is 0, this
property has no effect.

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BodyTypeScale](/docs/reference/engine/classes/HumanoidDescription#BodyTypeScale), which also
  affects rig proportions
* [WidthScale](/docs/reference/engine/classes/HumanoidDescription#HeightScale),
  [HeightScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale) and
  [DepthScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale), which provide finer
  control over the dimensions of a rig
* [HeadScale](/docs/reference/engine/classes/HumanoidDescription#HeadScale), which provides specific
  control over the scale of the rig's head

Provide feedback

---

RightArm

Not Replicated

Read Parallel

Determines the asset ID of the RightArm to be applied to the
[Humanoid](/docs/reference/engine/classes/Humanoid).

HumanoidDescription.RightArm:[number](/docs/luau/numbers)

RightArm determines the asset ID of the RightArm to be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a [Humanoid](/docs/reference/engine/classes/Humanoid).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Head](/docs/reference/engine/classes/HumanoidDescription#Head),
  [Torso](/docs/reference/engine/classes/HumanoidDescription#Torso),
  [LeftArm](/docs/reference/engine/classes/HumanoidDescription#LeftArm),
  [RightLeg](/docs/reference/engine/classes/HumanoidDescription#RightLeg) and
  [LeftLeg](/docs/reference/engine/classes/HumanoidDescription#LeftLeg), which are similar
  properties that also control body part
* [RightArmColor](/docs/reference/engine/classes/HumanoidDescription#RightArmColor), which controls
  the color of this limb

Provide feedback

---

RightArmColor

Not Replicated

Read Parallel

Determines the [BodyColors.RightArmColor3](/docs/reference/engine/classes/BodyColors#RightArmColor3) and
[BodyColors.RightArmColor](/docs/reference/engine/classes/BodyColors#RightArmColor) of a Humanoid when applied.

HumanoidDescription.RightArmColor:[Color3](/docs/reference/engine/datatypes/Color3)

RightArmColor determines the [BodyColors.RightArmColor3](/docs/reference/engine/classes/BodyColors#RightArmColor3) and
[BodyColors.RightArmColor](/docs/reference/engine/classes/BodyColors#RightArmColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when the
description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription). For R15 and
Rthro rigs, this property controls both the upper, lower, and hand parts
of the right arm.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [HeadColor](/docs/reference/engine/classes/HumanoidDescription#HeadColor),
  [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [LeftArmColor](/docs/reference/engine/classes/HumanoidDescription#LeftArmColor),
  [LeftLegColor](/docs/reference/engine/classes/HumanoidDescription#LeftLegColor), and
  [RightLegColor](/docs/reference/engine/classes/HumanoidDescription#RightLegColor), which are
  similar properties that also control body colors
* [RightArm](/docs/reference/engine/classes/HumanoidDescription#RightArm), which controls the mesh
  used for this limb
* [Shirt](/docs/reference/engine/classes/HumanoidDescription#Shirt), which can apply a texture to
  this limb

Provide feedback

---

RightLeg

Not Replicated

Read Parallel

Determines the asset ID of the RightLeg to be applied to the
[Humanoid](/docs/reference/engine/classes/Humanoid).

HumanoidDescription.RightLeg:[number](/docs/luau/numbers)

RightLeg determines the asset ID of the RightLeg to be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a [Humanoid](/docs/reference/engine/classes/Humanoid).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Head](/docs/reference/engine/classes/HumanoidDescription#Head),
  [Torso](/docs/reference/engine/classes/HumanoidDescription#Torso),
  [RightArm](/docs/reference/engine/classes/HumanoidDescription#RightArm),
  [LeftArm](/docs/reference/engine/classes/HumanoidDescription#LeftArm) and
  [LeftLeg](/docs/reference/engine/classes/HumanoidDescription#LeftLeg), which are similar
  properties that also control body part
* [RightLegColor](/docs/reference/engine/classes/HumanoidDescription#RightLegColor), which controls
  the color of this limb

Provide feedback

---

RightLegColor

Not Replicated

Read Parallel

Determines the [BodyColors.RightLegColor3](/docs/reference/engine/classes/BodyColors#RightLegColor3) and
[BodyColors.RightLegColor](/docs/reference/engine/classes/BodyColors#RightLegColor) of a Humanoid when applied.

HumanoidDescription.RightLegColor:[Color3](/docs/reference/engine/datatypes/Color3)

RightLegColor determines the [BodyColors.RightLegColor3](/docs/reference/engine/classes/BodyColors#RightLegColor3) and
[BodyColors.RightLegColor](/docs/reference/engine/classes/BodyColors#RightLegColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when the
description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription). For R15 and
Rthro rigs, this property controls both the upper, lower, and foot parts
of the right leg.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [HeadColor](/docs/reference/engine/classes/HumanoidDescription#HeadColor),
  [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [LeftArmColor](/docs/reference/engine/classes/HumanoidDescription#LeftArmColor),
  [RightArmColor](/docs/reference/engine/classes/HumanoidDescription#RightArmColor), and
  [LeftLegColor](/docs/reference/engine/classes/HumanoidDescription#LeftLegColor), which are similar
  properties that also control body colors
* [RightLeg](/docs/reference/engine/classes/HumanoidDescription#RightLeg), which controls the mesh
  used for this limb
* [Pants](/docs/reference/engine/classes/HumanoidDescription#Pants), which can apply a texture to
  this limb

Provide feedback

---

RunAnimation

Read Parallel

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), this determines the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to
play when its [state](/docs/reference/engine/classes/Humanoid#GetState) is
[Running](/docs/reference/engine/enums/HumanoidStateType) at a moderate speed.

HumanoidDescription.RunAnimation:[number](/docs/luau/numbers)

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), RunAnimation determines the
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to play when its
[state](/docs/reference/engine/classes/Humanoid#GetState) is [Running](/docs/reference/engine/enums/HumanoidStateType) at a
moderate speed.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [ClimbAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [FallAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [IdleAnimation](/docs/reference/engine/classes/HumanoidDescription#IdleAnimation),
  [JumpAnimation](/docs/reference/engine/classes/HumanoidDescription#JumpAnimation),
  [SwimAnimation](/docs/reference/engine/classes/HumanoidDescription#SwimAnimation) and
  [WalkAnimation](/docs/reference/engine/classes/HumanoidDescription#WalkAnimation), which are
  similar properties that determine animations to play on the rig

Provide feedback

---

Shirt

Read Parallel

Determines the [ShirtTemplate](/docs/reference/engine/classes/Shirt#ShirtTemplate) used by a
[Shirt](/docs/reference/engine/classes/Shirt) instance.

HumanoidDescription.Shirt:[number](/docs/luau/numbers)

Shirt determines the [ShirtTemplate](/docs/reference/engine/classes/Shirt#ShirtTemplate) used by
a [Shirt](/docs/reference/engine/classes/Shirt) instance when [Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription) is
called on a [Humanoid](/docs/reference/engine/classes/Humanoid). The asset type must be for Shirt, not a
Decal or Image.

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Pants](/docs/reference/engine/classes/HumanoidDescription#Pants), a similar property which
  applies to a [Pants](/docs/reference/engine/classes/Pants) object
* [GraphicTShirt](/docs/reference/engine/classes/HumanoidDescription#GraphicTShirt), a similar
  property which applies to a [ShirtGraphic](/docs/reference/engine/classes/ShirtGraphic) object
* [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [LeftArmColor](/docs/reference/engine/classes/HumanoidDescription#LeftArmColor) and
  [RightArmColor](/docs/reference/engine/classes/HumanoidDescription#RightArmColor), which can
  change the color of the body parts underneath the shirt texture

Provide feedback

---

ShouldersAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
shoulders (such as shoulder-mounted critters).

HumanoidDescription.ShouldersAccessory:[string](/docs/luau/strings)

ShouldersAccessory is a comma-separated list of asset IDs that
determine what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
shoulders (such as shoulder-mounted critters). The list does not contain
duplicates.

An error is thrown if you try to apply a new description which shares any
assets with the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BackAccessory](/docs/reference/engine/classes/HumanoidDescription#BackAccessory),
  [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory),
  [FrontAccessory](/docs/reference/engine/classes/HumanoidDescription#FrontAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory),
  [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [NeckAccessory](/docs/reference/engine/classes/HumanoidDescription#NeckAccessory) and
  [WaistAccessory](/docs/reference/engine/classes/HumanoidDescription#WaistAccessory), which are
  similar properties that apply accessories like this one

Provide feedback

---

SwimAnimation

Read Parallel

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), this determines the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to
play when its [state](/docs/reference/engine/classes/Humanoid#GetState) is
[Swimming](/docs/reference/engine/enums/HumanoidStateType).

HumanoidDescription.SwimAnimation:[number](/docs/luau/numbers)

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), SwimAnimation determines the
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to play when its
[state](/docs/reference/engine/classes/Humanoid#GetState) is [Swimming](/docs/reference/engine/enums/HumanoidStateType)

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [ClimbAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [FallAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [IdleAnimation](/docs/reference/engine/classes/HumanoidDescription#IdleAnimation),
  [JumpAnimation](/docs/reference/engine/classes/HumanoidDescription#JumpAnimation),
  [RunAnimation](/docs/reference/engine/classes/HumanoidDescription#RunAnimation) and
  [WalkAnimation](/docs/reference/engine/classes/HumanoidDescription#WalkAnimation), which are
  similar properties that determine animations to play on the rig

Provide feedback

---

Torso

Not Replicated

Read Parallel

Determines the asset ID of the Torso to be applied to the
[Humanoid](/docs/reference/engine/classes/Humanoid).

HumanoidDescription.Torso:[number](/docs/luau/numbers)

Torso determines the asset ID of the Torso to be
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a [Humanoid](/docs/reference/engine/classes/Humanoid).

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [Head](/docs/reference/engine/classes/HumanoidDescription#Head),
  [RightArm](/docs/reference/engine/classes/HumanoidDescription#RightArm),
  [LeftArm](/docs/reference/engine/classes/HumanoidDescription#LeftArm),
  [RightLeg](/docs/reference/engine/classes/HumanoidDescription#RightLeg) and
  [LeftLeg](/docs/reference/engine/classes/HumanoidDescription#LeftLeg), which are similar
  properties that also control body part
* [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor), which controls the
  color of this limb

Provide feedback

---

TorsoColor

Not Replicated

Read Parallel

Determines the [BodyColors.TorsoColor3](/docs/reference/engine/classes/BodyColors#TorsoColor3) and
[BodyColors.TorsoColor](/docs/reference/engine/classes/BodyColors#TorsoColor) of a Humanoid when applied.

HumanoidDescription.TorsoColor:[Color3](/docs/reference/engine/datatypes/Color3)

TorsoColor determines the [BodyColors.TorsoColor3](/docs/reference/engine/classes/BodyColors#TorsoColor3) and
[BodyColors.TorsoColor](/docs/reference/engine/classes/BodyColors#TorsoColor) of a [Humanoid](/docs/reference/engine/classes/Humanoid) when the description
is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription). For R15 and Rthro rigs,
this property controls both the upper and lower parts of the torso.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [HeadColor](/docs/reference/engine/classes/HumanoidDescription#HeadColor),
  [TorsoColor](/docs/reference/engine/classes/HumanoidDescription#TorsoColor),
  [LeftArmColor](/docs/reference/engine/classes/HumanoidDescription#LeftArmColor),
  [RightArmColor](/docs/reference/engine/classes/HumanoidDescription#RightArmColor),
  [LeftLegColor](/docs/reference/engine/classes/HumanoidDescription#LeftLegColor), and
  [RightLegColor](/docs/reference/engine/classes/HumanoidDescription#RightLegColor), which are
  similar properties that also control body colors
* [Torso](/docs/reference/engine/classes/HumanoidDescription#Torso), which controls the mesh used
  for this body part
* [GraphicTShirt](/docs/reference/engine/classes/HumanoidDescription#GraphicTShirt) and
  [Shirt](/docs/reference/engine/classes/HumanoidDescription#Shirt), which can apply a texture to
  this body part

Provide feedback

---

WaistAccessory

Not Replicated

Read Parallel

A comma-separated list of asset IDs that will be added as
[Accessories](/docs/reference/engine/classes/Accessory) to a [Humanoid](/docs/reference/engine/classes/Humanoid) rig when
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
waist (such as belts).

HumanoidDescription.WaistAccessory:[string](/docs/luau/strings)

WaistAccessory is a comma-separated list of asset IDs that determine
what accessories should be added when the description is
[applied](/docs/reference/engine/classes/Humanoid#ApplyDescription), usually those attached to its
waist (such as belts). The list does not contain duplicates.

An error is thrown if you try to apply a new description which shares any
assets with the existing description but a different accessory property.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BackAccessory](/docs/reference/engine/classes/HumanoidDescription#BackAccessory),
  [FaceAccessory](/docs/reference/engine/classes/HumanoidDescription#FaceAccessory),
  [FrontAccessory](/docs/reference/engine/classes/HumanoidDescription#FrontAccessory),
  [HairAccessory](/docs/reference/engine/classes/HumanoidDescription#HairAccessory),
  [HatAccessory](/docs/reference/engine/classes/HumanoidDescription#HatAccessory),
  [NeckAccessory](/docs/reference/engine/classes/HumanoidDescription#NeckAccessory) and
  [ShouldersAccessory](/docs/reference/engine/classes/HumanoidDescription#ShouldersAccessory), which
  are similar properties that apply accessories like this one

Provide feedback

---

WalkAnimation

Read Parallel

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), this determines the [Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to
play when its [state](/docs/reference/engine/classes/Humanoid#GetState) is
[Running](/docs/reference/engine/enums/HumanoidStateType) at a low speed.

HumanoidDescription.WalkAnimation:[number](/docs/luau/numbers)

When this description is [applied](/docs/reference/engine/classes/Humanoid#ApplyDescription) to a
[Humanoid](/docs/reference/engine/classes/Humanoid), WalkAnimation determines the
[Animation.AnimationId](/docs/reference/engine/classes/Animation#AnimationId) to play when its
[state](/docs/reference/engine/classes/Humanoid#GetState) is [Running](/docs/reference/engine/enums/HumanoidStateType) at a
low speed

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [ClimbAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [FallAnimation](/docs/reference/engine/classes/HumanoidDescription#FallAnimation),
  [IdleAnimation](/docs/reference/engine/classes/HumanoidDescription#IdleAnimation),
  [JumpAnimation](/docs/reference/engine/classes/HumanoidDescription#JumpAnimation),
  [RunAnimation](/docs/reference/engine/classes/HumanoidDescription#RunAnimation) and
  [SwimAnimation](/docs/reference/engine/classes/HumanoidDescription#SwimAnimation), which are
  similar properties that determine animations to play on the rig

Provide feedback

---

WidthScale

Read Parallel

Determines by what factor the width (left-to-right distance) of a
[Humanoid](/docs/reference/engine/classes/Humanoid) is scaled, as well as all accessories not attached to its
head.

HumanoidDescription.WidthScale:[number](/docs/luau/numbers)

WidthScale determines by what factor the width (left-to-right
distance) of a [Humanoid](/docs/reference/engine/classes/Humanoid) is scaled, as well as all accessories not
attached to its head. When the description is applied through
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription), this value maps to a
BodyWidthScale [NumberValue](/docs/reference/engine/classes/NumberValue) within the [Humanoid](/docs/reference/engine/classes/Humanoid).

#### See Also

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [BodyTypeScale](/docs/reference/engine/classes/HumanoidDescription#BodyTypeScale) and
  [ProportionScale](/docs/reference/engine/classes/HumanoidDescription#ProportionScale), which can
  provide more realistic rig proportions
* [HeightScale](/docs/reference/engine/classes/HumanoidDescription#HeightScale) and
  [DepthScale](/docs/reference/engine/classes/HumanoidDescription#DepthScale)

Provide feedback

---

Methods

AddEmote

Adds the emote to the description given a name and its asset ID.

HumanoidDescription:AddEmote(

name:[string](/docs/luau/strings), assetId:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  A string that identifies what emote is being added. Example: "Salute". |
| assetId:[number](/docs/luau/numbers)  An emote asset ID. |

Returns

()

AddEmote will add an Emote asset to the description given a name and
its asset ID. The asset ID must be for an "Emote" asset (see
[Featured emotes](https://www.roblox.com/catalog?Category=0&Subcategory=39)
in the Catalog).

You can add multiple emotes of the same name. All emotes of the same name
can be removed using
[RemoveEmote](/docs/reference/engine/classes/HumanoidDescription#RemoveEmote). If an emote with
the same ID is added under the same name,
[EmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EmotesChanged) fires.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [GetEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEmotes), which can be used to
  retrieve the emotes that have been added by this function
* [SetEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) and
  [RemoveEmote](/docs/reference/engine/classes/HumanoidDescription#RemoveEmote), which also
  manipulate what emotes have been added
* [EmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EmotesChanged), which fires
  after this function is called

Provide feedback

---

GetAccessories

Returns a table of an avatar's current accessories.

HumanoidDescription:GetAccessories(includeRigidAccessories:[boolean](/docs/luau/booleans)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| includeRigidAccessories:[boolean](/docs/luau/booleans)  Set to true if rigid accessories from the rigid accessory properties should also be included in the return array. False means only include layered clothing accessories from the AccessoryBlob. |

Returns

[Array](/docs/luau/tables#arrays)

Returns an array where each entry specifies for an individual
accessory the AccessoryType, AssetId, IsLayered, Order and Puffiness.

Returns a table of an avatar's current accessories. If the second
parameter (includeRigidAccessories) is true then the returned table will
also include entries for rigid accessories from the rigid accessory
properties.

Code Samples

Get Accessories

This code sample prints out all the asset IDs and types of the accessories in
the HumanoidDescription.

```
local includeRigidAccessories = true



local accessoriesTable =



game:GetService("Players"):GetHumanoidDescriptionFromUserId(1):GetAccessories(includeRigidAccessories)



for _, accessoryInfo in ipairs(accessoriesTable) do



print(tostring(accessoryInfo.AssetId) .. " " .. tostring(accessoryInfo.AccessoryType))



end
```

Provide feedback

---

GetEmotes

Returns a dictionary of emotes that have been
[added](/docs/reference/engine/classes/HumanoidDescription#AddEmote) or
[set](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) to this description.

HumanoidDescription:GetEmotes():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary of emotes where the key is the emote name and the value
is an array of emote asset IDs. Example:

```
{



Salute = {3360689775},



Agree = {4849487550},



Disagree = {4849495710}



}
```

.

GetEmotes returns a dictionary of emotes that have been
[added](/docs/reference/engine/classes/HumanoidDescription#AddEmote) or
[set](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) to this description. The keys
of this dictionary are the names of the emotes, and the values are a
non-empty array of emote IDs for that name.

#### Example

```
local hd = Instance.new("HumanoidDescription")



hd:AddEmote("Salute", 3360689775)



local emotes = hd:GetEmotes()



for name, ids in emotes do



print(("The emote %s has %d ids:"):format(name, #ids))



for _, id in ids do



print(id)



end



end
```

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [SetEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) and
  [AddEmote](/docs/reference/engine/classes/HumanoidDescription#AddEmote), which can add emotes
  that may be returned by this function
* [EmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EmotesChanged), which fires
  with the value returned this function after it may have changed

Provide feedback

---

GetEquippedEmotes

Returns an array of tables describing the equipped emotes that have been
[set](/docs/reference/engine/classes/HumanoidDescription#SetEquippedEmotes).

HumanoidDescription:GetEquippedEmotes():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of tables describing the name and slot which each emote is
equipped. Example:

```
{



{Slot = 3, Name = "Salute"},



{Slot = 2, Name = "Agree"},



{Slot = 1, Name = "Disagree"},



}
```

.

GetEquippedEmotes returns an array of tables which indicate the Name
and Slot of each equipped emote as it was set by
[SetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEquippedEmotes).

#### Example

```
local hd = Instance.new("HumanoidDescription")



hd:SetEmotes({Salute = {3360689775}, Agree = {4849487550}})



hd:SetEquippedEmotes({"Salute", "Agree"})



-- Iterate over the equipped emotes:



for _, t in hd:GetEquippedEmotes() do



print(("In slot %d: emote %s is equipped"):format(t.Slot, t.Name))



end
```

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [SetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEquippedEmotes), which
  sets the currently equipped emotes and changes what this function
  returns
* [EquippedEmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EquippedEmotesChanged),
  which fires when the function returned by this value may have changed

Provide feedback

---

RemoveEmote

Removes any emotes that have been added under the given name.

HumanoidDescription:RemoveEmote(name:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the emote as it was [set](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) or [added](/docs/reference/engine/classes/HumanoidDescription#AddEmote). |

Returns

()

RemoveEmote removes all emotes from the description that have been
[added](/docs/reference/engine/classes/HumanoidDescription#AddEmote) or
[set](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) under the given name. If there
are no added emotes with the given name, no error is thrown and
[EmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EmotesChanged) does not fire.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [SetEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) and
  [AddEmote](/docs/reference/engine/classes/HumanoidDescription#AddEmote), which can add emotes
  that may be removed
* [GetEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEmotes), which can retrieve a
  dictionary of emotes that may be removed

Provide feedback

---

SetAccessories

Accepts a table that sets the accessories and related properties for an
avatar.

HumanoidDescription:SetAccessories(

accessories:[Array](/docs/luau/tables#arrays), includeRigidAccessories:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| accessories:[Array](/docs/luau/tables#arrays)  Each entry specifies for an individual accessory the AccessoryType, AssetId, IsLayered, Order and Puffiness. |
| includeRigidAccessories:[boolean](/docs/luau/booleans)  Set to true if rigid accessories are also included in the passed in array (they would have to not specify Order). |

Returns

()

Accepts a table that sets the accessories and related properties for an
avatar. If the second parameter (includeRigidAccessories) is true, then
this function can also be used to set the rigid accessories in the rigid
accessory properties. In this case any table entry that does not have an
Order will be considered a rigid accessory and put in the appropriate
property according to the AccessoryType.

Code Samples

Set Accessories

This code sample adds two accessories to a HumanoidDescription.

```
local humanoidDescription = Instance.new("HumanoidDescription")



local originalSpecifications = {



{



Order = 1,



AssetId = 123456789,



Puffiness = 0.5,



AccessoryType = Enum.AccessoryType.Sweater,



},



}



humanoidDescription:SetAccessories(originalSpecifications)



local updatedSpecifications = humanoidDescription:GetAccessories(false)



local newIndividualSpecification = {



Order = 2,



AssetId = 987654321,



Puffiness = 0.7,



AccessoryType = Enum.AccessoryType.Jacket,



IsLayered = true,



}



updatedSpecifications[#updatedSpecifications + 1] = newIndividualSpecification



humanoidDescription:SetAccessories(updatedSpecifications)
```

Provide feedback

---

SetEmotes

Sets all of the emotes on this description.

HumanoidDescription:SetEmotes(emotes:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| emotes:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary of emotes where the key is the emote name and the value is an array of emote asset IDs. Example:  ```  {  Salute = {3360689775},  Agree = {4849487550},  Disagree = {4849495710}  } ```  . |

Returns

()

SetEmotes sets all of the emotes on this description given a table
similar to that returned by
[GetEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEmotes). It fires
[EmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EmotesChanged)

#### Example

```
local emotes = {



Salute = {3360689775}, -- Syntax note: can also use ["Salute"] = ...



Agree = {4849487550},



Disagree = {4849495710}



}



local hd = Instance.new("HumanoidDescription")



hd:SetEmotes(emotes)
```

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [AddEmote](/docs/reference/engine/classes/HumanoidDescription#AddEmote) and
  [RemoveEmote](/docs/reference/engine/classes/HumanoidDescription#RemoveEmote) which can modify
  the added emotes on an individual level
* [EmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EmotesChanged), which fires
  when this function is called

Provide feedback

---

SetEquippedEmotes

Sets the currently equipped emotes given an array of emote names.

HumanoidDescription:SetEquippedEmotes(equippedEmotes:[Array](/docs/luau/tables#arrays)):()

Parameters

|  |
| --- |
| equippedEmotes:[Array](/docs/luau/tables#arrays)  An array of emote names. Example:  ```  { "Disagree", "Agree", "Salute" } ```  – OR – An array of tables describing the name and slot which each emote is equipped. Example:  ```  {  {Slot = 3, Name = "Salute"},  {Slot = 2, Name = "Agree"},  {Slot = 1, Name = "Disagree"},  } ```  . |

Returns

()

SetEquippedEmotes sets the currently equipped emotes given an array of
emote names as they were passed to
[AddEmote](/docs/reference/engine/classes/HumanoidDescription#AddEmote) or
[SetEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEmotes). It can also take an
array of tables similar to that returned by
[GetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEquippedEmotes). Calling
this function fires
[EquippedEmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EquippedEmotesChanged).

#### Example

```
local hd = Instance.new("HumanoidDescription")



hd:SetEmotes({Salute = {3360689775}, Agree = {4849487550}})



-- Can provide either an array of strings... (index is slot number)



hd:SetEquippedEmotes({"Salute", "Agree"})



-- ...or an array of tables as returned by GetEquippedEmotes (Slot and Name keys set)



hd:SetEquippedEmotes({{Slot = 1, Name = "Salute"}, {Slot = 2, Name = "Agree"}})
```

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [GetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEquippedEmotes), which
  returns a value describing the equipped emotes set by this function
* [EquippedEmotesChanged](/docs/reference/engine/classes/HumanoidDescription#EquippedEmotesChanged),
  which fires when this function is called

Provide feedback

---

Events

EmotesChanged

Fires when emotes are added, removed or set on this description.

HumanoidDescription.EmotesChanged(newEmotes:[Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| newEmotes:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary of emotes where the key is the emote name and the value is an array of emote asset IDs. Example:  ```  {  Salute = {3360689775},  Agree = {4849487550},  Disagree = {4849495710}  } ```  . |

EmotesChanged fires when emotes are
[added](/docs/reference/engine/classes/HumanoidDescription#AddEmote),
[removed](/docs/reference/engine/classes/HumanoidDescription#RemoveEmote) or
[set](/docs/reference/engine/classes/HumanoidDescription#SetEmotes) on the description. The event
fires with the new emote table as returned by
[GetEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEmotes).

If [AddEmote](/docs/reference/engine/classes/HumanoidDescription#AddEmote) is called with the same
name and ID as an existing emote, this event fires.

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [AddEmote](/docs/reference/engine/classes/HumanoidDescription#AddEmote),
  [RemoveEmote](/docs/reference/engine/classes/HumanoidDescription#RemoveEmote) and
  [HumanoidDescription:SetEmotes()](/docs/reference/engine/classes/HumanoidDescription#SetEmotes), which can cause this event to
  be fired

Provide feedback

---

EquippedEmotesChanged

Fires when the equipped emotes are
[set](/docs/reference/engine/classes/HumanoidDescription#SetEquippedEmotes) on this description.

HumanoidDescription.EquippedEmotesChanged(newEquippedEmotes:[Array](/docs/luau/tables#arrays)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| newEquippedEmotes:[Array](/docs/luau/tables#arrays)  An array of tables describing the name and slot which each emote is equipped. Example:  ```  {  {Slot = 3, Name = "Salute"},  {Slot = 2, Name = "Agree"},  {Slot = 1, Name = "Disagree"},  } ```  . |

EquippedEmotesChanged fires when the equipped emotes are set on this
description using
[SetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEquippedEmotes). It
provides the new equipped emotes in a table like that returned by
[GetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEquippedEmotes).

#### Example

```
local hd = Instance.new("HumanoidDescription")



hd.EquippedEmotesChanged:Connect(function(equippedEmotes)



print(("We have %d emotes equipped"):format(#equippedEmotes))



for _, t in equippedEmotes do



print(("In slot %d: emote %s is equipped"):format(t.Slot, t.Name))



end



end)



hd:SetEquippedEmotes({"Salute", "Agree"}) --> We have 2 emotes equipped
```

See also:

* [HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
  for more information on [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).
* [SetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#SetEquippedEmotes), which
  fires this event
* [GetEquippedEmotes](/docs/reference/engine/classes/HumanoidDescription#GetEquippedEmotes), which
  can be used to query the currently equipped emotes without this event
  firing

Provide feedback

---