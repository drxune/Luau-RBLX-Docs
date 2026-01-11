# Controller | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Controller
Scraped: 2026-01-11T02:30:29.874853Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- Controller
- HumanoidController
- SkateboardController
- VehicleController
- LocalScript
- Controller:GetButton()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Controller](/docs/reference/engine/classes/Controller)

English

Feedback

Engine Class

![Controller](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Controller-Dark.webp)Controller

The base class for controller objects, such as the [HumanoidController](/docs/reference/engine/classes/HumanoidController)
object.

Not Creatable

---

Summary

Methods

|  |
| --- |
| [BindButton](#BindButton)(button: [Enum.Button](/docs/reference/engine/enums/Button),caption: [string](/docs/luau/strings)):() |
| [bindButton](#bindButton)(button: [Enum.Button](/docs/reference/engine/enums/Button),caption: [string](/docs/luau/strings)):()  Deprecated |
| [GetButton](#GetButton)(button: [Enum.Button](/docs/reference/engine/enums/Button)):[boolean](/docs/luau/booleans) |
| [getButton](#getButton)(button: [Enum.Button](/docs/reference/engine/enums/Button)):[boolean](/docs/luau/booleans)  Deprecated |
| [UnbindButton](#UnbindButton)(button: [Enum.Button](/docs/reference/engine/enums/Button)):() |

Events

|  |
| --- |
| [ButtonChanged](#ButtonChanged)(button: [Enum.Button](/docs/reference/engine/enums/Button)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[HumanoidController](/docs/reference/engine/classes/HumanoidController), [SkateboardController](/docs/reference/engine/classes/SkateboardController), [VehicleController](/docs/reference/engine/classes/VehicleController)

The base class for controller objects, such as the [HumanoidController](/docs/reference/engine/classes/HumanoidController)
object.

---

API Reference

Methods

BindButton

Activates an overriding bind on the specified button.

Controller:BindButton(

button:[Enum.Button](/docs/reference/engine/enums/Button), caption:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| button:[Enum.Button](/docs/reference/engine/enums/Button) |
| caption:[string](/docs/luau/strings) |

Returns

()

Activates an overriding bind on the specified button.

Code Samples

Controller:BindButton1

The example below when placed inside a [LocalScript](/docs/reference/engine/classes/LocalScript), would result in a
GUI saying "Press Backspace to win!".

```
local ControllerService = game:GetService("ControllerService")



local humanoidController = ControllerService:FindFirstChildOfClass("HumanoidController")



humanoidController:BindButton(Enum.Button.Dismount, "win!")
```

Provide feedback

---

bindButton

Deprecated

Show details

---

GetButton

Returns whether or not Button is being pressed.

Controller:GetButton(button:[Enum.Button](/docs/reference/engine/enums/Button)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| button:[Enum.Button](/docs/reference/engine/enums/Button) |

Returns

[boolean](/docs/luau/booleans)

Returns whether or not Button is being pressed.

Provide feedback

---

getButton

Deprecated

Show details

---

UnbindButton

Removes the bind on button.

Controller:UnbindButton(button:[Enum.Button](/docs/reference/engine/enums/Button)):()

Parameters

|  |
| --- |
| button:[Enum.Button](/docs/reference/engine/enums/Button) |

Returns

()

Removes the bind on button.

Provide feedback

---

Events

ButtonChanged

Fired when the pressed state of a bound button is changed. This event can
be used in conjunction with [Controller:GetButton()](/docs/reference/engine/classes/Controller#GetButton) to see whether
a bound button is being pressed down or not.

Controller.ButtonChanged(button:[Enum.Button](/docs/reference/engine/enums/Button)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| button:[Enum.Button](/docs/reference/engine/enums/Button) |

Fired when the pressed state of a bound button is changed. This event can
be used in conjunction with [Controller:GetButton()](/docs/reference/engine/classes/Controller#GetButton) to see whether
a bound button is being pressed down or not.

Provide feedback

---