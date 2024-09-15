- 3.8.2
  - Removed code related to compatibility with LethalEscape. I will only be supporting the use of StarlancerEnemyEscape going forward.

- 3.8.1
  - Removed code related to WeedEnemies since Zeekers removed it in the latest beta.

- 3.8.0
  - Implemented fixes for spawning interior enemies on the Company moon.
    - Thanks 1A3!
  - The sandworm can now attack in interiors other than the vanilla Factory. Only tested in the vanilla Mansion, but the fix should be universal.

- 3.7.0
  - Enemy power level should now subtract from the correct spawnlist upon death.
	- Previously, a Thumper spawned that spawned outside would still subtract its power level from the interior spawn sytem after dying.
  - Using a pre-defined list, certain vanilla interior enemies now receive a generic threat component. In the future, this may be expanded to be more dynamic and affect modded enemies as well.
	- This should allow exterior enemies (such as Old Birds) to attack the ones that normally exist only inside the facility.

- 3.6.0
  - When finding the AI nodes in the level, AIFix now also caches their locations. This was done primarily for EnemyEscape, but it offers a non-zero performance boost for AIFix as well.

- 3.5.1
  - Removed the additional code implemented in 3.5.0 since Zeekers fixed the masked. It's further unnecessary now that I've released StarlancerEnemyEscape, which depends on StarlancerAIFix.

- 3.5.0
  - Implemented the same code that runs on EnemyAI.Start() in EnemyAI.DoAIInterval. This should fix the issue with Masked being unable to hurt employees after teleporting, as well as ensure that if any future mod allows an enemy to travel in and out of the facility that their AI will automatically switch.

- 3.4.0
  - Improved accuracy and optimization.

- 3.3.0
  - Fixed prefab Spore Lizards being a little silly with their initial behavior.
    - Previously they would navigate to (0,0,0) and stand there until otherwise interacted with.

- 3.2.0
  - Optimized the NRE patch. It now only runs the null removal if a null reference is found, which also means it doesn't spam the log.
  - Fixed an issue where jesters would get stuck in place if they entered the attack behavior outside and then lost their targets.

- 3.1.0
  - Accidentally broke the plugin in v3.0.0, this is now fixed.

- 3.0.0
  - Added a patch for dealing with null reference exceptions regarding MeshRenderers and SkinnedMeshRenderers in EnableEnemyMesh().
  - Fixed the issue where jesters would get stuck in their cranking animation after attacking (or attempting to attack) outside.
  - Added compatibility with Lethal Escape.
    - Automatically disables LEsc's JesterAI.Update() Postfix in favor of SLAI.
	- This addresses the issue where jesters would be immediately hostile and stuck in the incorrect animation state upon spawning outside.
  - Added future compatibility for Seamless Dungeon.
  - Refined SpringManAnimPatch.
  - Further code optimizations.
  
- 2.0.0
  - Added SandwormResetPatch
    - Previous behavior: After attacking, sandworm would appear just below the surface and break its AI.
	- New behavior: Interior sandworms now relocate to a random inside node after they attack, thus preserving their AI.
  - Added SpringManAnimPatch
    - Previous behavior: Upon losing all targets (such as its target player entering the ship and there being no other targets available to it), a springman would begin sliding around without animating a walk cycle.
	- New behavior: Upon losing all targets, a springman will now correctly resume its walking animation.

- 1.2.0
  - Added JesterAIPatch, which fixes the jester enemy being unable to attack while outside.
    - Previous behavior: Jester would wind up, pop out, then immediately return to box.
    - New behavior: Jester winds up, pops out, then massacres anyone unfortunate enough to be outside.

- 1.1.1
  - Actually put the updated plugin in this time hahahahaaaaaaaaaa

- 1.1.0
  - Performance and accuracy optimization. (Big thanks to **RoboticPrism** and **IAmBatby** for helping to optimize the code! :3 )
    - Removed the "magic numbers" the initial release relied upon.

- 1.0.0  
  - Initial Release.