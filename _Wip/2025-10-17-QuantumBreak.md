---
layout: post
title:  "Quantum Break"
date:   2025-10-17 00:05:55 +0300
image:  QB_POST.jpg
tags:   Screenshooting
---

From Remedy Entertainment, the masters of cinematic action games, comes Quantum Break, a time-amplified suspenseful blockbuster. The Quantum Break experience is part game, part live action show—where decisions in one dramatically affect the other.

## Required
* [Hatti Watti Camera Tool](https://www.mediafire.com/file/63a2cpfs46gzefn/CT_QuantumBreak_20181024.rar/file)
* [Quantum Break game patches with dev menu](https://github.com/illusion0001/Windows-Game-Patches/releases/tag/1.0.201-0349c14b%2B910-branch-main) (download the file named Windows-Game-Patches-1.0.201-0349c14b+910-branch-main.7z
)

## Optional 
* [ReShade](https://reshade.me)

## Installation
* Rename original bink2w64.dll in game dx11 folder to bink2w64Hooked.dll for ASI Loader.
* Extract dinput8.dll from zip !ASI_Loader_x64 and rename to bink2w64.dll and copy to game dx11 folder.
* Extract QuantumBreak.Patches.asi to game dx11 folder.
* Run game once to generate ini and close it.
* Enable config for desried patches (QuantumBreak.Patches.ini).
```
[Settings]
bDisableStartupLogo = true
bEnableDevMenu = true
bDisablePauseGameOnFocusLoss = true
```

## Controls
### Hatti Watti Camera Tool
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
            <td>Insert</td>
            <td>Enable/disable camera</td>
        </tr>
        <tr>
            <td>Delete</td>
            <td>Pause/unpause game</td>
        </tr>
        <tr>
            <td>Home</td>
            <td>Disable/Enable HUD</td>
        </tr>
        <tr>
            <td>End</td>
            <td>Disable/Enable Tool UI</td>
        </tr>
        <tr>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Left stick</td>
            <td>Move camera forward/backwards/left/right</td>
        </tr>
        <tr>
            <td>Right stick</td>
            <td>Pan and yaw</td>
        </tr>
        <tr>
            <td>RB/LB</td>
            <td>Roll left/right</td>
        </tr>
        <tr>
            <td>RT/LT</td>
            <td>Move camera up/down</td>
        </tr>
        <tr>
            <td>RS/LS down</td>
            <td>Increase/decrease FOV</td>
        </tr>
    </tbody>
</table>
</div>

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
            <td>F1</td>
            <td>Display console</td>
        </tr>
        <tr>
            <td>F2</td>
            <td>Pause</td>
        </tr>
        <tr>
            <td>F3</td>
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
            <td>Right Control</td>
            <td>Fast camera movements</td>
        </tr>
        <tr>
            <td>Left ALT</td>
            <td>Slow camera movements</td>
        </tr>
    </tbody>
</table>
</div>
