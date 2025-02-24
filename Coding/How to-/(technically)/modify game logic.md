hookerino  
https://rainworldmodding.miraheze.org/wiki/Hooking

example:  
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/IL_hooking/Slam

Hooking a property  
https://rainworldmodding.miraheze.org/wiki/MonoMod_RuntimeDetour

### IL Hooking

https://github.com/tModLoader/tModLoader/wiki/Expert-IL-Editing

lmao chinese wiki  
https://rwmoddingch.github.io/ChModdingWiki/%E5%9F%BA%E7%A1%80%E6%95%99%E7%A8%8B/IL%E7%AE%80%E6%98%93%E6%95%99%E7%A8%8B/

##### Wrapping in try-catch with IL hook  
(source: [RWMS](https://discord.com/channels/1237826015829557400/1237868501960491141/1329397865029697587))

##### Guidelines

> 1. expect the hook to fail, they're much less robust than regular hooks (and are likely to break after game updates or if another mod IL hooks the same place), so write them with a lot of redundancy   
> 2. try-catch the hook definition, this will catch any exceptions that are thrown inside the hook   
> 3. good practice to use TryGotoNext and return if it fails over just GoToNext, so your hook can handle missing instructions   
> 4. avoid removing instructions, it will cause other mod's IL Hooks to fail if they try to match them, instead branch over them

(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/1332333516641407038))

https://rainworldmodding.miraheze.org/wiki/IL_Hooking_Bible

