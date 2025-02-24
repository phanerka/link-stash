---
dg-publish: true
---
(basically you'll need to follow [this](https://rainworldmodding.miraheze.org/wiki/Code_Environments) tutorial)
### Things to know
C# my ass
Useful concepts (you can learn them later):
- [[modify game logic|Hooking / IL hooking]] (to modify base game logic)
- [[store data for existing objects|ConditionalWeakTables]] (to store data)
- [[add a creature or item|EnumExt]] (to register new objects)
### Things to download
- IDE for C#

If you're planning to [[add new shader|make shaders]] or make Debug version of RW yourself (there's a download link, but *what if!*), you'll have to download [[Unity version|specific version]] of Unity. It's very bulky, make sure to do it beforehand!
#### Setting up RW for debugging
> [!info] Disclaimer
> It's your choice whether you want to do it or not.
 > 
> Personally I advise to set up it up. If you learn how to use DNSpy features, it will massively help you to identify bugs and explore game code.
> But Debug World is proven to be problematic with *any* enabled mod that has custom region and sometimes is hard to attach to.

- Debug world versions of Rain World
	- the [one](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/coding/DebugWorld-rvrKbEeqowXM2GOMBub4GDKEjJfkuZ.zip) from \#modding-resources channel. Note that has modified `Assembly-CSharp.dll` file, which causes all mods to be verified by mod version, not checksum. Also, it doesn't work with Meadow.
	- another one made by stupid me who likes to do things the hard way. Oh well. At least I put some additional info in there. 
	Just unzip the files and replace them in RW game folder.
	If the game breaks on start: delete `Rain World\BepInEx\config\BepInEx.cfg` and restart the game.
	If the game breaks on loading: some room that is added by *any* enabled mod wasn't baked properly. Refer to [[Making a region TO-DOs#Region baking|this]] for proper baking instructions.
- [DnSpy](https://github.com/dnSpyEx/dnSpy)
### Things to learn
[Technical Glossary](https://rainworld.miraheze.org/wiki/Technical_Glossary)

### Tutorials 
- [YT basic mod creation vid](https://www.youtube.com/watch?v=JG9cyL5FW90)
- [wiki page](https://rainworldmodding.miraheze.org/wiki/BepInPlugins)
- Unfinished [YT playlist](https://www.youtube.com/playlist?list=PLuHyVLkKIJi3P6xu-V3aRTAlwWpdDKxSa) (and likely will never be finished :( ): for advanced modding. 

> [!tip] Also recommended to check [[Coding/Tips|Tips]] for making more convenient setup.


### Example of code mod #templates
https://github.com/NoirCatto/RainWorldRemix/tree/master/Templates 
### Useful links 
##### wikis
[Modding Wiki](https://rainworldmodding.miraheze.org/wiki/Main_Page) (duh) - will most likely provide some info
https://rainworld.miraheze.org/wiki/Category:Technical_pages - technical information about Rain World
https://rainworld.miraheze.org/wiki/UserWiki:Alphappy