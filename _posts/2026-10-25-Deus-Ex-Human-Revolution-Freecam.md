---
layout: post
title: "Deus Ex: Human Revolution — Director's Cut"
date: 2026-10-25 10:00:00 +0100
tags: Screenshooting
---

You play Adam Jensen, an ex-SWAT specialist who's been handpicked to oversee the defensive needs of one of America's most experimental biotechnology firms. When a black ops team breaks in and kills the very scientists you were hired to protect, everything you thought you knew about your job changes.

## Required

* Deus Ex: Human Revolution — Director's Cut (Steam version).
* [DXHRDC Freecam v0.29](https://anticowl.github.io/files/DXHRDCFreecamInjector.zip)
* **DirectX 11** enabled in the game settings.

## Optional

* [ReShade](https://reshade.me/) for additional effects and screenshot capture.
* An Xbox / XInput controller for moving the camera.

## Installation

1. Launch the game and load your save into gameplay.
2. Run **DXHRDCFreecamInjector.exe** from your extracted camera folder. Keep the camera DLL beside it. The confirmation closes after three seconds.
3. Return to the game. **End** opens or closes the camera interface.
4. Press **Insert** to activate the free camera.

Close the interface with **End** before flying the camera. You can reopen it whenever you want to adjust an option. **F1** remains a game key.

## Controls

<style>
.table_component {
    overflow: auto;
    width: 100%;
}

.table_component table {
    border: 1px solid #dededf;
    height: 100%;
    width: 100%;
    table-layout: fixed;
    border-collapse: collapse;
    border-spacing: 1px;
    text-align: left;
}

.table_component caption {
    caption-side: top;
    text-align: left;
}

.table_component th {
    border: 1px solid #dededf;
    background-color: #eceff1;
    color: #000000;
    padding: 5px;
}

.table_component td {
    border: 1px solid #dededf;
    background-color: #ffffff;
    color: #000000;
    padding: 5px;
}
</style>

With **Num Lock ON**:

<div class="table_component" role="region" tabindex="0">
<table>
<thead><tr><th>Action</th><th>Key</th></tr></thead>
<tbody>
<tr><td>Show / hide the interface</td><td><strong>End</strong></td></tr>
<tr><td>Enable / release freecam</td><td><strong>Insert</strong></td></tr>
<tr><td>Restore game and original resolution</td><td><strong>Ctrl + Insert</strong></td></tr>
<tr><td>Forward / backward</td><td><strong>Numpad 8 / 5</strong></td></tr>
<tr><td>Left / right</td><td><strong>Numpad 4 / 6</strong></td></tr>
<tr><td>Down / up</td><td><strong>Numpad 7 / 9</strong></td></tr>
<tr><td>Look</td><td><strong>Mouse</strong> or <strong>arrow keys</strong></td></tr>
<tr><td>Roll left / right</td><td><strong>Numpad 1 / 3</strong></td></tr>
<tr><td>Reset roll</td><td><strong>Numpad 2</strong></td></tr>
<tr><td>Increase / decrease FOV</td><td><strong>Numpad + / −</strong></td></tr>
<tr><td>Fast / slow movement</td><td><strong>Shift / Ctrl</strong></td></tr>
<tr><td>Hide / show HUD and highlights</td><td><strong>Delete</strong></td></tr>
<tr><td>Freeze / unfreeze</td><td><strong>Numpad 0</strong></td></tr>
<tr><td>Lock / unlock camera movement</td><td><strong>Numpad decimal</strong></td></tr>
</tbody>
</table>
</div>

## The Tool

### Camera

#### Freeze the scene

Find the scene you want to photograph, then press **Numpad 0** to freeze it. Characters and the simulation stop, while the free camera remains movable.

If you need the scene to advance, press **Numpad 0** again. Freeze it once more when the moment is right.

#### Frame the shot

Use **Numpad 8 / 5** to move forward and backward, **4 / 6** to move sideways and **7 / 9** to move down and up. Look around with the **mouse** or **arrow keys**.

Hold **Shift** to cover distance quickly, or **Ctrl** for smaller adjustments. The **Move speed** and **Rotation speed** sliders in the Camera tab let you set a comfortable pace.

Use **Numpad + / −** to change the field of view. Moving the camera changes your viewpoint; changing FOV changes how much of the scene fits into the frame. You can combine the two to work on your composition.

For a tilted frame, use **Numpad 1 / 3** to roll left and right. **Numpad 2** brings the roll back to zero.

**Num Lock must be ON** for these controls.

#### Hide the HUD

Press **Delete** to hide the gameplay HUD and the yellow highlights around interactable objects. Press it again to bring them back.

Once you have your composition, **Numpad decimal** locks camera movement. This helps you keep the pose while working on the image. Press it again when you want to move.

#### Adjust the look

Open the interface with **End**. The **Gold Filter** tab lets you work with the restored Human Revolution look, while ReShade can provide your additional effects.

The filter is optional: experiment with its controls and keep the result that suits your shot. The available adjustments are described below.

#### Take a screenshot

Close the camera interface and any ReShade panel before taking the screenshot. Use your configured **ReShade screenshot key** to include its effects. In the tested setup, that key is **Print Screen**.

For a larger image, follow the **Hotsampling** steps below before capturing.

### Gamepad

An **Xbox / XInput controller** can move the camera while the game is frozen. Close the interface before using the sticks. While freecam is active, controller movement controls the camera without also moving Jensen.

<div class="table_component" role="region" tabindex="0">
<table>
<thead><tr><th>Action</th><th>Control</th></tr></thead>
<tbody>
<tr><td>Enable / release freecam</td><td><strong>Back + Start</strong></td></tr>
<tr><td>Move</td><td><strong>Left stick</strong></td></tr>
<tr><td>Look</td><td><strong>Right stick</strong></td></tr>
<tr><td>Move up / down</td><td><strong>RT / LT</strong></td></tr>
<tr><td>Roll right / left</td><td><strong>RB / LB</strong></td></tr>
<tr><td>Increase / decrease FOV</td><td><strong>D-pad up / down</strong></td></tr>
<tr><td>Halve / double movement speed</td><td><strong>D-pad left / right</strong></td></tr>
<tr><td>Hide / show the HUD and highlights</td><td><strong>X</strong></td></tr>
<tr><td>Freeze / unfreeze the scene</td><td><strong>Y</strong></td></tr>
<tr><td>Reset roll</td><td><strong>B</strong></td></tr>
<tr><td>Fast / slow movement</td><td><strong>Left-stick click / right-stick click</strong></td></tr>
</tbody>
</table>
</div>

PlayStation controllers need an XInput translation layer, such as Steam Input.

### Gold Filter

The **Gold Filter** tab brings together restoration effects from **[DXHRDC-GFX by Silent / CookiePLMonster](https://github.com/CookiePLMonster/DXHRDC-GFX)**.

#### Choose the overall look

- **Enable gold color grading** switches the grading on or off.
- **Color preset** offers three starting looks.
- **Bloom** switches between **Director's Cut** and **Human Revolution** bloom. Compare how bright areas and their glow appear in your scene.
- **Lighting** offers **Director's Cut**, **Director's Cut (fixed)** and **Human Revolution** styles. Their visible effect depends on the location and lighting in the shot.

#### Fine-tune the grading

Open **Advanced color grading** for:

<div class="table_component" role="region" tabindex="0">
<table>
<thead><tr><th>Adjustment</th><th>Use it to…</th></tr></thead>
<tbody>
<tr><td><strong>Intensity</strong></td><td>Change the strength of the grading.</td></tr>
<tr><td><strong>Saturation</strong></td><td>Adjust the amount of color.</td></tr>
<tr><td><strong>Temperature threshold</strong></td><td>Change how the grading separates its temperature ranges.</td></tr>
<tr><td><strong>Cold / Moderate / Warm</strong></td><td>Edit the colors used by those three ranges.</td></tr>
<tr><td><strong>Vignette</strong></td><td>Adjust the vignette. <strong>Reset vignette</strong> returns it to its defaults.</td></tr>
</tbody>
</table>
</div>

Your Gold Filter changes save automatically for later sessions.

The restoration is already integrated into this camera. Leave the separate **DXHRDC-GFX ASI** disabled when using these controls, so the same effects are not applied twice.

### Distance and shadows

The Camera tab also contains two **experimental** options that may help a particular shot:

- **Object distance** extends the visibility range of objects, from **×1 to ×16**. Check the background of your composition when changing it. It does not guarantee higher-detail models.
- **2x shadow resolution** increases the resolution of the supported shadow atlas. It may help shadow detail in some scenes, but its benefit varies. It starts switched off and uses additional GPU memory when enabled.

Both options can affect performance. Compare the result in the scene you are photographing; neither is a general lighting overhaul. **Restore game** returns these options to their original state.

### Hotsampling

Hotsampling makes the game render at a larger window size. The window can extend beyond the monitor, so you may only see part of the image on screen. The screenshot still contains the **complete rendered frame**.

Compose your image at your normal window size first, then:

1. Keep the scene frozen and open **End → Hotsampling**.
2. Select **2560 × 1440** or **3840 × 2160**. You can also enter a custom **Width / height** and click **Apply resolution**.
3. Wait until **Rendered resolution** shows the size you requested.
4. Close the interface with **End** and take your **ReShade screenshot**.
5. Reopen the interface and click **Restore resolution** to return to your original window size and position.

Use **windowed DirectX 11 mode** for this. **1440p and 4K have been tested**, including complete **3840 × 2160** ReShade captures with its effects. Larger images need more memory; sizes above 4K have not received the same validation.

Restore the original resolution before changing display mode or loading another area.

#### Saved resolutions

The **Saved resolutions** list remembers successfully applied sizes automatically. It keeps up to **16 different resolutions**, with the most recent first.

Click a saved resolution to apply it again. Your last saved size also fills the width and height fields the next time you use the camera. Failed changes and **Restore resolution** do not add entries.

### Return to gameplay

Press **Ctrl + Insert**, or choose **Restore game** in the Camera tab. This releases the free camera, restores time and the HUD, unlocks camera movement, resets object distance and enhanced shadows, and returns the window to its original resolution.

Your **Gold Filter** choices stay in place. Change them separately if you want a different look for gameplay.

**Keep running without focus** is enabled when the camera is injected. It keeps the game processing when you switch windows and stays enabled after Restore game. You can turn it off in the Camera tab.

Release freecam before loading another save or entering a cinematic.

## Credits

- **Gold Filter restoration:** **Adrian Zdanowicz (Silent / CookiePLMonster)**, creator of **[DXHRDC-GFX](https://github.com/CookiePLMonster/DXHRDC-GFX)**. The integrated color grading, bloom and lighting effects are adapted from his work under the **[MIT license](https://github.com/CookiePLMonster/DXHRDC-GFX/blob/77ac54d786b6e15dde7b3b2cb6d0812beded2d53/LICENSE)**. Original copyright: **© 2020–2021 Adrian Zdanowicz (Silent)**. Full credit for the original restoration effects belongs to Silent.


