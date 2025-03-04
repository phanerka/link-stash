# Ways of modification

> [!warning] A thing to keep in mind
> Friendly reminder that it works with region files but it might work with literally everything else; in that case, refer to [[import X resource in the game|coding section]].

Let's assume that path to certain in-game file, starting from `Rain World\RainWorld_Data\StreamingAseets` folder, is `%file_path%`.  
For example, full path to image of `SU_A53` room (`su_a53_1.png`) would be
`Rain World\RainWorld_Data\StreamingAssets\world\su-rooms\`.  
In this case, `%file_path%` would be `world\su-rooms\`.


If you want to **straight up replace** original files, for example: 
- replace room image
- replace room settings,  

then you put file with *SAME* name as in-game file in `your-mod\%file_path%` directory.  
In case of SU_A53 image, that would be `your-mod\world\su-rooms\su_a53_1.png`.  
Main Wiki page:  
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Mod_Directories#Overwriting_Files


If you want to **modify** original files, for example:
- add connection to your own room/region
- append own songs to song list for arena
- replace some creature spawns with custom ones,

then you _will_ have to use modification files.  
ALL modification files require *SAME* name as in-game file BUT have to be put in `your-mod\modify\%file_path%` instead.  
Main Wiki page:  
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Modification_Files

Unfinished guide :3  
https://docs.google.com/document/d/1-n6fcQlVHS_ctQh-lULal8x4FfZ8N0eOWcZJ1G6pP0U/edit  
(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/1273601361870721094))  
# Rooms

### Modifying rooms' text file  
This way, its possible to modify:  
- poles location  
- batfly spawner location  
- amount and location of pipe connections  
- water level  
- wormgrass :3
> [!info] Wormgrass can also be modified via regionkit iirc, without having to touch files.  
https://ln5.sync.com/dl/55a36f020/ab9tsrvb-pawzct9a-cevwrdgn-2pkthfz2/view/default/10520072550004  
Modifying manually: [[Rooms#text files]] (WIP!)  

### Modifying rendered image  
This way, you can modify everything else.  
Region project files are located in the Warehouse. Render them manually and put in the folder n stuff 

> [!info] Some level editors like Rained supply with region projects by default.

https://seroen.github.io/Seroens-Repo/regions.html  
https://github.com/Seroen/Seroens-Repo-Files/tree/main/LevelEditorProjects  
### Modifying palette, objects or smth  
use dev tools in game duh  
Maybe [[Lediting/Navigation]] will help you