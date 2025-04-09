Looking up online: [wiki](https://rainworld.miraheze.org/wiki/Pearl/Dialogue) duh (for [Downpour](https://rainworld.miraheze.org/wiki/Pearl/Dialogue/Downpour) and Watcher \[TBA])
TODO add decrypted files archive
For pearls from modded regions, go [[Other mods#Via CRS Decryptor mod|here]]

## Encryption and decryption
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

*Decrypts ALL text files from enabled mods, whether it's from base game, DLCs or modded regions.*  
*Doesn't provide encryption.*  
Path for decrypted files:  
`Rain World\RainWorld_Data\StreamingAssets\decrypt`

> [!warning] huh
> seems like `decrypt` folder breaks the game on launch now
> TODO: check if the mod still works

## Syntax
TBA TODO

`0` in beginning: is unencrypted