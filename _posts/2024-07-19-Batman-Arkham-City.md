---
layout: post
title:  "Batman: Arkham City"
date:   2024-11-06 18:05:55 +0300
image:  BAC_POST.jpg
tags:   Screenshooting
---

Bruce Wayne is incarcerated in Arkham City, a super-prison enclosing the decaying urban slums of Gotham City. He dons his alter ego, Batman, and goes on a mission to uncover the secret behind a sinister scheme orchestrated by the facility's warden, Hugo Strange.

## Required
* [Debug Menu by dron_3](https://mega.nz/file/k0kQhQhL#T7UaN_fmEgqAqSr2tB7EU1lnttRO_6ZQ8ltP5-9KVKY)
* [Arkham City Redux](https://www.nexusmods.com/batmanarkhamcity/mods/407)

## Optional
* [Cheat Table by One3rd, Cielos and Sunbeam](https://framedsc.com/CheatTables/BatmanACv0.5.2.CT)
* Reshade

## Installation 

### Debug Menu Installation
Unzip, copy and paste the `dinput8.dll` file into the game folder direcotry `..\Batman Arkham City GOTY\Binaries\Win32\`.
The installation directory will depend of the store version (Steam, GOG or Epic). 

### Arkham City Redux Installation

No need of a long explanation here, you will find the detailed procedure on this [Steam Community Post](https://steamcommunity.com/sharedfiles/filedetails/?id=1188257825).

## Configuration

If everything is going according to plan, when you launch Batman Arkham City, you should be welcomed by the Advanced Launcher.
Here the fun begins with multiple settings. The game is from 2011 and should have no problem running on recent hardware with some settings maxed out. 
<div style="width:65%; margin: auto;">
<img src="/images/BAC_00.jpg" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

Something that needs to be disabled if active is the Debug Menu keybind. it's not useful here. 
<div style="width:65%; margin: auto;">
<img src="/images/BAC_01.jpg" alt="UUU v3 GUI" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

## How To Take A Shot

Once in game, simply press `BACKSPACE` on your keyboard to enter in debug camera mode. 
Great thing about it is that it has 3 modes: Free, chase and oribtal.

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

Press `BACKSPACE` again when you get your shot to get back into the game.

## Debug Menu and Visuals

To access the debug menu, two choices `RT + Menu` on your controller or hold `Right SHIFT` or `DEL`.
The navigation is far more easier with the controller as you won't have to keep the debug menu key pressed when navigating.

To have a better LOD (Level of Details), navigate until you reach the `ENGINE` page. you should see this

<div style="width:65%; margin: auto;">
<img src="/images/BAC_06.jpg" alt="UUU v3 GUI" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

If the `Min Obj Pixels` default value is on 25.0000, lower it until you reach 0.5000 for more detailed environment.

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/BAC_04.jpg" />
  <img slot="second" src="/images/BAC_05.jpg" />
</img-comparison-slider>

By default, the MassiveLOD Distance Scale is set to 4.0000. Set it to 5.0000

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/BAC_02.jpg" />
  <img slot="second" src="/images/BAC_03.jpg" />
</img-comparison-slider>

## Some Reading
[PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Batman:_Arkham_City)
