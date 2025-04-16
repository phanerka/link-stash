*While DW doesn't do much on it's own, it allows [[DNSpy#Attaching|DNSpy]] and [[Visual Studio 20xx|Visual Studio]] to attach to the game. More info on respective pages.*
### Installing 

Just unzip the files and replace them in RW game folder.  

In case you want to make Debug version of Rain World on your own:
> [!note]- Le guide
> The main guide is located [here](https://github.com/dnSpyEx/dnSpy/wiki/Debugging-Unity-Games#debugging-release-builds), as Wiki page of DNSpy Github repository.
> The one below is simplified and tuned to Rain World, with additional step 6 (to prevent game breaking on startup)
> 
> 1. Download and install [[Unity version|Unity]] (its version **has** to match the one the game has got).
> 2. Find where Unity is installed. It's default path is:
> 	`C:\Program Files\Unity\Hub\Editor\2020.3.45f1\Editor\`
> 3. Now, head to:
>	`Data\PlaybackEngines\windowsstandalonesupport\Variations\win64_development_mono`
> 	Just copy all the contents, excluding `Data` folder, in `Rain World` folder. Allow to override files.
> 	Technically speaking, not all files are *required* to be copied (as they're identical to base game ones); I don't wanna explain it cause it would complicate things for no reason.
> 4. Delete `RainWorld.exe`. Rename `UnityPlayer.exe` into `RainWorld.exe`.
 >5. Go to `Rain World\RainWorld_Data\` folder, open `boot.config` file.
 >	Add the following line:
> `player-connection-debug=1`
> 	Save and close the file.
> 6. go to `Rain World\BepInEx\config\` folder, open `BepInEx.cfg` file.
> 	Scroll to the bottom, to `[Preloader.Entrypoint]` section, and change the`Type = MonoBehaviour` line to the following:
> 	`Type = Application`
> 	Save and close the file.
> 
> Phew! Should be done.

### Troubleshooting
If the game breaks on loading:  
some room that is added by *any* enabled mod wasn't baked properly. Refer to [[Region baking|this]] for proper baking instructions.  

### DW customization
%% TODO:: finish %%
~~live logging in bepinex~~
wait for manager debugger = 1
etc etc

#### Hiding "development build" label
The one in bottom left corner.

How to hide:  
- open `Rain World\RainWorld_Data\Resources\unity default resources` file in any hex editor  
Online Hex editor: https://hexed.it/
- find `UnityWatermark-dev` string
- find 73 and 11 values a bit further in the table (they should be within 2 next lines)
- replace both of them with 1
- save and replace old file with ✨ brand new ✨ illegal one.

(source: source code of [Unity Remove Dev Watermark](https://github.com/kyubuns/UnityRemoveDevWatermark/blob/main/Assets/RemoveDevWatermark/Editor/BuildPostProcessor.cs) plugin)