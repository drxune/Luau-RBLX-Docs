# RunService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RunService
Scraped: 2026-01-11T02:31:35.047469Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- RunService
- IsClient()
- IsServer()
- IsStudio()
- ModuleScripts
- PreRender
- PreAnimation
- PreSimulation
- PostSimulation
- Heartbeat
- IsStudio
- IsClient
- IsServer
- IsEdit
- IsRunning
- IsRunMode
- RunService.PreRender
- Unbind
- RunService:UnbindFromRenderStep()
- RunService:BindToRenderStep()
- Workspace.UseFixedSimulation
- RenderStepped
- LocalScript
- ModuleScript
- Script
- RunContext
- Players.LocalPlayer
- IsRunning()
- RunService:Run()
- IsEdit()
- ServerStorage
- ServerScriptService
- IsRunMode()
- BindToRenderStep()
- Stepped
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [RunService](/docs/reference/engine/classes/RunService)

English

Feedback

Engine Class

RunService

Service responsible for all runtime activity and progression of time.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [ClientGitHash](#ClientGitHash):[string](/docs/luau/strings) |
| [RunState](#RunState):[Enum.RunState](/docs/reference/engine/enums/RunState) |

Methods

|  |
| --- |
| [BindToRenderStep](#BindToRenderStep)(name: [string](/docs/luau/strings),priority: [number](/docs/luau/numbers),function: [function](/docs/luau/functions)):() |
| [BindToSimulation](#BindToSimulation)(function: [function](/docs/luau/functions),frequency: [Enum.StepFrequency](/docs/reference/engine/enums/StepFrequency)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [GetPredictionStatus](#GetPredictionStatus)(context: [Instance](/docs/reference/engine/datatypes/Instance)):[Enum.PredictionStatus](/docs/reference/engine/enums/PredictionStatus) |
| [IsClient](#IsClient)():[boolean](/docs/luau/booleans) |
| [IsEdit](#IsEdit)():[boolean](/docs/luau/booleans) |
| [IsRunMode](#IsRunMode)():[boolean](/docs/luau/booleans) |
| [IsRunning](#IsRunning)():[boolean](/docs/luau/booleans) |
| [IsServer](#IsServer)():[boolean](/docs/luau/booleans) |
| [IsStudio](#IsStudio)():[boolean](/docs/luau/booleans) |
| [Pause](#Pause)():() |
| [Reset](#Reset)():()  Deprecated |
| [Run](#Run)():() |
| [SetPredictionMode](#SetPredictionMode)(context: [Instance](/docs/reference/engine/datatypes/Instance),mode: [Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode)):() |
| [Stop](#Stop)():() |
| [UnbindFromRenderStep](#UnbindFromRenderStep)(name: [string](/docs/luau/strings)):() |

Events

|  |
| --- |
| [Heartbeat](#Heartbeat)(deltaTime: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PostSimulation](#PostSimulation)(deltaTimeSim: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PreAnimation](#PreAnimation)(deltaTimeSim: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PreRender](#PreRender)(deltaTimeRender: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PreSimulation](#PreSimulation)(deltaTimeSim: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [RenderStepped](#RenderStepped)(deltaTime: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Stepped](#Stepped)(time: [number](/docs/luau/numbers),deltaTime: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

RunService contains methods and events for time management as well as for
managing the context in which an experience or script is running. Methods like
[IsClient()](/docs/reference/engine/classes/RunService#IsClient),
[IsServer()](/docs/reference/engine/classes/RunService#IsServer), and
[IsStudio()](/docs/reference/engine/classes/RunService#IsStudio) can help you determine under what
context code is running. These methods are useful for
[ModuleScripts](/docs/reference/engine/classes/ModuleScript) that may be required by both client and
server scripts. Furthermore, [IsStudio()](/docs/reference/engine/classes/RunService#IsStudio) can be
used to add special behaviors for in‑Studio testing.

RunService also houses events that allow your code to adhere to the engine's
frame‑by‑frame loop, such as [PreRender](/docs/reference/engine/classes/RunService#PreRender),
[PreAnimation](/docs/reference/engine/classes/RunService#PreAnimation),
[PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation),
[PostSimulation](/docs/reference/engine/classes/RunService#PostSimulation), and
[Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat). Selecting the proper event to use for
any case is important, so you should read
[Task Scheduler](/docs/performance-optimization/microprofiler/task-scheduler)
to make an informed decision.

##### Context Test Results

| Environment | [IsStudio](/docs/reference/engine/classes/RunService#IsStudio) | [IsClient](/docs/reference/engine/classes/RunService#IsClient) | [IsServer](/docs/reference/engine/classes/RunService#IsServer) | [IsEdit](/docs/reference/engine/classes/RunService#IsEdit) | [IsRunning](/docs/reference/engine/classes/RunService#IsRunning) | [IsRunMode](/docs/reference/engine/classes/RunService#IsRunMode) |
| --- | --- | --- | --- | --- | --- | --- |
| Live (Client) | false | true | false |  | true | false |
| Live (Server) | false | false | true |  | true | false |
| Edit | true | true | true | true | false | false |
| Collaborative Edit | true | true | false | true | false | false |
| Run Mode | true | false | true |  | true | true |
| Play Mode (Client) | true | true | false |  | true | false |
| Play Mode (Server) | true | false | true |  | true | false |
| Team Test (Client) | true | true | false |  | true | false |
| Team Test (Server) | true | false | true |  | true | false |
| Luau Execution | false | false | true |  | false | false |

---

API Reference

Properties

ClientGitHash

Read Only

Not Replicated

Roblox Script Security

Read Parallel

RunService.ClientGitHash:[string](/docs/luau/strings)

Provide feedback

---

RunState

Not Replicated

Plugin Security

Read Parallel

RunService.RunState:[Enum.RunState](/docs/reference/engine/enums/RunState)

Provide feedback

---

Methods

BindToRenderStep

Given a string name of a function and a priority, this method binds the
function to [RunService.PreRender](/docs/reference/engine/classes/RunService#PreRender).

RunService:BindToRenderStep(

name:[string](/docs/luau/strings), priority:[number](/docs/luau/numbers), function:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Label for the binding which can be used with [Unbind](/docs/reference/engine/classes/RunService#Unbind) if the binding is no longer needed. |
| priority:[number](/docs/luau/numbers)  Priority of the binding as an integer; it determines when during the render step to call the custom function. The lower this number, the sooner the custom function will be called. If two bindings have the same priority, the engine will randomly pick one to run first. |
| function:[function](/docs/luau/functions)  The custom function being bound. |

Returns

()

The BindToRenderStep() function binds a custom function to be called at
a specific time during the render step. There are three main arguments:
name, priority, and what function to call.

As it is linked to the client's rendering process, BindToRenderStep()
can only be called on the client.

##### Name

The name parameter is a label for the binding and can be used with
[RunService:UnbindFromRenderStep()](/docs/reference/engine/classes/RunService#UnbindFromRenderStep) if the binding is no longer
needed.

```
local RunService = game:GetService("RunService")



local function functionToBind() end



-- Bind the function above to the binding named "tempBinding"



RunService:BindToRenderStep("tempBinding", 1, functionToBind)



-- Unbind the function bound to "tempBinding"



RunService:UnbindFromRenderStep("tempBinding")
```

##### Priority

The priority of the binding is an integer; it determines when during the
render step to call the custom function. The lower this number, the sooner
the custom function will be called. If two bindings have the same
priority, the engine will randomly pick one to run first. The default
control scripts run with these specific priorities:

* Player Input: 100
* Camera Controls: 200 For convenience; the [Enum.RenderPriority](/docs/reference/engine/enums/RenderPriority) enum
  can be used to determine the integer value to set a binding. For
  example, to make a binding right before the default camera update,
  simply subtract 1 from the camera priority level.

When using [Enum.RenderPriority](/docs/reference/engine/enums/RenderPriority), remember to use .Value at the end of
the desired enum. [RunService:BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep) will not work if
just the enum is used on its own.

```
local RunService = game:GetService("RunService")



local function beforeCamera(delta)



-- Code in here will run before the default camera script



end



RunService:BindToRenderStep("Before camera", Enum.RenderPriority.Camera.Value - 1, beforeCamera)
```

##### Custom Function and Delta Time

The last argument (function) is the custom function to call. This
function will be passed one parameter called deltaTime which shows how
much time passed between the beginning of the previous render step and the
beginning of the current render step.

All rendering updates will wait until the code in the render step
finishes. Make sure that any code called by BindToRenderStep() runs
quickly and efficiently; if code takes too long, the experience visuals
will be choppy.

Code Samples

Frame Moving in Circle

This code sample moves a GuiObject in a circle within its parent object using
RunService's BindToRenderStep. It defines a parametric equation in a function
to help with positioning the GuiObject.

To try this code out, put a ScreenGui in the StarterGui. Inside the ScreenGui,
insert a Frame with a LocalScript. Paste this code into the LocalScript, then
play the game. Watch the Frame travel counterclockwise within.

```
local RunService = game:GetService("RunService")



-- How fast the frame ought to move



local SPEED = 2



local frame = script.Parent



frame.AnchorPoint = Vector2.new(0.5, 0.5)



-- A simple parametric equation of a circle



-- centered at (0.5, 0.5) with radius (0.5)



local function circle(t)



return 0.5 + math.cos(t) * 0.5, 0.5 + math.sin(t) * 0.5



end



-- Keep track of the current time



local currentTime = 0



local function onRenderStep(deltaTime)



-- Update the current time



currentTime = currentTime + deltaTime * SPEED



-- ...and the frame's position



local x, y = circle(currentTime)



frame.Position = UDim2.new(x, 0, y, 0)



end



-- This is just a visual effect, so use the "Last" priority



RunService:BindToRenderStep("FrameCircle", Enum.RenderPriority.Last.Value, onRenderStep)



--RunService.RenderStepped:Connect(onRenderStep) -- Also works, but not recommended
```

RunService Custom Function

This example shows how to bind a simple function to the render step. All this
function does is print how much time passed between the last render step and
the current one. Note that this code will need to be in a LocalScript to
run.

```
local RunService = game:GetService("RunService")



local function checkDelta(deltaTime)



print("Time since last render step:", deltaTime)



end



RunService:BindToRenderStep("Check delta", Enum.RenderPriority.First.Value, checkDelta)
```

Bind and Unbind a Function

This example uses the RunService to bind and unbind a function named
printHello. First, we bind the function to the RenderStep so that fires
every *step*. Then, after we wait 5 seconds (wait(5)), we unbind the
function.

```
local RunService = game:GetService("RunService")



-- Step 1: Declare the function and a name



local NAME = "Print Hello"



local function printHello()



print("Hello")



end



-- Step 2: Bind the function



RunService:BindToRenderStep(NAME, Enum.RenderPriority.First.Value, printHello)



-- Step 3: Unbind the function



RunService:UnbindFromRenderStep(NAME)
```

Provide feedback

---

BindToSimulation

Binds a custom function to be called at a fixed frequency which is
independent of the frame rate.

RunService:BindToSimulation(

function:[function](/docs/luau/functions), frequency:[Enum.StepFrequency](/docs/reference/engine/enums/StepFrequency)

):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| function:[function](/docs/luau/functions)  The function to call. This function will be passed one parameter called deltaTime which shows how much time passed between the beginning of the previous simulation step and the beginning of the current simulation step. |
| frequency:[Enum.StepFrequency](/docs/reference/engine/enums/StepFrequency) Default Value: "Hz60" Optional [Enum.StepFrequency](/docs/reference/engine/enums/StepFrequency) value indicating the frequency at which to call the bound function. If not provided, the default frequency will be used. |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

BindToSimulation() binds a custom function to be called at a fixed
frequency which is independent of the frame rate. In the server authority
model, bound functions will also get called when the client needs to
resimulate. This method is only available when
[Workspace.UseFixedSimulation](/docs/reference/engine/classes/Workspace#UseFixedSimulation) is enabled.

Note that since the bound function is meant for physics controllers and
prediction, an error will trigger if you read or write from unsynchronized
properties or call an unsynchronized method. This error is meant to help
guide you in writing a pure, synchronized simulation.

To synchronize inaccessible properties, you should store the relevant data
in [attributes](/docs/studio/properties#instance-attributes) and
update the relevant property in
[PostSimulation](/docs/reference/engine/classes/RunService#PostSimulation) or
[RenderStepped](/docs/reference/engine/classes/RunService#RenderStepped) by reading from attributes.
This will leverage attribute synchronization to keep the property fully
synchronized through the rollback mechanism.

Code Samples

Synchronizing a Part's Color Property

```
local RunService = game:GetService("RunService")



local Workspace = game:GetService("Workspace")



local somePart:BasePart = Workspace:WaitForChild("Part")



RunService:BindToSimulation(function(deltaTime: number)



local syncdColor = Color3.fromHSV(math.fmod(time(), 1.0), 1.0, 1.0)



somePart:SetAttribute("SyncdColor", syncdColor)



end)



RunService.RenderStepped:Connect(function(deltaTime: number)



local syncdColor = somePart:GetAttribute("SyncdColor")



somePart.Color = syncdColor



end)
```

Provide feedback

---

GetPredictionStatus

Checks the [Enum.PredictionStatus](/docs/reference/engine/enums/PredictionStatus) of a specific context instance, useful
for debugging scripts affecting multiple instances where some might be
predicted and others might not.

RunService:GetPredictionStatus(context:[Instance](/docs/reference/engine/datatypes/Instance)):[Enum.PredictionStatus](/docs/reference/engine/enums/PredictionStatus)

Parameters

|  |
| --- |
| context:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) for which to check prediction status. |

Returns

[Enum.PredictionStatus](/docs/reference/engine/enums/PredictionStatus)

Clients can use this method to check the [Enum.PredictionStatus](/docs/reference/engine/enums/PredictionStatus) of a
specific context instance, useful for debugging scripts affecting multiple
instances (vehicle controllers, custom physics, etc.) where some might be
predicted and others might not. This method is also useful for debugging
and observing the effects of [Enum.PredictionMode.Automatic](/docs/reference/engine/enums/PredictionMode#Automatic) prediction
mode.

Provide feedback

---

IsClient

Write Parallel

Returns whether the current environment is running on the client.

RunService:IsClient():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the current environment is running the client.

If the code that invoked this method is running in a client context (in a
[LocalScript](/docs/reference/engine/classes/LocalScript), in a [ModuleScript](/docs/reference/engine/classes/ModuleScript) required by a
[LocalScript](/docs/reference/engine/classes/LocalScript), or in a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client)),
this method will return true. In all other cases, this method will
return false.

If this method returns true, the current environment can access
client‑only features like [RunService.PreRender](/docs/reference/engine/classes/RunService#PreRender) or
[Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer).

Provide feedback

---

IsEdit

Plugin Security

Write Parallel

Returns whether the current environment is in Edit mode.

RunService:IsEdit():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the current environment is in "edit" mode.

This method returns whether the current environment is in "edit" mode, for
example in Studio when the experience is not running.

IsEdit() will return the inverse of
[IsRunning()](/docs/reference/engine/classes/RunService#IsRunning), except when the simulation has
been paused, in which case both methods will return false.

Provide feedback

---

IsRunMode

Write Parallel

Returns whether a Run playtest has been initiated in Studio.

RunService:IsRunMode():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether a Run playtest has been initiated in Studio.

This method returns whether a Run playtest has been initiated in
Studio. It will continue to return true if the simulation has been
paused using the Pause button; however, once it has been stopped using
the Stop button, it will revert to returning false. Note that Studio
only enters "run" mode when a Run playtest (without the user's player
character) is initiated. Also note that this method will return false if
the simulation was started using [RunService:Run()](/docs/reference/engine/classes/RunService#Run).

Provide feedback

---

IsRunning

Returns whether the experience is currently running.

RunService:IsRunning():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the experience is currently running.

Returns whether the experience is currently running. IsRunning() will
always return the inverse of [IsEdit()](/docs/reference/engine/classes/RunService#IsEdit) except
when the simulation has been paused, in which case both methods will
return false.

Provide feedback

---

IsServer

Write Parallel

Returns whether the current environment is running on the server.

RunService:IsServer():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the current environment is running on the server.

This method returns whether the current environment is running on the
server. If the code that invoked this method is running in a server
context (in a [Script](/docs/reference/engine/classes/Script) with [RunContext](/docs/reference/engine/classes/BaseScript#RunContext)
set to [Enum.RunContext.Server](/docs/reference/engine/enums/RunContext#Server) or [Enum.RunContext.Legacy](/docs/reference/engine/enums/RunContext#Legacy), or in a
[ModuleScript](/docs/reference/engine/classes/ModuleScript) required by a [Script](/docs/reference/engine/classes/Script)), this method will
return true. In all other cases, this method will return false.

If this function returns true, then the current environment can access
server‑only features like [ServerStorage](/docs/reference/engine/classes/ServerStorage) or
[ServerScriptService](/docs/reference/engine/classes/ServerScriptService).

Provide feedback

---

IsStudio

Write Parallel

Returns whether the current environment is running in Studio.

RunService:IsStudio():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the current environment is running in Studio.

This method returns whether the current environment is running in Studio.
It can be used to wrap code that should only execute when testing in
Studio.

Provide feedback

---

Pause

Plugin Security

Pauses the experience's simulation if it is running, suspending physics
and scripts.

RunService:Pause():()

Returns

()

This method pauses the experience's simulation if it is running,
suspending physics and scripts. When the simulation is paused,
[IsRunning()](/docs/reference/engine/classes/RunService#IsRunning) will return false.

Provide feedback

---

Reset

Deprecated

Show details

---

Run

Plugin Security

Runs the game's simulation, running physics and scripts.

RunService:Run():()

Returns

()

This method runs the experience's simulation (physics and scripts). When
the simulation is running, [IsRunning()](/docs/reference/engine/classes/RunService#IsRunning) will
return true. However, [IsRunMode()](/docs/reference/engine/classes/RunService#IsRunMode) will
only return true if the simulation was started using the Run button
in Studio.

Provide feedback

---

SetPredictionMode

Sets the prediction mode for an [Instance](/docs/reference/engine/classes/Instance) to an
[Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode) value.

RunService:SetPredictionMode(

context:[Instance](/docs/reference/engine/datatypes/Instance), mode:[Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode)

):()

Parameters

|  |
| --- |
| context:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) for which to set the prediction mode. |
| mode:[Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode)  The [Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode) to set for the context instance. |

Returns

()

Sets the prediction mode for an [Instance](/docs/reference/engine/classes/Instance) (context) to an
[Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode) value. Mismatches between the physics properties or
attributes for predicted instances will cause a rollback and resimulation
on the client. Can only be called on the client.

Provide feedback

---

Stop

Plugin Security

Stops the experience's simulation if it is running.

RunService:Stop():()

Returns

()

This method stops the experience's simulation if it is running. When the
simulation is stopped, [IsRunning()](/docs/reference/engine/classes/RunService#IsRunning) will
return false and [IsEdit()](/docs/reference/engine/classes/RunService#IsEdit) will return
true.

In contrast to the Stop button in Studio, calling this method will not
restore the experience to the state it was in prior to the simulation
being run. This means any changes made to the experience by the physics
simulation and scripts will persist after the simulation has ended.

Provide feedback

---

UnbindFromRenderStep

Unbinds a function that was bound to the render loop using
[RunService:BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep).

RunService:UnbindFromRenderStep(name:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the function being unbound. |

Returns

()

Given a name of a function sent to
[BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep), this method will
unbind the function from being called during
[PreRender](/docs/reference/engine/classes/RunService#PreRender). This is used to unbind bound
functions once they are no longer needed, or when they no longer need to
fire every step.

If there is no bound function by the given name, this method takes no
action and continues without raising an error.

Provide feedback

---

Events

Heartbeat

Fires every frame, after the physics simulation has completed.

RunService.Heartbeat(deltaTime:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| deltaTime:[number](/docs/luau/numbers)  The time (in seconds) that has elapsed since the previous frame. |

The Heartbeat event fires every frame, after the physics simulation has
completed. The deltaTime argument indicates the time that has elapsed
since the previous frame.

This event is when most scripts run. It occurs at the end of each frame
and it's also when any waiting scripts are executed, such as those
scheduled with the [task](/docs/reference/engine/libraries/task) library. Heartbeat is commonly used
for periodic tasks, such as updating core game systems like health
regeneration.

Following this step, the engine sends property updates and events to the
server or clients which are later received as part of the
[replication](/docs/projects/client-server#replication) receive
step.

Provide feedback

---

PostSimulation

Fires every frame, after the physics simulation has completed.

RunService.PostSimulation(deltaTimeSim:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| deltaTimeSim:[number](/docs/luau/numbers)  The time (in seconds) that the current frame has stepped the physics simulation, not accounting for physics throttling. |

The PostSimulation event fires every frame, after the physics simulation
has completed. The deltaTimeSim argument indicates the time that the
current frame has stepped the physics simulation, not accounting for
physics throttling. This may deviate from the actual time between frames
in Studio edit mode or when framerate is very low.

This event is useful for making final adjustments to the outcome of the
simulation. Following this phase, the engine triggers the
[Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat) event.

Provide feedback

---

PreAnimation

Fires every frame, prior to the physics simulation but after rendering.

RunService.PreAnimation(deltaTimeSim:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| deltaTimeSim:[number](/docs/luau/numbers)  The time (in seconds) that the current frame has stepped animations. |

The PreAnimation event fires every frame, prior to the physics
simulation but after rendering. The deltaTimeSim argument indicates the
time that the current frame has stepped animations.

This event is useful for modifying animation objects, such as adjusting
their speed or priority. Once the PreAnimation event is complete, the
engine proceeds to run these animations, updating the joint transforms
which will later be used to update objects during the physics simulation.

After animations are stepped, the engine triggers the
[PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation) event.

Provide feedback

---

PreRender

Fires every frame, prior to the frame being rendered.

RunService.PreRender(deltaTimeRender:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| deltaTimeRender:[number](/docs/luau/numbers)  The time (in seconds) that has elapsed since the previous frame. |

The PreRender event (replacement for
[RenderStepped](/docs/reference/engine/classes/RunService#RenderStepped)) fires every frame, prior
to the frame being rendered. The deltaTimeRender argument indicates the
time that has elapsed since the previous frame.

This event allows you to run code and update the world before it's drawn
on a player's screen. This is useful for last‑minute adjustments such as
changing object positions, updating animations, or preparing visual
effects, but it should be used sparingly as the engine cannot start to
render the frame until code running in this event has finished executing.

As PreRender is client-side, it can only be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript), in a [ModuleScript](/docs/reference/engine/classes/ModuleScript) required by a
[LocalScript](/docs/reference/engine/classes/LocalScript), or in a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client).

Following the PreRender phase, the simulation phase begins with the
[PreAnimation](/docs/reference/engine/classes/RunService#PreAnimation) event.

Provide feedback

---

PreSimulation

Fires every frame, prior to the physics simulation.

RunService.PreSimulation(deltaTimeSim:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| deltaTimeSim:[number](/docs/luau/numbers)  The time (in seconds) that the current frame will step the physics simulation, not accounting for physics throttling. |

The PreSimulation event (replacement for
[Stepped](/docs/reference/engine/classes/RunService#Stepped)) fires every frame, prior to the
physics simulation. The deltaTimeSim argument indicates the time that
the current frame will step the physics simulation, not accounting for
physics throttling. This may deviate from the actual time between frames
in Studio edit mode or when framerate is very low.

This event is useful for adjusting properties like velocity or forces just
before they're applied as part of the simulation. The simulation then
runs, potentially multiple times, as the physics solver runs at a higher
frequency than other engine systems. Once this is complete, the
[PostSimulation](/docs/reference/engine/classes/RunService#PostSimulation) event is fired.

Provide feedback

---

RenderStepped

Fires every frame, prior to the frame being rendered.

RunService.RenderStepped(deltaTime:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| deltaTime:[number](/docs/luau/numbers)  The time (in seconds) that has elapsed since the previous frame. |

Fires every frame, prior to the frame being rendered.

##### Migration Note

This event has been superseded by [PreRender](/docs/reference/engine/classes/RunService#PreRender)
which should be used for new work.

Provide feedback

---

Stepped

Fires every frame, prior to the physics simulation.

RunService.Stepped(

time:[number](/docs/luau/numbers), deltaTime:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  The duration (in seconds) that [RunService](/docs/reference/engine/classes/RunService) has been running for. |
| deltaTime:[number](/docs/luau/numbers)  The time (in seconds) that has elapsed since the previous frame. |

Fires every frame, prior to the physics simulation.

##### Migration Note

This event has been superseded by
[PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation) which should be used for
new work.

Provide feedback

---