# ForgeLinks
Links for commonly asked questions related to Forge Networking Remastered.

Use the Github: https://github.com/BeardedManStudios/ForgeNetworkingRemastered.

Get the **newest** nightly edition of Forge Networking Remastered: [DOWNLOAD](https://fnr.rumstein.eu/).


For setup and basic RPC or Field tutorials, use the [DOCUMENTATION](http://docs.forgepowered.com/GettingStarted/getting-started/).


For community support, join the [DISCORD](https://discord.gg/yzZwEYm) channel, this wouldn't be possible without you!


- Learning Forge
  - [Videos](#videos)
  - [Tips](#tips)
  - [Fields](#fields)
  - [RPCs](#rpcs)
- Miscellaneous
  - [Demo Projects](#demo-projects)
  - [Server Options](#server-options)
  - [Binary Messages](#binary-messages)


## Videos
* [Bearded Man Studios Video Tutorials](https://www.youtube.com/playlist?list=PLm1w78-UUlMIi5Vfwy6ckJQIQMHMT-QS5) - Brent produced a collection of introductory video tutorials to learn Forge Networking Remastered.
* [NAT Hole Punching Video Tutorial](http://docs.forgepowered.com/nat-hole-punching/) - A video tutorial on NAT Hole Punching from Bearded Man Studios. 


## Tips
* **Click these to expand the answer.**

* <details>
    <summary>I'm getting a null reference exception?</summary>
   Typically it would be 1 of 3 issues. 1 - You forgot to turn on Run in Background, 2 - you tried pressing the play button in the scene and not loading the Multiplayer Menu scene first (IE: by double clicking it on Windows), 3 - you're not setting up the multiplayer menu scene as index 0 and the demo scene as index 1.
</details>

* <details>
    <summary>My Objects aren't showing up on the Client/Server!</summary>
    If you're not changing scenes after connecting try calling NetworkObject.Flush(networker) on both the server and the client. - mcguinessdr
</details>

* <details>
    <summary>Help! The Network Contract Wizard (NCW) shows blank?! </summary>
    The NCW checks for all files in the generated folder and fills the NCW with what it reads, however, it will not show ANY network objects if your project can't compile. Usually your project can't compile because you added some RPCs without implementing them. It is reqruired to implement the RPCs as they are abstracted methods. Your NCW will also give an error if you have it open while your project can compile, however simply reopen it to make your network objects appear again. Note: If you moved files into the generated folder it will appear empty as well. Generated folder is only meant for generated files by the NCW - NFMynster
</details>

* <details>
    <summary>Hmm, I get this error KeyNotFoundException: The given key was not present in the dictionary. whenever I call an RPC?</summary>
    If you get that error, it's likely because you are calling an RPC on the wrong network object. You are technically allowed to call an RPC with whatever byte id there is, but ensure the RPC and the byte id is on the right network object & behavior. - NFMynster
</details>

## Fields

* [Field Documentation Tutorial](http://docs.forgepowered.com/GettingStarted/basic-moving-cube-example/) - Basic field tutorial on moving a cube object.
* [Instantiation Documentation Tutorial](http://docs.forgepowered.com/GettingStarted/basic-instantiation-example/) - A tutorial on instantiating an object into a scene that includes the use of fields. 

## RPCs

* [RPC Documentation Tutorial](http://docs.forgepowered.com/GettingStarted/basic-rpc-example/) - Basic RPC tutorial including the use of arguments. 
* [Advanced Documentation Tutorial](http://docs.forgepowered.com/GettingStarted/jump-start-guide/) - A more in depth tutorial that also includes the use of RPCs.

## Demo Projects

* [NFMynster's Semi-Authoritative FPS Example](https://github.com/NFMynster/ArenaGame) - In depth example of a 3D FPS, including an animation sync and server authoritative shooting. 
* [Relic's Authoritative Movement Example](https://github.com/Relic/AuthoritativeMovementExample) - A 2D demo of Server authoritative motion control by Relic.
* [New Guy's Authoritative Movement Example](https://github.com/g-klein/ForgeAuthoritativeMovementDemo) - A 2D demo of Server authoritative motion control by New Guy.

## Server Options

* [Headless Linux Documentation Tutorial](https://developers.forgepowered.com/Tutorials/SelfAndCloudHosting/Headless-Linux-Server) - Video tutorial on using a Headless Linux server.
* [Web Server Documentation Tutorial](http://docs.forgepowered.com/WebServer/jumpstart/) - Tutorial on using a web server.
* [Master Server & NAT Punch on Digital Ocean](https://github.com/BeardedManStudios/ForgeNetworkingRemastered/wiki/Starting-up-MasterServer-and-NatPunch-on-DigitalOcean-droplet) - Tutorial from the Forge Networking Remastered Wiki. 


## Binary Messages

* [Sending A Binary Frame](https://github.com/BeardedManStudios/ForgeNetworkingRemastered/wiki/Creating%2C-sending-and-receiving-binary-messages) - Tutorial from the Forge Networking Remastered Wiki. 


