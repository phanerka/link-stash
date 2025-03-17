> [!warning] Remix "Alpha Reds" option seems to change red lizard's variations (source: bald lizard bug in meadow; [message](https://discord.com/channels/1094716194180841602/1094730628970320044/1320268178680582215) in Rain Meadow server).

### Creature variations  
##### Lizards  
Wiki: https://rainworld.miraheze.org/wiki/Lizards#Attribute_Generation  
Make sure to also check pages for specific lizard's types (e.g.: [green lizard](https://rainworld.miraheze.org/wiki/Green_Lizard#Variants_&_Attributes)) for more details.

https://docs.google.com/presentation/d/1cvSBNvqKPz6rGZoNMvfQ8mzaArgdUfiPu-fxIcPTAZ8  
##### Scavengers  
Screenshots of scavs with ID 1-10999 (yes, *11 000 pictures*.)  
https://drive.google.com/file/d/1uMbi7PP_2Dl_VeahhEmMDAA6N4uve9Gw/view?usp=sharing  
(source: [RW Main](https://discord.com/channels/291184728944410624/385548182102212608/747554089402892298))  
Also, available in [[References#Github images repository|Github images repo]].
### Creature IDs
##### Finding ID  
Base game IDs vary from 1,000 to 10,000. For every new creature / item, the game increments ID number by 1.  
However, [IDs expanded](https://steamcommunity.com/sharedfiles/filedetails/?id=3094610084) mod increases ID range up to technical limitations (from -2,147,483,648 to 2,147,483,647) and hands out absolutely random ID numbers. 
- [id finder](https://steamcommunity.com/sharedfiles/filedetails/?id=3040378054): if the creature cannot be accessed in game
- [visible ids](https://steamcommunity.com/sharedfiles/filedetails/?id=2934997065): if the creature *exists* in game
- [[Technical files#console log|consoleLog.txt]] records IDs of creatures that weren't saved after cycle end (died, save position was outside of region world coordinates (whatever that means..) )
##### Spawning by ID  
- via [Dev Console](https://steamcommunity.com/sharedfiles/filedetails/?id=2920528044)  mod  
Spawn command: `spawn [creature] ID.-1.[id]`  
- via [biography](https://steamcommunity.com/sharedfiles/filedetails/?id=2985657499) mod (seems to be broken ATM however)