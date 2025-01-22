---
layout: post
title:  "Alien: Isolation"
date:   2025-01-21 18:05:55 +0300
image:  AI_POST.jpg
tags:   Screenshooting
---

## Required
* [OpenCAGE by Matt Filer](https://github.com/MattFiler/OpenCAGE)
* [Alias Isolation by Ryan J Gray](https://github.com/aliasIsolation/aliasIsolation/releases)
  
## Optional
* [Reshade](https://reshade.me)

## Installation
### OpenCAGE
Put the downloaded `OpenCAGE.exe` in Alien Isolation root directory along with the game exe. That's all you have to do for now.

### Alias Isolation
There are two versions of the anti aliasing mod. One for pre-2011 CPU that doesn't not support AVX (`AliasIsolation-v1.2.0-SSE3-Legacy.7z`) but SSE3 and the other that support AVX (`AliasIsolation-v1.2.0.7z`). you will probably want to download the one with AVX support.

Extract the mod into the root game folder. Be sure to see the mod folder being there. Again, you are done with the installation.

## Configuration
### OpenCAGE
Start OpenCAGE and it will The tool will set themselve up. When all done, click on `Edit Configurations`. Add your resoutions, shadow map size, lod etc. the way you want.

<div style="width:65%; margin: auto;">
<img src="/images/AI_00.jpg" alt="OpenCAGE Configuration" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

The `Shadow Map Resolution` maximum value is by default `2048`. The engine support higher with a maximum of `4096`. Everything set above that value will fallback to that value.
Regarding the LOD, the default `Ultra` value is by default `1.0`. You can go to `999` for no texture popup.

### Alias Isolation
You have 2 choices here. First one will be in game and second one via the ini file. 

### About Modded Engine File
If you have a modded `ENGINE_SETTINGS.XML` from one of the mods available on Nexus Mods, be sure that the `Anti Aliasing` section is exactly as this. 
```
			<Setting name="AntiAliasing">
			<Quality name="Off"  				int="0"		precedence="1"/>
			<Quality name="FXAA"				int="1"		precedence="2"/>
			<Quality name="SMAA T1x"			int="2"		precedence="3"/>
			<Quality name="SMAA T2x"			int="3"		precedence="4"/>
```
The `x` after T1 and T2 **MUST** be in lower case. Without that, the TAA won't work. 

### About Missing Shadows And Reflections After Planar Gloss Activation
You will need to executre the script below map per map. Once done most of the reflections and shadows will be visible.
Some can be missing.
```
Commands commands = new Commands("commands.pak");
foreach (Composite composite in commands.Entries)
{
    foreach (FunctionEntity function in composite.functions)
    {
        if (function.function != CommandsUtils.GetFunctionTypeGUID(FunctionType.ModelReference))
            continue;

        function.AddParameter("include_in_planar_reflections", new cBool(true));
        function.AddParameter("cast_shadows", new cBool(true));
        function.AddParameter("cast_shadows_in_torch", new cBool(true));
    }
}
commands.Save();
```
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

### Cinametic Tools
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
After completing and saved the graphic configuration click on `Save` and close the window.
Click on `Open Game`. 
<div style="width:65%; margin: auto;">
<img src="/images/AI_04.jpg" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>
Be sure to to check `Enable Cinematic Tools` then press `Star Alien: Isolation`. 
<div style="width:65%; margin: auto;">
<img src="/images/AI_01.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>
You shoudl see the log windows poping up. If yes, all OK.
<div style="width:65%; margin: auto;">
<img src="/images/AI_02.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

### Note About ReShade
The game can crash after taking 2 or 3, or maybe 4 shots. This because the space needed in the game memory goes above the 2 gigabyte alllowed by the 32 bit.
Workaround would be to take your shots in BMP. Be warned that the files could be **VERY** large.
<p></p>
A special thanks to Ryan J Gray and Matt Filler for their precious help!
