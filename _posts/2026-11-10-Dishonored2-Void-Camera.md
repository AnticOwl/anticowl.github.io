---
layout: post
title: "Dishonored 2 — Void Camera"
date: 2026-11-10 10:00:00 +0100
tags: Screenshooting
---

Reprise your role as a supernatural assassin in Dishonored 2. Declared a “masterpiece” by Eurogamer and hailed “a must-play revenge tale” by Game Informer, Dishonored 2 is the follow up to Arkane’s 1st-person action blockbuster & winner of 100+ 'Game of the Year' awards, Dishonored.

## Required

* **Dishonored 2** on PC.
* [Dishonored 2 — Void Camera](https://github.com/AnticOwl/VoidCamera-Dishonored2/releases) from the Releases page. Download and extract the ZIP containing the injector and camera DLL.

## Optional

* [SRWE (Simple Runtime Window Editor)](https://github.com/dtgDTGdtg/SRWE) for custom render sizes and aspect ratios.
* An Xbox / XInput controller for gamepad camera control.
* ReShade with add-on support, the IGCS Connector add-on, and the IGCS DOF shader for the IGCS depth-of-field workflow.

## Installation

1. Extract the downloaded ZIP to a folder. Keep **VoidCameraInjector.exe** and **VoidCamera.dll** together.
2. Start Dishonored 2 and wait at the main menu.
3. Run **VoidCameraInjector.exe**. If Windows asks for permission, allow it. The injector checks that the running game is the supported retail executable before loading the DLL.
4. When injection succeeds, load your save and enter gameplay.
5. Press **F10** to show or hide the camera panel. Press **Insert** to enable or disable the free camera.

Choose **Keyboard** or **Gamepad** in the Camera tab before enabling the camera. Your choice is saved in `%LOCALAPPDATA%\\VoidCamera\\settings.ini`. The DLL unloads when the game exits. Do not inject another camera hook at the same time.

## Controls

With the camera panel hidden and the game focused:

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

<div class="table_component" role="region" tabindex="0">
<table>
<thead><tr><th>Action</th><th>Keyboard</th></tr></thead>
<tbody>
<tr><td>Show / hide the camera panel</td><td><strong>F10</strong></td></tr>
<tr><td>Enable / disable free camera</td><td><strong>Insert</strong></td></tr>
<tr><td>Lock / unlock the camera pose</td><td><strong>Home</strong></td></tr>
<tr><td>Move forward / backward</td><td><strong>Numpad 8 / 5</strong></td></tr>
<tr><td>Move left / right</td><td><strong>Numpad 4 / 6</strong></td></tr>
<tr><td>Move down / up</td><td><strong>Numpad 7 / 9</strong></td></tr>
<tr><td>Look up / down / left / right</td><td><strong>Arrow keys</strong></td></tr>
<tr><td>Roll left / right</td><td><strong>Numpad 1 / 3</strong></td></tr>
<tr><td>Reset roll</td><td><strong>Numpad 2</strong></td></tr>
<tr><td>Increase / decrease vertical FOV</td><td><strong>Numpad + / −</strong></td></tr>
<tr><td>Move faster / slower</td><td><strong>Shift / Ctrl</strong></td></tr>
<tr><td>Move very slowly</td><td><strong>Alt</strong></td></tr>
<tr><td>Stop / resume game time</td><td><strong>Numpad 0</strong></td></tr>
<tr><td>Hide / restore game UI, markers and supported cutscene subtitles</td><td><strong>Delete</strong></td></tr>
<tr><td>Add a path node</td><td><strong>F6</strong></td></tr>
<tr><td>Insert a node after the selected node</td><td><strong>Shift + F6</strong></td></tr>
<tr><td>Delete the selected node</td><td><strong>F7</strong></td></tr>
<tr><td>Play the path from the start / stop playback</td><td><strong>F8 / F9</strong></td></tr>
<tr><td>Move the selected node earlier / later</td><td><strong>Ctrl + Page Up / Page Down</strong></td></tr>
</tbody>
</table>
</div>

Enable **Num Lock** when using the numeric keypad. The selected input device controls free-camera movement; keyboard camera movement is not active while **Gamepad** is selected. The game disables pause-on-focus-loss when the camera is injected, so it can keep running while you use another window.

The **PYR rotation speed (deg/s)** slider adjusts pitch, yaw and roll speed. Its value is saved in `settings.ini`. **Shift** multiplies movement speed by 5, **Ctrl** by 0.1, and **Alt** by 0.01.

### Gamepad

With **Gamepad** selected, the first connected XInput controller uses these controls:

<div class="table_component" role="region" tabindex="0">
<table>
<thead><tr><th>Action</th><th>Gamepad</th></tr></thead>
<tbody>
<tr><td>Move forward / backward and left / right</td><td><strong>Left stick</strong></td></tr>
<tr><td>Look</td><td><strong>Right stick</strong></td></tr>
<tr><td>Move up / down</td><td><strong>Left / right trigger</strong></td></tr>
<tr><td>Roll left / right</td><td><strong>D-pad left / right</strong></td></tr>
<tr><td>Adjust vertical FOV</td><td><strong>D-pad up / down</strong></td></tr>
<tr><td>Move faster / slower</td><td><strong>A / X</strong></td></tr>
<tr><td>Reset vertical FOV</td><td><strong>B</strong></td></tr>
</tbody>
</table>
</div>

## The Tool

### Camera and time

Enable **Free camera** with **Insert**, then hide the panel with **F10** before moving. Use the Camera tab to choose the input device, lock the pose, set rotation speed, adjust vertical FOV, or edit the camera position and orientation numerically.

**Numpad 0** toggles time stop. The camera can still move while the game simulation is paused. Press it again when you want the scene to advance. **Delete** toggles the game UI, world markers and supported cutscene subtitles. Cinematic black bars and the **Skip** prompt are shader effects and are not controlled by this camera.

### Camera path

A path is an ordered list of camera poses. Each node stores position, pitch, yaw, roll, vertical FOV, camera speed, and the duration in seconds for the segment from that node to the next one. Playback starts at **Node 01** and follows the list in order. Add at least two nodes before playing.

#### Build a simple path

1. Enable the free camera and frame the first shot.
2. Click **Add current pose**. This creates **Node 01** at the current camera pose.
3. Move to the next shot and click **Add current pose** again. This creates **Node 02** after Node 01.
4. Select **Node 01** and set **Seconds to next node** to **2.00 s**. This is the travel time from Node 01 to Node 02.
5. Add a third pose. Select **Node 02** and set its duration to **5.00 s**. Node 02 controls the time from Node 02 to Node 03.
6. Click **Play from start**. Playback uses the durations on the starting nodes: for example, Node 01 → Node 02 takes 2 seconds and Node 02 → Node 03 takes 5 seconds.

The duration belongs to the node’s outgoing segment. The last node has no following segment unless **Loop path** is enabled. The path advances according to elapsed time in seconds, not the camera movement-speed setting.

#### Insert a new node between two existing nodes

Suppose the current order is:

`Node 01 → Node 02 → Node 03 → Node 04`

To add a pose between Node 02 and Node 03:

1. Select **Node 02** in the node list.
2. Move the camera to the new composition you want between those poses.
3. Click **Insert after selected**. The order becomes:

   `Node 01 → Node 02 → Node 03 (new) → Node 04 → Node 05 (old Node 03)`

4. The old Node 02 → Node 03 duration is split between the two new segments. Adjust **Seconds to next node** on the affected nodes to set the timing you want.

This operation inserts immediately after the selected node, even if that node is in the middle of the list.

#### Reorder or replace a node

**Move earlier** and **Move later** shift the selected node by one place in the list. For example, if you appended a new pose and the order is:

`Node 01 → Node 02 → Node 03 → Node 04 (new pose)`

select Node 04 and click **Move earlier** once. The order becomes:

`Node 01 → Node 02 → Node 04 (new pose) → Node 03`

Click **Move earlier** again to move it before Node 02. Each click moves only one place. Moving a node also moves its stored outgoing duration with it, so review the segment times after reordering.

To change the pose of a node without changing its place in the list, select it, move the camera to the desired pose, then click **Update selected**. **Go to selected** moves the camera to that node’s saved pose. **Delete selected** removes it.

Use **Smooth interpolation** for a smoother path between poses. If the camera overshoots a tight corner or clustered nodes, turn smoothing off or adjust the node positions. **Loop path** joins the last node back to the first. Use **Stop playback** to stop at the current camera pose.

Click **Save path** to save the current path and **Load path** to restore it. The file is:

`%LOCALAPPDATA%\\VoidCamera\\Dishonored2_CameraPath.vcp`

### Post-process and environment

The **Post-process** tab exposes the verified in-game controls for auto exposure, exposure adaptation, custom EV, bloom, lens flares, color grading, depth of field, motion blur and tone mapping. The native depth-of-field controls adjust focal distance, focus range and circle of confusion. For IGCS DOF, install ReShade with add-on support and the IGCS Connector / DOF files according to the [IGCS DOF instructions](https://opm.fransbouma.com/igcsdof.htm); the camera communicates directly with the Connector.

The **Environment** tab contains live controls for fog, god rays, fog light scattering and sky. Use **Restore initial render settings** in the relevant tab to return exposed render values to the state captured when the camera was injected.

### LOD

The LOD tab contains **World LOD detail scale** and **Model shadow distance**. A lower World LOD detail-scale value retains more static-world detail. Model shadow distance affects model-shadow culling; it is separate from static-world mesh visibility. The camera does not expose a confirmed general-purpose object draw-distance override.

### Hotsampling with SRWE

Dishonored 2 must be in **Windowed** mode for SRWE resizing. The camera has no integrated Hotsampling tab; use SRWE to resize the game window’s client area.

1. Before resizing, note the game’s current client width and height in SRWE. This is the size to restore afterward.
2. In SRWE, select the Dishonored 2 window and set the desired client-area **Width** and **Height**. You can use landscape, ultrawide or portrait dimensions. Keep the ratio you intend to capture; for example, **3840 × 2160** is 16:9, **3440 × 1440** is 21:9, and **2160 × 3840** is portrait 9:16.
3. Apply the new size in SRWE. Use its window positioning/alignment controls if the enlarged window extends beyond the monitor.
4. The game renders at the new client-area size. Void Camera reads the active aspect ratio and recalculates horizontal FOV while preserving vertical FOV, so the image should keep its proportions in both landscape and portrait ratios.
5. Capture the complete game window at the rendered dimensions with your screenshot tool. The visible part of an oversized window on the desktop may be smaller than the actual rendered frame.
6. Restore the original client width and height in SRWE when finished.

Locking the camera with **Home** before resizing is optional; use it if you want to preserve the exact camera pose while you work in SRWE. Unlock with **Home** afterward. Resizing does not depend on the camera being locked. Hotsampling changes the render window size; it does not raise the game’s internal resolution-scale setting.

## Credits

* Camera tools and game research: **AnticOwl**.
* Camera connector: **IGCS Connector** by Frans Bouma.
