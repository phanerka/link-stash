>[!example]- List of language codes in game:
>- `chi`
>- `eng`
>- `fre`
>- `ger`
>- `ita`
>- `jap`
>- `kor`
>- `por`
>- `rus`
>- `spa`

for syntax and decrypting, check [[Dialogues]] page

>[!warning] Advice on mod translations 
> If you're translating MSC / other region mods, mark them as soft dependency. It will make sure your mod will load after them and translate lines properly.

Base game.
- `your-mod\text\xxx-text`:
	- `text`: main game text
		Structure:
		- `N.txt` (n for number):
			- iterators multi-line dialogues (items description, pearls)
				For exact pearl dialogues, refer to [[Exploring contents/Base game n DLCs/Pearls#PORL TABL|PORL TABL]]
			- echoes dialogues
			- 25-34: items descriptions
			- 35, 37: moons greeting
			- 38, 40: ???? multiple lines? sky islands and pebblepearl?
		- `strings.txt`: 
			- iterators single-line dialogues (FPs requests to leave)
			- UI strings (remix included?)
			- items names in arena?
			- achievement names (msc included?)
			- slugcat names
	- `mods\moreslugcatsexpansion\text`: MSC text
		Structure:
		- `ROOM-SLUGCAT.txt`: developer commentaries.
		- `chatlog_xxN.txt`: broadcasts in spearmaster campaign.
		- `strings.txt`: 
			- iterators dialogues
			- safari keybinds
			- tutorial strings
			- MSC slugcat names
- `your-mod\content\xxx-text`:
	- `mods\moreslugcatsexpansion\content\xxx-text`: MSC inv thing text
- `your-mod\illustrations\xxx`:
	- `idk`: illustrations.



Mods.
- `your-mod\cw_text\text-xxx`:
	- `region-mod\cw_text\text-yyy`: text lines from CRS regions