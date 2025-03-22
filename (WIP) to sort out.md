tbh i wanna also ask for custom decals that are free to use

"if ure patching the mod, u have to reaload it asap or else debugger will break"  
need to check this one once again. with palette creator

? rw main
https://discord.com/channels/291184728944410624/1349120847306293338

*atmo atmo atmo*
https://github.com/thalber/Atmo

https://discord.com/channels/291184728944410624/296133304632213504/1113545138204057650
worm grass values mod
is there any other mod that does the same thing?


yet another blender file n explanation  
(source: [RWMA](https://discord.com/channels/1083481230839922688/1238553690047119481/1291452791729950873))

  
tile viewer :3 (does it workie properly?) rwms  
https://discord.com/channels/1237826015829557400/1237868553450029208/1336442384388460577

  
txt = new FLabel("font", "");

bro what? is it finished???  
https://rainworldmodding.miraheze.org/wiki/Custom_Assets#Simple_/_UI_implementations

Rain World Composite Screenshots:  
https://ln.sync.com/dl/5644eba30/jtkgzkhc-jxeja24s-h3edv9g3-v84qz7kn  
(source: [RW Main](https://discord.com/channels/291184728944410624/296133304632213504/518599984258613248))

o0  
https://rainworldmodding.miraheze.org/wiki/DebugMouse  
isnt it better to turn into a mod  
or is there one already?

  
image converter  
oldie  
https://ln.sync.com/dl/357bdf1b0/z6tktgzw-a77f8imc-yw45zfsd-aytdk8hz

^ is it really useful at these days?

v newer one  
(source: [RW Main](https://discord.com/channels/291184728944410624/431534164932689921/772724366017691648))

  
a shitpost doc??? is it even conprehensible???  
https://docs.google.com/document/d/1ZYdP58SA1_b5otzLhNYnkilrUuwhNutcrXAMwjryj7k/  
(source: [RW Main](https://discord.com/channels/291184728944410624/965639206561009664/1309660909739708437))

Layers to create a full room  
(source: [RWMA](https://discord.com/channels/1083481230839922688/1083484064549437470/1306379121911136380))  
(source: [RWMA](https://discord.com/channels/1083481230839922688/1083484064549437470/1294397902231179418))

  
phew. oh my god.  
when will i deal with all that stuff

  
### people to annoy  
:3 :leditoroverload: :3

https://discord.com/channels/1083481230839922688/1083485771949949019/1326940012301914215 rwma  
distant city asset creator!!!!  
and rain shader!!!!

imma put unfinished cool shader here and pretend its supposed to be here  
[https://github.com/LudoCrypt/TurnRain](https://github.com/LudoCrypt/TurnRain "https://github.com/LudoCrypt/TurnRain") ([preview video]([https://www.youtube.com/watch?v=8-oeALLoL4A](https://www.youtube.com/watch?v=8-oeALLoL4A "https://www.youtube.com/watch?v=8-oeALLoL4A")))  
Explanation:   
> First we must understand how rain world knows how to draw rain. In vanilla, at room init, it makes a 'mask' texture the size of the level, basically going through every column and painting red, until it finds a solid block, then paints the rest black. Then in the shader it doesnt draw rain anywhere where it's black. So here was the plan: Redraw said mask texture but with an angle to it. Lets begin:  
>   
> 1. Make a texture twice the size of the level  
> 2. Go through every piece of geometry and paint four black pixels on the texture (because its upscaled)  
> 3. Add a pixel in the corner of two solid pieces of geometry (this is so it looks less blocky)  
> 4. Start in the bottom left corner of the image and move down x pixels (x is based on the angle) and right 1 pixel. If it is not black, dont do anything, but if it is black, paint the rest of the pixels on that path black.  
> 5. Move up x pixels and repeat.  
> 6. Once you reach upper oob, stop, and continue the process but moving right each time, instead of up.  
>   
> After this, I just clear the mask texture and replace it with the new one. Then for the actual rain angle I just change rainDirectionGetTo to whatever the new angle is

(source: [RWMA](https://discord.com/channels/1083481230839922688/1083485771949949019/1232426391522381875))


https://discord.com/channels/1083481230839922688/1083484108056957089/1305779046142971904 rmwa  
dev tools effect quick reload