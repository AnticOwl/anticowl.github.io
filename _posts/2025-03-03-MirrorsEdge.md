---
layout: post
title:  "Mirror's Edge"
date:   2025-03-10 18:05:55 +0300
image:  ME_POST.jpg
tags:   Screenshooting
---

In a city where information is heavily monitored, couriers called Runners transport sensitive data. In this seemingly utopian paradise, a crime has been committed, and you are being hunted. 
You are a Runner called Faith and this innovative first-person action-adventure is your story.

## Required
* [Mirror's Edge Tweaker by softsoundd](https://www.moddb.com/games/mirrors-edge/addons/persistent-fov)
* [Mirror's Edge Multiplayer Mod (Ady Endre GitHub Fork)](https://github.com/AdyStudios/mmultiplayer/releases) and [Launcher](https://github.com/LucasOe/mmultiplayer/releases/download/2.3.2/Launcher.exe) 

## Optional
* [Native Motion Blur](https://www.moddb.com/games/mirrors-edge/addons/native-motion-blur)
* [Rain Mod by keku](https://www.moddb.com/games/mirrors-edge/addons/rainy-mod)
* [ReShade](https://reshade.me)

## Installation
For the multiplayer mod, download `Launcher.exe` and `mmultiplayer.dll` and move them into your game directory. Usually `\steamapps\common\mirrors edge\Binaries`. Where `MirrorsEdge.exe` resides.
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

{% include note.html content="If you use the Steam version starting the game from the tweaker will result in a startup crash. Disabling the DoF automatically disable the Bloom as they are tied. If you are playing with headphones I suggest you update the OpenAL Soft (first button)."%}
<p></p>
### Keybinds and Ultra Graphics
You will need to add some keybinds to take advantage of the Ultra Graphics and the availables cheats. For this, go to `C:\Users\<YourUserName>\Documents\EA Games\Mirror's Edge\TdGame\Config` and uncheck the `Read Only` flag first. Edit TdInput.ini and add these lines just underneath `[Engine.PlayerInput]`. Save the file and set the file back to `Read Only`.
```
Bindings=(Name="F1",Command="exec cheats",Control=False,Shift=False,Alt=False)
Bindings=(Name="F1",Command="UltraGraphics",Control=True,Shift=False,Alt=False)
Bindings=(Name="F2",Command="set DOFEffect bAutoFocus 0 | set DOFEffect MaxFarBlurAmount 0",Control=False,Shift=False,Alt=False)
Bindings=(Name="F3",Command="FreezeWorld",Control=False,Shift=False,Alt=False)
Bindings=(Name="F4",Command="GameSpeed 0.1",Control=False,Shift=False,Alt=False)
Bindings=(Name="F4",Command="GameSpeed 0.3",Control=True,Shift=False,Alt=False)
Bindings=(Name="F4",Command="GameSpeed 1.0",Control=False,Shift=True,Alt=False)
```

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
            <td>F1</td>
            <td>Enable cheats</td>
        </tr>
        <tr>
            <td>CTRL+F1</td>
            <td>Enable highest graphics available</td>
        </tr>
        <tr>
            <td>F2</td>
            <td>Disable the depth of field but leave the bloom active</td>
        </tr>
        <tr>
            <td>F3</td>
            <td>Freeze everything beside yourself</td>
        </tr>
        <tr>
            <td>F4</td>
            <td>Set games speed at 1/10 of the normal game speed</td>
        </tr>
        <tr>
            <td>CTRL+F4</td>
            <td>Set games speed at 3/10 of the normal game speed</td>
        </tr>
        <tr>
            <td>SHIFT+F4</td>
            <td>Set games speed at normal game speed</td>
        </tr>
    </tbody>
</table>
</div>

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>
The `exec cheats` **MUST** be activated before being able to use the `UltraGraphics`, `GameSpeed` and `FreezeWorld`.  

Image comparison with in-game setting at highest values and Ultra Graphics.
<img-comparison-slider>
  <img slot="first" src="/images/ME_01A.jpg" />
  <img slot="second" src="/images/ME_01B.jpg" />
</img-comparison-slider>

## MMultiplayer for Screenshots 
This mod is not "just" adding support for multiplayer. It's much more than that. You can by example disable part of the scene, disable the lighting, have track recording with nodes, etc. We will focus on the `Dolly` part here for the sake of screenshotting and video clip recording. 

Start `Launcher` from the `\steamapps\common\mirrors edge\Binaries` folder and then start the game via Steam. You should see the interface when the game is started.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/d2dd4e41-a927-4627-a7ea-9dd87962732b" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

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
    <caption><br></caption>
    <thead>
        <tr>
            <th>Key</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>W, A, S, D</td>
            <td>Forward, backward, left and right</td>
        </tr>
        <tr>
            <td>Shift</td>
            <td>Camera lift down</td>
        </tr>
        <tr>
            <td>Space</td>
            <td>Camera lift up</td>
        </tr>
        <tr>
            <td>Mouse</td>
            <td>Yaw and tilt</td>
        </tr>
        <tr>
            <td>Numpad +</td>
            <td>FOV increase</td>
        </tr>
        <tr>
            <td>Numpad -</td>
            <td>FOV decrease</td>
        </tr>
        <tr>
            <td>Arrow up</td>
            <td>Roll increase</td>
        </tr>
        <tr>
            <td>Arrow down</td>
            <td>Roll decrease</td>
        </tr>
        <tr>
            <td>F5</td>
            <td>Add marker</td>
        </tr>
        <tr>
            <td>F6/CTRL+F6 </td>
            <td>Jump/Jumpback frame</td>
        </tr>
        <tr>
            <td>F7</td>
            <td>Start/stop recording</td>
        </tr>
        <tr>
            <td>F9</td>
            <td>Play/stop recording</td>
        </tr>
    </tbody>
</table>
</div>

{% include note.html content="All the controls can be customised via the in game settings and/or the MMultiplayer. `Force Roll` must be enable for the roll to work."%}

### In Flight 

Let say you want to take a shot of Faith jumping from one roof to another. You will need to use the `Dolly` option from `MMultiplayer` to accomplish this. The great thing here is you won't need to add markups. So, to do so, follow these steps:

* Press `F7` to start the recording.
* Start running and make your jump.
* Press `F7` again to stop the recording.
* Press `2` to activate the freecam.
* Press `F9` twice and then press `Insert` to open the Dolly interface.
* Move the cursor on the `Timeline` until you get the correct pose.
* Frame your shot, capture it and disable the free camera.
* Get back to your initial position and press `2`.
* Delete the recording and resume your play.

With this techique you will now be able to finally take shots of Faith in flight. 
<div style="width:65%; margin: auto;">
<img src="/images/ME_02.jpg" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

### Static 

* Press `F7` to start the recording.
* Take the pose.
* Press `F7` again to stop the recording.
* Press `2` to activate the freecam.
* Press `F9` twice
* Frame and take your shot
* Get back to your initial position and press `2`.
* Delete the recording and resume your play.

<div style="width:65%; margin: auto;">
<img src="/images/ME_03.jpg" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>


### Action
This one is a little bit more complicated and will involve taking some time to perfect it. The most important thing here is that the cheats **must** be active.

* Press `F7` to start the recording.
* Do your stuff like in a movie.
* Press `F7` again to stop the recording.
* Press `F3` to freeze the world beside your character.
* Open the console by pressing `~` or `CTRL+TAB`.
* Type `GOD` **IMPORTANT**
* Press `F3` again to unfreeze. If you are being shot at, cut the sound.
* Press `2` to activate the flycam
* Press `F9` twice followed by `Insert` to open the interface.
* Move the cursor on the `Timeline` until you get the correct pose and move around to frame your shot.
* REMEMBER THE POSITION!!!
* Open the console again and recall the `GOD` command with the `Arrow Up`.
* DIE (I am not even joking)!
* Do a rerun until a bit before you reach the point you started the recording.
* At this point you should see your character frozen!! 
* Press `F3` to freeze the world and press `F4` to enter slow motion.
* Press `2` to enter flycam and move at your frozen character.
* Press `F3` again to unfreeze the scene.
* If you are being shot at behind glass, wait until you have it flying around and press `F3` again to freeze the whole scene.
* Position yourself again where you wanted the camera to be.
* Take your shot.

<div style="width:65%; margin: auto;">
<img src="/images/ME_04.jpg" alt="Advanced Launcher" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

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
        <tr>
            <td>set primitivecomponent bownernosee 1/0</td>
            <td>Make Faith visible or invisible</td>
        </tr>
        <tr>
            <td>set tdmotionblurpostprocess tdmotionblurenabled 1/0</td>
            <td>Enable/disable motion blur</td>
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
Many thanks to softsoundd and Ady Endre for their help! 
