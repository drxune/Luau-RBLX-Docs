# AvatarCreationService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AvatarCreationService
Scraped: 2026-01-11T02:35:09.614659Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- AvatarCreationService
- Player
- EditableImage
- HumanoidDescription
- Model
- Object
- LoadGeneratedAvatarAsync()
- PromptCreateAvatarAsync()
- EditableMesh
- PromptSelectAvatarGenerationImageAsync()
- LoadAvatar2DPreviewAsync()
- GenerateAvatar2DPreviewAsync()
- AutoSetupAvatarAsync()
- GenerateAvatarAsync()
- AvatarCreationService:AutoSetupAvatarAsync()
- MeshPart
- WrapDeformer
- Accessory
- BodyPartDescription
- BodyPartDescription.Instance
- Folder
- MeshParts
- BodyPartDescription.BodyPart
- AccessoryDescription
- AccessoryDescription.Instance
- AccessoryDescription.AccessoryType
- BodyTypeScale
- HeadScale
- HeightScale
- WidthScale
- ProportionScale
- PromptCreateAvatarAssetAsync()
- GetOutfitDetails
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AvatarCreationService](/docs/reference/engine/classes/AvatarCreationService)

English

Feedback

Engine Class

AvatarCreationService

A service to support developer avatar creators.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [AutoSetupAvatarAsync](#AutoSetupAvatarAsync)(player: [Player](/docs/reference/engine/classes/Player),model: [Dictionary](/docs/luau/tables#dictionaries),progressCallback: [function](/docs/luau/functions)?):[string](/docs/luau/strings) |
| [GenerateAvatar2DPreviewAsync](#GenerateAvatar2DPreviewAsync)(avatarGeneration2dPreviewParams: [Dictionary](/docs/luau/tables#dictionaries)):[string](/docs/luau/strings) |
| [GenerateAvatarAsync](#GenerateAvatarAsync)(avatarGenerationParams: [Dictionary](/docs/luau/tables#dictionaries)):[string](/docs/luau/strings) |
| [GetBatchTokenDetailsAsync](#GetBatchTokenDetailsAsync)(tokenIds: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |
| [GetValidationRules](#GetValidationRules)():[Dictionary](/docs/luau/tables#dictionaries) |
| [LoadAvatar2DPreviewAsync](#LoadAvatar2DPreviewAsync)(previewId: [string](/docs/luau/strings)):[EditableImage](/docs/reference/engine/classes/EditableImage) |
| [LoadGeneratedAvatarAsync](#LoadGeneratedAvatarAsync)(generationId: [string](/docs/luau/strings)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |
| [PrepareAvatarForPreviewAsync](#PrepareAvatarForPreviewAsync)(humanoidModel: [Model](/docs/reference/engine/classes/Model)):() |
| [PromptCreateAvatarAssetAsync](#PromptCreateAvatarAssetAsync)(tokenId: [string](/docs/luau/strings),player: [Player](/docs/reference/engine/classes/Player),assetInstance: [Instance](/docs/reference/engine/datatypes/Instance),assetType: [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)):[Tuple](/docs/luau/tuples) |
| [PromptCreateAvatarAsync](#PromptCreateAvatarAsync)(tokenId: [string](/docs/luau/strings),player: [Player](/docs/reference/engine/classes/Player),humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[Tuple](/docs/luau/tuples) |
| [PromptSelectAvatarGenerationImageAsync](#PromptSelectAvatarGenerationImageAsync)(player: [Player](/docs/reference/engine/classes/Player)):[string](/docs/luau/strings) |
| [RequestAvatarGenerationSessionAsync](#RequestAvatarGenerationSessionAsync)(player: [Player](/docs/reference/engine/classes/Player),callback: [function](/docs/luau/functions)):[Tuple](/docs/luau/tuples) |
| [ValidateUGCAccessoryAsync](#ValidateUGCAccessoryAsync)(player: [Player](/docs/reference/engine/classes/Player),accessory: [Instance](/docs/reference/engine/datatypes/Instance),accessoryType: [Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType)):[Tuple](/docs/luau/tuples) |
| [ValidateUGCBodyPartAsync](#ValidateUGCBodyPartAsync)(player: [Player](/docs/reference/engine/classes/Player),instance: [Instance](/docs/reference/engine/datatypes/Instance),bodyPart: [Enum.BodyPart](/docs/reference/engine/enums/BodyPart)):[Tuple](/docs/luau/tuples) |
| [ValidateUGCFullBodyAsync](#ValidateUGCFullBodyAsync)(player: [Player](/docs/reference/engine/classes/Player),humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[Tuple](/docs/luau/tuples) |

Events

|  |
| --- |
| [AvatarAssetModerationCompleted](#AvatarAssetModerationCompleted)(assetId: [number](/docs/luau/numbers),moderationStatus: [Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [AvatarModerationCompleted](#AvatarModerationCompleted)(outfitId: [number](/docs/luau/numbers),moderationStatus: [Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

AvatarCreationService is a service that supports developer avatar creators,
providing methods that support the prompting of avatar creation from within
experiences.

---

API Reference

Methods

AutoSetupAvatarAsync

Yields

Automatically sets up a custom [Model](/docs/reference/engine/classes/Model) as an avatar asset.

AvatarCreationService:AutoSetupAvatarAsync(

player:[Player](/docs/reference/engine/classes/Player), model:[Dictionary](/docs/luau/tables#dictionaries), progressCallback:[function](/docs/luau/functions)?

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) that the avatar is being set up for. |
| model:[Dictionary](/docs/luau/tables#dictionaries)  The humanoid [Model](/docs/reference/engine/classes/Model) that will be set up as an avatar. |
| progressCallback:[function](/docs/luau/functions)?  Optional callback function that will be invoked periodically with a progressInfo table with the overall progress (from 0 to 1). Type: (progressInfo: { Progress: number }) -> () |

Returns

[string](/docs/luau/strings)

A unique identifier for the generated avatar.

Automatically sets up a custom [Model](/docs/reference/engine/classes/Model) as an avatar asset. This
method returns a string generation ID which can be passed to
[LoadGeneratedAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#LoadGeneratedAvatarAsync)
to load the generated avatar and return a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) with
all the generated instances and properties. The load method can be called
on both the server and client, allowing the generated avatar to be loaded
in both places (on the client for previewing, and on the server for saving
the generated avatar to the player's inventory using
[PromptCreateAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#PromptCreateAvatarAsync)).

Auto-setup has specific model requirements and accepts certain
configurations of models. For more information, see
[Auto-setup requirements](/docs/avatar-setup/auto-setup-requirements).
In addition to the above requirements, the input model must use
[EditableMesh](/docs/reference/engine/classes/EditableMesh) and [EditableImage](/docs/reference/engine/classes/EditableImage) objects for all mesh and
texture assets.

Code Samples

AutoSetupAvatarAsync

The following code invokes AutoSetup on the given Model.
The setup avatar is then loaded on the server and an event is sent to
the client to load the avatar for local preview.

A separate saveAvatarToInventory function is provided to demonstrate
how to pass the generated avatar to PromptCreateAvatarAsync if the
player wants to save it to their inventory.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local LoadAvatarEvent = ReplicatedStorage.LoadAvatarEvent



local generatedAvatars = {}



-- Must be called on the server



local function setupAvatar(player: Player, avatarModel: Model)



local pcallSuccess, result = pcall(function()



local generationId = AvatarCreationService:AutoSetupAvatarAsync(



player,



avatarModel,



function(progressInfo)



print(`AutoSetup progress: {progressInfo.Progress * 100}%`)



end



)



-- Load and store on the server to use with PromptCreateAvatarAsync



local humanoidDescription = AvatarCreationService:LoadGeneratedAvatarAsync(generationId)



generatedAvatars[generationId] = humanoidDescription



-- Signal the client so it can load the avatar for local preview



LoadAvatarEvent:FireClient(player, generationId)



end)



if not pcallSuccess then



warn("Avatar setup failed:", result)



end



end



local avatarCreationToken = "xyz" -- https://create.roblox.com/docs/production/monetization/avatar-creation-token



local function saveAvatarToInventory(generationId: string, player: Player)



local humanoidDescription = generatedAvatars[generationId]



return AvatarCreationService:PromptCreateAvatarAsync(avatarCreationToken, player, humanoidDescription)



end
```

Provide feedback

---

GenerateAvatar2DPreviewAsync

Yields

Creates a 2D avatar preview and returns a previewId.

AvatarCreationService:GenerateAvatar2DPreviewAsync(avatarGeneration2dPreviewParams:[Dictionary](/docs/luau/tables#dictionaries)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| avatarGeneration2dPreviewParams:[Dictionary](/docs/luau/tables#dictionaries)  A table of arguments for 2D preview generation. Type: avatarGeneration2dPreviewParams: {SessionId: string, FileId: string, TextPrompt: string?} |

Returns

[string](/docs/luau/strings)

A string previewId

Creates a 2D avatar image preview, taking as input the FileId from
[PromptSelectAvatarGenerationImageAsync()](/docs/reference/engine/classes/AvatarCreationService#PromptSelectAvatarGenerationImageAsync)
and an optional text prompt. It returns a previewId which can be passed to
[LoadAvatar2DPreviewAsync()](/docs/reference/engine/classes/AvatarCreationService#LoadAvatar2DPreviewAsync)
to retrieve the preview image on the client. This API can only be used on
the game server.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



function generateAvatar2DPreview(sessionId, fileId, textPrompt)



local pcallSuccess, result = pcall(function()



local args = {}



args.SessionId = sessionId



args.FileId = fileId



args.TextPrompt = textPrompt



return AvatarCreationService:GenerateAvatar2DPreview(args)



end)



if not pcallSuccess then



warn("Generating 2D preview failed: ", result)



end



return result



end
```

Provide feedback

---

GenerateAvatarAsync

Yields

Generates an avatar and returns a generationId.

AvatarCreationService:GenerateAvatarAsync(avatarGenerationParams:[Dictionary](/docs/luau/tables#dictionaries)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| avatarGenerationParams:[Dictionary](/docs/luau/tables#dictionaries)  A table of arguments for generating an avatar. Type: avatarGenerationParams: {SessionId: string, PreviewId: string} |

Returns

[string](/docs/luau/strings)

A string generationId.

Generate an avatar from a preview and return the generationId. The
[LoadGeneratedAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#LoadGeneratedAvatarAsync)
method is then called to retrieve the generated
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) avatar. This API can only be used on the game
server.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



function generateAvatar(sessionId, previewId)



local pcallSuccess, result = pcall(function()



local args = {}



args.SessionId = sessionId



args.PreviewId = previewId



return AvatarCreationService:GenerateAvatarAsync(args)



end)



if not pcallSuccess then



warn("Generating avatar failed: ", result)



end



return result



end
```

Provide feedback

---

GetBatchTokenDetailsAsync

Yields

Gets the avatar creation token details for a list of avatar creation
tokens at once.

AvatarCreationService:GetBatchTokenDetailsAsync(tokenIds:[Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| tokenIds:[Array](/docs/luau/tables#arrays)  The list of avatar creation token IDs to get details of. |

Returns

[Array](/docs/luau/tables#arrays)

Array of avatar creation token details as outlined above.

Gets the avatar creation token details for a list of avatar creation
tokens at once (tokens are generated through the
[token creation](/docs/production/monetization/avatar-creation-token)
process). Returns an array of avatar creation token details; each token
detail is a dictionary with the fields indicated in the example result
below:

```
{



["Name"] = "string",



["Description"] = "string",



["UniverseId"] = 0,



["CreatorId"] = 0,



["CreatorType"] = Enum.CreatorType.User,



["OnSale"] = true,



["Price"] = 0,



["OffSaleReasons"] = {



"string",



}



}
```

Provide feedback

---

GetValidationRules

Gets data regarding rules that assets must abide by to pass UGC
validation.

AvatarCreationService:GetValidationRules():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Dictionary of validation rules as detailed above.

Gets data regarding rules that assets must abide by to pass UGC
validation. Validation is an essential step before creating avatars and
there are various checks that occur, including mesh triangle limits,
texture sizes, body part size limits, attachment positions, and more.

The returned dictionary of validation rules takes the following form:

```
{



["MeshRules"] = {



["BodyPartMaxTriangles"] = {



Enum.AssetType.DynamicHead: number,



Enum.AssetType.LeftArm: number,



Enum.AssetType.RightArm: number,



Enum.AssetType.Torso: number,



Enum.AssetType.LeftLeg: number,



Enum.AssetType.RightLeg: number,



},



["AccessoryMaxTriangles"]: number,



["MeshVertColor"]: Color3,



["CageMeshMaxDistanceFromRenderMesh"]: number,



},



["TextureRules"] = {



["MaxTextureSize"]: number,



},



["BodyPartRules"] = {



[Enum.AssetType.DynamicHead] = {



["Bounds"] = {



["Classic"] = {



["MinSize"]: Vector3,



["MaxSize"]: Vector3,



},



["ProportionsSlender"] = {



["MinSize"]: Vector3,



["MaxSize"]: Vector3,



},



["ProportionsNormal"] = {



["MinSize"]: Vector3,



["MaxSize"]: Vector3,



},



},



["SubParts"] = {



["Head"] = {



["NeckRigAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["FaceFrontAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["HatAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["HairAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["FaceCenterAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



},



},



},



[Enum.AssetType.LeftArm] = {



["Bounds"] = {



["Classic"] = {



["MinSize"]: Vector3,



["MaxSize"]: Vector3,



},



["ProportionsSlender"] = {



["MinSize"]: Vector3,



["MaxSize"]: Vector3,



},



["ProportionsNormal"] = {



["MinSize"]: Vector3,



["MaxSize"]: Vector3,



},



},



["SubParts"] = {



["LeftHand"] = {



["LeftWristRigAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["LeftGripAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



},



["LeftUpperArm"] = {



["LeftShoulderRigAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["LeftShoulderAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["LeftElbowRigAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



},



["LeftLowerArm"] = {



["LeftElbowRigAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



["LeftWristRigAttachment"] = {



["LowerBound"]: Vector3,



["UpperBound"]: Vector3,



},



},



},



},



...



},



["AccessoryRules"] = {



[Enum.AssetType.HairAccessory] = {



["Attachments"] = {



{



["Size"]: Vector3,



["Offset"]: Vector3,



["Name"]: string,



},



},



["RigidAllowed"]: boolean,



},



...



}



}
```

Provide feedback

---

LoadAvatar2DPreviewAsync

Yields

Load an AvatarGeneration 2D preview on the client from a previewId.

AvatarCreationService:LoadAvatar2DPreviewAsync(previewId:[string](/docs/luau/strings)):[EditableImage](/docs/reference/engine/classes/EditableImage)

Parameters

|  |
| --- |
| previewId:[string](/docs/luau/strings)  Load the preview generated from [GenerateAvatar2DPreviewAsync()](/docs/reference/engine/classes/AvatarCreationService#GenerateAvatar2DPreviewAsync). |

Returns

[EditableImage](/docs/reference/engine/classes/EditableImage)

An [EditableImage](/docs/reference/engine/classes/EditableImage) containing the preview image.

Load an AvatarGeneration 2D preview as an [EditableImage](/docs/reference/engine/classes/EditableImage) on the
client for the given previewId. This API can only be used on the client.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



function loadAvatar2DPreview(previewId)



local pcallSuccess, result = pcall(function()



return AvatarCreationService:LoadAvatar2DPreviewAsync(previewId)



end)



if not pcallSuccess then



warn("Failed to load preview: ", result)



end



return result



end
```

Provide feedback

---

LoadGeneratedAvatarAsync

Yields

Loads a generated avatar using an avatar generation ID.

AvatarCreationService:LoadGeneratedAvatarAsync(generationId:[string](/docs/luau/strings)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Parameters

|  |
| --- |
| generationId:[string](/docs/luau/strings)  A unique string that identifies the generated avatar, as returned by  [AutoSetupAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#AutoSetupAvatarAsync). |

Returns

[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

The [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) of the generated avatar, which
includes all the generated instances and properties.

Loads a generated avatar using an avatar generation ID, as returned by
[AutoSetupAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#AutoSetupAvatarAsync)
or
[GenerateAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#GenerateAvatarAsync).
The generated avatar will be returned as a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)
with all the generated instances and properties. Mesh and texture assets
will be provided as [EditableMesh](/docs/reference/engine/classes/EditableMesh) and [EditableImage](/docs/reference/engine/classes/EditableImage)
objects, respectively, to allow continued editing of the generated avatar.

This method can be called on both the server and client, allowing the
generated avatar to be loaded in both places (on the client for
previewing, and on the server for saving the generated avatar to the
player's inventory using
[PromptCreateAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#PromptCreateAvatarAsync)).
Once the method has been invoked on both the client and server, the data
associated with the generation ID will be erased and subsequent calls to
his method with the same generation ID will fail.

Code Samples

LoadGeneratedAvatarAsync

The following code loads a generated avatar using an avatar generation ID
provided by [AvatarCreationService:AutoSetupAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#AutoSetupAvatarAsync). The result
is returned as a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

```
local AvatarCreationService = game:GetService("AvatarCreationService")



local Players = game:GetService("Players")



-- Can be called on either the server or client



local function loadAvatar(generationId: string): Model?



local pcallSuccess, result = pcall(function()



local humanoidDescription = AvatarCreationService:LoadGeneratedAvatarAsync(generationId)



local model = Players:CreateHumanoidModelFromDescription(humanoidDescription, Enum.HumanoidRigType.R15)



return model



end)



if pcallSuccess then



return result



else



print("Avatar failed to load:", result)



return nil



end



end
```

Provide feedback

---

PrepareAvatarForPreviewAsync

Yields

Prepares in-experience avatar for preview.

AvatarCreationService:PrepareAvatarForPreviewAsync(humanoidModel:[Model](/docs/reference/engine/classes/Model)):()

Parameters

|  |
| --- |
| humanoidModel:[Model](/docs/reference/engine/classes/Model)  The [Model](/docs/reference/engine/classes/Model) containing [MeshPart](/docs/reference/engine/classes/MeshPart) children with [WrapDeformer](/docs/reference/engine/classes/WrapDeformer) instances that require HSR data updating for preview. |

Returns

()

Triggers HSR generation and attachment point updating for in-experience
avatar previews. This allows for previewing of avatars created in
experience with layered clothing and accessories in the same way they will
appear when published through
[PromptCreateAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#PromptCreateAvatarAsync).

When developers use [EditableMesh](/docs/reference/engine/classes/EditableMesh) and [WrapDeformer](/docs/reference/engine/classes/WrapDeformer) to
modify avatars before publishing, the original HSR data may not accurately
account for the new deformations. This method generates updated HSR data
and corrects attachment points based on the [WrapDeformer](/docs/reference/engine/classes/WrapDeformer)
modifications, ensuring consistent preview and published avatar
appearance.

Provide feedback

---

PromptCreateAvatarAssetAsync

Yields

Prompts a [Player](/docs/reference/engine/classes/Player) to purchase and create an avatar asset from an
[Instance](/docs/reference/engine/classes/Instance).

AvatarCreationService:PromptCreateAvatarAssetAsync(

tokenId:[string](/docs/luau/strings), player:[Player](/docs/reference/engine/classes/Player), assetInstance:[Instance](/docs/reference/engine/datatypes/Instance), assetType:[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| tokenId:[string](/docs/luau/strings)  The ID of a creation token. The token must be valid in that the universe the method is called from is the same universe the token was created for. Furthermore, the token creator must maintain ID verification and [Roblox Premium](https://www.roblox.com/premium/membership). To create a token for utilization in this API, follow the [token creation](/docs/production/monetization/avatar-creation-token) process. The token's creation type must match the [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType) passed in to the method. |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) intended to be presented with the creation prompt. |
| assetInstance:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) of the avatar asset intended for creation. |
| assetType:[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)  The [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType) of the expected creation. This must match the creation type of the provided token. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing, in order:

* An [Enum.PromptCreateAssetResult](/docs/reference/engine/enums/PromptCreateAssetResult) indicating the result of the
  creation prompt.
* A string result. In the case of
  [Enum.PromptCreateAssetResult.Success](/docs/reference/engine/enums/PromptCreateAssetResult#Success), this will indicate the asset
  ID. In the case of any failure enum, this will indicate the
  resultant error message.

Prompts a [Player](/docs/reference/engine/classes/Player) to purchase and create an avatar asset from an
[Instance](/docs/reference/engine/classes/Instance). The price of the creation is dictated by the price
attributed to the avatar creation token. This creation token is required
for the purchasing and creation of the asset and can be generated by
following the
[token creation](/docs/production/monetization/avatar-creation-token)
process.

For avatar asset creation, the [Instance](/docs/reference/engine/classes/Instance) is expected to include a
new accessory to be created. This includes the following types:
[Hat](/docs/reference/engine/enums/AvatarAssetType#Hat), [Hair](/docs/reference/engine/enums/AvatarAssetType#HairAccessory),
[FaceAccessory](/docs/reference/engine/enums/AvatarAssetType#FaceAccessory),
[NeckAccessory](/docs/reference/engine/enums/AvatarAssetType#NeckAccessory),
[ShoulderAccessory](/docs/reference/engine/enums/AvatarAssetType#ShoulderAccessory),
[FrontAccessory](/docs/reference/engine/enums/AvatarAssetType#FrontAccessory),
[BackAccessory](/docs/reference/engine/enums/AvatarAssetType#BackAccessory),
[WaistAccessory](/docs/reference/engine/enums/AvatarAssetType#WaistAccessory),
[TShirtAccessory](/docs/reference/engine/enums/AvatarAssetType#TShirtAccessory),
[ShirtAccessory](/docs/reference/engine/enums/AvatarAssetType#ShirtAccessory),
[PantsAccessory](/docs/reference/engine/enums/AvatarAssetType#PantsAccessory),
[JacketAccessory](/docs/reference/engine/enums/AvatarAssetType#JacketAccessory),
[SweaterAccessory](/docs/reference/engine/enums/AvatarAssetType#SweaterAccessory),
[ShortsAccessory](/docs/reference/engine/enums/AvatarAssetType#ShortsAccessory),
[DressSkirtAccessory](/docs/reference/engine/enums/AvatarAssetType#DressSkirtAccessory).

To support this, the [Instance](/docs/reference/engine/classes/Instance) should be an [Accessory](/docs/reference/engine/classes/Accessory)
instance or contain an [Accessory](/docs/reference/engine/classes/Accessory) child instance. This should
include a [MeshPart](/docs/reference/engine/classes/MeshPart) child instance which makes up the accessory.

The avatar asset [MeshPart](/docs/reference/engine/classes/MeshPart) will also need to include:

* An [EditableImage](/docs/reference/engine/classes/EditableImage).
* An [EditableMesh](/docs/reference/engine/classes/EditableMesh).

If creating a layered clothing accessory such as a shirt, the
[MeshPart](/docs/reference/engine/classes/MeshPart) should include a [WrapDeformer](/docs/reference/engine/classes/WrapDeformer) with an
[EditableMesh](/docs/reference/engine/classes/EditableMesh).

Finally, the provided [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType) should match the creation
type of the token and the type of [Accessory](/docs/reference/engine/classes/Accessory) for upload.

Code Samples

PromptCreateAvatarAssetAsync

The following code prompts for avatar asset creation,
and responds to the result.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



local function publishAvatarAsset(tokenId: string, player: Player, assetInstance: Accessory, assetType: Enum.AvatarAssetType)



local pcallSuccess, result, resultMessage = pcall(function()



return AvatarCreationService:PromptCreateAvatarAssetAsync(tokenId, player, assetInstance, assetType)



end)



if pcallSuccess then



if result == Enum.PromptCreateAssetResult.Success then



print("Successfully uploaded with AssetId: ", resultMessage)



else



print("Unsuccessfully uploaded with error message:", resultMessage)



end



else



print("Avatar asset failed to create.")



end



end
```

Provide feedback

---

PromptCreateAvatarAsync

Yields

Prompts a [Player](/docs/reference/engine/classes/Player) to purchase and create an avatar from a
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

AvatarCreationService:PromptCreateAvatarAsync(

tokenId:[string](/docs/luau/strings), player:[Player](/docs/reference/engine/classes/Player), humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| tokenId:[string](/docs/luau/strings)  The ID of an avatar creation token. The token must be valid in that the universe the method is called from is the same universe the token was created for. Furthermore, the token creator must maintain ID verification and [Roblox Premium](https://www.roblox.com/premium/membership). To create a token for utilization in this API, follow the [token creation](/docs/production/monetization/avatar-creation-token) process. |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) intended to be presented with the creation prompt. |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  The [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) of the avatar intended for creation. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing, in order:

* An [Enum.PromptCreateAvatarResult](/docs/reference/engine/enums/PromptCreateAvatarResult) indicating the result of the
  creation prompt.
* A string result. In the case of
  [Enum.PromptCreateAvatarResult.Success](/docs/reference/engine/enums/PromptCreateAvatarResult#Success), this will indicate the
  bundle ID. In the case of any failure enum, this will indicate the
  resultant error message.
* A secondary optional string result. In the case of
  [Enum.PromptCreateAvatarResult.Success](/docs/reference/engine/enums/PromptCreateAvatarResult#Success), this will indicate the
  outfit ID. In the case of any failure enum, this will be nil.

Prompts a [Player](/docs/reference/engine/classes/Player) to purchase and create an avatar from a
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription). The price of the creation is dictated by the
price attributed to the avatar creation token. This avatar creation token
is required for the purchasing and creation of the body and can be
generated by following the
[token creation](/docs/production/monetization/avatar-creation-token)
process.

For avatar creation, the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) is expected to
include new assets to be created for each of the 6 body parts
([Head](/docs/reference/engine/enums/BodyPart#Head), [Torso](/docs/reference/engine/enums/BodyPart#Torso),
[RightLeg](/docs/reference/engine/enums/BodyPart#RightLeg), [LeftLeg](/docs/reference/engine/enums/BodyPart#LeftLeg),
[RightArm](/docs/reference/engine/enums/BodyPart#RightArm), [LeftArm](/docs/reference/engine/enums/BodyPart#LeftArm)).
Optionally, it can also include a new [Hair](/docs/reference/engine/enums/AccessoryType#Hair)
accessory.

To support this, the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) should include 6
[BodyPartDescription](/docs/reference/engine/classes/BodyPartDescription) children (one for each body part). For each,
the [BodyPartDescription.Instance](/docs/reference/engine/classes/BodyPartDescription#Instance) property references a
[Folder](/docs/reference/engine/classes/Folder) which includes all of the [MeshPart](/docs/reference/engine/classes/MeshPart) instances which
make up the body part, for example a LeftArm folder which has
LeftHand, LeftUpperArm, and LeftLowerArm [MeshParts](/docs/reference/engine/classes/MeshPart).
The [BodyPartDescription.BodyPart](/docs/reference/engine/classes/BodyPartDescription#BodyPart) property should also be set to
the relevant [Enum.BodyPart](/docs/reference/engine/enums/BodyPart).

Each body part [MeshPart](/docs/reference/engine/classes/MeshPart) will also need to include:

* An [EditableImage](/docs/reference/engine/classes/EditableImage).
* A [WrapDeformer](/docs/reference/engine/classes/WrapDeformer) with an [EditableMesh](/docs/reference/engine/classes/EditableMesh).

If including an accessory such as hair, the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)
should include a child [AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription) where:

* The [AccessoryDescription.Instance](/docs/reference/engine/classes/AccessoryDescription#Instance) property references the
  [Accessory](/docs/reference/engine/classes/Accessory) instance.
* The [AccessoryDescription.AccessoryType](/docs/reference/engine/classes/AccessoryDescription#AccessoryType) property is set to the
  relevant [Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType).

Finally, the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) should include the humanoid
scales of [BodyTypeScale](/docs/reference/engine/classes/HumanoidDescription#BodyTypeScale),
[HeadScale](/docs/reference/engine/classes/HumanoidDescription#HeadScale),
[HeightScale](/docs/reference/engine/classes/HumanoidDescription#HeightScale),
[WidthScale](/docs/reference/engine/classes/HumanoidDescription#WidthScale), and
[ProportionScale](/docs/reference/engine/classes/HumanoidDescription#ProportionScale). Be mindful of
the scales that a base body is imported with so that they match the scales
provided to the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

Code Samples

PromptCreateAvatarAsync

The following code populates a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) in the expected format, prompts for avatar creation,
and responds to the result.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



export type BodyPartInfo = {



bodyPart: Enum.BodyPart,



instance: Instance, --Folder with Created MeshParts



}



export type BodyPartList = { BodyPartInfo }



local function publishAvatar(bodyPartInstances: BodyPartList, player: Player, tokenId: string)



local humanoidDescription = Instance.new("HumanoidDescription")



for _, bodyPartInfo in bodyPartInstances do



local bodyPartDescription = Instance.new("BodyPartDescription")



bodyPartDescription.Instance = bodyPartInfo.instance



bodyPartDescription.BodyPart = bodyPartInfo.bodyPart



bodyPartDescription.Parent = humanoidDescription



end



local pcallSuccess, result, resultMessage = pcall(function()



return AvatarCreationService:PromptCreateAvatarAsync(tokenId, player, humanoidDescription)



end)



if pcallSuccess then



if result == Enum.PromptCreateAvatarResult.Success then



print("Successfully uploaded with BundleId: ", resultMessage)



else



print("Unsuccessfully uploaded with error message:", resultMessage)



end



else



print("Avatar failed to create.")



end



end
```

Provide feedback

---

PromptSelectAvatarGenerationImageAsync

Yields

Prompt the [Player](/docs/reference/engine/classes/Player) to take a selfie and return the FileId.

AvatarCreationService:PromptSelectAvatarGenerationImageAsync(player:[Player](/docs/reference/engine/classes/Player)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) to prompt for taking a selfie. |

Returns

[string](/docs/luau/strings)

A string FileId of the selfie.

Prompt the [Player](/docs/reference/engine/classes/Player) to take a selfie and return the FileId of the
selfie. This FileId is then passed as an argument to
[GenerateAvatar2DPreviewAsync()](/docs/reference/engine/classes/AvatarCreationService#GenerateAvatar2DPreviewAsync).
This API can only be used on the game server.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



function promptSelectAvatarGenerationImage(player)



local pcallSuccess, result = pcall(function()



return AvatarCreationService:PromptSelectAvatarGenerationImageAsync(player)



end)



if not pcallSuccess then



warn("Failed to prompt for image: ", result)



end



return result



end
```

Provide feedback

---

RequestAvatarGenerationSessionAsync

Yields

Request an AvatarGeneration session for a [Player](/docs/reference/engine/classes/Player).

AvatarCreationService:RequestAvatarGenerationSessionAsync(

player:[Player](/docs/reference/engine/classes/Player), callback:[function](/docs/luau/functions)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) to request an AvatarGeneration session for. |
| callback:[function](/docs/luau/functions)  Callback function that is invoked with a SessionInfo table, with information about the session. Type: (SessionInfo: { SessionId: string, Allowed2DGenerations: number, Allowed3DGenerations: number, SessionTime: number }) -> () |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing a [RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) that can be used
to cancel the session request and the estimated wait time in seconds.

Request an AvatarGeneration session for a [Player](/docs/reference/engine/classes/Player). Information
about the session is returned via the callback, including the SessionId
which is passed to the
[GenerateAvatar2DPreviewAsync()](/docs/reference/engine/classes/AvatarCreationService#GenerateAvatar2DPreviewAsync)
and
[GenerateAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#GenerateAvatarAsync)
methods. Additional session information includes allowed 2d preview
generations, allowed 3d avatar generations, and the session time. The
method returns a Tuple with an [RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) and
estimated waitTime. The [RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) allows canceling
a session request. The estimated waitTime is used to provide the player
an estimated time in seconds until the session will be ready. This API can
only be used on the game server.

```
local AvatarCreationService = game:GetService("AvatarCreationService")



local playerSessions = {}



local playerSessionRequests = {}



function requestAvatarGenerationSession(player)



local pcallSuccess, conn, waitTime = pcall(function()



return AvatarCreationService:RequestAvatarGenerationSessionAsync(player, function(sessionInfo)



playerSessions[player.UserID] = sessionInfo



playerSessionRequests[player.UserID] = nil



end)



end)



if not pcallSuccess then



warn("Failed to request Avatar generation session: ", conn)



end



playerSessionRequests[player.UserID] = conn



print("Wait time for session: ", tostring(waitTime))



end



function cancelAvatarGenerationSessionRequest(player)



if playerSessionRequests[player.UserID] ~= nil then



playerSessionRequests[player.UserID]:Disconnect()



end



end
```

Provide feedback

---

ValidateUGCAccessoryAsync

Yields

Studio only. Runs UGC validation for an [Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType).

AvatarCreationService:ValidateUGCAccessoryAsync(

player:[Player](/docs/reference/engine/classes/Player), accessory:[Instance](/docs/reference/engine/datatypes/Instance), accessoryType:[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) validation is completed for. |
| accessory:[Instance](/docs/reference/engine/datatypes/Instance)  The instance validation is run on. |
| accessoryType:[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType)  [Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType) the instance is expected to be. Expects [Eyebrow](/docs/reference/engine/enums/AccessoryType#Eyebrow), [Eyelash](/docs/reference/engine/enums/AccessoryType#Eyelash), or [Hair](/docs/reference/engine/enums/AccessoryType#Hair). |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing, in order:

* A boolean indicating if validation was successful for the accessory.
* An optional table of strings. This includes failure reasons if
  validation was unsuccessful; otherwise nil if validation was
  successful.

Studio only. Given a [Player](/docs/reference/engine/classes/Player) and [Instance](/docs/reference/engine/classes/Instance) for an
[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType), determines if UGC validation passes.

Provide feedback

---

ValidateUGCBodyPartAsync

Yields

Studio only. Runs UGC validation for an [Enum.BodyPart](/docs/reference/engine/enums/BodyPart).

AvatarCreationService:ValidateUGCBodyPartAsync(

player:[Player](/docs/reference/engine/classes/Player), instance:[Instance](/docs/reference/engine/datatypes/Instance), bodyPart:[Enum.BodyPart](/docs/reference/engine/enums/BodyPart)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) validation is completed for. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The instance validation is run on. |
| bodyPart:[Enum.BodyPart](/docs/reference/engine/enums/BodyPart)  [Enum.BodyPart](/docs/reference/engine/enums/BodyPart) the instance is expected to be. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing, in order:

* A boolean indicating if validation was successful for the body part.
* An optional table of strings. This includes failure reasons if
  validation was unsuccessful; otherwise nil if validation was
  successful.

Studio only. Given a [Player](/docs/reference/engine/classes/Player) and [Instance](/docs/reference/engine/classes/Instance) for an
[Enum.BodyPart](/docs/reference/engine/enums/BodyPart), determines if UGC validation passes. The instance
parameter is expected as a [Folder](/docs/reference/engine/classes/Folder) in the following example format
with relevant [MeshParts](/docs/reference/engine/classes/MeshPart):

* LeftArm ([Folder](/docs/reference/engine/classes/Folder))
  + R15ArtistIntent ([Folder](/docs/reference/engine/classes/Folder))
    - LeftLowerArm ([MeshPart](/docs/reference/engine/classes/MeshPart))
    - LeftUpperArm ([MeshPart](/docs/reference/engine/classes/MeshPart))
    - LeftHand ([MeshPart](/docs/reference/engine/classes/MeshPart))

However, if the expected bodyPart is [Enum.BodyPart.Head](/docs/reference/engine/enums/BodyPart#Head), the function
takes a singular Head [MeshPart](/docs/reference/engine/classes/MeshPart) directly.

Provide feedback

---

ValidateUGCFullBodyAsync

Yields

Studio only. Runs UGC validation for a whole body.

AvatarCreationService:ValidateUGCFullBodyAsync(

player:[Player](/docs/reference/engine/classes/Player), humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) validation is completed for. |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) representing the body that validation is run on. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing, in order:

* A boolean indicating if validation was successful for the body.
* An optional table of strings. This includes failure reasons if
  validation was unsuccessful; otherwise nil if validation was
  successful.

Studio only. Given a [Player](/docs/reference/engine/classes/Player) and [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), all
instances in the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) will be validated.

The [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) is expected to include instances set on
[BodyPartDescription](/docs/reference/engine/classes/BodyPartDescription) children for each of the 6 required
[Enum.BodyPart](/docs/reference/engine/enums/BodyPart) values. Optionally, it can include instances set on
[AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription) children for Eyebrow, Eyelash, and Hair
[AccessoryTypes](/docs/reference/engine/enums/AccessoryType).

Provide feedback

---

Events

AvatarAssetModerationCompleted

Fires when an in-experience-created avatar asset's moderation status has
been updated from pending.

AvatarCreationService.AvatarAssetModerationCompleted(

assetId:[number](/docs/luau/numbers), moderationStatus:[Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| assetId:[number](/docs/luau/numbers)  The asset ID of the asset that has completed moderation. |
| moderationStatus:[Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus)  The final [Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus) result after moderation completed. |

Fires when an in-experience-created avatar asset's moderation status has
been updated from pending. This event provides a streamlined way to know
when an avatar asset created through
[PromptCreateAvatarAssetAsync()](/docs/reference/engine/classes/AvatarCreationService#PromptCreateAvatarAssetAsync)
has completed the moderation process and is ready for use in-experience.

Note that this event only fires for avatar assets created within the
current experience and will trigger when the [Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus)
changes from [NotReviewed](/docs/reference/engine/enums/ModerationStatus#NotReviewed) to any other
status. The event fires on the client only.

Code Samples

```
local AvatarCreationService = game:GetService("AvatarCreationService")



local conn = AvatarCreationService.AvatarAssetModerationCompleted:Connect(function(assetId, moderationStatus)



print("Asset, " .. assetId .. ", ready with moderation status: " .. moderationStatus)



end)
```

Provide feedback

---

AvatarModerationCompleted

Fires when an in-experience-created avatar's moderation status has been
updated from pending.

AvatarCreationService.AvatarModerationCompleted(

outfitId:[number](/docs/luau/numbers), moderationStatus:[Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| outfitId:[number](/docs/luau/numbers)  The outfit ID of the avatar that has completed moderation. |
| moderationStatus:[Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus)  The final [Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus) result after moderation completion. |

Fires when an in-experience-created avatar's moderation status has been
updated from pending. This event provides a streamlined way to know when
an avatar created through
[PromptCreateAvatarAsync()](/docs/reference/engine/classes/AvatarCreationService#PromptCreateAvatarAsync)
has completed the moderation process and is ready for use in-experience.

Note that this event only fires for avatars created within the current
experience and will trigger when the [Enum.ModerationStatus](/docs/reference/engine/enums/ModerationStatus) changes from
[NotReviewed](/docs/reference/engine/enums/ModerationStatus#NotReviewed) to any other status. The
event fires on the client only.
[GetOutfitDetails](/docs/reference/engine/classes/AvatarEditorService#GetOutfitDetails) can be used
on the server to verify the current moderation status if needed.

Provide feedback

---