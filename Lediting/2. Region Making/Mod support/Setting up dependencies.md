Are set up via `modinfo.json`.

2 types:
- hard dependencies - your mod HAS to be enabled with dependency.
	Related keys: `requirements` (for mod IDs), `requirements_names` (for user-friendly mod name)
- soft dependencies - you mod can be enabled without dependency, however enabling dependency will provide more features in your mod.
	Related keys: `priorities` (for mod IDs)
	If possible, it's better to set MSC as soft dependency to not leave your mod behind paywall. 

To find ID of another mod, you can:
- check in Remix menu (it appears right under mod name on the right)
- check in `modinfo.json` of said mod in its [[Other mods|folder]]


### Setting up as soft dependency
#crs required
Mod / region existence based condition. Can be applied to:
- creature spawns
- room connections

https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#region-conditional-lines