Mod or .ASI Loader for THAW
===================


Use mods in Tony Hawk's American Wasteland. This is the same like it's available for other popular games.
Its like any other .ASI loader.

:wrench: How to install modloader
-------------------

 - Download the latest version from *[releases]* page.
 - Open the downloaded .ZIP file
 - Open Tony Hawk's American Wasteland root folder
 - Place all files from the downloaded .ZIP file inside the game's root folder.
 And your done.


:interrobang: How does it work
-------------------

The downloaded files are used to do one thing: load an empty bink32 dll with only our code but also / still handles/passes all function calls made from the game to the default dll it's expecting to have loaded, now the one having "hooked" in the name, and so making it possible to run code at the point of when the game tries to call the bink32 file for the first time.

Downsides: * Not the first run code, the game still has own control - until it loads the dll and makes stuff possible.
           * (project wise) no API and stuff
           
No matter what, u can code an dll and use memhax to do your thing -> thats what I was using this for. The base idea was taken from a Fallout mod, I believe.
           

[releases]: <https://github.com/michael-fa/thaw-modloader/releases>
