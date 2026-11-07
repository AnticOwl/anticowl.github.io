---
layout: page
title: "DXMD Freecam — Parameter reference"
permalink: /dxmd-freecam-parameters/
---

These are controls exposed by the tool, not a list of validated engine maxima. Numeric bounds below are **tool/UI bounds**. Scene-dependent, derived and experimental properties may have no visible effect in a particular shot. Memory offsets are intentionally omitted. See the [user guide](https://anticowl.github.io/deus-ex-mankind-divided-freecam/) for workflow and known limits.

## Post process and fog

Original is shown above each value. Editing enables Override; Restore returns game control. Boolean height-fog enable fields use checkboxes. Derived entries are transformed render inputs, not additional independent source properties.

### Atmospheric / height fog

| Control | Type |
| --- | --- |
| Fog Color1 / R | Floating-point slider |
| Fog Color1 / G | Floating-point slider |
| Fog Color1 / B | Floating-point slider |
| Fog Color2 / R | Floating-point slider |
| Fog Color2 / G | Floating-point slider |
| Fog Color2 / B | Floating-point slider |
| Height Fog Bottom Color / R | Floating-point slider |
| Height Fog Bottom Color / G | Floating-point slider |
| Height Fog Bottom Color / B | Floating-point slider |
| Height Fog Top Color / R | Floating-point slider |
| Height Fog Top Color / G | Floating-point slider |
| Height Fog Top Color / B | Floating-point slider |
| Fog Color Power | Floating-point slider |
| Fog Color Power | Floating-point slider |
| Height Fog Bottom Color Power | Floating-point slider |
| Height Fog Top Color Power | Floating-point slider |
| Fog Near Distances / min(X,Y) (derived) | Floating-point slider |
| Fog Near Distances / max(X,Y) (derived) | Floating-point slider |
| Fog Rotation Angle (derived) | Floating-point slider |
| Fog Air Density Factor (derived) | Floating-point slider |
| Height Fog Bottom Air Density Factor (derived) | Floating-point slider |
| Height Fog Bottom Start Fade | Floating-point slider |
| Height Fog Bottom End Fade | Floating-point slider |
| Height Fog Bottom Enabled (derived) | Checkbox |
| Height Fog Top Air Density Factor (derived) | Floating-point slider |
| Height Fog Top Start Fade | Floating-point slider |
| Height Fog Top End Fade | Floating-point slider |
| Height Fog Top Enabled (derived) | Checkbox |
| Height Fog Bottom Near Distances / min(X,Y) (derived) | Floating-point slider |
| Height Fog Bottom Near Distances / max(X,Y) (derived) | Floating-point slider |
| Height Fog Top Near Distances / min(X,Y) (derived) | Floating-point slider |
| Height Fog Top Near Distances / max(X,Y) (derived) | Floating-point slider |

### Tonemapping

| Control | Type |
| --- | --- |
| Tone Mapping Exposition | Floating-point slider |

### Volumetrics

| Control | Type |
| --- | --- |
| Scattering Air Density Factor (derived) | Floating-point slider |
| Scattering Air Density Factor (derived) | Floating-point slider |
| Scattering Smoke Speed | Floating-point slider |
| Scattering Smoke Intensity | Floating-point slider |
| Voxelized Max Range | Floating-point slider |

### Glare / bloom

| Control | Type |
| --- | --- |
| Glare Saturation | Floating-point slider |
| Bright Pass Threshold | Floating-point slider |
| Bloom Scale | Floating-point slider |
| Star Scale | Floating-point slider |

### Vignette

| Control | Type |
| --- | --- |
| Vignette Color / R (derived) | Floating-point slider |
| Vignette Color / G (derived) | Floating-point slider |
| Vignette Color / B (derived) | Floating-point slider |
| Vignette Gradient Light Color / R (derived) | Floating-point slider |
| Vignette Gradient Light Color / G (derived) | Floating-point slider |
| Vignette Gradient Light Color / B (derived) | Floating-point slider |
| Vignette Color / W (derived) | Floating-point slider |
| Vignette Gradient Light Size | Floating-point slider |
| Vignette Strength | Floating-point slider |
| Vignette Gradient Light Strength | Floating-point slider |

### Grain / noise

| Control | Type |
| --- | --- |
| Noise Scale | Floating-point slider |
| Noise Intensity | Floating-point slider |
| Noise Min Luminance | Floating-point slider |
| Noise Max Luminance | Floating-point slider |

### SSAO

| Control | Type |
| --- | --- |
| SSAO Occlusion Range | Floating-point slider |
| SSAO Strength | Floating-point slider |
| SSAO Strength Directional | Floating-point slider |
| SSAO Max Radius | Floating-point slider |

## Rain / entity parameters

Availability depends on the current world/entity. Rain is game-controlled unless overridden. Character rain does not control environment wetness. Global wind has a separate section.

| Control | Type |
| --- | --- |
| Rain / Active [m_bActive] | Checkbox |
| Rain / Rain Intensity [m_fRainIntensity] | Floating-point slider |
| Rain / Splat Min Size [m_fSplatMinSize] | Floating-point slider |
| Rain / Splat Max Size [m_fSplatMaxSize] | Floating-point slider |
| Rain / Splat Dry Speed [m_fSplatDrySpeed] | Floating-point slider |
| Rain / Splat Safe Zone [m_fSplatSafeZone] | Floating-point slider |
| Rain / Splat Alpha Multiplier [m_fSplatAlphaMultiplier] | Floating-point slider |
| Rain / Max Distance [m_fMaxDistance] | Floating-point slider |
| Rain / Dynamic Rain Accessibility Max Distance [m_fDynamicRainAccessibilityMaxDistance] | Floating-point slider |
| Rain / Specular Power [m_fSpecularPower] | Floating-point slider |
| Rain / Streak Scale / X [m_vStreakScale] | Floating-point slider |
| Rain / Streak Scale / Y [m_vStreakScale] | Floating-point slider |
| Rain / Streak Lighting Power [m_fStreakLightingPower] | Floating-point slider |
| Rain / Splash Lighting Power [m_fSplashLightingPower] | Floating-point slider |
| Rain / Streak Emissive [m_fStreakEmissive] | Floating-point slider |
| Rain / Splash Emissive [m_fSplashEmissive] | Floating-point slider |
| Rain / Rain Speed / X [m_vRainSpeed] | Floating-point slider |
| Rain / Rain Speed / Y [m_vRainSpeed] | Floating-point slider |
| Rain / Max Lighting Distance [m_fMaxLightingDistance] | Floating-point slider |
| Characters only / Character Rain Intensity [m_fCharacterRainIntensity] | Floating-point slider |
| Wind / Strength [m_fStrength] | Floating-point slider |
| Wind / Strength Amplitude [m_fStrengthAmplitude] | Floating-point slider |

## Global wind and roughness

| Control | Tool range / behavior |
| --- | --- |
| Wind strength | 0–1000 |
| Wind yaw | −36000 to 36000 degrees |
| Wind pitch | −90 to 90 degrees |
| Gust amplitude | 0–1000 |
| Gust frequency | 0–100 Hz |
| Particles / Cloth / Hair | Independent category checkboxes |
| Surface roughness | 0.01–1; lower = smoother/more reflective |

## LOD

Static and Dynamic geometry defaults are captured at injection. Restore reapplies all four quality-table entries. The displayed Original is the first captured entry; it is not the current quality-derived output. Other controls return to their native reference paths. The test of `g_fPcAmplifierLOD` from 1 to 4 showed no visible change in the test scene. Forced indices and scheduling remain experimental.

### Geometry - static / dynamic

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_fPCLevelOfDetailMultiplierStatic | Float | .01 to 5 |
| g_fPCLevelOfDetailMultiplierDynamic | Float | .01 to 5 |

### Camera LOD factor

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_fPcAmplifierLOD | Float | .01 to 32 |

### Geometry - forced LOD (unvalidated)

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_nForceLODIndex.m_iValue | Int | -1 to 32 |

### Geometry - transitions

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_nDisableDissolveLOD | Checkbox | 0 to 1 |
| g_nDisableEmissiveDissolveLOD | Checkbox | 0 to 1 |

### Shaders - separate from mesh geometry

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_nDisableShaderLOD | Checkbox | 0 to 1 |
| g_fRenderShaderLodDistance | Float | .001 to 100000 |

### Textures - mip bias

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_fMipMapLodBias | Float | -16 to 16 |

### Clothes / cloth simulation

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_Apex_ClothDisableLOD | Checkbox | 0 to 1 |
| g_fClothes_MaxHighLODDistance | Float | 0 to 100000 |
| g_fClothesMaxInvisibleLowLODDistance | Float | 0 to 100000 |

### Destructibles / physics

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_Apex_DestructibleLODEnabled | Checkbox | 0 to 1 |
| g_Apex_DestructibleLODBudget | Float | .001 to 100000 |
| g_Apex_DestructibleLODUnitCost | Float | .001 to 100000 |
| g_Apex_DestructibleLODBenefitValue | Float | 0 to 100000 |

### Animation - separate from mesh geometry

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_Animation_AllowSevereLOD | Checkbox | 0 to 1 |
| g_Animation_AllowLowMovementLOD | Checkbox | 0 to 1 |
| g_Animation_ForceSevereLOD | Checkbox | 0 to 1 |
| g_Animation_ForceLowMovementLOD | Checkbox | 0 to 1 |

### Streaming - may require area reload

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_nLoadOnlyLowResLOD | Checkbox | 0 to 1 |

### LOD update scheduling / camera

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_LODSystem_RatioPerFrame | Float | .001 to 1 |
| g_LODSystem_LODUpdateUnitsGroup_MaxSize | Int | 1 to 4096 |
| g_LODSystem_DistanceAngleSphereRadius | Float | .001 to 10000 |
| g_LODSystem_LockCamera | Checkbox | 0 to 1 |

### LOD diagnostics

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_nDisplayLODs | Checkbox | 0 to 1 |
| g_nDisplayRealLODs | Checkbox | 0 to 1 |
| g_DebugLOD | Checkbox | 0 to 1 |
| g_Animation_TraceAnimGraphLOD | Checkbox | 0 to 1 |
| g_LODSystem_Debug_Enable | Checkbox | 0 to 1 |
| g_LODSystem_Debug_DisplayAverageTimeOverNFrames | Int | 1 to 10000 |

| Live getter override | Tool bounds |
| --- | --- |
| Primitive LOD scale | 0.001 to 32; cannot be zero |
| Primitive LOD offset | −32 to 32 |

## Shadows

Resolution and coverage are different controls. Restore is available per field and for the whole shadow section. For the scene-tested distance combination, see the user guide. Resolution presets do not guarantee that the engine uses that exact effective map size.

### Projection

| Control | Type | Tool bounds |
| --- | --- | --- |
| m_vLightRotation.X | Float | -360 to 360 |
| m_vLightRotation.Y | Float | -360 to 360 |
| m_vLightRotation.Z | Float | -360 to 360 |
| m_vBoxSize.X | Float | .001 to 10000 |
| m_vBoxSize.Y | Float | .001 to 10000 |
| m_fMaxRange | Float | .001 to 10000 |

### Near cascade

| Control | Type | Tool bounds |
| --- | --- | --- |
| m_fNearCascadeRadius | Float | .001 to 10000 |
| m_fNearCascadeFadeRatio | Float | 0 to 1 |
| m_eNearCascadeResolution | Resolution | 64 to 8192 |
| m_eNearCascadeBlockers | Blockers | 1 to 3 |

### Middle cascade

| Control | Type | Tool bounds |
| --- | --- | --- |
| m_bMiddleCascadeEnabled | Checkbox | 0 to 1 |
| m_fMiddleCascadeRadius | Float | .001 to 10000 |
| m_fMiddleCascadeFadeRatio | Float | 0 to 1 |
| m_eMiddleCascadeResolution | Resolution | 64 to 8192 |
| m_eMiddleCascadeBlockers | Blockers | 1 to 3 |

### Far cascade

| Control | Type | Tool bounds |
| --- | --- | --- |
| m_bFarCascadeEnabled | Checkbox | 0 to 1 |
| m_fFarCascadeRadius | Float | .001 to 10000 |
| m_fFarCascadeFadeRatio | Float | 0 to 1 |
| m_eFarCascadeResolution | Resolution | 64 to 8192 |
| m_eFarCascadeBlockers | Blockers | 1 to 3 |

### Global CSM distances

| Control | Type | Tool bounds |
| --- | --- | --- |
| m_fCSMFadeDistance | Float | 0 to 10000 |
| m_fCSMDisableDistance | Float | 0 to 10000 |

### Global shadow parameters

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_nShadowMapResolution | Resolution | 64 to 8192 |
| g_fCSMLambda | Float | 0 to 1 |
| g_fCSMPankagePlaneOffset | Float | -10000 to 10000 |
| g_fShadowFadeTime | Float | 0 to 60 |
| g_fShadowExponent | Float | 0 to 256 |
| g_fShadowExponentLinear | Float | 0 to 256 |

### Global LOD and culling

| Control | Type | Tool bounds |
| --- | --- | --- |
| g_nCSMNearCascadeLODOffset | Int | -16 to 16 |
| g_nCSMMiddleCascadeLODOffset | Int | -16 to 16 |
| g_nCSMFarCascadeLODOffset | Int | -16 to 16 |
| g_nDisableCSMFade | Checkbox | 0 to 1 |
| g_bDisableCSMLODOffset | Checkbox | 0 to 1 |
| g_bDisableShadowMapCameraCulling | Checkbox | 0 to 1 |
| g_bDisableDynamicsInShadow | Checkbox | 0 to 1 |
| g_bDisableBakedShadows | Checkbox | 0 to 1 |
| g_bForceBakedUpdate | Checkbox | 0 to 1 |

### Rasterizer bias and draw depth

Rasterizer bias is DX12-only and staged until Apply. Restore clears the active cache; native states remain retained for reuse. Native capacity is separate.

| Control | Tool bounds / known behavior |
| --- | --- |
| Depth bias | Integer −1000000 to 1000000 |
| Depth bias clamp | −1 to 1 |
| Slope-scaled depth bias | −100 to 100; reported starting points: 0.5 at 2048, 15 at 4096 |
| Shadow depth offset | −10000 to 10000; visual effect not confirmed |
| Shadow depth range | 0.001 to 10000; visual effect not confirmed |

## Native photo lights

Only properties supported by the selected type are shown. Spot volumetrics are visually confirmed; other type toggles are not a guarantee of a working volumetric pass. Capsule does not expose shadow controls. Area Cast shadows is deliberately disabled in this DX12 build.

### Attenuation

| Control | Types exposing the property | Tool bounds / type |
| --- | --- | --- |
| Near start | Omni, Spot, Square spot, Capsule, Area | .01 to 1000 |
| Near end | Omni, Spot, Square spot, Capsule, Area | .02 to 1000 |
| Far start | Omni, Spot, Square spot, Capsule, Area | 0 to 1000 |

### Shadows

| Control | Types exposing the property | Tool bounds / type |
| --- | --- | --- |
| Cast shadows | Omni, Spot, Square spot, Area | Checkbox |
| Static shadows only | Omni, Spot, Square spot, Area | Checkbox |
| Shadow map resolution | Omni, Spot, Square spot, Area | 64 to 8192 |
| Shadow near distance | Omni, Spot, Square spot, Area | .001 to 100 |
| Shadow fade distance | Omni, Spot, Square spot, Area | 0 to 10000 |
| Shadow fade length | Omni, Spot, Square spot, Area | .001 to 10000 |
| Bleeding reduction | Omni, Spot, Square spot, Area | 0 to 1 |
| Invert shadow range | Omni, Spot, Square spot, Area | Checkbox |

### Volumetrics

| Control | Types exposing the property | Tool bounds / type |
| --- | --- | --- |
| Volumetric lighting | Omni, Spot, Square spot, Capsule, Area | Checkbox |
| Volumetric shadows (Spot only) | Spot | Checkbox |
| Volumetric power | Omni, Spot, Square spot, Capsule, Area | 0 to 10000 |
| Volumetric near fade distance | Omni, Spot, Square spot, Capsule, Area | 0 to 1000 |
| Volumetric near fade length | Omni, Spot, Square spot, Capsule, Area | .001 to 1000 |
| Volumetric minimum near intensity | Omni, Spot, Square spot, Capsule, Area | 0 to 1 |
| Voxelized samples | Omni, Spot, Square spot, Capsule, Area | 1 to 255 |

### Fading / culling

| Control | Types exposing the property | Tool bounds / type |
| --- | --- | --- |
| Enable distance fading | Omni, Spot, Square spot, Capsule, Area | Checkbox |
| Fade distance | Omni, Spot, Square spot, Capsule, Area | 0 to 10000 |
| Fade length | Omni, Spot, Square spot, Capsule, Area | .001 to 10000 |
| Near fade distance | Omni, Spot, Square spot, Capsule, Area | 0 to 1000 |
| Near fade length | Omni, Spot, Square spot, Capsule, Area | .001 to 1000 |
| Minimum near intensity | Omni, Spot, Square spot, Capsule, Area | 0 to 1 |
| Enable simplification | Omni, Spot, Square spot, Capsule, Area | Checkbox |
| Simplification distance | Omni, Spot, Square spot, Capsule, Area | 0 to 10000 |
| Simplification length | Omni, Spot, Square spot, Capsule, Area | .001 to 10000 |
| Projected area culling | Omni, Spot, Square spot, Capsule, Area | 0 to 10000 |
| Minimum projected area | Omni, Spot, Square spot, Capsule, Area | 0 to 10000 |

### GI / transparency

| Control | Types exposing the property | Tool bounds / type |
| --- | --- | --- |
| Exclude from GI | Omni, Spot, Square spot, Capsule, Area | Checkbox |
| Bounce light (disables shadows) | Omni, Spot, Square spot, Capsule, Area | Checkbox |
| Light transparent surfaces | Omni, Spot, Square spot, Capsule, Area | Checkbox |
| X-ray enabled | Omni, Spot, Square spot, Capsule, Area | Checkbox |

### Area box

| Control | Types exposing the property | Tool bounds / type |
| --- | --- | --- |
| Box fade negative X | Area | 0 to 1000 |
| Box fade negative Y | Area | 0 to 1000 |
| Box fade negative Z | Area | 0 to 1000 |
| Box fade positive X | Area | 0 to 1000 |
| Box fade positive Y | Area | 0 to 1000 |
| Box fade positive Z | Area | 0 to 1000 |

### Projection

| Control | Types exposing the property | Tool bounds / type |
| --- | --- | --- |
| Frame strategy (0 wrap / 1 clamp) | Spot, Square spot, Area | 0 to 1 |
| Projector frame index | Spot, Square spot, Area | 0 to 65535 |
| Tiling X | Spot, Square spot, Area | .001 to 100 |
| Tiling Y | Spot, Square spot, Area | .001 to 100 |
| Offset X | Spot, Square spot, Area | -100 to 100 |
| Offset Y | Spot, Square spot, Area | -100 to 100 |
| UV speed X | Spot, Square spot, Area | -100 to 100 |
| UV speed Y | Spot, Square spot, Area | -100 to 100 |

### Main light controls

| Control | Tool/UI bounds |
| --- | --- |
| Type | Omni / Spot / Square spot / Capsule / Area |
| Color | RGB picker |
| Intensity | 0–1000 in slider |
| Range | 0.1–100 in slider |
| Inner cone | 0–88 degrees, clamped below outer cone |
| Outer cone | 0.1–89 degrees |
| Square-spot aspect | 0.05–20 |
| Capsule length | 0.01–20 |
| Area size XYZ | 0.01–20 per axis |
| Placement | Created 0.25 units in front of camera; numeric and gizmo editing |
| Local rotation XYZ | −180 to 180 degrees |
| IES / projector | Already-loaded resources only |

