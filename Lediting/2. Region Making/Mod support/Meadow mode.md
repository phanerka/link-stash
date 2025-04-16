*For general Meadow support like syncing and blacklisting mods, go to [[Meadow|coding section]].*

Spreadsheet with music distribution in base regions:  
https://docs.google.com/spreadsheets/d/1rg14d7qPAnuyraE7zkSZvkA_8_6gDy_nrsypO1f6MaQ/edit  
Region that got no Meadow support will use **Shoreline** settings by default.

To configure music, you'll have to add `meadowPlaylist.txt` file to `your-mod\world\xx\` directory.  
In the file, define on separate lines:
- vibe zone properties
	Vibe zone is a pre-selected region room that can be warped into anytime (via pause menu). Unlike other rooms (which play songs from playlist for background music), its music is procedurally generated.  
	Define through comma:
	- name of the room that will be vibe zone   
	- minimum radius of vibe zone (relies on world coordinates)
	- maximum radius of vibe zone
	- waveform value (type of procedural music).  
	   Acceptable:
		 - `Trisaw`
		 - `Clar`
		 - `Litri`
		 - `Sine`
		 - `Bell`
- list of songs for area outside vibe zone  
List of all songs can be found & listened to in Meadow mod folder, i.e. :  
`Steam\steamapps\workshop\content\312520\3388224007\music\songs\`

There can be more than one vibe zone in a single region (most base regions have only one though), and you will be warped to the closest one in game.

Outer Expanse's `meadowPlaylist.txt` file as example:
```
OE_TREETOP,2800,4800,Sine
Eyes Vain
Woodback
me
Cascen
Folkada
Gray Orange
Void Genesis
Grasp
71104
Swan ode
OE_TOWER06,1000,2400,Litri
indufor
Eyto
Ones
Icy Parchment
tredjeplanen
Significance
Pedal Petal
Slightly Ill
Nevertop Side
Purple Puff
New and new
```