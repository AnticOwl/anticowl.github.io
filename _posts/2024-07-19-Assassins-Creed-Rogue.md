---
layout: post
title:  "Assassin's Creed Rogue"
date:   2024-07-19 17:04:55 +0300
image:  ACROGUE_POST.jpg
tags:   Screenshooting
---

Colder than the Caribeean seas, the North Atlantic Ocean is where Shay will forge his destiny. Cold blue toning for the icebergs, endless water and a camera to imortalize these beautiful views.

## Requirements
- Windows 10 Only
- Ubisoft Connect game version (1.1.0)
- Mod Loader ([Download Here](https://github.com/LionAG/ScriptEngine/releases/latest))

## Optional
* ReShade

## Features
- Camera control, also in cutscene (including custom roll, pitch, yaw)
- Built-in individual / panoramic screen capture 
- Save / Restore camera position
- Color correction
- More natural shadow
- Depth of Field
- Time of Day
- World Stop
- Slow Motion
- HUD Toggle
  
## Installation

- Download the loader and extract the archive to the game root folder.
- Run the GUI, click on `Add` and select the `.scrx` file.
- Click on `Run` to start the game.

Some AV software is known to block the program - you may need to add the game directory to the exclusion list.

## Image Quality and Draw Distance

Edit the `AssassinRogue.ini` located in `%USERPROFILE%\Documents\Assassin's Creed Rogue` and replace the default values by the ones below.

```
EnvironmentQuality=4
TextureQuality=4
```

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
            <th>Key</th>
            <th>Description </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>F1</td>
            <td> Toggle HUD </td>
        </tr>
        <tr>
            <td>F2</td>
            <td> Toggle world stop </td>
        </tr>
        <tr>
            <td>F3</td>
            <td> Toggle slow motion </td>
        </tr>
        <tr>
            <td>F5</td>
            <td> Reload configuration </td>
        </tr>
        <tr>
            <td>F6</td>
            <td> Reset camera to initial position </td>
        </tr>
        <tr>
            <td>F7</td>
            <td> Store camera position </td>
        </tr>
        <tr>
            <td>F8</td>
            <td> Restore camera position </td>
        </tr>
        <tr>
            <td>F9</td>
            <td> Individual capture </td>
        </tr>
        <tr>
            <td>F10</td>
            <td> Panoramic capture </td>
        </tr>
        <tr>
            <td>Delete</td>
            <td> First person view </td>
        </tr>
        <tr>
            <td>
            </td>
        </tr>
        <tr>
            <td>Numpad3</td>
            <td> Time of day forward </td>
        </tr>
        <tr>
            <td>Numpad1</td>
            <td> Time of day backward </td>
        </tr>
        <tr>
            <td>Numpad0</td>
            <td> Time of day freeze </td>
        </tr>
        <tr>
            <td>
            </td>
        </tr>
        <tr>
            <td>Home</td>
            <td> Enablef ree camera </td>
        </tr>
        <tr>
            <td>I</td>
            <td> Camera forward </td>
        </tr>
        <tr>
            <td>K</td>
            <td> Camera backward </td>
        </tr>
        <tr>
            <td>J</td>
            <td> Camera left </td>
        </tr>
        <tr>
            <td>L</td>
            <td> Camera right </td>
        </tr>
        <tr>
            <td>Space</td>
            <td> Camera up </td>
        </tr>
        <tr>
            <td>Control</td>
            <td> Camera down </td>
        </tr>
        <tr>
            <td>Numpad+</td>
            <td> Increase FOV </td>
        </tr>
        <tr>
            <td>Numpad-</td>
            <td> Decrease FOV </td>
        </tr>
        <tr>
            <td>
            </td>
        </tr>
        <tr>
            <td>End</td>
            <td> Activate rotation </td>
        </tr>
        <tr>
            <td>Numpad8</td>
            <td> Pitch up </td>
        </tr>
        <tr>
            <td>Numpad2</td>
            <td> Pitch down </td>
        </tr>
        <tr>
            <td>Numpad4</td>
            <td> Yaw left </td>
        </tr>
        <tr>
            <td>Numpad6</td>
            <td> Yaw right </td>
        </tr>
        <tr>
            <td>Numpad7</td>
            <td> Roll left </td>
        </tr>
        <tr>
            <td>Numpad9</td>
            <td> Roll right </td>
        </tr>
        <tr>
            <td>Numpad5</td>
            <td> Reset rotation to default </td>
        </tr>
        <tr></tr>
    </tbody>
</table>
</div>

## Color Corrections

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
            <th>Key </th>
            <th> Description </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ALT + NUMPAD9 </td>
            <td>Increase Hue </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD7 </td>
            <td>Decrease Hue </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD6 </td>
            <td>Increase Saturation </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD4 </td>
            <td>Decrease Saturation </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD3 </td>
            <td>Increase Brightness </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD1 </td>
            <td>Decrease Brightness </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD8 </td>
            <td>Increase Contrast </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD2 </td>
            <td>Decrease Contrast </td>
        </tr>
        <tr>
            <td>ALT + NUMPAD5 </td>
            <td>Reset </td>
        </tr>
        <tr></tr>
    </tbody>
</table>
</div>


## Custom keybinding

To customise the camera keybinding as well as various other parameters, head to:


`[game_root_directory]\ScriptEngine_Data\RTConfig`.


Configuration is stored in the file named `ACC_CameraTools.ini`.

Via this [LINK](https://cherrytree.at/misc/vk.htm) you can find the the correct key value reference.
</br>

## Notes
* Press F5 to apply changes made to the `ACC_CameraTools.ini` file.
* Keybinding cannot be empty. If you wish to disable a keybind set the value to 0. [eg. *KeyToggleFirstPersonCam = 46*. Change `46` by `0`] 
* Activating the first person view while sailing might result in a crash.
