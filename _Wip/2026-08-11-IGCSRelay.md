---
layout: post
title:  "IGCS Relay"
date:   2024-07-18 18:05:55 +0300
image:  IGCSRELAY_POST.jpg
tags:   Screenshooting
---

Forget depth-based blur that breaks on transparency. IGCSDOF doesn’t fake depth of field from the depth buffer.The result: cinematic, camera-like DoF where glass, hair, particles and translucency finally behave the way they should.

## What is IGCS Relay?

IGCS Relay is the link between IGCS Connector and supported custom game cameras.

Normally, IGCSDOF needs a compatible IGCS camera tool to control the camera during a render. IGCS Relay extends that support to other cameras, such as compatible Cheat Engine photo modes.

For the user, this simply means more games can use IGCSDOF without needing a dedicated IGCS camera tool.

Once the camera is enabled and the Relay status is OK, you can frame your shot, start IGCSDOF and render as usual. The Relay handles the camera movements automatically in the background.

## Required
* [ReShade 6.7 or higher with add-on support](https://reshade.me/downloads/ReShade_Setup_6.8.0_Addon.exe)
* [IGCS Relay](https://github.com/AnticOwl/IGCS-Relay/releases)
* [IGCS Connector](https://github.com/FransBouma/IgcsConnector/releases)
* [Cheat Engine 7.6 or higher](https://www.cheatengine.org)
* A compatible cheat table

## Installation

* Install ReShade for the game.
* Copy the IGCS Relay add-on into your ReShade add-on folder.
* Use the correct version for the game:
  * IGCSRelay.addon64 for 64-bit games
  * IGCSRelay.addon32 for 32-bit games

Launch the game and open the ReShade overlay.

You should see the IGCS Relay panel.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/ecc37fb1-b7ab-4cdf-b7ce-a4df954ed7ab" alt="IGCS Relay" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

## How To Use
* Start the game.
* Open the compatible Cheat Engine table.
* Attach Cheat Engine to the game.
* Enable the camera / Photo Mode.
* Enable the IGCS support.
* Check the IGCS Relay panel in ReShade.
* Make sure the Relay status is OK.
* Frame your shot.
* Start IGCSDOF.
* Configure your focus, aperture, samples and other IGCSDOF settings.
* Start the render.

IGCSDOF will automatically control the camera during the render.

<div style="width:65%; margin: auto;">
<img src="https://github.com/user-attachments/assets/2bba9692-668f-4794-87ec-56aa79dffa38" alt="IGCS Relay" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

When the render is finished, the camera will return to its original position.
