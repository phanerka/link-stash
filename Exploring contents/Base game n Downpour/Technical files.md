### Saves  
`%userprofile%\AppData\LocalLow\Videocult\Rain World`

??? TODO whats that  
https://gist.github.com/derofim/117566f49ebe1aa89c3b9079693db2f8

Save editor: https://github.com/Ved-s/RainState  
https://github.com/Fnafgameur/RwSavEditor/releases/tag/First  
https://github.com/Vultumast/RainWorldSaveEditor  
(TODO check if it still works)

##### Sandbox save file structure

Honestly..... I don't know why you'd need it since you can spawn creatures via Beasmaster / DevConsole mods or unlock all objects via [[Coding/Tips#Using cheat codes|cheat codes]]. But if you *do* need to read save files manually...  
![[sandbox-save.png]]  
(source: [RW Main](https://discord.com/channels/291184728944410624/296133304632213504/505218239853363200))  
##### Object IDs

Creatures:  
(can be looked up in `CreatureTemplate.cs -> Type` class)  
DP: `MoreSlugcatsEnums.cs -> CreatureTemplateType`  
Data for creatures: `CreatureSymbol.cs -> IconSymbol.IconSymbolData SymbolDataFromCreature(AbstractCreature creature)`

> [!example]- List of creatures' ID  
> `0-0-0` : "StandardGroundCreature"   
> 1-0-\#: "Slugcat" slugcat  
> - number corresponds to player number starting with 0, so player1 = 1-0-0
> 
> 2-0-0 : "LizardTemplate" ?   
> 3-0-0 : "PinkLizard" purple lizard   
> 4-0-0 : "GreenLizard" green lizard   
> 5-0-0 : "BlueLizard" blue lizard   
> 6-0-0 : "YellowLizard" yellow lizard   
> 7-0-0 : "WhiteLizard" white lizard   
> 8-0-0 : "RedLizard" red lizard   
> 9-0-0 : "BlackLizard" black lizard   
> 10-0-0 : "Salamander" salamander   
> 11-0-0 : "CyanLizard" cyan lizard   
> 12-0-0 : "Fly" batfly   
> 13-0-0 : "Leech" red leech   
> 14-0-0 : "SeaLeech" blue leech   
> 15-0-0 : "Snail" pop-snails   
> 16-0-\# : "Vulture" vulture  
> 17-0-0 : "GarbageWorm" garbage worm   
> 18-0-0 : "LanternMouse" lantern mice   
> 19-0-0 : "CicadaA" white squidcada   
> 20-0-0 : "CicadaB" squidcada   
> 21-0-0 : "Spider" spiders   
> 22-0-0 : "JetFish" jetfish   
> 23-0-0 : "BigEel" leviathan   
> 24-0-0 : "Deer" rain deer   
> 25-0-0 : "TubeWorm" grapple grub   
> 26-0-0 : "DaddyLongLegs" daddy long legs   
> 27-0-0 : "BrotherLongLegs" brother long legs   
> 28-0-0 : "TentaclePlant" living kelp   
> 29-0-0 : "PoleMimic" mimic   
> 30-0-0 : "MirosBird" miros bird   
> 31-0-0 : "TempleGuard" depths guardian   
> 32-0-\#: "Centipede"  
> - 32-0-1 as smallest, 32-0-3 as largest; no 0es
> 
> 33-0-0 : "RedCentipede" red centipede   
> 34-0-0 : "Centiwing" flying centipede   
> 35-0-0 : "SmallCentipede" infant centipede   
> 36-0-0 : "Scavenger" scavenger   
> 37-0-0 : "Overseer" overseer   
> 38-0-0 : "VultureGrub" vulture grub   
> 39-0-0 : "EggBug" egg bug   
> 40-0-0 : "BigSpider" wolf spider   
> 41-0-0 : "SpitterSpider" spitter spider   
> 42-0-0 : "SmallNeedleWorm" infant needlefly   
> 43-0-0 : "BigNeedleWorm" adult needlyfly   
> 44-0-0 : "DropBug" dropwig   
> 45-0-0 : "KingVuture" king vulture   
> 46-0-0 : "Hazer" hazer   
> 
>  **\[⬇ MSC ONLY]**  
>  
> 48-0-0 : "MirosVulture"  
> 49-0-0 : "SpitLizard"  
> 50-0-0 : "EelLizard"  
> 51-0-0 : "MotherSpider"  
> 52-0-0 : "TerrorLongLegs"  
> 53-0-0 : "AquaCenti"  
> 54-0-0 : "HunterDaddy"  
> 55-0-0 : "FireBug"  
> 56-0-0 : "StowawayBug"  
> 57-0-0 : "ScavengerElite"  
> 58-0-0 : "Inspector"  
> 59-0-0 : "Yeek"  
> 60-0-0 : "BigJelly"  
> 61-0-0 : "SlugNPC"  
> 62-0-0 : "JungleLeech"  
> 63-0-0 : "ZoopLizard"  
> 64-0-0 : "ScavengerKing"  
> 65-0-0 : "TrainLizard"

Items:  
(can be looked up in `AbstractPhysicalObject.cs -> AbstractObjectType` class)  
DP: `MoreSlugcatsEnums.cs -> AbstractObjectType`  
Data for items: `ItemSymbol.cs -> IconSymbol.IconSymbolData? SymbolDataFromItem(AbstractPhysicalObject item)`  
> [!example]- List of items ID  
> 0-0-0 : "Creature"  
> 0-1-0 : "Rock" rock   
> 0-2-\# : "Spear" spears  
> - 0-2-0 : spear   
> - 0-2-1 : explosive spear  
> - 0-2-2 : electric spear (MSC)  
> - 0-2-3 : firebug spear? (MSC) spear.hue != 0f  
>   
> 0-3-0 : "FlareBomb" flashbang   
> 0-4-\# : "VultureMask" vulture masks  
> - 0-4-0 vulture mask   
> - 0-4-1 king vulture mask  
> - 0-4-2 scav chief mask (MSC)   
>   
> 0-5-0 : "PuffBall" gas apple   
> 0-6-0 : "DangleFruit" pupa fruit   
> 0-7-0 : "Oracle"  
> 0-8-\# : "PebblesPearl" lore pearl   
> 0-9-0 : "SLOracleSwarmer" neuron   
> 0-10-0 : "SSOracleSwarmer" moon neuron   
> 0-11-# : "DataPearl" pearl   
> 0-12-0 : "SeedCob"  
> 0-13-0 : "WaterNut" water nut   
> 0-14-0 : "JellyFish" jellyfish   
> 0-15-0 : "Lantern" lantern/glowstone   
> 0-16-0 : "KarmaFlower" karma flower   
> 0-17-0 : "Mushroom" mushroom   
> 0-18-0 : "VoidSpawn"   
> 0-19-0 : "FireCrackerPlant" explosive fern   
> 0-20-0 : "FlyMold" orange mold   
> 0-21-0 : "FlyLure" batnip   
> 0-22-0 : "ScavengerBomb" explosive   
> 0-23-0 : "SporePlant" swarm cone  
> 0-24-0 : "AttachedBee"   
> 0-25-0 : "EggBugEgg" eggbug egg   
> 0-26-0 : "NeedleEgg" needlefly egg   
> 0-27-0 : "DartMaggot" spitter spider dart  
> 0-28-0 : "BubbleGrass" bubblegrass   
> 0-29-0 : "NSHSwarmer" green neuron   
> 0-30-0 : "OverseerCarcass" overseer eye  
> 0-31-0 : "CollisionField"  
> 0-32-0 : "BlinkingFlower"  
> 
>  **\[⬇ MSC ONLY]**  
>  
> 0-33-0 : "JokeRifle"  
> 0-34-0: "Bullet"  
> 0-35-0: "SingularityBomb"  
> 0-36-0: "Spearmasterpearl"  
> 0-37-0: "FireEgg"  
> 0-38-0: "EnergyCell"  
> 0-39-0: "Germinator"  
> 0-40-0: "Seed"  
> 0-41-0: "GooieDuck"  
> 0-42-0: "Lilypluck"  
> 0-43-0: "GlowWeed"  
> 0-44-0: "MoonCloak"  
> 0-45-0: "HalcyonPearl"  
> 0-46-0: "DancelionPeach"  
> 0-47-0: "HRGuard"

PORLS  
DP: `MoreSlugcatsEnums.cs -> DataPearlType`  
> 1 "Spearmasterpearl"  
> 2 "SU_filt"   
> 3 "SI_chat3"  
> 4 "SI_chat4"  
> 5 "SI_chat5"  
> 6 "DM"  
> 7 "LC"  
> 8 "OE"  
> 9 "MS"  
> 10 "RM"  
> 11 "Rivulet_stomach"  
> 12 "LC_second"  
> 13 "CL"   
> 14 "VS"  
> 15 "BroadcastMisc"  
##### Steam Cloud saving  
Conditions for files to be stored in Steam Cloud  
https://steamdb.info/app/312520/ufs/  
Your files that are stored in Steam Cloud  
https://store.steampowered.com/account/remotestorageapp/?appid=312520

### Logs  
yeah i blatantly stole descs from ;allthelogs pls spare me  
> [!warning] All logs are cleared on game restart. Make sure to save them in time.  
> Another option is to install [LogManager](https://steamcommunity.com/sharedfiles/filedetails/?id=3138158069) mod and configure it. It also changes logs' locations to `idk i forgor`, however.

> [!tip] Enabling live `LogOutput.log` logs: [[Coding/Tips#Live logs|coding tips]]

**TODO: FINISH IT**  
##### LogOutput log  
`Rain World\BepInEx\LogOutput.log`  
Created by BepInEx, a Unity mod loader.  
> [!info] if more that one instance are running on a single PC:  
> second one will have `LogOutput.log.1` name, third one `LogOutput.log.2`, etc.   
##### CustomRegionsSupport log #crs   
`Rain World\RainWorld_Data\StreamingAssets\crsLog.txt`  
Useful for lediting.   
Resolving issues with it: [[Connecting rooms]]  
##### exception log  
`Rain World\exceptionLog.txt`  
Collects all errors that occurred in game. If no errors occur, it won't be created.   
##### console log  
Logs what is loading and happening in the game.  
`Rain World\consoleLog.txt`