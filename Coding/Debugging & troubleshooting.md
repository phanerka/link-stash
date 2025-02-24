---
dg-publish: true
---
https://rainworldmodding.miraheze.org/wiki/User:Alphappy/Live/Common_issues


Debugging is closely tied to [[Technical files#Logs|logs]] and [[Code|base code]] inspection: make sure to do it as well. 

hopefully u downloaded [[Coding/Getting started#Setting up RW for debugging|everything]] you needed for it.

# DNSpy'ing

spy????? 🥖 🇫🇷 🇫🇷 🇫🇷 
### Setting up
To debug your own mod in DNSpy, drag-and-drop the built plugin that the game *is reading*, i.e. from
``

> [!warning] Don't forget to replace it every time after build!

to debug others mods: 
`Steam\steamapps\workshop\content\312520`

### Attaching
If attaching doesn't work, try
- disabling all mods (clean `enabledMods.txt` file and `mergedMods` folder)
- disabling all network drivers (VPN, local network) except the one that provides internet connection
- ??? https://docs.unity3d.com/6000.0/Documentation/Manual/managed-code-debugging.html

### Using breakpoints
Will work ONLY if you added the mod AND attached to the game.
todo goddammit

gotta add vids vids vids
how to use dnspy vid?

### Editing DLLs
> [!warning] Disclaimer: the video is outdated.
> Modifying Assembly-CSharp is highly discouraged, as you mod becomes ~~~~not portable and generally applicable~~~~ highly incompatible with other mods and impossible to upload to Steam Workshop, and distributing it enters legally grey area (since your file will consist of 99% base game code).
> 
> You might want to follow same steps to tweak different mod, but you'll have to keep in mind that:
> - u gotta know IL code son cause writing in C# might break things
> - u gotta replace file in DNSpy every time you change smth or it will break
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