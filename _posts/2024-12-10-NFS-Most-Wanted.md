---
layout: post
title:  "Need for Speed:  Most Wanted (2012)"
date:   2024-12-10 08:05:55 +0300
image:  NFSMW_POST.jpg
tags:   Screenshooting
---

The open-world action in Need for Speed Most Wanted gives you the freedom to drive your way. Hit jumps and shortcuts, switch cars, lie low or head for terrain that plays to your vehicle’s unique strengths. 
Fight your way past cops and rivals using skill, high-end car tech and tons of nitrous.

## Required
* [ToCa Edit 4.0.2](https://mega.nz/folder/iORliCIK#53Vv--UOAR77w6yXlihD-A/file/uSAHjIjR) (Download nfsmwrp40.zip)
* [NFSHD (2012) HD Effects by Aero](https://nfsmods.xyz/mod/2694)

## Optional
* [ReShade](https://reshade.me/downloads/ReShade_Setup_6.3.3_Addon.exe)

## Pre-Requisite
* EA App Overlay must be disabled (check if not magically re-activated).

## Installation

### ToCa Edit 4.0.2
Quite simple and straight forward. 
* Open the previous downloaded zip
* Extract `Remote Injection` folder somwhere on your disk
* Done

### NFSHD (2012) HD Effects by Aero
Also one of the simpliest thing to do
* Extract the content into your game folder (\Need for Speed(TM) Most Wanted). Where `NSF13.exe` reside.
* Done

## Configuration
For the HD Effects, read what the mod does. I can guarantee you that you won't be disappointed. 
To configure it, go to your game installation folder then in `scripts`. Ususally like `\Need for Speed(TM) Most Wanted\scripts`.
Open the file called `NFSMW2012HDEffects.ini` with a text editor. You will notice that for every setting there is an explanation. 
For me, the most interesting sections are [RESOLUTION], [VIEW DISTANCE] and [GENERAL]. 
If you have a GPU that is at least an NVIDIA Serie 2K or 8GB, you can set the [RESOLUTION] and [VIEW DISTANCE] at max.
For the [RESOLUTION] section, set the `HighShadowRefreshRate = 0` to `HighShadowRefreshRate = 1` and `SetReflectionShadow = 0` to `SetReflectionShadow = 1`.
Change `MotionBlurStrength = 5.0` to `MotionBlurStrength = 2.5`. At 5.0 it's already a bit high.

{% include note.html content="Changing `CinematicMode = 1` to `CinematicMode = 2` will automatically enable the Super Sampling at 4X. This can kill your FPS."%} 

## How To Take A Screenshot
First, we need to inject the camera. for this, open `Remote Injection` folder and launch `PluginInjector.exe`. You will see this.
<div style="width:65%; margin: auto;">
<img src="/images/NFSMW_01.jpg" alt="Remote Injection" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

Start Need for Speed: Most Wanted via EA launcher. You will get prompted with ToCa configuration screen. Once done, press `Play`.

<div style="width:65%; margin: auto;">
<img src="/images/NFSMW_02.jpg" alt="UUU v3 GUI" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
Basically, you will use the game pause feature as a time stop and the mods features for camera, time of day and HUD removal.
So, when you feel you have a great view and want to take a shot, Do as follow 

* Press the pause button on your controller or `ESC` on keyboard.
* Press `F6` or `Numpad 7` to disable the HUD.
* Press `Numpad *` to activate the camera.
* Press `Numpad 0` to activate the mouse - **IMPORTANT** for roll, pan and yaw.
* Frame your shot.
* Take your shot.
* Press `Numpad /` to disable the camera.
* Press `F6` or `Numpad 7` to enable the HUD.
* Press `B` or `ESC` to get back in game.

## Controls

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
            <th>Effect</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Numpad *</td>
            <td>Enable Camera</td>
        </tr>
        <tr>
            <td>Numpad /</td>
            <td>Disable Camera</td>
        </tr>
        <tr>
            <td>Numpad 9</td>
            <td>Free Look</td>
        </tr>
        <tr>
            <td>Numpad 3</td>
            <td>TrackIR (must be enable in config)</td>
        </tr>
        <tr>
            <td>Numpad 7 or F6</td>
            <td>Toggle HUD</td>
        </tr>
        <tr>
            <td>Numpad 1</td>
            <td>Next Car View</td>
        </tr>
        <tr>
            <td>Numpad 0</td>
            <td>Toggle Mouse</td>
        </tr>
        <tr>
            <td>Numpad .</td>
            <td>Change Camera Mode</td>
        </tr>
        <tr>
            <td>Numpad +</td>
            <td>Toggle Glass Texture</td>
        </tr>
        <tr>
            <td><br></td>
            <td><br></td>
        </tr>
        <tr>
            <td>G, J, Y, H</td>
            <td>Forward, Backward, Left, Right</td>
        </tr>
        <tr>
            <td>U, T</td>
            <td>Move Up, Down</td>
        </tr>
        <tr>
            <td>K</td>
            <td>Rest Camera</td>
        </tr>
        <tr>
            <td>SHIFT</td>
            <td>Move Faster</td>
        </tr>
                <tr>
            <td><br></td>
            <td><br></td>
        </tr>
        <tr>
            <td>F7</td>
            <td>Disable Lens Dirt</td>
        </tr>
        <tr>
            <td>F8</td>
            <td>Change Time of Day</td>
        </tr>
    </tbody>
</table>
</div>

## Resources
[PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Need_for_Speed:_Most_Wanted_(2012))



