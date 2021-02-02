Overview
--------

----------------------------------
All credit for the actual mod goes to the original AliasIsolation mod creator (https://github.com/aliasIsolation/aliasIsolation). I only changed the hooking code to work with the Epic version (it might actually work with other non-Steam clients, but I only tested with Epic).
----------------------------------

Alias Isolation is a mod for Alien: Isolation. It adds temporal anti-aliasing into the shipped game, and fixes a few small issues with the rendering.

The mod works by injecting itself into the executable, and hijacking D3D11 calls. It replaces a few shaders, and injects some of its own rendering.

This version is modified for the Epic store release - download the other version at https://github.com/aliasIsolation/aliasIsolation for non-Epic versions. It loads only the Alias Isolation mod - not the cinematic tools. 

Usage
-----
1. Download the .zip file from https://github.com/Samlis/AliasIsolationForEpicGamesStore/releases/tag/1.0

2. Save the mod files in a non-system directory. It could be "Program Files", or "My Documents", or anything else as long as no special permissions are required to access that direcotry. If you're using a pre-packaged release, please unzip it rather than launching the mod from within the zip.

3. Execute "epicisolation.cmd [path to AI.exe]" from Windows command-line. You have to pass in the path to your Alien Isolation installation folder as the parameter to the script. So, for example, if your installation folder is C:\Games\AlienIsolation, you would run the .cmd like this:
epicisolation.cmd C:\Games\AlienIsolation\AI.exe

That's it - the mod should be on by default and you should see the "Alias Isolation" logo in the top-left corner once you load a game.


Video Settings
--------------

Anti-aliasing must be set to SMAA T1x.
Chromatic Aberration must be disabled.
Motion blur must be enabled.


Runtime toggle
--------------

To disable the mod at runtime, hit "Ctrl+Delete". To re-enable it, hit "Ctrl+Insert".

More information at https://github.com/aliasIsolation/aliasIsolation
