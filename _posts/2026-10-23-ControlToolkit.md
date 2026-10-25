---
layout: post
title: "CONTROL Toolkit — In-Game Photo Mode Tools"
date: 2026-10-23 10:00:00 +0200
image: CONTROLTOOLKIT_POST.jpg
tags: Screenshooting
---

**CONTROL Toolkit** is a free in-game utility for virtual photography in the original **CONTROL** (DirectX 12). It brings Photo Mode camera controls, camera paths, lights, post-processing and high-resolution capture into one interface. It is intended for Photo Mode, not regular gameplay.

[Download the compiled v0.5c package](https://github.com/AnticOwl/CONTROL_Toolkit/blob/main/releases/ControlToolkit_0.5c.zip) · [Browse the source code](https://github.com/AnticOwl/CONTROL_Toolkit/tree/main/source/v0.5c)

## Install the toolkit

1. Download and extract the compiled ZIP.
2. Start CONTROL in **DirectX 12** and load into the game.
3. Run `ControlToolkitInjector.exe` from the extracted folder. Keep `ControlToolkit.dll` beside it.
4. Press **F10** to show or hide the toolkit.

Inject once per game session.

## About IGCSConnector — Frans' Depth of Field

The Frans DOF workflow uses the **IGCS Connector** ReShade add-on together with **IGCS Relay**. The Relay add-on is included in the toolkit ZIP.

1. Copy `IGCSRelay.addon64` from the toolkit ZIP into the same ReShade add-ons folder as `IgcsConnector.addon64`.
2. In ReShade, make sure **IGCS Connector** and **IGCSRelay** are enabled.
3. In the toolkit's **IGCSDOF** tab, enable the named-pipe provider.
4. Enter Photo Mode and move the camera. Then open **IGCS Connector → Depth of Field control** in ReShade and start the DOF session.

Keep the Relay beside the Connector in ReShade's add-ons folder; it does not go beside the Toolkit DLL or injector.

## Camera and Camera Path

Use the Photo Mode camera to compose a still image. The **Camera Path** tab lets you add and play a sequence of camera positions for a moving shot. Camera path files are saved beside the Toolkit DLL.

## Lights

The Toolkit supports both **Spot** and **Point / Omni** lights.

- A **Spot** light shines in a chosen direction, which is useful for lighting a subject or adding an accent.
- A **Point / Omni** light shines in every direction from its position. Create one, place it with the camera or adjust its position, then set its color, intensity and lighting range.
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
