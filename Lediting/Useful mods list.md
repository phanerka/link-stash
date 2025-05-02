> [!warning] Warning on mod dependencies in the collection
> If you subscribe to separate mods, make sure you'll download dependencies as well; Steam doesn't check them on Collections page.

*Mod collection in Steam Workshop is [here](https://steamcommunity.com/sharedfiles/filedetails/?id=3460033646).*

>[!watcher] sorry but watcher ate some of them
> Due to recent update of the game, some mods might not work.
> Confirmed to be broken mods are crossed out. If they stay broken for too long without a way to be fixed, while being potentially useful, they will move to "Cancelled projects" section.

*That's not entire list. Some mods are more niche and mentioned in "How-to"s*
##### Must-haves
- Dev Tools ([[Dev Tools|main page]]): a classic. You cannot finish a room without Dev Tools. Literally.
- [Custom Region Support](https://steamcommunity.com/sharedfiles/filedetails/?id=2941565790) ([docs](https://github.com/Bro748/Custom-Regions/tree/dp-release), older version of which were yoinked to [wiki](https://rainworldmodding.miraheze.org/wiki/Custom_Regions_Support) *bruh*): aside from providing features to make a decent region (custom pearls, threat music, landscape art), adds a separate log which helps with game crashes / freezes troubleshooting during room creation process.
- [Warp Menu](https://steamcommunity.com/sharedfiles/filedetails/?id=2920446893) (outdated [Wiki page](https://rainworldmodding.miraheze.org/wiki/Warp)): allows to teleport to any region / room in game. Extremely useful when adding rooms in Story.

##### Recommended
- [Better Decals](https://steamcommunity.com/sharedfiles/filedetails/?id=3241776574): allows decals to be more customized.
- [Stuck in a Cycle](https://steamcommunity.com/sharedfiles/filedetails/?id=3035801552): helps to edit the room with Dev Tools without worries that rain will eventually come. More info [[2+. Setting up environment#Rain disable|here]].
- [Room Screenshot](https://steamcommunity.com/sharedfiles/filedetails/?id=3125783486): self-explanatory. For general room recording topic, refer to [[Recording rooms|this]] page.
- ~~[Palette Creator](https://steamcommunity.com/sharedfiles/filedetails/?id=2959458351)~~: allows to easily create palettes. For general palette creation topic, refer to [[Custom palette|this]] page.
- [Spawn Resetter](https://steamcommunity.com/sharedfiles/filedetails/?id=3232143310): to reset creature spawns in the region. More info [[Region files#world_xx.txt|here]] in second warning block.

##### Dependencies
> [!warning] Friendly reminder to add following mods to [[Mod structure|modinfo.json]], if you're going to use them

- [RegionKit](https://steamcommunity.com/sharedfiles/filedetails/?id=2920439476) ([features](https://github.com/Rain-World-Modding/RegionKit/blob/main/README.md), [docs](https://github.com/Rain-World-Modding/RegionKit/tree/main/docs)): a "unified dependency and object kit"; provides a lot of various features, starting with more room customization and ending with more objects for DevTools.
	In case you hate the little yellow guy in bottom left corner, there's a [mod](https://steamcommunity.com/sharedfiles/filedetails/?id=3141904462) that sends em to the void dimension.
- [Lunacy](https://steamcommunity.com/sharedfiles/filedetails/?id=2930814260) ([docs](https://github.com/Nacu0021/Lunacy)): yet another feature library.
	*Requires POM and Fisiobs.*
- [KO Utils](https://steamcommunity.com/sharedfiles/filedetails/?id=3443204574) :3
- [Coloured Lanterns](https://steamcommunity.com/sharedfiles/filedetails/?id=3401635588): self-explanatory.
- [Connection Extension](https://steamcommunity.com/sharedfiles/filedetails/?id=3458613978): allows to have 2+ connections between same rooms and connect a room to self.
- [Dawn](https://steamcommunity.com/sharedfiles/filedetails/?id=3417857252): TBA
	*Requires Downpour DLC.*

- ~~[The M4rbelous Entity Pack](https://steamcommunity.com/sharedfiles/filedetails/?id=3311812030)~~: biggest custom creatures and items pack.

All other modded creatures and items can be found on RW Mods Wiki ([Creatures list](https://rainworldmods.miraheze.org/wiki/Creatures) and [Items list](https://rainworldmods.miraheze.org/wiki/Objects)).
*Make sure to ask mod authors for permission to use them!*


##### Cancelled projects
RIP 🫡
This section is for mods which, while had a great potential, unfortunately never came out and never will.
It doesn't mean anyone can fix them, though; check what license is used in Github repository, otherwise ask authors for permissions to modify.
- [Atmo](https://steamcommunity.com/sharedfiles/filedetails/?id=2920450391) ([Github repo](https://github.com/thalber/Atmo)): scripting mod.
- [Breadway](https://steamcommunity.com/sharedfiles/filedetails/?id=2993825578) ([Github repo](https://github.com/thalber/Breadway)): welp.
- Rain Angle effect ([demo](https://www.youtube.com/watch?v=8-oeALLoL4A), [Github repo](https://github.com/LudoCrypt/TurnRain)): yep.
	Announcement [here](https://discord.com/channels/1083481230839922688/1083483097145819348/1236746634235482122) (RWMA), a quick overview of how it works [here](https://discord.com/channels/1083481230839922688/1083485771949949019/1232426391522381875) (RWMA).
- Voxel World (demo: [one](https://www.youtube.com/watch?v=3lSxs1IKxeg), [two](https://www.youtube.com/watch?v=1c4yAcd2XWw), [three](https://www.youtube.com/watch?v=3lSxs1IKxeg); [Github repo](https://github.com/SlimeCubed/VoxelWorld))
