%% yeah i blatantly stole descs from ;allthelogs pls spare me %%
> [!warning] All logs are cleared on game restart. Make sure to save them in time.
> Another option is to install [LogManager](https://steamcommunity.com/sharedfiles/filedetails/?id=3138158069) mod and configure it. It also changes logs' locations to `idk i forgor`, however.

> [!tip] Enabling live `LogOutput.log` logs: [[Coding/Tips#Live logs|coding tips]]

# Important logs
## BepInEx log
`Rain World\BepInEx\LogOutput.log`
Created by BepInEx.
> [!info] if more that one instance are running on a single PC:
> second one will have `LogOutput.log.1` name, third one `LogOutput.log.2`, etc.
## Exceptions log
`Rain World\exceptionLog.txt`
Collects all errors that occurred in game. If no errors occur, it won't be created.
## Game log
Logs what is loading and happening in the game.
Doesn't seem to appear when absolutely no mods are applied.
`Rain World\consoleLog.txt`
## CRS log
#crs required
`Rain World\RainWorld_Data\StreamingAssets\crsLog.txt`
Useful for lediting.
Resolving issues using the log: [[Lediting/2. Region Making/Troubleshooting|here]]

# Niche logs

## Steam logs
Are located in `Steam\logs\`.
`content_log.txt` can be useful to check what failed to verify, for troubleshooting purposes.
## Unity log
*Is disabled by default; to enable, clean `nolog=` line in [[Launch options#Unity boot configuration file|boot configuration]] file.*
`%USERPROFILE%\AppData\LocalLow\Videocult\Rain World\Player.log`

Although it contains BepInEx, game and exceptions logs data altogether, it's not recommended to be used: it might potentially cause lags due to asynchronous nature.  
However, it also contains Unity-specific info such as debugging configurations ([[Debug World]]-related), which could be useful in some cases.