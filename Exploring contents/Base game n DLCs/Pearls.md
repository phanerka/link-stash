# Pearl colors 
![[pearls-color_by-juliacat57.png|500]]
(source: [RW Main](https://discord.com/channels/291184728944410624/296133304632213504/1113315552434323498))

1st and 2nd row: base game & Downpour pearls.
The order of pearls is like from `COLLECTION` menu from the game (read by columns: from top to bottom)

3rd row, left to right:
- `BroadcastMisc` ([broadcast pearls](https://rainworld.miraheze.org/wiki/Pearl/Dialogue/Downpour#BroadcastMisc))
- `Misc2` ([bonus pearls](https://rainworld.miraheze.org/wiki/Pearl#Misc2))
- `CL` ([Pebbles' music pearl](https://rainworld.miraheze.org/wiki/Pearl/Dialogue/Downpour#Silent_Construct_%E2%80%A2_Music_(faded)_(CL)))
- `PebblesPearl`, `marbleColor`: `1` or `-1` (iterators' silver pearl)
- `PebblesPearl`, `marbleColor`: `-3` (LTTM's blue pearl)
- `PebblesPearl`, `marbleColor`: `0` or `-2` (iterators' orange pearl)
- `PebblesPearl`, `marbleColor: 2` (FP's black pearl)


# Pearl dialogues
- from base game: go [[Dialogues#Online resources|here]].  
- from region mods: go [[Other mods#Via CRS Decryptor mod|here]].

##### PORL TABL  
#docs
*PORL TABL*

A spreadsheet that contains technical data about base game and MSC pearls.
Includes:
- pearl color (as used in Wiki)
- pearl location
- pearl ID
- dialogue ID
- text file name of the dialogue

https://docs.google.com/spreadsheets/d/1OanAHTU9rHI81HdgI_YFl9kR5WW6IsqpazSnkeTbguA/edit
(source: [RW Main](https://discord.com/channels/291184728944410624/296133304632213504/1111342813964161035))  

# Exploring pearls in game

## Getting pearl ID
[What's This Pearl?](https://steamcommunity.com/sharedfiles/filedetails/?id=3428753018) mod shows pearl name and (toggleable in Remix options) ID, after holding it for a bit.
## Triggering pearl dialogue
Mark of communication can be obtained:
- via Dev Console mod (as was shown in the video): `the_mark`
- by adding `the mark` line in [[Cheat codes|setup.txt]]

Getting to LTTM (`SL_AI` room):
- via Warp Menu, cmon its the easiest way

## Spawning a pearl
Alternative ways to get a pearl:
- via dev console
> [!warning] Warning on spawn command
>It's case-sensitve.
> Autocomplete lines via `Tab` key or type them correctly manually.

**White pearls:**
`spawn DataPearl Misc`

**Colored pearls:**
`spawn DataPearl [ID]`, where `[ID]` is pearl ID (list of available IDs will be shown; base game / Downpour IDs also can be looked up [[Saves#Object IDs|here]])

**Five Pebbles' and Looks to the Moon's pearls:**
`spawn PebblePearl [color]`, where `[color]` is `marbleColor` number; for the list, look [[Exploring contents/Base game n DLCs/Pearls#Pearl colors|above]].

