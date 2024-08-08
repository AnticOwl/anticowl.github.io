---
layout: post
title:  "Remember Me"
date:   2024-08-05 18:05:55 +0300
image:  RM_POST.jpg
tags:   Screenshooting
---
A game that went below my radar years ago. A game that was gathering dust in my library. A game that I finally started thanks to some people's shots. I honestly recommend it to anyone who wants a great story.

## Required
* [IDK31 EXCELLENT Camera Cheat Table](https://steamcommunity.com/sharedfiles/filedetails/?id=662482735)
* [Cheat Engine](https://www.cheatengine.org/)

## Optional
* Reshade 4.9.1 (versions above will probably give you problems when ALT-Tabbing).
* [Nilin Regular Outfit](https://www.nexusmods.com/rememberme/mods/5)
* [Nilin Intro Outfit](https://www.nexusmods.com/rememberme/mods/1)
* [Enhanced Lighting Modification](https://www.nexusmods.com/rememberme/mods/12)
* [No Grain](https://www.nexusmods.com/rememberme/mods/2) (really, you need that one. Thanks Shino!)
* [Better Graphics](https://www.nexusmods.com/rememberme/mods/24) 
* [TexMod Autoload](https://www.nexusmods.com/rememberme/mods/4?tab=files) (very optional)

## Installation
If you go for the optional items, and once downloaded, extract the 2 textures and no grain mods and place them in your installation folder (.\steamapps\common\Remember Me\Binaries\Win32).
Each time you want to play and/or take some shots with the mods enabled, you will have to run the texmod.exe then choose the Remember Me game exe and the texture mods you want to use like in the print below.     

<div style="width:65%; margin: auto;">
<img src="/images/RM_01.jpg" alt="Remember Me TexMod" style="box-shadow: 3px 3px 3px gray;">
</div>

If you feel comfortable with writing the.ini file yourself, you can also use TexMod Autoload to remove the need to manually select and load the mod files each time. 
<br>
Example with and without the No Grain mod. 
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/RM_10.jpg" />
  <img slot="second" src="/images/RM_11.jpg" />
</img-comparison-slider> 

Now, for the `Enhanced Lighting` Modification. Before you start, make a backup of the files in the following location: `\Documents\My Games\UnrealEngine3\RememberMeGame\Config`. You can do this by renaming  the .ini file in .org by example.

You can now extract the `Enhanced Lighting Modification` .rar file and copy the contents of the Config folder to the above location. The files residing in ``olour & Lighting` need to be extracted in the same folder as the 2 previous texture mods: `.\steamapps\common\Remember Me\Binaries\Win32`

For the Better Graphics, you can safely overwrite the `ExampleEngine.ini` file when extracting, but I would recommend a backup first. You should also test this mod as it could introduce shadow banding in some cases.


## Configuration
There isn't much to configure beside adding a keybind for a Pause. So, again, head to `\Documents\My Games\UnrealEngine3\RememberMeGame\Config` and open the `ExampleInput.ini` with Notepad.
Under `[ExampleGame.ExamplePlayerInput]` add the line `Bindings=(Name="F5",Command="pause")` and save the file. Now, you can pause the game before activating the camera while in game.
<br>
You are now ready to start!

{% include note.html content="Don't forget to switch texture when Nilin put her regula outfit."%}

## Things to Remember When Shooting
First off, you have a read to [IDK31 post](https://steamcommunity.com/sharedfiles/filedetails/?id=662482735). You will find a lot of usefeul information there. Trust me, you won't lose your time.
From my experience with Remember Me is that these are the things you need to remember when shooting. 

* When you pause the game with F5, the blur from the DoF (Depth of Field) is removed in most cases.
* Full HUD removal can only be achieved via the cheat table. You  can try `Bindings=(Name="Delete",Command="ShowHud | show scaleform")` but it won't remove some indicators like climb points.

## Resources
* [PC Wiki Gaming](https://www.pcgamingwiki.com/wiki/Remember_Me)
* [Steam IDK31](https://steamcommunity.com/sharedfiles/filedetails/?id=662482735)






