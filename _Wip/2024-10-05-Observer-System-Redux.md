---
layout: post
title:  "Obeserver: System Redux"
date:   2024-08-21 18:05:55 +0300
image:  HELLBLADE_POST.jpg
tags:   Screenshooting
---
The year is 2084. In a dark cyberpunk world shattered by plagues and wars, become a neural police detective and hack into the jagged minds of others. Make use of anything they felt, thought, or remembered to solve the case and catch the elusive killer.

## Required
* [UUU v3/v4](https://framedsc.com/GeneralGuides/universal_ue4_consoleunlocker.htm)

## Optional
* Reshade

If you, like me, ALT-TAB a lot, I would recommend changing `anshar.PauseGameOnUnfocused` from `1` to `0`. This expecially if you are using lights or post process in UUU v4.x.
To have the Observer AKA Rutger Hauer head displayed, type `toggledebugcamera`. Recall the command and execute it again to disable the debug camera after you have taken your shot.
By default, the global illumination and lens flares is disable, you can activate it by typing `r.RayTracing.GlobalIllumination 2` in the console. To activate the lens flare, type (or copy and paste) `r.DefaultFeature.LensFlare 1| r.LensFlareQuality 2`. `0` being disable and `3` high quality.

