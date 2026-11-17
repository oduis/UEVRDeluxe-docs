New to UEVR and want to play common flatscreen PC games in virtual reality using a headset such as Meta Quest? Here's how to get started. Click a section heading to expand it.

## 1. Ensure your PC can handle it  
VR requires rendering at a very high resolution, and the experience is sensitive to low frame rates. Therefore, you need a modern, powerful PC. Your graphics card should be particularly powerful and have ample VRAM. If the game you want to play does not achieve high frame rates at high resolutions in normal flatscreen mode, it is unlikely to perform well in VR.

## 2. Install and prepare your game
### 2.1. Unreal games only
First, check whether the game runs on Unreal Engine 4 or newer, which is required for UEVR (the very latest engine versions may also cause problems). The simplest way to do this is to search for the game's name along with "Unreal Engine version." UEVR Easy Injector currently supports Steam, Epic, GOG, and Xbox, as well as installations found in Windows' Apps & Features list. Install the game normally through any of these stores.
Pirated versions are not supported.

### 2.2. Common in-game settings
If the game supports it, adjust these in-game graphics settings:
- Chromatic aberration: OFF
- Motion blur: OFF
- Depth of field: OFF
- View/head bobbing: OFF
- Post processing: typically looks better at LOW

### 2.3. Optimize DLSS (NVIDIA cards only)
Because VR is very performance-intensive, DLSS is usually needed. Many older games still use outdated DLSS versions.
To optimize it, try replacing the game's DLSS DLL with the latest version using the [DLSS Swapper tool](https://github.com/beeradmoore/dlss-swapper/releases). Try DLSS Preset "K" first, using DLSS Swapper or the NVIDIA app.
DLSS 4.5 adds preset L for Ultra Performance and preset M for Performance; preset K is from DLSS 4 and is used for Balanced and Quality. The model itself runs slower with L than with M, and slower with M than with K. However, the lower rendering workload means Ultra Performance with L can deliver more game performance than Performance with M, which can deliver more than Balanced with K. Whether DLSS 4.5 is better for your setup depends largely on your GPU; newer GPUs are more likely to benefit. The big upgrade is from DLSS 3 to 4 (profile K).

## 3. Ensure you have a fast network connection to your headset
Transferring VR 3D display data from your PC to your headset requires a lot of bandwidth. Your options ordered best to worst:

### 3.1 DisplayPort
A DisplayPort-connected headset is the best option. It provides no compression and is not available for Meta Quest.

### 3.2 LAN connection (via adapter)
Since the Meta Quest operating system is based on Android, it unofficially supports many standard Realtek 1 Gb/s USB LAN adapters. Some 2.5 Gb/s adapters may also work, but are typically limited to 1 Gb/s speeds. Check the adapter description to see which chip it uses.
For convenience, consider purchasing a combined power supply and LAN adapter with separate power delivery so your headset can charge while connected to the network. To avoid having a dongle hanging from your headset, use a high-quality USB-C extension cable.
There is no specific setting in Meta Quest to enable USB LAN adapters. Simply turn off Wi-Fi in the settings, power down the headset, connect the USB LAN adapter, and then power the headset back on. It should connect to the network automatically, although some features such as app updates are disabled.  
If you experience connection issues, check whether the LAN adapter’s LEDs are blinking. Some adapters may enter sleep mode and not show any activity. In such cases, try temporarily connecting the USB LAN adapter to a PC to verify network connectivity and wake it up. If it works on the PC, reconnect it to the Quest.

### 3.3 Wi-Fi
Wi-Fi is a good option if:
- your PC is connected to your router via LAN
- your network router is modern (preferably Wi-Fi 6/6E/7)
  (The Windows built-in hotspot feature often has reliability issues under high CPU load or with suboptimal Wi-Fi adapter settings, so it is not a replacement for a modern router)
- your network channel is idle and not congested by nearby networks or other devices using significant bandwidth
- you prefer a cable-free setup

### 3.4. USB cable
Virtual Desktop now supports connecting your Meta Quest headset to your PC with a USB cable. This provides a stable, low-latency connection without relying on Wi-Fi and is the recommended wired option for Quest headsets.

## 4. Choose and install an app to link your headset to your PC
While there are several smaller ones out there, the most widely used and user-friendly ones are:

| App Name | Price | Network | Image quality |
|----------|-------|---------|---------------|
| [Virtual Desktop](https://www.vrdesktop.net/) | One-time purchase | Wi-Fi/LAN and USB | Best |
| [SteamVR](https://store.steampowered.com/app/250820/SteamVR/) | Free | Wi-Fi/LAN only | Good (best if you have a native SteamVR headset) |
| [Meta Quest Link](https://www.meta.com/en-us/help/quest/pcvr/) | Free | Wi-Fi (Air Link) and USB | Good |

If your network is excellent and your platform is supported, I highly recommend [Virtual Desktop (VD)](https://www.vrdesktop.net/), especially on Quest.
It has the best image encoding, upscaling options, and frame generation on the headset, resulting in the best image quality.
If your network is weak, you are a Meta Quest user, use Virtual Desktop's USB cable mode. It provides a better wired experience than [Meta Quest Link](https://www.meta.com/en-us/help/quest/pcvr/), which can be kept as a free fallback.  
If you are looking for a free option that is known to be very stable, use [SteamVR](https://store.steampowered.com/app/250820/SteamVR/). This is also the best option if you have a native SteamVR headset.
Except for Meta Quest Link, which only runs on the PC, installation requires an app on both the PC and the headset.

### 4.1 Tips for configuring Virtual Desktop (the recommended option)
In the PC app:
* __Automatically adjust bitrate__: Performs a quick network test on connecting and limits the maximum network bandwidth accordingly. ALWAYS leave this checked. It might seem too conservative at times, but the game will usually have random stutters if you override this recommended maximum.
* __Codec__: The "Auto" setting usually makes a sensible selection.
The newer the codec (AV1 is newer than HEVC, which is newer than H.264), the better the compression efficiency. Conversely, if you have a very fast connection and do not require much compression, older encoders such as H.264+ (which allows higher bit rates than H.264) can provide better image quality.
AV1 and HEVC codecs also come in 10-bit color variants compared with the standard 8-bit variant. These provide less banding and more detail, mostly visible in dark scenes (the game renders in 8-bit, while 10-bit is used for encoding). However, this comes at the cost of higher VRAM usage.
There is much less performance difference between the codecs when using modern NVIDIA cards because they have separate hardware encoding paths. HEVC and H.264 make little difference, while AV1 is a bit slower.
* __2-Pass encoding__: Delivers better compression. Although the tooltip warns about high overhead, I found the performance overhead on NVIDIA 4000-series cards to be zero because the separate hardware encoding chip was not saturated. It did add a few milliseconds of latency. Because the compression gains are relatively low, enable it only if you need to use a low bitrate.
* __Encrypt local traffic__: Switch this OFF
* __Additional Sharpening__: On the "Advanced" tab, this sharpening occurs before encoding and helps with small details on low-bandwidth connections more than sharpening in the headset.
* __VDXR Rendering Resolution__: Stick to 100%. Tends to introduce blurriness on any other value.

In the headset app's streaming settings:
The performance panel in Virtual Desktop or on your Meta Quest headset displays the Wi-Fi speed, but this represents the theoretical maximum link rate. In practice, you can expect your actual usable speed to be about one-third of that value.

* __Graphics presets__: This determines the rendering resolution and is the most important parameter for both sharpness and performance. On Quest, "Godlike" uses the full resolution for maximum detail, considering both panel resolution and optical distortion. Try "Ultra," as "Godlike" typically yields diminishing returns.
It is better to keep this higher and instead lower the DLSS setting (e.g. to Ultra Performance) to keep up the performance.
* __VR frame rate__: Set it just a bit higher than your PC can handle to reduce flickering.
* Enable [Snapdragon Super Resolution](https://www.qualcomm.com/developer/blog/2023/04/using-super-resolution-boost-resolution-virtual-reality) for great on-device AI upscaling. It produces a sharper image with no apparent downsides.
* __Bandwidth__: The higher the bandwidth, the better the picture quality, especially in irregular visuals such as foliage. However, if you exceed what the Wi-Fi or LAN adapter can handle, you will experience stuttering. Higher bandwidth also increases processing load, which can lead to lower frame rates, more latency, and reduced battery life.
* __Sharpening__: While Snapdragon Super Resolution increases fine detail and upscaling, this setting affects perceived contrast and often looks better only if needed. Try sharpening in the PC app first to improve encoding, then add more sharpening here only if needed. It largely depends on the game.
* __Synchronous Spacewarp (SSW)__: Lets your PC render at half the desired frame rate and interpolate the frames in between on the headset, using roughly half the network bandwidth. It feels much smoother, but be aware that it may cause flickering in elements such as health-bar HUD overlays that do not move at the same rate as the world view.
So if your PC is powerful enough, OFF will give you better quality.  
If your PC struggles, note the frame rate it can maintain without SSW (use "Show performance overlay" in the streaming options). Set __VR frame rate__ to about double that safe PC frame rate and enable SSW. If you leave the VR frame rate too low, for example 60 Hz, while your PC can render 45 Hz, the PC will render at a lower frame rate than it can support. That leads to noticeable input lag, even though the image may appear smooth.
* __Color Vibrance__/__Increase nominal range__: Consider enabling "Increase color vibrance" on non-OLED headsets like Quest and disabling "Increase nominal range" to prevent blown-out shadows.

## 5. Install UEVR Easy Injector

The latest releases can always be found here on GitHub:
<a href="https://github.com/oduis/UEVRDeluxe/releases" class="download-link">Download latest UEVR Easy Injector release</a>  
You do not need to download UEVR Classic. UEVR Easy includes the UEVR backend and does not require the Classic installation.

## 6. UEVR Easy Injector - Library page
When you start UEVR Easy Injector, you will see a list of installed Unreal Engine games from Steam, GOG, Xbox, and Epic that __might__ work. Simply click a game to start.
You can also click "Profile catalog" at the bottom to see the profiles available in the database. You are not restricted to these; you can install any profile from the internet using the usual manual method.

## 7. UEVR Easy Injector - Download a profile
To ensure UEVR handles the game correctly and connects your controller to in-game elements like weapons, you'll need a profile. Simply click "Search online" on this page to access a list of community-submitted and tested profiles. Select a suitable profile (if available) and click the "Install" button.

You can also download and install profiles manually from Discord or other websites, just as you would with UEVR Classic.

If no profile is available, you can create one yourself. Click the "Add profile" button and configure the options. It is recommended to start with the most performant settings. If the game crashes or exhibits graphical issues, try more conservative settings.

Profiles you download often include instructions for proper use. Some may require additional mods to be installed in the game, or have specific usage steps and workarounds. Be sure to read and follow any instructions provided with the profile to ensure it works correctly.

## 8. Select protocol
You will find an OpenVR/XR switcher for the runtime above the start button bar. But what is OpenXR?  
There are two protocol standards for transferring VR graphics data: OpenVR and OpenXR. OpenVR is the older standard, used by some older headsets and initially by SteamVR.  
OpenXR is the newer and recommended protocol. It allows you to choose which linking app should handle your OpenXR graphics. If you have multiple linking apps installed (to try out different options), you can select the one to start the game with here. This setting is a global option for *all* apps using OpenXR on your PC, not just UEVR Easy Injector. 

## 9. Launch game
Make sure your linking app is running and you are connected to your PC via your VR headset *before* continuing.  

There are two types of games (UEVR Easy will indicate which):

- For some games, you can simply click the launch button. The game will start (if it isn’t already running), and UEVR will inject itself a few seconds later. Continue in your headset. You may see a black screen in the headset during startup videos or loading screens.

- Other games require injection after the game has already started, usually when you are inside the 3D world. In these cases, clicking the launch button will only start the game without injection. Once you are in-game, press the inject button again. Alternatively, you can use the global hotkey Ctrl+Alt+U to inject without switching windows.

Initially, UEVR will display an in-game menu. You can hide the menu by pressing the Insert ("Ins") key on your keyboard or by pressing both joystick buttons simultaneously.

## 10. Mastering in-game controls
If the game supports gamepads, your VR controllers will function like a gamepad. You can typically use the joystick and the "A" button to navigate the menus:

| VR controller button... | ...will function as game button |
|----------------------|------------------------------|
| Left thumbstick | Move in game |
| Right thumbstick | Rotate view |
| Left Grip | LB |
| Right Grip | RB |
| Left Trigger | LT |
| Right Trigger | RT |
| Left Thumbstick Click | L3 |
| Right Thumbstick Click | R3 |
| Left System Button | Start/Pause |
| Left A Button (X on Meta Quest) | B/Circle |
| Left B Button (Y on Meta Quest) | Y/Triangle |
| Right A Button | A/X |
| Right B Button | X/Square |

Note the counterintuitive mapping of the buttons B/X/Y.
You can typically also play with the keyboard and mouse, using just the VR 3D view.

## 11. Connecting motion controls to your controllers
Connecting your 3D controllers to, for example, your hands or weapons greatly increases immersion (6DOF — six degrees of freedom).
However, if you do not have a preset profile from the "Search online" database, setup is quite complex.
See some [YouTube in-depth tutorials](https://www.youtube.com/watch?v=4ccaX8Hr1JU) for more details.
