---
layout: post
title:  "Hitman: Absolution"
date:   2025-01-27 18:40:00 +0100
image:  HMA_POST.jpg
tags:   Screenshooting
---

Hitman: Absolution follows the Original Assassin undertaking his most personal contract to date. 
Betrayed by the Agency and hunted by the police, Agent 47 finds himself pursuing redemption in a corrupt and twisted world.

## Required
[Hitman: Absolution SDK by Pavle](https://github.com/pavledev/HitmanAbsolutionSDK/releases)

## Optional
[ReShade](https://reshade.me)

## Installation
Simply unzip the content in the game root directory. 

## Configuration
Start the game. You will see a console window popping up and the launcher appearing. Press Play. 
<div style="width:65%; margin: auto;">
<img src="/images/HMA_02.jpg" alt="Console Window HMA" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>
When at the menu, load a save. press the `~` or `²` on your keyboard to open the SDK.
Click on `MODS` and check the ones you would like to use. Press OK when done. They should be displayed in the SDK menu bar.

<div style="width:65%; margin: auto;">
<img src="/images/HMA_01.jpg" alt="MODS Hitman SDK" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>

The `Camera` mod will allow you to completely disable the internal post proccessing and change the default game FOV.
<div style="width:65%; margin: auto;">
<img src="/images/HMA_03.jpg" alt="MODS Hitman SDK" style="box-shadow: 3px 3px 3px gray;">
</div>
<p></p>

The `Editor` mod will allow you to change the LOD, enable or disable parts of the scene, move and modify lights and many more other things.

![image](https://github.com/user-attachments/assets/4d9a12e6-e089-416d-8ca9-e2ac9bf38bb3)

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
    <caption><br></caption>
    <thead>
        <tr>
            <th>Key</th>
            <th>Effect</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>K</td>
            <td>Enable/Disable Free Camera</td>
        </tr>
        <tr>
            <td>B+R</td>
            <td>Increase/Decrease Camera Speed</td>
        </tr>
        <tr>
            <td>LS</td>
            <td>Forward/Backward/Left/Right</td>
        </tr>
        <tr>
            <td>RS</td>
            <td>Pan/Tilt</td>
        </tr>
        <tr>
            <td>A+LS</td>
            <td>Roll Camera</td>
        </tr>
        <tr>
            <td>Y+LS</td>
            <td>Change FOV</td>
        </tr>
        <tr>
            <td>LB</td>
            <td>Lock Camera and Enable 47 Input</td>
        </tr>
        <tr>
            <td>RT (HOLD)</td>
            <td>Faster Camera Movements</td>
        </tr>
        <tr>
            <td>LT+RS</td>
            <td>Camera Lift Up/Down</td>
        </tr>
        <tr>
            <td>A+LS (Press)</td>
            <td>Reset Roll</td>
        </tr>
        <tr>
            <td>F9</td>
            <td>Kill NPC</td>
        </tr>
        <tr>
            <td>CTRL+F9</td>
            <td>Teleport 47 To Camera</td>
        </tr>
        <tr>
            <td>F8</td>
            <td>Enable/Disable HUD</td>
        </tr>
        <tr>
            <td>F10</td>
            <td>Pause/Unpause Game and Activate/Deactivate Free Camera</td>
        </tr>
        <tr>
            <td>F11</td>
            <td>Pause/Unpause Game</td>
        </tr>        
    </tbody>
</table>
</div>

## How to Take A Screenshot
This one is quite simple. Once the game loaded and your level loaded, press `F11` to pause the game and the `K` to activate the camera.
Alternatively, you can press `F10` to do both.
<p></p>
Once done, pres `F10` to come back to the game.

### About ReShade and HUD
rename dxgi.dll to d3d11.dll to avoid the SDK to no load correctly. The HUD mod needs to be loaded for the keybind to work.
