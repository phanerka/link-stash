just a bit of theory.

1. The mod location is added into `enabledMod.txt`
	Note that DLCs have internal code check for being enabled, and aren't affected by the file.
### Content mods
2. If `checksumOverride` is `false`, then:
	1. ALL files from `modify` folder are merged with base game files and are put in `mergedmods` folder

### game runtime
The game checks `mergedmods` folder first, and if required file doesnt exist, fallbacks to base game folder

%% whats bout override tho? what file is read then? %%
%% and whats bout plugins? %%

%%
`Rain World/RainWorld_Data/StreamingAssets` is the root directory, and there are two relevant parts there:

- `enabledmods.txt` is the list of mods that are currently enabled in Remix.
- `mergedmods/` caches the results of applying the `modify/` files inside of mods, only getting updated when enabling/disabling mods.
%%