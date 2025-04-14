Is made via Dev Tools; its Map tab is explained on [wiki page](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#tabber-tabpanel-Map-0). 

Output location:  
`Rain World\RainWorld_Data\StreamingAssets\world\sh`

> [!warning] Warning on map image saving
> ok so be careful since there's a chance you'll override base game files
> make a backup of them beforehand or prepare to verify game files via Steam

To reveal entire region map in game, add `reveal map:1` to [[Cheat codes|setup.txt]] and enable Dev Tools.
### Merging maps
supports custom campaigns. 
%% TODO:: add %% 

Output location:  
`Rain World\RainWorld_Data\StreamingAssets\mergedmods\world\xx\map_xx.png`


### troubleshooting
*Disclaimer: I'm relying on own experience. I could miss other cases.*

room looks full on preview, empty on output:  
- your game is too tired to render rooms chill  
	reload the cycle with R with dev mode on and try again.
- room image didnt change on output as expected:  
	you probably locked the image with another app (image preview, paint, etc.). close the app, then try again.
- room empty both on preview and output OR
- all connections are zeroed out:  
	youre pressing the render button too quickly. reload the cycle with R w/ dev mode on and wait until region loading finishes (it stops lagging in the end)