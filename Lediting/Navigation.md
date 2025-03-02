Document-wide navigation notes: [[General doc navigation|here]]

Are you new to lediting or need a step-by-step tutorial to make a basic room? [[Lediting/Getting started|getting started]].  
Are you looking for:  
- something that's important for region making? [[Region making]]  
- list of mods and their documentation? [[Lediting/Useful mods list|Useful mods list]]  
- some specific object / property to add in room? Check the section below ⬇ 👁 👁  
- pre-devtooling specific tutorial? "How to-" folder  
`(custom palette isnt pre devtooling DAMMIT)`

### Figuring out how to add specific object / property to the room  
honestly, just ask in any server lmao  
but...

All lore-important objects are described in "How to add X in the mod".  
Talking bout the rest stuff, there are 4 possible ways how that could be done:  
- via Dev Tools  
	- If you have access to the room with what you want in game:  
		enter the room, open Dev Tools interface and check Objects and Properties tabs  
	- If you don't:  
		- check Dev Tools [wiki page](https://rainworldmodding.miraheze.org/wiki/Dev_Tools#Interface_Tabs) and search what you need in "Objects" and "Room Settings" tabs via `Ctrl + F`  
		- check [[Lediting/Useful mods list#Dependencies|libraries' docs]]  
- via [[Region making#properties.txt|region properties]] (recoloring creatures, setting amount of creatures)  
- with [[create custom palette|custom palettes]] (recoloring pipes / sky / water / acid, room-wide color manipulation)  
	If you have access to the room, open Dev Tools interface in it, try changing palettes (main palette, fade palette, accent colors) and see if color of what you need changes
- in very rare cases, its configured via code (like progress bar for gates)

If you're looking for hacky stuff, check "Fancy lediting tricks" folder.