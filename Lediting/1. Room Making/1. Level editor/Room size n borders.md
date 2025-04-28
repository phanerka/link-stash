Default size:
- `72 × 43` tiles (for a single-screen room)
- `48 × 35` (w/o borders, single-screen room)

# Multi-screen rooms
### Multi-screen room templates
#templates
https://solaristheworstcatever.github.io/Repo-Site/Dist/Templates/Size%20Templates.zip
For separate files download:
https://github.com/solaristheworstcatever/The-Level-Editor-Warehouse/tree/main/LevelEditorProjects/Templates/Size%20Templates

### Setting up manually
Approximate formula for calculating multi-screen room size:
https://rainworldmodding.miraheze.org/wiki/Level_Editor#Level_Size
![[level-size.png]]
 (^ source: was yoinked from wiki and posted in [RWMA](https://discord.com/channels/1083481230839922688/1083506128010358915/1217925887518048296))

%%
For more precise formula, here's this spoiler v
> [!info]- Putting on nerd glasses
> I tried figuring out where these numbers came from.
> It seems that 40 / 52 is inside all borders + outside all borders
> and 20 / 3 is all inbetween.
> But it's incorrect way to calculate.
>
> The issue with this formula is that with bigger amount of screens, *actual* borders will differ from set ones (12 tiles on sides, 3 on top and 5 on bottom), leading to some part of main area getting outside of 4 : 3 camera.
> Said case should be avoided, since someone that uses 4 : 3 resolution in game would experience following issues:
> - creatures will be able to walk into area the player simply can't see
> - edges of the area might be important/useful for the player but they, yet again, will not walk into it due to impossibility to see what's there
>
> A prime example of breaking said rule is arenas: a decent part of them is simply not visible in 4 : 3 resolution.
>
> \[imagine a pic here]
> *thank you painworld* very cool
> *i cant even see pipe exits*
>
> Now let's talk about proper size calculation.
> Common multi-screen structure consists of:
> - a row of 4 : 3 screens touching each other (in general, they do not intersect nor have space in-between)
> - borders on sides
>
>
> TODO:: okay what the fuck is that shit v. where is it pulled from. from what ass.
> verify
>
> The game takes the `1024 x 768` (4 : 3) resolution as base (as well as for camera size). *Any other resolution is just this one being scaled to said resolution's height with width being extended.*
> \[imagine a pic here]
> *A proof: no matter what resolution is, the game uses same spot to switch cameras.*
>
> Considering 1 tile is 20 pixels, said resolution is `51.2 x 38.4` tiles wide.
> Considering these cameras touch each other in multi-screen rooms (thus there's no space in-between them), we get the following formula:
> `[size of 4 : 3 screen] x N + [total borders size]`
> To calculate total borders size (left + right for x and above + below for y), we can take single screen room dimensions which are `72 x 43.`
> `72 - 51.2 = 20.8`, `43 - 38.4 = 4.6`.
>
> So we get the following formula:
> `51.2 x N + 20.8` for X
> and
> `38.4 x N + 4.6` for Y,
> both being rounded to closest number.
>
> thx for visiting my ted talk hope you enjoyed it

%%
# Borders

On room render, ONLY area inside border is preserved for geometry data; everything else past it will repeat the closest column / row closest to border.
This might cause unintentional issues such as:
- death pit
- infinitely out-of-bounds extending pole
- possibility to go *out of bounds* in a supposedly closed area
- unfinished pipe connection (which leads to game freeze on room loading)

A visual explanation:
\[pic here im lazy to put it here rn]