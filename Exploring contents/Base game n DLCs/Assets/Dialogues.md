# Online resources

## Rain World Collection Index
#docs
> [!watcher] *Contains Watcher spoilers.*

Contains all base game & DLCs dialogues with additional information attached:
- (if exist) conditions for dialogue to be triggered
- locations of objects that trigger dialogue, with link to the room on online map
- location of dialogue in game files

https://yanwittmann.github.io/rw-collection-index
Github repo: [here](https://github.com/YanWittmann/rw-collection-index)

(source: [RW Main](https://discord.com/channels/291184728944410624/1125237384318046339/1348976713610039314))
## Wiki pages
 
- Pearls: 
	https://rainworld.miraheze.org/wiki/Pearl/Dialogue ([Downpour](https://rainworld.miraheze.org/wiki/Pearl/Dialogue/Downpour))
- Broadcasts:
	https://rainworld.miraheze.org/wiki/Broadcast#Dialogue
- Developer commentaries:
	https://rainworld.miraheze.org/wiki/Developer_Commentary#Dialogue
- Monologues:
	- LTTM:
		https://rainworld.miraheze.org/wiki/Looks_to_the_Moon#Dialogue
	- FP:
		https://rainworld.miraheze.org/wiki/Five_Pebbles/Dialogue
	- Echoes:
		https://rainworld.miraheze.org/wiki/Echo/Dialogue ([Downpour](https://rainworld.miraheze.org/wiki/Echo/Dialogue/Downpour))

> [!watcher]- Watcher contents
> - The Prince dialogue:
> 	https://rainworld.miraheze.org/wiki/The_Prince/Dialogue
> - Echo:
> 	https://rainworld.miraheze.org/wiki/Spinning_Top/Dialogue

# Encryption and decryption

>[!warning] Warning on decryption issues
>The following ways will work with base game and DLC files but might fail with modded regions' files.
> If the latter is your case and it does happen, check [[Other mods#Via CRS Decryptor mod|Other mods]] page. 
#### Via built-in game feature
*Doesn't require any mods to be installed!*

 basically [RW Main](https://discord.com/channels/291184728944410624/1315395285647622214/1315408396249464922)

Copy the files in 
- `Rain World\RainWorld_Data\StreamingAssets\decrypt\text` (for decryption)
- `Rain World\RainWorld_Data\StreamingAssets\encrypt\text` (for encryption)
and launch the game.  
Once the game is loaded, the files put in that path will be converted.

>[!warning] Warning on encryption/decryption feature
> Files in `text` folder will be read and converted but folders in `text` folder with files inside *will not*.

#### Via Decryptor mod
>[!warning] Luckily the mod still works. But once it doesn't, please don't ask the author to update them! 

%% TODO:: okay it might NOT work anymore. its bricking my linux system now lmao %%

*Decrypts ALL text files from enabled mods, whether it's from base game, DLCs or modded regions.*  
*Doesn't provide encryption.*  
Path for decrypted files:  
`Rain World\RainWorld_Data\StreamingAssets\decrypt`
# Syntax
TBA TODO

`0` in beginning: is unencrypted