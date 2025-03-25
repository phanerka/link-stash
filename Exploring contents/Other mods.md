*This page is dedicated ONLY to exploring mods. For a guide how to modify their code, refer to [[DNSpy#Editing DLLs|this]].*


Workshop mods location:   
`Steam\steamapps\workshop\content\312520`, in respective folder with Workshop mod ID.
Easy way to determine the ID is to open Workshop mod page and check its link. To be exact, it's
`https://steamcommunity.com/workshop/filedetails/?id=number`,
where `number` is mod ID. (yeah ik im great at phrasing.)

Downloading mods w/o workshop:   
https://rainworldmodding.miraheze.org/wiki/Remix_Mods_Outside_of_Steam

### Technical files
Could be:
- save files
- logs (except [[Saves#CustomRegionsSupport log|CRS]] since it's a must-have for lediting in general)

Check "Coding" -> "How to-" -> "add mod compat" [[Coding/Guides/Mod compatibility/index|folder]].
### Code
To look up for open source mods, easiest solution is to open RW Workshop page and search by "github" ([hey look, i did it for ya](https://steamcommunity.com/workshop/browse/?appid=312520&searchtext=github))

You can debug other mods just like [[Coding/Troubleshooting|your own mod]]. 
### Regions
Main page on region project files is [[Editing in-game rooms|here]].

### PORLS
looking up online: rw mods wiki
#### Dialogues  
Some will work with [[Dialogues#Encryption and decryption|default decryption]] method. Some will not.
##### Via CRS Decryptor mod
*Will help to decrypt pearls if everything else fails.*  
https://steamcommunity.com/sharedfiles/filedetails/?id=3213183426

>[!warning] Warning on usage
> Do NOT attempt to read already decrypted files! The mod will attempt them to decrypt as well, causing the contents to become unreadable.

Tutorial (as example, the Howling Rift pearl with english dialogue is used):
- get the pearl with dialogue you need to decrypt.
	To spawn a pearl, check [[Exploring contents/Base game n Downpour/Pearls#Exploring pearls in game|this]] page.
- give the pearl to any iterator to read it.
- locate the path of dialogue file for the pearl in mod folder. There will be another file with same name but ends with `.decrypted`: it will contain decrypted dialogue. 
	For Howling Rift pearl, it would be:
	`Steam\steamapps\workshop\content\312520\2987817211\Text\Text_Eng\HC_PIT.txt` (for encrypted file)
	`Steam\steamapps\workshop\content\312520\2987817211\Text\Text_Eng\HC_PIT.txt.decrypted` (for decrypted file)
- open the `.decrypted` file, view or edit it.
- once you're done and want to allow the game to read the file:
	- remove the `.decrypted` line in file name
	- replace the 1st character in the beginning of the file with `0`.  

(source: translated from mod page)