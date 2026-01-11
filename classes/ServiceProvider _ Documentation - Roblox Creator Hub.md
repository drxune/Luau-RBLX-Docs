# ServiceProvider | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ServiceProvider
Scraped: 2026-01-11T02:29:04.257694Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- ServiceProvider
- DataModel
- GenericSettings
- Debris
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ServiceProvider](/docs/reference/engine/classes/ServiceProvider)

English

Feedback

Engine Class

ServiceProvider

A ServiceProvider is an abstract class, which stores, and provides certain
singleton classes, depending on what inherited class you are using its members
with.

Not Creatable

Not Browsable

---

Summary

Methods

|  |
| --- |
| [FindService](#FindService)(className: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetService](#GetService)(className: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [getService](#getService)(className: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [service](#service)(className: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |

Events

|  |
| --- |
| [Close](#Close)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ServiceAdded](#ServiceAdded)(service: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ServiceRemoving](#ServiceRemoving)(service: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[DataModel](/docs/reference/engine/classes/DataModel), [GenericSettings](/docs/reference/engine/classes/GenericSettings)

A ServiceProvider is an abstract class, which stores, and provides certain
singleton classes, depending on what inherited class you are using its members
with.

---

API Reference

Methods

FindService

Write Parallel

Returns the service specified by the given className if it's already
created, errors for an invalid name.

ServiceProvider:FindService(className:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings) |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Returns the service specified by the given className if it's already
created, errors for an invalid name.

Code Samples

ServiceProvider:FindService

```
print(game:FindService("Part"))



--> nil



print(game:FindService("Workspace"))



--> Workspace
```

Provide feedback

---

GetService

Returns the service with the requested class name, creating it if it does
not exist.

ServiceProvider:GetService(className:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  The class name of the requested service. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

An instance of the requested service.

Returns a service with the class name requested. When called with the name
of a service (such as [Debris](/docs/reference/engine/classes/Debris)) it will return the instance of that
service. If the service does not yet exist it will be created and the new
service is returned. This is the only way to create some services, and can
also be used for services that have unusual names, e.g. RunService's name
is "Run Service".

Note:

* This function will return nil if the className parameter is an
  existing class, but the class is not a service.
* If you attempt to fetch a service that is present under another Object,
  an error will be thrown stating that the "singleton serviceName already
  exists".

Code Samples

ServiceProvider:GetService

```
local BadgeService = game:GetService("BadgeService")



local GameSettings = UserSettings():GetService("UserGameSettings")



print(BadgeService)



print(GameSettings)
```

Provide feedback

---

getService

Deprecated

Show details

---

service

Deprecated

Show details

---

Events

Close

Fires when the current place is exited.

ServiceProvider.Close():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the current place is exited.

Code Samples

ServiceProvider.Close

This example prints "The place is closing" when the game.Close event fires.

```
local function onClose()



print("The place is closing")



end



game.Close:Connect(onClose)
```

Provide feedback

---

ServiceAdded

Fired when a service is created.

ServiceProvider.ServiceAdded(service:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| service:[Instance](/docs/reference/engine/datatypes/Instance) |

Fired when a service is created.

Provide feedback

---

ServiceRemoving

Fired when a service is about to be removed.

ServiceProvider.ServiceRemoving(service:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| service:[Instance](/docs/reference/engine/datatypes/Instance) |

Fired when a service is about to be removed.

Provide feedback

---