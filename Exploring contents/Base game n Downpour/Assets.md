rw decompiled sprite atlases, shaders, music (MSC included)  
https://drive.google.com/drive/u/2/folders/1YzPCwjKtODHf5JRlk8cYe5YLXBHqdq90  
(source: [RW Main](https://discord.com/channels/291184728944410624/1068344185016569856/1068395551164473386))  
# Images  
**Looking up online:** most of images can be found [[References|here]].

  
### Scenes & art  
~~Anything that is NOT sprites (for creatures, items, UI, font),~~  
It's not encrypted and is located in folders in `Rain World\RainWorld_Data\StreamingAssets`  
Also, available in [[References#Github images repository|Github image repo]].  
Breakdown: #wiki  
https://rainworldmodding.miraheze.org/wiki/Slideshows_and_Scenes#Breaking_up_the_basics_of_a_scene

##### Krita plugin for convenient importing and exporting scenes: #utils  
https://github.com/henpemaz/RWSceneEditor ([demo](https://dl.dropboxusercontent.com/s/8pmjwl0998l2wbc/krita_2022-09-02_17-52-05.mp4))  
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1015364893198782624))

All Downpour assets are stored as common mod assets in `Rain World\RainWorld_Data\StreamingAssets\mods\moreslugcats`

### Sprites  
**Looking up online:**  
> [!warning] These sprites are from RW v1.5. Downpour and Remix-related assets are absent.  
https://drive.google.com/drive/u/0/folders/1HnKRhfpON7VSAehGZN34qsPbZRnfHX8c  
(source: [Reddit](https://www.reddit.com/r/rainworld/comments/1dbtzrt/comment/l7vgv0y/))

MSC sprites conveniently put on a canvas for view:   
[rainworldmsc](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/game-contents/sprites/rainworldmsc_Split-icjBDGhflHQG62ZP2UxblH2BdozSrF.kra)  
[uispritesmsc](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/game-contents/sprites/uispritesmsc-RqkQzXY70z0XFb0RwbqekPFpILChsO.kra)  
(source: [RW Main](https://discord.com/channels/291184728944410624/296133304632213504/1113616624105308160))

Decrypting: #wiki  
https://rainworldmodding.miraheze.org/wiki/Custom_Assets#Sprites_and_Atlases  
##### Packing/depacking online or smth

unpacking  
https://tu.enea.sk/  
packing or smth  
https://www.codeandweb.com/tp-online  
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1098995144923041843))  
### Arena icons  
https://dl.dropboxusercontent.com/s/151jfgurb6otcjc/arenaicons_by_henpemaz.zip  
(source: [RW Main](https://discord.com/channels/291184728944410624/481900360324218880/722224693893136466))  
Also, available in [[References#Github images repository|Github image repo]].

### Color hex codes  
Most encrypted assets (e.g. for slugcats) are white and colored via game code.  
![[hex-colors.png]]  
(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/1081023267378303036))

##### List of other colors
Nightcat's body: `1E112E`

> [!example]- Secondary and tetriary colors for base slugcats  
> Monk: `C7AB3B`, `4FBA42`  
> Survivor: `A68E97`, `40A6D1`  
> Hunter: `6F4D66`, `992999`  
> Nightcat: `19082D`, `F5BFF2`

> [!example]- Downpour slugcats  
> Arti's blue pup: `99B2E6`  
> Arti's green pup: `7ADECF`  
>   
> Spearmarter's body (more correct? dunno): `4C2C65`  
> Spearmaster's needles: `FFFFFF`  
> Spearmaster's needle veins: `B75544`*  
>   
> Rivulet's gills: `DF2DEA`  
>   
> Saint's tongue: `FF80A6`  
>   
> Inv's body: `17244F`

\**The following color codes were not pulled from the game, they were colorpicked instead.*

(sources: [RW Main](https://discord.com/channels/291184728944410624/952002932826583080/1100566406828924978), [RW Main](https://discord.com/channels/291184728944410624/952002932826583080/1266033578882502777))

~~Besides, it's possible to find values in game, upon opening color picker (for example, in custom slugcat color selection)-~~  
where tf did i see that feature????  
hsl / rgb / predetermined colors switch  
this? fr??? TODO  
https://steamcommunity.com/sharedfiles/filedetails/?id=3371225357

# Sounds  
**Looking up online: [[Music making/For inspiration#In game sounds|here]]**.

### Music  
TODO: check if it works  
All music (threat, arena, on region enter) and few other sounds are in `resources.assets`

  
### Sound effects  
`Rain World\RainWorld_Data\StreamingAssets\loadedsoundeffects`  
Decrypting:  
https://www.reddit.com/r/rainworld/comments/11apuoi/having_trouble_accessing_sound_effects_in_game/

  
### Shaders  
`Rain World\RainWorld_Data\StreamingAssets\shaders`  
Shaders code ~~is decompiled~~ NUH UH and is readable via any text editor.   
put preview here 

(source: [RWMA](https://discord.com/channels/1083481230839922688/1083484108056957089/1095172254549168268))

##### Documentation on LevelColor shader #docs  
responsible for room coloring  
https://gist.github.com/EtiTheSpirit/97dfdc63f667e19acb6314dc8c1e2d18  
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1150360982397386823))

# Dialogues (PORLS included)  
Encrypting and decrypting: [RW Main](https://discord.com/channels/291184728944410624/1315395285647622214/1315408396249464922)

  
# Fonts  
Some fonts are encrypted in a form of sprite atlases. Others technically don't even exist (characters are just a bunch of sprites).

The fonts below are made by the community, for convenient usage.

https://fontstruct.com/gallery/tag/48144/Rain%20World

- RW title-like font (based on [Rodondo](https://www.dafont.com/rodondo.font))  
https://drive.google.com/file/d/15q8BBFUtt8G3XGyYi1JsD3IAuC-aUbpy/view?usp=drive_link  
Rodondo RU: `#general` pins  
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1166479012193906718))

- UI-like font  
wawa  
Supports cyrillic!  
(source: [RW Main](https://discord.com/channels/291184728944410624/481900360324218880/1094033795524612147))

- RW Glyphs being assembled in a font  
https://drive.google.com/file/d/1jEUJ23r1vTYXXoI21I1PexlfiIetJVzv/view  
(source: [Reddit post](https://www.reddit.com/r/rainworld/comments/1bei8sy/i_created_a_fully_functional_typeface_for_every/))

https://drive.google.com/file/d/1fmA2AK0utiy1Yajb10Hlny8_Bkpl8m3u/view  
(source: [RW Main](https://discord.com/channels/291184728944410624/481900360324218880/540335659890769931))

https://docs.google.com/document/d/1QZnQgeoW3RyoR3_ZR1DGse99p1UPZRhU5LoVvCGUT_A/edit?usp=sharing  
(source: [RW Main](https://discord.com/channels/291184728944410624/296133304632213504/822957346711928922))