Easiest way to figure out issues is by using Custom Region Support mod.

some people use arena mode to test rooms before adding them to a region
so if it works in arena then the issue is not the room

first, check [[Lediting/1. Room Making/Troubleshooting|room making troubleshooting]]

TBA

# Shelter issues



# Gate issues

%%
### Guide from [RWMA](https://discord.com/channels/1083481230839922688/1083483045329375393/1191210118918979644)



**game freezing or crashing upon entering region (includes infinite water gates, failing to load in arena and "abstractroom failed to load")**

1. check your room's geometry to ensure that no entrances are out of bounds (see pinned messages)
2. check to ensure you're using the rendered version of the room (the red version, in the Levels folder of your level editor) rather than the project file (from the LevelProjectFiles folder)

if both of those are good, move on to folder issues

for a vanilla region:
1. ensure that you've properly added your room to the region via a modify file by ensuring it's in the right place and has the appropriate formatting for the type of file it is and the thing you're trying to do (adding a room to a region will be a merge)
2. ensure that your rooms files are in the correct place
3. check the `world_xx` file in `StreamingAssets/mergedmods` to see what your modify file is actually doing and adjust the contents as needed

if all three are clear, post here with an explanation of your error (game [does this] when i [do that], i.e "game freezes when i try and load the region i connected my room to" as well as the troubleshooting steps you took). if you have the Custom Regions Support mod enabled, be sure to send `crslog.txt` found in streamingassets when asking for help with an error!

for a custom region:
1. ensure your world file and room files are in the correct places (`modname/world/xx` and `modname/world/xx-rooms` respectively)
2. ensure your world file is formatted properly (it needs a CREATURES/END CREATURES bit even if there are no creatures)
3. ensure your region has been properly added to `regions.txt` by checking in mergedmods
4. for a gate, make sure that the room's files are in the `world/gates` folder, and check that the locks are appropriately defined in `modify/world/gates/locks.txt` by checking mergedmods' `locks.txt`

if none of those fix your issue, send a description of the error  and the troubleshooting steps you've taken. if you have the Custom Regions Support mod enabled, be sure to send `crslog.txt` found in streamingassets when asking for help with an error!

**error messages in rainworld**

there are only two messages youll get;
*sharing violation* - you have a file open in another application (probably a modify file) and the game can't do stuff with it because of that. close the file and try again
*could not find part of the path* - you missed a folder or put something in the wrong place. check which path it's complaining about (i.e c:/steam/steamapps/common/Rain World/RainWorld_Data/StreamingAssets/world/xx/world_xx) and check that everything is there and in the right place

**niche issues**

> if the room before a shelter loads but then quickly gets laggy and then freezes, the shelter has an entrance that is pointing out of bounds where the game is trying to place the shelter gate. remove or move that entrance and itll load

\- if your room's geometry is loaded, but it still looks like the previous room you were in, the room's png is either named wrong or in the wrong place. it should be named `roomname_1.png` - the `_1` tells the game which camera to switch to and should not be removed
\- if no room can be loaded in arena, and youre getting an exceptionlog that contains `Menu.MultiplayerMenu.PopulateSafariButtons`, you previously loaded a custom region in safari mode, and left the menu selector on the custom region, then disabled the custom region, which makes the game freak out and arena breaks as a result. enable all custom regions you have, enter safari mode and leave the selector on outskirts

%%