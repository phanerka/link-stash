---
dg-publish: true
---
# Gate
### Gate templates #templates
https://seroen.github.io/Seroens-Repo/Dist/Templates/Gate%20Templates.zip
For separate files download:
https://github.com/Seroen/Seroens-Repo-Files/tree/main/LevelEditorProjects/Templates/Gate%20Templates
### YT Tutorials
https://www.youtube.com/watch?v=t1_JnDUNtaY&list=PLOpeR3bQUKEJIGBJ3TATHBLmNvZwyYioT&index=5

### guide from [RWMA](https://discord.com/channels/1083481230839922688/1083485771949949019/1205579329413709876)
1. i suggest reusing a gate from the base game to make sure all the parts are in the right place
2. put the render in `world/gates`
3. youll need to add the gate to the world file of both regions it connects to. it'll need to be marked as ` : GATE` as both, and not connect to rooms outside of the world file that it's in. like so:

`world_xx`:
GATE_XX_YY : XX_A01, DISCONNECTED : GATE

`world_yy`:
GATE_XX_YY : DISCONNECTED, YY_A01 : GATE

4. youll also need to use a modify file for `world/gates/locks.txt`, to add your gates locks in the format:
`[ADD]GATE_XX_YY : KARMALEFT : KARMARIGHT` (where karmaleft and karmaright are numbers 1-5. also regionkit has some custom gate lock stuff, check it out on the github)

### More gate customization #regionKit

If you want to:
- add uncommon requirement (6+ karma, always unlocked, one-directioned, mark of communication/glow as condition)
- make multi-screen gate
- modify some gate animation settings,
, then you'll have to use RegionKit:
https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/ExtendedGates.md (for gate passing requirements)
https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/GateCustomization.md (for everything else)

# Shelter
TODO add notes on shelter tiles usage, probs with preview
### YT tutorials
Part 1 (shelter creation basics):
https://www.youtube.com/watch?v=nwpcTGyYTwY&list=PLOpeR3bQUKEJIGBJ3TATHBLmNvZwyYioT&index=6
Part 2 (important notes on open area shelter making):
https://www.youtube.com/watch?v=7GZ84MrSAas&list=PLOpeR3bQUKEJIGBJ3TATHBLmNvZwyYioT&index=7
### Shelter tempates #templates
https://seroen.github.io/Seroens-Repo/Dist/Templates/Shelter%20Templates.zip
For separate files download:
https://github.com/Seroen/Seroens-Repo-Files/tree/main/LevelEditorProjects/Templates/Shelter%20Templates
