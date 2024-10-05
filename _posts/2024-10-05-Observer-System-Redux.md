---
layout: post
title:  "Obeserver: System Redux"
date:   2024-10-06 00:05:55 +0300
image:  OBSERVER_POST.jpg
tags:   Screenshooting
---
The year is 2084. In a dark cyberpunk world shattered by plagues and wars, become a neural police detective and hack into the jagged minds of others. Make use of anything they felt, thought, or remembered to solve the case and catch the elusive killer.

## Required
* [UUU v3/v4](https://framedsc.com/GeneralGuides/universal_ue4_consoleunlocker.htm)

## Optional
* Reshade

##How To Take A Screenshot

Please, read carefully [THIS GUIDE](https://framedsc.com/GeneralGuides/universal_ue4_consoleunlocker.htm). It's not long and it has everything you need to know tu use the free UUU unlocker.
The free version is UUU v3. You will need to download v3.0.21. Once that version downloaded and extracted in a folder, start your game. then:
* Start UUU (uuuClient.exe).
* Click `Select` and choose `ObserverSystemRedux.exe` from the list.
* Press `Inject`.
  
<div style="width:65%; margin: auto;">
<img src="/images/OBSERVER_01.jpg" alt="UUU v3 GUI" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>
But honestly, you better read the Framed guide. Everything is explained in details. 

## Some Small Hints

#### Pause When ALT-TAB
If you, like me, ALT-TAB a lot, I would recommend changing `anshar.PauseGameOnUnfocused` from `1` to `0`. This expecially if you are using lights or post process in UUU v4.x.

### Full Character On Screen
To have the Observer AKA Rutger Hauer head displayed, type `toggledebugcamera` in the console when you are in Free Camera Mode via UUU. Recall the command and execute it again to disable the debug camera after you have taken your shot. Disable UUU Free Camera. Done.

### Global Illumination And Lens Flare
By default, the global illumination and lens flares are disable, you can activate it by typing `r.RayTracing.GlobalIllumination 2` in the console. To activate the lens flare, type (or copy and paste) `r.DefaultFeature.LensFlare 1| r.LensFlareQuality 2`. `0` being disable and `3` high quality.

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>
<img-comparison-slider>
  <img slot="first" src="/images/OBSERVER_02A.jpg" />
  <img slot="second" src="/images/OBSERVER_02B.jpg" />
</img-comparison-slider>
{% include note.html content="Global Illumination effect isn't always visible in certain scenes."%}

