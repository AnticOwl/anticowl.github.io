---
layout: post
title:  "WATCH_DOGS (WIP)"
date:   2024-07-20 18:05:55 +0300
image:  WD_POST.jpg
tags:   Screenshooting
---

Be the hacker. Or, sort of. It's mostly be the vigilante. Thanks to Sad_Gamers great work on the camera, and some mods to make the game even more attractive, you will see WATCH_DOGS like you never saw it.   

## Required
* [Sad_Gamers Ultimate Camera Tool](https://www.nexusmods.com/watchdogs/mods/258)

## Optional
* [EPIC MOD PACK](https://www.nexusmods.com/watchdogs/mods/269)
* ReShade
  
## Installation

Unzip the camera tool in the `Watch_Dogs\bin` directory. thats where the `Watch_Dogs.exe` resides.
Once done, you are good to go and you can start playing and shooting.

## The Tool

### Camera
<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu-Camera.jpg" alt="WATCH_DOGS UTC Camera Menu" style="box-shadow: 3px 3px 3px gray;">
</div>
2 modes available: Unbounded and Look At Player

### Unbounded A.K.A Free Camera

This mode let you freely move the camera around
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
            <th>Keys</th>
            <th> Movements </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Arrow Up</td>
            <td> Move Forward </td>
        </tr>
        <tr>
            <td>Arrow Down</td>
            <td> Move Backward </td>
        </tr>
        <tr>
            <td>Arrow Left</td>
            <td> Move Left </td>
        </tr>
        <tr>
            <td>Arrow Right</td>
            <td> Move Right </td>
        </tr>
        <tr>
            <td>Page Up</td>
            <td> Lift Up </td>
        </tr>
        <tr>
            <td>Page Down</td>
            <td> Lift Down </td>
        </tr>
        <tr>
            <td>Mouse</td>
            <td> Tilt and Pan </td>
        </tr>
        <tr>
            <td>Numpad 7</td>
            <td> Roll Left </td>
        </tr>
        <tr>
            <td>Numpad 4</td>
            <td> Reset Roll </td>
        </tr>
        <tr>
            <td>Numpad 1</td>
            <td> Roll Right </td>
        </tr>
        <tr>
            <td>Numpad 9</td>
            <td> Decrease FOV </td>
        </tr>
        <tr>
            <td>Numpad 6</td>
            <td> Reset FOV </td>
        </tr>
        <tr>
            <td>Numpad 3</td>
            <td> Increase FOV</td>
        </tr>
    </tbody>
</table>
</div>

### Look At Player

This mode will attach the camera to the player. Whatever on foot or in/on a vehicle

{% include note.html content="The Transitions and Lights tabs will only appear when the camera is active.
The DOF (Depth Of Field) isn't useable while in gameplay mode."%}
### Transitions

<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu-Transition.jpg" alt="WATCH_DOGS UTC Transitions Menu" style="box-shadow: 3px 3px 3px gray;">
</div>

This can be useful if you decide to make some short videos.  

### Lights
<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu-Lights.jpg" alt="WATCH_DOGS UTC Camera Menu" style="box-shadow: 3px 3px 3px gray;">
</div>

This is ideal for portraits in low light like night or evening times. 3 type of light temperatures are available: white, warm and cool.

## World
<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu-World.jpg" alt="WATCH_DOGS UTC Camera Menu" style="box-shadow: 3px 3px 3px gray;">
</div>

This is where you can change weather and time. 

## Player
<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu-Player.jpg" alt="WATCH_DOGS UTC Camera Menu" style="box-shadow: 3px 3px 3px gray;">
</div>

In this tab, you can swap Aiden with any other main character or even NPC.
Tha animation / Poses section allow you to play quite a lot of different animation or poses like standing against a wall, looking at, etc.

## Actor
<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu-Actor.jpg" alt="WATCH_DOGS UTC Camera Menu" style="box-shadow: 3px 3px 3px gray;">
</div>

Here, you can spawn any character available in the game, give them a pose or animate and place them wherever you want. 

## Rendering
This section will allow you to modifiy the LOD, Anti Aliasing, Shadow and texture map fot the water.
If you have a graphic card with enough VRAM, you can activate the `Super Render`. This will maximize the detail and render twice your actual resolution internally.
This means that if your 

<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu_Rendering.jpg" alt="WATCH_DOGS UTC Rendering Menu" style="box-shadow: 3px 3px 3px gray;">
</div>

Below, two examples with and without "Super Render".
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/WD_SR-Before.jpg" />
  <img slot="second" src="/images/WD_SR-After.jpg" />
</img-comparison-slider>

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/WD_SR-Before2.jpg" />
  <img slot="second" src="/images/WD_SR-After2.jpg" />
</img-comparison-slider>

## Configure
<div style="width:65%; margin: auto;">
<img src="/images/WD_Menu-Conf.jpg" alt="WATCH_DOGS UTC Camera Menu" style="box-shadow: 3px 3px 3px gray;">
</div>

Self explicit. Here you can change your keybinds. Or at least the ones thare are not fix.
The fixes section includes mods previously separately available from the camera author. enable or desactivate them at will.

## How To

### Motion Blur Shots

Required: ReShade and Real Long Exposure shader configured at like 0.2-0.4 seconds with a start shortcut key.

- Press F5 to pause the game and F4 to hide the HUD.
- Activate the camera by pressing Home then Insert to show the UCT GUI.
- Change the mode to Look At Player. The camera will be positioned attached to back back of the vehicule.                 
- Press Static Angles.
- Change the angles to your preferences in the Ideal Position Offset.
  First box is for horizontal axe, second is he depth, and third vertical.
- Change the angles to your preferences in the Ideal Angle Offset.
  First box is for tilt, second is roll, and third pan.
- Start the game back but in slow motion by pressing F6.
- Press your assigned shortcut to start the long exposure. 
- Press Print Screen to save your shot.
- Press your long exposure shortcut, disable the camera and press F6 to return to the game normal speed.

*Note:* 
*Tilt, roll and pan are orbital when in Look At Player mode.*
*For better image quality you can also use Cheat Engine Speed Hack when the tool Slomo is active.*

Example

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/assets/images/UCT-02.png" />
  <img slot="second" src="/assets/images/UCT-03.png" />
</img-comparison-slider>
