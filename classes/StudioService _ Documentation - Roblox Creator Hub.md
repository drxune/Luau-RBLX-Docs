# StudioService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StudioService
Scraped: 2026-01-11T02:32:02.504064Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- StudioService
- Plugins
- GridSize
- RotateIncrement
- UseLocalSpace
- PromptImportFile
- PromptImportFiles
- File
- GetClassIcon
- ActiveScript
- LuaSourceContainer
- CFrame
- StudioService:PromptImportFiles()
- Files
- StudioService:PromptImportFile()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StudioService](/docs/reference/engine/classes/StudioService)

English

Feedback

Engine Class

StudioService

Provides access to configuration of Roblox Studio and allows importing files
from the user's file system.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [ActiveScript](#ActiveScript):[Instance](/docs/reference/engine/datatypes/Instance) |
| [DraggerSolveConstraints](#DraggerSolveConstraints):[boolean](/docs/luau/booleans) |
| [DrawConstraintsOnTop](#DrawConstraintsOnTop):[boolean](/docs/luau/booleans)  Deprecated |
| [GridSize](#GridSize):[number](/docs/luau/numbers) |
| [RotateIncrement](#RotateIncrement):[number](/docs/luau/numbers) |
| [Secrets](#Secrets):[string](/docs/luau/strings) |
| [ShowConstraintDetails](#ShowConstraintDetails):[boolean](/docs/luau/booleans) |
| [ShowWeldDetails](#ShowWeldDetails):[boolean](/docs/luau/booleans) |
| [StudioLocaleId](#StudioLocaleId):[string](/docs/luau/strings) |
| [UseLocalSpace](#UseLocalSpace):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetClassIcon](#GetClassIcon)(className: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetUserId](#GetUserId)():[number](/docs/luau/numbers) |
| [GizmoRaycast](#GizmoRaycast)(origin: [Vector3](/docs/reference/engine/datatypes/Vector3),direction: [Vector3](/docs/reference/engine/datatypes/Vector3),raycastParams: [RaycastParams](/docs/reference/engine/datatypes/RaycastParams)):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)? |
| [PromptImportFileAsync](#PromptImportFileAsync)(fileTypeFilter: [Array](/docs/luau/tables#arrays)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [PromptImportFile](#PromptImportFile)(fileTypeFilter: [Array](/docs/luau/tables#arrays)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [PromptImportFilesAsync](#PromptImportFilesAsync)(fileTypeFilter: [Array](/docs/luau/tables#arrays)):Instances |
| [PromptImportFiles](#PromptImportFiles)(fileTypeFilter: [Array](/docs/luau/tables#arrays)):Instances  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

StudioService provides access to configuration of Roblox Studio, allows
importing files from the user's file system, and other miscellaneous
information. It is intended to be used by [Plugins](/docs/reference/engine/classes/Plugin) in order to
provide a consistent user experience.

* Plugins that allow the user to move objects may find
  [GridSize](/docs/reference/engine/classes/StudioService#GridSize),
  [RotateIncrement](/docs/reference/engine/classes/StudioService#RotateIncrement) and
  [UseLocalSpace](/docs/reference/engine/classes/StudioService#UseLocalSpace) useful.
* Plugins that require the user to import files should use
  [PromptImportFile](/docs/reference/engine/classes/StudioService#PromptImportFile) or
  [PromptImportFiles](/docs/reference/engine/classes/StudioService#PromptImportFiles) in order to
  receive [File](/docs/reference/engine/classes/File) objects.
* Plugins that display icons of Instance classes can use
  [GetClassIcon](/docs/reference/engine/classes/StudioService#GetClassIcon).
* Plugins that care about which script is currently being edited (if any) can
  read this from [ActiveScript](/docs/reference/engine/classes/StudioService#ActiveScript).

---

API Reference

Properties

ActiveScript

Read Only

Not Replicated

Read Parallel

Reflects the [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) currently being edited (if any).

StudioService.ActiveScript:[Instance](/docs/reference/engine/datatypes/Instance)

ActiveScript refers to the [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) currently being
edited by the user. If the user is not editing a script, this will be
nil. Below is an example that shows how you can use this property to
measure for how long a script was active.

```
local StudioService = game:GetService("StudioService")



local startTime = os.time()



local activeScript



local function onActiveScriptChanged()



local newActiveScript = StudioService.ActiveScript



if activeScript and newActiveScript ~= activeScript then



local deltaTime = os.time() - startTime



print(("You edited %s for %d:%2.d"):format(activeScript.Name, deltaTime // 60, deltaTime % 60))



end



startTime = os.time()



activeScript = newActiveScript



end



StudioService:GetPropertyChangedSignal("ActiveScript"):Connect(onActiveScriptChanged)
```

Provide feedback

---

DraggerSolveConstraints

Read Only

Not Replicated

Read Parallel

StudioService.DraggerSolveConstraints:[boolean](/docs/luau/booleans)

Provide feedback

---

DrawConstraintsOnTop

Deprecated

Show details

---

GridSize

Read Only

Not Replicated

Read Parallel

Determines the distance in studs by which Studio's drag and move tools
move objects each tick.

StudioService.GridSize:[number](/docs/luau/numbers)

GridSize determines the distance in studs by which Studio's drag and
move tools move objects each tick. This is set in the user's toolbar's
Model tab.

Provide feedback

---

RotateIncrement

Read Only

Not Replicated

Read Parallel

Determines the degrees by which Studio's rotation tool will rotate
selected objects each tick.

StudioService.RotateIncrement:[number](/docs/luau/numbers)

RotateIncrement determines the angle in degrees by which Studio's
rotation tool will rotate selected objects each tick. This is set in the
user's toolbar's Model tab.

Provide feedback

---

Secrets

Roblox Script Security

Read Parallel

StudioService.Secrets:[string](/docs/luau/strings)

Provide feedback

---

ShowConstraintDetails

Read Only

Not Replicated

Read Parallel

StudioService.ShowConstraintDetails:[boolean](/docs/luau/booleans)

Provide feedback

---

ShowWeldDetails

Read Only

Not Replicated

Roblox Script Security

Read Parallel

StudioService.ShowWeldDetails:[boolean](/docs/luau/booleans)

Provide feedback

---

StudioLocaleId

Read Only

Not Replicated

Read Parallel

The locale currently in-use by Studio, e.g. en\_US.

StudioService.StudioLocaleId:[string](/docs/luau/strings)

The StudioLocaleId property contains the locale currently in-use by
Studio, e.g. en\_US. It is useful when localizing plugins.

Below is a trivial example of localization based on the value returned by
this function.

```
local locale = game:GetService("StudioService").StudioLocaleId



if locale == "en_US" then



print("Howdy, ya'll")



elseif locale == "en_GB" then



print("'Ello, gov'na")



elseif locale:sub(1, 2) == "en" then



print("Hello")



elseif locale == "fr_FR" then



print("Bonjour")



end
```

Provide feedback

---

UseLocalSpace

Not Replicated

Read Parallel

Determines whether Studio tools will use local space of an object or
global space.

StudioService.UseLocalSpace:[boolean](/docs/luau/booleans)

UseLocalSpace determines whether the Studio movement/rotation tools
will manipulate a part's [CFrame](/docs/reference/engine/classes/BasePart#CFrame) using the local
space of an object or global space. By default, this setting is toggled
with CtrlL or ⌘L. Plugins can
read from this property if they implement their own object movement tools.

Provide feedback

---

Methods

GetClassIcon

Plugin Security

Provides a dictionary that allows the display of a class' Explorer window
icon.

StudioService:GetClassIcon(className:[string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings) |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

GetClassIcon provides a dictionary that allows the display of a class'
Explorer window icon, e.g. calling this function with "Part" returns
property values that display the part icon from the Explorer window.

Below is a literal table representation of the value returned when this
function is called with "Part".

```
{



Image = "rbxasset://textures/ClassImages.png",



ImageRectOffset = Vector2.new(16, 0),



ImageRectSize = Vector2.new(16, 16)



}
```

The utility function below may prove useful when displaying class icons:

```
local StudioService = game:GetService("StudioService")



local imageLabel = script.Parent



local function displayClassIcon(image, className)



for k, v in StudioService:GetClassIcon(className) do



image[k] = v -- Set property



end



end



displayClassIcon(imageLabel, "Part")
```

Provide feedback

---

GetUserId

Plugin Security

Returns the Studio user's userId if they're logged in, otherwise
returns 0.

StudioService:GetUserId():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the Studio user's userId if they're logged in, otherwise
returns 0.

Code Samples

StudioService:GetUserId

The example prints the currently logged in user's ID.

```
-- Can only be used in a plugin



local StudioService = game:GetService("StudioService")



local Players = game:GetService("Players")



local loggedInUserId = StudioService:GetUserId()



local loggedInUserName = Players:GetNameFromUserIdAsync(loggedInUserId)



print("Hello,", loggedInUserName)
```

Provide feedback

---

GizmoRaycast

Plugin Security

StudioService:GizmoRaycast(

origin:[Vector3](/docs/reference/engine/datatypes/Vector3), direction:[Vector3](/docs/reference/engine/datatypes/Vector3), raycastParams:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams)

):[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Parameters

|  |
| --- |
| origin:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| direction:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| raycastParams:[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) Default Value: "RaycastParams{IgnoreWater=false, BruteForceAllSlow=false, RespectCanCollide=false, CollisionGroup=Default, FilterDescendantsInstances={}}" |

Returns

[RaycastResult](/docs/reference/engine/datatypes/RaycastResult)?

Provide feedback

---

PromptImportFileAsync

Yields

Plugin Security

Prompts the current Studio user to select one file to add as a
[File](/docs/reference/engine/classes/File).

StudioService:PromptImportFileAsync(fileTypeFilter:[Array](/docs/luau/tables#arrays)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| fileTypeFilter:[Array](/docs/luau/tables#arrays) Default Value: "{}" A list of file types that the user is allowed to select. File types are formatted without a period. For example, {"jpg", "png"} would allow only a JPG or PNG file to be selected. If no filter is provided, the filter is nil and allows the user to select any file type. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The imported [File](/docs/reference/engine/classes/File). Returns nil if no files were selected, or
if the selected file was too large (FileSize greater than 100
megabytes).

This function prompts the current Studio user to select one file, which
will then be loaded as a [File](/docs/reference/engine/classes/File).

See also:

* [StudioService:PromptImportFiles()](/docs/reference/engine/classes/StudioService#PromptImportFiles), the same function but for
  loading a list of files instead of a single file

Provide feedback

---

PromptImportFile

Deprecated

Show details

---

PromptImportFilesAsync

Yields

Plugin Security

Prompts the current Studio user to select files to add as
[Files](/docs/reference/engine/classes/File).

StudioService:PromptImportFilesAsync(fileTypeFilter:[Array](/docs/luau/tables#arrays)):Instances

Parameters

|  |
| --- |
| fileTypeFilter:[Array](/docs/luau/tables#arrays) Default Value: "{}" A list of file types that the user is allowed to select. File types are formatted without a period. For example, {"jpg", "png"} would allow only JPG and PNG files to be selected. If no filter is provided, the filter is nil and allows the user to select any file type. |

Returns

Instances

The imported [Files](/docs/reference/engine/classes/File). Returns an empty list if no files
were selected. Returns nil if the user selected one or more files
that were too large (FileSize greater than 100 megabytes).

This function prompts the current Studio user to select one or more files,
which will then be loaded as [Files](/docs/reference/engine/classes/File).

Throws an error if the fileTypeFilter was an empty list.

See also:

* [StudioService:PromptImportFile()](/docs/reference/engine/classes/StudioService#PromptImportFile), the same function but for
  loading a single file instead of a list of files

Provide feedback

---

PromptImportFiles

Deprecated

Show details

---