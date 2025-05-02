# Common rooms' naming
room names' identification or smth... head hurtie pls no bad wordie
`XX_N01`
\[region acronym]\_\[amount of screens in a room, identified with a letter]\[room number]

For example, `SU_B05`:
- `SU` is Outskirts acronym
- `B` stands for 2 screens (A = 1, B = 2, C = 3, etc.)
- `05` is number of room.

So, that's a room from Outskirts that has 2 screens.
(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/496281533678878740); can we pin this?)

# Palettes list
#docs
*List of all palettes used by the game, sorted by palette number and region name (on separate sheets).*
https://docs.google.com/spreadsheets/d/1WloVDTQ4MOv0mnodrED1KLArJS7u5FUikr_DWpEkgsE/edit

#### Accent colors list
le list. i should probs update w/ MSC TODO
the watcher said hi i know im preparing to suffer
(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/485013629763059722))

# Room files

## Images
- rendered room assets (looking red)
are in `Rain World\SteamingAssets\world\XX-rooms` (where XX is region acronym)
- rendered AND colored rooms (like how they look in game)
TODO map exporter for online maps!!!!!
check out [[References n inspiration#Region maps|rain world maps]] for quick view, [[References#Github images repository|Github image repo]] for download and [RoomScreenshot mod](https://steamcommunity.com/sharedfiles/filedetails/?id=3125783486) (single room) /  ???? (all region rooms) for manual rendering.
- project files for lediting
Refer to "[[Editing in-game rooms]]" page.


Static map images:
https://drive.google.com/drive/folders/1EW91sf2nWv4S6Ine6pUfnzav4zn7LUPA

## Text files
Are located in same spot as room assets.

```
room name (unread)
width*height|water level|water depth
lightAngle
camerapos|camerapos|ect
Border: Solid (unread)
placed spears & rocks


ConnMap
AIMap (visibility map & prebaked pathfinding)
Geometry array
```
(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/1079483524354154687))

Connections map and AI map are added on room baking.

### Geometry array structure
All rooms' data is horizontally mirrored and rotated by 90 degrees counterclockwise.
\[uh imagine image here]
First attribute:
- 0: air
- 1: full tile
- 2: slope (how does the game determine slope direction tho?..)
- 3: platform
- 4: shortcut entrance

Second+ attributes: (should confirm.)
- 1: vertical pole
- 2: horizontal pole
- 3: shortcut dot
- 4: room entrance
- 5: whack-a-mole hole?
- 6: background wall
- 7: bathive
- 8: waterfall
- 9: scavenger hole
- 10: garbage worms den
- 11: wormgrass
- 12: regional interconnection wut????

(source: ASCII room render script, [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/444544647570915336))