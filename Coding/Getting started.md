(basically you'll need to follow [this](https://rainworldmodding.miraheze.org/wiki/Code_Environments) tutorial)
btw make sure to use `PUBLIC-Assembly-CSharp`, NOT `Assembly-CSharp`!
### Things to know  
C#. yeah.
For syntax, here's a list of shortcuts for shorter and cleaner code:
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/Shortcuts

Useful concepts (you can learn them later):  
- [[! Modifying game logic|Hooking / IL hooking]] (to modify base game logic)  
- [[Storing data for existing objects|ConditionalWeakTables]] (to store data)  
- [[Creating a creature or item|ExtEnum]] (to register new objects)
### Things to download  
- IDE for C#

If you're planning to [[Coding/Guides/Loading custom assets/Shaders|make shaders]] or make Debug version of RW yourself (there's a download link, but *what if!*), you'll have to download [[Unity version|specific version]] of Unity. It's very bulky, make sure to do it beforehand!  
#### Setting up RW for debugging  
> [!info] Disclaimer  
> It's your choice whether you want to do it or not.  
 >   
> Personally I advise to set it up. If you learn how to use DNSpy features, it will massively help you to identify bugs and explore game code.  
> But Debug World is proven to be problematic with *any* enabled mod that has custom region and sometimes is hard to attach to.

- set up [[Debug World]]  
- install [[DNSpy]]
### Things to learn  
Technical glossary which includes RW-specific terms:
https://rainworld.miraheze.org/wiki/Technical_Glossary

### Tutorials   
- [YT basic mod creation vid](https://www.youtube.com/watch?v=JG9cyL5FW90)  
- [wiki page](https://rainworldmodding.miraheze.org/wiki/BepInPlugins)  
- Unfinished [YT playlist](https://www.youtube.com/playlist?list=PLuHyVLkKIJi3P6xu-V3aRTAlwWpdDKxSa) (and likely will never be finished :( ): for advanced modding. 

> [!tip] Also recommended to check [[Coding/Tips|Tips]] for making more convenient setup.

  
### Code mod template
#templates  
https://github.com/NoirCatto/RainWorldRemix/tree/master/Templates   
### Useful links   

Risk of Rain 2 wiki, esp general modding info  
https://risk-of-thunder.github.io/R2Wiki/Mod-Creation/C%23-Programming/Assembly-References/  
BepInEx documentation  
https://docs.bepinex.dev/articles/index.html
##### RW Wikis  
[Modding Wiki](https://rainworldmodding.miraheze.org/wiki/Main_Page) (duh) - will most likely provide some info  
https://rainworld.miraheze.org/wiki/Category:Technical_pages - technical information about Rain World  
https://rainworld.miraheze.org/wiki/UserWiki:Alphappy
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live