> [!wip] This page is WIP.
> Its supposed to explain what's possible to change for slugcat campaigns. However, here's only a draft ATM; wait until it's made or make it yourself and PR it.

Slugcats have to be named in own way, which might differ from in-game name:
(where to lookup: `SlugcatStats` class, defined as `SlugcatStats.Timeline` objects)

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
> - Watcher: `Watcher`

use Slugcat Randomizer, to see registered scugs


#### (optional) Defining campaign-specific changes
this and below
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/File_Formats#map_xx.txt/map_xx.png




adding rep: default alignments.txt

**campaign-specific customization**
entire region swap: `Equivalences.txt`
room connections: world_xx.txt (via conditional linking); crs adds [4th one](https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#replaceroom)
creature spawns: world_xx.txt
threat music
Room Settings xx_01_settings.txt
Map Files map_xx.png, map_image_xx.txt, map_xx.txt
Region Properties properties.txt
Region Display Names displayname.txt

**conditions based on mod being enabled**


**Connecting to other regions**


can be customized; more info in next section