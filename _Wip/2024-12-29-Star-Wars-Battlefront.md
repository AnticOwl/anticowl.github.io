---
layout: post
title:  Star Wars Battlefront
date:   2024-07-19 15:01:35 +0300
image:  SWBF_POST.jpg
tags:   Screenshooting
---

Engage in epic battles on iconic planets including Hoth, Endor, and Tatooine. Also, bring the fight to the previously unexplored planet, Sullust. Command a diverse set of ground-based vehicles including nimble speeder bikes, massive AT-ATs, and more.

## Required

* [Star Wars Battlefront Cinematic Tool by Hatti Watti](https://www.mediafire.com/file/4axk4e12cw8wn9z/CT_SWBF_20170119-8fa295.rar/file)
* [ReShade](https://reshade.me/downloads/ReShade_Setup_6.3.3.exe)

## How to Use
Start the game and resume where you left. Once the map is loaded, launch `SWBF Cinematic Tools.exe`. You will get an error saying `Unable to check for updates.`. 
Just click OK and it will continue to load. The tool GUI and a console window will popup. Click on `FIX LOD` for better in game details.

<div style="width:65%; margin: auto;">
<img src="/images/SWBF-01.jpg" alt="NFS Payback Camera Tools GUI" style="box-shadow: 3px 3px 3px gray;">
</div>

The ENVIRONMENT tab allows you to control the color correction, DOF, Tonemap and vignette
<div style="width:65%; margin: auto;">
<img src="/images/SWBF-02.jpg" alt="NFS Payback Camera Tools GUI" style="box-shadow: 3px 3px 3px gray;">
</div>

The MISC / ABOUT has some small things like Shadow Map Size (change it to 4096 for better shadows), Resolution Scale and Game Timescale that will be later useful.
<div style="width:65%; margin: auto;">
<img src="/images/SWBF-03.jpg" alt="NFS Payback Camera Tools GUI" style="box-shadow: 3px 3px 3px gray;">
</div>

If a a moment or another you would like to make usage of lights, click on `More Tools` and ... TADA!! 

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
            <td>Insert</td>
            <td>Enable/ disable camera</td>
        </tr>
        <tr>
            <td>Delete</td>
            <td>Pause/ unpause game</td>
        </tr>
        <tr>
            <td>Home</td>
            <td>Disable HUD</td>
        </tr>
        <tr>
            <td>Left stick</td>
            <td>Move camera forward/ backwards/ left/ right</td>
        </tr>
        <tr>
            <td>Right stick</td>
            <td>Pan and yaw</td>
        </tr>
        <tr>
            <td>RB/LB</td>
            <td>Roll left/ right</td>
        </tr>
        <tr>
            <td>RT/LT</td>
            <td>Move camera up/ down</td>
        </tr>
        <tr>
            <td>RS/LS down</td>
            <td>Increase/ decrease FOV</td>
        </tr>
    </tbody>
</table>
</div>

### How To Make Motion Blur Shots

You will need to configure ReShade - Real Long Exposure to something like 0.7 or 4.5 seconds. Assigna keybind to start and stop it too while you are at it. This time, no Cheat Engine needed so, you won't aaffect the game slow motion.
So, what would be the procedure to get some nice slomo shots? Follow the guide.

* In game, press `DELETE` to pause the game.
* Press `HOME` to disable the game UI.
* Press `Insert` to enable the camera.
* ALT-TAB to show the tools UI. And **VERY IMPORTANT HERE** click on `Lock to player` and ALT-TAB back to game.
* Frame your shot.
* ALT-TAB again. Uncheck `DISABLE GMAEPAD INPUT` to allow you to control your ship if needed. Go to the `MISC / ABOUT` tab. There, change the game timescale to a value that is like `0.003` to `0.01` (you choice).
* Quickly ALT-TAB to the game again and move your ship like you would like to have it.
* Press the `Real Long Exposure` key or control your ship until you see it's a good shot.
* Take your screenshot and Press `INSERT`, `HOME` and `DELETE` to go back to normal.
{% include note.html content="If you changed the FOV, you will need to type `-1` back in the `CAMERA` Tab"%}

