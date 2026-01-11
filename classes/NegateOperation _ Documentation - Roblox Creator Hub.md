# NegateOperation | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NegateOperation
Scraped: 2026-01-11T02:33:00.394184Z

## Inherits
- PartOperation
- NegateOperation
- TriangleMeshPart
- BasePart
- PVInstance
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PartOperation](/docs/reference/engine/classes/PartOperation)
6. /
7. [NegateOperation](/docs/reference/engine/classes/NegateOperation)

English

Feedback

Engine Class

![NegateOperation](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/NegateOperation-Dark.webp)NegateOperation

Result of a part that has been negated for use in solid modeling.

---

Summary

Inherited Members

5 inherited from [PartOperation](/docs/reference/engine/classes/PartOperation)

3 inherited from [TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart)

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A NegateOperation is the result of a part that has been negated through
Studio's solid modeling Negate tool.

A negated part turns pink and translucent as an indicator of its state. If the
negated part is then unioned with a normal part using the Union tool,
sections where the negated part overlaps the normal part will be cut out.

Note that you can undo part negation by selecting the negated part and
clicking Negate again.

See [Solid Modeling](/docs/parts/solid-modeling) to learn more about
Studio's solid modeling tools and methods.