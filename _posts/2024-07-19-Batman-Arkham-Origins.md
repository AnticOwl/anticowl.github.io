---
layout: post
title:  "Batman: Arkham Origins"
date:   2024-11-07 18:05:55 +0300
image:  BAO_POST.jpg
tags:   Screenshooting
---

Taking place before the rise of Gotham City’s most dangerous criminals, the game showcases a young and unrefined Batman as he faces a defining moment in his early career as a crime fighter that sets his path to becoming the Dark Knight.

## Required
* [Debug Menu by dron_3](https://mega.nz/file/k0kQhQhL#T7UaN_fmEgqAqSr2tB7EU1lnttRO_6ZQ8ltP5-9KVKY)
* [Improved Origins Graphics](https://www.nexusmods.com/batmanarkhamorigins/mods/451)

## Optional
* ReShade 

## Installation 

### Debug Menu Installation 
Unzip, copy and paste the `dinput8.dll` file into the game folder direcotry `.\Batman Arkham Origins\SinglePlayer\Binaries\Win32`.
The installation directory will depend of the store version (Steam, GOG or Epic). 

### Improved Origins Graphics Installation
Download the mod from NexusMods, unzip it in a folder and click twice on `ImprovedOriginsGraphics.bat`.
Choose `1 - Maximum` for better graphics and cape quality. Up to you for the contrast feature.
Once done, launch the game and reapply the graphic settings. The mod will then be active.

## How To Take A Shot
Batman Arkham Origins is somewhat more tricky if you want to take some screenchots. But it's doable. 
To activate the debug camera, do as follow:

* Press `Right Shift`.
* Press `A` on the controller (Cheat Menu)
* Navigate to `Activate Debug Camera` and press D-Pad Right
* Navigate to `Freeze Game` and press D-Pad Right
* Press `Right Shift`  

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
    <caption>Table 1</caption>
    <thead>
        <tr>
            <th>Key</th>
            <th>Effect</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>A</td>
            <td>Single Step Frame Advance</td>
        </tr>
        <tr>
            <td>B</td>
            <td>Focus DoF</td>
        </tr>
        <tr>
            <td>X</td>
            <td>Reset Roll</td>
        </tr>
        <tr>
            <td>Y</td>
            <td>Debug Light</td>
        </tr>
        <tr>
            <td>LT</td>
            <td>Move Up</td>
        </tr>
        <tr>
            <td>RT</td>
            <td>Move Down</td>
        </tr>
        <tr>
            <td>LB</td>
            <td>Slow Down Camera Movements</td>
        </tr>
        <tr>
            <td>RB</td>
            <td>Speed Up Camera Movements</td>
        </tr>
        <tr>
            <td>Zoom In / Increase FoV</td>
            <td>D-Pad Up</td>
        </tr>
        <tr>
            <td>Zoom Out / Decrease FoV</td>
            <td>D-Pad Down</td>
        </tr>
        <tr>
            <td>Roll Left</td>
            <td>D-Pad Left</td>
        </tr>
        <tr>
            <td>Roll Right</td>
            <td>D-Pad Right</td>
        </tr>
        <tr>
            <td>LS Down</td>
            <td>Camera Tracking Mode</td>
        </tr>
        <tr>
            <td>RS Down</td>
            <td>Camera Orbital Mode</td>
        </tr>
        <tr>
            <td>L</td>
            <td>Slow Motion</td>
        </tr>
        <tr>
            <td>H</td>
            <td>High Speed</td>
        </tr>
    </tbody>
</table>
</div>

When you got your shot, do the other way around to get back in the game

## Debug Menu and Visuals

To access the debug menu, two choices `RT + Menu` on your controller or `Right SHIFT`.
The navigation is far more easier with the controller as you won't have to keep the debug menu key pressed when navigating.

To have a better LOD (Level of Details), navigate until you reach the `ENGINE` page. you should see this
<div style="width:65%; margin: auto;">
<img src="/images/BAO-00.jpg" alt="Debug Menu" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
If the `Min Obj Pixels` default value is on 25.0000, lower it until you reach 0.5000 for more detailed environment.By default, the `MassiveLOD Distance Scale` is set to 1.0000. Set it to 5.0000

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/BAO-01.jpg" />
  <img slot="second" src="/images/BAO-02.jpg" />
</img-comparison-slider>

## Some Reading
[PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Batman:_Arkham_Origins)

