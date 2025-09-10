---
layout: post
title:  "How to create motion blur shots"
date:   2025-09-08 18:05:55 +0300
image:  MBL_POST.jpg
tags:   Reshade Cheat-Engine
---

For motion blur shots, PC virtual photography gives us the opportunity to experiment not only with the internal photo mode and game options available but also with tools. Free or paid ones. 
While it would be nice to have a single solution for this, the nature of the development mades it totally impossible. So let see some of the solutions available. 

## Absolutely Required at 100%
Reshade 6.x with reallongtimeexposure.fx

## Tools and processes
### UUU 4.x/5.x for Unreal Engine 4/5
Depending the engine of your game, you will need one of the 2 versions. And whatever the version the modus operandi is the same. 
<br>
</br>
Lets take by example Formula Legends demo as the game is not yet out at the time of writing this guide. Game is Unreal Engine 5. So, you will use UUU 5.x.

#### How to

1. While in game and UUU 5.x loaded. Press `Page Down` or `NumPad 0` to pause the game when driving.
2. Press `Delete` then `Insert` to hide the HUD and enable the free camera.
3. Frame your shot (FOV, angle, etc).
4. Go to UUU Client and enable the `Camera Path` window.
5. Check the print screen below and do exactly as is. You will need 1 camera path and 2 nodes. These nodes need to be at the sample place. So click twice on `+`. Set the gamespeed to 0.05 or lower.
6. Press F7 or `Play` to start. The camera will the follow the vehicle.
7. Press the assigned key to start the long exposure.
<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/a7b48945-f786-470c-9ed5-e0266ed4ddd3" alt="UUU Camera Path" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div> 

Formula Legends
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


Cheat Engine 7.5

Higher FPS = Better motion blur quality
![image](https://github.com/user-attachments/assets/b5dc41bf-458a-4b98-b598-5cd8a31f32ef)
Otherwise choppy 

UUU Camera Path
1 Path and 2 nodes at the same place or a bit spaced.

Cheat engine
Speed hack at like 0.05 or 0.1 to get a high fps
Not working in all games

Reshade 
Reallongexposure.fx 

Games
Batman: Arkham Knight
WATCH_DOGS
Cyberpunk 77
Days Gone
Mad Max
Death Stranding ???
