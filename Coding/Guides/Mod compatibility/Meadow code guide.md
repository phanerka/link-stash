### Things to know (very important!)  
If you're reading this doc, it's implied you're acknowledged with following concepts:  
1) Basics of networking structure in Meadow (mix of host-client AND p2p)  
	https://www.youtube.com/watch?v=-_WsvZAkFZI  
2) Difference & usage of abstractized and realized objects in Rain World  
	YT video (longer but imo it's better): https://www.youtube.com/watch?v=XEEahVX4kLw  
	Wiki page: https://rainworld.miraheze.org/wiki/Technical_Glossary/Abstractization  
3) *(optional)* List of technical terms used regarding Rain World (?) (you don't need mÄth, don't worry)  
	https://rainworld.miraheze.org/wiki/Technical_Glossary  
	*A little note: Meadow implements [own](https://github.com/henpemaz/Rain-Meadow/blob/main/Online/Entity/OnlineEntity.EntityId.cs) EntityId class, for online entities. Don't confuse it with [base game's one](https://rainworld.miraheze.org/wiki/Technical_Glossary/Entity_ID).*

  
If you know C# on basic level, here are concepts that might help you to understand things more:  
- basic concepts required for common RW modding ([[Coding/Getting started#Things to know|here]]'s the list)  
- attributes (creation and usage)  
- LinQ (wawa....)  
- more to add.

Now, let's begin! 🎉



abstractSpear.needle - most likely to identify spearmasters spears

:3   
this sillyhead forgets that dnspy shows only one spot where variable is used in the class

anyway  
im trying to figure out how things work by myself :3 sometimes im guessing to compensate for my lack of knowledge

online/resource/lobby.cs  
```cs  
public List<KeyValuePair<OnlinePlayer, OnlineEntity.EntityId>> playerAvatars = new(); // guess we can support multiple avatars per client  
```

(?) all player input data is synced by default, meaning movement-based slugcat things will be synced by default.  
### Attributes

### DeltaSupport attribute  
Attribute properties:  
- `StateHandler.DeltaSupport level` - dictates how to treat delta states ig.    
	Possible values:  
	- `StateHandler.DeltaSupport.None` - will not detect state differences AT ALL  
	- `StateHandler.DeltaSupport.FollowsContainer` - data differences will be detected if and ONLY if container\* data differences have been detected    
	- `StateHandler.DeltaSupport.NullableDelta` - like "Full", but also considers `null` value valid  
	- `StateHandler.DeltaSupport.Full` - default.

\*When creatures/objects start depending on another position wise (maybe somehow else as well? idk), they can be put in container (lizard carries a slugcat -> lizard is a container for said slugcat, batflies have been speared -> spear is a container for batflies, hunter holds a spear on their back -> the slugcat is container for the spear) (?)  
#### OnlineField attributes  
Variations:  
- `[OnlineField]`: default go-to one.  
- `[OnlineFieldHalf]`: if value is float, its will be [converted](https://docs.unity3d.com/2020.2/Documentation/ScriptReference/Mathf.FloatToHalf.html) into half to reduce amount of data transferred.  
- `[OnlineFieldColorRgb]`: for Unity's`Color` class variable. On serialization, transforms it into a set of `byte` variables with red, green and blue channels value. Is used to send players color customization.  
> [!warning] Note, alpha color isn't encoded!  
> ... i wonder if it causes any issues in the future....

OnlineField attribute properties:  
- `string group` (default: `"default"`): things on the same group are grouped in deltas, saving bytes  
exist: input (inputs?), entitydefs, entities, data, realized  
- `bool nullable` (default: `false`) - field can be null  
- `bool polymorphic` (default: `false`) - type of field needs to be serialized/parsed  
- `bool longList` (default: `false`) - field needs ushort for indexes rather than bytes  
- `bool always` (default: `false`) - field is always sent, to be used as key

  
OnlineEntity contains of  
 - `EntityId id`  
 - `OnlinePlayer owner` (player who owns that thing)  
 - `bool isTransferable` (whether its ownership can be transferred to another person or not (?))

OPO - OnlineEntity + APO

OPOD (OPODefiniton) structure: (used for creating a new online object from scratch, that has no APO: `ApoFromDef()`)  
- `int apoId` (own ID cause RW IDs suck :3)  
- `ushort apoSpawn` (idk)  
- `AbstractPhysicalObject.AbstractObjectType apoType` (type of APO; the list can be looked up in [[Technical files#Object IDs]])

Present new type of objects called `OnlinePhysicalObject` aka OPO in short:  
OPO consists of:  
entityDefinition (?) + inResource (?) + state of APO (AbstractPhysicalObject)  
state of APO records variable data every tick i suppose

### Code structure  
`Online`: woah there's a lot of stuff!... Gotta go thru it to explain.  
`Online/State/*`: handling online objects (send / receive data and override local variables)  
More info [here](https://github.com/TheLazyCowboy1/RainMeadowSyncTemplate#states)  
`Online/State/OnlineState.cs` defines [[Meadow code guide#Attributes|OnlineState]] and [[Meadow code guide#OnlineField|DeltaSupport]] attributes.  
`public StateHandler(OnlineState.StateType stateType, Type type)` function: takes case of delta state similarity detection, i suppose  
`Online/Serialization/`: prepping info to send, i guess?  
- deflating (compressing data, in simple (and rude) words, doing what .zip does)  
- serializing (converting classes data into text and vice versa)  
- generics hell (generics hell :3 )  
`Online/Events/` : watching players connections and notifying when they leave, i guess  
`Online/RPCs.cs` - list of all modes wide callable RPCs  
`Online/RPCManager.cs` - defines RPC templates, let's say (hope its phased well enough)  
`Online/ConsumableRPCs.cs` - list of RPCs that are caused by consumable items (wheres an explosion tho???)  
`Online/DebugOverlay.cs` -  renders additional info regarding other players' connection in DevTools  
Handling hooks:   
- `Game/*Hooks.cs` for all game modes  
- `X/XHooks.cs` for respective game mode (where X is name of game mode: `Arena`, `Story`, `Meadow`)

  
Folder structure  
- `OnlineUICompeonents`: chat  
- `Mod` : compiled mod, ready to be moved in RW local mod folder.