%% TODO:: differentiate defining (via modinfo json) and actual setting up %%
## Finding mod Remix ID
*Not to be confused with [[Other mods#Getting the mod|Workshop ID]].*

To find ID of another mod, you can:
- check in Remix menu (it appears right under mod name on the right)
- check in `modinfo.json` of said mod in its [[Other mods|folder]]

# Types of dependencies
Are defined via `modinfo.json` [[Mod structure#Mod description file|file]].
### Hard dependencies
your mod HAS to be enabled with dependency; is easier to set up.
Related keys for defining:
- `requirements` (for mod IDs)
- `requirements_names` (for user-friendly mod name)

### Soft dependencies
Your mod can be enabled without dependency, however enabling dependency will provide more features in your mod.
Related keys for defining: `priorities` (for mod IDs)
If possible, it's better to make DLCs be soft dependency to not leave your mod behind paywall.

*Lediting section got own [[Setting up soft dependency|page]] about setting up soft dependencies.*
