*Mostly, just follow this tutorial and check the rest of guide for more information or if any questions occur:*
https://rainworldmodding.miraheze.org/wiki/Code_Environments

%%btw make sure to use `PUBLIC-Assembly-CSharp`, NOT `Assembly-CSharp`!%%
# Things to know
C#. yeah.
## Optional
Useful concepts (you can learn them when you'll need to):
- [[! Modifying game logic|On / IL hooking]] (to modify base game logic)
- [[Storing data for existing objects|ConditionalWeakTables]] (to store data)
- [[Creating a creature or item|ExtEnum]] (to register new objects)

Worthy to be aware of, to check regularly:
- list of shortcuts for shorter and cleaner code
	https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/Shortcuts
- technical glossary which includes RW-specific terms
	https://rainworld.miraheze.org/wiki/Technical_Glossary
- coding [[Coding/Tips#Coding tips|advices]] to avoid making bad logic  
# Things to download
 - [ ] IDE for C# (`Visual Studio 2022` / `VS Codium` / `Intellij Rider` / etc.)
 - [ ] mod template
![[Code Mod template]]
- [ ] code decompiler (`DNSpy` / `ILSpy`)
## Optional
**Newtonsoft library**
*AKA `Newtonsoft.Json.dll`*
It's not required in the game anymore, however old mods might still use it.
So [here](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/coding/Newtonsoft.Json-eJ8S8xbGARSJa7PQDeogmX86y2UnUJ.dll)'s the download link for the library.

%%
- (optional: to explore game contents)
	[VSCodium](https://vscodium.com/) AKA [VS Code](https://code.visualstudio.com/) without telemetry.
	In general, any text editor that is able to do the following would work:
	- open and read big files (example: potential log files and room files) without issues
	- reload contents of a file in real-time (for logs)
	- search in a single file, with ability to replace found strings with another one
	- search in all files from a single folder, by contents / name (to look up something in game files)
%%
**Unity**
*Download it ONLY if you're planning to create [[Coding/Guides/Loading custom assets/Shaders|shaders]] or [[Debug World]] on your own.*

Unity with [[Unity version|same version]] of which Rain World would built on. It's very bulky, make sure to do it beforehand!
# Tutorials
Here's a list of available tutorials dedicated to basic mod creation; feel free to pick one and stick with it.
- YouTube video tutorial by `None`
	https://www.youtube.com/watch?v=JG9cyL5FW90
- Modding Wiki page
	https://rainworldmodding.miraheze.org/wiki/BepInPlugins
- YT playlist by `Henpemaz`
	*Outdated at some parts, unfinished and likely will never be; however, it concerns basics of RW code structure which is very useful to be aware of.*
	https://www.youtube.com/playlist?list=PLuHyVLkKIJi3P6xu-V3aRTAlwWpdDKxSa
# Useful links
*[[Source#Wikis|RW Wikis]] will be of huge help. Make sure to check them.*

**Risk of Rain 2 Wiki**
*Although it's tuned specifically for RoR2 modding, some guides (that concern BepInEx modding in general) could be useful for RW modding as well.*
https://risk-of-thunder.github.io/R2Wiki/

**BepInEx documentation**
https://docs.bepinex.dev/articles/index.html
