---
layout: post
title: "CONTROL Toolkit — In-Game Photo Mode Tools"
date: 2026-10-23 10:00:00 +0200
tags: Screenshooting
---

**CONTROL Toolkit** is an in-game utility for the original **CONTROL** (DirectX 12), **exclusively intended for use in the game's Photo Mode** for virtual photography and cinematic screenshots. It is not designed for normal gameplay. It brings camera controls, a camera path, lighting, post-processing and resolution adjustments together in one interface.

The current tested baseline is **v0.4j**. The version number is displayed in the title bar, so you can easily see which build is running.

## Main Features

* **Camera & Camera Path** — frame shots and set up camera movements.
* **Spot Lights** — work with the toolkit's native Spot Light functionality.
* **Post Process** — adjust bloom and other image effects.
* **Hotsampling** — switch to custom capture resolutions, revisit previously used resolutions and restore your original window size.
* **Configuration** — adjust supported key bindings and Photo Mode settings.
* **IGCSDOF integration** — use the existing connector features where applicable.

## Getting Started

1. **Unzip the CONTROL Toolkit ZIP archive into a folder of your choice.**
2. If you are using the source package, run `Build-Release.cmd` first to compile `ControlToolkit.dll` and its injector.
3. **Start CONTROL in DirectX 12 mode** and load your game.
4. Run `Inject-Control.cmd` to load the toolkit into `Control_DX12.exe`.
5. **Enter the game's Photo Mode.** Open the toolkit interface and adjust your shot.

The toolkit is **exclusively for Photo Mode**. Do not use it for regular gameplay.

The package includes an injector; Cheat Engine and a separate injector are not required.

> **Source package note:** The currently available ZIP contains source code and build scripts, not precompiled executables. Compiling it requires a working Windows C++ build environment.

## Camera & Camera Path

Use the camera controls to compose a frame, then work with the **Camera Path** controls when you want a moving shot instead of a single still. The toolkit includes configurable shortcuts, so check the **Configuration** tab for the keys assigned to your camera and path actions.

## Lights

The existing lighting controls include **native Spot Light creation**. Spots are directional: use them to highlight a subject or add an accent to a scene.

### Point / Omni Lights — planned

**Point (Omni) Light creation is not part of the confirmed v0.4j feature set yet.** Work is planned to add a native light that illuminates in all directions from a chosen position, ideally with position, color, intensity and radius controls. This section will be updated only once the function is implemented and tested in the original CONTROL game.

## Post Process

The **Post Process** tab groups the image adjustments that were previously spread across the interface. Bloom controls are clearly labeled:

* **Bloom Scale X** and **Bloom Scale Y**
* **Bloom Intensity**
* **Bloom Threshold**
* **Bloom Lens Dirt**
* **Bloom Scatter**

You can also adjust **Global Exposure**, **Radial Blur** and **Vignette** from this tab. Change one setting at a time and compare the effect in your scene.

## Hotsampling

The **Hotsampling** tab brings resolution management into the toolkit, reducing the need to use a separate window-resizing utility such as SRWE.

* Pick a custom resolution and apply it.
* Reuse resolutions from the clickable history.
* Restore the original window dimensions.
* Keep **Allow Window Resize** and **Allow Hotsampling** together in this tab.
* Keep **Force EXITSIZEMOVE after window resize** enabled, so CONTROL receives the resize-complete notification.

For best results, verify that the game's **Render Resolution** follows the resized window, both when moving to a higher resolution and when restoring the original one. The v0.4j baseline was user-tested with the **Native** rendering mode; results may differ with upscaling settings.

## Configuration

The **Configuration** tab provides the tool's keyboard customization options and **Photo Mode — 8 to 100**, enabled by default.

## Tips for Screenshots

If the image looks wrong after a resolution change, compare the window resolution and the game's render resolution. In a normal native hotsampling workflow, they should match. Return to your usual resolution using **Restore** when you finish capturing.

As with any runtime game modification, keep a backup of your working build and test new versions before replacing it.

## Notes

This documentation describes **CONTROL 1**, not **CONTROL Resonant**. The two toolkits are separate projects.

Point / Omni Light support remains **under investigation** and will be added to this page once a working in-game implementation is confirmed.
