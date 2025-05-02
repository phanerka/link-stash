yeah.

its just \_bkg.png
same size as room render
separate bkg image to separate room image!

Base game doesn't use such feature at all but MSC does a lot

> [!example]- example
> bruh not done yet

It's always purely white image but different areas vary in transparency
Value varies. In general, they're 10-30% transparent, rarely reach 50% or drop down to 4%

It's enough to reset cycle to update background / palette images used.
# Making of

Henry's Leditor comes with built-in feature to make layer 4 images.
unless someone makes a script for krita, idk if there can be better solution.
## Via masking
- pros: multi layer support, easy to import grayscale picture, more correct color output
- cons: can't see the result right away

*The point: make flat grayscale image and apply it as mask for purely white layer.*

should work in any advances program, ill use Krita for example.
make a layer group, put everything grayscale there
then merge it all to get a single picture (you can clone the folder, for backup)
then create a new layer, fill it with white
and apply the grayscale image as mask
ure done, save as png n stuff

sai 2 cannot allow to use existing layer as mask, unfortunately
so i came up with different solution for it

create a new layer, fill with white, apply "Difference" mode on it, merge with base image
then, "layer" -> "convert luminance to opacity"
and then, alpha lock the layer and fill it with white (yes, you can even use bucket on it)
done! ✨
%%
i think im deleting the one below
## Via overlay effect
- pros: given you've got image, you can check how it will approximately look in game
- cons: worse opacity control, first layer has to contain all shapes


New layer with "Overlay" effect and 100% opacity will increase old opacity *twice*.

### Examples
[RW Main](https://discord.com/channels/1237826015829557400/1237912787959812148/1329229720663097465)
%%

# Palette modification
The way how layer4 looks in game heavily relies on 2 colors in palette used.
%% oops i forgor rain palette %%
![[layer4.png]]