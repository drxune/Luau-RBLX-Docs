# ParticleFlipbookMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ParticleFlipbookMode
Scraped: 2026-01-11T02:44:28.720740Z

## Inherits
- ParticleEmitter.FlipbookFramerate
- ParticleEmitter.Lifetime
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ParticleFlipbookMode](/docs/reference/engine/enums/ParticleFlipbookMode)

English

Feedback

Engine Enum

ParticleFlipbookMode

---

Determines the type of the flipbook animation.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Loop | 0 | Continuously play through all frames, starting back at the first frame after playing the last. |
| OneShot | 1 | Play through the animation only once across the particle's lifetime. With this setting, the [ParticleEmitter.FlipbookFramerate](/docs/reference/engine/classes/ParticleEmitter#FlipbookFramerate) property doesn't apply; instead, the framerate is determined by the particle's [ParticleEmitter.Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime) divided evenly by the number of frames in the animation. OneShot animations are useful for clear non-repeating animations, such as an explosion that creates a puff of smoke and then fades out. |
| PingPong | 2 | Play from the first to the last frame, then in reverse from the last to the first, repeating throughout the [ParticleEmitter.Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime) of the particle. |
| Random | 3 | Play the frames in a random order, blending/crossfading from one frame to the next. This can be useful for organic particle textures at low framerates, such as stars slowly twinkling between subtly different shapes. |