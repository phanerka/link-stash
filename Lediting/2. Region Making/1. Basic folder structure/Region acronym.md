Acronym is a very short set of letters that works as region identifier in game code.  
All region acronyms MUST be unique; 2 different regions with same acronyms are incompatible with each other and, if enabled together, will break the game.

Due to long-lasting previous limitations, using only 2 letters as region acronym is very common practice; however since v1.10, the limitation was removed.

List of base game regions' acronyms:  
https://rainworld.miraheze.org/wiki/User:Alphappy/Region_codes  

>[!watcher]- Region naming for Watcher DLC
>The format follows as `WXXY`, where 
>- `W` stands for Watcher and is never changed 
>- `XX` is 2 letter region acronym
>- `Y` is variation index (most commonly, 4 for Watcher regions)

##### Region lease 
#sheets  
https://docs.google.com/spreadsheets/d/14wt42_ZalI5di8zpUFx3WvPWldC_L7SwIbgb_TxOpUk/edit   
*Is used to negotiate between region makers on defining region acronyms.*
Once you're confident with own acronyms, you'll need to request access to the document (submit [this](https://forms.gle/gdaGmLJuBJb4LvMS7) form) and add own entry. 

Includes:  
- Connections to vanilla regions  
- Connections to modded regions  
- Palette allocation chart  
- Region acronym chart

##### Acronym availability check
#utils  
Pulls info from spreadsheet for easy lookup of unused acronyms.  
https://rainworld-region-lease-improved.glitch.me/

##### Mass renaming acronym in mod folder
#utils  
if you ever decide to change region name during development, this might help you to do it quickly.  
https://github.com/glebi574/rw-fix-region-acronyms