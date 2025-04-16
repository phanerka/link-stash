---
draft: true
---
DEV TOOLS

rifts: floating debris (Decorations page2)

multiplayer item? what lmao


warping
gameplay page1: WarpPoint
page2: DynamicWarpPoint, SpinningTopSpot?

should add on raindeer / skywhale stuff or naw?


MOUSE DRAG EXPLORER
items save string (example on spear):
`Spear.AbstractSpear.ToString()`

creatures save string (example on lizard):
copy value of `Creature.AbstractCreature` property
find `SaveState` class via object explorer
find `SaveState.AbstractCreatureToStringSingleRoomWorld(AbstractCreature)` method, paste the property in parameters, evaluate

holy its so cool



CODE

(and all subtypes of `PlacedObject.Data`) `PlacedObject.Data.ToString()`: how its stored in settings files as i understand