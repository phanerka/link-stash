*Some fonts are stored in a form of [[Images#Sprites|sprite atlases]]: for more information, refer to [[Fonts n symbols#How to compile font on ur own|font converting guide]] below.*
*Others technically don't even exist: entire label is just a sprite.*
*The fonts below are made by the community, for convenient usage.*

Online website to check the font without having to install it:
https://fontdrop.info/?darkmode=true

## RW title
**Raindondo**

*Is modified version of [Rodondo](https://www.dafont.com/rodondo.font).*
https://drive.google.com/file/d/15q8BBFUtt8G3XGyYi1JsD3IAuC-aUbpy/view?usp=drive_link
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1166479012193906718))

Rodondo RU: `#general` pins
## UI
#### High resolution font
**Segoe UI RW Semibold**

Is based on `Segoe UI Semibold`.
Is used for majority of UI text, like description for Remix mods or slugcat campaigns.
#### Low resolution font
**Segoe UI RW Bold**

Is based on `Segoe UI Bold`.
Is used for text inside buttons in the game.
*Supports russian characters!*
(source: [RW Main](https://discord.com/channels/291184728944410624/481900360324218880/1094033795524612147))
## Glyphs

##### Ancient Braids Extended
%% ... im honestly afraid of thalber %%
https://fontstruct.com/fontstructions/show/2322206/ancient-braids-1
![[ancients-braids-extended.png|700]]

> [!info]- More glyphs of the font
> ![[special-letters.png]]
> ![[special-symbols.png]]
> ![[russian-letters.png]]
> ![[cyrillic-letters.png]]
> ![[georgian-letters.png]]

##### Ancients
https://drive.google.com/file/d/1H9CXAJTrzgTh4Vzz_4AblabBAjSYKNks/view
(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/1064335603128356904))
![[ancients.png|700]]


##### Iterator
https://fontstruct.com/fontstructions/show/2321323/iterator
![[iterator.png|700]]
##### RainRune
https://drive.google.com/file/d/1fmA2AK0utiy1Yajb10Hlny8_Bkpl8m3u/view
(source: [RW Main](https://discord.com/channels/291184728944410624/481900360324218880/540335659890769931))
![[rainrune.png|700]]
##### Rainscript C
https://fontstruct.com/fontstructions/show/2559995/rainscript-c
![[rainscript.png|700]]
##### RainWorldSymbols
https://drive.google.com/file/d/1jEUJ23r1vTYXXoI21I1PexlfiIetJVzv/view
(source: [Reddit post](https://www.reddit.com/r/rainworld/comments/1bei8sy/i_created_a_fully_functional_typeface_for_every/))
![[rainworldsymbols.png|700]]
##### le doc
https://docs.google.com/document/d/1QZnQgeoW3RyoR3_ZR1DGse99p1UPZRhU5LoVvCGUT_A/edit
(source: [RW Main](https://discord.com/channels/291184728944410624/296133304632213504/822957346711928922))

Rain World 1
![[rain-world-1.png|700]]
Rain World 2
![[rain-world-2.png|700]]

# Converting to TrueType format

> [!example]- ouf
> As it was told before, 2 files make up for a single font:
> - bitmap image of all characters, stored as a sprite in font atlas
> - bitmap decryptor for said image, that tells location of each character in the image.
>
> Converting said font to modern format (`.ttf` aka TrueType) is hard due to 2 reasons:
> - such weird file structure is made by [BMFont](https://www.angelcode.com/products/bmfont/), and barely any app supports it
> - TrueType format supports vector images, while RW fonts are based on bitmap image (which is raster)
>
> Okay, let's get started.
> For entire procedure, you'll need 4 utilities and make sure they will work (have been tested on Linux Mint 22):
> - [AssetRipper](https://assetripper.github.io/AssetRipper/articles/Downloads.html): to extract multiple files from the game
> - [TextureUnpacker](https://tu.enea.sk/  ) (is online, no need to download): to pull bitmap images out of sprite atlas
> - [monobit](https://github.com/robhagemans/monobit) *(requires Python to run)*: to convert BMFont files into something that is supported by the following app
> - [Bits'N'Picas](https://github.com/kreativekorp/bitsnpicas) *(requires Java to run)*: to vectorize the font and export to TTF.
>
> For the following tutorial, english font sprite that is used for slugcat campaign select screen, will be used as example. In your case, you'll have to replace file names with the ones you need.
> Here are the steps:
> 1. Open AssetRipper, open `assets.resources` in it.
> Extract the following files:
> - `displayFont` as text
> - `fontAsset` as image and `.json` file
>
> 2. Open Texture Unpacker. Open `fontAsset.png` image in it, then `fontAsset.json`. Download the archive it provides.
> It will contain 3 files: `font.png`, `displayFont.png` and `ps4Glyphs.png`. In this tutorial, only `displayFont.png` will be useful.
> 3. Open terminal go to the folder where `displayFont.png` is located, paste the following:
> `monobit-convert displayFont.txt --format=amiga`
> It will create `displayFont.font` in same folder.
> 4. Open Bits'N'Picas, open the file you just created (`displayFont.font`), export as  `.ttf`.
>
> As alternative in step 3, you can convert `displayFont.txt` using BDF format (`--format=bdf`) .
> But be warned that all font positioning will be incorrect; you'll have to modify it manually.
> First of all, you have to make baseline location correct.
> Double click any letter, check where black line is; that's baseline, the letters need to stand on it.
> On the left, scroll up and select `All glyphs in Font`, if it wasn't already selected before. Then, `Edit` tab -> `Select all`; move characters by selecting `Transform` tab -> `Nudge up` / `Nudge down`.
> Then, double click any letter and drag little arrows on sides to set up everything correctly:
> ![[font-theory.png]]
> You're done! Feel free to export.