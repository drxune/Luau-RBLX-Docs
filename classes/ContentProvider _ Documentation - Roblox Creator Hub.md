# ContentProvider | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ContentProvider
Scraped: 2026-01-11T02:36:26.729599Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- ContentProvider
- Object
- ContentProvider:PreloadAsync()
- Workspace
- ContentProvider:SetBaseUrl()
- GetAssetFetchStatusChangedSignal()
- Instances
- Decal
- Sound
- SurfaceAppearance
- MaterialVariant
- PreloadAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ContentProvider](/docs/reference/engine/classes/ContentProvider)

English

Feedback

Engine Class

ContentProvider

Service that is used to load content, or assets, into a game.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [BaseUrl](#BaseUrl):[string](/docs/luau/strings) |
| [RequestQueueSize](#RequestQueueSize):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetAssetFetchStatus](#GetAssetFetchStatus)(contentId: ContentId):[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) |
| [GetAssetFetchStatusChangedSignal](#GetAssetFetchStatusChangedSignal)(contentId: ContentId):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ListEncryptedAssets](#ListEncryptedAssets)():[Array](/docs/luau/tables#arrays) |
| [Preload](#Preload)(contentId: ContentId):()  Deprecated |
| [PreloadAsync](#PreloadAsync)(contentIdList: [Array](/docs/luau/tables#arrays),callbackFunction: [function](/docs/luau/functions)):() |
| [RegisterDefaultEncryptionKey](#RegisterDefaultEncryptionKey)(encryptionKey: [string](/docs/luau/strings)):() |
| [RegisterDefaultSessionKey](#RegisterDefaultSessionKey)(sessionKey: [string](/docs/luau/strings)):() |
| [RegisterEncryptedAsset](#RegisterEncryptedAsset)(assetId: ContentId,encryptionKey: [string](/docs/luau/strings)):() |
| [RegisterSessionEncryptedAsset](#RegisterSessionEncryptedAsset)(contentId: ContentId,sessionKey: [string](/docs/luau/strings)):() |
| [UnregisterDefaultEncryptionKey](#UnregisterDefaultEncryptionKey)():() |
| [UnregisterEncryptedAsset](#UnregisterEncryptedAsset)(assetId: ContentId):() |

Events

|  |
| --- |
| [AssetFetchFailed](#AssetFetchFailed)(assetId: ContentId):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Service that loads content (assets) into a game.

Roblox servers stream all assets to the client at runtime: objects in the
Workspace, mesh assets, texture assets, etc. Assets such as mesh visual data,
textures, decals, and sounds are streamed in as required, regardless of
whether [Streaming](/docs/workspace/streaming) is enabled.

In some cases, this behavior is undesirable, as it can lead to a delay before
the content loads into the experience.

ContentProvider lets you preload assets into an experience using the
[ContentProvider:PreloadAsync()](/docs/reference/engine/classes/ContentProvider#PreloadAsync) method. You might want to display a
loading screen, preload critical assets, and only then allow the player into
the experience.

#### Best Practices for Preloading

* Only preload essential assets, not the entire [Workspace](/docs/reference/engine/classes/Workspace). You
  might get occasional pop-in, but it decreases load times and generally
  doesn't disrupt the player experience. Assets that are good candidates for
  preloading include those required for the loading screen, the UI, or the
  starting area.
* Let players skip the loading screen, or automatically skip it after a
  certain amount of time.

Code Samples

ContentProvider

In this example a Decal and Sound are preloaded into a game. Once they have
finished loading the script will print a message to the output.

```
local ContentProvider = game:GetService("ContentProvider")



local LOGO_ID = "rbxassetid://658743164"



local PAGE_TURN_ID = "rbxassetid://12222076"



local decal = Instance.new("Decal")



decal.ColorMapContent = LOGO_ID



local sound = Instance.new("Sound")



sound.SoundId = PAGE_TURN_ID



local assets = { decal, sound }



ContentProvider:PreloadAsync(assets)



print("All assets loaded.")
```

---

API Reference

Properties

BaseUrl

Read Only

Not Replicated

Read Parallel

Used by the [ContentProvider](/docs/reference/engine/classes/ContentProvider) to download assets from the Roblox
website.

ContentProvider.BaseUrl:[string](/docs/luau/strings)

Used by the [ContentProvider](/docs/reference/engine/classes/ContentProvider) to download assets from the Roblox
website.

This URL points to a Roblox hosted website from which assets are
downloaded and is pulled from the AppSettings.xml file, located in the
version-hash folder.

It is possible to overwrite this property using the
[ContentProvider:SetBaseUrl()](/docs/reference/engine/classes/ContentProvider#SetBaseUrl) function in the command bar; however,
this is not recommended and may cause asset loading issues.

Provide feedback

---

RequestQueueSize

Read Only

Not Replicated

Read Parallel

Gives the number of items in the [ContentProvider](/docs/reference/engine/classes/ContentProvider) request queue
that need to be downloaded.

ContentProvider.RequestQueueSize:[number](/docs/luau/numbers)

Gives the number of items in the [ContentProvider](/docs/reference/engine/classes/ContentProvider) request queue
that need to be downloaded.

Items are added to the client's request queue when an asset is used for
the first time or [ContentProvider:PreloadAsync()](/docs/reference/engine/classes/ContentProvider#PreloadAsync) is called.

Developers are advised not to use RequestQueueSize to create loading bars.
This is because the queue size can both increase and decrease over time as
new assets are added and downloaded. Developers looking to display loading
progress should load assets one at a time (see example below).

Code Samples

ContentProvider Loading Bar

This code sample demonstrates how [ContentProvider:PreloadAsync()](/docs/reference/engine/classes/ContentProvider#PreloadAsync) can
be used to create a simple loading bar in a game, by loading the assets one at
a time.

```
local ContentProvider = game:GetService("ContentProvider")



local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



local playerGui = localPlayer:WaitForChild("PlayerGui")



local screenGui = Instance.new("ScreenGui")



screenGui.Parent = playerGui



-- create a basic loading bar



local frame = Instance.new("Frame")



frame.Size = UDim2.new(0.5, 0, 0.1, 0)



frame.Position = UDim2.new(0.5, 0, 0.5, 0)



frame.AnchorPoint = Vector2.new(0.5, 0.5)



frame.Parent = screenGui



local bar = Instance.new("Frame")



bar.Size = UDim2.new(0, 0, 1, 0)



bar.Position = UDim2.new(0, 0, 0, 0)



bar.BackgroundColor3 = Color3.new(0, 0, 1)



bar.Parent = frame



local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



local sound2 = Instance.new("Sound")



sound2.SoundId = "rbxassetid://9120385974"



local assets = {



sound,



sound2,



}



task.wait(3)



for i = 1, #assets do



local asset = assets[i]



ContentProvider:PreloadAsync({ asset }) -- 1 at a time, yields



local progress = i / #assets



bar.Size = UDim2.new(progress, 0, 1, 0)



end



print("loading done")
```

Provide feedback

---

Methods

GetAssetFetchStatus

Gets the current [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) of the contentId provided.

ContentProvider:GetAssetFetchStatus(contentId:ContentId):[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)

Parameters

|  |
| --- |
| contentId:ContentId  The ID of the content to fetch the status for. |

Returns

[Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus)

The [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) of the content.

Gets the current [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) of the contentId provided. Use
[GetAssetFetchStatusChangedSignal()](/docs/reference/engine/classes/ContentProvider#GetAssetFetchStatusChangedSignal)
to listen for changes to this value.

Code Samples

Monitoring AssetFetchStatus

Retrieves the initial [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) of an asset and listens for future updates.

```
local ContentProvider = game:GetService("ContentProvider")



-- An example asset to load



local ASSET_ID = "rbxassetid://9120386436"



local exampleAsset = Instance.new("Sound")



exampleAsset.SoundId = ASSET_ID



-- Output the current AssetFetchStatus of the asset



local initialAssetFetchStatus = ContentProvider:GetAssetFetchStatus(ASSET_ID)



print("Initial AssetFetchStatus:", initialAssetFetchStatus)



-- Listen for updates



local assetFetchStatusChangedSignal = ContentProvider:GetAssetFetchStatusChangedSignal(ASSET_ID)



local function onAssetFetchStatusChanged(newAssetFetchStatus: Enum.AssetFetchStatus)



print(`New AssetFetchStatus: {newAssetFetchStatus}`)



end



assetFetchStatusChangedSignal:Connect(onAssetFetchStatusChanged)



-- Trigger the asset to preload



local function onAssetRequestComplete(contentId: string, assetFetchStatus: Enum.AssetFetchStatus)



print(`Preload status {contentId}: {assetFetchStatus.Name}`)



end



ContentProvider:PreloadAsync({ exampleAsset }, onAssetRequestComplete)
```

Provide feedback

---

GetAssetFetchStatusChangedSignal

A signal that fires when the [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) of the provided
content changes.

ContentProvider:GetAssetFetchStatusChangedSignal(contentId:ContentId):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| contentId:ContentId |

Returns

[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

A signal that fires when the [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) of the provided
content changes. Connect to this signal by using a callback with one
argument of type [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus). This is particularly useful for
assets that might update themselves automatically like the thumbnail of a
user when they change clothes.

Code Samples

Monitoring AssetFetchStatus

Retrieves the initial [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus) of an asset and listens for future updates.

```
local ContentProvider = game:GetService("ContentProvider")



-- An example asset to load



local ASSET_ID = "rbxassetid://9120386436"



local exampleAsset = Instance.new("Sound")



exampleAsset.SoundId = ASSET_ID



-- Output the current AssetFetchStatus of the asset



local initialAssetFetchStatus = ContentProvider:GetAssetFetchStatus(ASSET_ID)



print("Initial AssetFetchStatus:", initialAssetFetchStatus)



-- Listen for updates



local assetFetchStatusChangedSignal = ContentProvider:GetAssetFetchStatusChangedSignal(ASSET_ID)



local function onAssetFetchStatusChanged(newAssetFetchStatus: Enum.AssetFetchStatus)



print(`New AssetFetchStatus: {newAssetFetchStatus}`)



end



assetFetchStatusChangedSignal:Connect(onAssetFetchStatusChanged)



-- Trigger the asset to preload



local function onAssetRequestComplete(contentId: string, assetFetchStatus: Enum.AssetFetchStatus)



print(`Preload status {contentId}: {assetFetchStatus.Name}`)



end



ContentProvider:PreloadAsync({ exampleAsset }, onAssetRequestComplete)
```

Provide feedback

---

ListEncryptedAssets

ContentProvider:ListEncryptedAssets():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Preload

Deprecated

Show details

---

PreloadAsync

Yields

Yields until all of the assets associated with the given
[Instances](/docs/reference/engine/classes/Instance) have loaded.

ContentProvider:PreloadAsync(

contentIdList:[Array](/docs/luau/tables#arrays), callbackFunction:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| contentIdList:[Array](/docs/luau/tables#arrays)  An array of instances to load. |
| callbackFunction:[function](/docs/luau/functions) Default Value: "nil" The function called when each asset request completes. Returns the [content](/docs/reference/engine/datatypes/Content) string and the asset's final [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus). |

Returns

()

Yields until all of the assets associated with the given
[Instances](/docs/reference/engine/classes/Instance) have loaded. This can be used to pause a script
and not use content until it is certain that the content has been loaded
into the experience.

When called, the engine identifies links to content for each item in the
list. For any of the [Instances](/docs/reference/engine/classes/Instance) which have properties that
define links to content, such as a [Decal](/docs/reference/engine/classes/Decal) or a
[Sound](/docs/reference/engine/classes/Sound), the engine attempts to load these assets from Roblox.
For each requested asset, the callback function runs, indicating the
asset's final [Enum.AssetFetchStatus](/docs/reference/engine/enums/AssetFetchStatus).

If any of the assets fail to load, an error message appears in the output.
The method itself will not error and it will continue executing until it
has processed each requested instance.

##### Limitations

[SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) and [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) are not supported by
[PreloadAsync()](/docs/reference/engine/classes/ContentProvider#PreloadAsync) because these
objects rely on processed texture pack assets rather than directly loading
individual textures. Calling it on a [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) instance
will not do anything, but the associated textures will still be streamed
in during runtime.

Code Samples

Preloading Assets

In this code sample, a sound and a texture are preloaded using [Sound](/docs/reference/engine/classes/Sound) and
[Decal](/docs/reference/engine/classes/Decal) instances.

```
local ContentProvider = game:GetService("ContentProvider")



local sound = Instance.new("Sound")



sound.SoundId = "rbxassetid://9120386436"



local decal = Instance.new("Decal")



decal.ColorMapContent = "rbxassetid://5447528495"



local assets = {



decal,



sound,



}



-- This will be hit as each asset resolves



local callback = function(assetId, assetFetchStatus)



print("PreloadAsync() resolved asset ID:", assetId)



print("PreloadAsync() final AssetFetchStatus:", assetFetchStatus)



end



-- Preload the content and time it



local startTime = os.clock()



ContentProvider:PreloadAsync(assets, callback)



local deltaTime = os.clock() - startTime



print(("Preloading complete, took %.2f seconds"):format(deltaTime))
```

Provide feedback

---

RegisterDefaultEncryptionKey

ContentProvider:RegisterDefaultEncryptionKey(encryptionKey:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| encryptionKey:[string](/docs/luau/strings) |

Returns

()

Provide feedback

---

RegisterDefaultSessionKey

ContentProvider:RegisterDefaultSessionKey(sessionKey:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| sessionKey:[string](/docs/luau/strings) |

Returns

()

Provide feedback

---

RegisterEncryptedAsset

ContentProvider:RegisterEncryptedAsset(

assetId:ContentId, encryptionKey:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| assetId:ContentId |
| encryptionKey:[string](/docs/luau/strings) |

Returns

()

Provide feedback

---

RegisterSessionEncryptedAsset

ContentProvider:RegisterSessionEncryptedAsset(

contentId:ContentId, sessionKey:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| contentId:ContentId |
| sessionKey:[string](/docs/luau/strings) |

Returns

()

Provide feedback

---

UnregisterDefaultEncryptionKey

ContentProvider:UnregisterDefaultEncryptionKey():()

Returns

()

Provide feedback

---

UnregisterEncryptedAsset

ContentProvider:UnregisterEncryptedAsset(assetId:ContentId):()

Parameters

|  |
| --- |
| assetId:ContentId |

Returns

()

Provide feedback

---

Events

AssetFetchFailed

ContentProvider.AssetFetchFailed(assetId:ContentId):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| assetId:ContentId |

Provide feedback

---