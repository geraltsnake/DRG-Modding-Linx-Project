# DRG-Modding-Linx-Project
This Project is just a showcase of what I made for Deep Rock Galactic Modding(This is new project. So these old mods that I created are not included). 
![Image1](https://user-images.githubusercontent.com/14234445/144624818-277b7bb6-5c99-45e3-b1cc-428b174679c4.png)

## About The UE4 Project
Firstly It's free to use this project whatever you want. All of assets(that are inside Linx folders) that I included is made by me, and I won't include any lisenced asset. You don't need to ask a permission or crediting me when you use something from this project :)  
but the current project is not optimized and has poor readability. I will improve these eventually.  
**Currently this project only works in the single-player mode. It doesn't work in the multiplayer mode.**  

You can also download .pak from the release tab. And install to the mod folder.

The most of things can be tested in the project without launching DRG. But some stuffs that rely on DRG's assets can be seen such as SFX, VFX. If you want to try these thing in the project, see the input in the editor setting.
![Animation2](https://user-images.githubusercontent.com/14234445/144623014-a6b03f50-1d22-45f2-8244-8cdef5ee5fff.gif)

## About Initialization
The native spawning method is used. In /Content/_Linx_Initialization, there are blueprints for the initialization.  
  
- InitCave and InitSpacerig - Only spawns BP_Initialization.
- BP_Initialization - Do all needed initializations for other BP_managers.
	
## How to Control
- ADS   
	- Left Mouse Button(Do not assign any key to the LMB.)  
  
- Relates to Placeables  

	- Push to Talk - Place Light  
	- Reject Invite - Equipments  
	- Accept Invite - Sentry Mine  
	- Ignore Invite - Grenade, Turret  
	- 9 - Debug Tools(Currently these tools are very poor(Only I can understand what they do), so it shouldn't be used for now.)  
	- Mouse Wheel Up & Down - Change a placeable object(While holding a key such as Push to Talk)  
  
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
