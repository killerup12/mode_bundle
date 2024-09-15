# 2.0.36
+ Fixed a typo in the code that caused the mod to sometimes fail to detect when the inventory size changes mid-game. This is in place to prevent errors when other mods add inventory slots mid-game.
# 2.0.35
+ Fixed issue with controller not working properly on recent versions of ReservedItemSlotCore, when InputUtils is *not* enabled.
# 2.0.34
+ Updated mod description for latest update compatibility.
# 2.0.33
+ Removed config option for toggling the reserved hotbar slots.
+ Added another keybind for toggling the reserved hotbar slots that will work along side the press (and hold) to focus. Default key: Right alt<br>
The keybind can be changed in the keybind settings in the menu, if the InputUtils mod is enabled.
# 2.0.32
+ Thanks JillCrungus for pointing out and help fixing the issues in the BoneMap that was incorrectly mapping a few bones, making it impossible to anchor reserved items to those bones.
# 2.0.31
+ Added checks to prevent potential errors (likely because of slight mod conflicts?) in some rare cases when trying to display reserved items on Masked Enemies.
# 2.0.30
+ Added config option to enable/disable verbose logs.
+ If verbose logs are enabled, the mod will log when it blocks the user from swapping items to help determine if issues related to not being able to swap items are caused by this mod or not.<br>
This will not spam more than once per second.
# 2.0.29
+ Fixed issue when joining a player when you have the ForceEnableThisModIfNotEnabledOnHost config set to true, and then when leaving and hosting a new game, the reserved slots don't appear.<br>
The mod was accidentally clearing the local list of reserved items data because of a wrong variable assignment.
+ The ForceEnableThisModIfNotEnabledOnHost config option should now work correctly if enabled, and if the host doesn't have the mod. **Remember, this is NOT stable and WILL cause de-sync, and please, don't enable this in lobbies with players you don't know.**
# 2.0.28
+ Fixed a few UI scaling inconsistencies when paired with HotbarPlus.
+ Should scale properly in size with custom HotbarPlus item slot sizes.
+ Reserved item slots will no longer match HotbarPlus's item slot spacing (UI). The spacing now scales with its own size so it won't overlap with other reserved item slots.
# 2.0.27
+ Rewrote the logic for syncing already held reserved items between clients. This does fix non gamebreaking issues, but might also fix bigger issues with some players.
+ "Destroying" reserved items in inventory, and also when dying, will now update the reserved item slots UI, which will hide empty reserved item slots if this is enabled in the config.
# 2.0.26
+ Updating the hide empty reserved item slots while in game will now apply and update the UI immediately.
# 2.0.25
+ Prevents potential errors that may arise from save corruption. This will not fix the corruption, but *may* help users find the issue.
# 2.0.24
+ Fixed the bug that I created in 2.0.23 (I think) where dropping a reserved item while you have another reserved item would bug out the first item, and you couldn't see it, but other players could.
+ Reloading a shotgun shell will now trigger the reserved item slots in the HUD to reload. This means that if the config is set to hide empty reserved item slots, the shotgun shell slot will automatically hide after reloading.
# 2.0.23
+ Item slot frames should now animate correctly again while maintaining compat with mods that set the item frame's override sprite. This is what broke the animation.
+ Placing reserved items in a storage container should now correctly trigger on discard effects, such as automatic swapping to another slot, or hiding the reserved item slot if the option is enabled in the config.
# 2.0.22
+ Fixed issue with furniture/unlockables not syncing with clients when a client joins while another player is holding a reserved item.
+ Added extra checks to ensure that copied item slots in the HUD copy the texture and material as well, in case they do not.<br>
This should resolve some issues with mods who have custom textures for the item slot frames.
# 2.0.21
+ Accidentally logged some false errors.
# 2.0.20
+ Minor update to TooManyEmotes compat.
+ Fixed a possible error caused when saving/loading unlocked slots.
+ Fixed error caused when checking if an item is in a reserved item slot, but a known bug is causing the start/end reserved item slot indexes to go outside the bounds of the player's item slots.
# 2.0.19
+ Prevents the errors when te game tries to swap the player back to an invalid index after picking up a reserved item.<br>
The cause of this issue is still unknown, but this fix should work as a band-aid.
# 2.0.18
+ Potential fixes for issues where the mod tries to swap the player to a negative hotbar slot. (hopefully)
# 2.0.17
+ Fixed errors caused when the game tried to sync already held reserved items before the client fully synced with the host.
# 2.0.16
+ Added config entries to allow/disable any HUD formatting from HotbarPlus from being applied to the reserved item slots.
+ Added a config entry to disable the energy bar from HotbarPlus from being displayed in the reserved item slots.
+ The above config settings will do nothing if HotbarPlus is not enabled.
+ Any changes to the above config settings while in-game (via another mod that lets you modify them) will be applied automatically upon closing the quick menu. (*should*)
# 2.0.15
+ Fixed some cases where dropping, or storing an item from a reserved item slot, would not hide the reserved item slot. (if the option to hide empty reserved item slots is enabled in the config)
+ Fixed a potential issue when grabbing a reserved item, where it would throw grab invalidated errors for the local player.
+ Added various null checks to prevent various unexpected errors.
+ Added more logs for debugging.
# 2.0.14
+ Fixed issue when purchasing reserved item slots is enabled, where item slots with a price of 0 were not automatically unlocking upon ship resets.
+ Fixed issue with various reserved item meshes displaying a blue sphere (map node). This should be fixed for good now. (hopefully)
+ Fixed some cases where reserved items may appear invisible for players. May not have fixed *all* issues, but if this is still happening, I would appareciate it if you could post the issue on the mod's github!
+ Added a config option to hide empty reserved item slots. If enabling this config option creates issues, please call the police immediately. Also, I would greatly appreciate it if you could post the issue on the mod's github. Thank you!
+ Fixed some cases when picking up reserved items, where the grabbing animation sometimes appear to happen twice.
# 2.0.13
+ Items can now be grabbed no matter which hotbar you're on.<br>
If you're already in the reserved hotbar, you will swap to the slot that you picked up the item in instead of keeping your current slot unchanged.
+ Grabbing an item while toggled in the reserved item slots should not cause the items to show up as invisible anymore.
+ Dropping a reserved item should automatically swap to the next reserved item slot, unless no more are held.
+ The focus hotbar tooltip can now be hidden in the config.
+ Added more api functions, and organized the existing api code a little more.
+ Removed terminal tips from this mod if purchasing slots is disabled by host.
+ Reserved hotbar slots (HUD) shouldn't fade anymore while you're currently in the reserved hotbar.
+ Will add the config option *soon* for swapping between hotbars with scrolling. This will disable swapping with a hotkey.
# 2.0.12
+ Removed wrong changelog entry.
# 2.0.11
+ You can now swap between hotbar slots while emoting, except when emoting with TooManyEmotes, unless the config in TooManyEmotes allows moving while emoting.
+ Added config options to disable displaying holstered reserved items on players, and a config option to disable this for masked enemies as well.
# 2.0.10
+ Added methods for mapping items to their original name.<br>
This should fix issues with items not going to their reserved item slot when players running localization mods.
# 2.0.9
+ Fixed issue with reserved item slots with prices set to 0 not automatically unlocking upon starting/loading a game.
+ Possible item duplication fix.
# 2.0.8
+ Fixed issue where some reserved items would appear invisible in your hand. This usually happened with the Stun grenade and Improvised flashbang.
+ Fixed issue with terminal scrolling being inverted when entering it while your reserved slots are focused.
+ Masked enemies should correctly have any holstered flashlight enabled. (*should*)
# 2.0.7
+ Cleaned up some API functions.
+ As always, to reference the latest API features, reference the latest ReservedItemSlotCore.dll
+ If your mod depends on this mod, I also recommend updating the dependency string in your manifest.json file to require the latest version of this mod.
+ Added more useful API functions in the ReservedItemSlotCore.SessionManager class.
+ Added some more API examples in the README.
+ Added config options for adding custom item slots.<br>Setting the number of custom reserved item slots in the config, and then launching the game will generate new configs for each custom reserved item slot for you to fill out.
# 2.0.6
+ Fixed potential issue with other mods that might add item slots. This fixes the issues with HotbarPlus.
+ Found and fixed another issue causing de-sync.
+ Fixed an issue in some scenarios where the item mesh of a holstered item was being disabled.
+ Fixed the issue where holstered reserved item slots would not immediately appear on players upon joining a game. (and they had them equipped already)
+ Thanks for all the tips and reporting these issues!
# 2.0.5
+ Fixed most of the new de-sync issues introduced in 2.0.x
+ Fixed the main cause of duplicate items appearing in your hand.
+ You now have access to the reserved item slots in the pre-game lobby.
+ Items in reserved slots *should* sync with clients joining the session for the first time. This should work in the pre-lobby, or mid-game, if using mods that allows this.<br>
Note: When joining a session, reserved items may be invisible at first when they should appear on the player holstered. This is fine, but will be fixed.
+ Fixed some cases where item slots, unlocked item slots, and some UI were not resetting upon new games when purchasing item slots is enabled.
+ There may be a few more (hopefully only minor) bugs, but if you could please report them on the github, I would greatly appreciate it!<br>
Also note: I did not test EVERY aspect for bugs except for the ones immediately known to me, so I am not claiming that they are all fixed. Hopefully most of them.
# 2.0.4
+ Fixed issue with terminal always showing that purchasing slots is disabled in some cases.
+ Potential fix for other random issues. (sorry this is vague)
+ Checking if a reserved slot is unlocked is more accurate and fixes a few issues.
+ Still a lot more issues that I'm currently trying to consistently reproduce. Fixes will come soon!
+ Fixed issue with purchased item slots not disappearing upon starting new games.
+ If you have issues or bugs to share, I would appreciate if you could post an issue on the github, and let me know if you guys enabled purchasing slots in the config, who it affected, or was it everyone? Did it affect both host and clients? Can you reproduce it?<br>
Any of that information would be extremely helpful, and thanks!
# 2.0.3
+ Fixed terminal preventing the TooManyEmotes store from appearing.
+ Fixed some internal issues that was causing this mod to incorrectly identify an item in a reserved item slot.<br>
This is partially related to not being able to activate the flashlight with [F], or walkie with [X].
+ Disabled purchasing slots by default.
+ Terminal will now display under the Reserved Tip if the host disabled purchasing slots.
+ More fixes coming soon!
# 2.0.2
+ Fixed issue with non-host clients not unlocking slots when host disabled purchasing them.
+ Added pre-game reminder that reserved item slots won't be available until the round has started.
# 2.0.1
+ Quick fix for the terminal not showing tips related to this mod, or how to buy reserved item slots.
# 2.0.0
+ Re-did most (if not all) of the codebase revolving around reserved slots data, and how it is handled to support new features and API functionality.<br>
This update may break other mods' references to this one, and if so, I do apologize!
+ For more info regarding this update, please read the README.
+ Added progression. You can now purchase reserved item slots in the terminal! (can be disabled in the config)
+ Added API functions to offically allow mod developers to create their own reserved item slots, and add their items (any item) to it.<br>
The added API features also allows mod developers to easily add items from their mod (or even items from another mod) to existing reserved item slots, if this mod is enabled.
+ Even more configurable! The following config options can only be used if implemented by developers of reserved item slot mods.
+ Reserved item slot priorities can be can now be changed from their default values in the config.<br>
Changing priorities will change the order of the reserved item slots on the right (and left) side of your screen. The higher the priority, the further down in order they will be.
+ Adds support for adding extra items to reserved slots in the config.
+ Adds support for removing existing items from reserved slots in the config.
+ The ReservedItemSlotCore mod now handles all of the displaying of holstered reserved items. (Optional) When creating reserved items, or adding items to existing reserved item slots, mod developers can easily specify a bone to anchor a reserved item to when holstered, as well as a position/rotation offset.<br>
Read the README for more information on this.
+ The ReservedItemSlotCore mod now handles displaying reserved items on Masked Enemies, as long as developers define how their item will be displayed while holstered.
+ Added functionality to swap and toggle specific reserved item slots. Example: ReservedWeaponSlot has a keybind to toggle the reserved weapon slot. When pressed, that reserved slot will be toggled until you scroll off of it, without needing to hold Alt.<br>
This will need to be implemented by developers who create their own reserved item slot mods.
+ I probably broke a few things, or introduced new bugs with this update, so please post any major issues on my github. Thank you!
# 1.8.17
+ Fixed warnings when InputUtils is not enabled.
# 1.8.16
+ Re-restricted the use of this mod for non-host clients if the host does not have it enabled. This still CAN, and likely WILL cause desync issues if used this way, but for those who are stubborn enough, you can force allow this in the config. You have been warned!
# 1.8.15
+ Keybind display names should now display the correct keybind, whether on keyboard or controller.
+ All relevant keybind display names for this mod should automatically switch between keyboard and controller accordingly.
+ Added more controller support, with and without InputUtils. Works best with InputUtils installed, and easier to configure the controls.
# 1.8.14
+ Gave internal access to the ReservedKeySlot mod by: nitsuD
# 1.8.13
+ Revised a few methods to help prevent the error spam with players sending negative hotbar slot changes to the server.
+ Added more logs to help debug current or future errors.
+ Removed a block of code that could have been miscalculating the new reserved item slots start index when inventory size changes. (for other players)
+ As always, if this version seems unstable, please revert back to 1.8.12 until this has been updated.
# 1.8.12
+ Disabled adjusting inventory HUD elements in AdvancedCompany is enabled. (temporary maybe)
+ Small tweaks to code.
# 1.8.11
+ Added more reliable checks for the local player when the inventory size changes, for calculating which item slot index is the start of the reserved item slots. Should fix <i>some</i> issues.<br>
+ When using this mod with AdvanceCompany, (and it decides to behave itself) the reserved slots shouldn't use the feet slots from that mod.
+ If this mod creates errors with AdvancedCompany, it might be best to run without this mod (or AC) until the issue is fixed.
# 1.8.10
+ Minor changes.
# 1.8.9
+ Fixed some issues throwing errors in the console.
+ Fixed item appearing quickly and then disappearing from your hand when you pick up a reserved item.
+ Fixed control tips flickering to grabbed reserved item controls, and then back to the previous controls.
+ Maybe fixed more cases where you can't scroll in the reserved slots?
+ Added more code to support features for the reserved item slot mods.
# 1.8.8
+ Added more checks, and prevented some more issues if host does not have mod. (Again, use with caution!)
# 1.8.7
+ Fixed bug with controllers not being able to scroll through reserved hotbar slots with d-pad. (or another keybind)
+ Added some compatibility checks.
+ Reallowed use of reserved slot mods even if host doesn't have them. Use with caution!
+ Automatically changes any relevant control tooltips if player is using a controller or not.
# 1.8.6
+ Some compat tweaks.
+ Focus reserved hotbar tooltip now changes when keybind is updated in game. (with InputUtils)
# 1.8.5
+ Fixed the bug preventing you from swapping hotbars that I created in 1.8.4 (sorry!)
# 1.8.4
+ Removed old code that had methods being called before they were instantiated. Hopefully fixes some errors people are getting.
# 1.8.3
+ Fixed typo in bug.
+ Forgot to re-edit a line of code I changed that prevented the server from getting hotbar swap updates from the clients.
# 1.8.2
+ Fixed some bugs.
+ Added support for InputUtils, as a soft dependency. If this mod is enabled, you will be able to access any relevant hotkeys within the game's keybind menu. (will do the same for the individual reserved mods soon)
+ Added to the compatibility logic for other mods that increase inventory size. (may need more testing)
+ The reserved hotbar scroll direction should now match the mouse, regardless of inverted scroll settings.
+ (Readded) Swapping between reserved hotbar slots will now skip empty slots.
+ Attempted to refix compat with AdvancedCompany. May or may not work? No promises!
# 1.8.1
+ Added debug logs and dumps when errors occur when certain functions are called with incorrect values. Hopefully people share these with me on the Lethal Company Modding Discord!
# 1.8.0
+ Support for v47.
+ Slight code structure revamp.
+ Add compatibility between other mods that may change players' inventory size dynamically, such as LethalThings' utility belt. Not guaranteed for all mods.
+ Maybe added some bugs, idk.
# 1.7.7
+ Potential fix for the infamous de-sync issue.
# 1.7.6
+ Gave internal assembly access to LuckE's ReservedPersonalBoomboxSlot mod.
# 1.7.5
+ Tweaked more methods that could possibly cause de-sync.
# 1.7.4
+ More stability improvements and fixed more cases of potential de-sync issues. Probably still more to go, but should be at least a little more stable.
# 1.7.3
+ Added config entry to enable toggling swapping between the main hotbar slots and the reserved ones, rather than swapping while holding the hotkey.
+ Fixed quick bug with some reserved items being "registered" to the same reserved slot index amongst all clients. This will prevent some de-sync issues.
+ Reduced how often you can swap between the main and reserved hotbar slots. This will help with latency.
+ Will re-fix hotbar scroll direction in the reserved hotbar slots (up/down) to match scroll direction when I can ensure that it will sync with all clients, regardless of inverted values.
# 1.7.2
+ Fixed issue with clients not swapping their currently held reserved item correctly.
+ Restructured a part of this mod. Regardless of which of the reserved item slots that non-host clients have, they will now have all of the reserved item slots that the host is using, even if they don't have that specific mod installed.<br>
Syncing reserved slots from the host for a mod that you don't have should not cause any issues. You just won't have the extra features, such as any specific hotkeys for those mods, or items being displayed on players' while not currently held.<br>
This new adjusted framework can allow for custom reserved slots from the host to be synced with other clients, if I do end up making a CustomReservedItemSlot mod.
# 1.7.1
+ Fixed some compatibility issues in some cases with other mods not being able to run their transpiled code.
+ Scrolling up will now always scroll up in the reserved item slots.
+ Made swapping between reserved hotbar slots smarter. It will now not let you swap to empty inventory slots when focused on the reserved hotbar slots.<br>
There still may be syncing issues between which reserved item is held between players. Will update this next.
# 1.7.0
+ Added more tools for ReservedItemSlot mods.
+ Adds support for ReservedWeaponSlot!
# 1.6.7
+ Added support for ReservedSprayPaintSlot and the upcoming ReservedWeaponSlot mods.
# 1.6.6
+ My mod and LethalThings mutally broke compat with each other temporarily. Fixed now.<br>
My mod should now dynamically update the start index for the reserved slots in case other mods do change the order.
# 1.6.5
+ Temporary fix for reserved hud slots starting at index 4 regardless of hotbar size, when first joining a server.
# 1.6.4
+ Added support for other mods that might increase hotbar slots, such as LethalThings Utility Belt.<br>
# 1.6.2
+ Minor internal code tweaks.
# 1.6.1
+ Gave internal assembly access to LuckE's ReservedBoomboxSlot mod.
# 1.6.0
+ Revised structure of this mod.
# 1.5.2
+ Fixed issue with HUD not updating properly on custom inventory sizes. May not play well with other mods, aside from HotbarPlus that change inventory sizes.
# 1.5.1
+ Fixed invisible item issue when charging a reserved item.
# 1.5.0
+ Internal changes to support expanding inventory UI to keep the reserved item slots separate.
+ Should now support inventories that dynamically change in size. Adding inventory slots will copy the reserved item slots to the new last slots of the inventory, if needed.
# 1.4.4
+ Minor fixes.
# 1.4.3
+ Fixed (again?) being able to switch to your reserved hotbar while holding a two-handed item.
+ Improved logic for swapping between hotbars, or preventing you, while in certain animations or events.
+ Removed old debug logs.
# 1.4.2
+ Finally tracked down and fixed the bug preventing players from using their hotkeys to swap hotbars, or activate their reserved items with [F] or [X]
# 1.4.1
+ Fixed not properly handling PlayerActions in the OnDisable method if they were not yet initialized.
# 1.4.0
+ Major code restructure/organization to optimize network syncing and stability.<br>
Along with the restructure, more bugs and issues may be introduced, but these will be addressed asap!<br>
+ Reverted some functions to rely on built-in code to reduce the likelyhood of desyncs caused by these mods.<br>
This will help with future syncing with clients not uses these mods, but will likely not play nice with them at this point.
+ Other various fixes.
# 1.2.9
+ Fixed issue with being able to grab reserved items off of other players (caused de-sync)
# 1.2.8
+ Fixed issue where non-reserved items were going into the reserved item slots when the rest of the inventory is full.
+ Fixed a cursor tooltip issue showing that your inventory is full when looking at a ReservedItem, but you still have an available slot for it.
# 1.2.7
+ Fixed a few desync issues and tweaked some of the network transport settings.
+ Optimized some areas of code.
# 1.2.6
+ Fixed syncing issue with clients that occurs when clients leave and rejoin.
# 1.2.5
+ Swapping hotbar states should now be synced with all clients using this mod.<br>This means that the item held in each player's hand should be the same for everyone else.
# 1.2.4
+ Hopefully fixed all of the issues with grabbing and dropping reserved items, and a few other issues.
+ There are a few minor issues I ran into that I will fix soon.
# 1.2.2
+ Fixed issue with non-host clients not correctly picking up the ReservedItemSlot items.
# 1.2.1
+ Revamped functionality.
+ You can no longer swap to the reserved item hotbar slots, even if they're filled.
+ You can now swap to the reserved item hotbar slots by holding Alt, and scrolling up and down to switch between them.<br>
This way, you can swap to these items to drop them, as well as other actions, such as charging, storing, etc.<br>
The reserved item slots are still on the right side of the screen.
+ Added configs so you can change the swap hotbar modifier.
# 1.1.0
+ Reserved item slots now won't fade with the main hotbar.
# 1.0.0
+ Initial release