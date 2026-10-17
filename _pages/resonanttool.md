---
layout: page
title: "ResonantTool — CONTROL Resonant"
permalink: /resonanttool/
---

# ResonantTool

**Native lighting and post-processing tool for CONTROL Resonant**  
**Documented source version:** `v0.12i` · **Module:** `ResonantTool.dll` · **Platform:** Windows x64 / DirectX 12

> **Screenshots:** An in-game screenshot will be added later. This page deliberately contains no placeholder screenshot from another application or version.

## Overview

ResonantTool is an in-game **DirectX 12 / Dear ImGui** tool for editing native lighting, selected post-processing parameters and LOD settings in `CONTROLResonant.exe`. The interface exposes four tabs: **Spots**, **Point Lights**, **PP** and **LOD**. It is implemented as a single x64 DLL loaded into the game's process; it does not require a DX11 renderer or a ReShade overlay.

ResonantTool uses engine-native requests where they have been identified, and direct process-relative values for selected rendering parameters. The distinction matters: a native request may be accepted before the renderer reflects the change; a direct value may be overwritten by Northlight's own updates.

**Compatibility:** This documentation describes the current, specific executable mappings used by the v0.12i source. It is not a universal Northlight SDK. Changes to the game's executable can invalidate offsets or native call sites.

## Requirements and installation

- A compatible Windows x64 installation of **CONTROL Resonant** (`CONTROLResonant.exe`).
- The `ResonantTool.dll` built for that executable version.
- An injection method capable of loading a 64-bit DLL into the running game process. The runtime module itself is one DLL; the source archive additionally includes an *optional developer injector*.
- DirectX 12 active in the game.

**To use an existing DLL:** Launch the game, load `ResonantTool.dll` into `CONTROLResonant.exe` using your preferred compatible injection method, then press **F11** to display the overlay. Press **F11** again to hide it.

**Build from source:** On Windows, use Visual Studio 2022 with C++ x64 tools and CMake, then run `Build.cmd` from the source directory. The CMake project downloads Dear ImGui **v1.91.9b** and MinHook **v1.3.4** and builds `ResonantTool.dll`. The included build script also builds/copies the optional `ResonantInjector.exe`; that executable is **not required as a runtime companion** once the DLL is injected. Network access is needed for CMake's dependency download unless those dependencies are already cached.

> Source packages are not equivalent to a prebuilt DLL. Windows compilation, executable compatibility and in-game behavior should be checked separately. Avoid applying this experimental process modification to an important game session without a backup.

## Controls and navigation

- **F11** — open or hide the tool's in-game ImGui window.
- **Mouse** — operate tabs, sliders, toggles, color pickers and buttons.
- **Ctrl + click a slider** — enter a precise numeric value (for ImGui sliders that support it).
- The tool is **not a free camera**: its Spot/Point creation controls use the game's **current live camera position and orientation**; an external free camera can be used when compatible.

With the overlay open, the implementation attempts to prevent normal game keyboard/mouse input from also being triggered. Hiding the overlay returns normal input handling.

## Spots tab

The **Spots** tab creates native spotlights, lists created spots and edits the selected one. The creation panel includes **Create Spot at Camera**, **Move Spot at Camera**, distance, default intensity and default color. An optional position override is available in the source UI; the camera remains the normal starting point.

### Position and rotation

Select a created Spot and use **Spot Positioning | XYZ / PYR**:

| Control | Meaning |
|---|---|
| X / Y / Z | Spotlight world position |
| Pitch / Yaw / Roll | Spotlight orientation, in degrees |
| Move Spot at Camera | Move the selected Spot to the current camera-based position |
| Align selected to camera | Copy the live camera position and orientation to the selected Spot |

The tool submits the native transform while you edit, throttled to roughly **20 updates per second**, with a final request when the edit is released. The displayed edit values may precede renderer confirmation.

### Lighting and shape

| Control | Description |
|---|---|
| Intensity | Light output strength |
| Color | RGB light color |
| Specular Multiplier | Specular contribution, presented on a **0–1** control in the current UI |
| Spot Angle | Cone angle |
| Spot Softness | Cone edge softness |
| Spot Roundness | Cone roundness |
| Directionality | Directional component / renderer-pool test when no native component base is available |
| Scatter Multiplier | Scattering contribution |
| Spot ON / OFF | Current implementation toggles **intensity**, saving/restoring the previous positive value; it is not a native component-enable flag |

### Distance and far clip

The **Distance & Far Clip** section exposes **Near**, **Near Softness**, **Far** and **Far Softness** via identified native float commands. **Far Clip** itself is assumed enabled in the game configuration; the source does not implement a validated Far Clip ON/OFF opcode.

### Volumetric

The **Volumetric** section includes **Enable Volumetric**, **Volumetric Intensity**, **Scattering Phase 1**, **Scattering Phase 2**, **Scattering Phase Blend** and **Volumetric Bounding Shape**. Native request submission and the final visual effect are not identical guarantees; some phase values may be updated or derived internally by the renderer.

## Point Lights tab

The **Point Lights** tab can create a Point Light at the current camera, select a created light, and move it back to the camera.

| Control | Description |
|---|---|
| Create Point at Camera | Request a new native Point Light |
| Distance | Offset relative to the camera for initial placement |
| Default intensity / Default color | Initial creation values |
| Move Point to Camera | Align selected point light to camera position |
| Position X / Y / Z | Edit position |
| Intensity / Color | Edit light output |
| Scatter Multiplier | Scattering |
| Far Distance / Draw Distance | Attenuation and visibility-related distances |
| Source Radius | Source size |
| Directional Falloff | Directional falloff |

**Point volumetric controls are intentionally not provided.** The Point Light editor sends identified native commands, but some command-to-renderer responses remain less thoroughly verified than Spot creation.

## PP tab — Post-processing

The PP tab exposes **13 parameters** grouped by Bloom, PostProcess, Atmosphere and Camera. The current v0.12i UI has **exactly four** `Override` checkboxes, placed to the right of the corresponding numeric controls. Other PP parameters remain **direct value editing only**; no global PP override checkbox is added.

| Group | Control | UI behavior |
|---|---|---|
| Bloom | **Bloom Intensity** | Direct numeric edit; **Override** checkbox (native setter interception) |
| Bloom | **Bloom Threshold** | Direct numeric edit |
| Bloom | **Bloom Scatter** | Direct numeric edit; **Override** checkbox (native setter interception) |
| Bloom | **Bloom Lens Dirt** | Direct numeric edit |
| PostProcess | **Radial Blur** | Direct numeric edit |
| PostProcess | **Brightness** | Direct numeric edit |
| PostProcess | **Saturation** | Direct numeric edit |
| PostProcess | **Vignette** | Direct numeric edit; **Override** checkbox (native setter interception) |
| PostProcess | **Film Grain** | Direct numeric edit; **Override** checkbox (native setter interception) |
| Atmosphere | **Scatter Blur** | Direct numeric edit |
| Atmosphere | **Scatter Direction 1** | Direct numeric edit |
| Atmosphere | **Scatter Direction 2** | Direct numeric edit |
| Camera | **Lens Distortion** | Direct numeric edit |

### Understanding the overrides

**Direct edit:** A value is written to an identified game parameter field when you change the control. If the engine recomputes this value later, the displayed setting may change again.

**Native `Override`:** For the four checked controls, the source installs a guarded shared hook on the game's float-parameter setter. When Northlight updates a matching parameter ID, the tool replaces the submitted value with the user-selected one. When a checkbox is off, that parameter is left to the native setter. The hook is deliberately limited to those four controls; it does **not** automatically support every PostProcess value.

**Validation distinction:** Bloom Intensity and Bloom Scatter were confirmed in earlier Cheat Engine override experiments. The Vignette and Film Grain hooks were added in v0.12i; the source's own release notes say their interception **was not yet validated in game**. The user subsequently accepted v0.12i as the project baseline, but no additional per-feature verification log is bundled with that source archive. A checked box is therefore not, by itself, evidence that Northlight is issuing a corresponding setter call.

**Not included in the PP tab:** DoF, Exposure, SSAO, SSR, Motion Blur and ColorGrading were deliberately excluded from the new PP tab. A **separate existing Fixed Exposure / Override Exposure control** remains in the broader tool UI because it predates this tab. **Flare is not implemented** in this release.

## LOD tab

The LOD tab contains the **three selected controls**, with no extra override checkboxes:

| Control | Value type | What it influences |
|---|---|---|
| **LOD:Target Size** | Signed 32-bit integer | Reference target size used by LOD selection; changing **1080 → 2160** produced a visible difference in earlier tests |
| **Hierarchy LOD:Distance scale** | Float32 | Scale affecting hierarchy LOD transitions; values including **1 → 0** produced a visual change |
| **LOD: Lod Menu Multiplier** | Float32 | LOD multiplier; accessible in the current UI, but its exact visual effect was not independently established in the documented tests |

**LOD:Default Cutoff Screen Size** is intentionally excluded at the user's request. **LOD:Force Highest Visual LOD** is not exposed as a switch because its underlying ON/OFF field was not conclusively identified.

### LOD vs. shadow draw distance

LOD affects which geometry/detail version Northlight selects. **Shadow culling range, shadow-cascade transitions and vegetation shadows can be separately controlled internally**, so changing a LOD setting does not necessarily increase the distance at which vegetation shadows are rendered. The exact native Shadow Draw Distance parameter has **not** been confirmed for this tool. Do not describe the three LOD controls as a proven shadow-distance override.

## Technical notes

This section is intended for maintainers. All the following numeric addresses are **RVAs** relative to `CONTROLResonant.exe`, not absolute process pointers, and are **version-specific**.

### PP parameter addresses

The direct editable PP values use the native block's `+A4` field in the mappings tested. Among the primary entries:

| Parameter | RVA of editable field |
|---|---|
| Bloom Intensity | `0x5ED4164` |
| Bloom Threshold | `0x5ED4094` |
| Bloom Scatter | `0x5ED3F34` |
| Bloom Lens Dirt | `0x5ED3CF4` |
| Radial Blur | `0x5D240C4` |
| Brightness | `0x5D24F84` |
| Saturation | `0x5D24B34` |
| Vignette | `0x5D24D94` |
| Film Grain | `0x5D24EB4` |
| Scatter Blur | `0x5ED3E64` |
| Scatter Direction 1 | `0x5D21844` |
| Scatter Direction 2 | `0x5D22094` |
| Lens Distortion | `0x5E5F784` |

The guarded native float setter is at **`+0x1B5CBD0`**. Bloom Intensity uses ID `0x7036C003`; Bloom Scatter uses ID `0x21A17DB0`. Vignette and Film Grain IDs are read from their parameter blocks at runtime. The shared hook relies on an expected instruction sequence and **refuses installation if that signature does not match**. It preserves normal execution via a MinHook trampoline, without using NOP-based PP freezing.

### LOD addresses

| Parameter | RVA of edited value | Type |
|---|---|---|
| LOD:Target Size | `0x5E73060` | Int32 |
| Hierarchy LOD:Distance scale | `0x5C13F68` | Float32 |
| LOD: Lod Menu Multiplier | `0x5E73590` | Float32 |

### Rendering and module structure

- **DX12 only:** the DLL uses the D3D12 command queue, swap chain and ImGui DX12 backend.
- **Native lighting:** Spot and Point creation and updates use game-specific native request paths and ID-based control operations.
- **Camera source:** native camera capture is used for spawn and alignment. This DLL does not implement a general free-camera controller.
- **UI lifetime:** **F11** toggles the overlay; light objects and previous commands are not deleted by hiding the UI.
- **Exposure:** the existing UI supports fixed exposure with restoration of the previously observed exposure mode when its override is disabled.
- **Source dependencies:** C++17, CMake, Dear ImGui and MinHook.

## Troubleshooting

| Symptom | Check |
|---|---|
| **F11** does nothing | Confirm the DLL was injected into the intended running `CONTROLResonant.exe`, that the game is using DX12, and that no other overlay conflicts with its input handling |
| Camera-based Spot/Point creation is unavailable | The game's live camera pointer may not yet be captured; enter gameplay before attempting creation |
| Native request accepted but light is not visible | A native request may be queued before the renderer confirms it; inspect position, intensity, draw distance and game state |
| PP value returns to its previous value | That control may be direct-edit only, or its setter hook may not intercept the producer updating it |
| A PP Override refuses to enable | The known native setter signature may not match the running executable |
| LOD has no visible effect on distant shadows | LOD selection and shadow-culling range are distinct rendering systems |
| Build fails | Check Visual Studio 2022 x64 C++ workload, CMake and dependency downloads; the source build has not been compiled by this documentation process |

## Status and scope

**Baseline:** ResonantTool v0.12i source, user-accepted for documentation. This page reflects the features actually present in that source, and explicitly marks uncertain or experimental areas rather than claiming full game validation.

**Not in this release:** a native Flare editor, a validated Force Highest Visual LOD toggle, or a dedicated native shadow draw-distance override. No extra tabs, global overrides or diagnostics are implied.

## Screenshots

*An actual screenshot of the final ResonantTool in-game interface will be inserted here after it is provided.*

---

*Unofficial community tool; not affiliated with or endorsed by Remedy Entertainment.*