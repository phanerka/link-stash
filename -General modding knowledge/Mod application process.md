---
draft: true
---
> [!wip] This page is WIP.
> It's messy, incomplete and possibly incorrect; I know.

just a bit of theory.
%% okay i should decide if im describing *loading* applied mods or *saving* applied mods
or else its gonna be a mess %%

1. The mod location is added into `enabledMods.txt`
	Note that DLCs have internal code check for being enabled, and aren't affected by the file.
### Remix
*Is responsible for loading **content** part of the mods.*
%% i wonder if it dictates to bepinex, what to load %%

2. If `checksumOverride` is `false`, then:
	1. ALL files from `modify` folder are merged with base game files and are put in `mergedmods` folder

### BepInEx
*Is responsible for loading **code** part of the mods.*
Loads ALL plugins (from `plugins` folder and its subdirectories) and patchers (`patchers` folder and its subdirectories) from the following locations:
- `Rain World\BepInEx\` , if the file name exists in the following file:
	`Rain World\RainWorld_Data\StreamingAssets\whitelist.txt`
- `Rain World\RainWorld_Data\StreamingAssets\mods\[mod-name]` , if folder name of the mod is mentioned in `enabledMods.txt` file
- `Steam\steamapps\workshop\content\312520\[mod-workshop-id]` , if full path (appended with `[WORKSHOP]` string in the beginning) to the mod  is mentioned in `enabledMods.txt` file

Path to `enabledMods.txt` file:
`Rain World\RainWorld_Data\StreamingAssets\enabledMods.txt`

If any of the new applied mods (or mods that were no loner applied) contained plugins or patchers, the game will be forced to restart.
### Resources load on game runtime

The order of loading files:
1. `mergedmods` folder
2. mods folders
3. base game folder (`SteamingAssets`)

If the game has way to save a file, it will put it next to / override the one that is read; if there's none found, it will be put in base game folder.

Example:
if the game finds map files in `mergedmods`, it will override them there too, not in mods or base game folder.

%% whats bout override tho? what file is read then? %%
%% and whats bout plugins? %%
%% i mean... how are they applied? %%