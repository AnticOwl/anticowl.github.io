---
layout: post
title:  "Borderlands GOTY Enhanced"
date:   2025-05-13 18:05:55 +0300
image:  BORDERLANDSGOTY.jpg
tags:   Screenshooting
---

Discover the original co-op shooter-looter, crammed with new enhancements! As one of 4 trigger-happy mercenaries with RPG progression, equip bazillions of guns to take on the desert planet Pandora.

## Required
* [Borderlands GOTY Enhanced cheat table](https://anticowl.github.io/files/_borderlandsgotye/BorderlandsGOTYEnhanced.CT)
* Cheat Engine 7.5 or higher
* ReShade 6.x with add-on support
* [Pause Menu Shader Toggle ini file](https://anticowl.github.io/files/_borderlandsgotye/ShaderToggler.ini)

## Optional
* Third person mode

## Installation
Install ReShade if not already done. If not start the installer. Click OK for the warning and choose you game from the list. Click `Next` twice.
Install the effects you want or click `Uncheck All` and press `Next`. Now, check the `ShaderToggler by Otis Inf`. Click next and Finish the installation.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/14b93ab3-6845-459d-bf97-49426a850899" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

If not already done, install Cheat Engine. 
Copy the `ShadderToggler.ini` file here `.\steamapps\common\BorderlandsGOTYEnhanced\Binaries\Win64` and nowhere else.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/7afe40de-92a6-4718-8f25-72e124762fa2" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

## Configuration
**This part is optional unless you want you characte in third person**
Open `WillowInput.ini` located in `C:\Users\<YOURUSERAME>\Documents\My Games\Borderlands Game of the Year\WillowGame\Config` and add the following lines at the end of `[Engine.PlayerInput]` and just before `[Engine.DebugCameraInput]`
```
Bindings=(Name="FirstPersonZoom",Command="advancedbutton bAdvancedButtonAux5",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="ThirdPersonZoom",Command="advancedbutton bAdvancedButtonAux5 | Camera FirstPerson | OnRelease Camera ThirdPerson",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="FirstPersonToggle",Command="Camera FirstPerson | setbind RightMouseButton FirstPersonZoom | setbind F1 ThirdPersonToggle",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="ThirdPersonToggle",Command="Camera ThirdPerson | setbind RightMouseButton ThirdPersonZoom | setbind F1 FirstPersonToggle",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="F1",Command="ThirdPersonToggle",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
```
Just like on the print below.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/02dbcc03-181c-43ca-b217-11abe5e20786" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

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
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
         <tr>
            <td>Page Down</td>
            <td>Enable camera structure</td>
        </tr>
        <tr>
            <td>Insert</td>
            <td>Detach and enable camera movements</td>
        </tr>
        <tr>
            <td>End</td>
            <td>Enable SloMo</td>
        </tr>
        <tr>
            <td>Delete</td>
            <td>Disable HUD</td>
        </tr>
        <tr>
            <td><br></td>
            <td><br></td>
        </tr>
        <tr>
            <td>NUMPAD 8,5,4,6</td>
            <td>Forward, backward, left and right</td>
        </tr>
        <tr>
            <td>NUMPAD 7,9</td>
            <td>Camera up and down</td>
        </tr>
        <tr>
            <td>NUMPAD 1,3</td>
            <td>Camera roll</td>
        </tr>
        <tr>
            <td>NUMPAD +,-</td>
            <td>Zoom in, out</td>
        </tr>
        <tr>
            <td>Arrow up, down</td>
            <td>Pitch up and down</td>
        </tr>
        <tr>
            <td>Arrow left, right</td>
            <td>Yaw left and right</td>
        </tr>
        <tr>
            <td><br></td>
            <td><br></td>
        </tr>
        <tr>
            <td>Left Control</td>
            <td>Fast camera movements</td>
        </tr>
        <tr>
            <td>Left ALT</td>
            <td>Slow camera movements</td>
        </tr>
    </tbody>
</table>
</div>

## How To
### Use The Cheat Table
Once you have installed Cheat Engine 7.5 or higher (if not already done), click twice on the cheat table file you downloaded. Check the `Auto Attach to Game` box. Cheat Engine will automatically connect to the game when detected.
Press `Page Down` to enable the camera structure.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/07c92f7d-0936-4589-b620-662359a128fb" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

### Take A Screenshot
This is in fact pretty simple.
* Pause the game.
* Press `Delete` to disable the HUD
* Press `Insert` to detach and activate the camera movement
* Frame, take your shot and go the other way around to get back in game.

## Resources 
[PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Borderlands:_Game_of_the_Year_Enhanced)
