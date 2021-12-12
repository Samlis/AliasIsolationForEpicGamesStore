Overview
--------

----------------------------------
All credit for the actual mod goes to the original AliasIsolation mod creator (https://github.com/aliasIsolation/aliasIsolation). I only changed the hooking code to work with the Epic version (it might actually work with other non-Steam clients, but I only tested with Epic). Source code will be added soon.
----------------------------------



Alias Isolation is a mod for Alien: Isolation. It adds temporal anti-aliasing into the shipped game, and fixes a few small issues with the rendering.

The mod works by injecting itself into the executable, and hijacking D3D11 calls. It replaces a few shaders, and injects some of its own rendering.

This version is modified for the Epic store release - download the other version at https://github.com/aliasIsolation/aliasIsolation for non-Epic versions. It loads only the Alias Isolation mod - not the cinematic tools. 

Usage
-----
1. Download the .zip file from the release (https://github.com/Samlis/AliasIsolationForEpicGamesStore/releases/download/1.1/aliasIsolation-EpicGamesStore_R1.1.zip)

2. Save the mod files in a non-system directory. It could be "Program Files", or "My Documents", or anything else as long as no special permissions are required to access that direcotry. If you're using a pre-packaged release, please unzip it rather than launching the mod from within the zip.

3. Make sure the game is NOT running. Execute "epicisolation.cmd [path to AI.exe]" from Windows command-line. You have to pass in the full path to your Alien: Isolation executable as the parameter to the script. So, for example, if your installation folder is C:\Games\AlienIsolation, you would run the .cmd like this:
epicisolation.cmd C:\Games\AlienIsolation\AI.exe
This will run the game and apply the mod.

**NOTE**: Some users have reported that they had to increase the number of attempts at mod injection in order to get it to work. By default, the number is set to 150, which should be plenty enough. If the mod is not triggering for you, it is possible that you may need to increase this value as well. Open epicisolation.cmd and change the number 150 to something higher (one user set it to 500 to get it to work), save and re-run as per step 3.

Injection has to be done this way because it wouldn't work directly via code. For some reason there's a very small window of when the mod properly injects - not too soon and not too late - and these repeated attempts work.

Set the video options as per the "Video Settings" section below and that's it - the mod should be on by default and you should see the "Alias Isolation" logo in the top-left corner once you load a game. It should also work with DLC.

**g_device->CreateTexture2D(&texDesc, nullptr, &tempTex) failed. error / overlay error**:
If you get this error, rename the Overlay folder under your Epic installation to something else, e.g. if your Epic is installed under
C:\Program Files (x86)\Epic Games
rename folder C:\Program Files (x86)\Epic Games\Launcher\Portal\Extras\Overlay to something else, like C:\Program Files (x86)\Epic Games\Launcher\Portal\Extras\OverlayABC.


Video Settings
--------------

Anti-aliasing must be set to SMAA T1x.
Chromatic Aberration must be disabled.
Motion blur must be enabled.


Runtime toggle
--------------

To disable the mod at runtime, hit "Ctrl+Delete". To re-enable it, hit "Ctrl+Insert".

More information at https://github.com/aliasIsolation/aliasIsolation
