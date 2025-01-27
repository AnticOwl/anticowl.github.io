---
layout: post
title:  "Alien: Isolation"
date:   2025-01-21 18:05:55 +0300
image:  AI_POST.jpg
tags:   Screenshooting
---

Discover the true meaning of fear in Alien: Isolation, a survival horror set in an atmosphere of constant dread and mortal danger. Fifteen years after the events of Alien™, Ellen Ripley’s daughter, Amanda enters a desperate battle for survival, on a mission to unravel the truth behind her mother's disappearance.

## Required
* [OpenCAGE by Matt Filer](https://github.com/MattFiler/OpenCAGE/releases)
* [Alias Isolation by Ryan J Gray](https://github.com/aliasIsolation/aliasIsolation/releases)
  
## Optional
* [Reshade](https://reshade.me)

## Installation
### OpenCAGE
Download the tool from Steam and that it. That's all you have to do for now.

### Alias Isolation
There are two versions of this anti-aliasing mod. One for old pre-2011 CPUs that don't support the AVX (vector extensions for performance optimisation) (`AliasIsolation-v1.2.0-SSE3-Legacy.7z`), and the other version that only supports AVX (`AliasIsolation-v1.2.0.7z`). you will very likely want to download the one with AVX support for best performance on post-2011 hardware.

Extract the mod files into the root game directory, make sure to check that the `mods` folder is there. Once again, you are done with the installation at this point.

## Configuration
### OpenCAGE
Start OpenCAGE and the tool will set itself up. Click on the cogwheel and check `Receive updates from staging branch` and click `Apply Settings`. OpenCAGE will then start updating.
The update will resolve some bugs regarding Alias Isolation and the Graphics Settings Editor. When all is done, click on `Edit Configurations`. 

<div style="width:65%; margin: auto;">
<img src="/images/AI_00a.jpg" alt="OpenCAGE Configuration" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>

Add your resolutions, shadow map size, lod etc. exactly the way you want.

<div style="width:65%; margin: auto;">
<img src="/images/AI_00.jpg" alt="OpenCAGE Configuration" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>

* The `Shadow Map Resolution` maximum value is by default `2048`. You can go up to `4096` as this is the maximum value allowed by the engine. Everything set above that value will fallback to the engine maximum value.
* Regarding the LOD, the default `Ultra` value is by default `1.0`. You can go to `999` for no texture pop-in.
* The `Shadow Map Filter Quality` has a maximum engine value of `6`. Higher value will have the same effect as `High` (`5`).

### Alias Isolation
For this mod's configuration, you have 2 choices to change its settings. While in game by pressing `DELETE` or via a file called `settings.txt`. This file can be found in `\steamapps\common\Alien Isolation\mods\aliasIsolation\`.

An example of the contents of this file is below:
```
sharpening = 0.600000
chromaticAberration = 0.000000
```

### About Modded Engine File
If you have a modded `ENGINE_SETTINGS.XML` from one of the mods available on Nexus Mods, be sure that the `Anti Aliasing` section is exactly as follows. 
```
			<Setting name="AntiAliasing">
				<Quality name="Off"  				int="0"		precedence="1"/>
				<Quality name="FXAA"				int="1"		precedence="2"/>
				<Quality name="SMAA T1x"			int="2"		precedence="3"/>
				<Quality name="SMAA T2x"			int="3"		precedence="4"/>
			</Setting>
```
The names are case-sensitive, and the `x` after T1 and T2 **MUST** be in lower-case. Without that, Alias Isolation will not work and the game's anti-aliasing will be disabled entirely. 

### About Missing Shadows And Reflections After Planar Gloss Activation
For performance reasons, some, or most, objects are not reflected as they can add performance overhead on lower-end systems.
The only way to activate most of them would be by using game scripting (via Visual Studio).

## Controls
### Alias Isolation
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
            <td>Delete</td>
            <td>Show mod UI</td>
        </tr>
        <tr>
            <td>CTRL+Delete</td>
            <td>Disable mod</td>
        </tr>
        <tr>
            <td>CTRL+Insert</td>
            <td>Enable mod</td>
        </tr>
    </tbody>
</table>
</div>

### Cinematic Tools
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
            <td>F5</td>
            <td>Show/ hide camera tool</td>
        </tr>
        <tr>
            <td>Insert</td>
            <td>Enable/ disable camera</td>
        </tr>
        <tr>
            <td>Delete</td>
            <td>Pause/ unpause game</td>
        </tr>
        <tr>
            <td>Home</td>
            <td>Disable HUD</td>
        </tr>
        <tr>
            <td>Left stick</td>
            <td>Move camera forward/ backwards/ left/ right</td>
        </tr>
        <tr>
            <td>Right stick</td>
            <td>Pan and yaw</td>
        </tr>
        <tr>
            <td>RB/LB</td>
            <td>Roll left/ right</td>
        </tr>
        <tr>
            <td>RT/LT</td>
            <td>Move camera up/ down</td>
        </tr>
        <tr>
            <td>RS/LS down</td>
            <td>Increase/ decrease FOV</td>
        </tr>
    </tbody>
</table>
</div>

## How to Take A Screenshot
After completing and saving the graphics configuration click on `Save` and close the window.
Click on `Open Game`. 
<div style="width:65%; margin: auto;">
<img src="/images/AI_04.jpg" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>
Be sure to to check `Enable Cinematic Tools` then press `Start Alien: Isolation`. 
<div style="width:65%; margin: auto;">
<img src="/images/AI_01.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>
You should see the log windows popping up.
<div style="width:65%; margin: auto;">
<img src="/images/AI_02.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>
In your game, the Cinematic Tools UI should be displayed. Press F5 to close it.
<div style="width:65%; margin: auto;">
<img src="/images/AI_00c.jpg" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>

If you decide to use Alias Isolation, I would recommend to rebind `Insert` and `Delete` to something else, as they could conflict.

### Note About ReShade
The game can crash after taking 2, 3, or maybe 4 shots. This because the space needed in the game's memory goes above the 2 gigabyte allowed in 32-bit applications.
A workaround would be to take your shots in BMP. Be warned that the files can be **VERY** large.
<p></p>

## Special Thanks
Special thanks to Ryan J. Gray and Matt Filer for their precious help!
