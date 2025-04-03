**Exploring existing shaders:** [[Exploring contents/Base game n DLCs/Assets/index#Shaders|here]]

*WARNING: this page is on hiatus, some guides may be outdated. I want to make own shader later to confirm everything myself.*
### Prerequisites  
You need unity with same version of rain world (check [[Unity version|here]] for more info)

Full guide:   
https://docs.google.com/document/d/16IPRW0ulD2sWIXtqj8W3jMq6KQFtn14z9iHPKZB3tLY/edit  
(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/1237835470080180235))

you WILL have to make AssetBundle to load shader in game.

;-; i dont wanna copy stuff

oh yea i forgot about that. dammit
(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/858276294353092609))

TODO
```
For that, you might need to get [[Unity version|Unity Editor]] and compile AssetBundle on your own (i might add tutorial soon)  
ooor  
ill try to verify if it works  
and if you can create fresh bundles with it :D  
https://github.com/nesrak1/UABEA

In worst cases, ask someone in modding channel to do it for you  
Or ask me, I don't mind
```
  
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

### Shader hot reload
#utils 
For hot reload (duh)
TODO ill figure out how it works.
https://github.com/PJB3005/RainWorldMods/tree/master/ShaderReload

  
### General shader tutorials
i.e. non RW related only

https://www.youtube.com/watch?v=kfM-yu0iQBk

idk if entire playlist is viable i didnt watch it yet
https://www.youtube.com/playlist?list=PLImQaTpSAdsCnJon-Eir92SZMl7tPBS4Z