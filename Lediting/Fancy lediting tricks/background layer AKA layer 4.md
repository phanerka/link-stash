yeah.

its just \_bkg.png
separate bkg image to separate room image!

Value varies. In general, they're 10-30% transparent, rarely reach 50% or drop down to 4%

values (out of 255):
136 (53%), 91 (36%), 70 (27%), 39 (15%)
70 (27%), 54 (21%), 39 (15%) 
109 (43%)
51

33 (13%)
36 (14%)
43, 60, 23 (9%)
9 (4%)
# Making of

wow ive been thinking bout that  
and for now, ive come only one decently good solution  
the single downside is that it requires krita and it might be a laggy solution for some people
also its not precise tbh, might change color transparency by a few %  

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
- pros: more control over scene overall, multi layer support, works with any grayscale picture
- cons: can't see the result right away

## Via overlay effect
- pros: given you've got image, you can check how it will approximately look in game
- cons: worse opacity control, first layer has to contain all shapes


New layer with "Overlay" effect and 100% opacity will increase old opacity *twice*.

### Examples  
[RW Main](https://discord.com/channels/1237826015829557400/1237912787959812148/1329229720663097465)

