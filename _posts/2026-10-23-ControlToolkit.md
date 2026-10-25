---
layout: post
title: "CONTROL Toolkit v0.5c — In-Game Photo Mode Tools"
date: 2026-10-23 10:00:00 +0200
image: CONTROLTOOLKIT_POST.jpg
tags: Screenshooting
---

**This guide covers CONTROL Toolkit v0.5c** for the original **CONTROL** (DirectX 12). It brings Photo Mode camera controls, camera paths, lights, post-processing and high-resolution capture together in one interface. It is intended for Photo Mode, not regular gameplay.

[Download the compiled v0.5c package](https://github.com/AnticOwl/CONTROL_Toolkit/blob/main/releases/ControlToolkit_0.5c.zip) · [Browse the source code](https://github.com/AnticOwl/CONTROL_Toolkit/tree/main/source/v0.5c)

## Install the toolkit

1. Download and extract the compiled ZIP.
2. Start CONTROL in **DirectX 12** and load into the game.
3. Run `ControlToolkitInjector.exe` from the extracted folder. Keep `ControlToolkit.dll` beside it.
4. Press **F10** to show or hide the toolkit.

Inject once per game session.

## About IGCSConnector

For Frans' DOF in v0.5c, copy `IGCSRelay.addon64` from the Toolkit ZIP into the ReShade add-ons folder that contains `IgcsConnector.addon64`. That's all you need to do.

## Camera and Camera Path

Use the Photo Mode camera to compose a still image. The **Camera Path** tab lets you add and play a sequence of camera positions for a moving shot. Camera path files are saved beside the Toolkit DLL.

## Lights

The Toolkit supports both **Spot** and **Point / Omni** lights.

- A **Spot** light shines in a chosen direction, which is useful for lighting a subject or adding an accent.
- A **Point / Omni** light shines in every direction from its position. Choose **Point / Omni**, create a light, then set its position, color, intensity and range.
- Select a light from the list to edit it. **Enabled** turns the selected light on or off.

For Point / Omni lights, **Source Radius** changes the size of the light source; **Range** controls how far the light reaches.

## Post Process

The **Post Process** tab includes Bloom Scale X/Y, Intensity, Threshold, Lens Dirt and Scatter, as well as Global Exposure, Radial Blur and Vignette.

## Hotsampling

Choose a window size in the **Hotsampling** tab, apply it, and use **Restore original** to return to the original size. The Toolkit preserves the game's selected internal render scale when resizing, including reduced DLSS and supersampling ratios.

## Configuration

Use **Configuration** to change supported keyboard shortcuts and Photo Mode options. **F10** shows or hides the Toolkit by default.

## Compatibility

This guide is for the original **CONTROL** running in **DirectX 12**. It does not describe CONTROL Resonant, which is a separate game and project.
