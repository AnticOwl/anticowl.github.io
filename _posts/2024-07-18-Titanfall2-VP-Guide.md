# Titanfall 2 Screenshooting Guide

## Required
* Titanfall 2 Camera by Otis_inf.
* ReShade with Shaders Toggler for HUD or [The Janitor HUD Toggle](http://www.moddb.com/games/titanfall-2/downloads/toggle-hud5)

## Pre-Requisite
* EA App Overlay must be disabled as otherwise you won't be able to use the one from the camera tool.

## Resolution and Super Sampling
### Resolution 
Titanfall 2 doesn't detect DSR resolutions and the only way to have a fullscreen resolution of 4K is to change some values in the videoconfig.txt file located in `%USERPROFILE%\Documents\Respawn\Titanfall2\local\videoconfig.txt` by the settings below.
```
"setting.defaultres" "3840"
"setting.defaultresheight" "1920"
```
### Super Sampling
"Dynamically raises rendering resolution if the game is running faster than the target framerate."

To achieve this, you will need to activate the Adaptive Resolution FPS Target and configure it below your average FPS and activate the Adaptive SuperSampling.

![image](/assets/images/TF2-Guides.png)
>NOTE
>
>The default anti-aliasing will change to TSAA.


## Image Quality

```
"VideoConfig"
{
    "setting.cl_gib_allow"        "1"
    "setting.cl_particle_fallback_base"        "0"
    "setting.cl_particle_fallback_multiplier"        "0"
    "setting.cl_ragdoll_maxcount"        "16"
    "setting.cl_ragdoll_self_collision"        "1"
    "setting.mat_depthfeather_enable"        "1"
    "setting.mat_forceaniso"        "16"
    "setting.mat_mip_linear"        "1"
    "setting.stream_memory"        "4592762"
    "setting.mat_picmip"        "-10"
    "setting.particle_cpu_level"        "2"
    "setting.r_createmodeldecals"        "1"
    "setting.r_decals"        "1024"
    "setting.r_lod_switch_scale"        "4.000000"
    "setting.shadow_enable"        "1"
    "setting.shadow_depthres"        "2048"
    "setting.shadow_maxdynamic"        "4"
    "setting.r_hbaoenabled"        "1"
    "setting.modeldecals_forceAllowed"        "1"
    "setting.dvs_enable"        "1"
    "setting.dvs_gpuframetime_min"        "15000"
    "setting.dvs_gpuframetime_max"        "16250"
    "setting.defaultres"        "3840"
    "setting.defaultresheight"        "2160"
    "setting.fullscreen"        "1"
    "setting.nowindowborder"        "1"
    "setting.mat_vsync_mode"        "2"
    "setting.mat_backbuffer_count"        "2"
    "setting.mat_antialias_mode"        "3"
    "setting.csm_enabled"        "1"
    "setting.csm_quality_level"        "3"
    "setting.csm_cascade_res"        "4096"
    "setting.fadeDistScale"        "4.000000"
    "setting.dvs_supersample_enable"        "1"
    "setting.gamma"        "1.000000"
    "setting.configversion"        "7"
}
```

## Some Reading
* [nVidia - titanfall-2 Graphics Performance and Tweaking Guide](https://www.nvidia.com/en-us/geforce/guides/gfecnt/titanfall-2-graphics-performance-and-tweaking-guide/)
* [PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Titanfall_2)
