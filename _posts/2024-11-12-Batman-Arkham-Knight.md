---
layout: post
title:  "Batman: Arkham Knight"
date:   2024-11-12 08:05:55 +0300
image:  BAK_POST.jpg
tags:   Screenshooting
---

In this explosive finale, Batman faces the ultimate threat against the city that he is sworn to protect, as Scarecrow returns to unite the super criminals of Gotham and destroy the Batman forever.

## Required
* [Console Unlocker by Sunbeam](https://www.youtube.com/watch?v=NcvzZl5vXng) - Download in the description
* [ReShade](https://reshade.me/)

## Optional
* Snacks and soda

## Installation

* Unzip and copy the d3d9.dll in your game folder where the .exe reside. Usually in `steamapps\common\Batman Arkham Knight\Binaries\Win64)`
* In `\steamapps\common\Batman Arkham Knight\DLC\356474\Content\BmGame\Config` create a new file called `bminput.ini`
* Add these lines <br />

[Engine.Console]

ConsoleKey=Tilde<br /> 
TypeKey=Backslash<br />

* Change the Console key according to your needs (optional)
* Load the game and test in the menu if you can open the console.

{% include note.html content="The console will crash your game while entering the batmobile. To avoid these, you will have to disable the NVIDIA settings Interactive smoke/fog and paper debris. "%}<br />

## How To Take A Shot

### Simple Shot

Here you have 2 choices. You use the internal photo mode with limited range. Or, you use the debug camera with an unlimited range and many more capabilities.

If you decide to use the debug camera, once in game, simply press `BACKSPACE` on your keyboard to enter in debug camera mode. 
Great thing about it is that it has 3 modes: Free, track and oribtal.

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
            <td>N/A</td>
        </tr>
        <tr>
            <td>X</td>
            <td>Reset Roll</td>
        </tr>
        <tr>
            <td>Y</td>
            <td>Teleport</td>
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
        <tr>
            <td>Tilde</td>
            <td>Console</td>
        </tr>
    </tbody>
</table>
</div>

To exit the debug camera and return to game, press `BACKSPACE`.

{% include note.html content="About H and L, pressing one of these 2 keys has an impact on the game speed and the frame advance. If you want to fine tune your shot and advance with a slower frame, use L then press A on your controller. press L again to come back to the normal game speed. Thanks Filip Cop for this trick"%}<br />

### Batmobile Motion Blur

It looks difficult but it's not. Really. Easy peasy to do. But you will need to configure ReShade first.

**ReShade**

* Configure `RealLongExposure.fx` with a delay of zero second and an exposure between 0.5 and 2 seconds.
* Assign a key to start the motion blur with ReShade UI disabled.

**In Game**

* In console, paste that command `set BmGame.RVehicleBatmobileBase ForceHeadlightsSwitchedOn 1` **!!!IMPORTANT!!!**<br />
*If you do not enter that command, the batmobile lights will be turned off as soon as you start the motion blur.*
* Enter debug camera by pressing `backspace`
* Frame your shot and enter orbital mode by pressing the right stick. **!!!IMPORTANT!!!**
* In console type `slomo 0.05`. Lower values won't work. The car won't move at all.
* In console type `playersonly`.
* Press your assigned key to start the motion blur.
* Press your assigned key to take your shot.
* In console disable the slomo by typing `slomo 1`. **!!!IMPORTANT!!!**
*If you do not disable the slomo, the game will still run at 0.05 when you come back to it*
* Press `Backspace` to disable the debug camera.

<div style="width:65%; margin: auto;">
<img src="/images/BAK_01.jpg" alt="UUU v3 GUI" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

## Interesting Console Commands
Here are some interesting console commands that can or could be used in game.

Add heavy rain. Change the amount of falling rain. Around 150000-185000 is already enough.<br />
Keep in mind that it also has an impact on the bloom when moving the camera.<br />
Execute that command in the main menu or in game followed by `|restartlevel`.<br />
`set engine.RRainComponent ParticleCount 999999`<br />

Switches on headlights of all abandoned cars.<br />
`set BmGame.RAbandonedVehicle HeadlightsSwitchedOn true`<br />

Switches on interior lights of all abandoned cars.<br />
`set BmGame.RAbandonedVehicle InteriorLightsSwitchedOn true`<br />	

Switches on AUX lights of all abandoned cars.<br />
`set BmGame.RAbandonedVehicle AuxLightsSwitchedOn true`<br />	

Switches on hazard lights of all abandoned cars.<br />
`set BmGame.RAbandonedVehicle HazardLightsSwitchedOn true`<br />	

Makes abandoned Taxis on fire.<br />
`set BmGame.RAbandonedVehicle bOnFire true`<br />

Removes Coloured Strike Trails.<br />
`set BmGame.RPersistentDebugData Debug_Combat_DisableStrikeTrails true`<br />

Removes Stun Stars above enemies when knocked down.<br />
`set BmGame.RPersistentDebugData Debug_Combat_DisableStunStars true`<br />

Remove hit marker when hitting an enemy.<br />
`set BmGame.RPersistentDebugData Debug_Combat_DisableImpactVFX 1`<br />

God Mode.<br />
`set engine.playercontroller bgodmode true`<br />


