#### Connecting to other modded regions  
#crs required for soft dependency.  

First, check if the connection you want to use is free: [Mod-mod connections tab](https://docs.google.com/spreadsheets/d/14wt42_ZalI5di8zpUFx3WvPWldC_L7SwIbgb_TxOpUk/edit?gid=758721855#gid=758721855) in Region Lease spreadsheet.

*Ask region mod author for permissions to connect your region to theirs.*  

After they agree, here's the list:  
(assuming `XX` is your region, `YY` is their region)
- define their mod as [[Setting up dependencies|dependency]]
- in `world\yy`, place ALL changed / new rooms for `YY` region (that connect to your region)
- in `modify\world\yy\world_yy.txt`:
	- *replace* connections of the `YY` existing room you changed to lead to own region
	- *merge* everything else related to new rooms in `YY`, which can be:
		- connections
		- creature spawns
		- conditional links
		- etc.
- set up the gate
	- add `xx_yy` gate room files to `world\gates`
	- in `modify\world\gates\locks.txt`: 
		`[ADD]GATE_XX_YY : N : M` (N is left karma, M is right karma)
- fix part of `YY` region map you modified:
	- (easy way) via replacing entire map: `world\yy`
	- (compatible with other modded regions connected to `YY`) via map merging: `modify\world\yy`
- in `world\xx`, set up rooms on your side.
	If `YY` is set as soft dependency, set up via region existence checks (CRS required):
	- connections if `YY` is enabled: `{YY}`
	- connections if `YY` is disabled: `{!YY}`

### Using DLC / modded creatures
Set them up as [[Setting up dependencies#Setting up as soft dependency|soft dependency]].