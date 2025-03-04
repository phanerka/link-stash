Whoa, that will take a lot of time and effort... but, good luck!   

Regarding mod folder structure, refer to [[Mod structure]] (duh).
## World editors  
World editor by Bro: #utils   
https://github.com/Bro748/World-Editor/releases/tag/MSC-1.01 ([guide](https://www.youtube.com/watch?v=MgeEBM9EKS4))

FloodForge: #utils  
https://github.com/Haizlbliek/FloodForge

To reveal entire region map in game, add `reveal map` to [[Cheat codes|setup.txt]]  
## Region files
**List of ALL files for proper region making:**
https://rainworldmodding.miraheze.org/wiki/Creating_A_Region

Below is a list of *just some of them* with clarifications.
#### world-xx.txt  
The only file that is **required** for region to work.  
Can be created with FloodForge (?)  
It's settings can be viewed by opening Dev Tools interface, in [Map](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Map-0) tab.  

https://rainworldmodding.miraheze.org/wiki/World_File_Format  #wiki
**Always** has to use the following [format](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Format).

Responsible for:  
- defining room types via tag (shelters, gates, etc.)  
- connecting rooms  
	Can be modified for specific slugcat campaigns\*, via conditional links ([Wiki page](https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/File_Formats#world_xx.txt), [video guide](https://www.youtube.com/watch?v=mQfZwHSxNTA))  
> [!Warning] Warning on room connections
> tbh i'm surprised it's not mentioned in wiki.  
> Connections count starts from **top left corner** of the room and is read by lines (not columns!)
> Lever editor Rained can show pipe numbers... somewhere. wawa
- setting up creature spawns  
	May contain additional creature flags ([Creature Flags](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Creature_Flags) section on Wiki page)  
	Can be modified for specific slugcat campaigns\* (the bottom of [Creature Spawns](https://rainworldmodding.miraheze.org/wiki/World_File_Format#Creature_Spawns) section on Wiki page)
	Note that batflies' spawning is defined by room tags, not this section.
> [!warning] Warning on creature spawns  
> Region creature spawns settings are read only **once**, when you enter the region for the first time. Afterwards, they're read from your save.   
> To apply new creature spawns settings, you can:  
> 1) install [Spawn Resetter](https://steamcommunity.com/sharedfiles/filedetails/?id=3232143310) mod (press `BACKSPACE` while dev tools is enabled to activate)   
> 2) wipe your save and enter the region again.    
> 3) ... `clean spawns` in [[Cheat codes|setup.txt]]? maybe? need to verify  
- preventing batflies to enter specific room  

\* Slugcats have to be named in own way, which might differ from in-game name:
> [!example]- List of slugcat naming
> - Monk: `Yellow`
> - Survivor: `White`
> - Hunter: `Red`
> - Artificer: `Artificer`
> - Gourmand: `Gourmand`
> - Rivulet: `Rivulet`
> - Spearmaster: `Spear`
> - Saint: `Saint`
> - ???: `Inv`
##### Mod conditional connections and creature spawns 
#crs required.
Can modify pipe connections and creature spawns (bruh i am repeating myself)
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
## Pre-release TO-DO  
#### Region naming (acronym)  
Acronym is 2-letter identifier for a region.
If someone gets 2 regions with same acronyms.... Eh, they better not. Trust me.
> [!info] Note on acronyms
> Recently, a [mod](https://steamcommunity.com/sharedfiles/filedetails/?id=3412393061) was released that allows to use more than 2 letters for acronym. Yay!  

List of base game regions' acronyms:
https://rainworld.miraheze.org/wiki/User:Alphappy/Region_codes  

##### Region lease 
#sheets  
https://docs.google.com/spreadsheets/d/14wt42_ZalI5di8zpUFx3WvPWldC_L7SwIbgb_TxOpUk/edit   
*Is used to make all regions compatible with each other.* TODO holy shit im so bad at phrasing
Once you're confident with own acronyms, you'll need to request access to the document (submit [this](https://forms.gle/gdaGmLJuBJb4LvMS7) form) and add own values. 

Includes:  
- Connections to vanilla regions  
- Connections to modded regions  
- Palette allocation chart  
- Token usage chart (blue/gold)  
- Region acronym chart

##### Acronym availabilty check
#utils  
Pulls info from spreadsheet.
https://rainworld-region-lease-improved.glitch.me/

##### Mass renaming acronym in mod folder
#utils  
if you ever decide to change region name during development, this might help you to do it quickly.  
https://github.com/glebi574/rw-fix-region-acronyms
#### (optional) Defining campaign-specific changes
this and below
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/File_Formats#map_xx.txt/map_xx.png
#### (optional) Connecting to other modded regions  
#crs only.  

First, check if the connection you want to use is free: [Mod-mod connections tab](https://docs.google.com/spreadsheets/d/14wt42_ZalI5di8zpUFx3WvPWldC_L7SwIbgb_TxOpUk/edit?gid=758721855#gid=758721855) in Region Lease speadsheet

Ask region mod authors for permissions to connect your region to theirs.  
After they agree, check this  
https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#pearls

##### Region baking  
just a friendly reminder to [bake](https://rainworldmodding.miraheze.org/wiki/Creating_A_Region#Baking) your rooms.  
You can also bake via Remix menu in RegionKit  
i need to add regarding debugging..... ouf todo

## Post-release TO-DO  
When you finish the region, you'll likely want its map to be shared.  
https://seroen.github.io/Seroens-Repo/Dist/Tools/Cornifer.zip  
Check this and reach out Alduris to post your region map. 

##### Making static image map

  
##### Map exporter beta  
> Makes interactive maps. The interface is in the remix menu. Instructions are included there, but here's the general gist of things:  
> 1. Run the screenshotter for the regions/slugcats of your choice.  
> 2. Use the editor to edit the map in case of overlapping or unpositioned rooms. The map takes from the dev view map in dev tools, NOT the canon view (in-game map).  
> 3. Run the generator to turn the map into tiles.  
> 4. Run the local server in the export tab to view it in-browser. The export feature is not done yet.  
>   
> Permalink to download the latest version of the beta: https://github.com/alduris/MapExporter/releases/latest  
> If you receive an error or the screenshotter stops running without closing, please upload LogOutput.log, LogOutput.log.1, and, if it exists, exceptionLog.txt

(source: [RWMS](https://discord.com/channels/1237826015829557400/1273913033831350296/1273913775732555816))  
