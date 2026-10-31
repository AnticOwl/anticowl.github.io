---
layout: page
title: Dishonored 2 Void Camera
permalink: /dishonored-2-void-camera/
image:
---

# Dishonored 2 — Void Camera 1.49.0

A practical guide to using Void Camera with the retail version of Dishonored 2 (1.77.9.0). The in-game interface is in English, so control names below match the labels shown in the tool.

## Install and launch

1. Extract the release archive to a folder. Keep `VoidCameraInjector.exe` and `VoidCamera.dll` together.
2. Launch Dishonored 2 and wait at the main menu.
3. Run `VoidCameraInjector.exe`. It checks the game executable and injects the camera DLL.
4. Load a save. Press **F10** to show or hide the in-game panel.

Do not run another camera hook at the same time. If the injector reports that a hook is occupied, close the game completely and relaunch it before trying again. The DLL is unloaded when the game process exits.

## Camera controls

In the **Camera** tab, select **Keyboard** or **Gamepad** from **Control device** before enabling **Free camera (Insert)**. The selected device and rotation speed are saved in `%LOCALAPPDATA%\VoidCamera\settings.ini`.

Hide the panel with **F10** to control the camera. Keyboard input is read while the game window is focused. Release any movement keys before enabling the camera.

| Action | Keyboard | XInput gamepad |
|---|---|---|
| Move forward / backward | Numpad 8 / 5 | Left stick up / down |
| Move left / right | Numpad 4 / 6 | Left stick left / right |
| Move up / down | Numpad 9 / 7 | Left / right trigger |
| Look | Arrow keys | Right stick |
| Roll | Numpad 1 / 3 | D-pad left / right |
| Reset roll | Numpad 2 | — |
| Adjust vertical FOV | Numpad + / - | D-pad up / down |
| Move faster / slower | Shift / Ctrl | A / X |
| Reset FOV | — | B |

On the keyboard, **Shift** multiplies speed by 5, **Ctrl** by 0.1, and **Alt** by 0.01. Alt takes precedence over the other modifiers. **PYR rotation speed (deg/s)** adjusts rotation independently from movement speed.

**Lock camera (Home)** freezes the current camera pose without turning the camera off. Press Home again to unlock it. This is useful before resizing the game window with SRWE.

The panel shows position (XYZ), Pitch / Yaw / Roll, and vertical FOV. Values can also be entered directly. Void Camera tracks the active aspect ratio and recalculates horizontal FOV while preserving vertical FOV, including portrait and ultrawide ratios.

## Time stop and game UI

- **Time stop (Numpad 0)** in the panel, or **Numpad 0**, pauses or resumes game simulation. The camera remains controllable while time is stopped.
- **Hide game UI + markers + subtitles (Delete)** in the panel, or **Delete**, hides or restores the HUD, world markers, and cutscene subtitles where their runtime control is available.
- Cinematic black bars and the **Skip** prompt are not controlled by Void Camera.
- Pause-on-focus-loss is disabled when the DLL is injected, so the game can keep running while you use another window.

## Camera paths

1. Enable **Free camera** and position the camera at the start of the shot.
2. Open **Camera path** and select **Add current pose** to create the first node.
3. Move the camera to each new shot position and add more nodes. At least two nodes are required for playback.
4. Select a node and set **Seconds to next node**. This is the travel time from that node to the next. The last node has no outgoing segment unless **Loop path** is enabled.
5. Enable **Smooth interpolation** for a smoothed path, then choose **Play from start**.

You can insert a node after the selected node, move the selection earlier or later, update a node from the current pose, jump to a node, delete nodes, stop playback, and save or load a path. Paths are stored at `%LOCALAPPDATA%\VoidCamera\Dishonored2_CameraPath.vcp`.

With the panel hidden, path shortcuts remain available: **F6** adds a node, **Shift+F6** inserts after the selected node, **F7** deletes the selected node, **Ctrl+Page Up/Down** moves it, **F8** starts playback, and **F9** stops. Select a node in the Camera path tab before hiding the panel if you plan to use shortcuts that act on the current selection.

## Post-process, Environment, and LOD

These tabs expose render controls recognized in the supported retail build. A disabled control means its retail variable was not resolved and cannot be changed. **Restore initial render settings** returns supported values to those captured when the DLL was injected.

- **Post-process** includes exposure, bloom, lens flares, color grading, native depth of field, camera motion blur, and tone mapping. Native game DOF is separate from IGCS DOF.
- **Environment** includes fog, god rays, fog light scattering, and sky controls.
- **LOD** includes **World LOD detail scale** (lower values retain more static-world detail) and **Model shadow distance**. There is no verified general object draw-distance control in this build.

## Custom aspect ratios and capture sizes with SRWE

Version 1.49.0 does not include a Hotsampling tab. Use SRWE to resize the game window:

1. Set Dishonored 2 to **Windowed** mode.
2. In SRWE, set the game client area width and height and apply the size.
3. Optionally press **Home** first to lock the camera pose during resizing.
4. Press **Home** again to unlock it when you are ready to move.

Void Camera follows the resulting aspect ratio and recalculates horizontal FOV. SRWE handles the window size; Void Camera does not change the game's internal resolution scale.

## IGCS DOF

Void Camera connects directly to IGCS Connector through ReShade add-on support. IGCS DOF requires ReShade with add-on support, IGCS Connector, and the IGCS DOF shader and texture files. Install those files in the matching ReShade folders, enable the `IgcsDOF` technique in ReShade, then enable Void Camera before starting an IGCS DOF session. Connector status is shown in the Camera and Post-process tabs.

## Troubleshooting

- **Unsupported Dishonored 2 executable:** this build supports the verified retail executable only.
- **Hook already occupied:** close the game fully and restart it to release a camera hook left by another tool or session.
- **Camera not detected:** wait until the save has loaded and the in-game view is active.
- **Camera controls do not respond:** check that the camera is unlocked, the game is focused, the panel is hidden, and the desired control device is selected.
- **The game pauses when focus changes:** the focus-loss setting is applied by the injector. Check the injector result and restart the game before retrying if injection reported an error.
