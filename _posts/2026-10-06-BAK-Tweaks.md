---
layout: post
title:  "BAK Tweaks"
date:   2026-10-06 21:30:00 +0200
image:  BAK_POST.jpg
tags:   Screenshooting
---

**BAK Tweaks** is an in-game utility for **Batman: Arkham Knight** built for virtual photography, cinematic captures and experimentation.

It brings several useful game systems together in one compact interface: dynamic lights, light gizmos, weather, lightning, cape controls, post-process exposure and a selection of environment effects.

The idea is simple: give you useful controls and let you experiment. There are no fixed lighting recipes and no single "correct" setup. Different locations, materials and scenes react very differently, so the fun is in trying things.

## Main Features

* Runtime **Point Light** and **Spot Light** creation
* Real-time light editing
* Multiple light gizmos visible at the same time
* Individual gizmo toggle for every created light
* Exposure control
* Rain, snow, dust and pollen controls
* Manual lightning controls
* Cape controls
* Radio Mode Eyes
* Gauntlet Light
* Vehicle and burning vehicle effects
* Combat VFX controls
* Automatic cleanup of spawned lights when a level is restarted or changed

## BatLit

**BatLit** is the runtime lighting system included in BAK Tweaks.

Point Lights and Spot Lights can be created directly in-game and adjusted while building a shot.

Depending on the light type, you can work with position, rotation, intensity, radius, cone angle and enabled state.

The goal is not to reproduce the game's original lighting exactly. BatLit is there to give you extra creative control when the existing scene needs a little more shape, separation or atmosphere.

## Light Gizmos

Each created light has its own **Gizmo** checkbox, so you can decide exactly which helpers remain visible.

Several gizmos can be displayed at the same time, which is useful when working with a small lighting setup instead of a single light.

The colors are intentionally simple:

* **White** - Light position
* **Gray** - Point Light radius
* **Red** - Spot Light direction
* **Blue** - Spot Light cone

Point Lights display their spherical influence radius.

Spot Lights keep the display cleaner: they show the direction and cone, without the large radius sphere.

<!-- Add the BAK Tweaks gizmo screenshot here.
<div style="width:85%; margin:auto;">
<img src="/images/BAKTweaks/BAKTweaks_Gizmo.jpg" alt="BAK Tweaks BatLit gizmos" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
-->

## A Few Examples

These are ideas rather than presets. The values that work in one scene may look completely different somewhere else.

### Separate Batman From The Background

A Spot Light placed behind or to the side of the character can help create a stronger outline and make the silhouette stand out against a dark background.

Use the red direction line and blue cone to see where the Spot Light is actually aimed, then move and rotate it until the result fits the scene.

### Add A Little Fill

A Point Light can be useful when part of a character or environment falls completely into shadow.

The gray radius sphere gives a quick visual indication of the area influenced by the light. Moving the light a short distance can often matter more than simply increasing its intensity.

### Build With Several Lights

Because every created light has an independent gizmo toggle, you can keep several helpers visible while arranging a scene.

For example, one light might shape the subject while another affects the background or a nearby prop. Once the placement is finished, disable the gizmos individually without removing the lights.

### Mix Lighting And Environment

Lighting does not have to be used on its own.

Rain, lightning, exposure and the existing scene lighting can all change the way a custom light feels. A setup that looks subtle in a dry scene can become much more dramatic once wet surfaces and lightning are involved.

Experiment rather than treating any value as a recipe.

## Environment

The **Environment** tab exposes several effects already used by Arkham Knight.

### Weather

Weather controls are kept compact and direct:

* Rain
* Snow
* Dust
* Pollen

Each effect can be adjusted from the main Weather section without opening additional sub-panels.

Not every location reacts in exactly the same way, so some effects are more useful in certain parts of the game than others.

### Lightning

Lightning can be triggered and adjusted independently.

It can be useful for dramatic backlighting, brighter skies or simply experimenting with the way a location responds to a sudden light source.

### Misc

Additional environment and VFX controls are available as direct checkboxes:

* Radio Mode Eyes
* Gauntlet Light
* Vehicles
* Vehicles On Fire
* Combat VFX

These are intentionally simple toggles so they can be switched on and off quickly while composing a scene.

## Cape

The **Cape** tab provides access to several parameters related to Batman's cape simulation.

The result depends heavily on the current animation, movement and environment. Rather than recommending one set of values, the controls are best treated as another creative tool to experiment with while setting up a shot.

## Exposure

BAK Tweaks also provides control over level post-process exposure.

This can be especially useful after adding custom lights, since the same light can look very different depending on the current exposure and environment.

Small changes are often enough.

## Interface

BAK Tweaks uses a compact dark interface designed to stay out of the way while working.

The UI can be hidden while keeping selected light gizmos visible in the game.

The interface and gizmos are independent, so it is possible to work with several visible light helpers without keeping the full menu open.

## Installation

Copy or inject:

`BAKTweaks.dll`

using your preferred DLL injector after **Batman: Arkham Knight** has reached gameplay.

BAK Tweaks creates:

`BAKTweaks.log`

for diagnostic information. The log is reset when BAK Tweaks starts, so it only contains information from the current session.

## Notes

BAK Tweaks modifies game systems at runtime and is intended primarily for screenshot and cinematic use.

Spawned lights belong to the current level. When the level is restarted or changed, BAK Tweaks clears the old spawned-light records and gizmos instead of carrying them into the next scene.

Some environment effects depend on the current map, game state or assets loaded by the game, so their visual result can vary between locations.

Most importantly: **experiment**. BAK Tweaks is meant to provide tools, not recipes.
