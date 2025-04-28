(basically you'll need to follow [this](https://rainworldmodding.miraheze.org/wiki/Code_Environments) tutorial)
btw make sure to use `PUBLIC-Assembly-CSharp`, NOT `Assembly-CSharp`!
# Things to know
C#. yeah.

Basic C# concepts (this is basicest base of basics; you *need* to know them):
- constructors (sometimes referred as `ctor` or `cctor`)
- getters and setters
- access modifiers or smth

Useful concepts (you can learn them later):
- [[! Modifying game logic|On / IL hooking]] (to modify base game logic)
- [[Storing data for existing objects|ConditionalWeakTables]] (to store data)
- [[Creating a creature or item|ExtEnum]] (to register new objects)

For syntax, here's a list of shortcuts for shorter and cleaner code:
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/Shortcuts

Technical glossary which includes RW-specific terms:
https://rainworld.miraheze.org/wiki/Technical_Glossary
# Things to download
- IDE for C#
- (optional: to explore game contents)
	[VSCodium](https://vscodium.com/) AKA [VS Code](https://code.visualstudio.com/) without telemetry.
	In general, any text editor that is able to do the following would work:
	- open and read big files (example: potential log files and room files) without issues
	- reload contents of a file in real-time (for logs)
	- search in a single file, with ability to replace found strings with another one
	- search in all files from a single folder, by contents / name (to look up something in game files)
- (optional: to create [[Coding/Guides/Loading custom assets/Shaders|shaders]] or [[Debug World]] on your own)
	Unity with [[Unity version|same version]] of which Rain World would built on. It's very bulky, make sure to do it beforehand!

## Code mod template
#templates
Some IDEs like Visual Studio 2018 and later don't allow new projects to target .NET 3.8 and below. Thus, it's easier to download mod template that already targets it, and use it as a base.
https://github.com/NoirCatto/RainWorldRemix/tree/master/Templates

Alternative mod templates (*they might be outdated!*):
- by `Alduris`: [here](https://github.com/alduris/TemplateMod)
- by `PJB`: here
- by `aaaaaaa`: here yeah.
### Newtonsoft library
%% ? is it needed %%
*AKA `Newtonsoft.Json.dll`*
It's not required in the game anymore, however old mods might still use it.
So here's the download link for the library.
#### Setting up RW for debugging
> [!info] Disclaimer
> It's your choice whether you want to do it or not.
 >
> Personally I advise to set it up. If you learn how to use DNSpy features, it will massively help you to identify bugs and explore game code.
> But Debug World is proven to be problematic with *any* enabled mod that has custom region and sometimes is hard to attach to.

- set up [[Debug World]]
- install [[DNSpy]]
### Tutorials
- [YT basic mod creation vid](https://www.youtube.com/watch?v=JG9cyL5FW90)
- [wiki page](https://rainworldmodding.miraheze.org/wiki/BepInPlugins)
- Unfinished [YT playlist](https://www.youtube.com/playlist?list=PLuHyVLkKIJi3P6xu-V3aRTAlwWpdDKxSa) (and likely will never be finished :( ): for advanced modding.

> [!tip] Also recommended to check [[Coding/Tips|Tips]] for making more convenient setup.

### Useful links

[[Source#Wikis|RW Wikis]] will be of huge help. Make sure to check them.

Risk of Rain 2 wiki, esp general modding info
<https://risk-of-thunder.github.io/R2Wiki/Mod-Creation/C#-Programming/Assembly-References/>

BepInEx documentation
https://docs.bepinex.dev/articles/index.html
