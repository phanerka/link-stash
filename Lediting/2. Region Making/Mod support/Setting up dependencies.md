are set up via modinjo.json.

2 types:
- hard dependencies - required to be enabled, your mod wont be enabled otherwise.
	Related keys: `requirements` (for mod IDs), `requirements_names` (for user-friendly mod name)
- soft dependencies - not required to be enabled with your mod
	Related keys: `priorities` (for mod IDs)
	If possible, it's better to set MSC as soft dependency to not leave your mod behind paywall. 

To find ID of another mod, you can:
- check in Remix menu (it appears right under mod name on the right)
- check in `modinfo.json` of said mod in its [[Other mods|folder]]


### Mod existence based condition
#crs required
Can be applied to:
- creature spawns
- room connections

https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#region-conditional-lines