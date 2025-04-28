for mod application issues.

# Absent mod in the mod list
It's most likely related to incorrect `modinfo.json` file.
To make sure it's the case, you can replace it with another working `modinfo.json` file (from remix mod: `Rain World\RainWorld_Data\StreamingAssets\mods\rwremix`) and modify its ID and name only. %% wont it break due to LF too tho? %%
- (?) using LF instead of CRLF (more info [[Mod structure|here]], in warning block)
- incorrect JSON formatting

# Code mod not working
There are 2 common reasons why that could happen:
- you're running Rain World NOT on WIndows (aka via emulator on Linux, MacOS, Android???)
	You'll need to ask Wine to use `winhttp.dll` that is located in game folder, not the one supplied by Wine. The steps vary on how and where you're running the game.
	- Steam - add the following in launch options of the game:
		`WINEDLLOVERRIDES="winhttp=n,b" %command%`
	- Wine (Linux) - install Winetricks and add there.
	- MasOS, i forgot what and ill fill it out later
- your `doorstop_config.ini` is corrupted.
	Delete it and force Steam to verify game files.
- maybe you forgot to put the `.dll` plugin in `your-mod\plugins` folder?