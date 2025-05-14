---
layout: post
title:  "Borderlands"
date:   2025-05-13 18:05:55 +0300
image:  BORDERLANDSGOTY.jpg
tags:   Screenshooting
---

Discover the original co-op shooter-looter, crammed with new enhancements! As one of 4 trigger-happy mercenaries with RPG progression, equip bazillions of guns to take on the desert planet Pandora.

## Required
* Borderlands GOTY Enhanced cheat table
* Cheat Engine 7.5 or higher
* ReShade 6.x with add-on support
* Pause Menu Shader Toggle ini file

## Optional
* Third person mode

## Installation
Install ReShade if not already done. If not start the installer. Click OK for the warning and choose you game from the list. Click `Next` twice.
Install the effects you want or click `Uncheck All` and press `Next`. Now, check the `ShaderToggler by Otis Inf`. Click next and Finish the installation.
![image](https://github.com/user-attachments/assets/14b93ab3-6845-459d-bf97-49426a850899)
If not already done, install Cheat Engine. 
Copy the `ShadderToggler.ini` file here `.\steamapps\common\BorderlandsGOTYEnhanced\Binaries\Win64` and nowhere else.
![image](https://github.com/user-attachments/assets/7afe40de-92a6-4718-8f25-72e124762fa2)

## Configuration
**This part is optional unless you want you characte in third person**
Open `WillowInput.ini` located in `C:\Users\<YOURUSERAME>\Documents\My Games\Borderlands Game of the Year\WillowGame\Config` and add the following lines at the end of `[Engine.PlayerInput]` and just before `[Engine.DebugCameraInput]`
```
Bindings=(Name="FirstPersonZoom",Command="advancedbutton bAdvancedButtonAux5",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="ThirdPersonZoom",Command="advancedbutton bAdvancedButtonAux5 | Camera FirstPerson | OnRelease Camera ThirdPerson",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="FirstPersonToggle",Command="Camera FirstPerson | setbind RightMouseButton FirstPersonZoom | setbind F1 ThirdPersonToggle",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="ThirdPersonToggle",Command="Camera ThirdPerson | setbind RightMouseButton ThirdPersonZoom | setbind F1 FirstPersonToggle",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
Bindings=(Name="F1",Command="ThirdPersonToggle",Control=False,Shift=False,Alt=False,LeftTrigger=False,RightTrigger=False,bIgnoreCtrl=False,bIgnoreShift=False,bIgnoreAlt=False)
```
