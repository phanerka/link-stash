*While DW doesn't do much on it's own, it allows DNSpy to attach to the game. More info about attaching is in DNSpy [[DNSpy#Attaching|section]].*
### Installing 
TODO rework the section; RW is x64 now
get [one](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/coding/DebugWorld-rvrKbEeqowXM2GOMBub4GDKEjJfkuZ.zip) from `#modding-resources` channel (source: ?????)
TODO add one from github forums, by thalber

Note that it has modified `Managed\Assembly-CSharp.dll` library, which causes all mods to be verified by mod version, not checksum. Also, it doesn't work with Meadow. Replace the library at own discretion.

Just unzip the files and replace them in RW game folder.  

In case you want to make Debug version of Rain World on your own:
> [!note]- Le guide
> 1)  Download and install [[Unity version|Unity]] (its version has to match the one the game has got). :)
> go get some tea or smth, its gonna take a while
> 2)  Time to copy stuff!
you'll need to dig a bit in where unity is installed to and check following folders:
> - `Data\PlaybackEngines\windowsstandalonesupport\Variations\win32_development_mono`
> 	 just copy them to "Rain World" aka root folder, override them:
> 	- `WindowsPlayer.exe` (rename to `RainWorld.exe`)
> 	- `UnityPlayer.dll`
 > - `Data\PlaybackEngines\windowsstandalonesupport\Variations\win32_development_mono\Data\Managed`
 > 	Copy to `Rain World\RainWorld_Data\Managed`, override again:
> 	- a-a-all the .dll libraries u see 
  > - `Data\PlaybackEngines\windowsstandalonesupport\Variations\win32_development_mono\MonoBleedingEdge\EmbedRuntime\`
  > 	copy to `Rain World\MonoBleedingEdge\EmbedRuntime\`, override.... again.
> 	- `mono-2.0-bdwgc.dll`
> 
 >3) go to `Rain World\RainWorld_Data\` folder, open `boot.config` file. Add this line:
> `player-connection-debug=1`
> Save the file, close the file.
> 
> Phew! Should be done.
> And don't forget bout cleaning `bepinex.cfg` to make things work!

### Troubleshooting
- if the game breaks on start and shows red errors in the corner:  
	delete `Rain World\BepInEx\config\BepInEx.cfg` and restart the game.  
- if the game breaks on loading:  
	some room that is added by *any* enabled mod wasn't baked properly. Refer to [[Region acronym#Region baking|this]] for proper baking instructions.  


### DW customization
live logging in bepinex
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
- save and replace old file with brand new illegal one.  
(source: source code of [Unity Remove Dev Watermark](https://github.com/kyubuns/UnityRemoveDevWatermark/blob/main/Assets/RemoveDevWatermark/Editor/BuildPostProcessor.cs) plugin)