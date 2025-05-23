# Setting up proper mod structure
In one way or another, region making topic has to be concerned.
The main comprehensive guide is in [[Lediting/2. Region Making/|Region Making]] folder; this page exists just to cover *minimum* requirements to put a single room in a region.

> [!warning] Warning on folder structure
> Be *very* attentive to correct folders and files naming. It's easy to make a mistake, examples being:
> - forgetting about `modify` folder (files placed in `modify` will *be merged* with base game files, not override them; more info [[Ways to edit in-game files|here]].)
> - using `_` instead of `-` and vice versa
> - writing words in incorrect order (e. g. `rooms-su` instead of `su-rooms`)
> - deleting or renaming the image without leaving `_1` in the end (there might be another number, if the room is multi-screen)
>
> Any of these mistakes will most likely make your game crash on campaign launch.
### in existing region
*Is easier than the next option.*

Let's take outskirts for example. Its [[Region acronym|acronym]] is `SU`.
- put all your room files in the mod
	`your-mod\world\su-rooms`: all room files
- modify outskirts region file so it would include your room
	`your-mod\modify\world\su\world_su.txt`:
```
[MERGE]
ROOMS
SU_X01: DISCONNECTED, DISCONNECTED, DISCONNECTED
END ROOMS

[ENDMERGE]
```


### in new region

XX.

- put all your room files in the mod
	`your-mod\world\xx-rooms`: all room files
- set up basic region requirement
	`your-mod\world\xx\world_xx.txt`
	
	The file requires specific format to work:
	```
	CONDITIONAL LINKS
	END CONDITIONAL LINKS
	
	ROOMS
	END ROOMS
	
	CREATURES
	END CREATURES
	
	BAT MIGRATION BLOCKAGES
	END BAT MIGRATION BLOCKAGES
	```
	Just copypaste it into `world_xx.txt`.
	
	Between `ROOMS` and `END ROOMS`, add the following line:
	`SU_X01: DISCONNECTED, DISCONNECTED, DISCONNECTED`
	the result goes here yada yada
	%% yes, not done yet. %%
- modify world region acronyms file so the game would know about your region
	`your-mod\modify\world\regions.txt`
	Add the following text inside:
	```
	[MERGE]
	XX
	[ENDMERGE]
	```

# Reaching the room in game

- install Warp Menu mod and teleport in the room in game
- (not recommended) modify original game connections to make it accessible in game, and get there on your own
