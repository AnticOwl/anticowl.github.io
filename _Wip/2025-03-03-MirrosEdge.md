---
layout: post
title:  "Mirror's Edge"
date:   2025-03-03 18:05:55 +0300
image:  ME_POST.jpg
tags:   Screenshooting
---

In a city where information is heavily monitored, couriers called Runners transport sensitive data. In this seemingly utopian paradise, a crime has been committed, & you are being hunted. 
You are a Runner called Faith and this innovative first-person action-adventure is your story.

## Required
* Mirror's Edge Free Camera by IDK31.
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
Start `Mirror's Edge Tweaks` and the first thing to do is point to your game directory and choose `TdGame Fix` as your version if you care of being able to have a Cinematic Faith model.

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

![image](https://github.com/user-attachments/assets/bff46ef0-35a8-4935-ae39-90dfef2ac8f3)
![image](https://github.com/user-attachments/assets/9e65f5ee-ac8e-4eaa-9a84-0bf64573d089)
![image](https://github.com/user-attachments/assets/8288f7be-bd4f-41cc-82d3-2c3b1d77aded)








```
Bindings=(Name="F1",Command="exec cheats",Control=False,Shift=False,Alt=False)
Bindings=(Name="F1",Command="UltraGraphics",Control=True,Shift=False,Alt=False)
Bindings=(Name="F2",Command="tdpause",Control=False,Shift=False,Alt=False)
Bindings=(Name="F3",Command="FreeFlightCamera",Control=False,Shift=False,Alt=False)
```

UltraGraphics
Enable cheats first by, in console, typing `exec cheats` and then `UltraGraphics`.

LOD in Tweakers Min and Max must be like 1024 to 4096. Global like 1,0 or -1

Reshade d3d9.dll to be renamed in dinput8.dll if using mmultiplayer mod
