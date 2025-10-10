---
layout: post
title:  "DOOM Eternal"
date:   2024-07-21 17:43:55 +0300
image:  DOOMEternal_POST.jpg
tags:   Screenshooting
---

DOOM Eternal, beautiful decors, and demons. Still as brutal as the first one and even more fast paced. No rest until they are all gone! 
So let's see what we can do to get the most of the game for some epic shots.

## Required

* [DOOM Eternal Mod Injector](https://gamebanana.com/tools/7475)

## Optional
* ReShade 6.1.1

{% include note.html content="ReShade works only via the installer. Be sure to activate 'Enable ReShade in Vulkan Globally'." %}

## How To Use
Extract the content of the zip into the game root directory (.\steamapps\common\DOOMEternal) and overwrite if prompted.
Now start `EternalModInjector.bat` to patch your game and have full access to the cvars and commands. You will get such window.
The game will start after the patching is done.

![image](https://github.com/user-attachments/assets/703c8c50-2ac4-4c7c-a1c2-3bb13330fff3)

To see if everything was correctly patched, open the console by pressing `~` and type `listcvars`. you shoud have a total of 7397.
If so, you are good to go.

## Photo Mode Anytime and Image Quality 

In `%USERPROFILE%\Documents\Saved Games\id Software\DOOMEternal\base` create a new file called `myconfig.cfg` and copy the content below in it. 
Save it when done. 

Notice the `g_allowphotomode 1`. This will allow you to open the photo mode whenever you want. 

```
g_allowphotomode 1;photomode_freecamleashdistance -1;photomode_freecammovementtype 2;r_lodforce 0;r_texturelodbias -8;p_showFootstepParticles "1"; r_shadowAtlasWidth 16384;r_shadowAtlasHeight 16384;r_shadowAtlasTileSize 5200;g_showPlayerShadow 1;r_filmGrainRatio -1;r_cloudsQuality 3;r_cloudsQualityUseJitter 0;r_shadowPlayerLOD 1;r_dofHalfRes 0;r_lodScale 10;r_lodForce 0;r_lodRender 1; r_shadowLodForceValue 0;r_flaresQuality 0;r_dlssTextureLodBias -5;r_cineLensflaresBlurMode 2;r_cineLensflaresAnamorphicIntensity 1.05;r_blurRadialQuality 3;r_blurRadialScale 1.0;r_SSDORaytrace 1;r_lightGridResolutionX 16;r_lightGridResolutionY 16;r_lightGridResolutionZ 16;pm_photoModeTurnFXOff 0;bind KP_0 toggle com_overrideDOF;bind KP_1 cvaradd com_override_dof_intensity 0.01;bind KP_2 cvaradd com_override_dof_intensity -0.01;bind KP_3 com_override_dof_intensity 1.0;bind KP_4 cvaradd r_cineLensflaresAnamorphicIntensity 0.01;bind KP_5 cvaradd r_cineLensflaresAnamorphicIntensity -0.01;bind KP_6 r_cineLensflaresAnamorphicIntensity 0.925;bind KP_7 cvaradd r_cineLensflaresAnamorphicWidth 0.01;bind KP_8 cvaradd r_cineLensflaresAnamorphicWidth -0.01;bind KP_9 r_cineLensflaresAnamorphicWidth 1.5;
```
<br>
<style>
.table_component {
    overflow: auto;
    width: 100%;
}

.table_component table {
    border: 1px solid #dededf;
    height: 100%;
    width: 100%;
    table-layout: fixed;
    border-collapse: collapse;
    border-spacing: 1px;
    text-align: left;
}

.table_component caption {
    caption-side: top;
    text-align: left;
}

.table_component th {
    border: 1px solid #dededf;
    background-color: #eceff1;
    color: #000000;
    padding: 5px;
}

.table_component td {
    border: 1px solid #dededf;
    background-color: #ffffff;
    color: #000000;
    padding: 5px;
}
</style>
<div class="table_component" role="region" tabindex="0">
<table>
    <thead>
        <tr>
            <th>Key</th>
            <th>Effect </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>NumPad 0</td>
            <td>Allow override default DOF value </td>
        </tr>
        <tr>
            <td>NumPad 1</td>
            <td>Raise DOF intensity by 0.01 </td>
        </tr>
        <tr>
            <td>NumPad 2</td>
            <td>Lower DOF intensity by 0.01 </td>
        </tr>
        <tr>
            <td>NumPad 3</td>
            <td>Reset DOF to default value 1.0 </td>
        </tr>
        <tr>
            <td>NumPad 4</td>
            <td>Raise lens flare intensity by 0.01 </td>
        </tr>
        <tr>
            <td>NumPad 5</td>
            <td>Lower lens flare intensity by 0.01 </td>
        </tr>
        <tr>
            <td>NumPad 6</td>
            <td>Reset lens flare to default value 1.0 </td>
        </tr>
        <tr>
            <td>NumPad 7</td>
            <td>Raise lens flare width by 0.01 </td>
        </tr>
        <tr>
            <td>NumPad 8</td>
            <td>Lower lens flare width by 0.001 </td>
        </tr>
        <tr>
            <td>NumPad 9</td>
            <td>Reset lens flare width to default value 1.5 </td>
        </tr>
        <tr></tr>
    </tbody>
</table>
</div>

Some other lens flares variables and their defaultvalues that can be tweaked.

```
r_cineLensflaresAnamorphicBlueshift "0.4"
r_cineLensflaresBlurMode         "1"
r_cineLensflaresBrightpassThreshold "3.0"
r_cineLensflaresChromaShiftStrength "0.5"
r_cineLensflaresDirtRatio        "10.0"
r_cineLensflaresGhostIntensity   "0.05"
r_cineLensflaresGhostOffset      "0.2"
r_cineLensflaresHaloIntensity    "0.05"
r_cineLensflaresHaloSize         "0.4"
```
<br>
Now it's time to test your config. For this, start the game . Once you are ready to fight demons and the level is loaded, press the `~` (tilde).
Type `exec myconfig.cfg`, press enter and your config will load. After it's loaded, you should see the Photo Mode message appearing.
You will need to recall and apply the line at every new level. If you don't sse the photo mode option in the hud, re-excute the line by opeining the console and pressing arrow up. 
Press enter to apply.

{% include note.html content="If loading your config crash the game, copy and paste the line in the game console and press enter." %}
