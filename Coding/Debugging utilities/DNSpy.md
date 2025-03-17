Download link:
https://github.com/dnSpyEx/dnSpy

spy????? 🥖 🇫🇷 🇫🇷 🇫🇷   
### Setting up  
To debug your own mod in DNSpy, drag-and-drop the built plugin that the game *is reading*, i.e. from  
`Rain World\RainWorld_Data\StreamingAssets\mods\YOUR_MOD_NAME\plugins`

> [!warning] Don't forget to replace it every time after build!

to debug others mods:   
`Steam\steamapps\workshop\content\312520`  
TODO bruh i duped info, theres same one in [[Other mods]]
### Attaching  
If attaching doesn't work, try  
- disabling all mods (clean `enabledMods.txt` file and `mergedMods` folder)  
- disabling all network drivers (VPN, local network) except the one that provides internet connection  
- ??? https://docs.unity3d.com/6000.0/Documentation/Manual/managed-code-debugging.html

maybe this will fix your things if you happen to find this archive and youre making a mod in visual studio (not visual studio code!! yes!!!!!) atm and want to debug that mod but cant for some reason:
- go to your project properties
- go to build -> general tab, scroll to its bottom
- find "Debug symbols" setting and change it to:
"PDB file, portable across platforms"

and dont forget to rebuild your mod lmao
and move pdb file as well to your mod folder lmao

### Using breakpoints  
Will work ONLY if you added the mod AND attached to the game.  
todo goddammit

"breakpoint could not be placed"
possible causes:
- youre using the library thats not read by the game.
- that part of code is overridden by another mod (like mergefix, concerning merging code). Explore that mod library or disable it.
- (map image render code) that part of code uses multithreading, maybe?... i think i can disable it in the library?...
- you changed the code and didnt save it / restarted the game? needs confirmation


gotta add vids vids vids  
how to use dnspy vid?

### Editing DLLs  
> [!warning] Disclaimer: the video is outdated.  
> Modifying Assembly-CSharp is highly discouraged, as your mod becomes ~~no more portable and generally applicable~~ highly incompatible with other mods and impossible to upload to Steam Workshop, and distributing it enters legally grey area (since your file will consist of 99% base game code).  
>   
> You might want to follow same steps to tweak different mod, but you'll have to keep in mind that:  
> - u gotta know IL code son cause writing in C# doesn't always work (and might break things)  
> - you gotta replace your freshly saved plugin in DNSpy every time you change smth or it will break  
>   
> Instead, it's usually advised to just make a separate mod what will hook the code you want to change.

  
https://www.youtube.com/watch?v=xOjaM3wjpO0  
### Other DNSpy features  
You can:  
- add bookmarks.  
	From my experience, DNSpy loses them very frequently, so it could be useful to save them in a file and store it somwhere.  
- check list of breakpoints  
- configure breakpoints (add conditions or filters, log in internal console)  
- analyze methods.  
- search across entire library, even string / number values

whats bout unity explorer? can it even be useful?