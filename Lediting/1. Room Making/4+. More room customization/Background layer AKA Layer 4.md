yeah.

its just \_bkg.png
same size as room render
separate bkg image to separate room image!

Base game doesn't use such feature at all but MSC does a lot

Value varies. In general, they're 10-30% transparent, rarely reach 50% or drop down to 4%

# Making of

Henry's Leditor comes with built-in feature to make layer 4 images.


unless someone makes a script for krita, idk if there can be better solution.
## Using filter masks
- pros: live preview, multi-layer support
- cons: not precise (might change color transparency by a few %), requires krita (it might be laggy for some people)

create a group where you will do layers  
and apply filter mask to the group "Add.. " -> "Filter mask"  
Leave threshold to 100, change color to pure black  

add another filter mask, *below the prev one*  
adjust -> threshold, slide down to 0  
it will make all images grayscale & fix some color not being purely white  
thats all 🔥 draw any grayscale opaque layers in the group, and you will get result right away

and friendly reminder to change colorpickers "Color Sampler" settings to "Sample current layer" instead of "Sample All Visible Layers"

Okay ive been thinking of it for a bit.  
Got 2 ideas: via masking and via overlay effect.  
If you've got other ideas, let me know.  
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

i think im deleting the one below
## Via overlay effect
- pros: given you've got image, you can check how it will approximately look in game
- cons: worse opacity control, first layer has to contain all shapes


New layer with "Overlay" effect and 100% opacity will increase old opacity *twice*.

### Examples  
[RW Main](https://discord.com/channels/1237826015829557400/1237912787959812148/1329229720663097465)

