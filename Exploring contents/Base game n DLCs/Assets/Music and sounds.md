**Looking up online: [[Music making/For referencing n inspiration#In game sounds|here]]**.

### Music
*Is encrypted in AssetBundle, in `AudioClip` folder.*

Dummy files' location:
`Rain World\RainWorld_Data\StreamingAssets\music\procedural\` (threat music)
`Rain World\RainWorld_Data\StreamingAssets\music\songs\` (everything else)
Actual files are bundled in following file:
`Rain World\RainWorld_Data\resources.resource`

Contains:
- threat music layers
- arena music
- short tracks that play on region enter
- passage music
- LTTM's sirens sounds
- rain sound that plays on game start (without music!)
- sounds from RW alpha version (steps, long jump, spear pickup, etc.)
### Sounds
*Are encrypted in AssetBundle.*

Dummy files' location:
`Rain World\RainWorld_Data\StreamingAssets\loadedsoundeffects\`
Actual files are bundled in following file:
`Rain World\RainWorld_Data\StreamingAssets\AssetBundles\loadedsoundeffects`
Decrypting:
https://www.reddit.com/r/rainworld/comments/11apuoi/having_trouble_accessing_sound_effects_in_game/

> [!warning] Silly warning :3
> These descriptions may be not 100% right.
> If you cannot find ambient sound you're looking for, there's a chance it's actually in sound effects folder. Same thing applies for sound effect sounding files.

What to expect here:
- any sounds caused by slugcat's actions
- creature sounds
- UI sounds
- post-cycle rain sounds / music
### Ambient sounds
*Are encrypted in AssetBundle.*

Dummy files' location:
`Rain World\RainWorld_Data\StreamingAssets\loadedsoundeffects\ambient\`
Actual files are bundled in following file:
`Rain World\RainWorld_Data\StreamingAssets\AssetBundles\loadedsoundeffects_ambient` Decrypting is same as for [[Music and sounds#Sounds|sounds]].

Contains *(organized by abbreviations from files' names)*:
- ambient music (`AM`)
	- environmental (`ENV`)
	- industrial (`IND`)
	- nature related (`NAT`)
	- rain sounds (`RAIN`)
	- Random Gods (`SFX`)
	- The Depths ambience (`SUB`)
	- water related (`WAT`)
	- wind sounds (`WIN`)
- sound effects (`SO`)
	- environmental (`ENV`)
	- industrial (`IND`)
	- nature related (`NAT`)
	- SS region related (`SFX`)
		(is `SO_SFX_Pulse` actually void sea effect?)
	- water related (`WAT`)