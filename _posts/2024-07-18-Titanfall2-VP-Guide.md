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
    | Setting | Description |
    | ------- | ----------- |
    | "setting.cl_particle_fallback_multiplier"        "0" ||
    | "setting.r_decals"        "1024"|  Number of impacts visible. Default is 256 |             
    | "setting.r_lod_switch_scale"        "4.000000"||
    | "setting.cl_ragdoll_maxcount"        "16"||
    | "setting.shadow_depthres"        "2048"||
    | "setting.csm_quality_level"        "3"||
    | "setting.csm_cascade_res"        "4096"||
    | "setting.fadeDistScale"        "4.000000"||


## Some Reading
* [nVidia - titanfall-2 Graphics Performance and Tweaking Guide](https://www.nvidia.com/en-us/geforce/guides/gfecnt/titanfall-2-graphics-performance-and-tweaking-guide/)
* [PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Titanfall_2)
