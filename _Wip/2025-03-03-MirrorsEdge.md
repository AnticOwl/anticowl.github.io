---
layout: post
title:  "Mirror's Edge"
date:   2023-12-12 18:05:55 +0300
image:  ME_POST.jpg
tags:   Screenshooting
---

In a city where information is heavily monitored, couriers called Runners transport sensitive data. In this seemingly utopian paradise, a crime has been committed, and you are being hunted. 
You are a Runner called Faith and this innovative first-person action-adventure is your story.

## Required
* Mirror's Edge Free Camera by IDK31
* [Mirror's Edge Tweaker by softsoundd](https://www.moddb.com/games/mirrors-edge/addons/persistent-fov)
* [Mirror's Edge Multiplayer Mod](https://github.com/LucasOe/mmultiplayer/releases)

## Optional
* [Native Motion Blur](https://www.moddb.com/games/mirrors-edge/addons/native-motion-blur)
* [Rain Mod by keku](https://www.moddb.com/games/mirrors-edge/addons/rainy-mod)
* [ReShade](https://reshade.me)

## Installation
For the multiplayer mod, download `Launcher.exe` and `mmultiplayer.dll` and move them into your game directory. No need of the `mirrors-edge-multiplayer-2.3.2.exe` that is in fact the launcher and dll installer.
If you prefer that way you will find the launcher in your start menu. 
<p></p>
Download and extract the tweaker in your game directory. 

## Configuration
### Mirror's Edge Tweaks
The last softsoundd release will do everything for you. No need to download the exe patcher, ini tweaks (beside the ones a bit further) or anything like that.  
Start `Mirror's Edge Tweaks` and the first thing to do is point to your game directory and choose `TdGame Fix` as your version if you care of being able to have a Cinematic Faith model. You will only have to do this once. 

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/9fb5066e-24bc-48ed-8568-73721a17d310" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

Apply the `Console` and `Mod` patches, install the `Cheats and trainer` and have your fps and PhysX fps capped at the same value. Very very very important for later. 
<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/5f9be333-261b-4f52-828b-0719d6b919c8" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

For the Graphic Tweaks, it's up to you. Just one thing: do not set the anti aliasing to 16xQ! It's not supported anymore on NVIDIA cards. Your game won't start if you do so.
<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/bff46ef0-35a8-4935-ae39-90dfef2ac8f3" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

Enable `HQ dynamic shadows` and set Texture management to `Modern` for a better and smooth texture display. Leave or change the LOD. Your choice. 
<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/9e65f5ee-ac8e-4eaa-9a84-0bf64573d089" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>


Last, enable the Cinematic Faith model and you are done with the tweaks. 
<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/8288f7be-bd4f-41cc-82d3-2c3b1d77aded" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

{% include note.html content="If you use the Steam version starting the game from the tweaker will result in a startup crash. Disablind the DoF automatically disable the Bloom as they are tied."%}

### Keybinds and Ultra Graphics
You will need to add some keybinds to take advantage of the Ultra Graphics and the availables cheats. For this, go to `C:\Users\<YourUserName>\Documents\EA Games\Mirror's Edge\TdGame\Config` and uncheck the `Read Only` flag first. Edit TdInput.ini and add these lines just underneath `[Engine.PlayerInput]`. Save the file and set the file back to `Read Only`.
```
Bindings=(Name="F1",Command="exec cheats",Control=False,Shift=False,Alt=False)
Bindings=(Name="F1",Command="UltraGraphics",Control=True,Shift=False,Alt=False)
Bindings=(Name="F2",Command="set DOFEffect bAutoFocus 0 | set DOFEffect MaxFarBlurAmount 0",Control=False,Shift=False,Alt=False)
Bindings=(Name="F3",Command="FreeFlightCamera",Control=False,Shift=False,Alt=False)
Bindings=(Name="F4",Command="GameSpeed 0.01",Control=False,Shift=False,Alt=False)
Bindings=(Name="F4",Command="GameSpeed 0.1",Control=True,Shift=False,Alt=False)
Bindings=(Name="F4",Command="GameSpeed 1.0",Control=False,Shift=True,Alt=False)
Bindings=(Name="F5",Command="FreezeWorld",Control=False,Shift=False,Alt=False)
```
The `exec cheats` **MUST** be activated before being able to use the `UltraGraphics`, `GameSpeed` and `FreezeWorld`. So, press F1 first, the level will reload and then press CTRL+F1 to activate the grpahic tweak.

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/ME_01A.jpg" />
  <img slot="second" src="/images/ME_01B.jpg" />
</img-comparison-slider>

## What is MMultiplayer
This mod is not "just" adding support for multiplayer. It's much more than that. You can by example disable part of the scene, disable the lighting, have track recording with nodes, etc. We will focus on the `Dolly` part here for the sake of screenshotting and video clip recording. 
![image](https://github.com/user-attachments/assets/d22f682d-c12e-4252-80a1-d787c7fb5705)

### In Flight Screenshotting

Let say you want to take a sot of Faith jumping from one roof the another. You will need to use the `Dolly` option from `mmultiplayer` to accomplish this. Keep in mind that the count is made in frames and not in seconds. But here, it has not much importance. So, to do so, follow these steps:

#### The Recording
* Press `F9` to start the recoding.
* Start running and make you jump.
* Press `F9` again to stop the recording.

#### Play the Recording
* Press `2` to activate the freecam.
* Press `F9` twice and then press `Insert` to open the Dolly interface.
* Move the cursor on the `Timeline` until you get the correct pose.
* Frame your shot, capture it and disable the free camera.
* Get back to your initial position and press `2`.
* Delete the recording and resume your play.

With this techique you will now be able to finally take shots of Faith in flight. 

### Clip Recording

## Some Interesting Commands
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
            <th>Command</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ToggleOcclusions</td>
            <td>Enable/disable ambient occlusions</td>
        </tr>
        <tr>
            <td>ToggleDynamicContrast</td>
            <td>Enable/disable tone mapping and curves</td>
        </tr>
        <tr>
            <td>show lensflares</td>
            <td>Enable/disable lens flares&nbsp;</td>
        </tr>
        <tr>
            <td>scale toggle TdSunHaze</td>
            <td>Enable/disable sun haze</td>
        </tr>
    </tbody>
</table>
</div>

## About Reshade
If you installed the `mmultiplayer` mod, and if reshade is installed, the game will not start correctly. For this, you will need to rename `d3d9.dll` to `dinput8.dll`.
You will then be able to use ReShade in conjunction with the multiplayer mod.


## Resources
* [PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Mirror%27s_Edge#:~:text=Mirror%27s%20Edge%20is%20a%20sci,title%20began%20full%2Dscale%20production.)
* [Mirror's Edge Various Tweaks and QOL Mods](https://docs.google.com/document/d/10D4a3mbhmcOR08EgqD59pSLqT3JcAZX_3FeExK_FqKc/preview?tab=t.0#heading=h.u0or801068b4)
<p></p>
Many thanks tyo softsoundd and Ady Endre for their help! 
