*This page is dedicated to adding **region-wide and arena music**.*

*To add music **in particular room**, refer to [[music or sounds|lediting section]].*  
*To add **new sounds**, refer to [[add new sounds|coding section]].*

## Arena music
To tweak arena music list, you might need:
- `your-mod\music\songs\` folder 
	Create *only* if you're adding own music (`.mp3` format required)
-  `your-mod\modify\music\mpmusic.txt` file  
	Note that you'll need to make a **modify** folder here. Just a friendly reminder.  
	Use [modification syntax](https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Modification_Files) to customize base song list.  
	If you just want to add own music, here's a template:  

```
[MERGE]
Your very cool music name here
[ENDMERGE]
```
Note that file extension isn't required to add.

## Threat music
#crs required, i suppose

https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#procedural-music

https://rainworldmodding.miraheze.org/wiki/Threat_Music_File_Format 

How to replace threat music (video guide):  
https://www.youtube.com/watch?v=mkou-vg5oNo

#### Post-cycle rain music
*AKA rain song*
#regionKit required

https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/RainSong.md  