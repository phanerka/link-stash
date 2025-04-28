*The following page concerns room files only. For everything else, refer to [[Ways to edit in-game files|this]] page.*

Region project files are located in the Warehouse. Render them manually and put in the folder n stuff
> [!info] Some level editors like Rained supply with region projects by default.

Contains modded regions project files as well.
> [!warning] Disclaimer on using MODDED regions project files
> **Make sure you read [this](https://github.com/solaristheworstcatever/The-Level-Editor-Warehouse/blob/main/Please%20read%20this%20if%20you%20are%20installing%20the%20region%20files.txt) before you use any of region packs.**
**You may use `Deserted Wastelands` (`DW`) region ONLY for reference.**


https://solaristheworstcatever.github.io/Repo-Site/levels.html
https://github.com/solaristheworstcatever/The-Level-Editor-Warehouse/tree/main/LevelEditorProjects


# Replacing something in particular
*i mean, it's probably possible to modify text files but are you sure it's worth the effort?*

Entire section uses `XX_A01` room as example room. It will be different in your case.
### Room text file
`xx_a01.txt` is responsible for main room properties, AI pathfinding data and interactable part of the room (tiles included).
This way, its possible to change:
- tiles location
- poles location
- batfly spawner location
- amount and location of pipe connections
- water level
- wormgrass :3
> [!info] Note on wormgrass
> Wormgrass can also be added via RegionKit as Dev Tool object, in `RegionKit-Gameplay` tab.
> It doesn't mean you can *edit* worgrass added by room text file, though.
- manually placed rocks and spears

That's not a full list. For explanation how data is stored and all values meaning, refer to [[Rooms#text files|this]] page.
##### AndrewFM's Unofficial Level Editor
#utils
*wawa*
https://ln5.sync.com/dl/55a36f020/ab9tsrvb-pawzct9a-cevwrdgn-2pkthfz2/view/default/10520072550004
### Room image file
`xx_a01.png`
Responsible for purely visual part of the room.
Editing manually is hard and not recommended but described [[Manual editing|here]].

### Room settings text file
It's defined in `xx_a01-settings.txt` file.
Changing room palette, objects, etc; [[I want to use a thing from that room!|this]] page might help you to find the object you need.
Just use Dev Tools in game to modify it.
