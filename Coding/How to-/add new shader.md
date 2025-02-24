---
dg-publish: true
---
### Prerequisites
You need unity with same version of rain world (check [[Unity version|here]] for more info)


guide: 
https://docs.google.com/document/d/16IPRW0ulD2sWIXtqj8W3jMq6KQFtn14z9iHPKZB3tLY/edit
(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/1237835470080180235))

https://twitter.com/joar_lj/status/1525445116789497856 (a [mirror](https://nitter.poast.org/joar_lj/status/1525445116789497856) for non-twitter users)

https://github.com/PJB3005/RainWorldMods/tree/master/ShaderReload for hot reload


**Exploring existing shaders:** [[Assets#Shaders]]

;-; i dont wanna copy stuff


(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/858276294353092609))

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


> **Shaders, Lighting, and Shadows Information (For Shader Authors)**
> 
> This post addresses quirks with the lighting engine and how it interacts with custom shaders, as well as the available shader keywords and uniforms.
> 
> For some background, Futile is a bit of a frankenstein's monster when it comes to iteroperability with base Unity systems; while Unity shaders work, the behavior is overshadowed by Futile's layer system. This caused me to spend more hours than I care to admit trying to figure out why an unlit holographic/additive shader I wrote was casting shadows. It was pretty terrible to deal with.
> 
> Rather than witness people deal with that again, I spent the past couple hours gathering information and testing. You can read up on necessary information about the renderer here: <https://gist.github.com/EtiTheSpirit/655d8e81732ba516ca768dbd7410ddf4>
> 
> This should save shader authors a lot of time and headache c:

source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1128354653051044023)


### Basic shaders tutorials


wawa