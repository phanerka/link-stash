Majority of mods' code relies on hooking, to modify game's code to desired needs.
## Referencing hooking library
aka `HOOKS-Assembly_CSharp.dll`
Is used to modify any method to provided by the library.
#### Standard hooking 
Most common and simple type of hooks.
Can be used to:
- add custom code before and/or after original one
- replace original code
#wiki
https://rainworldmodding.miraheze.org/wiki/Hooking#On_hooking
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/Standard_hooking

#### IL Hooking
Advanced type of hooking.
%% TODO:: bad phrasing %%
Is used to modify *part* of code in function, which helps to avoid ugly copy-pasting of original code into your mod (which is the only way with non-IL hooking).
https://github.com/tModLoader/tModLoader/wiki/Expert-IL-Editing

lmao chinese wiki  
https://rwmoddingch.github.io/ChModdingWiki/%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/IL%E7%AE%80%E6%98%93%E6%95%99%E7%A8%8B/

RW WIki page
https://rainworldmodding.miraheze.org/wiki/Hooking#IL_hooking

Example:
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/IL_hooking/Slam

### Creating a hook manually
Can be used to modify *anything*, be it method, property or constructor. However, is harder to make. 
The hook needs to be declared in `OnEnable()` [[Adding logic on mod enable or disable|mod lifecycle]] function.
https://rainworldmodding.miraheze.org/wiki/Hooking#Manual_hooking
#### RuntimeDetour hooking (outdated?)
https://rainworldmodding.miraheze.org/wiki/MonoMod_RuntimeDetour

### NativeDetour hooking
https://rainworldmodding.miraheze.org/wiki/Hooking#Native_Detours

##### Wrapping in try-catch with IL hook  
Done via ExceptionHandler.
(source: [RWMS](https://discord.com/channels/1237826015829557400/1237868501960491141/1329397865029697587))

# Guidelines

> 1. expect the hook to fail, they're much less robust than regular hooks (and are likely to break after game updates or if another mod IL hooks the same place), so write them with a lot of redundancy   
> 2. try-catch the hook definition, this will catch any exceptions that are thrown inside the hook   
> 3. good practice to use TryGotoNext and return if it fails over just GoToNext, so your hook can handle missing instructions   
> 4. avoid removing instructions, it will cause other mod's IL Hooks to fail if they try to match them, instead branch over them

(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/1332333516641407038))

https://rainworldmodding.miraheze.org/wiki/IL_Hooking_Bible

