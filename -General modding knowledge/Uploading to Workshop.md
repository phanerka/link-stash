> [!warn] Friendly reminder to turn `checksum override option` [[Coding/Tips#checksum override option?|off]].  
### Custom Workshop Uploader

Remix mod uploader is trash lol
becase yes
i need to ckeck it myself

### The issues with in-built mod uploader  

**"Why?"**  
 because V

> that's what happens when you change your mod's ID  
> or try to update a private mod, which shouldn't be your case

> why is rain world suddenly not updating my mod when i hit upload? for some reason now when i hit upload it now uploads it as an entirely separate mod instead of just updating what i already uploaded

> 1. Huh ![:saintsmirk:](https://cdn.discordapp.com/emojis/951914063720513596.webp?size=44) usually had that be the sole determining factor in whether the game's built-in uploader works properly, with it only working on Public mods Either way the Vigaro mod uploader works better. (edited)

https://github.com/MatheusVigaro/RainWorldWorkshopUploader/releases  
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1080334872364732526))

> I made a small tool for viewing all KVPs added to a Steam workshop mod via SteamUGC::AddItemKeyValueTag  
> https://github.com/Gamer025/SteamUGCKVPViewer  
> The tool will get all metadata from all mods your are subscribed to and outputs it as JSON which you can put into a website like https://jsonviewer.stack.hu/ for easier viewing  
> This metadata is normally used internally by games for example to filter for specific mods or display information about them in builtin mod manager   
> Rain World also has multiple of these fields but currently only uses the ID field for mod updating (modinfo.json is used by Remix to display mod data)  
> It currently seems like there is a limit to 17 or 16 possible values per key and reaching this limit is very likely the cause for the "Invalid metadata" mod update error  
> While this tool allows you to confirm if this is happening to your own mod it currently does not provide a way to clear these values  
> If you reached this limit I recommend updating your mod using Vigaros mod uploader instead or waiting till this issue is being fixed in a new PC release of Rain World  
> You can either compile the code yourself or get the latest version here https://github.com/Gamer025/SteamUGCKVPViewer/releases/latest  
> The program is already configured to get all Rain World mods but you can also check out other games by putting their AppID into the steam_appid.txt

(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1147616659624964148))  
