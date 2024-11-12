---
layout: post
title:  "Batman: Arkham Knight"
date:   2024-11-13 08:05:55 +0300
image:  BAK_POST.jpg
tags:   Screenshooting
---

In this explosive finale, Batman faces the ultimate threat against the city that he is sworn to protect, as Scarecrow returns to unite the super criminals of Gotham and destroy the Batman forever.

## Required
* [Console Unlocker by Sunbeam](https://www.youtube.com/watch?v=NcvzZl5vXng) - Downlad in the description
* [ReShade](https://reshade.me/)

## Installation

* Unzip and copy the d3d9.dll in your game folder where the .exe reside. Usually in `steamapps\common\Batman Arkham Knight\Binaries\Win64)`
* In `\steamapps\common\Batman Arkham Knight\DLC\356474\Content\BmGame\Config` create a new file called `bminput.ini`
* Add these lines 
```
[Engine.Console]

ConsoleKey=Tilde
TypeKey=Backslash
```
* Change the Console key according to your needs (optional)
* Load the game and test in the menu if you can open the console.

{% include note.html content="The console will crash your game while entering the batmobile. To avoid these, you will have to disable the nVidia settings Interactive smoke/fog and paper debris. "%}

## How To Take A Shot

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



