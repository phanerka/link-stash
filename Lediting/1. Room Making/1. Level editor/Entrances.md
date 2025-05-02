> [!wip] This page is on hiatus and thus WIP.
> Old connection guide is outdated, and I'm waiting for new one to be created.

*Every room requires to have at **least 1** room exit to work.*
# Entrance types
Their view might depend on level editor used.
![[entrance-types.png]]
1: a shortcut
Types of shortcut exits:
- 2: room exit (can be called `Room Entrance` / `Entrance`)
- 3: creature den (can be called `Dragon Den`)
- 4: creature shortcut (can be called `Whack-A-Mole Hole`)
- 5: scavenger shortcut (can be called `Scavenger Hole`)

6: garbage worm den
# Placement
If not followed, connection might become invalid, causing the game crash on room load.
##### Placement process
![[2018-01-20_23-24-05.gif]]
(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/431657655120166922))
## Placement rules
**Nothing can touch or cross room border.**

Conditions for a working shortcut exit:
- it needs to be surrounded by 8 solid tiles and 1 air tile (which can be located only on side, above or below the exit)
- it needs to touch a single connection tile OR exit tile on side, above or below

Garbage worm dens MUST have:
- solid tiles on sides and below
- tile of air above.

Connection path can:
- not lead to exit 
- cross another connection path 
	%% add picture here %%
- be located on second layer
- be connected to entrance from any direction, excluding diagonal
%%
correct and incorrect examples:

pipe connections can be just player connection - player connection
https://discord.com/channels/1083481230839922688/1083483045329375393/1250182010446544997
%%

# Hiding entrances

hiding entrances is done not here but with dev tools, with `ExitSymbolHidden` object


