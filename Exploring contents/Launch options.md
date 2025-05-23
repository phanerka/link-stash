---
draft: true
---
# Game configuration

If certain files exist in game folder, it's possible to *temporarily* unlock some features.
Have to be located in `Rain World\RainWorld_Data\StreamingAssets\` (or in subfolder, if specified)

There are 2 types:
- proper file name (sometimes with proper contents)
	https://rainworld.miraheze.org/wiki/Configuration_Files#Existence_check
- setup values in `setup.txt` file (**Dev Tools must be enabled**)
	https://steamcommunity.com/sharedfiles/filedetails/?id=2979934883
	Yes, there's similar section on Wiki page attached above but it lacks some values, compared to Steam guide.
# Command line arguments
**Unity documentation page:**
https://docs.unity3d.com/2020.3/Documentation/Manual/PlayerCommandLineArguments.html

# Unity boot configuration file
`Rain World\RainWorld_Data\boot.config`

There's no documentation on the file, as it's not intended to be edited; however, here's a list of settings that might come in handy. 

```
Require value; require Debug build to work
"wait-for-managed-debugger" WaitForManagedDebugger
"wait-for-pix-timing-capture" WaitForPixTimingCapture
"player-connection-debug" AllowDebugging
"player-connection-multicast" AllowMulticasting
"player-connection-allow-pause" AllowPause
"player-connection-ip" ConnectIP
"player-connection-mode" ConnectionMode
"player-connection-name" ConnectionName
"player-connection-guid" EditorGUID
"player-connection-listen-address" ListenIp
"player-connection-project-name" ProjectName

Require no value
"headless"
"single-instance"
"nolog"
```