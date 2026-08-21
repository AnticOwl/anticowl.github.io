---
layout: post
title:  "Batman: Arkham Series"
date:   2026-05-02 18:05:55 +0300
image:  BAS_POST.jpg
tags:   Screenshooting
---
Here is pack cameras for Batman: Arkham Asylum, Batman: Arkham City, and Batman: Arkham Origins, giving a fresh cinematic feel to exploring Gotham from every angle. On top of that, a better LOD for sharper visuals because Batman deserves nothing less than a crystal-clear night patrol.

The latest tables also include **controller support** and **IGCS Relay support** for use with IGCSDOF.

## Required
* [Batman: Arkham Asylum Cheat Table](https://anticowl.github.io/files/Batman_Arkham_Asylum_v2.3.CT)
* [Batman: Arkham City Cheat Table](https://anticowl.github.io/files/Batman_Arkham_City_v2.3.CT)
* [Batman: Arkham Origins Cheat Table](https://anticowl.github.io/files/Batman_Arkham_Origins_v2.3.CT)
* [Cheat Engine 7.6 or higher](https://du0wcodktyky8.cloudfront.net/installer/003333/420362877561915)

## Optional
These mods are optional but highly recommended. Read their description and how to install.
* [Batman: Arkham Asylum](https://www.nexusmods.com/batmanarkhamasylum/mods/1?tab=description)
* [Batman: Arkham City](https://www.nexusmods.com/batmanarkhamcity/mods/407)
* [Batman: Arkham Origins](https://www.nexusmods.com/batmanarkhamorigins/mods/451)

## Controls
<style>
.table_component {
    overflow: auto;
    width: 100%;
}

.table_component table {
    border: 1px solid #dededf;
    height: 100%;
    width: 100%;
    table-layout: fixed;
    border-collapse: collapse;
    border-spacing: 1px;
    text-align: left;
}

.table_component caption {
    caption-side: top;
    text-align: left;
}

.table_component th {
    border: 1px solid #dededf;
    background-color: #eceff1;
    color: #000000;
    padding: 5px;
}

.table_component td {
    border: 1px solid #dededf;
    background-color: #ffffff;
    color: #000000;
    padding: 5px;
}
</style>
<div class="table_component" role="region" tabindex="0">
<table>
    <caption><br></caption>
    <thead>
        <tr>
            <th>Key</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>NUMPAD 8,5,4,6</td>
            <td>Forward, backward, left and right</td>
        </tr>
        <tr>
            <td>NUMPAD 7,9</td>
            <td>Camera up and down</td>
        </tr>
        <tr>
            <td>NUMPAD 1,3</td>
            <td>Camera roll</td>
        </tr>
        <tr>
            <td>ARROW Up, Down </td>
            <td>Pitch up and down</td>
        </tr>
        <tr>
            <td>ARROW Left, Right</td>
            <td>Yaw left and right</td>
        </tr>
        <tr>
            <td>NUMPAD +,-</td>
            <td>Zoom in and out</td>
        </tr>
        <tr>
            <td><br></td>
            <td><br></td>
        </tr>
        <tr>
            <td>Insert</td>
            <td>Enable camera structure</td>
        </tr>
        <tr>
            <td><br></td>
            <td><br></td>
        </tr>
        <tr>
            <td>Delete</td>
            <td>Disable pause menu</td>
        </tr>
        <tr>
            <td>Page Down (Only Asylum and City)</td>
            <td>Enable slomo</td>
        </tr>
        <tr>
            <td>F1-F3</td>
            <td>Slomo 0.15, 0.3 and Normal speed</td>
        </tr>
        <tr>
            <td>Page Up</td>
            <td>Better LOD</td>
        </tr>
        <tr>
            <td><br></td>
            <td><br></td>
        </tr>
        <tr>
            <td>Left Control</td>
            <td>Slow camera movements</td>
        </tr>
        <tr>
            <td>Left Alt</td>
            <td>Slower camera movements</td>
        </tr>
    </tbody>
</table>
</div>

### Controller
The camera can also be controlled with an Xbox/XInput compatible controller.

* **Left Stick** - Move forward/backward and strafe left/right
* **Right Stick** - Yaw and pitch
* **Left / Right Trigger** - Move camera down/up
* **LB / RB** - Roll
* **B** - Reset roll
* **X** - Slow movement
* **Y** - Fast movement
* **D-Pad Up / Down** - FOV

Controller input is ignored while IGCSDOF is rendering so it does not interfere with an IGCS Relay session.

## Better Level of Detail

### Arkham Origins

<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/BAO_01.jpg" />
  <img slot="second" src="/images/BAO_02.jpg" />
</img-comparison-slider>

### Arkham City
<script defer
  src="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/index.js">
</script>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/img-comparison-slider@8/dist/styles.css"
/>

<img-comparison-slider>
  <img slot="first" src="/images/BAC_01.jpg" />
  <img slot="second" src="/images/BAC_02.jpg" />
</img-comparison-slider>

## How To
### Use The Cheat Table
Once you have installed Cheat Engine 7.6 or higher (if not already done), click twice on the cheat table file you downloaded. Check the `Auto Attach to Game` box. Cheat Engine will automatically connect to the game when detected.
Press `Page Down` to enable the camera structure and leave on.  

The current tables include the camera, pause/slomo and LOD options together with the new **IGCS Support** script.

<div style="width:55%; margin: auto;">
<img src="/images/BatmanArkham_Table_v2.3.png" alt="Batman Arkham Cheat Engine table with IGCS Support" style="box-shadow: 3px 3px 3px gray;">
</div>
<div> </div>

### How to use IGCS Support
All three games are **32-bit**, so use the 32-bit versions of IGCS Connector and IGCS Relay:

* `IGCSConnector.addon32`
* `IGCSRelay.addon32`

The rendering API is different depending on the game:

* **Batman: Arkham Asylum** - DirectX 9. Use **dgVoodoo2** first, then install ReShade for DirectX 10/11/12.
* **Batman: Arkham City** - DirectX 11. Install ReShade directly for DirectX 10/11/12. dgVoodoo2 is not required.
* **Batman: Arkham Origins** - DirectX 11. Install ReShade directly for DirectX 10/11/12. dgVoodoo2 is not required.

You need:

* [ReShade with add-on support](https://reshade.me/)
* [IGCS Connector](https://github.com/FransBouma/IgcsConnector/releases)
* [IGCS Relay](https://github.com/AnticOwl/IGCS-Relay/releases)
* [dgVoodoo2](https://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/) for **Arkham Asylum only**

#### Arkham Asylum - dgVoodoo2 setup
Arkham Asylum uses DirectX 9, so dgVoodoo2 is required before installing ReShade.

From the dgVoodoo2 archive, copy these files into the same directory as `ShippingPC-BmGame.exe`:

* `MS\x86\D3D9.dll`
* `dgVoodooCpl.exe`
* `dgVoodoo.conf`

Run `dgVoodooCpl.exe` from the game directory so it uses the local `dgVoodoo.conf` file.

In the **General** tab, set the output API to **Direct3D 11 (feature level 11.0)**. This is the recommended target for ReShade.

Then open the **DirectX** tab and disable the **dgVoodoo Watermark** option so the dgVoodoo logo is not displayed in-game. Click **Apply** to save the configuration.

For more information about dgVoodoo2 installation and configuration, see [dgVoodoo2 - Marty's Mods Guides](https://guides.martysmods.com/additionalguides/apiwrappers/dgvoodoo2/).

Once dgVoodoo2 is configured, install ReShade for **DirectX 10/11/12**, not DirectX 9. dgVoodoo2 translates Arkham Asylum's original DX9 output to DX11 for ReShade. This is important for the IGCS Connector/Relay add-ons, and it also allows you to use ReShade shaders and effects that require a DX10/11 rendering path and are not available through native DX9.

#### Arkham City and Arkham Origins - DirectX 11
No wrapper is needed. Install ReShade directly and select **DirectX 10/11/12**.

Make sure you use a ReShade build with **add-on support**.

#### Install IGCS Connector and IGCS Relay
Copy the 32-bit add-ons into the ReShade add-on folder:

* `IGCSConnector.addon32`
* `IGCSRelay.addon32`

Do **not** use the `.addon64` versions for these games.

#### Enable the camera and Relay support
Start the game and open the Cheat Engine table.

* Enable `Auto Attach To Game`.
* Enable `Camera - Leave On`.
* Enable `IGCS Support`.
* Open the ReShade overlay and check the **IGCS Relay** panel.
* The Relay status should show that the camera connection is ready.

Once the status is OK, frame your shot and start IGCSDOF normally. IGCS Relay will control the Cheat Engine camera automatically while the image is rendered and restore the camera position when the render is finished.

For more information about the Relay itself, see the [IGCS Relay guide](https://anticowl.github.io/2026/08/12/IGCSRelay/).

### Take A Screenshot
* Press `Escape` on keyboard or `Pause` on your controller to pause the game.
* Press `Delete` to disable the pause menu.
* Frame, take your shot and go the other way around to get back in game.

## Resources

* [PC Gaming Wiki - Arkham Origins](https://www.pcgamingwiki.com/wiki/Batman:_Arkham_Origins)
* [PC Gaming Wiki - Arkham City](https://www.pcgamingwiki.com/wiki/Batman:_Arkham_City)
* [PC Gaming Wiki - Arkham Asylum](https://www.pcgamingwiki.com/wiki/Batman:_Arkham_Aylum)

Big thanks to [One3rd](https://www.flickr.com/photos/one3rd_v2/) for the tests. Be sure to check his work! 
