# 2.0.6
+ Updated mod description for latest update compatibility.
# 2.0.5
+ You can now activate the walkie while in an item grabbing animation. This also allows you to use the walkie while looking at the monitor when using the touch screen mod.
# 2.0.4
+ Fixed an oopsie where the conditions for talking into the walkie were checked when you *released* the push to talk key, instead of pressing it.
# 2.0.3
+ Added more checks on when you can activate the walkie. You now can't use the walkie while typing, in the menu, etc. You can still use it in the terminal.
# 2.0.2
+ Added reminder in config descriptions about adding items, that translated items may need to be added to the list of additional items.
+ Changed default item slot priority to 150 (from 100). Flashlight priority has been raised to 200 (from 120). Priority order should remain be unchanged.
+ Added current items in slot to the README.
# 2.0.1
+ Fixed issue with not being able to activate the push-to-talk hotkey for the walkie when disabling purchasing slots.
# 2.0.0
+ Adds support for ReservedItemSlotCore 2.0.0 features.
+ Walkie slot can now be purchased!
+ Item slot price can be adjusted in the config.
+ Item slot priority can now be adjusted in the config.
+ Items can be added to this reserved item slot in the config. This can be handy when adding variations of this item, or when adding an item's translated name to the slot.
# 1.6.2
+ Fixed warnings when InputUtils is not enabled.
# 1.6.1
+ Fix for issue where dead masked enemies would constantly try to re-equip walkies.
+ Fix for issue where masked enemies wouldn't properly destroy their holstered reserved walkie after being destroyed.
# 1.6.0
+ Masked enemies will now display your holstered reserved items if they are mimicking you.
# 1.5.5
+ Changes to support ReservedItemSlotCore 1.8.9
+ Fixed issue with not being able to type correctly in terminal with walkie equipped, and pressing the talk hotkey.
+ Fixed issue with building placement/rotation being canceled when speaking into walkie.
# 1.5.4
+ Added support for InputUtils, as a soft dependency. If this mod is enabled, you will be able to access any relevant hotkeys within the game's keybind menu.
+ Undid the edited tooltip for the walkie controls.
# 1.5.3
+ Fixed a specific issue causing an error about index out of range.
# 1.5.2
+ Stability improvements when running this mod, but host does not. (Temporarily disabling the use of the walkie's push to talk hotkey (when holstered) if host is not running this mod. Will re-implement this again soon)
+ Updated dependency for ReservedItemSlotCore 1.7.4
# 1.5.1
+ Walkie now renders on shoulder in some cases where you can view yourself in third person.
# 1.5.0
+ Various tweaks.
+ Updated for ReservedItemSlotCore 1.6.0
# 1.4.6
+ Updated dependency.
# 1.4.5
+ Should be able to activate the walkie again with LMB when currently held.
# 1.4.4
+ Fixed some cases where the walkie mesh's active state was incorrect.<br>
I will re-add the mesh to the local player when I get a good position for it.
# 1.4.3
+ Finally tracked down and fixed the bug preventing players from using their hotkeys to swap hotbars, or activate their reserved items with [F] or [X]
# 1.4.2
+ Updated load order to ensure the core mod loads first.
# 1.4.1
+ Fixed not properly handling PlayerActions in the OnDisable method if they were not yet initialized.
# 1.4.0
+ The walkie now straps nicely to your chest when not in your hand.
+ Involved in a code restructure/organization and updated to support ReservedItemSlotCore 1.4.0
+ Refer to the ReservedItemSlotCore 1.4.0 patch notes for more.
# 1.2.2
+ Updated to support a few tweaks in the ReservedItemSlotCore mod.
+ Fixed some desync issues, and tweaked some other settings.
# 1.2.1
+ The activate walkie keybind shouldn't "try" to run on non-owned players anymore.
+ Fixed bug causing players to get stuck on terminal.
# 1.2.0
+ Updated dependency to support the updated Core plugin.
# 1.1.0
+ You can now change hotkey for talking in the walkie in the config.
+ Various tweaks to support the updated core mod.
# 1.0.1
+ Fixed a bug in the item controls tooltip where some text was duplicating.
# 1.0.0
+ Initial release