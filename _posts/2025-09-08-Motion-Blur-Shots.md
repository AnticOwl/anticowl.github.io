---
layout: post
title:  "How To Create Motion Blur Shots"
date:   2023-09-08 18:05:55 +0300
image:  MBL_POST.jpg
tags:   Reshade Cheat-Engine
---

For shots that include motion blur, PC virtual photography gives us the opportunity to experiment not only with the internal photo mode and game options available but also with third party tools: both free and paid ones. While it would be nice to have a single solution for this, the nature of game development makes that totally impossible. So, let's see some of the solutions that are available.

## Absolutely Required at 100%
Reshade 6.x with reallongtimeexposure.fx

## Tools and processes
### UUU 4.x/5.x for Unreal Engine 4/5
Let's take Formula Legends as an example. The game is yet to be released at the time of writing this guide, so I have used the demo. The game is build on Unreal Engine 5, so you will use UUU 5.x here.

#### How to

* While in game and UUU 5.x loaded. Press `Page Down` or `NumPad 0` to pause the game when driving.
* Press `Delete` then `Insert` to hide the HUD and enable the free camera.
* Frame your shot (FOV, angle, etc).
* Go to UUU Client and enable the `Camera Path` window.
* Check the print screen below and do exactly as is. You will need 1 camera path and 2 nodes. These nodes need to be at the sample place. So click twice on `+`. Set the gamespeed to 0.05 or lower.
* Press F7 or `Play` to start. The camera will the follow the vehicle. P
* Press the assigned key to start the long exposure.
<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/a7b48945-f786-470c-9ed5-e0266ed4ddd3" alt="UUU Camera Path" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div> 

Formula Legends (Unreal Engine 5)
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/FL-Before.png" />
  <img slot="second" src="/images/FL-After.png" />
</img-comparison-slider>

Trail Out (Unreal Engine 4)
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/TO-Before.png" />
  <img slot="second" src="/images/TO-After.png" />
</img-comparison-slider>

Rennsport (Unreal Engine 5)
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/RS-Before.png" />
  <img slot="second" src="/images/RS-After.png" />
</img-comparison-slider>

### Cheat Engine A.K.A. The Frame Generator

Higher FPS = Better motion blur quality
Speed hack at like 0.05 or 0.1 to get a high fps
Not working in all games






## Game Specific Tools. Or Not.
### Batman: Arkham Knight
[Requirements](https://anticowl.github.io/2024/11/12/Batman-Arkham-Knight/) 
* In console, paste that command `set BmGame.RVehicleBatmobileBase ForceHeadlightsSwitchedOn 1` **!!!IMPORTANT!!!**<br />
*If you do not enter that command, the batmobile lights will be turned off as soon as you start the motion blur.*
* Enter debug camera by pressing `backspace`
* Frame your shot and enter orbital mode by pressing the right stick. **!!!IMPORTANT!!!**
* In console type `slomo 0.05`. Lower values won't work. The car won't move at all.
* In console type `playersonly`.
* Press your assigned key to start the motion blur.
* Press your assigned key to take your shot.
* In console disable the slomo by typing `slomo 1`. **!!!IMPORTANT!!!**
*If you do not disable the slomo, the game will still run at 0.05 when you come back to it*
* Press `Backspace` to disable the debug camera.
  
<div style="width:65%; margin: auto;">
<img src="/images/BAK_01.jpg" alt="UUU v3 GUI" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

### WATCH_DOGS
[Requirements](https://anticowl.github.io/2024/07/20/WATCH_DOGS/) 
- Press F5 to pause the game and F4 to hide the HUD.
- Activate the camera by pressing Home then Insert to show the UCT GUI.
- Change the mode to Look At Player. The camera will be positioned attached to back back of the vehicule.                 
- Press Static Angles.
- Change the angles to your preferences in the Ideal Position Offset.
  First box is for horizontal axe, second is he depth, and third vertical.
- Change the angles to your preferences in the Ideal Angle Offset.
  First box is for tilt, second is roll, and third pan.
- Start the game back but in slow motion by pressing F6.
- Press your assigned shortcut to start the long exposure. 
- Press Print Screen to save your shot.
- Press your long exposure shortcut, disable the camera and press F6 to return to the game normal speed.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/e8006492-04f2-4779-ba7c-bfb91ae4d4cd" alt="UUU v3 GUI" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

### Cyberpunk 77
Required: [Otis_inf Cyberpunk 2077 Camera Tools](https://www.patreon.com/posts/46311727)
<br>
As the tool is from Otis_inf and his tools are using a standard interface. The process is the same as for UUU4.x/5.x.

* While in game and the tool loader, press `NumPad 0` to pause the game when driving.
* Press `Delete` then `Insert` to hide the HUD and enable the free camera.
* Frame your shot (FOV, angle, etc).
* Go to UUU Client and enable the `Camera Path` window.
* Check the print screen below and do exactly as is. You will need 1 camera path and 2 nodes. These nodes need to be at the sample place. So click twice on `+`. Set the gamespeed to 0.05 or lower.
* Press F7 or `Play` to start. The camera will the follow the vehicle. 
* Press the assigned key to start the long exposure.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/abdbd1d6-9edf-47d2-8cda-05f2329cc212" alt="Cyberpunk 2077" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

### Mad Max

