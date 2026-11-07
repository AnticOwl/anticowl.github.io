---
layout: post
title: "Deus Ex: Mankind Divided — DXMD Freecam"
date: 2026-11-07 00:00:00 +0100
permalink: /deus-ex-mankind-divided-freecam/
tags: Screenshooting
---

This guide covers **DXMD Freecam 0.63** for the **Steam Windows x64 build 1.19.801.0**. The tool combines a free camera, game pause, HUD and outline hiding, native photo lights, post-processing, environment controls, geometry LOD, shadows and Jensen bone posing. It includes IGCS Connector communication for compatible ReShade screenshot workflows.

Use **DirectX 12** for the DX12-only shadow-bias controls. The camera supports DX11 and DX12; this does not mean that every experimental rendering option behaves identically in both APIs.

## Contents

Full field list: [parameter reference on the site](https://anticowl.github.io/dxmd-freecam-parameters/) · [parameter reference on GitHub](https://github.com/AnticOwl/Guides/blob/main/DXMD_Freecam_Parameters.md).

- [Install and start](#install-and-start)
- [Keyboard and controller](#keyboard-and-controller)
- [Editing and restoring values](#editing-and-restoring-values)
- [Camera](#camera)
- [Lights](#lights)
- [Post process](#post-process)
- [Environment](#environment)
- [LOD and geometry](#lod-and-geometry)
- [Shadows and banding](#shadows-and-banding)
- [Bones lab and saved poses](#bones-lab-and-saved-poses)
- [IGCS, ReShade and high-resolution capture](#igcs-reshade-and-high-resolution-capture)
- [Troubleshooting and limits](#troubleshooting-and-limits)
- [Credits](#credits)

## Install and start

1. Extract the complete compiled **0.63** package to a writable folder. Keep its folder structure and the injector, controller and DLL together.
2. Start the game, load a save and pass the **Continue [Space]** screen.
3. Run **Launch Freecam.cmd** from the extracted package, or **DXMDFreecamInjector.exe** in its versioned Release folder.
4. Return to the game. **F10** shows or hides the interface; **Insert** activates the free camera.
5. Choose **Camera input** in the Camera tab. Close F10 before flying the camera.

Inject once per game session. To replace the DLL with another version, restart the game first; stopping the camera is not a hot replacement of the loaded DLL. The tool is specific to the supported executable. Other stores, modified executables and other builds are not confirmed compatible.

ReShade, IGCS Connector and SRWE are optional external tools and are not bundled with the camera. The camera itself does not require Cheat Engine.

## Keyboard and controller

Enable **Num Lock** for the numpad camera controls. Select Keyboard / mouse or Gamepad in **Camera > Camera input**. That selection is saved to `DXMDFreecam.ini` beside the DLL. Global keyboard shortcuts remain available when Gamepad is selected.

| Action | Keyboard / mouse | Xbox / XInput controller |
| --- | --- | --- |
| Open / close the interface | F10 | Use F10 |
| Enable / disable freecam | Insert | Back + Start |
| Forward / backward | Numpad 8 / 5 | Left stick up / down |
| Strafe | Numpad 4 / 6 | Left stick left / right |
| Move down / up | Numpad 7 / 9 | LT / RT |
| Look | Mouse or arrow keys | Right stick |
| Roll left / right | Numpad 1 / 3 | D-pad left / right |
| Reset roll | Numpad 2 | B |
| Decrease / increase FOV | Numpad minus / plus | D-pad up / down |
| Slow camera movement | Hold Alt | Hold X or click/hold right stick |
| Fast camera movement | Hold Ctrl | Hold Y or click/hold left stick |
| Hide / show HUD and game UI | Delete | LB while freecam is active and F10 is closed |
| Freeze / resume game | Numpad 0 | RB while freecam is active and F10 is closed |
| Hide / show object outlines | Page Up | Use Page Up |
| Lock / unlock camera movement | Home; numpad decimal also remains available | Use Home |
| Restore camera/game camera controls | Ctrl + Insert, or Camera > Restore game | Use the button or shortcut |

Home replaced Page Down in 0.59. LB and RB are HUD and pause controls, not roll controls. The camera movement modifiers and the slider modifiers have different meanings.

## Editing and restoring values

Expandable categories keep related settings together. Boolean controls use checkboxes; numeric controls use sliders where applicable. **Ctrl + click** a slider to enter an exact value.

| Floating-point slider movement | Change per mouse pixel |
| --- | --- |
| No modifier | 1 |
| Hold Alt | 0.001 |
| Hold Ctrl | 0.1 |

The same step values are used for slider keyboard navigation. Small ranges can reach their ends quickly with the normal step; use Alt for fine work. Integer controls remain integers. Color pickers and camera/gizmo dragging are separate controls.

In Post process and the native Environment controls, editing a value enables its override. **Original** above the slider shows its native reference, and **Restore** returns the parameter to game control. For the two geometry quality tables, Original has a specific injection-time meaning described below.

**Disable effect** bypasses/neutralizes that entire supported effect. It is separate from restoring an individual parameter. **Reset post process** affects Post process; **Reset environment** affects Environment. Camera > Restore game restores camera-related state; use the tab-specific resets for PP and Environment.

Most changes apply while dragging. **Rasterizer shadow bias is deliberately different: edit, then press Apply rasterizer bias.** This prevents continuous dragging from creating a large number of native rendering states.

## Camera

- **Free camera:** move independently of gameplay. Reopen F10 to edit position, pitch, yaw, roll, vertical FOV and movement/rotation speed.
- **Freeze game:** pauses game time while the freecam stays movable. This is useful before editing lights or bones.
- **Keep running without focus:** prevents the normal loss-of-focus pause when switching to another window. It does not cancel a freeze you explicitly enabled.
- **Hide HUD and game UI:** hides the interface rendering. Restore it before you need game menus.
- **Hide object outlines:** removes object highlighting independently of the HUD.
- **Lock movement:** keeps the current camera framing while retaining the other controls.
- **Restore game:** resumes camera control, pause/HUD and related camera settings. It does not replace the PP/Environment reset buttons.

The camera tracks the game's active camera path, including cinematic work added during development. Cinematics may switch cameras or change scene state; test the specific sequence before relying on it for a long capture. Do not assume prerendered video becomes a movable 3D scene.

The freecam stores the native camera matrix and FOV for restoration. FOV is vertical in the panel; changing aspect ratio changes the relationship between vertical and horizontal framing. A persistent camera-position bookmark is not included: **Saved poses saves Jensen's skeleton, not the camera.**

## Lights

The Lights tab creates native photo lights without replacing the map's own lights. It lists only lights created by the tool, up to **16**. They are not written into the game's save.

### Create and position a light

1. Choose **Omni**, **Spot**, **Square spot**, **Capsule** or **Area**.
2. Press **Create in front of camera**. The light is placed **0.25 game units** in front of the current camera and is selected automatically. This is placement distance, not intensity.
3. Adjust Enabled, color, intensity and range. Changes are submitted while editing.
4. Use **Gizmos** with Move, Rotate or Scale, or expand Placement for numeric controls. Shape displays the light volume.
5. **Place in front of camera** repositions the selected light using the current camera. **Reset light** returns it to its creation settings; Delete light/Delete all lights remove tool-created lights.

Gizmos remain visible with F10 closed until you turn them off. Open the interface to interact with them. Use the light list to choose which light you edit.

### Types and type-specific controls

| Type | Main shape controls | Important limits |
| --- | --- | --- |
| Omni | Position, intensity and range | Omnidirectional light; no cone angle |
| Spot | Inner and outer cone angles | Native volumetric rendering and volumetric shadows were confirmed for Spot |
| Square spot | Cone angles and aspect ratio | Square/rectangular projection; volumetric pass not confirmed |
| Capsule | Capsule length | The current UI does not expose shadow-casting controls for this type |
| Area | Size XYZ and positive/negative box fades | **Area shadows are blocked in this DX12 build** because the native shader path crashed the renderer |

The interface shows the advanced properties available for the selected type:

- **Attenuation:** Near start, Near end and Far start shape the transition into/out of the light's range. The tool keeps attenuation distances ordered.
- **Shadows:** Cast shadows, Static shadows only, shadow-map resolution, near/fade distances, fade length, bleeding reduction and range inversion, where supported.
- **Volumetrics:** lighting enable, power, near fades, minimum near intensity, voxelized samples and Spot-only volumetric shadows. A visible toggle on another light type is not proof that its volumetric pass is implemented.
- **Fading / culling:** distance/near fading, simplification and projected-area thresholds. These can make a light disappear earlier than expected.
- **GI / transparency:** Exclude from GI, transparent-surface lighting and X-ray. **Bounce light disables shadows.**
- **Area box:** per-axis positive and negative fades.
- **Projection:** frame strategy/index, tiling, offsets and UV speeds. These require a projector texture to have the intended effect.
- **IES / projector resources:** choose only resources already loaded in the current level. Refresh light resources updates the list; it is not an arbitrary texture importer.

Created lights are tied to the active scene/session. Do not rely on them surviving a level transition. There is no light-rig file save/load in this version.

## Post process

These native rendering controls remain experimental. A parameter name can be known even when every value and every scene has not been visually tested. Change one parameter at a time and use Restore to compare.

| Category | Exposed controls and purpose |
| --- | --- |
| Tonemapping | **Tone Mapping Exposition** adjusts the native exposure/tonemapping input. The visible multiplication/change was confirmed during testing. |
| Glare / bloom | **Glare Saturation**, **Bright Pass Threshold**, **Bloom Scale**, **Star Scale**. Threshold selects bright input; scale controls the contribution. |
| Vignette | Vignette Color RGB/W, Gradient Light Color RGB, Gradient Light Size, Vignette Strength and Gradient Light Strength. Derived color channels are renderer values rather than independent artist-facing source properties. |
| Grain / noise | Noise Scale, Intensity, Min Luminance and Max Luminance. The luminance controls limit which brightness range receives noise. |
| SSAO | **SSAO Occlusion Range**, **SSAO Strength**, **SSAO Strength Directional**, **SSAO Max Radius**. These affect the screen-space occlusion pass; they do not increase geometry or shadow-map resolution. |

Some displayed fog/volumetric/color controls are **derived values**. Similar labels can represent different channels or transformed inputs; they are not necessarily independent duplicates. Do not assume a linear scale maps directly to a physical unit.

Chromatic aberration, sharpening and native depth-of-field experiments are not included as dedicated controls. Use your chosen ReShade workflow for additional effects where appropriate.

## Environment

Weather and shadow objects are discovered automatically after a stable level load. Wait for **Please wait until finished** before editing a dependent section. **Find weather / shadow objects** lets you request discovery again; repeatedly pressing it is unnecessary.

### Rain

The game controls rain by default. To force it:

1. Enable **Override rain**.
2. Check **Rain enabled**.
3. Adjust Rain intensity and, if needed, Advanced rain and entity parameters.

Uncheck Rain enabled while Override rain remains on to force it off. **Unchecking Override rain also unchecks and disables Rain enabled and cancels forced rain.** The native weather then resumes: if the level was naturally raining, native rain can return. Restore native rain also returns rain parameters and particle rendering to game control.

Advanced parameters include splat minimum/maximum size, dry speed, safe zone and alpha; rain/accessibility/lighting distances; specular power; streak scale, lighting and emissive contribution; splash lighting/emissive contribution; and rain speed. **Hide rain particles** only suppresses rendered particles; it is separate from the weather state.

**Character Rain Intensity affects characters, not the road or walls.** Forcing rain was visibly confirmed as rain particles, but did not automatically make the tested environment wetter.

### Atmospheric and height fog

**Atmospheric fog** includes two RGB colors, color power, near-distance endpoints, rotation and density-related derived inputs. Disabling/zeroing the atmospheric fog contribution and changing its color were confirmed during testing.

**Height fog** separates bottom and top layers, with their own enabled checkbox, RGB color, color power, density, start/end fade and near-distance endpoints. This is separate from volumetric scattering. Scene lighting, depth and game pause can make a color or density adjustment less apparent; a missing visible change is not proof that every fog layer uses that input in the current scene.

### Volumetrics

Scattering Air Density Factor has two derived entries. Smoke Speed, Smoke Intensity and Voxelized Max Range are separate controls. These affect scattering rather than the ordinary atmospheric fog composite. Their useful range depends on the scene.

### Wind

The global wind override can supply wind even without a matching level wind entity. It offers strength, yaw, pitch, gust amplitude/frequency and separate Particles, Cloth and Hair categories. Restore native wind returns control to the engine.

This does not guarantee that every visible prop responds: some effects use local wind volumes or their own simulation. The procedural global controls do not have one universal native scalar default, so their reference is shown as **Game controlled**. Their visual scope remains experimental. Entity-specific wind strength/amplitude also appear among the advanced entity parameters when a matching entity is available.

### Surface roughness

This changes the **global surface roughness**, including ground, walls and characters. Lower values are smoother/more reflective; higher values are rougher/more diffuse. An effect on the environment was visually confirmed.

It is not a complete wetness system: it does not swap every dry material to a rain variant or accumulate puddles. Actual scene wet materials exist, but no universal environment-wetness switch was validated. Restore returns the original roughness.

### Time of Day

Time of Day was removed. There is no exposed native 24-hour clock controlling sun position and color in this tool. Changing a directional light is not a sky, baked-lighting or day/night transition. The old research/status and native-property catalog panels are also absent.

## LOD and geometry

### Static and Dynamic geometry multipliers

- **g_fPCLevelOfDetailMultiplierStatic:** static environment geometry.
- **g_fPCLevelOfDetailMultiplierDynamic:** dynamic geometry.

Their current maximum is **5**. This is the tool's deliberate limit, not a proven hard maximum in the engine. Increasing them can keep more detailed geometry farther away, at a performance cost. The highest detail still depends on what the asset contains. A higher number is not a promise of extra detail on every nearby object.

Each slider currently overrides **all four entries of the corresponding native quality table**. They are not four objects and they are not four levels of a mesh.

**At injection, the tool saves all four native entries.** Original displays the first saved entry consistently, before/during/after an override. For the observed setup, the Static table was **0.85 / 0.925 / 1 / 2**, and Dynamic was **0.5 / 0.75 / 1 / 2**. These are reference observations, not forced universal defaults.

Pressing Restore reapplies each table's own captured entries. Thus the slider returns to **0.85** or **0.5** if those were the first entries at injection. The game may separately derive a current quality-dependent value of 2; that derived result must not replace the slider's saved reference. Restore does not flatten the four original entries to 0.85 or 0.5.

### Other LOD groups

| Group | What it controls / limitation |
| --- | --- |
| Camera LOD factor | `g_fPcAmplifierLOD`. A 1-to-4 test showed no visible change in the tested scene; keep it experimental. |
| Geometry — forced LOD | Forced index candidate. Its retail render consumer is not proven; do not assume every index selects a real mesh level. |
| Geometry — transitions | Dissolve and emissive-dissolve transition flags. |
| Shaders | Shader LOD enable/distance, separate from mesh geometry. |
| Textures | Mip-map bias, separate from mesh detail. |
| Clothes / cloth | Cloth LOD and high/invisible-low detail distances. |
| Destructibles / physics | Destructible LOD enable, budget, cost and benefit inputs. |
| Animation | Severe and low-movement LOD flags, separate from geometry. |
| Streaming | Low-resolution loading flag; may require an area reload. |
| LOD scheduling / camera | Update ratio, work-group size, distance/angle sphere and lock-camera candidate. |
| LOD diagnostics | Debug displays and timing candidates. |
| Primitive LODScale / LODOffset getters | Overrides native getter reads. Zero calls means no effect through that path in the current scene; scale cannot be zero. |

A PDB-confirmed name is not visual validation of every advanced switch. Shadow LOD is controlled separately under Shadows. Start with Static/Dynamic and leave unrelated budgets/scheduling native unless you are deliberately testing them.

## Shadows and banding

Shadow-map **resolution** controls detail within a map; **radius/range/cutoff** control where it covers. Increasing resolution alone does not extend shadow coverage or fix camera-dependent culling. A wider coverage at a fixed resolution can reduce apparent shadow detail.

### Distance and cascades

Near, middle and far cascades have separate enable, radius, resolution and related controls. Enabled radii must be ordered **near < middle < far**.

**Apply tested near-distance 40 preset** applies a complete tested combination:

| Parameter | Preset value |
| --- | --- |
| Near radius | 40 |
| Near source resolution | 2048 |
| Middle / far cascades | Disabled |
| Projection box | 200 × 200 |
| Projection range | 150 |
| CSM fade | 80 |
| CSM cutoff | 100 |

The successful test covered that combination, not near radius 40 in isolation. The source resolution can be scaled by native shadow quality; compare the renderer's registered map/readback where available. The global base-map setting is different from cascade resolution, and its effective sizes above 4096 were observed to be ignored by the engine.

Other groups include projection rotation/box/range, cascade light fading and caster selection, global CSM parameters, shadow exponents, cascade LOD offsets, baked/dynamic-shadow flags and camera culling. Many remain experimental. Each field has Restore; **Restore all shadow defaults** resets the shadow controls together.

### Reduce shadow banding with bias — DX12

Open **Environment > Shadows > Rasterizer shadow bias (DX12 / experimental)**. The three controls are:

- **Depth bias:** integer constant bias.
- **Depth bias clamp:** clamp applied to the bias.
- **Slope-scaled depth bias:** floating-point bias that depends on surface slope.

For **Slope-scaled depth bias**, the author reports these useful starting points against shadow banding in the tested scene:

| Shadow-map resolution | Slope-scaled depth bias |
| --- | --- |
| 2048 | **0.5** |
| 4096 | **15** |

Enter the value, then click **Apply rasterizer bias**. These are scene-tested starting points, not universal defaults or guarantees for every light and cascade. Compare both banding and shadow contact: excessive bias can detach or remove fine shadows. The sign/effect also depends on the engine's depth convention. No universal 8192 setting has been validated.

The bias controls affect shadow-map recording rather than replacing all rasterizer states in the game. DX11 keeps native rasterizer bias.

### Apply, Restore and cache limits

Moving the bias sliders only stages the three values. **Apply** commits them together. This avoids allocating a new state at every small mouse movement.

**Restore native bias** disables the override and clears the tool's **active cache to 0/48**. You can then apply another combination. Already-created native states stay alive because queued GPU commands and cached pipelines may still refer to them. Previously used combinations are reused instead of allocated again.

The native CRC table is a separate limit. If its safety capacity is reached, the tool refuses new states and reports that a restart is needed for new combinations. Clearing the active cache is not destruction of native GPU states. In older versions, a full 48/48 cache could make new slider values appear ineffective.

**Shadow depth offset / range** is another experimental pair of draw-context parameters. It is not the same as the rasterizer bias controls above, and its visual effect is not confirmed.

## Bones lab and saved poses

### Show and hold the full character

1. Enable freecam and **Show full Jensen (freecam)**.
2. Move the camera back to frame the whole character.
3. Freeze the game if you want the rest of the scene still.
4. Select **Current animation pose** or **Native reference pose (T / A)**, then click **Capture Jensen pose**.

The tool's full-body handling removes the first-person render behavior that previously displaced the body, hair and beard relative to the camera. The held pose remains editable. **Restore animation** returns Jensen to the native animator; turning off Show full Jensen returns the normal body rendering path.

### Animation poses

**Animation poses (loaded clips)** lists clips currently loaded for Jensen. Refresh the catalog after a level change. Filter by name, select a clip and choose an Animation frame. Previous frame, Next frame and Apply pose give precise control; Preview animation plays the loaded clip until stopped. Stopping preview keeps the current pose. Keep root translation preserves the captured root translation when applying a clip.

The reference session contained **379 clips**. That is a session catalog, not every animation ever shipped with the game; no universal walking-pose list is guaranteed in every level. The corrected sampler applies native finalization/procedural conversion to the complete body, not just the legs. Animation events are not replayed as gameplay actions.

### Edit bones and gizmo

Use the bone filter/list or click a joint to select it. The selected joint/name is highlighted **red**. Choose Move bone or Rotate bone and drag the gizmo axes/rings. **Escape** cancels the current drag. Bone gizmos stay visible with F10 closed when enabled; interaction requires the interface to be open.

Local rotation/translation sliders adjust the selected bone relative to the held base pose. Reset this bone removes that bone's edits; Reset pose offsets removes edits from all bones without replacing the held base pose. A natural walk requires coordinated pelvis, spine, arms and legs; using a suitable animation frame is usually easier than constructing the entire stride manually.

### Save and load complete poses

Open **Bones lab > Saved poses**:

1. Give the pose a name using letters/numbers, spaces, `-` or `_`.
2. Press **Save pose**. The current local pose and every bone edit are saved, including gizmo changes.
3. Choose a saved name from **Saved pose**, then press **Load pose** to restore it. Refresh saved poses updates the file list.

Files use `.dxmdpose` and are stored in **Poses beside DXMDFreecam.dll**, in that version's Release folder. They persist after restarting the game. Copy that Poses folder when moving to a different extracted tool version; do not overwrite your saved files with a clean package.

Loading requires freecam, Show full Jensen and a matching skeleton. Bone names and hierarchy must match; incompatible or malformed files are refused. The pose base and edits are both restored, so edits remain editable rather than being baked into an opaque final snapshot. Save/Load stops animation preview at the chosen frame.

This saves **Jensen's complete local skeleton pose**. It does not save camera framing, photo lights or Jensen's entity/world placement; the current world placement is retained. The save/load path was tested with a 336-bone round trip, but final visual reloading of a particular costume/scene still needs an in-game check.

## IGCS, ReShade and high-resolution capture

### IGCS Connector / DoF

Install a compatible ReShade setup and the external **IGCS Connector** add-on using its own instructions. The camera communicates directly with the connector; a separate IGCS Relay is not required for this built-in communication.

For a DoF or multishot session, enable freecam, frame the shot and start the session from the connector. The camera preserves the shot's pose/pause/lock state for restoration and locks conflicting edits during the capture. End the session through the connector before trying to change camera state or stop the tool. IGCS DoF was visually confirmed during development.

### Hotsampling with SRWE

The in-tool Hotsampling tab and SSAA/internal-resolution controls were removed after rendering artifacts were reported. There is **no SSAA slider in the current UI**.

External window resizing through **SRWE** remains supported. Use windowed mode, select the game window and apply the desired output size/aspect ratio. This changes output resolution; it is distinct from internal SSAA. Return to a normal window size before changing display mode or loading another area.

Portrait/nonstandard aspect handling and FOV restoration have received camera-specific fixes. Test the intended ratio in the current scene: cinematic framing, prerendered video, UI or a different camera path can still behave differently. A high output size increases GPU/VRAM cost even if the screen only shows part of the window.

## Troubleshooting and limits

| Symptom | Check |
| --- | --- |
| Camera does not move | Close F10; enable freecam; unlock with Home; verify Camera input and Num Lock. |
| Controller look/movement seems wrong | Select Gamepad, close F10 and distinguish gameplay from freecam. Do not mix a native animator issue with a freecam input test. |
| Tool waiting / object unavailable | Load a save, pass Continue, wait for discovery; retry Find weather / shadow objects after the scene is stable. |
| Rain stays checked after disabling its parent | In 0.60+, Override rain clears/disables Rain enabled. Native rain may resume if the game was raining. |
| Rain does not make the pavement wet | Rain particles and environment materials are separate. Surface roughness is a global visual alternative, not a full wetness/material swap. |
| A shadow disappears at distance | Check cascade radius/range/cutoff/caster culling, not only resolution. Try the documented near-distance preset before changing unrelated flags. |
| Bias sliders do nothing | Press Apply; check DX12, active cache and diagnostics. Restore clears the active cache. A full native state table still requires restart for new values. |
| Camera feels less smooth with LOD/shadows | Compare at the same framing. Higher geometry multipliers, wider shadow coverage and bigger maps increase rendering cost. Do not assume the maximum slider value is free. |
| Hair/beard or body displaced | Use the full-body option and held-pose workflow; the first-person body path is different. Restore animation before resuming gameplay. |
| Saved pose is refused | Check file validity and matching bone names/hierarchy. Loading does not remap a different character rig automatically. |
| You changed tool version but cannot see poses | Copy the previous version's Poses folder beside the new DLL, then Refresh saved poses. |
| Controls are locked during an IGCS capture | End the connector capture session first. |

**Validation scope:** camera/HUD/pause/controller and selected environment/light behaviors were tested in game during development. The latest slider, pose-file and cache changes also have local regression tests. Not every field/range, every cinematic, every rig or every DX11/DX12 rendering combination has received visual validation. Experimental names/ranges should not be presented as universal engine limits.

## Credits

- **Olivier César / AnticOwl:** tool and guide.
- **Frans Bouma / Otis_Inf**, with the original DXMD camera contributions from **K-putt** and **Jim2Point0**: camera interception/research adapted from [Injectable Generic Camera System — DXMD](https://github.com/FransBouma/InjectableGenericCameraSystem/tree/master/Cameras/DXMD/InjectableGenericCameraSystem), under its two-clause BSD license. The package includes `LICENSE-IGCS.txt`.
- **Dear ImGui**, Omar Cornut and contributors — MIT license.
- **MinHook**, Tsuda Kageyu and contributors — BSD license.
- **IGCS Connector / ReShade** and **SRWE** are external projects. Their own installation requirements and licenses apply; they are not redistributed by this guide.

The native parameter research used the matching retail PDB and runtime checks. Parameters that remain experimental are identified above. This guide does not include game binaries or the PDB.
