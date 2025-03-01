Mod ID: `yea`

I made something :>  
https://gist.github.com/phanerka/3618d34c26e07da20d1f4456bcaa9da0  
all future changes will go directly there!!!

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

# Meadow mode music support for custom regions  
Spreadsheet with music distribution in base regions:  
https://docs.google.com/spreadsheets/d/1rg14d7qPAnuyraE7zkSZvkA_8_6gDy_nrsypO1f6MaQ/edit  
Region that have no Meadow support will have **Shoreline** settings by default \[TBA next version].

**\[ISTG THE FORMATTING ISNT BROKEN FOR ME AND I WONT TRY FIXING IT AAAAAAAAAAAAAAAAA]**

*! The file structure is going through an overhaul. Described structure will work only post next version of Meadow (v0.2.0)*  
To configure music, you'll have to add ``meadowPlaylist.txt`` file to `your-mod-name\world\xx\` directory.  
You'll need to define on separate line:  
- vibe zone properties  
Vibe zone is a special in-game room that has procedural music in it. You're free to warp to it anytime via pause menu.  
 Define through comma:
 - room name that will be vibe zone   
 - minimum radius of vibe zone (relies on world coordinates)
 - maximum radius of vibe zone
 - waveform value (acceptable: ``Trisaw``, ``Clar``, ``Litri``, ``Sine``, ``Bell``)  
- songs playlist for area outside vibe zone  
List of all songs can be found inside meadow mod folder, i.e. :  
`Steam\steamapps\workshop\content\312520\3388224007\music\songs\`

There can be more than one vibe zone in a single region (most base regions have only one though), and you will be warped to the closest one in game.

Outer Expanse's `meadowPlaylist.txt` file as example:  
```  
OE_TREETOP,2800,4800,Sine  
Eyes Vain  
Woodback  
me  
Cascen  
Folkada  
Gray Orange  
Void Genesis  
Grasp  
71104  
Swan ode  
OE_TOWER06,1000,2400,Litri  
indufor  
Eyto  
Ones  
Icy Parchment  
tredjeplanen  
Significance  
Pedal Petal  
Slightly Ill  
Nevertop Side  
Purple Puff  
New and new  
```

# Adding dependencies and blacklist  
TBA  
Keep looking after this PR  
https://github.com/henpemaz/Rain-Meadow/pull/645  
but basically, there will be .json file :D  
 