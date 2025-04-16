> [!warning] A thing to keep in mind
> In general, it applies to *any* game asset, with some exception of [[Coding/Guides/Loading custom assets/Shaders|shaders]] (they need to be put into AssetBundle). 
> Besides, some assets have got multiple files related to them: 
> - [[Fonts n symbols#How to compile font on ur own|fonts]] (sprite sheet and text file AKA decryptor, more info in compiling font section)
> - [[Sounds|sounds]] (music file and text file that allows to mix sounds)
> 
> And keep in mind that [[How to add in game|music]] and [[Sounds|sounds]] need to use location of respective dummy files, not AssetBundles.

%%
To avoid confusion, i should call every file that is put into modify folder "modification file of X" (X with modification syntax?) probably?...
its very easy to miss out that folder in path.  
%%

Let's assume that path to certain in-game file, starting from `Rain World\RainWorld_Data\StreamingAseets` folder, is `[file_path]`.  
For example, full path to image of `SU_A53` room (`su_a53_1.png`) would be
`Rain World\RainWorld_Data\StreamingAssets\world\su-rooms\`.  
In this case, `[file_path]` would be `world\su-rooms\`.  
### Overriding
**Main Wiki page:**  
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Mod_Directories#Overwriting_Files

If you want to **straight up override** original files, for example:  
- replace room image  
- replace room settings,  

then you put file with *SAME* name as in-game file in `your-mod\[file_path]` directory.  
In case of `SU_A53` image, that would be `your-mod\world\su-rooms\su_a53_1.png`.  
### Modifying
*Works **only** with text files!*  
**Main Wiki page:**  
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Modification_Files

**Unfinished (yet extensive) guide on modification syntax:**  
*by `jonahfagnus`*
https://docs.google.com/document/d/1-n6fcQlVHS_ctQh-lULal8x4FfZ8N0eOWcZJ1G6pP0U/edit  
(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/1273601361870721094))  

*Due to complexity, map merging got own [[In-game map rendering#Merging maps|page]].*

If you want to **change a part of** original files, for example:
- add connection to your own room/region  
- append own songs to song list for arena  
- replace some creature spawns with custom ones,  

then you _will_ have to use modification files.  

ALL modification files require *SAME* name as in-game file BUT have to be put in `your-mod\modify\[file_path]` instead.  
Speaking of example, room images cannot be edited for obvious reasons. Room settings file will be used instead (`su_a53-setings.txt`), which is located in same directory.  
In that case, full path would be `your-mod\modify\world\su-rooms\su_a53-setings.txt`  