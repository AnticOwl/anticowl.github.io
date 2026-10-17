---
layout: page
title: "ResonantTool — CONTROL Resonant"
permalink: /resonanttool/
---

# ResonantTool

**ResonantTool** is an in-game lighting and visual adjustment utility for **CONTROL Resonant**, designed for virtual photography, cinematic screenshots and experimenting with the look of a scene.

It lets you create and adjust lights, fine-tune post-processing and explore level-of-detail settings without having to leave the game.

The idea is simple: **make a scene your own**. Add a soft light to a face, push some color into the background, adjust bloom or change how distant details appear. There are no required presets or recommended values — experiment and keep what looks good to you.

<!-- Screenshot to be provided later.
<div style="width:85%; margin:auto;">
<img src="/images/RESONANTTOOL_01.jpg" alt="ResonantTool in-game interface" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
-->

## Main Features

* Create **Spot Lights** and **Point Lights** directly in-game.
* Adjust the lighting of a scene in real time.
* Change light position, direction, color and intensity.
* Work with bloom, radial blur, brightness, saturation and other post-process settings.
* Experiment with vegetation and object detail using LOD controls.
* Keep the interface out of the way while composing a screenshot.

## Getting Started

1. Launch **CONTROL Resonant** and load into gameplay.
2. Inject `ResonantTool.dll` using your preferred DLL injector.
3. Press **F11** to show or hide the interface.
4. Choose the tab you want to use and adjust the scene.

ResonantTool uses an in-game **DirectX 12** interface. The tool also comes with an **injector EXE** to load `ResonantTool.dll` into the game.

When a control has an **Override** checkbox, enable it if you want that setting to take priority over the game's own updates. The four controls with this option are listed under **Post-Processing** below.

## Spot Lights

The **Spots** tab is for focused, directional lighting.

Create a Spot Light and place it where you need it. Change its direction, color and brightness to highlight a subject, add a rim light or bring attention to a part of the environment.

Depending on the control, you can adjust:

* **Position and rotation** — place and aim the light.
* **Color** — choose the light's tint.
* **Intensity** — control its brightness.
* **Beam angle** — make the light cone narrower or wider.
* **Spot Softness** and **Spot Roundness** — shape the transition and appearance of the cone.
* **Specular** — control how strongly the light affects shiny surfaces.
* **Source size, distance and fade** — experiment with the light's shape and reach.
* **Volumetric settings** — experiment with how the light interacts with atmospheric effects.

Different materials and locations react differently. A light that looks subtle on a wall may look much stronger on a reflective surface.

## Point Lights

The **Points** tab is for lighting an area from a single position in all directions.

Point Lights work well for filling dark corners, adding a small colored accent or simulating a nearby light source.

You can experiment with:

* **Position**
* **Color**
* **Intensity**
* **Radius and distance-related settings**

Try combining a broad Point Light with a more focused Spot Light. Often, a small change is enough to add depth without overpowering the original scene.

## Post-Processing (PP)

The **PP** tab adjusts the overall look of the image. These are creative controls rather than fixed recipes.

### Bloom

* **Intensity** — changes the strength of the glow around bright areas.
* **Threshold** — changes which bright areas contribute to bloom.
* **Scatter** — changes how broadly the glow spreads.
* **Lens Dirt** — adjusts the lens-dirt contribution to bright highlights.

**Bloom Intensity** and **Bloom Scatter** each have an **Override** checkbox to the right of their slider.

### Image Effects

* **Radial Blur** — adds or adjusts radial blur.
* **Brightness** — lightens or darkens the image.
* **Saturation** — changes color intensity.
* **Vignette** — darkens or emphasizes the edges of the frame.
* **Film Grain** — adds or adjusts grain.
* **Camera Lens Distortion** — changes the lens distortion effect.

**Vignette** and **Film Grain** also have an **Override** checkbox to the right of their slider.

These are the **only four Override checkboxes** in the PP tab.

### Atmosphere

The PP tab also includes:

* **Scatter Blur**
* **Scatter Direction 1**
* **Scatter Direction 2**

These settings can produce different results depending on the scene and its atmospheric effects. Try small adjustments and compare the image.

## Level of Detail (LOD)

The **LOD** tab lets you experiment with how objects and vegetation are displayed at different distances.

It currently includes:

* **LOD:Target Size** — affects the level-of-detail reference size.
* **Hierarchy LOD:Distance scale** — adjusts distance-based hierarchy detail behavior.
* **LOD: Lod Menu Multiplier** — adjusts the LOD multiplier.

LOD changes can affect vegetation and distant objects, but they should not be mistaken for a dedicated **shadow-distance** control. The game's shadows may use their own rules.

Because these settings can be demanding, change one value at a time and watch the result in your current scene.

## A Few Creative Ideas

### Shape a Portrait

Use a Spot Light to gently highlight the subject. Adjust beam angle and softness until the light blends into the environment. Add a small amount of bloom if the highlights need extra presence.

### Add Color to a Dark Scene

Place a Point Light behind or beside the subject. Try a contrasting color, then use the PP saturation control to fine-tune the overall palette.

### Work With Vegetation and Distance

In the LOD tab, adjust Target Size or Hierarchy Distance Scale and compare how distant foliage and objects appear. Results vary by location.

### Finish the Frame

After positioning your lights, use the PP tab for small changes to brightness, bloom, vignette or film grain. The goal is to support the image rather than change everything at once.

## Interface

ResonantTool uses an in-game **ImGui interface** designed to keep light creation and visual settings together.

Use **F11** to open or close the menu. The active adjustments are intended to be used while framing screenshots with the interface hidden.

Sliders let you make quick adjustments, while supported controls also allow finer numeric entry.

## Installation

ResonantTool includes **`ResonantTool.dll`** and an **injector EXE**.

1. Start **CONTROL Resonant**.
2. Load your save and enter gameplay.
3. Use the included injector EXE to load `ResonantTool.dll` into the game.
4. Press **F11** to open the menu.

A public download link will be added here when the release file is available.

## Screenshots

**Screenshots coming soon.** The in-game interface and examples will be added once the final images are available.

## Notes

ResonantTool changes game systems at runtime and is primarily intended for virtual photography and cinematic experimentation.

Some settings depend on the location, materials, lighting conditions or current game state. The same settings can look quite different from one scene to another.

There is no single perfect lighting setup. **Try things, compare the results and build the look you want.**
