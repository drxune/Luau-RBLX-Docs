# Configuration | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Configuration
Scraped: 2026-01-11T02:32:55.019429Z

## Inherits
- Object
- Instance
- Configuration
- Tools
- Scripts
- Folder
- BrickColorValue
- NumberValue
- IntValue
- ObjectValue
- Script
- LocalScript
- BasePart
- Model
- Tool
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Configuration](/docs/reference/engine/classes/Configuration)

English

Feedback

Engine Class

![Configuration](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Configuration-Dark.webp)Configuration

The Configuration object is a container object that is designed to hold value
objects to make values used in [Tools](/docs/reference/engine/classes/Tool) or any model using
[Scripts](/docs/reference/engine/classes/Script) more accessible.

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Configuration object is a container object that is designed to hold value
objects to make values used in [Tools](/docs/reference/engine/classes/Tool) or any model using
[Scripts](/docs/reference/engine/classes/Script) more accessible.

How does the Configuration object work?
---------------------------------------

The Configuration object is just a container, and does not automatically offer
any additional functionality to a [Folder](/docs/reference/engine/classes/Folder).

Configurations should hold value objects ([BrickColorValue](/docs/reference/engine/classes/BrickColorValue),
[NumberValue](/docs/reference/engine/classes/NumberValue), [IntValue](/docs/reference/engine/classes/IntValue), [ObjectValue](/docs/reference/engine/classes/ObjectValue) etc). These value
objects should be read by the [Script](/docs/reference/engine/classes/Script) or [LocalScript](/docs/reference/engine/classes/LocalScript) associated
with the configuration to determine constants such as damage, speed or color.

For example,

```
local damage = 10
```

Becomes:

```
local configuration = tool:FindFirstChildWhichIsA("Configuration", true)



damage = configuration:FindFirstChild("Damage").Value -- A NumberValue
```

The Configuration object is intended to be placed inside a [BasePart](/docs/reference/engine/classes/BasePart) in
a [Model](/docs/reference/engine/classes/Model) or [Tool](/docs/reference/engine/classes/Tool). It was originally intended to be used with a
tool that provided a GUI interface to edit these properties. However it is
more common now for developers to edit these values directly in the Roblox
Studio properties window.

Why should I use the Configuration object?
------------------------------------------

Use of Configurations is optional, but a number of developers chose to use
them for the following reasons.

* Variables held in a Configuration can be found quickly and are in a single
  place
* When sharing your work, others can make changes without needing to modify
  your code
* Provides a single location for variables read by multiple scripts in more
  complex games