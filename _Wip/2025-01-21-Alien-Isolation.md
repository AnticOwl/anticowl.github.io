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
* [Improved Graphics by GPUnity](https://www.nexusmods.com/alienisolation/mods/19)
  
## Optional
* Reshade

## Installation
### OpenCAGE
Put the downloaded `OpenCAGE.exe` in Alien Isolation root directory alon with the game exe. That all you have to do for now.

### Alias Isolation
There are two versions of the anti aliasing mod. One for pre-2011 CPU that doesn't not support AVX (`AliasIsolation-v1.2.0-SSE3-Legacy.7z`) but SSE3 and the other that support AVX (`AliasIsolation-v1.2.0.7z`). you will probably want to download the one with AVX support.

Extract the mod into the root game folder. Be sure to see the mod folder being there. Again, you are done with the installation.

## Configuration
### OpenCAGE
Start OpenCAGE and it will The tool will set themselve up. When all done, click on `Edit Configurations`. Add your resoutions, shadow map size, lod etc. the way you want.

<div style="width:65%; margin: auto;">
<img src="/images/AI_03.jpg" alt="OpenCAGE Configuration" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
OR
<div> </div>
Run the GPUnity tool to modify the `ENGINE_SETTINGS.XML`. Disable startup movies and/or lens falre if you want. 

### Alias Isolation
You have 2 choices here. First one will be in game and second one via the ini file. 

### About Modded Engine File
If you have a modded `ENGINE_SETTINGS.XML` be sure that the `Anti Aliasing` section is exactly as this. 
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
            <th>Effect </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Toggle Camera Tools UI</td>
            <td>F5 </td>
        </tr>
	<tr>
            <td>Toggle Camera</td>
            <td>Insert </td>
        </tr>
        <tr>
            <td>Toggle HUD</td>
            <td>Home </td>
        </tr>
        <tr>
            <td>Toggle Freeze Time</td>
            <td>Delete </td>
        </tr>
        <tr>
            <td>Camera Forward</td>
            <td>W </td>
        </tr>
        <tr>
            <td>Camera Backward</td>
            <td>S </td>
        </tr>
        <tr>
            <td>Camera Left</td>
            <td>A </td>
        </tr>
        <tr>
            <td>Camera Right</td>
            <td>D </td>
        </tr>
        <tr>
            <td>Camera Up</td>
            <td>Space </td>
        </tr>
        <tr>
            <td>Camera Down</td>
            <td>Left Ctrl </td>
        </tr>
        <tr>
            <td>Camera Forward Secondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera Backward Secondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera Left Secondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera Right Secondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera Up Secondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera Down Secondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera Pitch Up</td>
            <td>Up Arrow </td>
        </tr>
        <tr>
            <td>Camera Pitch Down</td>
            <td>Down Arrow </td>
        </tr>
        <tr>
            <td>Camera Yaw Left</td>
            <td>Left Arrow </td>
        </tr>
        <tr>
            <td>Camera Yaw Right</td>
            <td>Right Arrow </td>
        </tr>
        <tr>
            <td>Camera Roll Left</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera Roll Right</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Increment Fov</td>
            <td>NumPad + </td>
        </tr>
        <tr>
            <td>Decrement Fov</td>
            <td>NumPad - </td>
        </tr>
        <tr>
            <td>Track Create Node</td>
            <td>F1 </td>
        </tr>
        <tr>
            <td>Track Delete Node</td>
            <td>F2 </td>
        </tr>
        <tr>
            <td>Track Play</td>
            <td>F3 </td>
        </tr>
        <tr>
            <td>Object Pick Up</td>
            <td>Q </td>
        </tr>
        <tr>
            <td>Object Rotate</td>
            <td>E </td>
        </tr>
        <tr>
            <td>Object Remove</td>
            <td>R </td>
        </tr>
        <tr>
            <td>Incrememnt Dof Scale</td>
            <td>NumPad 3 </td>
        </tr>
        <tr>
            <td>Decrement Dof Scale</td>
            <td>NumPad 2 </td>
        </tr>
        <tr>
            <td>Increment Dof Strength</td>
            <td>NumPad 8 </td>
        </tr>
        <tr>
            <td>Decrement Dof Strength</td>
            <td>NumPad 9 </td>
        </tr>
        <tr>
            <td>Increment Focus Distance </td>
            <td>NumPad 6 </td>
        </tr>
        <tr>
            <td>Decrement Focus Distance </td>
            <td>NumPad 5 </td>
        </tr>
        <tr>
            <td>Toggle Invisibility</td>
            <td>I </td>
        </tr>
        <tr>
            <td>Freeze Characters</td>
            <td>F7</td>
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
A special thanks to Ryan J Gray and Matt Filler for the precious help!
