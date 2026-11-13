---
layout: post
title: "Horizon Light Studio — Lighting a shot in Zero Dawn Remastered and Forbidden West"
date: 2026-11-13 00:00:00 +0100
image: HLS_POST.jpg
permalink: /horizon-light-studio/
tags: Screenshooting
---

Horizon Light Studio **0.22** lets you place spotlights and omnidirectional lights inside Horizon’s photo mode. You can light Aloy from one camera position, move back to frame the portrait, and leave the light exactly where you placed it. The same in-game panel works in both games.

| Supported Windows game | Game build |
| --- | --- |
| Horizon Zero Dawn Remastered | 1.5.89.0 |
| Horizon Forbidden West Complete Edition | 1.5.80.0 |

[Set up the tool](#setup) · [Light your first portrait](#portrait) · [Position a light](#position) · [Control exposure](#exposure) · [Light settings](#settings) · [Finish or troubleshoot](#finish)

<a id="setup"></a>
## Set up the tool

1. Extract the **Horizon Light Studio 0.22** archive to a folder of your choice. Keep `HorizonLightStudio.exe`, `HorizonLightOverlay.dll` and `HorizonLightsRuntime.dll` together.
2. Launch the game, load a save and enter its native photo mode. If you already loaded an earlier version of Light Studio, restart the game once before loading the new version.
3. Run `HorizonLightStudio.exe` and return to the game window. The panel header identifies the game and tool version. **F10** shows or hides the panel.
4. Look for **Ready** at the bottom. If the panel is waiting for a camera update, give the game focus and move the photo-mode camera slightly.

The native photo-mode camera is sufficient. If you use Frans Bouma’s camera tools, you can keep using them to frame the shot. With Light Studio open, point at the settings pane to scroll it. Hide the panel with **F10** to give the camera controls the mouse again.

<a id="portrait"></a>
## Light your first portrait

1. **Choose the lighting angle.** Move the photo-mode camera slightly above and to one side of Aloy. Aim at her cheek. This is where the lamp will stand.
2. **Create the key light.** Click **+ Spot**. The spot starts at the camera and points along its view. Rename it `Key` in **Light settings** so it is easy to pick out later.
3. **Move back to your shooting position.** The spot stays in the scene. Toggle **Enabled** off and on to see exactly what it adds. If the face is dark in both views, check the aim and **Far range** before increasing **Intensity**.
4. **Shape the beam.** Adjust **Cone angle (deg)** until the beam covers the face. Adjust **Hotspot angle (deg)** to change how much of that beam forms the bright central region. Switch on **Shadows** beside **Intensity** and inspect the nose and jaw.
5. **Add fill if needed.** Move near the shadow side of the face and click **+ Omni**. An omni spreads light in every direction. Set **Radius** large enough to reach the face, then bring up **Intensity** until the shadow retains the detail you want.
6. **Take the shot.** Return to your composition, turn off **Keep gizmo visible with UI hidden**, and press **F10**. Your lights stay enabled. Use the game’s photo-mode control to hide its own HUD separately.

<a id="position"></a>
## Select, move and aim a light

Use the dropdown beside **+ Spot** or **+ Omni** to select an existing light of that type. The **Name** field identifies the light currently being edited. Both types share a pool of **32 lights**. **Duplicate** creates a copy you can reposition. **Enabled** lets you compare a light on and off while retaining its settings.

| Control | How to use it |
| --- | --- |
| **Move to camera** | Select a light, put the camera where you want the lamp and aim at the subject. Click once to copy the camera position and orientation. The local rotation offsets reset to zero. Move the camera away again to inspect the light. |
| **XYZ** | Edit the light’s world position numerically. This is useful for matching a placement or moving the light along a single axis. |
| **P / Y / R** | Adjust pitch, yaw and roll in degrees. Pitch tilts the spot, yaw turns it sideways and roll rotates it around its aim. Roll can be hard to see on a circular beam. |
| **Gizmos → Move / Rotate** | Drag a colored axis to translate the selected light or a ring to rotate it. Hold **Alt** while dragging for finer control. Move the camera away from a newly created light to see its handles. |
| **Light shape** | Shows the spot cone or the omni’s radius as a wireframe. Its origin stays attached to the light as you change the camera angle. |
| **Keep gizmo visible with UI hidden** | Keeps the selected gizmo visible after F10. Useful for checking placement from another angle. Clear it for a clean capture. |

<a id="exposure"></a>
## Balance the scene with exposure

The **EV** slider at the top changes exposure across the whole image. Its range is **−32 to +32 EV**, including values below the native photo-mode limit of −4. Hold **Alt** while dragging for small adjustments.

For a dark background with a lit subject, compose the shot and enable **Disable auto exposure**. Lower **EV** until the background looks right, then adjust the key light’s **Intensity** to expose the face. This order makes it easier to see which adjustment affects the background and which affects the subject.

Uncheck **Disable auto exposure** to resume automatic metering. Click **Restore** to release the manual EV override as well. Your placed lights stay available while you compare the exposures.

<a id="settings"></a>
## Light settings at a glance

| Setting | What to look for in the image |
| --- | --- |
| **Intensity** | Changes the output of the selected light. Use **Ctrl+click** on the numeric drag field to enter a precise value. Decimal values use a point. |
| **RGB color** | Each channel ranges from 0 to 1. For a warmer white, keep red high and lower blue slightly. After editing the color, select a second spot or omni and click **Apply previous RGB**. The next color edit becomes the new remembered RGB. |
| **Cone angle / Hotspot angle** | The cone sets the full outer opening of a spot. The hotspot defines its inner bright region. Keep the hotspot smaller than the cone. Compare on a wall to see the transition clearly. |
| **Near range / Far range** | Set the working distance of a spot. If the beam points at the subject but the surface stays dark, check that the subject falls within range. |
| **Radius** | Sets the reach of an omni. Put it close to a surface and toggle **Enabled** to judge its contribution. |
| **Volume amount / Volume samples** | Adjust the volumetric contribution and sampling. A beam can be subtle in clear air even when its light is visible on the ground. **Directionality** and **Camera depth bias** give further control over the volume. |

### Advanced controls

**Advanced** contains emitter **Dimensions**, **Diffusion**, rendering switches and fade ranges. **Dimensions** changes the emitter size. Use **Cone angle** to change the beam opening and **Far range** to change its reach. If a light fades as you move the camera, inspect **Near fade range** and **Distance fade range**.

**Advanced shadows** exposes **Shadow map resolution**, **Filter size**, **Filter samples** and **Shadow depth bias**, along with distance and size thresholds. For a rough shadow edge, hold the camera still, enable **Shadows** and compare one setting at a time. For speckling or a shadow that seems detached from a surface, make small bias adjustments and check the contact point.

**Advanced spot** adds depth fade, far-range override, shadow near plane and caustics controls. **Advanced omni** includes shadow cone and hotspot angles, shadow near plane and a volume cone multiplier. Available fields depend on the selected light and game. Their visible effect can depend on the scene and rendering mode. Duplicate a light before experimenting and disable one copy while comparing.

<a id="finish"></a>
## Finish a scene or troubleshoot a shot

- **Remove one light:** select it by name and click **Delete**. To remove every Light Studio light and its gizmo, click **Clear all lights**. Click **Restore** separately to return exposure control to the game.
- **The panel is visible but the controls are grey:** enter native photo mode, focus the game window and wait for **Ready**. Check the game build against the table above.
- **I lost a spot:** select its name, aim the camera at a nearby surface and click **Move to camera**. Back away to inspect the cone, or toggle **Enabled** to compare the surface lighting.
- **The wireframe appears in my screenshot:** open the panel, clear **Keep gizmo visible with UI hidden**, then hide the panel with **F10**.
- **I want to compare two setups:** duplicate the light, give each copy a descriptive name and enable one at a time. Light Studio 0.22 has no per-slider undo.
