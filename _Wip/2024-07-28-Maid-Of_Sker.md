---
layout: post
title:  "Maid Of Sker"
date:   2024-07-28 13:55:55 +0300
image:  MOS_POST.jpg
tags:   Screenshooting
---

Now the Originalnicodr release his last version of his Cinematic Unity Explorer, it is even easier than before to shot some of these marvelous Unity games.
Maid of Sker is one of them.

## Required
* [Melon Loader 0.5.7](https://github.com/HerpDerpinstine/MelonLoader/releases/latest/download/MelonLoader.Installer.exe)
* [Cinematic Unity Explorer v 1.2.0  - IL2CPP](https://github.com/originalnicodr/CinematicUnityExplorer/releases/latest/download/CinematicUnityExplorer.MelonLoader.IL2CPP.zip)

## Optional
* Reshade

## Installation

### Melon Loader Installation
Start Melon Loader installer and uncheck `Latest`. Click on triangle in the `Version` field and choose 0.5.7
Click on `Select` and point to your game installation directory. Choose `Maid of Sker.exe` and click `Open`.
Back to Melon Loader installer, click `Install`

### Cinematic Unity Explorer Installation
Unzip the content to your game directory usually something like `\steamapps\common\Maid of Sker` (Steam).
Don't be affraid, this 2 folders may already exist but are empty. 

Once this all done, start the game. It may take some time to see the first game splash screen. This is completely normal.
Second time, your game will start in no time. You should see something like this. Press `F7` to hide the CUE interface.

![image](/images/MOS_Interface.jpg)

## How To Take A Screenshot

OK, don't be affraid, it easy and don't ask NASA knowledge. Just some first manipulations.
Basically, for this game this how you would proceed to get the shooting part easier.

* Press `Page Up` to pause the game.
* Press `Delete` to hide the HUD.
* Press `F7` to show the CUE interface.
* Check `Use Game Camera` if you want to keep the game post processing. You will only need to do this once. That setting stays active the whole time the game is running.
* Press `Begin Freecam`. 
* Press `Inspect Free Camera` and click `Inspect Game Object`.
* Uncheck the `Opsive.UltimateCharacterController.Camera.CameraController`. Don't press anywhere else as it will open the properties of that component. Just uncheck it.
  ![image](/images/MOS_Inspector.jpg)
* Press `F7` to hide CUE interface.
* Frame and take your shot.
  
For the camera movement, refer to the free camera window when CUE interface is active. 

Once done, enable CUE interface, check back `Opsive.UltimateCharacterController.Camera.CameraController`, end the Free Cam session, Un-Hide the interface and finally resume the game.

The cheat code for that one is now `Page Up`, `Delete`, `Insert`, `F7`, uncheck, `F7` to start the shooting session. Then the other way around to come back to the game.
Easy peasy! 




