%%
add room related issues here

- Room breaks: .txt file wrong
	Potential issues:
	- Pipe connections
		Check that page for more info.
	- Incorrect file being used: grab files from another folder, not project files.
	- Incorrect folder structure
- Room invisible: .png file wrong
	- forgor \_1 in the end

%%
# Error messages

## Remix Menu
*Make sure to check out [[Remix troubleshooting]] page too.*

--------------

Remix Menu: top of log
```
Mods failed to apply due to the following error: Could not find a part of the path "...Rain World\RainWorld_Data\StreamingAssets\world\[merge\world_[merge].txt"
...
```
you put `regions.txt` file to incorrect path.
your path:
`your-mod\world\regions.txt`
correct path:
`your-mod\modify\world\regions.txt`

-------------

Remix Menu: top of log
```
Mods failed to apply due to the following error: Could not find a part of the path "...Rain World\RainWorld_Data\StreamingAssets\world\xx\world_xx.txt"
...
```
Remix can't find your `world_xx.txt`. Are you sure it got correct name AND path?

## In-game
Warp Menu: the room isn't visible there

Unlike file names, room name in `world_xx.txt` is case sensitive; *at least* region acronym has to be entered capitalized, to make room be recognized as theirs.

---------

Warp Menu: `An error occured while realising the destination room`
Entire room line appears in room name

CRS:
```
[ERROR] Corrupted vanilla line [XX_A01: DISCONNECTED]

          Broken connection. Current room does not appear in any other connection Disconnecting...

These lines were disconnected:
Room: []. Connections: [] replaced with -> [DISCONNECTED]
[ERROR] Found broken connections in world file! Read crsLog.txt for more information
```

Congratulations! You forgot space before comma.

XX_A01 \[here's space] : DISCONNECTED

-------

Warp Menu (with CRS): freezes for a second, then loads the room
CRS:
```
Baking room: [XX_a01]
Finished baking room: [XX_a01], elapsed time: [0:00:06.13]
```

You forgot to define where every entrance leads to.

-------

Warp Menu: `An error occured while moving the RoomCamera to the new room`
Missing image / incorrect name for the image.
Make sure its called `[room-name_N.png]`, where N is number of screen (starting from 1)

------

`Corrupted vanilla entrance`
Incorrect line.
Make sure you formatted room entrance lines properly

----------

Warp Menu: `An error occured while loading the destination AbstractRoom`
CRS:
```
[ERROR] cannot find room file XX_A01
System.ArgumentNullException: Value cannot be null.
```

incorrect text file name of the room.

----------

Warp Menu: `An error occured while loading the destination AbstractRoom`
CRS:
```
[ERROR] room file is LevelEditorProject file instead of Level file XX_A01
the correct output files for a render will appear in Level Editor\levels
it appears this room file is from Level Editor\LevelEditorProjects
System.IndexOutOfRangeException: Index was outside the bounds of the array.
```
Exactly what CRS said, you've put project files instead of rendered ones.

--------------

The game: got pipe eaten
CRS: nothing

`exceptionLog.txt`:
```
IndexOutOfRangeException: Index was outside the bounds of the array.
ShortcutHandler.Update ()
....
```

you defined one-way connection: your room A leads to room B but room B doesn't lead to room A.