# ThreadPoolConfig | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ThreadPoolConfig
Scraped: 2026-01-11T02:43:36.155302Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ThreadPoolConfig](/docs/reference/engine/enums/ThreadPoolConfig)

English

Feedback

Engine Enum

ThreadPoolConfig

---

Controls the thread pooling scheme of the underlying 'TaskScheduler'.

See TaskScheduler for details.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Auto | 0 | Let task scheduler make a decision internally. |
| Threads1 | 1 | Utilize 1 worker thread, ignore the physical CPU core count. |
| Threads2 | 2 | Utilize 2 worker threads, ignore the physical CPU core count. |
| Threads3 | 3 | Utilize 3 worker threads, ignore the physical CPU core count. |
| Threads4 | 4 | Utilize 4 worker threads, ignore the physical CPU core count. |
| Threads8 | 8 | Utilize 8 worker threads, ignore the physical CPU core count. |
| Threads16 | 16 | Utilize 16 worker threads, ignore the physical CPU core count. |
| PerCore1 | 101 | Utilize 1 worker thread per available physical CPU core. |
| PerCore2 | 102 | Utilize 2 worker threads per available physical CPU core. |
| PerCore3 | 103 | Utilize 3 worker threads per available physical CPU core. |
| PerCore4 | 104 | Utilize 4 worker threads per available physical CPU core. |