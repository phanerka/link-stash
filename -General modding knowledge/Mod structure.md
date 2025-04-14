AKA info useful for ANY mod creation

*Mod thumbnail: [[make a mod thumbnail|here]]*

> [!warning] Warning on proper text file formatting
> Every text file *must* have:
> - `CRLF` as line sequence for ending
> 	Saving in `Notepad` is safe, however this might be an option in other text editors
> - `UTF-8` as encoding
> Otherwise, the file might end up causing errors for the game.

### modinfo.json
#wiki
*Defines basic mod info, is used by Remix.*
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Mod_Directories  

### Folder structure  
#wiki
https://rainworldmodding.miraheze.org/wiki/UserWiki:Tat0110

### Targeting multiple game versions
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