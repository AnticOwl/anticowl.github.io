---
layout: post
title:  "Need for Speed: Payback"
date:   2024-09-08 18:05:55 +0300
image:  NFSP_POST.jpg
tags:   Screenshooting
---
Set in the underworld of Fortune Valley, you and your crew were divided by betrayal and reunited by revenge to take down The House, a nefarious cartel that rules the city’s casinos, criminals and cops. In this corrupt gambler’s paradise, the stakes are high and The House always wins.

## Required
* [Hatti NFS Payback Camera Tools](https://www.mediafire.com/file/xuwjz99rdgn72ys/CT_NFS17_20180620.rar/file)
* [ReShade 6.x](https://reshade.me/downloads/ReShade_Setup_6.2.0_Addon.exe)
* [Cheat Enhgine 7.x](https://www.cheatengine.org/downloads.php)

## How to Use
Start the game and resume where you left. Once the map is loaded, launch `NFS Payback Cinematic Tools.exe`. You will get an error saying `Unable to check for updates.`. 
Just click OK and it will continue to load. A console window will popup and after everything is loaded the GUI should be visible in game. 

<div style="width:65%; margin: auto;">
<img src="/images/NFS-01A.jpg" alt="NFS Payback Camera Tools GUI" style="box-shadow: 3px 3px 3px gray;">
</div>

Also, don't forget to apply the LOD fixes in the visuals. In this section you can also alter the time of day by clicking on `Override Time of Day` and changing it by clicking the `+` or `-`.
Manual input is also possible. 

<div style="width:65%; margin: auto;">
<img src="/images/NFS-01B.jpg" alt="Remember Me TexMod" style="box-shadow: 3px 3px 3px gray;">
</div>

For better shadows change the default value (1600) to something like `3072` or `4096`.

<div style="width:65%; margin: auto;">
<img src="/images/NFS-01C.jpg" alt="Remember Me TexMod" style="box-shadow: 3px 3px 3px gray;">
</div>

{% include note.html content="Changing the resolution scale in the tool will lead to a game crash. The camera needs to be reset at every use."%}
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
            <td>Enable/disable camera</td>
        </tr>
        <tr>
            <td>Delete</td>
            <td>Pause/unpause game</td>
        </tr>
        <tr>
            <td>Home</td>
            <td>Disable HUD</td>
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

### How To Make Motion Blur Shots

First of all, as there is no game speed option in the tool, you will have to use the Speed Hack in Cheat Engine. For this, configure two hotkeys and set the lowest key to 0.01 and the other to 1.00.
Now, configure ReShade - Real Long Exposure to something like 0.2 or 0.3 to start. Assigna keybind to start and stop it too while you are at it. As you are slowing down the game itself, it will also have an impact on the long exposure time. So, test first with these values.
So, what would be the procedure to get some nice slomo shots? Follow the guide.

* In game, press `DELETE` to pause the game.
* Press `F1` to show the tools UI. And **VERY IMPORTANT HERE** click on `Lock to player` and uncheck `Disable keyboard and mouse input` (see first print screen). `F1` again to close the UI.
* Press `HOME` to disable the game UI.
* Press `Insert` to enable the camera and frame your shot. Once done **UNCHECK** `Disable gamepad input`. This will allow you to control your car while the camera is active.
* Press your first Cheat Engine keybind to activate the slow motion then `DELETE` to unpause the game. It can take a few seconds before you see your car moving again. Control it and press the key assigned to for the Reshade real long exposure.
* Take your screenshot and Press `DELETE` again to pause the game back.
* Press your second Cheat Engine keybind to come back to the default game speed and press `INSERT` to disable the camera, `HOME` to show the GUI and `DELETE` to unpause the game.
* Continue driving your car.  
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>
<img-comparison-slider>
  <img slot="first" src="/images/NFS-02A.jpg" />
  <img slot="second" src="/images/NFS-02B.jpg" />
</img-comparison-slider>
{% include note.html content="For a better and more realistic image, it's recommended to disable the in-game motion blur."%}
