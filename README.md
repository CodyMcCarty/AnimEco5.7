# Animation Ecosystem for Game Development - Unreal Engine Game
> Following [Animation Ecosystem for Game Development](https://dev.epicgames.com/community/learning/courses/2Lz/unreal-engine-animation-ecosystem-for-game-development/yp13/unreal-engine-animation-ecosystem-for-game-development-overview). with some changes because it's out of date

# Project Features
Great Examples of making small changes to animations in engine. The assets are not reuseable. The Rifle Jump is subpar. The holster is to specific. 
- The project was a bit out of date so I made some changes.  I started with a blank 5.7 project. I added the third person content from a 5.3 project. I added the weapon and a few misc things from the course project. 
- Doesn't cover additive, child animBP, layers, choosers, anim notify states (but does use regular anim notify).
- Broke up a full jump anim into jump start, fall loop, and jump land in L7 using control rig.
- Edits an animation using control rig.  L15, the holster and present weapon montage doesn't line up where the weapon should be holstered, but does after the edit.
- The rifle jump anims are WIP. Look for rifle jump anims from elsewhere. These need some work. The land needs to be additive, I couldn't getting it working as additive properly in a timely manner.  The Rifle fall loop is janky and looks best as a single frame. 
- In the animBP, State Aliases, special anim node, are used to split up locomotion states from jumping & falling states. This is again used for crouching.
- Adding Sockets vs Virtual Bones is covered in Ls10 Attaching a weapon using sockets. VBs can be used in animBP. Socket transform can't be modified during runtime(can modify the object's). He mentions not needing to animate the weapon.
- Montage Slots overview at L12. Goes over full body vs upper body. Can Have a montage with both full and upper and choose in animBP. 
- Has unscalable decisions to animate with crouch, rifle, unarmed. It's already painful, Adding more would be exhausting. Lots of blend by bool nodes.
- The anims need some polish. The anims from the animation starter pack get converted to Manny from UE4_Skele.  They look ok, but need some work. eg his hands are not on the pistol in the pistol anim. 
- I would prefer different anims. The pistol anims are in weaver stance. The Idle is hip fire instead of low ready. Could be useful for a skilled vs unskilled trigger puller.
- Reacts to anim notify in animBP. Not strange inherently, but the animBP logic calls functions on the character, seems reverse of how I see their relationship.
- He made his own IsCrouched and dealt with the state management. There is MoveComp::IsCrouching() and Character.IsCrouched
- Used ChildActorComp instead of Actor Comp or Actor. There are issues with "child actor comp" not to be confused with and actor comp that is a child of something. Not sure how else to word that.



<br>

# MY_SYSTEM_1

MY_SYSTEM_DESCRIPTION

# Performance & Optimization
## MY_PERF&OPT_1

# Credits

**Game Assets:** Licensed for use with the Unreal Engine only. Without a custom license you cannot use to create sequels, remasters, or otherwise emulate the original game or use the original game’s trademarks, character names, or other IP to advertise or name your game. (Unreal Engine EULA applies)
