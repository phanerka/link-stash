**Looking up online: [[Music making/For referencing n inspiration#In game sounds|here]]**.
*Everything is stored in AssetBundle, as `AudioClip` file. For extraction guide, go [[-Extraction|here]].*

> [!watcher] Watcher files are tagged with `RWTW` in file name, with the exception of:
> - threat music
> - room / arena music
> - *some creature* related sounds (not explicitly named to avoid spoilers)
# Threat music
Dummy files' location:
`Rain World\RainWorld_Data\StreamingAssets\music\procedural\` (threat music)

Can be extracted via:
`Rain World\RainWorld_Data\resources.assets`
OR 
`Rain World\RainWorld_Data\StreamingAssets\AssetBundles\music_procedural`

Contains:
- threat music layers
	- Outskirts: `SU_1` - `SU-7`
	- every other region in existence: prefix is `TH_XX`, where `XX` is region acronym
- void sea background music (*yes* it counts as procedural music): prefix is `VS_`
# Songs
Dummy files' location:
`Rain World\RainWorld_Data\StreamingAssets\music\songs\` (everything else)

Can be extracted via:
`Rain World\RainWorld_Data\resources.assets`
OR 
`Rain World\RainWorld_Data\StreamingAssets\AssetBundles\music_songs`

Contains:
- arena music / music that starts playing in some room: prefix is `RW_`
- intro/outro cutscenes music: prefix is `RW_Intro` or `RW_Outro`, respectively
- short unique tracks that play on region enter: prefix is `BM_`
- passage music: `Passages`
- LTTM's sirens sounds: `MOON_SIREN` and `MOON_SIREN_MS`
- rain sound that plays on game start (without music!): `TitleRollRain`
- sounds from RW alpha version (steps, long jump, spear pickup, etc.)

> [!watcher]- Watcher contents
> - Echo background music: prefix is `BM_RWTW_TAG_`
# Sounds
> [!warning] Warning
> The sounds might *not* sound same as in game: a lot of in-game sounds are actually file sounds being mixed together / modified, and their ID's are declared there:
> `Rain World\RainWorld_Data\StreamingAssets\soundeffects\sounds.txt`

Dummy files' location:
`Rain World\RainWorld_Data\StreamingAssets\loadedsoundeffects\`

Can be extracted via:
`Rain World\RainWorld_Data\StreamingAssets\AssetBundles\loadedsoundeffects`
Decrypting:
https://www.reddit.com/r/rainworld/comments/11apuoi/having_trouble_accessing_sound_effects_in_game/

> [!warning] Silly warning :3
> The "contains" descriptions for sounds and ambient sounds may be not 100% right.
> If you cannot find ambient sound you're looking for, there's a chance it's actually in sound effects folder. Same thing applies for sound effect sounding files.

Contains:
- any sounds caused by slugcat actions
- creature sounds
- iterators sounds
- UI sounds
- sleep screen sounds
- post-cycle rain sounds / music

> [!watcher]- Watcher contents
> %% idk what to add its kinda obvious what to expect here %%
> - items sounds
> - creature sounds
> - echo sounds
> - The Prince sounds
> - rift related sounds
# Ambient sounds
Dummy files' location:
`Rain World\RainWorld_Data\StreamingAssets\loadedsoundeffects\ambient\`

Can be extracted via:
`Rain World\RainWorld_Data\StreamingAssets\AssetBundles\loadedsoundeffects_ambient`

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

> [!watcher]- Watcher contents
> *Unfinished cause I'm lazy to look where all sounds come from*
> Not tagged with `RWTW`:
> - locusts sounds: `locustCloudFar` and `locustCloudNear`
> %% maybe `Basic Mech` is also from watcher? idk %%
> 
> Tagged with `RWTW`:
> - karma10 dimension: prefix is `RWTW_RippleSpace`
> - Aether Ridge-related sounds: prefix is `RWTW_AR_`