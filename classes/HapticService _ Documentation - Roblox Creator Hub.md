# HapticService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HapticService
Scraped: 2026-01-11T02:32:05.791805Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- HapticService
- HapticEffect
- UserInputType
- SetMotor()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [HapticService](/docs/reference/engine/classes/HapticService)

English

Feedback

Engine Class

![HapticService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/HapticService-Dark.webp)HapticService

Deprecated

Provides haptic feedback to controllers and devices.

Not Creatable

Service

Not Replicated

This service has been superseded by [HapticEffect](/docs/reference/engine/classes/HapticEffect), a newer instance
that supports multiple haptic effect types, looped effects, and customizable
haptics.

---

Summary

Methods

|  |
| --- |
| [GetMotor](#GetMotor)(inputType: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),vibrationMotor: [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor)):[Tuple](/docs/luau/tuples) |
| [IsMotorSupported](#IsMotorSupported)(inputType: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),vibrationMotor: [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor)):[boolean](/docs/luau/booleans) |
| [IsVibrationSupported](#IsVibrationSupported)(inputType: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans) |
| [SetMotor](#SetMotor)(inputType: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),vibrationMotor: [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor),vibrationValues: [Tuple](/docs/luau/tuples)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Methods

GetMotor

Returns the current vibration value set to the specified
[UserInputType](/docs/reference/engine/classes/InputObject#UserInputType) and [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor).

HapticService:GetMotor(

inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), vibrationMotor:[Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType). |
| vibrationMotor:[Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor)  The specified [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor). |

Returns

[Tuple](/docs/luau/tuples)

The current vibration value set to the specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)
and [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor) or nil if
[SetMotor()](/docs/reference/engine/classes/HapticService#SetMotor) has not been called prior.

Returns the current vibration value set to the specified
[UserInputType](/docs/reference/engine/classes/InputObject#UserInputType) and [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor).
This will not return anything if
[SetMotor()](/docs/reference/engine/classes/HapticService#SetMotor) has not been called prior.

Provide feedback

---

IsMotorSupported

Returns true if the specified motor is available to be used with the
specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType).

HapticService:IsMotorSupported(

inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), vibrationMotor:[Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The specific [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) being checked for [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor) support. |
| vibrationMotor:[Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor)  The specified [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor) checked to see if it supports the specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType). |

Returns

[boolean](/docs/luau/booleans)

Boolean of true if the specified motor is available to be used with
the specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType), false if not.

Returns true if the specified motor is available to be used with the
specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType).

Provide feedback

---

IsVibrationSupported

Returns true if the specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) supports haptic
feedback.

HapticService:IsVibrationSupported(inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) checked to see if it supports haptic feedback. |

Returns

[boolean](/docs/luau/booleans)

Boolean of true if the specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) supports
haptic feedback.

Returns true if the specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) supports haptic
feedback.

Provide feedback

---

SetMotor

Sets the vibration intensity of the specified
[UserInputType](/docs/reference/engine/classes/InputObject#UserInputType) and [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor).

HapticService:SetMotor(

inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), vibrationMotor:[Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor), vibrationValues:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| inputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The specified [Enum.UserInputType](/docs/reference/engine/enums/UserInputType). |
| vibrationMotor:[Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor)  The specified [Enum.VibrationMotor](/docs/reference/engine/enums/VibrationMotor). |
| vibrationValues:[Tuple](/docs/luau/tuples)  How intensely the motor should vibrate. Only uses the first value in the tuple, which should be a number. |

Returns

()

Sets the vibration intensity of the specified inputType and
vibrationMotor. Note that almost all usage cases specify
[Enum.UserInputType.Gamepad1](/docs/reference/engine/enums/UserInputType#Gamepad1) for inputType which is internally mapped
to the device's respective hardware.

Code Samples

HapticService:SetMotor()

This example makes the small motor vibrate depending on how much pressure is
applied to the left trigger, and the large motor vibrate depending on how much
pressure is applied to the right trigger.

```
local UserInputService = game:GetService("UserInputService")



local HapticService = game:GetService("HapticService")



local cachedInputs = {}



local keyToVibration = {



[Enum.KeyCode.ButtonL2] = Enum.VibrationMotor.Small,



[Enum.KeyCode.ButtonR2] = Enum.VibrationMotor.Large,



}



local function onInputChanged(property)



if property == "Position" then



HapticService:SetMotor(inputType, vibrationMotor, input.Position.Z)



end



end



local function onInputBegan(input)



if not cachedInputs[input] then



local inputType = input.UserInputType



if inputType.Name:find("Gamepad") then



local vibrationMotor = keyToVibration[input.KeyCode]



if vibrationMotor then



-- Watch this input manually to accurately update the vibration motor



cachedInputs[input] = input.Changed:Connect(onInputChanged)



end



end



end



end



UserInputService.InputBegan:Connect(onInputBegan)
```

Provide feedback

---