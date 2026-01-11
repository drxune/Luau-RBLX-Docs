# TouchTransmitter | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TouchTransmitter
Scraped: 2026-01-11T02:34:03.760838Z

## Tags
- Not Creatable

## Inherits
- Instance
- TouchTransmitter
- BasePart.Touched
- BasePart.TouchEnded
- Object
- BasePart
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TouchTransmitter](/docs/reference/engine/classes/TouchTransmitter)

English

Feedback

Engine Class

TouchTransmitter

An internal object used by networking and replication code to transmit
[BasePart.Touched](/docs/reference/engine/classes/BasePart#Touched) and [BasePart.TouchEnded](/docs/reference/engine/classes/BasePart#TouchEnded) events.

Not Creatable

Not Browsable

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An internal object used by networking and replication code to transmit
[BasePart.Touched](/docs/reference/engine/classes/BasePart#Touched) and [BasePart.TouchEnded](/docs/reference/engine/classes/BasePart#TouchEnded) events.

The TouchTransmitter object named 'TouchInterest' is created and parented to a
[BasePart](/docs/reference/engine/classes/BasePart) when the [BasePart.Touched](/docs/reference/engine/classes/BasePart#Touched) or
[BasePart.TouchEnded](/docs/reference/engine/classes/BasePart#TouchEnded) events are listened (connected) to.

Removing the TouchTransmitter will prevent the touched events from working.
The TouchTransmitter object can also be removed exclusively on the client.
This will prevent collisions from models the client has network ownership of
(such as the player's character) from registering.

Note, in almost all circumstances developers should disconnect the connection
using [RBXScriptConnection:Disconnect()](/docs/reference/engine/datatypes/RBXScriptConnection#Disconnect) method rather than removing
the TouchTransmitter. Otherwise the connection will not be cleaned up which
can cause performance issues over time.