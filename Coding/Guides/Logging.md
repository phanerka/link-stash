Log locations are described [[Technical files#Logs|here]].

You can log variables on runtime if you [[Coding/Troubleshooting#DNSpy'ing|attach DNSpy]] to the game.

https://docs.bepinex.dev/articles/dev_guide/plugin_tutorial/3_logging.html


> `Debug.Log` is Unity's logger, which is not ready when `OnEnable` runs  
>   
> try using `Logger.LogDebug` instead, which goes to `Rain World\BepInEx\LogOutput.log`

(source: [RWMA](https://discord.com/channels/1083481230839922688/1083483097145819348/1334384577371705367))