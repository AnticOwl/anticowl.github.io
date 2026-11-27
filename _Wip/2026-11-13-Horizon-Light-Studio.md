---
layout: post
title: "Horizon Light Studio and Poses — Lighting and posing in both Horizon games"
date: 2026-11-27 00:00:00 +0100
image: HLS_POST.jpg
permalink: /horizon-light-studio/
tags: Screenshooting
---

Horizon Light Studio and Poses **0.51** lets you place spotlights and omnidirectional lights inside Horizon’s photo mode. You can light Aloy from one camera position, move back to frame the portrait, and leave the light exactly where you placed it. The same in-game panel works in both games. Switch between **Lights** and **Poses** to adjust lighting, body bones, facial controls and animation frames. This guide was updated on **25 November 2026** for the 0.51 prototype.

| Supported Windows game | Game build |
| --- | --- |
| Horizon Zero Dawn Remastered | 1.5.89.0 |
| Horizon Forbidden West Complete Edition | 1.5.80.0 |

[Set up the tool](#setup) · [Light your first portrait](#portrait) · [Position a light](#position) · [Control exposure](#exposure) · [Light settings](#settings) · [Body and face](#poses) · [Save and load](#save-poses) · [Finish or troubleshoot](#finish)

<a id="setup"></a>
## Set up the tool

**Download the tool [HERE](https://anticowl.github.io/files/HorizonLightStudio.0.51.zip)**

1. Extract the **Horizon Light Studio and Poses 0.51** archive to a folder of your choice. Keep `HorizonLightStudio.exe`, `HorizonLightOverlay.dll` and `HorizonLightsRuntime.dll` together.
2. Launch the game, load a save and enter its native photo mode. If you already loaded an earlier version of Light Studio, restart the game once before loading the new version.
3. Run `HorizonLightStudio.exe` and return to the game window. The panel header identifies the game and tool version. **F10** shows or hides the panel.
4. Look for **Ready** at the bottom. If the panel is waiting for a camera update, give the game focus and move the photo-mode camera slightly.

Open **Interface** to adjust **Text size** from 100% to 200%. The panel can be resized and moved. In Poses, the bone tree can be widened independently or switched to **Full-width bone tree**.

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

**Advanced** contains emitter **Dimensions**, **Diffusion**, rendering switches and fade ranges. **Dimensions** changes the emitter size. Use **Cone angle** to change the beam opening and **Far range** to change its reach. If a light fades as you move the camera, inspect **Near fade range** and **Distance fade range**. These are separate from the spot’s physical **Near range / Far range**.

**Near fade range should normally be 0 / 0 for photography.** Nonzero values can fade out the entire light as the camera approaches, even with Shadows disabled. From **0.49**, new spots and omnis use **0 / 0** in both games. Duplicating a light preserves its edited fade settings; check the values on older or duplicated lights.

**Advanced shadows** exposes **Shadow map resolution**, **Filter size**, **Filter samples** and **Shadow depth bias**, along with distance and size thresholds. **Shadow map resolution** is a dropdown in 0.49, with **64, 128, 256, 512, 1024, 2048, 4096 and 8192**. Higher resolutions can improve shadow detail but use more graphics resources; choose the lowest value that gives the result you need. The new 8192 option still needs in-game validation. For a rough shadow edge, hold the camera still, enable **Shadows** and compare one setting at a time. For speckling or a shadow that seems detached from a surface, make small bias adjustments and check the contact point.

**Advanced spot** adds depth fade, far-range override, shadow near plane and caustics controls. **Advanced omni** includes shadow cone and hotspot angles, shadow near plane and a volume cone multiplier. Available fields depend on the selected light and game. Their visible effect can depend on the scene and rendering mode. Duplicate a light before experimenting and disable one copy while comparing.

### Shadow near plane is a different control

**Advanced spot → Shadow near plane** defaults to **1.350** for new spots. It controls the near clipping plane used for the shadow projection. It is **not** the camera-proximity fade. Keep these two settings distinct:

| Location | Setting | Default for a new light |
| --- | --- | --- |
| Advanced | Near fade range | **0 / 0** for spots and omnis in 0.49 |
| Advanced spot | Shadow near plane | **1.350** for spots |

The shadow near plane may need adjustment for very close light placements. Test it with Shadows enabled and inspect both self-shadowing and the projected silhouette.

From **0.48**, tool-created lights include dynamic objects such as Aloy in their shadow maps, instead of inheriting a static-only shadow-cache mode from a scene light. This restored Aloy’s projected shadow in the tested HFW scene. It does not guarantee that every camera-dependent shadow fade is resolved: distance and screen-size thresholds remain relevant, and the separate long-distance attenuation report is still under investigation.

<a id="poses"></a>
## Pose the body and face

Enter native photo mode before using **Poses** so the tool can acquire Aloy’s rig. Keep the game focused while editing.

### Body bones, root position and rotation

1. Open **Poses → Body** and enable **Enable pose edits**. Turn on **Bones and gizmo** to see the skeleton.
2. Select a joint in the bone tree or click its node on Aloy. Use **Find bone** to narrow the tree. Expand its arrows to reach child joints.
3. Drag a colored rotation ring, or edit **Rotation offset (degrees)**. The X / Y / Z values use the bone’s parent-local axes. Child bones follow their parent. Hold **Alt** for fine adjustment.
4. Select **rootBone** to access **Position offset X / Y / Z (m)** and move the whole pose. These are offsets in the character’s local coordinate system, not absolute map coordinates. With rootBone selected, use **Rotation offset (degrees)** to rotate the whole pose (pitch / yaw / roll, P/Y/R), or drag its rotation rings.
5. **Reset selected** clears the selected bone’s edits; selecting rootBone and resetting clears both its XYZ position offset and its rotation offsets, while preserving edits on other bones. **Reset all** in the body panel clears the body edits and any loaded body snapshot.

**Validated in 0.51 in both HFW and HZDR:** root XYZ movement, P/Y/R rotation and reset work with animations active. You can reposition and orient Aloy while retaining the animation and the edits on individual bones.

In **HZDR**, use **Bypass Look At requirement** if body editing does not update with the native camera’s Toggle Look At disabled or unavailable. This control bypasses the body-update requirement without moving the camera. HFW does not need this checkbox.

### Native poses and animation playback

Under **Native poses and playback**, choose a named pose and use the time slider to select a frame. **Play**, **Reset time**, speed and **Ping-pong** control playback. Native pose names use a fixed English list in both games, independently of the game’s language.

**Combat animations** provides a searchable list of available clips, including melee attacks and bow aiming. Select a clip, scrub **Clip time**, or use **Play**, **Loop** and speed. Bone offsets stay applied over the animation. **Use game pose** releases the combat animation override and requests restoration of the original weapon state.

**Weapon limitation:** entering photo mode with the relevant weapon already held gives the most reliable results. Starting without a weapon and selecting a combat clip can still produce incorrect weapon attachment, bow-string tension or arrow placement. This remains unfinished in both games; do not assume that a visible weapon is correctly attached throughout every animation.

### Facial controls

Open **Poses → Face**, enable **Enable facial edits**, then choose a category. The grouped controls let you adjust the face without editing each of the 178 underlying channels individually: for example, look left/right or up/down, close either eyelid, and open the jaw in **Mouth**. Changes apply live. Use the available individual resets or **Reset face** to release facial edits. Body and face edits are independent.

Leaving native photo mode automatically resets pose-editor overrides, including body, face and animation playback. It does not clear your placed lights or restore exposure. Save a pose before leaving if you want to reuse it.

<a id="save-poses"></a>
## Save and load a pose

1. In **Poses**, open **Save / Load pose** after the rig is ready.
2. Enter a **Pose name**, then click **Save pose**. Confirm **Replace** only when you intend to overwrite an existing file.
3. To reuse it, click **Refresh files**, select the saved pose and click **Load pose**.

Files are stored beside the tool’s overlay DLL, normally in the same extracted folder as the launcher:

```text
Horizon Light Studio and Poses/
  HorizonLightStudio.exe
  HorizonLightOverlay.dll
  HorizonLightsRuntime.dll
  poses/
    HFW/
    HZDR/
```

The folders are created automatically when a valid pose is saved. The tool folder must be writable. When moving to a new release folder, copy your **poses** folder too. Since 0.47, paths and pose names support Unicode, including Chinese characters, regardless of Windows language. Windows filename restrictions still apply; names cannot contain characters such as `/`, `\`, `:` or `*`.

A pose file stores the captured body pose, root position offset and available facial values. Loading applies a static snapshot at Aloy’s current location; it does not resume the source animation. Saves are separated by game and do not store the lighting setup, camera, equipment or bow-string tension.

If the saved-pose list is empty, check the folder path displayed in the panel and click **Refresh files**. If Save reports that pose data is not ready, return focus to the game, enter photo mode and wait for the live rig to be available before saving again.

<a id="finish"></a>
## Finish a scene or troubleshoot a shot

- **Remove one light:** select it by name and click **Delete**. To remove every Light Studio light and its gizmo, click **Clear all lights**. Click **Restore** separately to return exposure control to the game.
- **The panel is visible but the controls are grey:** enter native photo mode, focus the game window and wait for **Ready**. Check the game build against the table above.
- **I lost a spot:** select its name, aim the camera at a nearby surface and click **Move to camera**. Back away to inspect the cone, or toggle **Enabled** to compare the surface lighting.
- **The wireframe appears in my screenshot:** open the panel, clear **Keep gizmo visible with UI hidden**, then hide the panel with **F10**.
- **I want to compare two setups:** duplicate the light, give each copy a descriptive name and enable one at a time. Light Studio and Poses 0.51 has no per-slider undo.
