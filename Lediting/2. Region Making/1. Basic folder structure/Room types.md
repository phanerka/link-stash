# Gate
![[Gate templates]]

### YT Tutorials
https://www.youtube.com/watch?v=t1_JnDUNtaY&list=PLOpeR3bQUKEJIGBJ3TATHBLmNvZwyYioT&index=5

> [!note] A lil note on guide
> Entire page assumes that `xx` (`XX`) and `yy` (`YY`) are respective [[Region acronym|acronyms]] of regions you want to connect. Replace every single mention of them with actual region acronyms you're going to use.

Requires:
- gate render files being put inside `your-mod\world\gates\` folder (**unlike all other room renders which are in `your-mod\world\xx-rooms\`!**)
- modification of `world_xx.txt` and `world_yy.txt` files
	*Declares the room as a gate and defines connections to other rooms.*
	> [!warning] Warning on shelter
	> If a shelter is directly connected to the gate room, its icon will not be shown.
	> To fix it, add `ExitSymbolShelter` / `ExitSymbolAncientShelter` object via Dev Tools interface.
	
	Each gate requires ` : GATE` tag, and every pipe that leads to the opposite region (i.e. pipe that leads to `yy`, in `world_xx.txt`) must be replaced with `DISCONNECTED.`
	
	Let's assume your gate has only 2 pipe exits, both are on different sides, then the following lines will look something like this:
	- `world_xx.txt`
	`GATE_XX_YY : XX_A01, DISCONNECTED : GATE`
	-  `world_yy.txt`
	`GATE_XX_YY : DISCONNECTED, YY_A01 : GATE`
	
	Keep in mind logic how pipes are numbered in the room, which means `XX_A01` and `YY_A01` might be swapped in your case.
- `your-mod\modify\world\gates\locks.txt` file
	*Defines karma requirement.*
	Add the following line:
	`[ADD]GATE_XX_YY : KARMALEFT : KARMARIGHT : SWAPSYMBOL` , where
	- `KARMALEFT` and `KARMARIGHT` are respective karma requirements for each side in range of `1-5`
	- `: SWAPSYMBOL` is an optional tag; if added, it swaps karma requirement shown on the map.

(the guide was made based on this message from [RWMA](https://discord.com/channels/1083481230839922688/1083485771949949019/1205579329413709876) and ludos tutorial videos)
#### Electric gate
*Is gate that works without water.*

Mostly same things to do but
- Instead of gate template, grab `dryGate` template
- `your-mod\modify\world\gates\egates.txt`
	Add the following line there to make it work:
	`[ADD]GATE_XX_YY`


### More gate customization
#regionKit

If you want to:
- add uncommon requirement (6+ karma, always unlocked, one-directioned, mark of communication/glow as condition to pass)
- make multi-screen gate
- modify some gate animation settings,
then you'll have to use RegionKit:
https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/ExtendedGates.md (for gate passing requirements)
https://github.com/Rain-World-Modding/RegionKit/blob/main/docs/GateCustomization.md (for everything else)

# Shelter

![[Shelter templates]]
## Common shelter
Requires `: SHELTER` tag in `world_xx.txt`

TODO add notes on shelter tiles usage, probs with preview
also, regionkit seems to add some dev objects
### YT tutorials
Part 1 (shelter creation basics):
https://www.youtube.com/watch?v=nwpcTGyYTwY&list=PLOpeR3bQUKEJIGBJ3TATHBLmNvZwyYioT&index=6
Part 2 (important notes on open area shelter making):
https://www.youtube.com/watch?v=7GZ84MrSAas&list=PLOpeR3bQUKEJIGBJ3TATHBLmNvZwyYioT&index=7


## Ancient shelter
Requires `: ANCIENTSHELTER` tag in `world_xx.txt`

Friendly reminder that Warp Menu does not recognize this tag and puts ancient shelters in list of general rooms
# Scavenger toll room
Requires:
- `: SCAVOUTPOST` tag in `world_xx.txt`
- `ScavengerOutpost` object in room, more info in [Dev Tools objects list](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Objects-0) in Wiki
- scavengers themselves lol
	- set their spawns in `world_xx.txt` (main page about `world_xx.txt` [[Region files#world_xx.txt|here]])
		All scavs go to ~~hell~~ offscreen. The following example will spawn 2 scavengers:
		`OFFSCREEN : 0-Scavenger-2`
	- add scavenger holes to the rooms
# Scavenger merchant room
Requires
- `: SCAVENGERTRADER` tag in `world_xx.txt`
- `TradeOutpost` object in room, more info in [Dev Tools objects list](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Objects-0) in Wiki

# Rubicon arena
Requires `: ARENA` in `world_xx.txt`

# Batfly spawning room
Requires
- `: SWARMROOM` tag in `world_xx.txt`
- setting up bathives
	Bathives are set up in geometry section of any leditor
	its color is defined by room palette