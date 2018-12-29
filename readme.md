Mod or .ASI Loader for THAW
===================


Use mods in Tony Hawk's American Wasteland. This is the same like it's available for other popular games.
Its like any other .ASI loader. 


Modding support and API
-------------

Besides loading mods, it will soon have build-in debugging functions.
Also, this mod loader is a part of my soon-to-be-announced modding API for THAW.

> **Planned features for modding API:**

> - Access HUD Components
> - Gameplay changes via script injection (scripting)
> - Spawn Objects, Peds and also stream car models
> - DirectX access
> - Support for multiplayer scripting (script natives for thaw's multiplayer mode - for server side host)
    - maybe stream peds / objects to without using different networking??
#### <i class="icon-plus"></i> Install Mods

Installing mods is as easy as dropping downloaded .ASI files for THAW inside the game's root folder.

> C:\Games\THAW\ <- thaw.exe and d3dx9_27.dll should also be located there.

----------


<i class="icon-lightbulb"></i>How to install modloader
-------------------

 1.Download the latest version from **releases** page. [<i class="icon-download"></i>](https://github.com/michael-fa/thaw-modloader/releases)
 2. Open the downloaded .ZIP file
 3. Open Tony Hawk's American Wasteland root folder
 4. Place all files from the downloaded .ZIP file inside the game's root folder.
 And your done.


How does it work
-------------------

I decided to write down some information for less expierenced users.

It is basically is an empty .DLL file named exactly like the .DLL file "binkw32.dll" inside the game's folder. It comes with the game - for the game, and is needed for audio/video related things. 

Now that we have one original binkw32.dll and our .dll file named the same, we need to rename the original to something like binkw32Hooked.dll.

Now the game loads my binkw32.dll with my code in it, because it thinks its the one that came with the game. We can now do whatever whe want (and are able to) as long as we redirect all function calls from the game that are bink-functions to the original bink .dll file to let the code operate normally. As soon as our custom made binkw32.dll gets loaded, it finds all other .dll files, but renamed to .ASI - and loads them into the game like any other .dll. 
