# FaceControls | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/FaceControls
Scraped: 2026-01-11T02:36:58.798844Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- FaceControls
- MeshPart
- WrapTarget
- Bone
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [FaceControls](/docs/reference/engine/classes/FaceControls)

English

Feedback

Engine Class

![FaceControls](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/FaceControls-Dark.webp)FaceControls

The [FaceControls](/docs/reference/engine/classes/FaceControls) object defines a set of properties for controlling
the facial expressions of a Dynamic Head.

---

Summary

Properties

|  |
| --- |
| [ChinRaiser](#ChinRaiser):[number](/docs/luau/numbers) |
| [ChinRaiserUpperLip](#ChinRaiserUpperLip):[number](/docs/luau/numbers) |
| [Corrugator](#Corrugator):[number](/docs/luau/numbers) |
| [EyesLookDown](#EyesLookDown):[number](/docs/luau/numbers) |
| [EyesLookLeft](#EyesLookLeft):[number](/docs/luau/numbers) |
| [EyesLookRight](#EyesLookRight):[number](/docs/luau/numbers) |
| [EyesLookUp](#EyesLookUp):[number](/docs/luau/numbers) |
| [FlatPucker](#FlatPucker):[number](/docs/luau/numbers) |
| [Funneler](#Funneler):[number](/docs/luau/numbers) |
| [JawDrop](#JawDrop):[number](/docs/luau/numbers) |
| [JawLeft](#JawLeft):[number](/docs/luau/numbers) |
| [JawRight](#JawRight):[number](/docs/luau/numbers) |
| [LeftBrowLowerer](#LeftBrowLowerer):[number](/docs/luau/numbers) |
| [LeftCheekPuff](#LeftCheekPuff):[number](/docs/luau/numbers) |
| [LeftCheekRaiser](#LeftCheekRaiser):[number](/docs/luau/numbers) |
| [LeftDimpler](#LeftDimpler):[number](/docs/luau/numbers) |
| [LeftEyeClosed](#LeftEyeClosed):[number](/docs/luau/numbers) |
| [LeftEyeUpperLidRaiser](#LeftEyeUpperLidRaiser):[number](/docs/luau/numbers) |
| [LeftInnerBrowRaiser](#LeftInnerBrowRaiser):[number](/docs/luau/numbers) |
| [LeftLipCornerDown](#LeftLipCornerDown):[number](/docs/luau/numbers) |
| [LeftLipCornerPuller](#LeftLipCornerPuller):[number](/docs/luau/numbers) |
| [LeftLipStretcher](#LeftLipStretcher):[number](/docs/luau/numbers) |
| [LeftLowerLipDepressor](#LeftLowerLipDepressor):[number](/docs/luau/numbers) |
| [LeftNoseWrinkler](#LeftNoseWrinkler):[number](/docs/luau/numbers) |
| [LeftOuterBrowRaiser](#LeftOuterBrowRaiser):[number](/docs/luau/numbers) |
| [LeftUpperLipRaiser](#LeftUpperLipRaiser):[number](/docs/luau/numbers) |
| [LipPresser](#LipPresser):[number](/docs/luau/numbers) |
| [LipsTogether](#LipsTogether):[number](/docs/luau/numbers) |
| [LowerLipSuck](#LowerLipSuck):[number](/docs/luau/numbers) |
| [MouthLeft](#MouthLeft):[number](/docs/luau/numbers) |
| [MouthRight](#MouthRight):[number](/docs/luau/numbers) |
| [Pucker](#Pucker):[number](/docs/luau/numbers) |
| [RightBrowLowerer](#RightBrowLowerer):[number](/docs/luau/numbers) |
| [RightCheekPuff](#RightCheekPuff):[number](/docs/luau/numbers) |
| [RightCheekRaiser](#RightCheekRaiser):[number](/docs/luau/numbers) |
| [RightDimpler](#RightDimpler):[number](/docs/luau/numbers) |
| [RightEyeClosed](#RightEyeClosed):[number](/docs/luau/numbers) |
| [RightEyeUpperLidRaiser](#RightEyeUpperLidRaiser):[number](/docs/luau/numbers) |
| [RightInnerBrowRaiser](#RightInnerBrowRaiser):[number](/docs/luau/numbers) |
| [RightLipCornerDown](#RightLipCornerDown):[number](/docs/luau/numbers) |
| [RightLipCornerPuller](#RightLipCornerPuller):[number](/docs/luau/numbers) |
| [RightLipStretcher](#RightLipStretcher):[number](/docs/luau/numbers) |
| [RightLowerLipDepressor](#RightLowerLipDepressor):[number](/docs/luau/numbers) |
| [RightNoseWrinkler](#RightNoseWrinkler):[number](/docs/luau/numbers) |
| [RightOuterBrowRaiser](#RightOuterBrowRaiser):[number](/docs/luau/numbers) |
| [RightUpperLipRaiser](#RightUpperLipRaiser):[number](/docs/luau/numbers) |
| [TongueDown](#TongueDown):[number](/docs/luau/numbers) |
| [TongueOut](#TongueOut):[number](/docs/luau/numbers) |
| [TongueUp](#TongueUp):[number](/docs/luau/numbers) |
| [UpperLipSuck](#UpperLipSuck):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [FaceControls](/docs/reference/engine/classes/FaceControls) object defines a set of properties for controlling
the facial expressions of a character head capable of animation.

The FaceControls properties are based on the Facial Action Coding System
(FACS), a comprehensive system for describing all visually discernible facial
movement based on anatomy. [FaceControls](/docs/reference/engine/classes/FaceControls) properties can only be set
between 0 and 1. Different combinations of the [FaceControls](/docs/reference/engine/classes/FaceControls) property
values create different facial expressions. Recording multiple facial
expressions over time creates facial animation.

What is an Animatable Head?
---------------------------

An animatable head is a [MeshPart](/docs/reference/engine/classes/MeshPart) that implements a facial rig and is
capable of playing facial animations and triggering facial expressions. A
[FaceControls](/docs/reference/engine/classes/FaceControls) object that is a child of a head [MeshPart](/docs/reference/engine/classes/MeshPart) can
change the facial expressions of the head.

A head consists of the following three components:

* Skinned MeshPart instance for the head geometry with an internal rig that
  deforms this skinned MeshPart
* FaceControls instance that drives the internal rig when properties such as
  FaceControls.JawDrop are changed.
* Cage [WrapTarget](/docs/reference/engine/classes/WrapTarget) instance for tight fitting facial accessories

In a third-party modeling tool, such as Blender or Maya, an artist can create
a joint-driven facial rig, pose the joints to match each of the individual
FACS controls, and save as an FBX. When a head .FBX is imported in Studio, a
facs-to-joint mapping is created. This mapping deforms the mesh geometry when
FaceControls properties are changed. The mapping and the facial rig (including
[Bone](/docs/reference/engine/classes/Bone) instances) are not exposed to developers and can only be accessed
through the FaceControls instance. The [MeshPart](/docs/reference/engine/classes/MeshPart) for a Dynamic Head
looks and behaves the same as a regular [MeshPart](/docs/reference/engine/classes/MeshPart) except when a
FaceControls instance is a child of the MeshPart. Editing the properties of
the FaceControls deforms the MeshPart's geometry. These properties are
available to animate in the Animation Editor.

See [Facial Animation](/docs/art/characters/facial-animation) for
more information on usage and creation of an animatable head.

Animatable Heads in the Marketplace
-----------------------------------

If you are publishing your head to the Marketplace, your head asset must
include a minimum subset of face controls. Roblox's publishing validation
rejects assets without the following required poses:

* EyesLookDown
* EyesLookLeft
* EyesLookRight
* EyesLookUp
* JawDrop
* LeftEyeClosed
* LeftLipCornerPuller
* LeftLipStretcher
* LeftLowerLipDepressor
* LeftUpperLipRaiser
* LipsTogether
* Pucker
* RightEyeClosed
* RightLipCornerPuller
* RightLipStretcher
* RightLowerLipDepressor
* RightUpperLipRaiser

See
[FACS pose reference](/docs/art/characters/facial-animation/facs-poses-reference)
for more information on usage and creation of an animatable head.

---

API Reference

Properties

ChinRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the chin up; moves the lower lip upwards.

FaceControls.ChinRaiser:[number](/docs/luau/numbers)

Raises the chin up; moves the lower lip upwards

Provide feedback

---

ChinRaiserUpperLip

Not Replicated

Plugin Security

Read Parallel

Moves the upper lip when ChinRaiser is engaged and touching the upper lip.

FaceControls.ChinRaiserUpperLip:[number](/docs/luau/numbers)

Moves the upper lip when ChinRaiser is engaged and touching the upper lip

Provide feedback

---

Corrugator

Not Replicated

Plugin Security

Read Parallel

Brings the left and right brows inward together.

FaceControls.Corrugator:[number](/docs/luau/numbers)

Brings the left and right brows inward together

Provide feedback

---

EyesLookDown

Not Replicated

Plugin Security

Read Parallel

Moves gaze down. This is a required pose for avatars.

FaceControls.EyesLookDown:[number](/docs/luau/numbers)

Moves gaze down. This is a required pose for avatars.

Provide feedback

---

EyesLookLeft

Not Replicated

Plugin Security

Read Parallel

Moves gaze left. This is a required pose for avatars.

FaceControls.EyesLookLeft:[number](/docs/luau/numbers)

Moves gaze left. This is a required pose for avatars.

Provide feedback

---

EyesLookRight

Not Replicated

Plugin Security

Read Parallel

Moves gaze right. This is a required pose for avatars.

FaceControls.EyesLookRight:[number](/docs/luau/numbers)

Moves gaze right. This is a required pose for avatars.

Provide feedback

---

EyesLookUp

Not Replicated

Plugin Security

Read Parallel

Moves gaze up. This is a required pose for avatars.

FaceControls.EyesLookUp:[number](/docs/luau/numbers)

Moves gaze up. This is a required pose for avatars.

Provide feedback

---

FlatPucker

Not Replicated

Plugin Security

Read Parallel

Also known as lip tightener; brings the corners of the mouth inward and
pressing the lips back against the teeth.

FaceControls.FlatPucker:[number](/docs/luau/numbers)

Also known as lip tightener; brings the corners of the mouth inward and
pressing the lips back against the teeth

Provide feedback

---

Funneler

Not Replicated

Plugin Security

Read Parallel

Makes a 'O' shape with the mouth.

FaceControls.Funneler:[number](/docs/luau/numbers)

Makes a 'O' shape with the mouth

Provide feedback

---

JawDrop

Not Replicated

Plugin Security

Read Parallel

Lowers the jaw downward opening the mouth. This is a required pose for
avatars.

FaceControls.JawDrop:[number](/docs/luau/numbers)

Lowers the jaw downward opening the mouth. This is a required pose for
avatars.

Provide feedback

---

JawLeft

Not Replicated

Plugin Security

Read Parallel

Moves mouth and jaw to the left (character left).

FaceControls.JawLeft:[number](/docs/luau/numbers)

Provide feedback

---

JawRight

Not Replicated

Plugin Security

Read Parallel

Moves mouth and jaw to the right (character right).

FaceControls.JawRight:[number](/docs/luau/numbers)

Moves mouth and jaw to the right (character right)

Provide feedback

---

LeftBrowLowerer

Not Replicated

Plugin Security

Read Parallel

Lowers the left brow down.

FaceControls.LeftBrowLowerer:[number](/docs/luau/numbers)

Lowers the left brow down

Provide feedback

---

LeftCheekPuff

Not Replicated

Plugin Security

Read Parallel

Puffs up the left cheek.

FaceControls.LeftCheekPuff:[number](/docs/luau/numbers)

Puffs up the left cheek

Provide feedback

---

LeftCheekRaiser

Not Replicated

Plugin Security

Read Parallel

Squints the left eye.

FaceControls.LeftCheekRaiser:[number](/docs/luau/numbers)

Squints the left eye

Provide feedback

---

LeftDimpler

Not Replicated

Plugin Security

Read Parallel

Moves the corners of the mouth back in Z.

FaceControls.LeftDimpler:[number](/docs/luau/numbers)

Moves the corners of the mouth back in Z

Provide feedback

---

LeftEyeClosed

Not Replicated

Plugin Security

Read Parallel

Closes the left eyelid. This is a required pose for avatars.

FaceControls.LeftEyeClosed:[number](/docs/luau/numbers)

Closes the left eyelid. This is a required pose for avatars.

Provide feedback

---

LeftEyeUpperLidRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the left eyelid upwards to reveal more of the eye white above the
iris.

FaceControls.LeftEyeUpperLidRaiser:[number](/docs/luau/numbers)

Raises the left eyelid upwards to reveal more of the eye white above the
iris

Provide feedback

---

LeftInnerBrowRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the interior half of the left brow upwards.

FaceControls.LeftInnerBrowRaiser:[number](/docs/luau/numbers)

Raises the interior half of the left brow upwards

Provide feedback

---

LeftLipCornerDown

Not Replicated

Plugin Security

Read Parallel

Lowers the corners of the mouth downwards in a frown.

FaceControls.LeftLipCornerDown:[number](/docs/luau/numbers)

Lowers the corners of the mouth downwards in a frown

Provide feedback

---

LeftLipCornerPuller

Not Replicated

Plugin Security

Read Parallel

Raises the corners of the mouth upwards in a smile. This is a required
pose for avatars.

FaceControls.LeftLipCornerPuller:[number](/docs/luau/numbers)

Raises the corners of the mouth upwards in a smile. This is a required
pose for avatars.

Provide feedback

---

LeftLipStretcher

Not Replicated

Plugin Security

Read Parallel

Stretches the corners of the mouth apart. This is a required pose for
avatars.

FaceControls.LeftLipStretcher:[number](/docs/luau/numbers)

Stretches the corners of the mouth apart. This is a required pose for
avatars.

Provide feedback

---

LeftLowerLipDepressor

Not Replicated

Plugin Security

Read Parallel

Lowers the lower lip down away from the upper lip revealing the lower
teeth. This is a required pose for avatars.

FaceControls.LeftLowerLipDepressor:[number](/docs/luau/numbers)

Lowers the lower lip down away from the upper lip revealing the lower
teeth. This is a required pose for avatars.

Provide feedback

---

LeftNoseWrinkler

Not Replicated

Plugin Security

Read Parallel

Raise the left nostril, pulls the brow down slightly, and wrinkles on the
side of the nose.

FaceControls.LeftNoseWrinkler:[number](/docs/luau/numbers)

Raise the left nostril, pulls the brow down slightly, and wrinkles on the
side of the nose

Provide feedback

---

LeftOuterBrowRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the outer part of the left brow upwards.

FaceControls.LeftOuterBrowRaiser:[number](/docs/luau/numbers)

Raises the outer part of the left brow upwards

Provide feedback

---

LeftUpperLipRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the left upper lip away from the lower lip revealing the upper
teeth. This is a required pose for avatars.

FaceControls.LeftUpperLipRaiser:[number](/docs/luau/numbers)

Raises the left upper lip away from the lower lip revealing the upper
teeth. This is a required pose for avatars.

Provide feedback

---

LipPresser

Not Replicated

Plugin Security

Read Parallel

Presses the lips together.

FaceControls.LipPresser:[number](/docs/luau/numbers)

Presses the lips together

Provide feedback

---

LipsTogether

Not Replicated

Plugin Security

Read Parallel

Brings the lips together relative to JawDrop. This is a required pose for
avatars.

FaceControls.LipsTogether:[number](/docs/luau/numbers)

Brings the lips together relative to JawDrop. This is a required pose for
avatars.

Provide feedback

---

LowerLipSuck

Not Replicated

Plugin Security

Read Parallel

Rolls the lower lip up over the teeth.

FaceControls.LowerLipSuck:[number](/docs/luau/numbers)

Rolls the lower lip up over the teeth

Provide feedback

---

MouthLeft

Not Replicated

Plugin Security

Read Parallel

Moves the mouth left.

FaceControls.MouthLeft:[number](/docs/luau/numbers)

Moves the mouth left

Provide feedback

---

MouthRight

Not Replicated

Plugin Security

Read Parallel

Moves the mouth right.

FaceControls.MouthRight:[number](/docs/luau/numbers)

Moves the mouth right

Provide feedback

---

Pucker

Not Replicated

Plugin Security

Read Parallel

Makes a kiss-like shape with the mouth. This is a required pose for
avatars.

FaceControls.Pucker:[number](/docs/luau/numbers)

Makes a kiss-like shape with the mouth. This is a required pose for
avatars.

Provide feedback

---

RightBrowLowerer

Not Replicated

Plugin Security

Read Parallel

Lowers the right brow down.

FaceControls.RightBrowLowerer:[number](/docs/luau/numbers)

Lowers the right brow down

Provide feedback

---

RightCheekPuff

Not Replicated

Plugin Security

Read Parallel

Puffs up the right cheek.

FaceControls.RightCheekPuff:[number](/docs/luau/numbers)

Puffs up the right cheek

Provide feedback

---

RightCheekRaiser

Not Replicated

Plugin Security

Read Parallel

Squints the right eye.

FaceControls.RightCheekRaiser:[number](/docs/luau/numbers)

Squints the right eye

Provide feedback

---

RightDimpler

Not Replicated

Plugin Security

Read Parallel

Moves the corners of the mouth back in Z.

FaceControls.RightDimpler:[number](/docs/luau/numbers)

Moves the corners of the mouth back in Z

Provide feedback

---

RightEyeClosed

Not Replicated

Plugin Security

Read Parallel

Closes the right eyelid. This is a required pose for avatars.

FaceControls.RightEyeClosed:[number](/docs/luau/numbers)

Closes the right eyelid. This is a required pose for avatars.

Provide feedback

---

RightEyeUpperLidRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the right eyelid upwards to reveal more of the eye white above the
iris.

FaceControls.RightEyeUpperLidRaiser:[number](/docs/luau/numbers)

Raises the right eyelid upwards to reveal more of the eye white above the
iris

Provide feedback

---

RightInnerBrowRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the interior half of the right brow upwards.

FaceControls.RightInnerBrowRaiser:[number](/docs/luau/numbers)

Raises the interior half of the right brow upwards

Provide feedback

---

RightLipCornerDown

Not Replicated

Plugin Security

Read Parallel

Lowers the corners of the mouth downwards in a frown.

FaceControls.RightLipCornerDown:[number](/docs/luau/numbers)

Lowers the corners of the mouth downwards in a frown

Provide feedback

---

RightLipCornerPuller

Not Replicated

Plugin Security

Read Parallel

Raises the corners of the mouth upwards in a smile. This is a required
pose for avatars.

FaceControls.RightLipCornerPuller:[number](/docs/luau/numbers)

Raises the corners of the mouth upwards in a smile. This is a required
pose for avatars.

Provide feedback

---

RightLipStretcher

Not Replicated

Plugin Security

Read Parallel

Stretches the corners of the mouth apart. This is a required pose for
avatars.

FaceControls.RightLipStretcher:[number](/docs/luau/numbers)

Stretches the corners of the mouth apart. This is a required pose for
avatars.

Provide feedback

---

RightLowerLipDepressor

Not Replicated

Plugin Security

Read Parallel

Lowers the lower lip down away from the upper lip revealing the lower
teeth. This is a required pose for avatars.

FaceControls.RightLowerLipDepressor:[number](/docs/luau/numbers)

Lowers the lower lip down away from the upper lip revealing the lower
teeth. This is a required pose for avatars.

Provide feedback

---

RightNoseWrinkler

Not Replicated

Plugin Security

Read Parallel

Raises the right nostril, pulls the brow down slightly, and wrinkles on
the side of the nose.

FaceControls.RightNoseWrinkler:[number](/docs/luau/numbers)

Raises the right nostril, pulls the brow down slightly, and wrinkles on
the side of the nose

Provide feedback

---

RightOuterBrowRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the outer part of the right brow upwards.

FaceControls.RightOuterBrowRaiser:[number](/docs/luau/numbers)

Raises the outer part of the right brow upwards

Provide feedback

---

RightUpperLipRaiser

Not Replicated

Plugin Security

Read Parallel

Raises the right upper lip away from the lower lip revealing the upper
teeth. This is a required pose for avatars.

FaceControls.RightUpperLipRaiser:[number](/docs/luau/numbers)

Raises the right upper lip away from the lower lip revealing the upper
teeth. This is a required pose for avatars.

Provide feedback

---

TongueDown

Not Replicated

Plugin Security

Read Parallel

Bends the tongue down.

FaceControls.TongueDown:[number](/docs/luau/numbers)

Bends the tongue down

Provide feedback

---

TongueOut

Not Replicated

Plugin Security

Read Parallel

Extends the tip of the tongue out of the mouth.

FaceControls.TongueOut:[number](/docs/luau/numbers)

Extends the tip of the tongue out of the mouth

Provide feedback

---

TongueUp

Not Replicated

Plugin Security

Read Parallel

Bends the tongue up.

FaceControls.TongueUp:[number](/docs/luau/numbers)

Bends the tongue up

Provide feedback

---

UpperLipSuck

Not Replicated

Plugin Security

Read Parallel

Rolls the upper lip around the teeth.

FaceControls.UpperLipSuck:[number](/docs/luau/numbers)

Rolls the upper lip around the teeth

Provide feedback

---