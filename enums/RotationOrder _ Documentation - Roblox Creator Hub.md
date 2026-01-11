# RotationOrder | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/RotationOrder
Scraped: 2026-01-11T02:42:54.864203Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [RotationOrder](/docs/reference/engine/enums/RotationOrder)

English

Feedback

Engine Enum

RotationOrder

---

Euler angles encode a rotation in 3D space via a sequence of three rotations
along the X, Y, and Z axes. The RotationOrder enum specifies the order in
which the engine performs these rotations.

To help visualize the many rotation orders, you can test them manually in
Studio with the [Rotate](/docs/../../../parts#rotate) tool or by inserting
[task.wait()](/docs/reference/engine/libraries/task#wait) statements between individual rotations of a cube with a
unique face:

```
local Workspace = game:GetService("Workspace")



local cube = Workspace.Cube



local rx, ry, rz = math.rad(90), math.rad(90), math.rad(90)



task.wait(5)



cube.CFrame *= CFrame.fromEulerAngles(rx, 0, 0)  -- X



task.wait(5)



cube.CFrame *= CFrame.fromEulerAngles(0, ry, 0)  -- Y



task.wait(5)



cube.CFrame *= CFrame.fromEulerAngles(0, 0, rz)  -- Z
```

An equivalent operation is:

```
local Workspace = game:GetService("Workspace")



local cube = Workspace.Cube



local rx, ry, rz = math.rad(90), math.rad(90), math.rad(90)



cube.CFrame = CFrame.fromEulerAngles(rx, ry, rz, Enum.RotationOrder.XYZ)
```

Items

| Name | Value | Summary |
| --- | --- | --- |
| XYZ | 0 | X, Y, Z order. |
| XZY | 1 | X, Z, Y order. |
| YZX | 2 | Y, Z, X order. |
| YXZ | 3 | Y, X, Z order. |
| ZXY | 4 | Z, X, Y order. |
| ZYX | 5 | Z, Y, X order. |