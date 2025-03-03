Default size is `72 × 43` tiles (for a single-screen room)

Effective default size is `48 × 35` (w/o borders, single-screen room)
(is it still valid?)  
alright, it all depends on the red line in the camera editor  
72×43 is the size of 1 camera, and 1 screen rooms  
to get the right amount of overlap in multi-screen rooms, you need to make sure the camera's red borders touch  
camera's red border is 52×43  
so, for the x axis 72 (the basic size for 1 screen) + (52 (the size of the red camera border for multi-screen rooms) × one less the number of horizontal screens you want)  
then, for the y axis it's 43 × the number of screens you want (edited)  
when im referring to the red line, i mean the little red border on the inside of the camera  
(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/518874593621049344))

**what the fuck is this formula.
seriously.**

https://rainworldmodding.miraheze.org/wiki/Level_Editor#Level_Size  
![[level-size.png]]  
 (^ source: was originally yoinked from wiki but posted in [RWMA](https://discord.com/channels/1083481230839922688/1083506128010358915/1217925887518048296)) 
  
### Multiscreen room templates #templates  
https://seroen.github.io/Seroens-Repo/Dist/Templates/Size%20Templates.zip  
For separate files download:  
https://github.com/Seroen/Seroens-Repo-Files/tree/main/LevelEditorProjects/Templates/Size%20Templates