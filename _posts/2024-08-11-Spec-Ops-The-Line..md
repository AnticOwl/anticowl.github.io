---
layout: post
title:  "Spec Ops: The Line"
date:   2024-08-11 18:05:55 +0300
image:  SOTL_POST.jpg
tags:   Screenshooting
---
What about you and your team are sent in recognition and end up in the most messed up situation possible. This, in a now destroyed Dubai where sand storms are becoming typical.

## Required
* [Free Camera and Effects](https://www.moddb.com/games/spec-ops-the-line/downloads/sotl-camera-effect-binds)

## Optional
* Reshade 
* [Spec Ops: The Line INI Decrypt/Encrypt Tool](https://www.moddb.com/games/spec-ops-the-line/downloads/spec-ops-the-line-ini-decryptencrypt-tool)

## Installation
Place the file in `Documents\My Games\SpecOps-TheLine\SRGame\Config`. Be sure to backup the original one before you overwrite it.

## Commands
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
            <td>F2</td>
            <td>Enable/Disable HUD</td>
        </tr>
        <tr>
            <td>F3</td>
            <td>Free Camera</td>
        </tr>
        <tr>
            <td>F5</td>
            <td>Spectator Camera</td>
        </tr>
        <tr>
            <td>F6</td>
            <td>Attached to Player (Look At)</td>
        </tr>
        <tr>
            <td>F7</td>
            <td>Attached to Player&nbsp;</td>
        </tr>
        <tr>
            <td>F8</td>
            <td>Top View</td>
        </tr>
        <tr>
            <td>F9</td>
            <td>Reset</td>
        </tr>
        <tr>
            <td>F10</td>
            <td>Hide Animations</td>
        </tr>
        <tr>
            <td>F11</td>
            <td>Enable/Disable Fog</td>
        </tr>
        <tr>
            <td>F12</td>
            <td>Enable/Disable Post Process</td>
        </tr>
        <tr>
            <td>Page Up</td>
            <td>FoV 70</td>
        </tr>
        <tr>
            <td>Page Down</td>
            <td>FoV 90</td>
        </tr>
        <tr>
            <td>Home</td>
            <td>FoV 110</td>
        </tr>
    </tbody>
</table>
</div>
  
## How To Add Other FoV Values
To do so, unzip the [Spec Ops: The Line INI Decrypt/Encrypt Tool](https://www.moddb.com/games/spec-ops-the-line/downloads/spec-ops-the-line-ini-decryptencrypt-tool) in `\Documents\My Games\SpecOps-TheLine\SRGame\Config`.
Once done, drag and drop the `SRInput.ini` on `Gibbed.SpecOpsTheLine.IniDecrypt.exe`. Your file is now decrypted. Open it with Notepad++ and add the lines below just before `[IniVersion]`.

```
Bindings=(Name="NumPadFour",Command="FOV 20")
Bindings=(Name="NumPadFive",Command="FOV 30")
Bindings=(Name="NumPadSix",Command="FOV 40")
Bindings=(Name="NumPadSeven",Command="FOV 50")
Bindings=(Name="NumPadEight",Command="FOV 60")
Bindings=(Name="NumPadNine",Command="FOV 80")
```

When finished, save the file and drag it on `Gibbed.SpecOpsTheLine.IniEncrypt.exe` to encrypt it back.

## Resources
* [PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Spec_Ops%3A_The_Line)
* [How to enable Anti-Aliasing in Spec Ops: The Line](https://steamcommunity.com/sharedfiles/filedetails/?id=567778402)
