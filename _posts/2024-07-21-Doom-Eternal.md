---
layout: post
title:  "DOOM Eternal (WIP)"
date:   2024-07-21 17:43:55 +0300
image:  DOOMEternal_POST.jpg
tags:   ["Screenshooting"]
---

DOOM Eternal, beautiful decors, and demons. Still as brutal as the first one and even more fast paced. No rest until they are all gone! 
So let's see what we can do to get the most of the game for some epic shots.

## Required

* [DOOM Eternal Console Unlocker 1.6 by Sunbeam ]

## Optional
* ReShade 6.1.1

## How To Use
Once the game is started, open the cheat table, connect to the game process and check the boxes like in the print screen below.
When done, you will have full access to the in game console. 

![image](/images/DOOMEternal-01.png)
 
## Photo Mode Anytime and Image Quality 
{% include note.html content="ReShade works only via the installer. Be sure to activate 'Enable ReShade in Vulkan Globally'." %}

In `%USERPROFILE%\Documents\Saved Games\id Software\DOOMEternal\base` create a new file called `myconfig.cfg` and copy the content below in it. 
Save it when done. 

Notice the `g_allowphotomode 1`. This will allow you to open the photo mode whenever you want. 

```
g_allowphotomode 1;photomode_freecamleashdistance -1;photomode_freecammovementtype 2;r_lodforce "0";r_texturelodbias "-8";p_showFootstepParticles "1";
r_shadowAtlasWidth 16384;r_shadowAtlasHeight 16384;r_shadowAtlasTileSize 5200;g_showPlayerShadow 1;r_filmGrainRatio -1;r_cloudsQuality 3;
r_cloudsQualityUseJitter 0;r_shadowPlayerLOD 1;r_dofHalfRes 0;r_lodScale 10;r_lodForce 0;r_lodRender 1; ;_shadowLodForceValue 0;r_flaresQuality 0;
r_dlssTextureLodBias -5;r_cineLensflaresBlurMode 2;r_cineLensflaresAnamorphicIntensity 1.05;r_blurRadialQuality 3;r_blurRadialScale 1.0;r_SSDORaytrace 1;
r_lightGridResolutionX 16;r_lightGridResolutionY 16;r_lightGridResolutionZ 16;pm_photoModeTurnFXOff 0;r_cineLensflaresAnamorphicWidth 1.5;
r_cineLensflaresAnamorphicBlueshift 0.4";
bind "F1" "g_stopTime 0";
bind "F2" "g_stopTime 1";
bind "F3" "timescale 0.1";
bind "F4" "timescale 1";
bind "F5" "toggle r_hdrAutoExposureRatio";
bind "F6" "r_cineLensflaresAnamorphicIntensity 0.925; 
bind "F7" "com_override_dof_intensity 1.0";
```

Now it's time to test your config. For this, start the game . Once you are ready to fight demons and the level is loaded, press the `~` (tilde).
Type `exec myconfig`, press enter and your config will load. After it's loaded, you should see the Photo Mode message appearing.
You will need to recall and apply the line at every new level. If you don't sse the photo mode option in the hud, re-excute the line by opeining the console and pressing arrow up. 
Press enter to apply.

{% include note.html content="If loading your config crash the game, copy and paste the line in the game console and press enter." %}
