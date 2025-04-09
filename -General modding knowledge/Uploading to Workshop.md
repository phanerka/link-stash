> [!warn] Friendly reminder to turn `checksum override option` [[Coding/Tips#checksum override option?|off]].  

Remix mod uploader is known to cause the following issues:
- upload the mod as a separate one instead of updating the old version
	- the mod has got private visibility
	- mod's ID in `modinfo.json` is changed
- clear mod description on mod update
- throw "Invalid metadata" error on mod upload for reaching [[Uploading to Workshop#KVP viewer|certain limit in metadata]]

Therefore, it's recommended to use 3rd party tool to upload mods.
### Vigaro's Workshop Uploader
#utils
https://github.com/MatheusVigaro/RainWorldWorkshopUploader/releases  
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1080334872364732526))

> [!watcher] oops watcher ate tags
> I've heard that it doesn't support new Workshop tags yet. RIP.

### KVP viewer
#utils  
https://github.com/Gamer025/SteamUGCKVPViewer   
*Displays all metadata key-value pairs of subscribed mods in the console.*  
Outputs in `JSON` format right in console window; can be formatted to readable view via external tools like [this](https://jsonviewer.stack.hu/) website.  

If your mod reaches 16-17 values per key, it will likely cause "Invalid metadata" error in Remix mod uploader.  
There's no currently known ways to clear said values; the only option is to update via Vigaro's mod uploader.

(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1147616659624964148))  
