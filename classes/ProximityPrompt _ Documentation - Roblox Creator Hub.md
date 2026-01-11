# ProximityPrompt | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ProximityPrompt
Scraped: 2026-01-11T02:37:02.859333Z

## Inherits
- Instance
- ProximityPrompt
- LocalizationTable
- Player
- Object
- BasePart
- Attachment
- Model
- PrimaryPart
- Style
- ObjectText
- ActionText
- KeyboardKeyCode
- GamepadKeyCode
- ProximityPromptService
- ProximityPrompt.ActionText
- ProximityPrompt.ObjectText
- ProximityPrompt.RootLocalizationTable
- character
- Camera
- Part
- ProximityPrompt.AutoLocalize
- DataModel
- LocalizationService
- ProximityPrompt.PromptShown
- ProximityPrompt.PromptHidden
- LocalScript
- ProximityPrompt.PromptButtonHoldBegan
- ProximityPrompt.PromptButtonHoldEnded
- ProximityPrompt.HoldDuration
- ProximityPrompt:InputHoldBegin()
- key
- prompt
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)

English

Feedback

Engine Class

![ProximityPrompt](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ProximityPrompt-Dark.webp)ProximityPrompt

An object that lets you prompt players to interact with an object in the 3D
world.

---

Summary

Properties

|  |
| --- |
| [ActionText](#ActionText):[string](/docs/luau/strings) |
| [AutoLocalize](#AutoLocalize):[boolean](/docs/luau/booleans) |
| [ClickablePrompt](#ClickablePrompt):[boolean](/docs/luau/booleans) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Exclusivity](#Exclusivity):[Enum.ProximityPromptExclusivity](/docs/reference/engine/enums/ProximityPromptExclusivity) |
| [GamepadKeyCode](#GamepadKeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [HoldDuration](#HoldDuration):[number](/docs/luau/numbers) |
| [KeyboardKeyCode](#KeyboardKeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [MaxActivationDistance](#MaxActivationDistance):[number](/docs/luau/numbers) |
| [MaxIndicatorDistance](#MaxIndicatorDistance):[number](/docs/luau/numbers) |
| [ObjectText](#ObjectText):[string](/docs/luau/strings) |
| [RequiresLineOfSight](#RequiresLineOfSight):[boolean](/docs/luau/booleans) |
| [RootLocalizationTable](#RootLocalizationTable):[LocalizationTable](/docs/reference/engine/classes/LocalizationTable) |
| [Style](#Style):[Enum.ProximityPromptStyle](/docs/reference/engine/enums/ProximityPromptStyle) |
| [UIOffset](#UIOffset):[Vector2](/docs/reference/engine/datatypes/Vector2) |

Methods

|  |
| --- |
| [InputHoldBegin](#InputHoldBegin)():() |
| [InputHoldEnd](#InputHoldEnd)():() |

Events

|  |
| --- |
| [IndicatorHidden](#IndicatorHidden)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [IndicatorShown](#IndicatorShown)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptButtonHoldBegan](#PromptButtonHoldBegan)(playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptButtonHoldEnded](#PromptButtonHoldEnded)(playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptHidden](#PromptHidden)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptShown](#PromptShown)(inputType: [Enum.ProximityPromptInputType](/docs/reference/engine/enums/ProximityPromptInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Triggered](#Triggered)(playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TriggerEnded](#TriggerEnded)(playerWhoTriggered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The ProximityPrompt instance lets you prompt players to interact with an
object in the 3D world, such as opening a door or picking up an item. A
[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) object works when parented to a [BasePart](/docs/reference/engine/classes/BasePart),
[Attachment](/docs/reference/engine/classes/Attachment), or [Model](/docs/reference/engine/classes/Model) (with
[PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) set) in the workspace. When the player's
character approaches, a UI appears to prompt them for input.

Prompts consist of three primary elements, each of which can be controlled by
the noted properties. The default UI can be swapped out for your own custom
appearance as outlined in [Style](/docs/reference/engine/classes/ProximityPrompt#Style).

![](https://prod.docsiteassets.roblox.com/assets/ui/proximity-prompt/Prompt-Diagram.png)

| Property | Description | Default |
| --- | --- | --- |
| [ObjectText](/docs/reference/engine/classes/ProximityPrompt#ObjectText) | An optional name for the object being interacted with. |  |
| [ActionText](/docs/reference/engine/classes/ProximityPrompt#ActionText) | An optional action name shown to the player. | Interact |
| [KeyboardKeyCode](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode) | The keyboard key which will trigger the prompt. | E |
| [GamepadKeyCode](/docs/reference/engine/classes/ProximityPrompt#GamepadKeyCode) | The gamepad button which will trigger the prompt. | ButtonX |

You can connect to proximity prompt events either on the
[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) object itself or globally through
[ProximityPromptService](/docs/reference/engine/classes/ProximityPromptService). The [ProximityPromptService](/docs/reference/engine/classes/ProximityPromptService) allows you
to manage all proximity prompt behavior from one location, preventing any need
for duplicate code in your experience.

For more information regarding proximity prompts, see the
[Proximity Prompts](/docs/ui/proximity-prompts) guide.

Code Samples

Using a Proximity Prompt with a Seat

In the example below, a user must interact with a chair to sit in it. Paste
this into a Script that is a child of a ProximityPrompt, which is itself a
sibling of a Seat object named *Seat*.

```
local proximityPrompt = script.Parent



local seat = proximityPrompt.Parent.Seat



seat:GetPropertyChangedSignal("Occupant"):Connect(function()



if seat.Occupant then



proximityPrompt.Enabled = false



else



proximityPrompt.Enabled = true



end



end)



proximityPrompt.Triggered:Connect(function(player)



seat:Sit(player.Character.Humanoid)



end)
```

Generating a Custom Proximity Prompt

The example below generates a custom ProximityPrompt UI similar to the
default style, which you may use as a starting point. It should be used in a
LocalScript.

```
local UserInputService = game:GetService("UserInputService")



local ProximityPromptService = game:GetService("ProximityPromptService")



local TweenService = game:GetService("TweenService")



local TextService = game:GetService("TextService")



local Players = game:GetService("Players")



local LocalPlayer = Players.LocalPlayer



local PlayerGui = LocalPlayer:WaitForChild("PlayerGui")



local GamepadButtonImage = {



[Enum.KeyCode.ButtonX] = "rbxasset://textures/ui/Controls/xboxX.png",



[Enum.KeyCode.ButtonY] = "rbxasset://textures/ui/Controls/xboxY.png",



[Enum.KeyCode.ButtonA] = "rbxasset://textures/ui/Controls/xboxA.png",



[Enum.KeyCode.ButtonB] = "rbxasset://textures/ui/Controls/xboxB.png",



[Enum.KeyCode.DPadLeft] = "rbxasset://textures/ui/Controls/dpadLeft.png",



[Enum.KeyCode.DPadRight] = "rbxasset://textures/ui/Controls/dpadRight.png",



[Enum.KeyCode.DPadUp] = "rbxasset://textures/ui/Controls/dpadUp.png",



[Enum.KeyCode.DPadDown] = "rbxasset://textures/ui/Controls/dpadDown.png",



[Enum.KeyCode.ButtonSelect] = "rbxasset://textures/ui/Controls/xboxView.png",



[Enum.KeyCode.ButtonStart] = "rbxasset://textures/ui/Controls/xboxmenu.png",



[Enum.KeyCode.ButtonL1] = "rbxasset://textures/ui/Controls/xboxLB.png",



[Enum.KeyCode.ButtonR1] = "rbxasset://textures/ui/Controls/xboxRB.png",



[Enum.KeyCode.ButtonL2] = "rbxasset://textures/ui/Controls/xboxLT.png",



[Enum.KeyCode.ButtonR2] = "rbxasset://textures/ui/Controls/xboxRT.png",



[Enum.KeyCode.ButtonL3] = "rbxasset://textures/ui/Controls/xboxLS.png",



[Enum.KeyCode.ButtonR3] = "rbxasset://textures/ui/Controls/xboxRS.png",



[Enum.KeyCode.Thumbstick1] = "rbxasset://textures/ui/Controls/xboxLSDirectional.png",



[Enum.KeyCode.Thumbstick2] = "rbxasset://textures/ui/Controls/xboxRSDirectional.png",



}



local KeyboardButtonImage = {



[Enum.KeyCode.Backspace] = "rbxasset://textures/ui/Controls/backspace.png",



[Enum.KeyCode.Return] = "rbxasset://textures/ui/Controls/return.png",



[Enum.KeyCode.LeftShift] = "rbxasset://textures/ui/Controls/shift.png",



[Enum.KeyCode.RightShift] = "rbxasset://textures/ui/Controls/shift.png",



[Enum.KeyCode.Tab] = "rbxasset://textures/ui/Controls/tab.png",



}



local KeyboardButtonIconMapping = {



["'"] = "rbxasset://textures/ui/Controls/apostrophe.png",



[","] = "rbxasset://textures/ui/Controls/comma.png",



["`"] = "rbxasset://textures/ui/Controls/graveaccent.png",



["."] = "rbxasset://textures/ui/Controls/period.png",



[" "] = "rbxasset://textures/ui/Controls/spacebar.png",



}



local KeyCodeToTextMapping = {



[Enum.KeyCode.LeftControl] = "Ctrl",



[Enum.KeyCode.RightControl] = "Ctrl",



[Enum.KeyCode.LeftAlt] = "Alt",



[Enum.KeyCode.RightAlt] = "Alt",



[Enum.KeyCode.F1] = "F1",



[Enum.KeyCode.F2] = "F2",



[Enum.KeyCode.F3] = "F3",



[Enum.KeyCode.F4] = "F4",



[Enum.KeyCode.F5] = "F5",



[Enum.KeyCode.F6] = "F6",



[Enum.KeyCode.F7] = "F7",



[Enum.KeyCode.F8] = "F8",



[Enum.KeyCode.F9] = "F9",



[Enum.KeyCode.F10] = "F10",



[Enum.KeyCode.F11] = "F11",



[Enum.KeyCode.F12] = "F12",



}



local function getScreenGui()



local screenGui = PlayerGui:FindFirstChild("ProximityPrompts")



if screenGui == nil then



screenGui = Instance.new("ScreenGui")



screenGui.Name = "ProximityPrompts"



screenGui.ResetOnSpawn = false



screenGui.Parent = PlayerGui



end



return screenGui



end



local function createProgressBarGradient(parent, leftSide)



local frame = Instance.new("Frame")



frame.Size = UDim2.fromScale(0.5, 1)



frame.Position = UDim2.fromScale(leftSide and 0 or 0.5, 0)



frame.BackgroundTransparency = 1



frame.ClipsDescendants = true



frame.Parent = parent



local image = Instance.new("ImageLabel")



image.BackgroundTransparency = 1



image.Size = UDim2.fromScale(2, 1)



image.Position = UDim2.fromScale(leftSide and 0 or -1, 0)



image.Image = "rbxasset://textures/ui/Controls/RadialFill.png"



image.Parent = frame



local gradient = Instance.new("UIGradient")



gradient.Transparency = NumberSequence.new({



NumberSequenceKeypoint.new(0, 0),



NumberSequenceKeypoint.new(0.4999, 0),



NumberSequenceKeypoint.new(0.5, 1),



NumberSequenceKeypoint.new(1, 1),



})



gradient.Rotation = leftSide and 180 or 0



gradient.Parent = image



return gradient



end



local function createCircularProgressBar()



local bar = Instance.new("Frame")



bar.Name = "CircularProgressBar"



bar.Size = UDim2.fromOffset(58, 58)



bar.AnchorPoint = Vector2.new(0.5, 0.5)



bar.Position = UDim2.fromScale(0.5, 0.5)



bar.BackgroundTransparency = 1



local gradient1 = createProgressBarGradient(bar, true)



local gradient2 = createProgressBarGradient(bar, false)



local progress = Instance.new("NumberValue")



progress.Name = "Progress"



progress.Parent = bar



progress.Changed:Connect(function(value)



local angle = math.clamp(value * 360, 0, 360)



gradient1.Rotation = math.clamp(angle, 180, 360)



gradient2.Rotation = math.clamp(angle, 0, 180)



end)



return bar



end



local function createPrompt(prompt, inputType, gui)



local tweensForButtonHoldBegin = {}



local tweensForButtonHoldEnd = {}



local tweensForFadeOut = {}



local tweensForFadeIn = {}



local tweenInfoInFullDuration =



TweenInfo.new(prompt.HoldDuration, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)



local tweenInfoOutHalfSecond = TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)



local tweenInfoFast = TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)



local tweenInfoQuick = TweenInfo.new(0.06, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)



local promptUI = Instance.new("BillboardGui")



promptUI.Name = "Prompt"



promptUI.AlwaysOnTop = true



local frame = Instance.new("Frame")



frame.Size = UDim2.fromScale(0.5, 1)



frame.BackgroundTransparency = 1



frame.BackgroundColor3 = Color3.new(0.07, 0.07, 0.07)



frame.Parent = promptUI



local roundedCorner = Instance.new("UICorner")



roundedCorner.Parent = frame



local inputFrame = Instance.new("Frame")



inputFrame.Name = "InputFrame"



inputFrame.Size = UDim2.fromScale(1, 1)



inputFrame.BackgroundTransparency = 1



inputFrame.SizeConstraint = Enum.SizeConstraint.RelativeYY



inputFrame.Parent = frame



local resizeableInputFrame = Instance.new("Frame")



resizeableInputFrame.Size = UDim2.fromScale(1, 1)



resizeableInputFrame.Position = UDim2.fromScale(0.5, 0.5)



resizeableInputFrame.AnchorPoint = Vector2.new(0.5, 0.5)



resizeableInputFrame.BackgroundTransparency = 1



resizeableInputFrame.Parent = inputFrame



local inputFrameScaler = Instance.new("UIScale")



inputFrameScaler.Parent = resizeableInputFrame



local inputFrameScaleFactor = inputType == Enum.ProximityPromptInputType.Touch and 1.6 or 1.33



table.insert(



tweensForButtonHoldBegin,



TweenService:Create(inputFrameScaler, tweenInfoFast, { Scale = inputFrameScaleFactor })



)



table.insert(tweensForButtonHoldEnd, TweenService:Create(inputFrameScaler, tweenInfoFast, { Scale = 1 }))



local actionText = Instance.new("TextLabel")



actionText.Name = "ActionText"



actionText.Size = UDim2.fromScale(1, 1)



actionText.Font = Enum.Font.GothamMedium



actionText.TextSize = 19



actionText.BackgroundTransparency = 1



actionText.TextTransparency = 1



actionText.TextColor3 = Color3.new(1, 1, 1)



actionText.TextXAlignment = Enum.TextXAlignment.Left



actionText.Parent = frame



table.insert(tweensForButtonHoldBegin, TweenService:Create(actionText, tweenInfoFast, { TextTransparency = 1 }))



table.insert(tweensForButtonHoldEnd, TweenService:Create(actionText, tweenInfoFast, { TextTransparency = 0 }))



table.insert(tweensForFadeOut, TweenService:Create(actionText, tweenInfoFast, { TextTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(actionText, tweenInfoFast, { TextTransparency = 0 }))



local objectText = Instance.new("TextLabel")



objectText.Name = "ObjectText"



objectText.Size = UDim2.fromScale(1, 1)



objectText.Font = Enum.Font.GothamMedium



objectText.TextSize = 14



objectText.BackgroundTransparency = 1



objectText.TextTransparency = 1



objectText.TextColor3 = Color3.new(0.7, 0.7, 0.7)



objectText.TextXAlignment = Enum.TextXAlignment.Left



objectText.Parent = frame



table.insert(tweensForButtonHoldBegin, TweenService:Create(objectText, tweenInfoFast, { TextTransparency = 1 }))



table.insert(tweensForButtonHoldEnd, TweenService:Create(objectText, tweenInfoFast, { TextTransparency = 0 }))



table.insert(tweensForFadeOut, TweenService:Create(objectText, tweenInfoFast, { TextTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(objectText, tweenInfoFast, { TextTransparency = 0 }))



table.insert(



tweensForButtonHoldBegin,



TweenService:Create(frame, tweenInfoFast, { Size = UDim2.fromScale(0.5, 1), BackgroundTransparency = 1 })



)



table.insert(



tweensForButtonHoldEnd,



TweenService:Create(frame, tweenInfoFast, { Size = UDim2.fromScale(1, 1), BackgroundTransparency = 0.2 })



)



table.insert(



tweensForFadeOut,



TweenService:Create(frame, tweenInfoFast, { Size = UDim2.fromScale(0.5, 1), BackgroundTransparency = 1 })



)



table.insert(



tweensForFadeIn,



TweenService:Create(frame, tweenInfoFast, { Size = UDim2.fromScale(1, 1), BackgroundTransparency = 0.2 })



)



local roundFrame = Instance.new("Frame")



roundFrame.Name = "RoundFrame"



roundFrame.Size = UDim2.fromOffset(48, 48)



roundFrame.AnchorPoint = Vector2.new(0.5, 0.5)



roundFrame.Position = UDim2.fromScale(0.5, 0.5)



roundFrame.BackgroundTransparency = 1



roundFrame.Parent = resizeableInputFrame



local roundedFrameCorner = Instance.new("UICorner")



roundedFrameCorner.CornerRadius = UDim.new(0.5, 0)



roundedFrameCorner.Parent = roundFrame



table.insert(tweensForFadeOut, TweenService:Create(roundFrame, tweenInfoQuick, { BackgroundTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(roundFrame, tweenInfoQuick, { BackgroundTransparency = 0.5 }))



if inputType == Enum.ProximityPromptInputType.Gamepad then



if GamepadButtonImage[prompt.GamepadKeyCode] then



local icon = Instance.new("ImageLabel")



icon.Name = "ButtonImage"



icon.AnchorPoint = Vector2.new(0.5, 0.5)



icon.Size = UDim2.fromOffset(24, 24)



icon.Position = UDim2.fromScale(0.5, 0.5)



icon.BackgroundTransparency = 1



icon.ImageTransparency = 1



icon.Image = GamepadButtonImage[prompt.GamepadKeyCode]



icon.Parent = resizeableInputFrame



table.insert(tweensForFadeOut, TweenService:Create(icon, tweenInfoQuick, { ImageTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(icon, tweenInfoQuick, { ImageTransparency = 0 }))



end



elseif inputType == Enum.ProximityPromptInputType.Touch then



local buttonImage = Instance.new("ImageLabel")



buttonImage.Name = "ButtonImage"



buttonImage.BackgroundTransparency = 1



buttonImage.ImageTransparency = 1



buttonImage.Size = UDim2.fromOffset(25, 31)



buttonImage.AnchorPoint = Vector2.new(0.5, 0.5)



buttonImage.Position = UDim2.fromScale(0.5, 0.5)



buttonImage.Image = "rbxasset://textures/ui/Controls/TouchTapIcon.png"



buttonImage.Parent = resizeableInputFrame



table.insert(tweensForFadeOut, TweenService:Create(buttonImage, tweenInfoQuick, { ImageTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(buttonImage, tweenInfoQuick, { ImageTransparency = 0 }))



else



local buttonImage = Instance.new("ImageLabel")



buttonImage.Name = "ButtonImage"



buttonImage.BackgroundTransparency = 1



buttonImage.ImageTransparency = 1



buttonImage.Size = UDim2.fromOffset(28, 30)



buttonImage.AnchorPoint = Vector2.new(0.5, 0.5)



buttonImage.Position = UDim2.fromScale(0.5, 0.5)



buttonImage.Image = "rbxasset://textures/ui/Controls/key_single.png"



buttonImage.Parent = resizeableInputFrame



table.insert(tweensForFadeOut, TweenService:Create(buttonImage, tweenInfoQuick, { ImageTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(buttonImage, tweenInfoQuick, { ImageTransparency = 0 }))



local buttonTextString = UserInputService:GetStringForKeyCode(prompt.KeyboardKeyCode)



local buttonTextImage = KeyboardButtonImage[prompt.KeyboardKeyCode]



if buttonTextImage == nil then



buttonTextImage = KeyboardButtonIconMapping[buttonTextString]



end



if buttonTextImage == nil then



local keyCodeMappedText = KeyCodeToTextMapping[prompt.KeyboardKeyCode]



if keyCodeMappedText then



buttonTextString = keyCodeMappedText



end



end



if buttonTextImage then



local icon = Instance.new("ImageLabel")



icon.Name = "ButtonImage"



icon.AnchorPoint = Vector2.new(0.5, 0.5)



icon.Size = UDim2.fromOffset(36, 36)



icon.Position = UDim2.fromScale(0.5, 0.5)



icon.BackgroundTransparency = 1



icon.ImageTransparency = 1



icon.Image = buttonTextImage



icon.Parent = resizeableInputFrame



table.insert(tweensForFadeOut, TweenService:Create(icon, tweenInfoQuick, { ImageTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(icon, tweenInfoQuick, { ImageTransparency = 0 }))



elseif buttonTextString ~= nil and buttonTextString ~= "" then



local buttonText = Instance.new("TextLabel")



buttonText.Name = "ButtonText"



buttonText.Position = UDim2.fromOffset(0, -1)



buttonText.Size = UDim2.fromScale(1, 1)



buttonText.Font = Enum.Font.GothamMedium



buttonText.TextSize = 14



if string.len(buttonTextString) > 2 then



buttonText.TextSize = 12



end



buttonText.BackgroundTransparency = 1



buttonText.TextTransparency = 1



buttonText.TextColor3 = Color3.new(1, 1, 1)



buttonText.TextXAlignment = Enum.TextXAlignment.Center



buttonText.Text = buttonTextString



buttonText.Parent = resizeableInputFrame



table.insert(tweensForFadeOut, TweenService:Create(buttonText, tweenInfoQuick, { TextTransparency = 1 }))



table.insert(tweensForFadeIn, TweenService:Create(buttonText, tweenInfoQuick, { TextTransparency = 0 }))



else



error(



"ProximityPrompt '"



.. prompt.Name



.. "' has an unsupported keycode for rendering UI: "



.. tostring(prompt.KeyboardKeyCode)



)



end



end



if inputType == Enum.ProximityPromptInputType.Touch or prompt.ClickablePrompt then



local button = Instance.new("TextButton")



button.BackgroundTransparency = 1



button.TextTransparency = 1



button.Size = UDim2.fromScale(1, 1)



button.Parent = promptUI



local buttonDown = false



button.InputBegan:Connect(function(input)



if



(



input.UserInputType == Enum.UserInputType.Touch



or input.UserInputType == Enum.UserInputType.MouseButton1



) and input.UserInputState ~= Enum.UserInputState.Change



then



prompt:InputHoldBegin()



buttonDown = true



end



end)



button.InputEnded:Connect(function(input)



if



input.UserInputType == Enum.UserInputType.Touch



or input.UserInputType == Enum.UserInputType.MouseButton1



then



if buttonDown then



buttonDown = false



prompt:InputHoldEnd()



end



end



end)



promptUI.Active = true



end



if prompt.HoldDuration > 0 then



local circleBar = createCircularProgressBar()



circleBar.Parent = resizeableInputFrame



table.insert(



tweensForButtonHoldBegin,



TweenService:Create(circleBar.Progress, tweenInfoInFullDuration, { Value = 1 })



)



table.insert(



tweensForButtonHoldEnd,



TweenService:Create(circleBar.Progress, tweenInfoOutHalfSecond, { Value = 0 })



)



end



local holdBeganConnection



local holdEndedConnection



local triggeredConnection



local triggerEndedConnection



if prompt.HoldDuration > 0 then



holdBeganConnection = prompt.PromptButtonHoldBegan:Connect(function()



for _, tween in ipairs(tweensForButtonHoldBegin) do



tween:Play()



end



end)



holdEndedConnection = prompt.PromptButtonHoldEnded:Connect(function()



for _, tween in ipairs(tweensForButtonHoldEnd) do



tween:Play()



end



end)



end



triggeredConnection = prompt.Triggered:Connect(function()



for _, tween in ipairs(tweensForFadeOut) do



tween:Play()



end



end)



triggerEndedConnection = prompt.TriggerEnded:Connect(function()



for _, tween in ipairs(tweensForFadeIn) do



tween:Play()



end



end)



local function updateUIFromPrompt()



-- todo: Use AutomaticSize instead of GetTextSize when that feature becomes available



local actionTextSize =



TextService:GetTextSize(prompt.ActionText, 19, Enum.Font.GothamMedium, Vector2.new(1000, 1000))



local objectTextSize =



TextService:GetTextSize(prompt.ObjectText, 14, Enum.Font.GothamMedium, Vector2.new(1000, 1000))



local maxTextWidth = math.max(actionTextSize.X, objectTextSize.X)



local promptHeight = 72



local promptWidth = 72



local textPaddingLeft = 72



if



(prompt.ActionText ~= nil and prompt.ActionText ~= "")



or (prompt.ObjectText ~= nil and prompt.ObjectText ~= "")



then



promptWidth = maxTextWidth + textPaddingLeft + 24



end



local actionTextYOffset = 0



if prompt.ObjectText ~= nil and prompt.ObjectText ~= "" then



actionTextYOffset = 9



end



actionText.Position = UDim2.new(0.5, textPaddingLeft - promptWidth / 2, 0, actionTextYOffset)



objectText.Position = UDim2.new(0.5, textPaddingLeft - promptWidth / 2, 0, -10)



actionText.Text = prompt.ActionText



objectText.Text = prompt.ObjectText



actionText.AutoLocalize = prompt.AutoLocalize



actionText.RootLocalizationTable = prompt.RootLocalizationTable



objectText.AutoLocalize = prompt.AutoLocalize



objectText.RootLocalizationTable = prompt.RootLocalizationTable



promptUI.Size = UDim2.fromOffset(promptWidth, promptHeight)



promptUI.SizeOffset =



Vector2.new(prompt.UIOffset.X / promptUI.Size.Width.Offset, prompt.UIOffset.Y / promptUI.Size.Height.Offset)



end



local changedConnection = prompt.Changed:Connect(updateUIFromPrompt)



updateUIFromPrompt()



promptUI.Adornee = prompt.Parent



promptUI.Parent = gui



for _, tween in ipairs(tweensForFadeIn) do



tween:Play()



end



local function cleanup()



if holdBeganConnection then



holdBeganConnection:Disconnect()



end



if holdEndedConnection then



holdEndedConnection:Disconnect()



end



triggeredConnection:Disconnect()



triggerEndedConnection:Disconnect()



changedConnection:Disconnect()



for _, tween in ipairs(tweensForFadeOut) do



tween:Play()



end



task.wait(0.2)



promptUI.Parent = nil



end



return cleanup



end



local function onLoad()



ProximityPromptService.PromptShown:Connect(function(prompt, inputType)



if prompt.Style == Enum.ProximityPromptStyle.Default then



return



end



local gui = getScreenGui()



local cleanupFunction = createPrompt(prompt, inputType, gui)



prompt.PromptHidden:Wait()



cleanupFunction()



end)



end



onLoad()
```

Healing Proximity Prompt

The example below illustrates a prompt that requires the user to hold the
button down in order to heal their character. This should be used in a
Script that is a child of a ProximityPrompt.

```
local RunService = game:GetService("RunService")



local prompt = script.Parent



local playersHealing = {}



RunService.Stepped:Connect(function(_currentTime, deltaTime)



for player, _value in pairs(playersHealing) do



local humanoid = player.Character:FindFirstChildWhichIsA("Humanoid")



if humanoid then



humanoid.Health = humanoid.Health + 30 * deltaTime



end



end



end)



prompt.Triggered:Connect(function(player)



playersHealing[player] = true



end)



prompt.TriggerEnded:Connect(function(player)



playersHealing[player] = nil



end)
```

---

API Reference

Properties

ActionText

Read Parallel

The action text shown to the user.

ProximityPrompt.ActionText:[string](/docs/luau/strings)

This property determines the action text shown to the user.

Provide feedback

---

AutoLocalize

Read Parallel

Whether the prompt's [ProximityPrompt.ActionText](/docs/reference/engine/classes/ProximityPrompt#ActionText) and
[ProximityPrompt.ObjectText](/docs/reference/engine/classes/ProximityPrompt#ObjectText) will be localized according to the
[ProximityPrompt.RootLocalizationTable](/docs/reference/engine/classes/ProximityPrompt#RootLocalizationTable).

ProximityPrompt.AutoLocalize:[boolean](/docs/luau/booleans)

This property determines whether the prompt's
[ProximityPrompt.ActionText](/docs/reference/engine/classes/ProximityPrompt#ActionText) and [ProximityPrompt.ObjectText](/docs/reference/engine/classes/ProximityPrompt#ObjectText)
will be localized according to the
[ProximityPrompt.RootLocalizationTable](/docs/reference/engine/classes/ProximityPrompt#RootLocalizationTable). When set to true,
localization will be applied.

Provide feedback

---

ClickablePrompt

Read Parallel

Whether the prompt can be activated by clicking/tapping on the prompt UI.

ProximityPrompt.ClickablePrompt:[boolean](/docs/luau/booleans)

This property determines whether the prompt can be activated by
clicking/tapping on the prompt's UI. When set to false, the prompt cannot
be activated by click/tap except on mobile.

Provide feedback

---

Enabled

Read Parallel

Whether or not this prompt should be shown.

ProximityPrompt.Enabled:[boolean](/docs/luau/booleans)

This property indicates whether or this [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) should be
shown.

Provide feedback

---

Exclusivity

Read Parallel

Used to customize which prompts can be shown at the same time.

ProximityPrompt.Exclusivity:[Enum.ProximityPromptExclusivity](/docs/reference/engine/enums/ProximityPromptExclusivity)

This property is used to customize which prompts can be shown at the same
time.

Provide feedback

---

GamepadKeyCode

Read Parallel

The gamepad button the player should press to trigger the prompt.

ProximityPrompt.GamepadKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

This property determines the gamepad button the player should press to
trigger the [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt). Default is
ButtonX.

Provide feedback

---

HoldDuration

Read Parallel

The duration, in seconds, that the player must hold the button/key down to
trigger the prompt.

ProximityPrompt.HoldDuration:[number](/docs/luau/numbers)

This property indicates the duration, in seconds, that the player must
hold the button/key down to trigger the prompt.

Provide feedback

---

KeyboardKeyCode

Read Parallel

The key the player should press to trigger the prompt.

ProximityPrompt.KeyboardKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

This property determines the key the player should press to trigger the
[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt). Default is E.

Provide feedback

---

MaxActivationDistance

Read Parallel

The maximum distance a Player's [character](/docs/reference/engine/classes/Player#Character) can be
from the [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) for the prompt to appear.

ProximityPrompt.MaxActivationDistance:[number](/docs/luau/numbers)

This property determines the maximum distance a Player's
[character](/docs/reference/engine/classes/Player#Character) can be from the [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt)
for the prompt to appear.

Provide feedback

---

MaxIndicatorDistance

Read Parallel

ProximityPrompt.MaxIndicatorDistance:[number](/docs/luau/numbers)

Provide feedback

---

ObjectText

Read Parallel

An optional property that determines the object name text shown to the
user.

ProximityPrompt.ObjectText:[string](/docs/luau/strings)

This optional property determines the optional object name text shown to
the user.

Provide feedback

---

RequiresLineOfSight

Read Parallel

Whether the prompt is hidden if the path between the player's
[Camera](/docs/reference/engine/classes/Camera) and object parented to the [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) is
obstructed.

ProximityPrompt.RequiresLineOfSight:[boolean](/docs/luau/booleans)

This property indicates whether the prompt is hidden if the path between
the player's [Camera](/docs/reference/engine/classes/Camera) and object parented to the
[ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) is obstructed. If true, this prompt will only be
shown if there is a clear path from the camera to the object.

The parent [Part](/docs/reference/engine/classes/Part) or [Model](/docs/reference/engine/classes/Model) of the prompt will be excluded
from this check.

Provide feedback

---

RootLocalizationTable

Read Parallel

A reference to a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) to be used to apply automated
localization to this prompt's [ProximityPrompt.ActionText](/docs/reference/engine/classes/ProximityPrompt#ActionText) and
[ProximityPrompt.ObjectText](/docs/reference/engine/classes/ProximityPrompt#ObjectText).

ProximityPrompt.RootLocalizationTable:[LocalizationTable](/docs/reference/engine/classes/LocalizationTable)

This property serves as a reference to the [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) used
to apply automated localization to the prompt's
[ProximityPrompt.ActionText](/docs/reference/engine/classes/ProximityPrompt#ActionText) and [ProximityPrompt.ObjectText](/docs/reference/engine/classes/ProximityPrompt#ObjectText).
In order for this to apply, [ProximityPrompt.AutoLocalize](/docs/reference/engine/classes/ProximityPrompt#AutoLocalize) must be
set.

Developers can set this to reference a LocalizationTable anywhere in the
[DataModel](/docs/reference/engine/classes/DataModel). It is not required to be a child of
[LocalizationService](/docs/reference/engine/classes/LocalizationService). If there is no translation available in the
referenced table it will look for a translation in the parent of that
table, if it is also a LocalizationTable, and so on.

Provide feedback

---

Style

Read Parallel

The style of the prompt's UI.

ProximityPrompt.Style:[Enum.ProximityPromptStyle](/docs/reference/engine/enums/ProximityPromptStyle)

This property indicates the prompt's style. When set to Custom, no default
UI will be provided.

The provided UI can be swapped out for a custom UI. In order to do this,
set Style to Custom. Then, listen to the
[ProximityPrompt.PromptShown](/docs/reference/engine/classes/ProximityPrompt#PromptShown) and
[ProximityPrompt.PromptHidden](/docs/reference/engine/classes/ProximityPrompt#PromptHidden) events in a [LocalScript](/docs/reference/engine/classes/LocalScript),
where developers should create and tear down the UI.

Developers may also use [ProximityPrompt.PromptButtonHoldBegan](/docs/reference/engine/classes/ProximityPrompt#PromptButtonHoldBegan) and
[ProximityPrompt.PromptButtonHoldEnded](/docs/reference/engine/classes/ProximityPrompt#PromptButtonHoldEnded) in order to utilize the
[ProximityPrompt.HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration) progress animation feature.

Provide feedback

---

UIOffset

Read Parallel

The pixel offset applied to the prompt's UI.

ProximityPrompt.UIOffset:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property indicates the pixel offset applied to the prompt's UI.

Provide feedback

---

Methods

InputHoldBegin

Fires a signal indicating that the user began pressing the prompt GUI
button.

ProximityPrompt:InputHoldBegin():()

Returns

()

This function triggers a signal indicating that the user began pressing
the [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt) prompt button. It should be used by developers
who wish to customize the prompt and trigger it from a prompt GUI button
press.

Provide feedback

---

InputHoldEnd

Fires a signal indicating that the user ended pressing the prompt GUI
button.

ProximityPrompt:InputHoldEnd():()

Returns

()

A counterpoint to [ProximityPrompt:InputHoldBegin()](/docs/reference/engine/classes/ProximityPrompt#InputHoldBegin), this signals
that the user ended pressing the prompt GUI button.

Provide feedback

---

Events

IndicatorHidden

ProximityPrompt.IndicatorHidden():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Provide feedback

---

IndicatorShown

ProximityPrompt.IndicatorShown():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Provide feedback

---

PromptButtonHoldBegan

Triggered when a player begins holding down the
[key](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode)/button connected to a prompt
with a non-zero [ProximityPrompt.HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration).

ProximityPrompt.PromptButtonHoldBegan(playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who begins holding down the prompt button. |

This event triggers when a player begins holding down the
[key](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode)/button on a prompt with a
non-zero [ProximityPrompt.HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration). One possible usage includes
to animate a hold progress bar.

Provide feedback

---

PromptButtonHoldEnded

Triggers when the player ends holding down the button on a prompt with a
non-zero [ProximityPrompt.HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration).

ProximityPrompt.PromptButtonHoldEnded(playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The player who ended the input hold. |

This event triggers when the player ends holding down the button on a
prompt with a non-zero [ProximityPrompt.HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration). One possible
usage includes to animate a hold progress bar.

Provide feedback

---

PromptHidden

Triggers when the [prompt](/docs/reference/engine/classes/ProximityPrompt) becomes hidden.

ProximityPrompt.PromptHidden():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event triggers when the [prompt](/docs/reference/engine/classes/ProximityPrompt) becomes
hidden. This event is triggered client-side for LocalScripts.

Provide feedback

---

PromptShown

Triggers when the [prompt](/docs/reference/engine/classes/ProximityPrompt) becomes visible.

ProximityPrompt.PromptShown(inputType:[Enum.ProximityPromptInputType](/docs/reference/engine/enums/ProximityPromptInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| inputType:[Enum.ProximityPromptInputType](/docs/reference/engine/enums/ProximityPromptInputType)  The input that triggers the prompt. |

This event triggers when the [prompt](/docs/reference/engine/classes/ProximityPrompt) becomes
visible. This event is triggered client-side for LocalScripts.

Provide feedback

---

Triggered

Triggered when the prompt
[key](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode)/button is pressed, or after a
specified amount of time holding the button, if
[ProximityPrompt.HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration) is used.

ProximityPrompt.Triggered(playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who triggered the prompt. |

This event is triggered when the prompt
[key](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode)/button is pressed, or after a
specified amount of time holding the button, if
[ProximityPrompt.HoldDuration](/docs/reference/engine/classes/ProximityPrompt#HoldDuration) is used.

Provide feedback

---

TriggerEnded

Triggers when [key](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode)/button is
released, for longer events where the user is required to hold down the
button.

ProximityPrompt.TriggerEnded(playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoTriggered:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who released the key/button, ending the trigger event. |

This event is triggered when the
[key](/docs/reference/engine/classes/ProximityPrompt#KeyboardKeyCode)/button is released, for longer
events where the user is required to hold down the button (e.g. heal
another player over time.)

Provide feedback

---