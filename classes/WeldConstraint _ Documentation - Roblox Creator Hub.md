# WeldConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WeldConstraint
Scraped: 2026-01-11T02:38:12.802010Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- WeldConstraint
- BaseParts
- BasePart
- WeldConstraints
- Position
- Workspace
- Weld
- Snap
- Motor
- Motor6D
- BasePart.Position
- BasePart.Orientation
- WeldConstraint.Part0
- WeldConstraint.Part1
- WeldConstraint.Enabled
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [WeldConstraint](/docs/reference/engine/classes/WeldConstraint)

English

Feedback

Engine Class

![WeldConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/WeldConstraint-Dark.webp)WeldConstraint

Connects two [BaseParts](/docs/reference/engine/classes/BasePart) together such that their relative
position and orientation remain the same.

---

Summary

Properties

|  |
| --- |
| [Active](#Active):[boolean](/docs/luau/booleans) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Part0](#Part0):[BasePart](/docs/reference/engine/classes/BasePart) |
| [Part1](#Part1):[BasePart](/docs/reference/engine/classes/BasePart) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

WeldConstraint connects two [BaseParts](/docs/reference/engine/classes/BasePart) and ensures they
stay in the same relative position/orientation to each other, meaning that if
one part moves, the other moves the same amount. Even if the two parts are not
touching, they can be welded together.

The most common way to create a weld constraint is by selecting Weld
through Studio's Create menu in the toolbar's Model tab.

Note that this tool behaves differently depending on how many
[BaseParts](/docs/reference/engine/classes/BasePart) are selected when the tool is activated:

* If no [BaseParts](/docs/reference/engine/classes/BasePart) are selected, the next two
  [BaseParts](/docs/reference/engine/classes/BasePart) clicked will be connected by a new
  [WeldConstraint](/docs/reference/engine/classes/WeldConstraint). If the same [BasePart](/docs/reference/engine/classes/BasePart) is clicked twice, no
  constraint will be created.
* If one [BasePart](/docs/reference/engine/classes/BasePart) is already selected, the next [BasePart](/docs/reference/engine/classes/BasePart)
  clicked will be connected to the selected one with a new
  [WeldConstraint](/docs/reference/engine/classes/WeldConstraint).
* If multiple [BaseParts](/docs/reference/engine/classes/BasePart) are selected, those which are
  touching or overlapping will be automatically welded together by new
  [WeldConstraints](/docs/reference/engine/classes/WeldConstraint).

#### Repositioning Behavior

Moving a welded [BasePart](/docs/reference/engine/classes/BasePart) behaves differently depending on whether the
part was moved through its [Position](/docs/reference/engine/classes/BasePart#Position) or through its
[CFrame](/docs/reference/engine/datatypes/CFrame).

* If a welded part's [Position](/docs/reference/engine/classes/BasePart#Position) is updated, that part
  will move but none of the connected parts will move with it. The weld will
  recalculate the offset from the other parts based on the moved part's new
  position.
* If a welded part's [CFrame](/docs/reference/engine/datatypes/CFrame) is updated, that part will move and
  all of the connected parts will also move, ensuring they maintain the same
  offset as when the weld was created.

---

API Reference

Properties

Active

Read Only

Not Replicated

Read Parallel

Indicates if the WeldConstraint is currently active in the world.

WeldConstraint.Active:[boolean](/docs/luau/booleans)

True if the WeldConstraint is currently active in the world.

If the WeldConstraint or one of its parts is not in [Workspace](/docs/reference/engine/classes/Workspace) the
weld will be inactive.

Rigid joints like [Weld](/docs/reference/engine/classes/Weld), [Snap](/docs/reference/engine/classes/Snap), [WeldConstraint](/docs/reference/engine/classes/WeldConstraint),
[Motor](/docs/reference/engine/classes/Motor), or [Motor6D](/docs/reference/engine/classes/Motor6D) may also be disabled due to conflicts
with other rigid joints, such as joints between the same two parts or
indirect cycles in the weld graph. Joints disabled this way may be
re-enabled later when another joint or part is added or removed.

Duplicate WeldConstraints do not conflict because WeldConstraints derive
their internal CFrames from the relative positions of their parts when
they are enabled and all update when [BasePart.Position](/docs/reference/engine/classes/BasePart#Position) or
[BasePart.Orientation](/docs/reference/engine/classes/BasePart#Orientation) is set on a part. The spanning tree may still
disable them if they are redundant or form a cycle.

Provide feedback

---

Enabled

Not Replicated

Read Parallel

Toggles the constraint on and off.

WeldConstraint.Enabled:[boolean](/docs/luau/booleans)

The Enabled property of a [WeldConstraint](/docs/reference/engine/classes/WeldConstraint) sets whether the
constraint is active or not. When this property is set to true, if the
constraint's [WeldConstraint.Part0](/docs/reference/engine/classes/WeldConstraint#Part0) and [WeldConstraint.Part1](/docs/reference/engine/classes/WeldConstraint#Part1)
properties are set, then the constraint will ensure that its two connected
parts will be locked together.

Provide feedback

---

Part0

Not Replicated

Read Parallel

The first part connected by the constraint.

WeldConstraint.Part0:[BasePart](/docs/reference/engine/classes/BasePart)

The Part0 and [WeldConstraint.Part1](/docs/reference/engine/classes/WeldConstraint#Part1) properties of a
[WeldConstraint](/docs/reference/engine/classes/WeldConstraint) set which two [BasePart](/docs/reference/engine/classes/BasePart) the weld connects.
As soon as both properties are set and the weld is
[WeldConstraint.Enabled](/docs/reference/engine/classes/WeldConstraint#Enabled), the weld will lock the two parts together.

If Part0 or Part1 are ever set to new parts, then the WeldConstraint
will instantly link the new part. The old part will no longer be
constrained.

```
local Workspace = game:GetService("Workspace")



local partA = Instance.new("Part")



local partB = Instance.new("Part")



partA.Position = Vector3.new(0, 10, 0)



partA.Parent = Workspace



partB.Position = Vector3.new(0, 10, 10)



partB.Parent = Workspace



local weld = Instance.new("WeldConstraint")



weld.Part0 = partA



weld.Part1 = partB



weld.Parent = partA
```

Provide feedback

---

Part1

Not Replicated

Read Parallel

The second part connected by the constraint.

WeldConstraint.Part1:[BasePart](/docs/reference/engine/classes/BasePart)

The [WeldConstraint.Part0](/docs/reference/engine/classes/WeldConstraint#Part0) and Part1 properties of a
[WeldConstraint](/docs/reference/engine/classes/WeldConstraint) set which two [BasePart](/docs/reference/engine/classes/BasePart) the weld connects.
As soon as both properties are set and the weld is
[WeldConstraint.Enabled](/docs/reference/engine/classes/WeldConstraint#Enabled), the weld will lock the two parts together.

If Part0 or Part1 are ever set to new parts, then the WeldConstraint
will instantly link the new part. The old part will no longer be
constrained.

```
local Workspace = game:GetService("Workspace")



local partA = Instance.new("Part")



local partB = Instance.new("Part")



partA.Position = Vector3.new(0, 10, 0)



partA.Parent = Workspace



partB.Position = Vector3.new(0, 10, 10)



partB.Parent = Workspace



local weld = Instance.new("WeldConstraint")



weld.Part0 = partA



weld.Part1 = partB



weld.Parent = partA
```

Provide feedback

---