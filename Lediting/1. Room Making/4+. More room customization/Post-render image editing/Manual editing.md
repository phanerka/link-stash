Entire room coloring is made via [[Exploring contents/Base game n Downpour/Shaders#Documentation on LevelColor shader|LevelColor]] shader.

  
45 degrees:  
https://youtu.be/WgXjyBE6-IA  
effect colors:  
![[rendered-room-colors.png]]

shit i forgot the source

### decomposing & composing rendered rooms  
[composing](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/lediting/render-edit/Screen_Maker-iuPPf9f6qhusUKxbR7Sng3ZPfh2TdO.ipynb)  
[decomposer](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/lediting/render-edit/Screen_Decomposer-roU2EDl43T7j8AhPBV2QQIfKPOc5Th.ipynb)  
run in google collab

[viewer](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/lediting/render-edit/Level%20Viewer-ZoJp2B2T4gf2Z6chb0tduxxhJakwfF.ipynb)

```
I’ve used it to hand paint levels, but the screen decomposer can be used to tweak existing rooms. The benefit is having more control than leditors give.  
For example, maybe you want:  
• grime on everything  
• to change the shape of pipes  
• different camera perspectives  
• stable decals between close cameras  
• to use effect colors for extra shading  
• to use the *”Secret 3rd effect color”* (white for batfly hives)   
TODO put a preview of this somewhere  
• to do a bit of touch-up

To avoid Google Colab you can use Jupyter Notebook, Spyder, and the like. If you want use the old versions or modify the new ones (just change the file input/output stuff) then you could use a mobile app like Carnets.
```

Room rendering documentation #docs  
[the doc](https://nqywadcmwusjqlrg.public.blob.vercel-storage.com/notes/files/lediting/render-edit/Manual%20Camera%20Rendering-dRiTNeFHKb6cMFENUkcMmEcMgOu45X.pdf)

(source: [RWMA](https://discord.com/channels/1083481230839922688/1083483045329375393/1304508041189916714))

todo: replace with [[Exploring contents/Base game n Downpour/Assets/index#Documentation on LevelColor shader]]  
another doc on LevelColor shader (how the game renders rooms):   
https://gist.github.com/EtiTheSpirit/97dfdc63f667e19acb6314dc8c1e2d18

wiki page  
https://rainworldmodding.miraheze.org/wiki/Level_Image_Format