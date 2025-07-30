---
layout: post
title:  "Quantum Break"
date:   2025-07-18 00:05:55 +0300
image:  GWT_POST.jpg
tags:   Screenshooting
---

## Required
* [Hatti Watti Camera Tool](https://www.mediafire.com/file/63a2cpfs46gzefn/CT_QuantumBreak_20181024.rar/file)
* [Quantum Break game patche with dev menu](https://github.com/illusion0001/Windows-Game-Patches/releases/tag/1.0.201-0349c14b%2B910-branch-main) (download the file named Windows-Game-Patches-1.0.201-0349c14b+910-branch-main.7z
)

## Optional 
* [ReShade](https://reshade.me)

## Installation
* Rename original bink2w64.dll in game dx11 folder to bink2w64Hooked.dll for ASI Loader.
* Extract dinput8.dll from zip !ASI_Loader_x64 and rename to bink2w64.dll and copy to game dx11 folder.
* Extract QuantumBreak.Patches.asi to game dx11 folder.
* Run game once to generate ini and close it.
* Enable config for desried patches (QuantumBreak.Patches.ini).
```
[Settings]
bDisableStartupLogo = true
bEnableDevMenu = true
bDisablePauseGameOnFocusLoss = true
```
