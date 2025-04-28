> [!wip] This page is WIP: needs better clarification and uploaded files.

*.... In general, you don't **need** to do this for average mod making. However, if you want to make a native build of the game for non-Windows platform....*
*... good luck with that.*

> [!warning] Warning: the page will never be fully finished.
> Remaking [[Running RW in Unity#Input issues|input]] won't be covered.
> Consider this as own challenge to complete, as getting RW running in *Unity* is... a pretty serious thing to do.

There will be a lot of files suggested to be download, for your own convenience.
Here are all of them in a single archive.

Note that the entire archive as well as guide was made for v1.10.2 version of the game; with future versions, something might change and make the files outdated / broken.
##### Credits
First off, i want to thank the following people; the guide wouldn't have been possible without them.
- `Gamer025` - for answering and helping with (sometimes silly) issues whenever something didn't work
- `Dan's Palace` Discord server - for providing resources and `Brendon`'s guide on pulling out Rewired configuration file.
	These people are the guys who are usually behind porting various games to Android; they might help with some questions regarding importing games to Unity.
	Invite link to the server: https://dsc.gg/danspalace
# Getting the project

> [!warning] Warning on folder
> Make sure the game folder is "clean": it doesn't contain any local mods or non game-native files.
> They will be pulled as well.

`AssetRipper`: target `Rain World` folder, export the project
Import `ExportedProject` in unity, wait until it finishes

I've heard you can get rid of some.. language files? to speed up decompilation process

Then, here are 2 options:
- left click `RainWorld.unity` to load the project AND the scene
- open the Hub, click on `export project file` button, select `Exported project` folder, then after importing pick `Open scene` option and use it on `RainWorld.unity`

In my case (budget gaming laptop), importing the project took ~1h 20 min. Be prepared.

Skip safe mode, go straight to Unity.

Here goes error fixing time....
# Pre-compilation fixing

This is a list of errors that are *have* to be fixed to run the game, or simplify the fixing process.
## Setting up VS 20xx for Unity
Visual Studio will be able to
- open when double clicking scripts in unity or going to `assets - open c# project`
- show errors in code
- run and debug the game

(required for debugging feature) Go to `Build Settings` and check the `Development Build` option. It's required to allow VS attach to the code.
If it was *after* the steps below, [here](https://discussions.unity.com/t/cant-see-attach-to-unity-button-in-visual-studio/659893/9)'s how to fix it.

Then, follow this guide:
https://learn.microsoft.com/en-us/visualstudio/gamedev/unity/get-started/getting-started-with-visual-studio-tools-for-unity?pivots=windows

TL;DR:
1. install Unity plugin for VS
2. in unity, `edit - preferences - external tools`
	if unity cant find path, then thats default one (where my vs is installed at)
	`C:\Program Files\Microsoft Visual Studio\2022\Community\Common7\IDE\devenv.exe`
3. (idk if its useful but better to have it too) Install `Visual Studio Editor` plugin in Unity.
### Missing firstpass namespaces and types
*AKA `AGLog<>`, `Kittehface`, `FromStaticClass`, `AssetBundles`, `UserData` and `AGCachedStrings`.*

There's a bug with Unity importing the project, and you'll have to fix it.
Delete `Assenbly-CSharp-firstpass` from references of `Assembly-CSharp` project and add it back.
Keep in mind that the issue might appear again in the future; you might need to repeat this step again.

Another way is to change in `.csproj` file
## Fixing dependencies

### Missing Unity.UI
It means the project is missing Unity plugins.
Find package manager tab, click on `Packages: In project`, switch to `Unity Registry` and install the following packages:
- `Sprite 2D`
- `Unity UI`

You might need to also delete all Unity UI-related libraries in `Libraries` folder and restart Unity to make errors disappear.
### Missing On namespace
It means the project is missing `HOOKS-Assembly-CSharp` library, but it's not that easy. Simply dropping said file won't work, as it's a weird library created with special [generator](https://github.com/MonoMod/MonoMod/blob/reorganize/docs/RuntimeDetour.HookGen/Usage.md) that does [black magic](https://www.strathweb.com/2018/10/no-internalvisibleto-no-problem-bypassing-c-visibility-rules-with-roslyn/).
1. add the following file to `Assets` folder.
	It contains *only* those hooks that the code needs to be compiled.
2. modify `ModManager.cs` file.
	It will be easier if you [[Running RW in Unity#Setting up VS 20xx for Unity|set up]] VS 20xx for Unity; the IDE will show lines that throw an error.
	you need to make all troublesome hooks refer to that file; just append `On.` to them.
	here's how a single hook block should like:
	\[imagine a pic here]
3. exclude that file from compilation.
	You need that code *just* to compile the base game code; that hooking code will be available in actual `HOOKS-Assembly-CSharp` library as well, which might cause conflicts on game runtime.

### Missing GfxPluginNativeRenderer library

Just grab the one from the game, located in `Rain World\RainWorld_Data\Plugins\x64` (or x86_64?), put it in `Assets\Plugins` and restart Unity.
Note that it doesn't require separate `x64` folder to be put in.
## Missing scripts in CanvasRenderer and Futile
*Might not occur; i probably just messed smth up.*
Basically, you did smth wrong; re-import `RainWorld.unity` file and replace it in the project.
### Input issues
i forgor how they're called
Basically, you've got 2 ways here:
- rewrite entire input from Rewired to Unity in-built one, and it's very tedious
- get `Rewired` plugin.
	There are 2 issues in this case:
	- the plugin can be found [here](https://assetstore.unity.com/packages/tools/utilities/rewired-21676) in Unity Asset Store, and it costs **$45**
	- Rain World uses older version of Rewired (`v1.1.39.2`), while Asset Store allows to download latest version only.
		There will be code-related issues related to version difference, and they will require to be taken care of.

I'm not going to attach Rewired plugin here, as it's illegal; however, you might ask for it in the server mentioned in the [[Running RW in Unity#Credits|Credits]].

If you get the plugin, clean all Rewired-related libraries in `Plugins` folder:
- `Rewired_Windows`
- `Rewired_Core`
- `Rewired.Runtime`
# Post-compilation issues

## Game launch crash
Unity crashes every 2nd time you run the game; it's caused by running Epic Games and GOG libraries, which are allowed to run only once.

Just disable their component before you build to fix it.
## Missing PlayerHandler prefab
Create `Prefabs` (you're free to use different name) folder in `Assets`, create prefab in there, call it `PlayerHandler` and add the following scripts as components:
- `ControllerHandler`
- `PlayerHandler`
Then, drag and drop the prefab on Futile object; open Futile object, in `RainWorld` script component add the prefab from missing options

also, add particlerot as shader
and maybe othertextures in RainWorld? dunno
## Rewired
*If you decided to go this way.*
### Rewired configuration
just have the file. Open Rewired editor, then switch to Tools tab -> export configuration or smth.

Here's a guide though, how to do it yourself:

> [!example]- yeah.
>  Based on messages from `Dan's Palace` server: [here](https://discord.com/channels/904608817290039336/932989734253375528/1266139316166328426)
>  Make sure to back up `Rewired_Core` and `Rewired.Runtime`; the following actions *WILL* break the game, but make the job done.
>  This will concern [[DNSpy#Editing DLLs|DLL editing]]; prepare your DNSpy.
>  First off, grab `Rewired_Core.dll` and publicize internal `RewiredVersion` class. Save the module, overwriting existing one.
>  Next, grab `Rewired.Runtime.dll` library and add the following lines:
>  - in the top, libraries used:
>  ```
>  using System.IO;
>  using Rewired.Data;
>  using Rewired.Utils.Libraries.TinyJson;
> ```
> - before the class, a new class:
> ```
> public class llKiiginqkswqqeEcJlxRkSxhwtq
>    {
>       public RewiredVersion rewiredVersion;
>       public UserData userData;
>    }
> ```
> - in the class, `Awake()` function:
> ```
> void Awake()
> {
>    string contents = JsonWriter.ToJson(new llKiiginqkswqqeEcJlxRkSxhwtq
>    {
>       rewiredVersion = new RewiredVersion(ReInput.programVersion),
>       userData = userData
>    });
>    File.WriteAllText("C:\\\\Halo.json", contents);
>    //var Userdata = JsonConvert.SerializeObject(userData);
>    //var ConfigVars = JsonConvert.SerializeObject(userData.ConfigVars);
>    //Debug.Log(Userdata);
>    Debug.Log(contents);
> }
> ```
> In the end, something like that should be in your code:
> \[pic here]
> Save the module too and overwrite the file.
> Then, launch Rain World once: the file put in the path you used should appear. DLL modification will also break the game, leaving it with white screen on startup, but you *did* back up the libraries, right?

### Rewired Input Manager object
Gotta put some objects back.
2nd script: is Input Manager component. probably would be nice to modify unity file, to save all settings
3rd script: Nintendo Switch Input Manager component, used *only* for building on Switch. Isn't required; feel free to delete (?)
## Assets issues
i forgot how they're called
but basically, move some .asset filles from resources folders
and it should work
## AssetBundle issues
How to create AssetBundle:
in `Assets\Editor` folder, create `CreateAssetBundle.cs` file with the following contents:

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEditor;
using UnityEngine;

public class CreateAssetBundle
{
    [MenuItem("Assets/Build AssetBundles")]
    static void BuildAllAssetBundles()
    {
        BuildPipeline.BuildAssetBundles("Assets/AssetBundles", BuildAssetBundleOptions.None, BuildTarget.StandaloneWindows64);
    }
}
```

This file will be put in the archive above.

then go back to unity, `Assets` tab -> `Build AssetBundles`, and wait until they're done; for me, it took ~5 minutes.
## ArgumentNullException on AssetBundle loading
The game code doesn't recognize the platform, thus doesn't know the name of the bundle related to the platform.

in `Assembly-CSHarp-fistpass` project, in `GetPlatformForAssetBundles` function,
add in the switch case:
`RuntimePlatform.WindowsEditor => "Windows"`

# Game run issues
## Not visible game
wawa
need to set up components properly
like `Camera Image` and `Futile`
and i need to put pics here aaaa
## Broken shaders
this one is easy.
just delete shader files in `Futile` folder and replace with the the ones from base game

## No cameras rendering text
~~It's not a bug, it's a feature~~

It's fine, just hide it by right clicking `Game` tab and clearing a tick from `Warn if No Cameras Rendering`.

# Building issues
Took ~6 minutes for me to build.

well, i know only one thing:

crash on compute shader building
idk of any other solution except deleting `RotParticle` compute shader :(

%% TODO:: ask for perms
https://discord.com/channels/904608817290039336/932989734253375528/1018241377349423234
%%