---
layout: post
title:  "Remember Me"
date:   2024-08-05 18:05:55 +0300
image:  RM_POST.jpg
tags:   Screenshooting
---

## Required
* [IDK31 EXCELLENT Camera Cheat Table](https://steamcommunity.com/sharedfiles/filedetails/?id=662482735)
* [Cheat Egnine](https://www.cheatengine.org/)

## Optional
* Reshade 4.9.1 (versions above will probably give you problems when ALT-Tabbing).
* [Nilin Regular Outfit](https://www.nexusmods.com/rememberme/mods/5)
* [Nilin Intro Outfit](https://www.nexusmods.com/rememberme/mods/1)
* [Enhanced Lighting Modification](https://www.nexusmods.com/rememberme/mods/12)
* [Better Graphics](https://www.nexusmods.com/rememberme/mods/24) 
* [TexMod Autoload](https://www.nexusmods.com/rememberme/mods/4?tab=files) (very optional)

## Installation
If you go for the optional items, and once downloaded, extract the 2 texture mods in your installation folder (.\steamapps\common\Remember Me\Binaries\Win32).
Each time you want to play and/or take some shots you will have to start `texmod.exe` and choose the texture mods and game exe like int the print below.     
![image](/images/RM_02.jpg)

You can also use `TexMod Autoload` if you feel confortable writing the ini file yourself. 
<br>
Now, for the `Enhanced Lighting Modification` and `Better Graphices` you will need to extract the first file in `\Documents\My Games\UnrealEngine3\RememberMeGame\Config`.
But, before that, be sure you backup these files first (rename the .ini file in .org by example)! The file residing in `Colour & Lighting` needs to be extracted in the same folder as the 2 previous texture mods.
For the `Better Graphics`, you can safely overwrite the file when extracting. But, I would recommend a backup first and test as it could introduce shadow banding in some cases. 

## Configuration
There isn't much to configure beside adding a keybind for a Pause. So, again, head to `\Documents\My Games\UnrealEngine3\RememberMeGame\Config` and open the `ExampleInput.ini` with Notepad.
Under `[ExampleGame.ExamplePlayerInput]` add the line `Bindings=(Name="F5",Command="pause")` and save the file. Now, you can pause the game before activating the camera while in game.
<br>
You are now ready to start!

## Things to Remember When Shooting
First off, have a read to [IDK31 post](https://steamcommunity.com/sharedfiles/filedetails/?id=662482735). You will find a lot of usefeul informations. Trust me, you won't loose your time.
So, from my experience with Remember Me is that there are things you need to remember when shooting. 
* The noise/grain in the game is quite heavy. Check below for a Before and After when taking a shot. Need to be deactivated at reload or level change. You can do it via `SPECIAL EFFECTS > Other Effects/Alt DOF > NOISE/FILM GRAIN`. Click on `ON` and change the value to `-` and press OK.
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/RM_03.jpg" />
  <img slot="second" src="/images/RM_04.jpg" />
</img-comparison-slider> 

* When you pause the game with F5, the blur from the DOF (Depth of Field) is in most cases removed.
* HUD can only be deactivated via the cheat table (or you can try adding the line like for the pause `Bindings=(Name="Delete",Command="ShowHud | show scaleform")`).

Happy shooting!






