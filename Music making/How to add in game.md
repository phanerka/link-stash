*This page is dedicated to adding music **in the game**.*

*To add music **in particular room**, refer to [[Music or sounds|lediting section]].*  
*To add **new sounds**, refer to [[Sounds|coding section]].*

%% TODO:: add siren music from regionKit %%
## Arena music
To tweak arena music list, you might need:
- `your-mod\music\songs\` folder 
	Music format: `.mp3`
	Create *only* if you're adding own music.
-  `your-mod\modify\music\mpmusic.txt` file with [modification syntax](https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Modification_Files) 
	If you want to *only* add own music, here's a template for the file:  

```
[MERGE]
A cool music name here
A cooler music name here
[ENDMERGE]
```
Note that music file extension isn't required to add here.

## Conditional music
`your-mod\music\songs` 
Music format: `.ogg`, sample rate: `44,100 kHz` (TODO verify like FR VERIFY)
[Triggers](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Triggers-0) 

### Environmental music
`your-mod\loadedsoundeffects\ambient`
Music format: `.wav` or `.ogg`, sample rate: `44,100 kHz` (TODO verify)

online preview [[Music making/For referencing n inspiration#Ambient sounds preview|here]].

[Sounds](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Sounds-0) tab from Dev Tools wiki page (for room-wide and area-wide environmental music)

## Threat music
`your-mod\music\procedural`

Contents:
- music layer files
Music format: `.ogg`, sample rate: `44,100 kHz`

- `xx.txt` file, where `xx` is region [[Region acronym|acronym]].
Otherwise, use `proceduralMusicBank` region property to define name of the text file.

https://rainworldmodding.miraheze.org/wiki/Threat_Music_File_Format 

How to replace threat music (video guide):  
https://www.youtube.com/watch?v=mkou-vg5oNo

Can be checked in game via Dev Tools main interface, in "Sounds" tab ([Wiki page](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Sounds-0), "General controls" -> "Mouse input" section)
#### Slugcat conditional threat music
#crs required.
https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#procedural-music

## Post-cycle rain music
*AKA rain song*
#regionKit required
`your-mod\music\songs`
Music format: `.ogg`

https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/RainSong.md  