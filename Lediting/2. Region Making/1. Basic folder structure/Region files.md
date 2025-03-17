**List of ALL files for proper region making:**
https://rainworldmodding.miraheze.org/wiki/Creating_A_Region

Below is a list of *just some of them* with clarifications.
#### world_xx.txt  
The only file that is **required** for region to work.  
It's settings can be viewed by opening Dev Tools interface, in [Map](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Map-0) tab.  

https://rainworldmodding.miraheze.org/wiki/World_File_Format  #wiki
**Always** has to use the following [format](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Format).

Can be created with [[World editors|FloodForge]] (?)  

Responsible for:  
- defining [[Room types|room types]] via tag (shelters, gates, etc.)  
- connecting rooms  
	Can be customized for various slugcat campaigns\*, via conditional links ([Wiki page](https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/File_Formats#world_xx.txt), [video guide](https://www.youtube.com/watch?v=mQfZwHSxNTA))  
> [!Warning] Warning on room connections
> tbh i'm surprised it's not mentioned in wiki.  
> Connections count starts from **top left corner** of the room and is read by lines (not columns!)
> Lever editor Rained can show pipe numbers... somewhere. wawa
- setting up creature spawns  
	May contain additional creature flags ([Creature Flags](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Creature_Flags) section on Wiki page)  
	Can be customized for various slugcat campaigns\* (the bottom of [Creature Spawns](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Creature_Spawns) section on Wiki page)
	Note that batflies' spawning is defined by room tags, not this section.
> [!warning] Warning on creature spawns  
> Region creature spawns settings are read only **once**, when you enter the region for the first time. Afterwards, they're read from your save.  
> To apply new creature spawns settings, you can:  
> 1) install [Spawn Resetter](https://steamcommunity.com/sharedfiles/filedetails/?id=3232143310) mod (press `BACKSPACE` while dev tools is enabled to activate)   
> 2) wipe your save and enter the region again.  
> 3) add `clean spawns` line in [[Cheat codes|setup.txt]]  
- preventing batflies to enter specific room  

##### Mod conditional connections / creature spawns 
#crs required.
Such properties can be set up depending of existence of certain regions / mod being enabled.
https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#region-conditional-lines

#### properties.txt
#wiki  
https://rainworldmodding.miraheze.org/wiki/Properties_File  

Responsible for defining:  
- all kinds of region-wide properties for creatures  
- settings templates for DevTools to use  
- subregion names  
- room attributes (what creatures are more/less likely or forbidden to visit specific room)  
##### More region properties customization
#crs required!  
- general properties  
https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#Region-Properties  
- overseers related properties  
https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/CustomProjections.md  
