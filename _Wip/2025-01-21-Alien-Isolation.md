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
* Reshade

## Installation
### OpenCAGE
Put the downloaded `OpenCAGE.exe` in Alien Isolation root directory alon with the game exe. That all you have to do for now.

### Alias Isolation
Extract the mod into the root game folder. Be sure to see the mod folder being there.

## Configuration
### OpenCAGE
Start OpenCAGE and click on `Edit Configurations`.

### Alias Isolation
You have 2 choices here. First one will be in game and second one via the ini file. 
### Controls
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
            <th>ToggleUI</th>
            <th>F5 </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ToggleCamera</td>
            <td>Insert </td>
        </tr>
        <tr>
            <td>Key</td>
            <td>Effect </td>
        </tr>
        <tr>
            <td>ToggleHUD</td>
            <td>Home </td>
        </tr>
        <tr>
            <td>ToggleFreezeTime</td>
            <td>Delete </td>
        </tr>
        <tr>
            <td>Camera_Forward</td>
            <td>W </td>
        </tr>
        <tr>
            <td>Camera_Backward</td>
            <td>S </td>
        </tr>
        <tr>
            <td>Camera_Left</td>
            <td>A </td>
        </tr>
        <tr>
            <td>Camera_Right</td>
            <td>D </td>
        </tr>
        <tr>
            <td>Camera_Up</td>
            <td>Space </td>
        </tr>
        <tr>
            <td>Camera_Down</td>
            <td>Left Ctrl </td>
        </tr>
        <tr>
            <td>Camera_ForwardSecondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_BackwardSecondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_LeftSecondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_RightSecondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_UpSecondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_DownSecondary</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_PitchUp</td>
            <td>Up Arrow </td>
        </tr>
        <tr>
            <td>Camera_PitchDown</td>
            <td>Down Arrow </td>
        </tr>
        <tr>
            <td>Camera_YawLeft</td>
            <td>Left Arrow </td>
        </tr>
        <tr>
            <td>Camera_YawRight</td>
            <td>Right Arrow </td>
        </tr>
        <tr>
            <td>Camera_RollLeft</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_RollRight</td>
            <td>(None) </td>
        </tr>
        <tr>
            <td>Camera_IncFov</td>
            <td>NumPad + </td>
        </tr>
        <tr>
            <td>Camera_DecFov</td>
            <td>NumPad - </td>
        </tr>
        <tr>
            <td>Track_CreateNode</td>
            <td>F1 </td>
        </tr>
        <tr>
            <td>Track_DeleteNode</td>
            <td>F2 </td>
        </tr>
        <tr>
            <td>Track_Play</td>
            <td>F3 </td>
        </tr>
        <tr>
            <td>Object_PickUp</td>
            <td>Q </td>
        </tr>
        <tr>
            <td>Object_Rotate</td>
            <td>E </td>
        </tr>
        <tr>
            <td>Object_Remove</td>
            <td>R </td>
        </tr>
        <tr>
            <td>Visuals_IncDofScale</td>
            <td>NumPad 3 </td>
        </tr>
        <tr>
            <td>Visuals_DecDofScale</td>
            <td>NumPad 2 </td>
        </tr>
        <tr>
            <td>Visuals_IncDofStrength</td>
            <td>NumPad 8 </td>
        </tr>
        <tr>
            <td>Visuals_DecDofStrength</td>
            <td>NumPad 9 </td>
        </tr>
        <tr>
            <td>Visuals_IncFocusDist</td>
            <td>NumPad 6 </td>
        </tr>
        <tr>
            <td>Visuals_DecFocusDist</td>
            <td>NumPad 5 </td>
        </tr>
        <tr>
            <td>ToggleInvisibility</td>
            <td>I </td>
        </tr>
        <tr>
            <td>FreezeCharacters</td>
            <td>F7</td>
        </tr>
    </tbody>
</table>
</div>

## How to Take A Screenshot
Now that 

<div style="width:65%; margin: auto;">
<img src="/images/AI_01.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>


<div style="width:65%; margin: auto;">
<img src="/images/AI_02.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
