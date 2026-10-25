---
layout: post
title: "Deus Ex: Human Revolution — Director's Cut: Screenshooting Guide"
date: 2026-10-25 10:00:00 +0100
description: "Freeze a scene, compose with the free camera, work with the Gold Filter and take high-resolution screenshots in Deus Ex: Human Revolution — Director's Cut."
tags: Screenshooting
---

**Deus Ex: Human Revolution — Director's Cut** offers plenty to photograph: its architecture, characters, lighting and atmosphere. **DXHRDC Freecam** lets you leave the gameplay viewpoint, hold a moment and compose your own image.

This guide uses **DXHRDC Freecam v0.29** with the **Steam Director's Cut** and **DirectX 11**. For high-resolution captures through hotsampling, use **windowed mode**.

## Get the camera ready

1. Launch the game and load your save into gameplay.
2. Run **DXHRDCFreecamInjector.exe** from your extracted camera folder. Keep the camera DLL beside it. The confirmation closes after three seconds.
3. Return to the game. **End** opens or closes the camera interface.
4. Press **Insert** to activate the free camera.

Close the interface with **End** before flying the camera. You can reopen it whenever you want to adjust an option. **F1** remains a game key.

## Take your first shot

### 1. Hold the moment

Find the scene you want to photograph, then press **Numpad 0** to freeze it. Characters and the simulation stop, while the free camera remains movable.

If you need the scene to advance, press **Numpad 0** again. Freeze it once more when the moment is right.

### 2. Find your framing

Use **Numpad 8 / 5** to move forward and backward, **4 / 6** to move sideways and **7 / 9** to move down and up. Look around with the **mouse** or **arrow keys**.

Hold **Shift** to cover distance quickly, or **Ctrl** for smaller adjustments. The **Move speed** and **Rotation speed** sliders in the Camera tab let you set a comfortable pace.

Use **Numpad + / −** to change the field of view. Moving the camera changes your viewpoint; changing FOV changes how much of the scene fits into the frame. You can combine the two to work on your composition.

For a tilted frame, use **Numpad 1 / 3** to roll left and right. **Numpad 2** brings the roll back to zero.

**Num Lock must be ON** for these controls.

### 3. Clear the frame

Press **Delete** to hide the gameplay HUD and the yellow highlights around interactable objects. Press it again to bring them back.

Once you have your composition, **Numpad decimal** locks camera movement. This helps you keep the pose while working on the image. Press it again when you want to move.

### 4. Work on the look

Open the interface with **End**. The **Gold Filter** tab lets you work with the restored Human Revolution look, while ReShade can provide your additional effects.

The filter is optional: experiment with its controls and keep the result that suits your shot. The available adjustments are described below.

### 5. Capture

Close the camera interface and any ReShade panel before taking the screenshot. Use your configured **ReShade screenshot key** to include its effects. In the tested setup, that key is **Print Screen**.

For a larger image, follow the **Hotsampling** steps below before capturing.

## Compose with a gamepad

An **Xbox / XInput controller** can move the camera while the game is frozen. Close the interface before using the sticks. While freecam is active, controller movement controls the camera without also moving Jensen.

| Action | Control |
|---|---|
| Enable / release freecam | **Back + Start** |
| Move | **Left stick** |
| Look | **Right stick** |
| Move up / down | **RT / LT** |
| Roll right / left | **RB / LB** |
| Increase / decrease FOV | **D-pad up / down** |
| Halve / double movement speed | **D-pad left / right** |
| Hide / show the HUD and highlights | **X** |
| Freeze / unfreeze the scene | **Y** |
| Reset roll | **B** |
| Fast / slow movement | **Left-stick click / right-stick click** |

PlayStation controllers need an XInput translation layer, such as Steam Input.

## Gold Filter: shape the image

The **Gold Filter** tab brings together restoration effects from **[DXHRDC-GFX by Silent / CookiePLMonster](https://github.com/CookiePLMonster/DXHRDC-GFX)**.

### Choose the overall look

- **Enable gold color grading** switches the grading on or off.
- **Color preset** offers three starting looks.
- **Bloom** switches between **Director's Cut** and **Human Revolution** bloom. Compare how bright areas and their glow appear in your scene.
- **Lighting** offers **Director's Cut**, **Director's Cut (fixed)** and **Human Revolution** styles. Their visible effect depends on the location and lighting in the shot.

### Fine-tune the grading

Open **Advanced color grading** for:

| Adjustment | Use it to… |
|---|---|
| **Intensity** | Change the strength of the grading. |
| **Saturation** | Adjust the amount of color. |
| **Temperature threshold** | Change how the grading separates its temperature ranges. |
| **Cold / Moderate / Warm** | Edit the colors used by those three ranges. |
| **Vignette** | Adjust the vignette. **Reset vignette** returns it to its defaults. |

Your Gold Filter changes save automatically for later sessions.

The restoration is already integrated into this camera. Leave the separate **DXHRDC-GFX ASI** disabled when using these controls, so the same effects are not applied twice.

## Distance and shadows

The Camera tab also contains two **experimental** options that may help a particular shot:

- **Object distance** extends the visibility range of objects, from **×1 to ×16**. Check the background of your composition when changing it. It does not guarantee higher-detail models.
- **2x shadow resolution** increases the resolution of the supported shadow atlas. It may help shadow detail in some scenes, but its benefit varies. It starts switched off and uses additional GPU memory when enabled.

Both options can affect performance. Compare the result in the scene you are photographing; neither is a general lighting overhaul. **Restore game** returns these options to their original state.

## Hotsampling: capture a larger image

Hotsampling makes the game render at a larger window size. The window can extend beyond the monitor, so you may only see part of the image on screen. The screenshot still contains the **complete rendered frame**.

Compose your image at your normal window size first, then:

1. Keep the scene frozen and open **End → Hotsampling**.
2. Select **2560 × 1440** or **3840 × 2160**. You can also enter a custom **Width / height** and click **Apply resolution**.
3. Wait until **Rendered resolution** shows the size you requested.
4. Close the interface with **End** and take your **ReShade screenshot**.
5. Reopen the interface and click **Restore resolution** to return to your original window size and position.

Use **windowed DirectX 11 mode** for this. **1440p and 4K have been tested**, including complete **3840 × 2160** ReShade captures with its effects. Larger images need more memory; sizes above 4K have not received the same validation.

Restore the original resolution before changing display mode or loading another area.

### Reuse a resolution

The **Saved resolutions** list remembers successfully applied sizes automatically. It keeps up to **16 different resolutions**, with the most recent first.

Click a saved resolution to apply it again. Your last saved size also fills the width and height fields the next time you use the camera. Failed changes and **Restore resolution** do not add entries.

For screenshots, use your ReShade capture key; there is no **Save PNG** section in this tab.

## Return to gameplay

Press **Ctrl + Insert**, or choose **Restore game** in the Camera tab. This releases the free camera, restores time and the HUD, unlocks camera movement, resets object distance and enhanced shadows, and returns the window to its original resolution.

Your **Gold Filter** choices stay in place. Change them separately if you want a different look for gameplay.

**Keep running without focus** is enabled when the camera is injected. It keeps the game processing when you switch windows and stays enabled after Restore game. You can turn it off in the Camera tab.

Release freecam before loading another save or entering a cinematic.

## Keyboard quick reference

With **Num Lock ON**:

| Action | Key |
|---|---|
| Show / hide the interface | **End** |
| Enable / release freecam | **Insert** |
| Restore game and original resolution | **Ctrl + Insert** |
| Forward / backward | **Numpad 8 / 5** |
| Left / right | **Numpad 4 / 6** |
| Down / up | **Numpad 7 / 9** |
| Look | **Mouse** or **arrow keys** |
| Roll left / right | **Numpad 1 / 3** |
| Reset roll | **Numpad 2** |
| Increase / decrease FOV | **Numpad + / −** |
| Fast / slow movement | **Shift / Ctrl** |
| Hide / show HUD and highlights | **Delete** |
| Freeze / unfreeze | **Numpad 0** |
| Lock / unlock camera movement | **Numpad decimal** |

## Credits

- **Camera tool and integration:** AnticOwl / Olivier César.
- **Gold Filter restoration:** **Adrian Zdanowicz (Silent / CookiePLMonster)**, creator of **[DXHRDC-GFX](https://github.com/CookiePLMonster/DXHRDC-GFX)**. The integrated color grading, bloom and lighting effects are adapted from his work under the **[MIT license](https://github.com/CookiePLMonster/DXHRDC-GFX/blob/77ac54d786b6e15dde7b3b2cb6d0812beded2d53/LICENSE)**. Original copyright: **© 2020–2021 Adrian Zdanowicz (Silent)**. Full credit for the original restoration effects belongs to Silent.
- **Interface:** **[Dear ImGui](https://github.com/ocornut/imgui)** by Omar Cornut and contributors.
- **Hooking library:** **[MinHook](https://github.com/TsudaKageyu/minhook)** by Tsuda Kageyu and contributors.

