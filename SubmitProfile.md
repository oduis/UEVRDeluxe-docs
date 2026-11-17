## How to submit a UEVR Easy Injector game profile to the online database
Have you built a battle-tested, working profile? This is how to publish it to the community so everyone can enjoy your work:

### 1. Test it to make sure quality is good
Many games run with a few minor glitches, so test the profile before submitting it:
- Play the game yourself for more than five minutes, in case it crashes later, for example, during cutscenes
- Better yet, have the community on [Discord UE-Games](https://discord.com/channels/747967102895390741/1062167556129030164) test it

### 2. Add descriptions and metadata
Many games need special graphics settings to look good in VR or require notes about workarounds for glitches. Add this information in "Edit profile."
It is stored in the files `ProfileMeta.json` and `ProfileDescription.md`, which you can edit directly without the GUI.
`ProfileMeta.json` also supports the automatic installation of `.pak` files.

### 3. Publish the full profile as Zip
After adding the description, click "Publish" again. UEVR Easy Injector will check some basics, delete temporary files such as crash dumps and logs, and package a ZIP file for you.
The packaged profile resets settings that may be user-dependent, such as log level and enable depth buffer, but it leaves your local profile unchanged. It is NOT the same as zipping the folder yourself ;-).

### 4. Submit on Discord
Post this to the Flat2VR Discord #UE-games channel for the game. Mention the UEVR Easy Injector admin @oduis_94020 to ensure it is read. I will check it briefly and upload it to the cloud database.
  
### :-) Thanks for helping the community!
