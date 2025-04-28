*Compiled shaders are encrypted in `AssetBundle`, in `Shader` folder.*
Location: `Rain World\RainWorld_Data\resources.resource`

However, source code (for referencing) is available unencrypted:
`Rain World\RainWorld_Data\StreamingAssets\shaders`

>[!example]- List of all game shaders
> - `Basic`
> - `LevelColor`
> - `Background`
> - `WaterSurface `
> - `DeepWater`
> - `Shortcuts`
> - `DeathRain`
> - `LizardLaser `
> - `WaterLight`
> - `WaterFall`
> - `ShockWave`
> - `Smoke`
> - `Spores`
> - `Steam`
> - `ColoredSprite`
> - `ColoredSprite2`
> - `LightSource`
> - `LightBloom`
> - `SkyBloom`
> - `Adrenaline`
> - `CicadaWing`
> - `BulletRain`
> - `CustomDepth`
> - `UnderWaterLight`
> - `FlatLight`
> - `FlatLightBehindTerrain`
> - `VectorCircle`
> - `VectorCircleFadable`
> - `FlareBomb`
> - `Fog`
> - `WaterSplash`
> - `EelFin`
> - `EelBody`
> - `JaggedCircle`
> - `JaggedSquare`
> - `TubeWorm`
> - `LizardAntenna`
> - `TentaclePlant`
> - `LevelMelt`
> - `LevelMelt2`
> - `CoralCircuit`
> - `DeadCoralCircuit`
> - `CoralNeuron`
> - `Bloom`
> - `GravityDisruptor`
> - `GlyphProjection`
> - `BlackGoo`
> - `Map`
> - `MapAerial`
> - `MapShortcut`
> - `LightAndSkyBloom`
> - `SceneBlur`
> - `EdgeFade`
> - `HeatDistortion`
> - `Projection`
> - `SingleGlyph`
> - `DeepProcessing`
> - `Cloud`
> - `CloudDistant`
> - `DistantBkgObject`
> - `BkgFloor`
> - `House`
> - `DistantBkgObjectRepeatHorizontal`
> - `Dust`
> - `RoomTransition`
> - `VoidCeiling`
> - `FlatLightNoisy`
> - `VoidWormBody`
> - `VoidWormFin`
> - `VoidWormPincher`
> - `FlatWaterLight`
> - `WormLayerFade`
> - `OverseerZip`
> - `GhostSkin`
> - `GhostDistortion`
> - `GateHologram`
> - `OutPostAntler`
> - `WaterNut`
> - `Hologram`
> - `FireSmoke`
> - `HoldButtonCircle`
> - `GoldenGlow`
> - `ElectricDeath`
> - `VoidSpawnBody`
> - `SceneLighten`
> - `SceneBlurLightEdges`
> - `SceneRain`
> - `SceneOverlay`
> - `SceneSoftLight`
> - `SceneMultiply`
> - `HologramImage`
> - `HologramBehindTerrain`
> - `Decal`
> - `SpecificDepth`
> - `LocalBloom`
> - `MenuText`
> - `DeathFall`
> - `DeathFallHeavy`
> - `KingTusk`
> - `HoloGrid`
> - `SootMark`
> - `NewVultureSmoke`
> - `SmokeTrail`
> - `RedsIllness`
> - `HazerHaze`
> - `Rainbow`
> - `LightBeam`
> - `DistantBkgObjectAlpha`
> - `WaterSlush`
> - `SporesSnow`
> - `SnowFall`
> - `OESphereTop`
> - `OESphereLight`
> - `OESphereBase`
> - `MoonProjection`
> - `LocalBlizzard`
> - `LightningBolt`
> - `LevelHeat`
> - `FastSnowFall`
> - `FastLocalBlizzard`
> - `EnergySwirl`
> - `EnergyCell`
> - `DisplaySnowShader`
> - `BlizzardMapPrerenderer`
> - `Blizzard`
> - `LevelSnowShader`
> - `InterpolateWindMap`
> - `DustwaveLow`
> - `DustFlowRenderer`
> - `DustWave`
> - `DustWaveLevel`
> - `DustWaveLevelLow`
> - `BlizzardReduction`
> - `BlizzardMap`
> - `CellDist`
> - `DisplayWind`
> - `SingleGlyphHologram`
> - `WaterFallInverted`
> - `AquapedeBody`
> - `MenuTextGold`
> - `MenuTextCustom`

>[!example]+ Shaders preview in game
> ![[shaders-cheat-sheet-pt1.mp4]]
>
> ![[shaders-cheat-sheet-pt2.mp4]]

(source: [RWMA](https://discord.com/channels/1083481230839922688/1083484108056957089/1095172254549168268))

##### Shaders Tester mod
%%
Okay, a bit of explanation:
I've put this mod here, apart from the mods list in respective page, because it's highly unstable and, again, won't ever be fixed or updated. I don't want to leave people with questions just because people would potentially subscribe to all mods without a thought and without reading all these warnings.
%%
> [!warning] Disclaimer: the mod won't be updated or fixed.
> Only I asked mod author to publish the mod, and they explicitly warned me so.
> My point is that "having broken base is better than nothing"; if you don't like it, make a similar mod on your own.

*An utility to view all shaders in the game at the same time, with configuration options.*

**Requires [ImGUI API](https://steamcommunity.com/sharedfiles/filedetails/?id=3417372413) as dependency; please download it yourself.**

Steam Workshop:
https://steamcommunity.com/sharedfiles/filedetails/?id=3460778746

Press `Delete` key in game to toggle the menu; turn it off to be able to close the game xd

##### Documentation on LevelColor shader
#docs
responsible for room coloring
https://gist.github.com/EtiTheSpirit/97dfdc63f667e19acb6314dc8c1e2d18
(source: [RW Main](https://discord.com/channels/291184728944410624/838185248981385256/1150360982397386823))

wiki page
https://rainworldmodding.miraheze.org/wiki/Level_Image_Format

##### How shadows work
https://twitter.com/joar_lj/status/1525445116789497856
A [mirror](https://nitter.poast.org/joar_lj/status/1525445116789497856) for non-twitter users

