Majority of mods' code relies on hooking, to modify game's code to desired needs.
## Referencing hooking library
aka `HOOKS-Assembly_CSharp.dll`
Is used to modify any method to provided by the library.
#### Standard hooking
*AKA On hooking*

Most common and simple type of hooks.
Can be used to:
- add custom code before and/or after original one
- replace original code
#wiki
https://rainworldmodding.miraheze.org/wiki/Hooking#On_hooking
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/Standard_hooking

#### IL Hooking
Advanced type of hooking.

Is used to modify *part* of original code in method, which helps to avoid ugly copy-pasting of original code into your mod (which is the only way with non-IL hooking).
For guidelines, check the [[! Modifying game logic#IL hooking guidelines|section]] below.
##### IL documentiation
#docs
https://github.com/tModLoader/tModLoader/wiki/Expert-IL-Editing

lmao chinese wiki
<https://rwmoddingch.github.io/ChModdingWiki/基础教程/IL简易教程/>
##### IL examples
https://rainworldmodding.miraheze.org/wiki/Hooking#IL_hooking

https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/IL_hooking/Slam



### Creating a hook manually
*AKA RuntimeDetour hooking*

Can be used to modify *anything*, be it method, property or constructor. However, is harder to make.
The hook needs to be declared in `OnEnable()` [[Adding logic on mod enable or disable|mod lifecycle]] function.
Example:
https://rainworldmodding.miraheze.org/wiki/Hooking#Manual_hooking

Is based on features of `MonoMod` library. It's code exists on [Github](https://github.com/MonoMod/MonoMod/tree/master), as well as:
- `RuntimeDetour` documentation
	https://monomod.dev/docs/RuntimeDetour/Usage.html
- technical explanation how `RuntimeDetour` works
	https://github.com/MonoMod/MonoMod/blob/master/README-RuntimeDetour.md
- examples of using various types of hooks
	https://github.com/MonoMod/MonoMod/tree/master/MonoMod.UnitTest/RuntimeDetour

#### NativeDetour hooking
https://rainworldmodding.miraheze.org/wiki/Hooking#Native_Detours

### Low-level hooking
> [!wip] okay this page is only theoretical dont expect it to be 100% correct

Is based on features of `Cecil` library, the one `MonoMod` is based on.
https://github.com/jbevain/cecil/tree/master
##### Wrapping in try-catch with IL hook
Done via ExceptionHandler.
(source: [RWMS](https://discord.com/channels/1237826015829557400/1237868501960491141/1329397865029697587))

# IL hooking guidelines

> 1. expect the hook to fail, they're much less robust than regular hooks (and are likely to break after game updates or if another mod IL hooks the same place), so write them with a lot of redundancy
> 2. try-catch the hook definition, this will catch any exceptions that are thrown inside the hook
> 3. good practice to use TryGotoNext and return if it fails over just GoToNext, so your hook can handle missing instructions
> 4. avoid removing instructions, it will cause other mod's IL Hooks to fail if they try to match them, instead branch over them

(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/1332333516641407038))

https://rainworldmodding.miraheze.org/wiki/IL_Hooking_Bible

