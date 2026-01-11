# CaptureService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CaptureService
Scraped: 2026-01-11T02:29:04.794294Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- CaptureService
- Capture
- ReadCapturesFromGalleryAsync()
- UploadCaptureAsync()
- CapturesPages
- CaptureScreenshot()
- PromptSaveCapturesToGallery()
- VideoCapture
- StopVideoCapture()
- StartVideoCaptureAsync()
- CaptureBegan
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [CaptureService](/docs/reference/engine/classes/CaptureService)

English

Feedback

Engine Class

CaptureService

A service which provides control over screenshot and video capture features.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [CaptureScreenshot](#CaptureScreenshot)(onCaptureReady: [function](/docs/luau/functions)):() |
| [PromptCaptureGalleryPermissionAsync](#PromptCaptureGalleryPermissionAsync)(captureGalleryPermission: [Enum.CaptureGalleryPermission](/docs/reference/engine/enums/CaptureGalleryPermission)):[boolean](/docs/luau/booleans) |
| [PromptSaveCapturesToGallery](#PromptSaveCapturesToGallery)(captures: [Array](/docs/luau/tables#arrays),resultCallback: [function](/docs/luau/functions)):() |
| [PromptShareCapture](#PromptShareCapture)(captureContent: [Content](/docs/reference/engine/datatypes/Content),launchData: [string](/docs/luau/strings),onAcceptedCallback: [function](/docs/luau/functions),onDeniedCallback: [function](/docs/luau/functions)):() |
| [ReadCapturesFromGalleryAsync](#ReadCapturesFromGalleryAsync)(captureTypeFilters: [Array](/docs/luau/tables#arrays)):[Tuple](/docs/luau/tuples) |
| [StartVideoCaptureAsync](#StartVideoCaptureAsync)(onCaptureReady: [function](/docs/luau/functions),captureParams: [Dictionary](/docs/luau/tables#dictionaries)):[Enum.VideoCaptureStartedResult](/docs/reference/engine/enums/VideoCaptureStartedResult) |
| [StopVideoCapture](#StopVideoCapture)():() |
| [UploadCaptureAsync](#UploadCaptureAsync)(capture: [Capture](/docs/reference/engine/classes/Capture)):[Tuple](/docs/luau/tuples) |

Events

|  |
| --- |
| [CaptureBegan](#CaptureBegan)(captureType: [Enum.CaptureType](/docs/reference/engine/enums/CaptureType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [CaptureEnded](#CaptureEnded)(captureType: [Enum.CaptureType](/docs/reference/engine/enums/CaptureType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [CaptureSaved](#CaptureSaved)(captureInfo: [Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [UserCaptureSaved](#UserCaptureSaved)(captureContentId: ContentId):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

CaptureService is a client-side service that allows developers to control
how the screenshot and video capture feature integrates with their
experiences. It can be used to include preset moments where a capture is
automatically taken for a user, and that user can then save, share, or delete
the capture.

---

API Reference

Methods

CaptureScreenshot

Takes a screenshot and provides a temporary contentId to identify it.

CaptureService:CaptureScreenshot(onCaptureReady:[function](/docs/luau/functions)):()

Parameters

|  |
| --- |
| onCaptureReady:[function](/docs/luau/functions)  A callback function that is called with the contentId of the new capture once it is ready. |

Returns

()

This method captures a screenshot for the user but does not immediately
save it to their Captures gallery within the experience's main menu.
Instead, a temporary contentId is created to identify the new capture.

Note that any screenshots taken by this method will not be accessible via
[ReadCapturesFromGalleryAsync()](/docs/reference/engine/classes/CaptureService#ReadCapturesFromGalleryAsync)
or be uploadable via
[UploadCaptureAsync()](/docs/reference/engine/classes/CaptureService#UploadCaptureAsync).

The onCaptureReady callback can be used to prompt the user to save or
share the screenshot:

```
local CaptureService = game:GetService("CaptureService")



-- Reference to an ImageLabel parent of the script containing this code



local imageLabel = script.Parent



local function onCaptureReady(contentId)



imageLabel.Image = contentId



end



CaptureService:CaptureScreenshot(onCaptureReady)
```

Provide feedback

---

PromptCaptureGalleryPermissionAsync

Yields

CaptureService:PromptCaptureGalleryPermissionAsync(captureGalleryPermission:[Enum.CaptureGalleryPermission](/docs/reference/engine/enums/CaptureGalleryPermission)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| captureGalleryPermission:[Enum.CaptureGalleryPermission](/docs/reference/engine/enums/CaptureGalleryPermission)  An [Enum.CaptureGalleryPermission](/docs/reference/engine/enums/CaptureGalleryPermission) representing the type of access for which the user will be prompted. |

Returns

[boolean](/docs/luau/booleans)

A boolean representing whether or not the user has allowed access to
their captures.

This client-side function prompts a user for permission to access their
local captures. Once they have accepted or rejected the prompt, it returns
a boolean representing their choice. This function is a necessary
prerequisite to ReadCapturesFromGalleryAsync and UploadCaptureAsync,
as both of these require gallery permissions to work.

Code Samples

Prompt capture gallery permission

This code snippet demonstrates how to prompt a user for access to their captures gallery.

```
local CaptureService = game:GetService("CaptureService")



local function isGalleryAccessGranted()



local accepted = CaptureService:PromptCaptureGalleryPermissionAsync(Enum.CaptureGalleryPermission.ReadAndUpload)



return accepted



end
```

Provide feedback

---

PromptSaveCapturesToGallery

Prompts the user to save specified captures to their gallery.

CaptureService:PromptSaveCapturesToGallery(

captures:[Array](/docs/luau/tables#arrays), resultCallback:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| captures:[Array](/docs/luau/tables#arrays)  An array of content IDs and/or [Capture](/docs/reference/engine/classes/Capture) objects. |
| resultCallback:[function](/docs/luau/functions)  A callback function that will be invoked with a dictionary mapping each contentId and/or [Capture](/docs/reference/engine/classes/Capture) object to a boolean indicating if the user accepted saving that capture. |

Returns

()

This method prompts the user to save the captures identified by the
provided contentIds or [Capture](/docs/reference/engine/classes/Capture) objects to their Captures
gallery within the experience's main menu.

Provide feedback

---

PromptShareCapture

Prompts the user to share a specified capture.

CaptureService:PromptShareCapture(

captureContent:[Content](/docs/reference/engine/datatypes/Content), launchData:[string](/docs/luau/strings), onAcceptedCallback:[function](/docs/luau/functions), onDeniedCallback:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| captureContent:[Content](/docs/reference/engine/datatypes/Content)  A [Content](/docs/reference/engine/datatypes/Content) containing a contentId or [Capture](/docs/reference/engine/classes/Capture) object. |
| launchData:[string](/docs/luau/strings)  An optional string to include as launch data in the invite link. |
| onAcceptedCallback:[function](/docs/luau/functions)  An optional callback function invoked if the user accepts sharing. |
| onDeniedCallback:[function](/docs/luau/functions)  An optional callback function invoked if the user denies sharing. |

Returns

()

This method prompts the user to share the capture identified by the
provided contentId or [Capture](/docs/reference/engine/classes/Capture) object using the native share
sheet on their device.

The capture is shared along with an invite link to the experience when
supported. Not all devices support including both a screenshot or video
and an invite link.

The launchData will be available in the launchData field for users who
join through the invite link.

For users or devices who are not eligible to use share sheets, this method
prompts them to download the capture instead.

```
local CaptureService = game:GetService("CaptureService")



local function onShareAccepted()



print("Capture share was accepted!")



end



local function onShareDenied()



print("Capture share was denied!")



end



local onCaptureReady = function(result, videoCapture)



if videoCapture then



local captureContent = Content.fromObject(videoCapture)



CaptureService:PromptShareCapture(captureContent, "launchData" , onShareAccepted, onShareDenied)



end



end



CaptureService:StartVideoCaptureAsync(onCaptureReady, {})
```

Provide feedback

---

ReadCapturesFromGalleryAsync

Yields

CaptureService:ReadCapturesFromGalleryAsync(captureTypeFilters:[Array](/docs/luau/tables#arrays)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| captureTypeFilters:[Array](/docs/luau/tables#arrays) Default Value: "{}" An array of [Enum.CaptureType](/docs/reference/engine/enums/CaptureType). |

Returns

[Tuple](/docs/luau/tuples)

Tuple of (result: [Enum.ReadCapturesFromGalleryResult](/docs/reference/engine/enums/ReadCapturesFromGalleryResult), capturesPages:
[CapturesPages](/docs/reference/engine/classes/CapturesPages))

This client-side function returns a paginated list of captures from the
user's gallery as a [CapturesPages](/docs/reference/engine/classes/CapturesPages) object sorted
reverse-chronologically, which can be used to iterate through the
captures. The results can be filtered by capture type with the
captureTypeFilters parameter. If this parameter isn't provided, the
function returns all captures.

Currently, this method will only return captures taken in the experience
where it is called. Additionally, captures taken with
[CaptureScreenshot()](/docs/reference/engine/classes/CaptureService#CaptureScreenshot) and
subsequently saved with
[PromptSaveCapturesToGallery()](/docs/reference/engine/classes/CaptureService#PromptSaveCapturesToGallery)
will not be returned by this method.

Code Samples

Read captures from gallery and iterate over pages

This code snippet demonstrates how to fetch captures from a user gallery, iterate over the result pages, and return all captures.

```
local CaptureService = game:GetService("CaptureService")



local function readCapturesFromGallery()



local allCaptures = {}



local capturesPages



local success, result = pcall(function()



local readResult, pages = CaptureService:ReadCapturesFromGalleryAsync()



if readResult == Enum.ReadCapturesFromGalleryResult.Success then



capturesPages = pages



end



return readResult



end)



if not success or result ~= Enum.ReadCapturesFromGalleryResult.Success then



-- Likely a permissions error, see CaptureService:PromptCaptureGalleryPermissionAsync()



warn("Failed to fetch initial captures: " .. result.Name)



return



end



-- Iterate through current page



local currentPage = capturesPages:GetCurrentPage()



for _, capture in currentPage do



table.insert(allCaptures, capture)



end



-- Advance to next page until finished



while not capturesPages.IsFinished do



local advanceToNextPageSuccess, _ = pcall(function()



capturesPages:AdvanceToNextPageAsync()



end)



if not advanceToNextPageSuccess then



return



end



currentPage = capturesPages:GetCurrentPage()



for _, capture in currentPage do



table.insert(allCaptures, capture)



end



end



return allCaptures



end
```

Provide feedback

---

StartVideoCaptureAsync

Yields

Initiates a video capture recording.

CaptureService:StartVideoCaptureAsync(

onCaptureReady:[function](/docs/luau/functions), captureParams:[Dictionary](/docs/luau/tables#dictionaries)

):[Enum.VideoCaptureStartedResult](/docs/reference/engine/enums/VideoCaptureStartedResult)

Parameters

|  |
| --- |
| onCaptureReady:[function](/docs/luau/functions)  A callback function that is called on video capture completion with a [Enum.VideoCaptureResult](/docs/reference/engine/enums/VideoCaptureResult) and, if successful, a [VideoCapture](/docs/reference/engine/classes/VideoCapture). |
| captureParams:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" |

Returns

[Enum.VideoCaptureStartedResult](/docs/reference/engine/enums/VideoCaptureStartedResult)

This method initiates a video capture recording. The recording will
continue until the
[StopVideoCapture()](/docs/reference/engine/classes/CaptureService#StopVideoCapture) method is
called, or when 30 seconds have passed, whichever comes first. During the
video recording, all user voices are muted.

The onCaptureReady callback can be used to prompt the user to save or
share the video capture.

The captureParams parameter is currently non-operational.

```
local CaptureService = game:GetService("CaptureService")



local parent = script.Parent



local onCaptureReady = function(result, videoCapture)



if result ~= Enum.VideoCaptureResult.Success and result ~= Enum.VideoCaptureResult.TimeLimitReached or not videoCapture then



print("Video recording failed to complete for reason:", result)



else



-- Prompt the user to save the video capture to their gallery



CaptureService:PromptSaveCapturesToGallery({ videoCapture }, function()



print("Capture saved")



end)



end



end



parent.Activated:Connect(function()



local videoRecordingAllowedResult: Enum.VideoCaptureStartedResult = CaptureService:StartVideoCaptureAsync(onCaptureReady, {})



if videoRecordingAllowedResult ~= Enum.VideoCaptureStartedResult.Success then



print("Video recording failed to start for reason:", videoRecordingAllowedResult)



end



end)
```

Provide feedback

---

StopVideoCapture

Ends a video capture initiated by
[StartVideoCaptureAsync()](/docs/reference/engine/classes/CaptureService#StartVideoCaptureAsync).

CaptureService:StopVideoCapture():()

Returns

()

This method ends a video capture that was started by the
[StartVideoCaptureAsync()](/docs/reference/engine/classes/CaptureService#StartVideoCaptureAsync)
method.

Provide feedback

---

UploadCaptureAsync

Yields

CaptureService:UploadCaptureAsync(capture:[Capture](/docs/reference/engine/classes/Capture)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| capture:[Capture](/docs/reference/engine/classes/Capture)  a capture object of type [Capture](/docs/reference/engine/classes/Capture) |

Returns

[Tuple](/docs/luau/tuples)

Tuple of (result: [Enum.UploadCaptureResult](/docs/reference/engine/enums/UploadCaptureResult), assetId: number)

This client-side function uploads a capture, like one retrieved from
ReadCapturesFromGalleryAsync, to the asset system. It returns a tuple of
the result and the asset ID.

Notes:

* This function will only work properly if the Maturity and Compliance
  questionnaire has been filled out for the experience.
* For video capture types, there is an upload limit of 20 videos per day
  per user.
* This function can take up to several minutes to finish executing, and
  the user will need to remain in the experience.

Code Samples

Upload capture to asset system

This code snippet demonstrates how to upload a capture to the asset system.

```
local CaptureService = game:GetService("CaptureService")



local function uploadCapture(capture: Capture)



local success, result = pcall(function()



local uploadCaptureResult, assetId = CaptureService:UploadCaptureAsync(capture)



if uploadCaptureResult ~= Enum.UploadCaptureResult.Success then



-- Handle failure



return nil



end



return assetId



end)



if not success then



-- Handle error



return nil



end



return result



end
```

Provide feedback

---

Events

CaptureBegan

Fires immediately before a capture begins.

CaptureService.CaptureBegan(captureType:[Enum.CaptureType](/docs/reference/engine/enums/CaptureType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| captureType:[Enum.CaptureType](/docs/reference/engine/enums/CaptureType) |

This event fires right before a new capture is taken. It can be used to
customize the capture experience, for example by hiding certain GUI
elements.

Provide feedback

---

CaptureEnded

Fires after a capture finishes.

CaptureService.CaptureEnded(captureType:[Enum.CaptureType](/docs/reference/engine/enums/CaptureType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| captureType:[Enum.CaptureType](/docs/reference/engine/enums/CaptureType) |

This event fires after a new capture completes. It can be used to restore
any changes made when the [CaptureBegan](/docs/reference/engine/classes/CaptureService#CaptureBegan)
event fired.

Provide feedback

---

CaptureSaved

Deprecated

Show details

---

UserCaptureSaved

Fires when the user saves a capture.

CaptureService.UserCaptureSaved(captureContentId:ContentId):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| captureContentId:ContentId  The contentId identifying the screenshot that the user saved. |

This event fires when the user saves a screenshot using the Roblox
screenshot capture UI. It can be used for analytics or to prompt the user
to share their capture.

Provide feedback

---