> [!warning] Warning on DNSpy links
> Due to big popularity of DNSpy, there are seemingly "official" websites and project forks in the wild that actually contain malicious code. Be careful and download the app only from sources you trust.

Download link:
https://github.com/dnSpyEx/dnSpy

#### Linux troubleshooting
iirc you need some .NET framework, otherwise it will crash on launch
`winetricks` in terminal -> uhhh something from the following:
dotnet6, dotnetdesktop6, dotnet7, dotnet8, dotnetdesktop8
its most likely .net 8 but i cant tell for sure so gl

### Setting up  
To debug your own mod in DNSpy, drag-and-drop the built plugin that the game *is reading*, i.e. from  
`Rain World\RainWorld_Data\StreamingAssets\mods\YOUR_MOD_NAME\plugins`

> [!warning] Don't forget to replace it every time after build!

Works with other (Workshop) mods as well; for locating them, refer to [[Other mods|this]] section. 
### Attaching 
>[!warning] Won't work with Linux or Mac.

%% TODO:: add how-to here too %%
##### Troubleshooting
If attaching doesn't work, try  
- disabling all mods (clean `enabledMods.txt` file and `mergedMods` folder)  
- disabling all network drivers (VPN, local network) except the one that provides internet connection  
- check [Unity documentation](https://docs.unity3d.com/6000.0/Documentation/Manual/managed-code-debugging.html) (however, it doesn't seem of big use)
- if you're using Visual Studio to both develop and debug the mod: check [[Visual Studio 20xx#Attaching|this]].

### Using breakpoints  
Will work ONLY if you added the mod AND attached to the game.  
%% TODO:: simple how-to goddammit %%

"Breakpoint could not be placed"
Possible causes (at least what i encountered):
- you're using the library thats not read by the game.
- that part of code is overridden by another mod (like MergeFix, concerning merging code). Explore that mod library or disable it.
- (map image render code) that part of code uses multithreading, maybe?... i wonder if it can be disabled
- you changed the code and didn't save it / restarted the game? needs confirmation

### Editing DLLs  
> [!warning] Disclaimer: the video is outdated.  
> Modifying Assembly-CSharp is highly discouraged, as your mod becomes ~~no more portable and generally applicable~~ highly incompatible with other mods and impossible to upload to Steam Workshop, and distributing it enters legally grey area (since your file will consist of 99% base game code).  
>   
> You might want to follow same steps to tweak different mod, but you'll have to keep in mind that:  
> - u gotta know IL code son cause C# code won't always be able to be compiled (and might break things)  
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