*Log locations are described [[Logs|here]].*

Live logging:
- here in tips waaa
You can log variables on runtime if you [[DNSpy#Attaching|attach DNSpy]] to the game.


3 logging functions:
- `Logger.LogDebug(string)`: **recommended**.
	BepInEx function, outputs to `LogOutput.log`
	*Documentation:*
	https://docs.bepinex.dev/articles/dev_guide/plugin_tutorial/3_logging.html
- `Debug.Log(string)`
	Unity function, outputs to `consoleLog.txt`
	Isn't ready when `OnEnable` runs (source: [RWMA](https://discord.com/channels/1083481230839922688/1083483097145819348/1334384577371705367)), unlike the one above.
- `Custom.Log(string)`
	Custom logging functions.
	Are frequently used in base code but please don't use it, since:
	- `Log()` outputs to literally nowhere
	- `ImportantLog()` literally uses `Debug.Work()` %% TODO:: is it called like that?%%