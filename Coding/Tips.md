https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/Project_organization

### Tech tips
##### symlinking
*TODO repeating wikis tutorial; probs delete it*
go into `Rain World\RainWorld_Data\StreamingAssets\mods\`
type `cmd` in Address bar of Explorer, then paste the following:

``mklink /d folder_name referenced_location``

for junction (hard directory link):
``mklink /j folder_name referenced_location``

##### checksum override option?
> [!warning] DO NOT change this option if you plan on adding/modifying rooms in the mod. It will cause them to stop updating.

> [!warning] When you're about to upload the mod to Workshop, change it to `false`.
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/Mod_Directories

TODO
all it does is prevent the mod merging every time you start the game
if you have any asset replacements they might not be updated
iirc the option is only there to save time
otherwise you have to sit through that 'merging all regions' thing
and yeah for code only mods it makes no difference
honestly I would leave it disabled and install mergefix though
##### Live logs
- `LogOutput.log`: enable one setting in BepInEx config; pops up in separate from the game window
- `consoleOutput.txt`: press `K` with Dev Mode enabled; visible on the left
- `exceptionLog.txt`: available with [[Debug World]]; visible in bottom left, pops up whenever first exception is thrown
##### Using cheat codes
Refer to [[Launch options]].

### Coding tips
%%- for mod compatibility, class creation > hook creation%%
- no base code yoinking. if ya need to change a single line in the function, check out IL hooking
- For IL hooking: [[! Modifying game logic#Guidelines|guidelines]]