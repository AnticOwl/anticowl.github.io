---
layout: post
title:  "IGCS Relay"
date:   2023-07-18 18:05:55 +0300
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
* [IGCS Connector by Frans Bouma](https://github.com/FransBouma/IgcsConnector/releases)
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

## How to add IGCS Relay support to an existing Cheat Engine table

If you already have a working Cheat Engine free camera, adding IGCS Relay support is usually quite simple.

You do **not** need to rewrite the whole camera table.

In most cases, you only need to add the IGCS Relay Lua script and configure a few values so it knows where your camera data is stored.

The important information is:

* The camera base pointer
* Position offsets: X, Y and Z
* Rotation offsets: Pitch, Yaw and Roll
* FOV offset
* The correct engine tag

A typical configuration looks like this:

```
------------------------------------------------------------
-- USER CONFIGURATION
------------------------------------------------------------

local CONFIG = {

  engine = "UE3",

  bases = {
    position = "pCamera",
    rotation = "pCamera",
    fov      = "pCamera"
  },

  position = {
    x = 0x56C,
    y = 0x570,
    z = 0x574
  },

  rotation = {
    pitch = 0x578,
    yaw   = 0x57C,
    roll  = 0x580
  },

  fov = {
    offset = 0x584
  },

  cameraLockSymbol = "",

  writers = {
  },

  restoreHoldMs = 250,
  cameraIntervalMs = 16
}

------------------------------------------------------------
-- END USER CONFIGURATION
--
-- STOP EDITING HERE.
-- Everything below this line is universal provider core.
------------------------------------------------------------
```
The Relay script then uses your existing camera pointer.

For example, if your table already exposes a symbol such as:


`pCamera`


the Relay only needs a small function that returns the actual camera address.

```
function getCamBase()
    local p = getAddressSafe("pCamera")
    if not p then return nil end

    local cam = readInteger(p)
    if not cam or cam == 0 then return nil end

    return cam
end
```

### Engine tag

The engine tag tells IGCS Relay which camera math should be used.

Use one of the supported tags defined in the Relay Lua script.

For example:

```
ENGINE = "UE3"
```

for a compatible Unreal Engine 3 camera.

### Camera bases

You also need to tell the Relay which camera base contains the position, rotation and FOV values.

In many Cheat Engine cameras, everything is stored in the same camera structure:

```
bases = {
  position = "pCamera",
  rotation = "pCamera",
  fov      = "pCamera"
},
```

This means that the Position, Rotation and FOV offsets are all calculated from `pCamera`.

If your table uses different structures, you can define a different base for each one.

For example:

```
bases = {
  position = "pCamera",
  rotation = "pRotation",
  fov      = "pFov"
},
```

Most existing camera tables will only need the first configuration.


### Finding the offsets

The easiest way is usually to look at the existing camera script.

If the camera code reads or writes values such as:

```
[pCamera]+5C
[pCamera]+60
[pCamera]+64
```

those values are the offsets used by the camera structure.

For example:

```
X_OFFSET = 0x5C
Y_OFFSET = 0x60
Z_OFFSET = 0x64
```

Do the same for Pitch, Yaw, Roll and FOV.

You do not need to understand the complete Cheat Engine script. In most cases, you only need to identify the offsets already used by the working camera.

### Example

If you want to see how Relay support is added to a real Cheat Engine table, have a look at the **DmC: Devil May Cry** table.

DmC uses the **UE3** profile and is a good reference for:

* where to place the Relay Lua script;
* how `getCamBase()` is connected to the existing camera pointer;
* how the camera offsets are configured;
* how the engine tag is defined.

You can use it as a starting point when adapting another Cheat Engine camera to IGCS Relay.


