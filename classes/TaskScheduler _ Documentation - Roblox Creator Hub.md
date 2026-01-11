# TaskScheduler | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TaskScheduler
Scraped: 2026-01-11T02:35:34.059746Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- TaskScheduler
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TaskScheduler](/docs/reference/engine/classes/TaskScheduler)

English

Feedback

Engine Class

![TaskScheduler](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TaskScheduler-Dark.webp)TaskScheduler

Collection of settings for the *Task Scheduler* feature.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [SchedulerDutyCycle](#SchedulerDutyCycle):[number](/docs/luau/numbers) |
| [SchedulerRate](#SchedulerRate):[number](/docs/luau/numbers) |
| [ThreadPoolConfig](#ThreadPoolConfig):[Enum.ThreadPoolConfig](/docs/reference/engine/enums/ThreadPoolConfig) |
| [ThreadPoolSize](#ThreadPoolSize):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

TaskScheduler is a read-only settings class responsible for the Task Scheduler
feature. Can be found in Roblox Studio's settings with the name *Task
Scheduler*.

---

API Reference

Properties

SchedulerDutyCycle

Read Only

Not Replicated

Read Parallel

The average time divided by the average interval of the duty cycle.

TaskScheduler.SchedulerDutyCycle:[number](/docs/luau/numbers)

The average time divided by the average interval of the duty cycle.

Provide feedback

---

SchedulerRate

Read Only

Not Replicated

Read Parallel

The current average rate of the task scheduler.

TaskScheduler.SchedulerRate:[number](/docs/luau/numbers)

The current average rate of the task scheduler.

Provide feedback

---

ThreadPoolConfig

Read Parallel

The specified thread pooling configuration for the task scheduler.

TaskScheduler.ThreadPoolConfig:[Enum.ThreadPoolConfig](/docs/reference/engine/enums/ThreadPoolConfig)

The specified thread pooling configuration for the task scheduler.

Provide feedback

---

ThreadPoolSize

Read Only

Not Replicated

Read Parallel

The current size of the thread pool.

TaskScheduler.ThreadPoolSize:[number](/docs/luau/numbers)

The current size of the thread pool.

Provide feedback

---