## How to get started with UEVR Easy Injector
New to UEVR and want to play common flatscreen PC games in Virtual Reality using your e.g. Meta Quest headset? Here's how to get started.

### 1. Ensure your PC can handle it
VR requires rendering at a very high resolution, and the experience is sensitive to low frame rates. Therefore, you need a modern, powerful PC. Your graphics card should be particularly strong and have ample VRAM for the high resolution. If the game you want to play does not achieve high frame rates at high resolutions in normal flatscreen, it is unlikely to perform well in VR.

### 2. Install your game
First, check if the game runs on Unreal Engine version 4 or higher, which is required for UEVR (very latest versions of the engine might also causes problems). The simplest way to do this is by searching the game's name along with "Unreal Engine version" on Google or Bing. UEVR Easy Injector currently supports Steam, Epic, GOG and XBox. Install the game via these stores just normally. Privated versions installed outside of these stores are not supported.

### 3. Ensure you have a fast network connection to your headset
Transferring VR 3D display data from your PC to your headset requires a lot of bandwidth.

- If you have a **good Wifi and LAN connection**  - go for WIFI connection

	- Is your PC connected to your router via LAN?
	- Is your network router modern (preferably WIFI6/6E/7)?  
	(The Windows built-in Hotspot feature often has reliability issues under high CPU load and suboptimal Wifi card settings, so it is not a replacement for a modern router)
	- Is your network channel idle and not congested with other neighborhood networks or other devices using much bandwith? 

- **no good network** - go for **USB cable** connection  
Though it sounds like a better bet to simply always use USB, it will reduce your options. Better go for WIFI if you can.

### 4. Choose and install an app to link your headset to your PC
While there are several smaller ones out there, the most widely used and user-friendly ones are:

| App Name | Price | Network | Image quality |
|----------|-------|---------|---------------|
| [Virtual Desktop](https://www.vrdesktop.net/) | One time purchase | WIFI only | Best | 
| [SteamVR](https://store.steampowered.com/app/250820/SteamVR/) | Free | WIFI only | Good |
| [Meta Quest Link](https://www.meta.com/en-us/help/quest/pcvr/) | Free  | WIFI (Airlink) and USB | Good |

If your network is great, and your platform is supported, I highly recommend [Virtual Desktop](https://www.vrdesktop.net/).
It has the best image encoding, upscaling options and frame generation on headset, resulting in the best image quality.  
If your network is weak and you are a Meta Quest user, use USB on [Meta Quest Link](https://www.meta.com/en-us/help/quest/pcvr/).  
If you search for a free option that is also know to be very stable, use [SteamVR](https://store.steampowered.com/app/250820/SteamVR/).  
Except for Meta Quest Link (only PC) the installation requires an app both on PC as on the headset.

#### 4.1 Tipps for configuring Virtual Desktop (the recommended option)
In the PC app:
* __Codec__: The "Auto" setting usually makes asensible selection.  
The newer the codec (AV1 is newer than HEVC, which is newer than H.264), the better the compression efficiency. However vice versa, if you have a very fast Wi-Fi connection and don't require much compression, older encoders like the H.264+ (which allows higher bit rates than the H.264) can provide better image quality.
AV1 and HEVC codes also come in 10-bit color variants (compared to the standard 8-bit). These deliver less banding and more detail, mostly visible in dark scenes.  
There is no real performance difference when using modern NVidia cards, since they have seperate hardware encoding paths, so not affecting your game performance.
* __Encrypt local traffic__: Switch this OFF

In the headset app's streaming settings:
* __Network bandwith__: For VR this is set in the "Streamings" tab in the headset app. Do not push this too high, experiment around 50-80 MBit first, depending on the codec and wifi situation. Manually increasing bandwidth too much may cause hiccups due to network interference in busy environments. It also increases latency a bit.
* __VR frame rate__: Set a bit higher than your PC can handle to reduce flickering.
* Enable the [Snapdragon Super Resolution](https://www.qualcomm.com/developer/blog/2023/04/using-super-resolution-boost-resolution-virtual-reality) for a great on device AI upscaling. Sharper image, no downsides.
* __Synchronous Spacewarp (SSW)__: Lets your PC just render at half of the desired rate, interpolating the frames inbetween on your headset, also using half the network bandwidth. Feels much smoother, but be aware that this may cause flickering in elements like health bar HUD overlays that do not move the same way as the world view.  
So if your PC is powerful enough, OFF will give you better quality.  
If you PC struggles, note what frame rate it can push without SSW (use the option "Show performance overlay" in the streaming options). Now set the frame __VR frame rate__ to about double that safe PC framerate and enable SSW. If you leave you VR frame rate too low (e.g. 60Hz), while your PC can push eg. 45 Hz, your PC will render lower than it could. That leads to noticable input lag, though the image seems to be smooth.
* __Sharpening__: While Snapdragon super resolution increases fine detail and upscailing, this setting affects the perceived overall contrast, often looking better. Try e.g. 20-25% as a good starting point.
* __Color Vibrance__: Consider enabling "Increase color vibrance" and disabling "Increase nominal range" to prevent blown-out shadows.

### 5. Install UEVR Easy Injector
The latest releases can always be found here on GitHub:  
<a href="https://github.com/oduis/UEVRDeluxe/releases" class="download-link">Download latest UEVR Easy Injector release</a>

### 6. UEVR Easy Injector - Library page
When you start UEVR Easy Injector, you'll see a list of installed Unreal Engine Steam/GOG/Xbox/Epic games that __might__ work. Simply click a game to start.

### 7. UEVR Easy Injector - Game page
After selecting your OpenXR runtime (if necessary), simply click the game to start.

### 8. UEVR Easy Injector - select a profile & runtime
To ensure UEVR handles the game correctly and connects your controller to in-game elements like weapons, you'll need a profile. Simply click "Search online" on this page to access a list of community-submitted and tested profiles. Since UEVR is relatively new, the number of supported games may be limited. Select a suitable profile and click the "Install" button.

If no profile is available, you can create one yourself. Click the "Add profile" button and configure the options. It's recommended to start with the most performant settings. If the game crashes or exhibits graphical issues, try more conservative settings.

You will find an OpenVR/XR switcher for the runtime above the start button bar. But what is OpenXR?  
There are two protocol standards for transferring VR graphics data: OpenVR and OpenXR. OpenVR is the older standard, used by some older headsets and initially by SteamVR.  
OpenXR is the newer and recommended protocol. It allows you to choose which linking app should handle your OpenXR graphics. If you have multiple linking apps installed (to try out different options), you can select the one to start the game with here. This setting is a global option for *all* apps using OpenXR on your PC, not just UEVR Easy Injector. 

Make sure your linking app is running and you are connected to your PC via your VR headset *before* hitting the launch button.  
UEVR will start the game (if it is not already running) and inject UEVR into the game. Continue in your headset.  
Initially, UEVR will display a menu in-game. You can hide the menu by pressing the "Insert" ("Ins") key on your keyboard or by pressing both joystick buttons simultaneously.
Some games are better injected when already started, otherwise they might crash or show black screens. These games will just launch, but you have to inject again on the page e.g. when you already started the game, in the 3D world. While having UEVR Easy Injector running, just press the Ctrl-Alt-U while in the game to inject.

### 9. Mastering in-game controls
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

### 10. Connecting your controllers motion controls
Connecting your 3D controllers to e.g. your hand or weapons greatly increases the immersion (6DOF - six degrees of freedom).
However, if you have no preset profile from the "Search online" database, it is pretty complex to set up.
See some [Youtube in depth tutorials](https://www.youtube.com/watch?v=4ccaX8Hr1JU) for more details.
