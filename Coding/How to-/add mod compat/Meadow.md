*For adding region support for Meadow mode, check [[Meadow mode|lediting section]].*

Remix mod ID: `henpemaz_rainmeadow`
Workshop mod ID: `3388224007`

I made something :>  
https://gist.github.com/phanerka/3618d34c26e07da20d1f4456bcaa9da0  
all future changes will go directly there!!!

.... or not.
welp
here it goes back to my doc then ig

to replace remote links to local:  
logOutput.log  
setup.txt

# Meadow compatibility for code mods  
Any kind of compatibility has to be done on non-Meadow end (with exception when its impossible to do so without tweaking Meadow code).

Sync template + guide on mod syncing:  
https://github.com/TheLazyCowboy1/RainMeadowSyncTemplate

A guide on making new game mode based on existing one (here's Arena Mode as example):  
https://github.com/6fears7/Arena-Online/tree/main

### Debugging  
Meadow uses [[Technical files#LogOutput log|logOutput.log]] for logging. If more that one instance are running in same environment, additional ``logOutput.log.N`` files will be created (where N is number of instance - 1).  

Save files are stored in same directory with RW base files:  
`%userprofile%\AppData\LocalLow\Videocult\Rain World`  
- meadow mode: `meadow.json`  
- story mode: ``online_savN``, where N is number of save.  
Story mode save structure is identical to singleplayer save one! Feel free to rename it back and forth to use it for lobbies or singleplayer.  
**Meadow saves are NOT stored in Steam Cloud!** 

Debug info for connections (connected user id, ping) can be found by opening Dev Tools.  
### Getting custom Meadow build  
If you decide to build Meadow on your own, you will be able to test connection locally or do a hidden public playtesting.  
How to set up:  
https://github.com/henpemaz/Rain-Meadow/blob/main/CONTRIBUTING.md

##### Troubleshooting  
Most of issues are described in "CONTRIBUTING.md" file in Meadow repo but there's a bit more niche ones.

There is override for setup.txt that forces `start screen:0` value to automatically create lobby. But it wasn't updated in a while, and is broken now. Please don't use this value, at least for now.

If you use Debug World version from `#modding-resources`: do **NOT** copy ``RainWorld_Data\Managed\Assembly-CSharp.dll`` to Rain World folder! It will break Meadow.  
If you did manage to do that by accident, verify game files to get original library back and reenable Meadow.  
##### Configuration builds  
- ArenaP2P - local debug build with Arena mode available only (e.g. even if you try to host Story, Arena will be run instead)   
- Debug - Steam debug build.   
- FreeRoamP2P - local debug build with Free Roam mode available only.  
There was a mode called "Free Roam" which synced nothing but slugcats' movement and environment settings (rain, food pips, etc.). While it was the first mode that was working (sort of), it wasn't touched for a while, therefore becoming the buggiest of all. Now FreeRoam is hidden in mode select list, and starting FreeRoam lobby is broken at the moment.  
- LocalP2P - local debug build with Meadow mode available only.  
- Release - Steam release build. It's smaller and optimized, compared to debug builds, but likely won't be fitting for real-time debugging. This build is uploaded to Workshop.  
- StoryP2P - local debug build with Story mode available only.

P2P suffix is used for **local builds**, intended for testing networking in same environment. Game instance that is going to host has to be run via Steam, while clients are meant to be launched directly from executable (`Rain World\RainWorld.exe`)

##### Packet loss and delay (ping) simulation  
Local builds have it enabled by default.  
To configure it (or completely disable by setting ``simulatedLoss`` and ``simulatedLatency`` to ``0``), check `Online\Matchmaking\UdpPeer.cs`

##### Playtesting with custom build  
Meadow shows lobbies **only** with same meadow mod version installed.  
To hide all other lobbies for you (and make yours hidden for others at the same time), change `MeadowVersionStr` variable in `RainMeadow.cs` to some another value.  
Don't forget to share modified Meadow build with your playtesters!

### Code examples  
##### List of code mods that support Meadow  
- PearlCat ([Github repo](https://github.com/forthfora/pearlcat))  
- Rotund World ([Github repo](https://github.com/clkursch/Rotund-World))  
- DressMySlugcat (client-sided only) ([Github repo](https://github.com/MatheusVigaro/DressMySlugcat))  
- Revivify Meadow  
- Region Randomizer ([Github repo](https://github.com/TheLazyCowboy1/RegionRandomizer))  
- MoreSlugcatsNerfs ([Github repo](https://github.com/TheLazyCowboy1/MoreSlugcatsNerfs))  
- SwordMod ([Github repo](https://github.com/TheLazyCowboy1/SwordMod))  
- ping me i'll add :3

##### List of mods that add new mode  
- Tag Mode, based on story (?) game mode ([Github repo](https://github.com/henpemaz/RemixMods/tree/master/Tag))  
- Drown, based on arena mode ([Github repo](https://github.com/6fears7/Arena-Online/tree/main/Drown))  
- RATS  
##### List of Meadow addons  
- Pupifier ([Github repo](https://github.com/xamionex/Pupifier))  
- BetterHostControls ([Github repo](https://github.com/TheLazyCowboy1/BetterHostControls))

### Tech support  
Feel free to ask questions in [`#playtesting` -> Mod Porting](https://discord.com/channels/1094716194180841602/1326036277488914523) thread in Rain Meadow server!   
Rain Meadow invite link is attached in [Github repo](https://github.com/henpemaz/Rain-Meadow).

# Adding dependencies and blacklist  
TBA  
Keep looking after this PR  
https://github.com/henpemaz/Rain-Meadow/pull/645  
but basically, there will be .json file :D  
 