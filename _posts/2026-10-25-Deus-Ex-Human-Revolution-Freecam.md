---
layout: post
title: "Deus Ex: Human Revolution — Director's Cut Freecam"
date: 2026-10-25 10:00:00 +0100
description: "Free camera, gamepad controls, Gold Filter restoration, experimental graphics options and hotsampling for Deus Ex: Human Revolution — Director's Cut."
tags: Screenshooting
---

**DXHRDC Freecam v0.29** is a camera tool for virtual photography in **Deus Ex: Human Revolution — Director's Cut**. It provides free movement, pitch, yaw, roll and field-of-view controls, a movable camera while the game is frozen, HUD hiding, an integrated Gold Filter and hotsampling.

This guide covers the **Steam Director's Cut executable 2.0.66.0 (build 235963)**. The in-game interface and hotsampling use **DirectX 11**. Hotsampling requires **windowed mode**.

## Getting started

1. Extract the camera release into a folder of your choice. Keep `DXHRDCFreecamInjector.exe` and `DXHRDCFreecam.dll` together.
2. Start the game through Steam, enable DirectX 11 and load a save into gameplay.
3. Run `DXHRDCFreecamInjector.exe`. Injection is automatic. The success message closes after three seconds.
4. Return to the game. Press **End** to show or hide the interface, and **Insert** to enable or release the free camera.
5. Close the interface with **End** before moving the camera.

The injector checks the supported game executable. Inject once per game session. Closing the injector leaves the camera running.

The interface has four tabs: **Camera**, **Gold Filter**, **Hotsampling** and **Controls**. **End** is the interface shortcut; **F1** remains available to the game.

## Camera

| Option | What it does |
|---|---|
| **Free camera** | Enables or releases direct control of the gameplay camera. |
| **Freeze game** | Freezes the simulation while leaving the free camera movable. |
| **Hide HUD** | Hides the gameplay HUD and interactable-object highlights. Showing the HUD restores the previous highlight setting. |
| **Lock camera movement** | Holds the current camera pose by disabling movement input. |
| **Keep running without focus** | Keeps the game processing when you switch to another window. Enabled on injection. |
| **Position XYZ** | Changes the camera's position. |
| **Pitch / Yaw / Roll** | Adjusts the vertical look angle, horizontal look angle and camera tilt. |
| **FOV vertical** | Changes the vertical field of view in degrees. |
| **Reset roll** | Returns the camera tilt to zero. |
| **Move speed** | Changes translation speed. |
| **Rotation speed (deg/s)** | Changes keyboard and stick rotation speed. |
| **Restore game** | Releases the camera, restores game time and the HUD, unlocks camera movement, resets object distance, disables enhanced shadows and requests the original window resolution. |

**Restore game** is also available through **Ctrl + Insert**. The background-focus option and Gold Filter settings keep their current values; adjust them separately in their tabs.

Release the camera before loading another save or entering a cinematic. Camera modes outside the supported gameplay layouts suspend the override.

### Experimental graphics options

**Object distance (experimental)** changes drawable visibility ranges from **×1 to ×16**. This can help with distant objects, but it is not a guarantee of higher-detail meshes or additional streaming.

**2x shadow resolution (experimental)** increases the supported DX11 shadow atlas from **4096 × 3072** to **8192 × 6144**. It doubles each dimension, giving four times as many shadow pixels. The larger atlas uses approximately **96 MiB of additional VRAM**, which can remain allocated after the option is switched off until cleanup.

The shadow option starts disabled. Its visible benefit and performance cost depend on the scene. It affects the identified shadow atlas rather than every shadow or lighting effect in the game. Switching it off, or using **Restore game**, returns to the original shadow bindings.

## Keyboard and mouse

Use **Num Lock ON** for the numpad controls.

| Action | Key |
|---|---|
| Show / hide the interface | **End** |
| Enable / release freecam | **Insert** |
| Restore game and original resolution | **Ctrl + Insert** |
| Forward / backward | **Numpad 8 / 5** |
| Strafe left / right | **Numpad 4 / 6** |
| Move down / up | **Numpad 7 / 9** |
| Look | **Arrow keys** or **mouse** |
| Roll left / right | **Numpad 1 / 3** |
| Reset roll | **Numpad 2** |
| Increase / decrease vertical FOV | **Numpad + / −** |
| Fast / slow movement | **Shift / Ctrl** |
| Toggle HUD and object highlights | **Delete** |
| Freeze / unfreeze the game | **Numpad 0** |
| Lock / unlock camera movement | **Numpad decimal** |

## Xbox / XInput gamepad

The first connected XInput controller is used. Close the interface before flying the camera. The game's controller input is neutralized while freecam is active so that composing a shot does not also move Jensen.

| Action | Control |
|---|---|
| Enable / release freecam | **Back + Start** |
| Move | **Left stick** |
| Look | **Right stick** |
| Move up / down | **RT / LT** |
| Roll right / left | **RB / LB** |
| Increase / decrease FOV | **D-pad up / down** |
| Halve / double movement speed | **D-pad left / right** |
| Toggle HUD and highlights | **X** |
| Freeze / unfreeze the game | **Y** |
| Reset roll | **B** |
| Fast / slow movement | **Left-stick click / right-stick click** |

PlayStation controllers need an XInput translation layer, such as Steam Input. Stick and trigger deadzones help prevent drift. The **Controls** tab also displays the physical input values for checking controller reception.

## Gold Filter

The **Gold Filter** tab integrates the restoration effects from **[DXHRDC-GFX by Silent / CookiePLMonster](https://github.com/CookiePLMonster/DXHRDC-GFX)**. Its original color grading, bloom and lighting work is credited below.

| Option | Available adjustments |
|---|---|
| **Enable gold color grading** | Enables or disables the integrated color-grading effect. |
| **Bloom** | Selects **Director's Cut** or **Human Revolution** bloom. |
| **Lighting** | Selects **Director's Cut**, **Director's Cut (fixed)** or **Human Revolution** lighting. |
| **Color preset** | Selects one of three color-grading presets. |
| **Intensity** | Changes color-grading strength. |
| **Saturation** | Changes color saturation. |
| **Temperature threshold** | Adjusts how the grading separates temperature ranges. |
| **Cold / Moderate / Warm** | Changes the RGB colors used by the three grading ranges. |
| **Vignette** | Edits the four vignette values. **Reset vignette** restores its defaults. |

Open **Advanced color grading** to access intensity, saturation, temperature, the three color ranges and vignette.

Changes save automatically in `DXHRDCFreecam-GFX.ini` beside the camera DLL. Keep that file when moving or updating the camera folder.

The integrated controls do not require a separate installation of `DXHRDC-GFX.asi`. Leave that separate ASI disabled when using these integrated effects to avoid applying the same restoration twice. ReShade can still provide its own additional effects.

## Hotsampling

Hotsampling enlarges the actual game window and render resolution beyond the desktop size. Part of the window can extend outside the monitor; the screenshot still captures the complete rendered image. The high-resolution preview is not automatically scaled down to fit the screen.

1. Run the game in **windowed DirectX 11 mode**.
2. Open **Hotsampling** and use **2560 × 1440**, **3840 × 2160**, or enter a custom **Width / height** and click **Apply resolution**.
3. Wait until **Rendered resolution** shows the requested dimensions.
4. Close the interface with **End** and capture with your configured ReShade screenshot key. In the tested setup, this is **Print Screen**.
5. Reopen the interface and click **Restore resolution** to return to the window size and position recorded at injection.

**1440p and 4K have been tested**, including ReShade captures before and after its effects at **3840 × 2160**. Higher resolutions increase memory use; sizes above 4K have not received the same validation. Restore the original size before changing display mode or loading another area.

### Saved resolutions

Successfully applied sizes are saved automatically in `DXHRDCFreecam-Hotsampling.ini` beside the DLL. The **Saved resolutions** list keeps up to **16 unique sizes**, with the most recent first.

Click an entry to apply it again. The last saved size fills the width and height fields on the next injection. Failed requests and **Restore resolution** do not add entries. Keep the INI when moving or updating the camera folder.

Version 0.29 uses ReShade for the capture workflow; the Hotsampling tab no longer contains a **Save PNG** section.

## Credits

- **Camera tool and integration:** AnticOwl / Olivier César.
- **Gold Filter restoration:** **Adrian Zdanowicz (Silent / CookiePLMonster)**, author of **[DXHRDC-GFX](https://github.com/CookiePLMonster/DXHRDC-GFX)**. The integrated color grading, bloom and lighting effects are adapted from that project under its **[MIT license](https://github.com/CookiePLMonster/DXHRDC-GFX/blob/77ac54d786b6e15dde7b3b2cb6d0812beded2d53/LICENSE)**. Original copyright: **© 2020–2021 Adrian Zdanowicz (Silent)**. The camera's combined interface and injection path are adaptations; the original restoration work belongs to Silent.
- **Interface:** **[Dear ImGui](https://github.com/ocornut/imgui)** by Omar Cornut and contributors, under the MIT license.
- **Hooking library:** **[MinHook](https://github.com/TsudaKageyu/minhook)** by Tsuda Kageyu and contributors, under its BSD-style license.

The camera package includes `DXHRDC-GFX-LICENSE.txt` with the Gold Filter's original license notice.

