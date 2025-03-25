# Making palette image
There are 3 ways:  
- via Palette Creator mod  
The workshop version is broken. I sorta.... "fixed" it. partially. Couldn't bother to fix better. Here.  
TODO move the file link to actually there
- by combining existing palette and fade palette in main Dev Tool interface ( #regionKit required)  
- manually  

i should also make some templatte palette probs (typo intended)
### Palette creation guide
#docs  
> [!warning] Warning on palette location
> The described path is outdated. Correct path:  
> `Rain World\RainWorld_Data\StreamingAssets\palettes\`

https://docs.google.com/document/d/1fY_KEpD5RaXHS7Ho-kPee4Fe-xIBp5ilMuQ0-UBG0is/edit

# Adding palette in the game
Put your new palette in `your-mod\palettes\` folder, named as `paletteN.png`, where N is a number.
Make sure to give unique number to palette to not override other palettes by accident!
- palettes used by base game + MSC: 0-79
- palletes used by region mods: check "Palettes" [tab](https://docs.google.com/spreadsheets/d/14wt42_ZalI5di8zpUFx3WvPWldC_L7SwIbgb_TxOpUk/edit?gid=1310131772) of Region Lease spreadsheet. 