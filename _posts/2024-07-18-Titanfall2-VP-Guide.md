# Titanfall 2

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
"setting.defaultresheight" "2160"
```
### Super Sampling
"Dynamically raises rendering resolution if the game is running faster than the target framerate."

To achieve this, you will need to activate the Adaptive Resolution FPS Target and configure it below your average FPS and activate the Adaptive SuperSampling.

![image](/assets/images/TF2-Guides.png)
>NOTE
>
>The default anti-aliasing will change to TSAA.


## Image Quality

If you are not affrais of making your CPU and GPU working at the sake of sacrifying some FPS, here are some settings that will raise the image quality
Open `%USERPROFILE%\Documents\Respawn\Titanfall2\local\videoconfig.txt` and modify the settings at wish.

| Setting | Description |
| ------- | ----------- |
| "setting.cl_particle_fallback_multiplier"        "0" |Render particles effects at max details all the time|
| "setting.r_decals"        "1024"|  Number of impacts visible. Default is 256 |             
| "setting.r_lod_switch_scale"        "4.000000"|Level of details for rocks, trees and other game elements. Default High is 1|
| "setting.cl_ragdoll_maxcount"        "16"|Default is 8|
| "setting.shadow_depthres"        "2048"|Shadows resolution. The highest the better. Default Very High is 1024. Setting higher than 2048 will crash the game at start|
| "setting.csm_quality_level"        "3"|Shadow Cascade quality. From 0 to 3 (very low to high)|
| "setting.csm_cascade_res"        "4096"|Shadow Cascade resolution. Higher is better. Breaks if set to 8192|
| "setting.fadeDistScale"        "4.000000"|Distance a which the models start to fade|
| "setting.mat_picmip" "-8"| Textures resolution|

Once you are done modifying these settings, save and set the file to read only.

## Some Reading
* [nVidia - titanfall-2 Graphics Performance and Tweaking Guide](https://www.nvidia.com/en-us/geforce/guides/gfecnt/titanfall-2-graphics-performance-and-tweaking-guide/)
* [PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Titanfall_2)
