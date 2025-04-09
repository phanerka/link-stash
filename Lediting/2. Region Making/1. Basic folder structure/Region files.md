**List of ALL BASIC files** required for a proper region:
https://rainworldmodding.miraheze.org/wiki/Creating_A_Region

**List of ALL files** possible to be placed in world folder can be found in Tat's userwiki, in `modify\world` ([here](https://rainworldmodding.miraheze.org/wiki/UserWiki:Tat0110#World)) and `world` ([here](https://rainworldmodding.miraheze.org/wiki/UserWiki:Tat0110#World_2)) sections. 

Below is a list of *two most important ones* with clarifications.
## world_xx.txt  
The only file that is **required** for region to work.  
It's settings can be viewed by opening Dev Tools interface, in [Map](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Map-0) tab.  

https://rainworldmodding.miraheze.org/wiki/World_File_Format  #wiki
**Always** has to use the following [format](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Format).

Can be created with [[World editors|FloodForge]] (?)  

Responsible for:  
- defining [[Room types|room types]] via tag (shelters, gates, etc.)  
- connecting rooms  
	Can be customized for various slugcat campaigns\*, via conditional links ([Wiki page](https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/File_Formats#world_xx.txt), [video guide](https://www.youtube.com/watch?v=mQfZwHSxNTA))  
> [!info] Clarification on room connections order
> tbh i'm surprised it's not mentioned in wiki.  
> Connections count starts from **top left corner** of the room and is read by lines (not columns!)
> Lever editor Rained can show pipe numbers... somewhere. wawa
	.
> [!warning] Warning on connecting to rooms
>The following cases will not work in base game (however, can be fixed with [Connection Extension](https://steamcommunity.com/sharedfiles/filedetails/?id=3458613978) mod):
>- connect room to self
>- have 2+ connections from room A to room B
- setting up creature spawns  
	May contain additional creature flags ([Creature Flags](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Creature_Flags) section on Wiki page)  
	Can be customized for various slugcat campaigns\* (the bottom of [Creature Spawns](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Creature_Spawns) section on Wiki page)
	Note that batflies' spawning is defined by room tags, not this section.
> [!warning] Warning on creature spawns  
> Region creature spawns settings are read only **once**, when you enter the region for the first time. Afterwards, they're read from your save.  
> To apply new creature spawns settings, you can:  
> 1) install [Spawn Resetter](https://steamcommunity.com/sharedfiles/filedetails/?id=3232143310) mod (press `BACKSPACE` while dev tools is enabled to activate)   
> 2) add `clean spawns:1` line in [[Cheat codes|setup.txt]]  
> 3) wipe your save and enter the region again.  
- preventing batflies to enter specific room  

## properties.txt
#wiki  
https://rainworldmodding.miraheze.org/wiki/Properties_File  

Responsible for defining:  
- all kinds of region-wide properties for creatures (like color and amount of spawned creatures)  
- settings templates for DevTools to use  
- subregion names  
- room attributes (what creatures are more/less likely or forbidden to visit specific room) 

> [!watcher]- Properties from Watcher regions
> - `mudColor`
> Default: `0.31, 0.19, 0.13`, converted to HEX: `#4f3021`
> Example: `mudColor: 0.6, 0.6, 0.46`
> `fuseSize` (float... yes, for some reason) - Increases superstructure fuses objects.
> Default: `10`
> Example: `heat ducts: 20`
> - `mapSkyLayers`: defines if room boundaries should be rendered as air instead of ground, on the map; pic below. Was hardcoded with closest 2 layers for CC and SI.
> Example: `mapSkyLayers: 0, 2`
> - `cloudsStart` < `cloudsEnd`: define height (altidude) of where clouds show
> idk how its calculated and am lazy to figure out
> what i found is `(mapPos / 3 + 10) x 20 + inRoomPos - (roomSize x 20) / 2`
> maybe `abovecloudsview` room setting also affects it?...
> Default: `20000`, `31400` but not sure
> Example:
> ```
> cloudsStart: 8500
> cloudsEnd: 9500 
> ```
> - `globalCreatureFlags`: `properties.txt` flags but for every spawner.
> 	- creature specific: `globalCreatureFlags: Scavenger-Seed:2837`
> 	- for all creatures: `IgnoreCycle`
> Example of overly complicated working string, to show proper syntax:
> `globalCreatureFlags: Winter, Ignorecycle, Scavenger-Seed:2837, Scavenger-Lavasafe, Pink-Mean:0.7`
> - `hideTimer` (`true`  / `false`): duh
> Default: `false`
> - `proceduralMusicBank`: for using threat text file that isn't called as region. No need to mention `.txt`.
> Example: `proceduralMusicBank: wara`
> - `waterColorOverride` 
> Default: `0.05f, 0.05f, 0.8f`, converted to HEX: `#0d0dcc`
> Example: `waterColorOverride: 0.6, 0.6, 0.46`
> 
> note:
> corruption color by default in watcher timeline is now set to: `0.373f, 0.11f, 0.831f`, HEX: `#5f1cd4`


#### More region properties customization
#crs required!

`properties.txt`:
- general properties  
https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#Region-Properties  
- overseers related properties  
https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/CustomProjections.md  

`MetaProperties.txt`:
https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#metaproperties
