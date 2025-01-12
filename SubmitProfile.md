## How to submit a UEVR Easy Injector game profile to the online database
You have built a battle-tested, working profile? This is how to publish it to the community, so everyone can enjoy your work:

### 1. Test it to make sure quality is good
Many games run with some little glitches, but test it before submitting:
- Play the game yourself for more than just 5 minutes (in cases it crashes e.g. later on cutscenes etc.)
- Even better: Have the community on [Discord UE-Games](https://discord.com/channels/747967102895390741/1062167556129030164) test it

### 2. Add descriptions
Many games need special graphic settings to look good in VR, or need some remarks on what workarounds are needed for glitches. In "Edit profile", hit the "Publish" button. It will auto-generate some templates for ```ProfileMeta.json``` and ```ProfileDescription.md```  
Now click on "Open folder" and edit these two files.

#### 2.1 Edit ```ProfileMeta.json```
Please leave the default filled fields like EXEName alone. Edit these fields:
- ```authorName```  
Add your name here. Again just a short name, not a bio ;-)
- ```gameVersion```  
SHORT text info on what version of the game the profile is tested with. Sometimes game updates require newer profiles, so this is important.
- ```minUEVRVersionDay```  
If your profile needs a newer UEVR version you can state the minimum date of the version (code submission date) here. Leave the default (2024-10-31 for official 1.05) if you have not special needs.
- ```modifiedDate```  
Date when you edited and tested this profile. Pre-filled with todays date.
- ```remarks```  
A SHORT (128 chars max.) remark for this profile. This is shown when the user searches the database. It should helps him to select the right profile. Can be left empty.
Most descriptions go into the MD file, not here.
- ```lateInjection```  
Some game cannot inject from the start, but should inject manually when the user enterd the game. Set this to ```true``` if your game needs it.
- ```nullifyPlugins```  
Some game come with plug-ins that interfere with UEVR. Standard is to not block these plug-ins. If the game needs them and breaks, set it to ```true```

#### 2.2 Edit ```ProfileDescription.md```
This is the full description in [Markdown format](https://www.markdownguide.org/basic-syntax/). You can either edit the file with any text editor, use Visual Studio Code (built in preview support), or one of the many online editors like [Dillinger](https://dillinger.io/).

### 3. Publish the full profile as Zip
After having added the description, hit the "Publish" button again. UEVR Easy Injector will check some basics, delete temporary files like crash dumps and logs, and pack up a ZIP for you.  
The packed profile will have some settings resetted that might be user dependent (e.g. log level, enable depth buffer), but if will leave your local profile alone. So it is NOT the same as zipping the folder yourself ;-).

### 4. Submit on Discord
Now post this to the [Discord UE-general channel](https://discord.com/channels/747967102895390741/947806014344925274). Add the two UEVR Easy Injector admins @Pande4360 and @ODuis to make sure it's read. We'll check it briefly and upload it to the clouds database.  
  
### :-) Thanks for helping the community!
