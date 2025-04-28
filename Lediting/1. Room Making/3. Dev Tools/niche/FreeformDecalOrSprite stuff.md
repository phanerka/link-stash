---
draft: true
---
#regionKit only

> 1. you can fog a room with bloom and lightburn at the same time lmao

(source: [RW Main](https://discord.com/channels/1083481230839922688/1083485771949949019/1189233543734362212))

### Applying shaders

examples:

Hologram shader
![[hologram-decal_by-rorolly_13.png]]
![[hologram-decal2_by-rorolly_13.png]]
(source: [RW Main](https://discord.com/channels/291184728944410624/481900360324218880/1326363715246882849))



water shader
![[a23-1.gif]]
(source: [RWMA](https://discord.com/channels/1083481230839922688/1083483045329375393/1203462073556926524))


use as prop
![[prop-decal_by-merfaruk.png]]
(source: [RWMA](https://discord.com/channels/1083481230839922688/1083485771949949019/1189234052868341932))

bloom effect
![[Localbloom.gif]]
(source: [RWMA](https://discord.com/channels/1083481230839922688/1083483045329375393/1208488425154547822))

Heat distortion effect
example: [[RegionKit#Machine objects|here]] (that moving effect in center of the engine)

> [!example]- List of applicable shaders
>
> HoldButtonCircle
> GoldenGlow
> ElectricDeath
> VoidSpawnBody
> SceneLighten
> SceneBlurLightEdges
> SceneRain
> SceneOverlay
> SceneSoftLight
> HologramImage
> HologramBehindTerrain
> Decal
> SpecificDepth
> LocalBloom
> MenuText
> DeathFall
> KingTusk
> HoloGrid
> SootMark
> NewVultureSmoke
> SmokeTrail
> RedsIllness
> HazerHaze
> Rainbow
> LightBeam
> CicadaWing
> BulletRain
> CustomDepth
> UnderWaterLight
> FlatLight
> FlatLightBehindTerrain
> VectorCircle
> VectorCircleFadable
> FlareBomb
> Fog
> WaterSplash
> EelFin
> EelBody
> JaggedCircle
> JaggedSquare
> TubeWorm
> LizardAntenna
> TentaclePlant
> LevelMelt
> LevelMelt2
> CoralCircuit
> DeadCoralCircuit
> CoralNeuron
> Bloom
> GravityDisruptor
> GlyphProjection
> BlackGoo
> Map
> MapAerial
> MapShortcut
> LightAndSkуBloom
> SceneBlur
> EdgeFade
> HeatDistortion
> Projection
> SingleGlyph
> DeepProcessing
> Cloud
> CloudDistant
> DistantBkgObject
> BkgFloor
> House
> DistantBkgObjectRepea
> Dust
> RoomTransition
> VoidCeiling
> FlatLightNoisy
> VoidWormBody
> VoidWormFin
> VoidWormPincher
> FlatWaterLight
> WormLayerFade
> OverseerZip
> GhostSkin
> GhostDistortion
> GateHologram
> OutPostAntler
> WaterNut
> Hologram
> FireSmoke
> Basic
> LevelColor
> Background
> WaterSurface
> DeepWater
> Shortcuts
> DeathRain
> LizardLaser
> WaterLight
> WaterFall
> ShockWave
> Smoke
> Spores
> Steam
> ColoredSprite
> ColoredSprite2
> LightSource
> LightBloom
> SkyBloom
> Adrenaline

(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/995066729082388661))
For shaders preview, check [[Exploring contents/Base game n DLCs/Assets/Shaders|Shaders]] page.

### Animated decal

examples:
![[RainWorld_D3Dix48QRk.gif]]

![[RainWorld_6ds6xhh7U9.gif]]
one (source: [RW Main](https://discord.com/channels/291184728944410624/481900360324218880/1331360762337431612))
two (source: [RWMA](https://discord.com/channels/1083481230839922688/1083484064549437470/1224797331799670844))

guide

> first, create the frames you want to have. They should be named 0001 0002 0003 and so on.
i do that with blender

first you will have to get ffmperg from the internet
i got mine from https://www.gyan.dev/ffmpeg/builds/ the essential package one

then you open your comand prompt, via win+r. type cmd then enter.
cmd opens.
then enter the path to your ffmpeg, because it doesnt always do that itself
for me it is i downloads so ``C:\Users\ATOM\Downloads``
then the command should be
``C:\Users\ATOM\Downloads\ffmpeg-2024-03-28-git-5d71f97e0e-essentials_build\bin\ffmpeg -hide_banner -i C:\tmp\%04d.png -r 24 -pix_fmt yuva420p -c:v libvpx -b:v 2M -metadata:s :v: 0 alpha_mode="1" -auto-alt-ref 0 -y C:\Users\ATOM\Documents\output.webm``
In this command:
- ``-i C:\tmp\%04d.png`` specifies the input image sequence. location being C:\tmp\, or where blender outputs stuff by default. It uses all avaliable images that fit the description, it can be any images as long as they are png and named correctly. be carefull. It should accept resolution changes fine.
- ``-r 24`` sets the output frame rate to 24 fps.
- ``-pix_fmt yuva420p`` specifies the pixel format.
- ``-c:v libvpx`` selects the VP8/VP9 codec for video encoding.
- ``-b:v 2M`` sets the target bitrate for video encoding to 2 Mbps.
- ``-metadata:s :v: 0 alpha_mode="1"`` adds metadata to specify alpha channel mode.
- ``-auto-alt-ref 0`` disables automatic alternate reference frames.
- ``-y`` overwrites output files without asking.
- ``C:\Users\Documents\output.webm`` specifies the output filename with the .webm extension.
then put the ``output.webm`` (rename it) in to the decals folder
in rainworld, use custom decalorsprite from regionkit
enter the decal name as decal.webm othewrise wont show you anything
a oof


(source: [RWMA](https://discord.com/channels/1083481230839922688/1083483045329375393/1249297299662704681))