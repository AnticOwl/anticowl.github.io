---
layout: post
title:  "Alien: Isolation"
date:   2024-08-21 18:05:55 +0300
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

[!CAUTION]
If you have a modded `ENGINE_SETTINGS.XML` be sure that the `Anti Aliasing` is exactly as this 
```
			<Setting name="AntiAliasing">
			<Quality name="Off"  				int="0"		precedence="1"/>
			<Quality name="FXAA"				int="1"		precedence="2"/>
			<Quality name="SMAA T1x"			int="2"		precedence="3"/>
			<Quality name="SMAA T2x"			int="3"		precedence="4"/>
```
The `x` after T1 and T2 **MUST** be in lower case. Without that, the TAA won't work. 

<div style="width:65%; margin: auto;">
<img src="/images/AI_01.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

<div style="width:65%; margin: auto;">
<img src="/images/AI_02.png" alt="SOD2 Mod Manager" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
