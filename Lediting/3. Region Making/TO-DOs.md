## Pre-release
#### Region naming (acronym)  
Acronym is 2-letter identifier for a region.
If someone gets 2 regions with same acronyms.... Eh, they better not. Trust me.
> [!info] Note on acronyms
> Recently, a [mod](https://steamcommunity.com/sharedfiles/filedetails/?id=3412393061) was released that allows to use more than 2 letters for acronym. Yay!  

List of base game regions' acronyms:
https://rainworld.miraheze.org/wiki/User:Alphappy/Region_codes  

##### Region lease 
#sheets  
https://docs.google.com/spreadsheets/d/14wt42_ZalI5di8zpUFx3WvPWldC_L7SwIbgb_TxOpUk/edit   
*Is used to make all regions compatible with each other.* TODO holy shit im so bad at phrasing
Once you're confident with own acronyms, you'll need to request access to the document (submit [this](https://forms.gle/gdaGmLJuBJb4LvMS7) form) and add own values. 

Includes:  
- Connections to vanilla regions  
- Connections to modded regions  
- Palette allocation chart  
- Token usage chart (blue/gold)  
- Region acronym chart

##### Acronym availability check
#utils  
Pulls info from spreadsheet.
https://rainworld-region-lease-improved.glitch.me/

##### Mass renaming acronym in mod folder
#utils  
if you ever decide to change region name during development, this might help you to do it quickly.  
https://github.com/glebi574/rw-fix-region-acronyms
#### (optional) Defining campaign-specific changes
this and below
https://rainworldmodding.miraheze.org/wiki/Downpour_Reference/File_Formats#map_xx.txt/map_xx.png
#### (optional) Connecting to other modded regions  
#crs only.  

First, check if the connection you want to use is free: [Mod-mod connections tab](https://docs.google.com/spreadsheets/d/14wt42_ZalI5di8zpUFx3WvPWldC_L7SwIbgb_TxOpUk/edit?gid=758721855#gid=758721855) in Region Lease speadsheet

Ask region mod authors for permissions to connect your region to theirs.  
After they agree, check this  
https://github.com/Bro748/Custom-Regions/tree/dp-release?tab=readme-ov-file#pearls

##### Region baking  
just a friendly reminder to [bake](https://rainworldmodding.miraheze.org/wiki/Creating_A_Region#Baking) your rooms.  
You can also bake via Remix menu in RegionKit  
i need to add regarding debugging..... ouf todo

## Post-release
When you finish the region, you'll likely want its map to be shared.  
https://seroen.github.io/Seroens-Repo/Dist/Tools/Cornifer.zip  
Check this and reach out Alduris to post your region map. 

##### Making static image map

  
##### Map exporter beta  
> Makes interactive maps. The interface is in the remix menu. Instructions are included there, but here's the general gist of things:  
> 1. Run the screenshotter for the regions/slugcats of your choice.  
> 2. Use the editor to edit the map in case of overlapping or unpositioned rooms. The map takes from the dev view map in dev tools, NOT the canon view (in-game map).  
> 3. Run the generator to turn the map into tiles.  
> 4. Run the local server in the export tab to view it in-browser. The export feature is not done yet.  
>   
> Permalink to download the latest version of the beta: https://github.com/alduris/MapExporter/releases/latest  
> If you receive an error or the screenshotter stops running without closing, please upload LogOutput.log, LogOutput.log.1, and, if it exists, exceptionLog.txt

(source: [RWMS](https://discord.com/channels/1237826015829557400/1273913033831350296/1273913775732555816))  
