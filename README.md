# DRG-Modding-Linx-Project
Linx Project is just a showcase of what I made for DRG modding(This is new project. So these old mods that I created are not included). 

## About Linx Project
Firstly It's free to use this project whatever you want but the current project is not optimized and has poor readability. I improve these eventually.
This mod is like a personal mod so this project only works in the single-player mode. It doesn't work in the multiplayer mode.

When the project get stable, I might upload this to mod.io but for now I upload .pak here only. 
This project doesn't contain any licenced product(All assets I include is made by me), so it's free to use.

## Current Implemented Features(But WIP)
- Placeable Objects
- Jumppad
- Movable Platform
- Sentry Gun
- Controllable Turret
-  
-
-

## How to Control
ADS - Left Mouse Button(Do not assign any key to the LMB.)

Placeable
  Push to Talk - Place Light
  Reject Invite - Equipments
  Accept Invite - Sentry Mine
  Ignore Invite - Grenade, Turret
  
  Mouse Wheel Up & Down - Change a placeable object(While holding a key such as Push to Talk)
  
  ADS Manager(Only Work in DRG)
	The player's camera is attached to WPN actor's SK mesh directly when ADS, so it has weird camera movement sometimes. And also some weapon's reload animation cause very bad camera position.

	Activation - Automatically activated in the cave. Press RMB to ADS(Support tools are not supported yet). 

Placeable Manager
	This manager control how the player place an object.

_BP_Placeable_Template
	All placeables are based on this BP.

BP_Activator
	When the player is near this device, it allows the player to control something. But for now, it's only usable for the mountable turret.

	Activation - Press F to control when the player is near this device.

Mountable Turret
	BP_Activator is needed to control.

	Activation - Move mouse to aim, RMB to zoom(Toggle), LMB to fire, F to dismount.	

Jumppad
	Activation - When the player is on a jumppad. it automatically launches the player.

	Difference between BPs
		BP_Jumppad - An obvious jumppad. It launches the player.
		BP_Jumppad_High - High velocity version of the jumppad.
		BP_Jumppad_AntiFall - It only activates when the player is falling.

MovablePlatform
	When the player is on this platform, it allows the player to control. 

	Activation - Mouse wheel up & down to move upward and downward. MMB to stop.

	Difference between BPs
		BP_MovingPlatform_Base - Normal version.
		BP_MovingPlatform_Fast - Fast version.
Decoy
	After placing, It attracts enemies and when many enemies are around a decoy, it spawns something. For the decoy effect, I just spawns the DRG's character to the root location, so bugs target the character.

	Activation -  No control.

Explosives
	Altanate placeable explosives.

	Activation - By timer.

	Difference between BPs
		BP_DischargeBomb - Produce EMP discharge.
		BP_MiningExplosive - Explosive with carve.

Sentry
	It's just an obvious sentry gun. Currently the targeting system is not smart.

	Activation - No control.

Mine dispensor
	Produce mine 
