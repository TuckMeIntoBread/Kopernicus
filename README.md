﻿Kopernicus
==============================
December 19th, 2021
* Created by: BryceSchroeder and Nathaniel R. Lewis (Teknoman117)
* Actively maintained by: Prestja and R-T-B.
* Formerly maintained by: Thomas P., NathanKell and KillAshley
* Additional Content by: Democat3457, Gravitasi, aftokino, KCreator, Padishar, Kragrathea, OvenProofMars, zengei, MrHappyFace, Sigma88, Majiir (CompatibilityChecker)
* Much thanks to Sarbian for ModuleManager and ModularFlightIntegrator

New in this latest version release-69:

1.)  Upped the value of the minor 1.12.x version check since all seems well with 1.12.3.

Known Bugs:

1.) The ingame shadows without an external mod like scatterer can be glitchy.  It is advisable to use an external mod for best experience at the moment.

2.) Land scatters can appear at incorrect elevations if you don't use Kopernicus option "UsePureStockSCatters," which sadly, only works on pure stock systems.

2.) At interstellar ranges, heat can sometimes behave strangely, sometimes related to map zoom (be careful zooming out). It is best to turn off part heating when traveling far far away.

3.) When zooming out all the way out in map view at interstellar ranges, the navbal furthermore sometimes behaves oddly. We are working on this and nmonitoring all the interstellar bugs actively.

4.) 1.) Very Old craft files may complain about a missing module. This is a cosmetic error and can be ignored. Reload and re-save the craft to remove the error.

Known Caveats:

1.)  The 1.12.x release series works on 1.12.x,1.11.x,1.10.x, and 1.9.x.  The 1.8 release is for 1.8.x.

2.)  Mutlistar Solar panel support requires an additonal config file, attatched to release.

3.)  If you use the "AddWatchdog.cfg" file, A fake celestial body isthen used to fix the distant landing-gear sinking bug.  This body is called "KopernicusWatchdog" and will a.) intentionally keep it's distance from you at all times and is b.) invisible.  The body is usually hidden from in game processes, but this is new territory having to use another moving celestial to correct a bug, so there may be side effects.  Also, Principia does not benefit from this fix at this time, unfortunately.  Those users may try "MakingLessHistory" mod, the old workaround.

4.) When using the ultra/atlas shader, ocean effect customization (color etc) is unreliable.  Please use only high shader level (shader level 2) or lower if working with stock ocean effects.  This does not effect scatterer or other ocean rendering mods. 

About
-----
Kopernicus is a KSP add-on that allows for modification of stock planets and the creation of new planets via modification of the system prefab.  Why is this advantageous you might ask?  Previous planet adder mods, such as Planet Factory, modified the live planetary system and had to keep multiple hacks actively running to provide these worlds.  We strive to provide the least hacky solution by introducing planets into the game in the exact same manner Squad would.  

Kopernicus is a one step process.  It is started before the planetary system is created and rewrites a property called PSystemManager.Instance.systemPrefab.  The game itself then creates *our* planetary system as if it were blessed by Squad themselves.  The mod’s function ends here, and it terminates.  Kopernicus introduced worlds require zero maintenance by third party code, all support is driven entirely by built in functionality.  This yields an incredibly stable and incredibly flexible environment for planetary creation.

One caveat exists that prevents absolute control over a planetary system.  Due to the way Squad defines how launch control and ship recovery work, a planet called Kerbin must exist and must have a reference body id of 1.  While it is easy to provide this scenario, as a star to orbit and a single planet satisfies this, any would be universe architect needs to be aware so they don’t get mystery errors. The displayed name of the body (i.e. the celestialBody.bodyName property) can be changed after the spawn of the PSystem  

Each celestial body in KSP has a property called “flightGlobalsIndex.”  This number does not directly correspond to the reference id, but is related.  Once all of the celestial bodies have been spawned, references to them are written into the localBodies list.  This list is then sorted in increasing order of the flight globals index.  The index the body is located at after the sort becomes the reference body id.

We have yet to see if removing or rearranging the other bodies causes any sort of errors in the science or contracts system.


Instructions
------------
- Copy the contents of the GameData/ folder to KSP’s GameData/ folder
- Launch KSP and enjoy!
- Please report any bugs you may find to either or both of the email addresses above.

Examples
----------
Selectively copy folders inside of [KopernicusExamples/](https://github.com/Kopernicus/KopernicusExamples/) into a GameData/KopernicusExamples/ folder.  There are a number of examples of how to use Kopernicus.
