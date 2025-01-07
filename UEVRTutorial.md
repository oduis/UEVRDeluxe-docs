## How to get started with UEVRDeluxe?
New to UEVR, and you want to play 2D PC Steam games in Virtual Reality e.g. using your Meta Quest headset? This is how to get started.  

### 1. Make sure your PC can handle it
Because VR renders at a very high resolution, and VR experience is sensitive to low frame rates, you need a modern, powerful PC.
Especially the graphics card should be powerful and have lots of VRAM for the high resolution required to be rendered.  
If the game you want to play does not even run with high frame rates in high resolutions in 2D, do not even try it in VR.  

### 2. Install your game
First check if your game is running on Unreal Engine version 4 or higher, which is required for UEVR.
Simplest way: google/bing you games name including " unreal engine version".  
UEVR Deluxe currently only supports Steam. Install your game via Steam in the normal way.

### 3. Make sure you have fast network connections
Transferring the VR display data calculated on your PC to your headset requires lots of bandwidth.  

- If you have a good Wifi/LAN connection - go for WIFI connection  
Is your PC connected to your router via LAN? Is your network router modern (preferably WIFI6/6E/7)? 
Is your network channel idle and not congested with other neighborhood networks or e.g. other devices sipping bandwith?

- no good network - go for USB cable connection  
Though it sounds like a better bet to simply always use USB, it will reduce your options. Better go for WIFI if you can.

### 4. Choose and install an app to link your headset to your PC
While there are several smaller ones out there, the most widely used and user friendly ones are these:

| App Name | Price | Network | Image quality |
|----------|-------|---------|---------------|
| [Virtual Desktop](https://www.vrdesktop.net/) | One time purchase | WIFI only | Best | 
| [SteamVR](https://store.steampowered.com/app/250820/SteamVR/) | Free | WIFI only | Good |
| [Meta Quest Link](https://www.meta.com/en-us/help/quest/pcvr/) | Free  | WIFI (Airlink) and USB | Good |

If your network is great, I would highly recommend [Virtual Desktop](https://www.vrdesktop.net/).
It has the best image encoding, resulting in best image quality if your PC can handle it.  
If your network is weak and you are a Meta Quest user, go for USB on [Meta Quest Link](https://www.meta.com/en-us/help/quest/pcvr/).  
If you search for a free option that is also know to be very stable, go for [SteamVR](https://store.steampowered.com/app/250820/SteamVR/).  
Except from Meta Quest Link the installation requires an app both on PC as well as on the headset.

### 5. Install UEVR Deluxe
The latest releases can always be found here on GitHub:  
<a href="https://github.com/oduis/UEVRDeluxe/releases" class="download-link">Download latest UEVR Deluxe release</a>

### 6. UEVR Deluxe - Games page
When starting UEVR Deluxe you will find a list of installed Unreal engine Steam games that *might* work, plus a switcher for the OpenXR runtime - what is it?  
There are two protocol standards to transfer VR graphics data: OpenVR is the old one. Some older headsets run OpenVR natively, and SteamVR was first built on it.
The newer version and recommended protocol is OpenXR. Using OpenXR you can decide what linking app should handle your OpenXR graphics. If you have more than one installed (e.g. to try out different options), choose the one to start the game with here. It is a global option for *all* apps using OpenXR on your PC, not just UEVR Deluxe.
After selecting your OpenXR runtime (if necessary), just click the game to start.

### 7. UEVR Deluxe - select a profile
You need a profile telling UEVR how to handle the game, how to connect to your controller e.g. to your weapon etc.
Just hit "Search online" on this page. You will get a list of profiles submitted and tested by the community (since we are at the start there are not many games supported). Just select a profile that looks good and hit the "Install" button.  
If there is no profile you can create a simple one yourself. Hit the "Add profile" button and select the options. Typically you would try the most performant options first. If the game crashes or shows other graphical issues, go for some more conservative settings.

### 8. UEVR Deluxe - start the game
Make your that you link app is running and you are connected via VR headset to your PC *before* hitting the launch button.  
UEVR will start the game (if it is not already running) and injects UEVR into game. Continue in your headset.  
First UEVR shows a menu in-game. You can hide the menu using the "Insert" ("Ins") key on your keyboard, or by pressing both joystick buttons simultaneously.

### 9. Mastering in-game controls
If the game supports gamepads, you VR controllers will function like a gamepad. You can typically use the joystick and the A button to navigate the menus:

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

Not the counterintuitive mapping of the buttons B/X/Y.
You can typically also play with the keyboard and mouse, using just the VR 3D view.

### 10. Connecting your controllers motion controls
Connecting your 3D controllers to e.g. your hand or weapons greatly increases the immersion (6DOF).
However, if you have no preset profile from the "Search online" database, it is pretty complex to set up.
See some [Youtube in depth tutorials](https://www.youtube.com/watch?v=4ccaX8Hr1JU) for more details.
