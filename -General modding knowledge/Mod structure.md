AKA info useful for ANY mod creation

> [!warning] Warning on proper text file formatting
> Every text file in the mod *must* have:
> - `CRLF` as line sequence for ending
> 	Saving in `Notepad` is safe, however this might be an option in other text editors
> - `UTF-8` as encoding
> Otherwise, the file might end up causing errors for the game.

# Basic setup
All local mods are put in a folder in:
`Rain World\RainWorld_Data\StreamingAssets\mods\`
The name of the folder can be *anything* and doesn't really affect anything.

Below list of files that are useful for *any* mod.
## Mod thumbnail
*Is optional.*
### Requirements
Mandatory: 
- name: `thumbnail.png`
- up to `1 MB` size

Recommended: 
- aspect ratio: `16:9`
- size: at least `640x360`
	Size used by base game and DLC mods: `676 x 380`

(source: [Wiki page](https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Mod_Directories#ModInfo_JSON)) 
## Mod description file 
*Defines basic mod info; is used by Remix.*

Name: `modinfo.json`
List of available keys:
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Mod_Directories  

# Folder structure  
#wiki
https://rainworldmodding.miraheze.org/wiki/UserWiki:Tat0110

# Targeting multiple game versions
```
ModName
├── modinfo.json
├── newest
│   └── plugins
│       └── mod1.dll
├── v1.10.0
│   └── plugins
│       └── mod2.dll
└── v1.9.15b
    └── plugins
        └── mod3.dll
```

(source: [RWMA](https://discord.com/channels/1083481230839922688/1083483097145819348/1355701132990742718))