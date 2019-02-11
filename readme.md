Mod or .ASI Loader for THAW
===================


Use mods in Tony Hawk's American Wasteland. This is the same like it's available for other popular games.
Its like any other .ASI loader.
(Modding support (script hooking) is not ready and we got everything on hold now.)

*IMPORTANT* Right now, I am not working with thaw -> but im still developing my multiplayer mod.
Unless someone else knows his stuff and reverses the game on its own, or has something for thaw done yet there's no mod currently developed or at least working for/with this as far as I know, except my special meter keeper.

:wrench: How to install modloader
-------------------

 - Download the latest version from *[releases]* page.
 - Open the downloaded .ZIP file
 - Open Tony Hawk's American Wasteland root folder
 - Place all files from the downloaded .ZIP file inside the game's root folder.
 And your done.


:interrobang: How does it work
-------------------

I decided to write down some information for less expierenced users.

It is basically is an empty .DLL file named exactly like the .DLL file "binkw32.dll" inside the game's folder. It comes with the game - for the game, and is needed for audio/video related things. 

Now that we have one original binkw32.dll and our .dll file named the same, we need to rename the original to something like binkw32Hooked.dll.

Now the game loads my binkw32.dll with my code in it, because it thinks its the one that came with the game. We can now do whatever whe want (and are able to) as long as we redirect all function calls from the game that are bink-functions to the original bink .dll file to let the code operate normally. As soon as our custom made binkw32.dll gets loaded, it finds all other .dll files, but renamed to .ASI - and loads them into the game like any other .dll. 

[releases*]: <https://github.com/michael-fa/thaw-modloader/releases>
