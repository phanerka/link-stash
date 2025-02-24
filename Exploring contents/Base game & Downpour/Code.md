Most of stuff is in assembly-sharp-public. You know how to [[Debugging & troubleshooting|decompile]] it, right?  
#wiki  
https://rainworldmodding.miraheze.org/wiki/Rain_World_Code_Structure

Downpour code comes with base game code; its usually marked with "`is.MSC()`" check.  
> [!warning] **Do NOT copy DLC code or disable DLC checks!**  
> Your mod will be deleted from Workshop, once discovered.

https://mszegedy.github.io/rw-api-doc/html/index.html  
(but still highly suggested to explore locally as DnSpy got more features)

Some logic is covered in User Wiki made by Alphappy. 

### Referencing variables  
This might help.  
and i should extend and redraw that AAAAAAAAAAAAA  
![[variable-references-structure.png]]  
(source: [RWMA](https://discord.com/channels/1083481230839922688/1083483097145819348/1086547453010001960))

### Weird naming  
if you cannot find a certain item/creature in game code, maybe it's actually named differently. You can look its name up in official RW wiki. example: popcorn plant -> [SeedCob](https://rainworld.miraheze.org/wiki/Popcorn_Plant) (check "Code name" in object card), iterator -> [Oracle](https://rainworld.miraheze.org/wiki/Iterator#Trivia).

Known typos: Signal -> Singal. 

### Magic numbers  
Yeah.

> [!example]- Camera default layers  
> 0 - Shadows  
> 1 - BackgroundShortcuts  
> 2 - Background  
> 3 - Midground  
> 4 - Items  
> 5 - Foreground  
> 6 - ForegroundLights  
> 7 - Shortcuts  
> 8 - Water  
> 9 - GrabShaders  
> 10 - Bloom  
> 11 - HUD  
> 12 - HUD2

> [!example]- Slugcat sprites  
> 0 - BodyA (Body)  
> 1 - HipsA (Hips)  
> 2 - Futile_White (Tail)  
> 3 - HeadA0 (Head)  
> 4 - LegsA0 (Legs)  
> 5 - PlayerArm0 (Arm scaleY = -1f)  
> 6 - PlayerArm0 (Arm)  
> 7 - OnTopOfTerrainHandPole (Climbing arm)  
> 8 - OnTopOfTerrainHandPole (Climbing arm scaleX = -1f)  
> 9 - FaceA0 (Face)  
> 10 - Futile_WhiteGlow (From Neuron fly)  
> 11 - pixel (Mark of Communication)  
> 12 - MoonCloakTex (Moon's Cloak)  
> 

> [!example]- Animation indecies  
> None  
> CrawlTurn  
> StandUp  
> DownOnFours  
> LedgeCrawl  
> LedgeGrab  
> HangFromBeam  
> StandOnBeam  
> ClimbOnBeam  
> GetUpToBeamTip  
> HangUnderVerticalBeam  
> BeamTip  
> CorridorTurn  
> SurfaceSwim  
> DeepSwim  
> Roll  
> Flip  
> RocketJump  
> BellySlide  
> AntlerClimb  
> GrapplingSwing  
> ZeroGSwim  
> ZeroGPoleGrab  
> VineGrab  
> Dead 

(source: [RW Main](https://discord.com/channels/291184728944410624/305139167300550666/1200692551439626281))

  
> [!example]- Scav sprites  
> 0: Chest  
> 1: Hips  
> 2: Head

> [!example]- Lizard sprites  
> 0 : body mesh  
> 1 - 5 : body circles  
> 6 : tail  
> 7 - 10 : limbs  
> 11 - 15 : head  
> 16 - 19 : limb coloration

  
//0: can't grab. 1: can grab, will be overlapped by others. 2: can grab. 3: can grab, and dual wield together with a 1. 4: uses both hands.

//0 - doesn't count as kill, 1 - counts as a kill but won't increase Outlaw passage, 2 - full kill

//-------------------------------- Sprite Leaser----------------------------------------  
// The sprite leaser class consists of a list of sprites and a reference to a drawable object.  
// Each frame it lends itself to that object, and allows it to manipulate the sprites.   
// This way the storage of sprites is entirely contained in the camera object, and game objects  
// don't have to worry about whether they're currently being viewed by a camera

int CogSprite(int vert, int side, int cog) { return (door.number * TotalSprites) + (vert * 4) + (side * 2) + (1 - cog); }//0-7  
int BehindPansarSprite(int side) { return (door.number * TotalSprites) + 8 + side; }//8-9  
int PoleSprite(int pole) { return (door.number * TotalSprites) + 10 + pole; }//10-13  
int TrackSprite(int side, int vertical) { return (door.number * TotalSprites) + 14 + (vertical + side + side); }//14-17  
int CenterTrackSprite(int vertical) { return (door.number * TotalSprites) + 18 + vertical; }//18-19  
int ClampSprite(int side, int clamp) { return (door.number * TotalSprites) + 20 + (clamp * 2) + side; }//20-37  
int BlockSprite(int side, int block) { return (door.number * TotalSprites) + 38 + block + side + side; }//38-41  
int HandSprite(int side, int block) { return (door.number * TotalSprites) + 42 + block + side + side; }//42-45  
int ArmSprite(int side, int block) { return (door.number * TotalSprites) + 46 + block + side + side; }//46-49  
int BoltSprite(int bolt) { return (door.number * TotalSprites) + 50 + bolt; }//50-53  
int PansarSprite(int side) { return (door.number * TotalSprites) + 54 + side; }//54-55  
int PansarSegmentSprite(int segment) { return (door.number * TotalSprites) + 56 + segment / 2 + (segment % 2 == 0 ? 0 : 5); }//56-64  
int BigScrewSprite(int vertical) { return (door.number * TotalSprites) + 65 + vertical; }//65-66  
