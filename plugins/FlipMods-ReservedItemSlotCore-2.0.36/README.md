# ReservedItemSlotCore
### V62 Compatible!
**The core mod for all ReservedItemSlot mods.**<br><br>
This mod is required for my ReservedItemSlot mods to work, such as ReservedFlashlightSlot and ReservedWalkieSlot.<br>
These mods will give you free dedicated inventory slots for their respective item(s). These slots will be shown on the right side of your screen, stacking vertically.<br>

You cannot switch to these slots manually by scrolling. Instead, the method for swapping to these items is to hold Alt (default hotkey), and scrolling up and down to switch between them.<br>
This way, you can swap to these items to drop them, as well as other actions, such as charging, storing, etc.<br>

Grabbing reserved items, as well as switching between the main hotbar and reserved hotbar slots should sync between clients using this mod.<br>
If relevant, these mods will have dedicated keybinds to activate the items without needing to have them currently selected.<br>

<strong>All clients running this core mod will sync with the host, and have the same reserved item slots as them, regardless of which of the reserved item slot mods they have installed.</strong><br>
Using reserved item slots from the host for mods that you don't have should not cause issues, but you will not benefit from their extra mod features, such as specific hotkeys for reserved items, and you won't see these reserved items on players while they are not currently held.<br>
This may change, or be adjusted in the future, but it's currently in place to try and keep everyone's inventory the same size to help with syncing.<br>
This can also help with sending custom reserved item slots to other clients from the host if I do end up adding functionality to create them in the config, or if I end up creating a ReservedCustomItemSlot mod, which would be a server-side mod.<br>

**~Using this mod while the host does not have the mod has been re-allowed, but expect bugs and de-sync issues. Use with caution!~**<br>
**This mod will again, be disabled for non-host clients if the host does not have this mod for various reasons.**<br>
**For those stubborn enough, this can be force allowed in the config. You have been warned!**<br><br>


## Purchasing Reserved Item Slots (new in 2.0.0)
+ Reserved item slots can be purchased at the terminal. As of now, purchasing reserved item slots will unlock the slot for every player. There is no option currently to set it to be unlocked per individual.<br>
+ You can type "reserved" in the terminal to view tips on how to purchase reserved item slots.
+ For Reserved Item Slot mods that support this, prices can be adjusted in the config. All Reserved Item Slots that *I* made have these configs.
+ Purchased item slots will be saved to your game's save. Quitting and reloading a save *should* re-load all previously unlocked item slots. Unlocked slots will be reset upon starting a new game.
+ Purchasing item slots can be disabled in the config.<br><br>


## Configurable
+ **Each of the following configurations will need to be supported by each Reserved Item Slot mod.**
+ Adds support to allow Reserved Item Slot mods to adjust the **price** of their item slot in the config.
+ Adds support to allow Reserved Item Slot mods to adjust the **priority** of their item slot in the config.<br>
The higher the priority, the further down in order they will be on the right side of the screen.<br>
Negative priority will force the item slots to appear on the right side of the screen, unless this is disabled in the config.
+ Adds support for adding extra items to reserved slots in the config.
+ Adds support for removing existing items from reserved slots in the config.<br><br>


## Supports InputUtils
- Any relevant hotkeys for this mod can be managed in the in-game keybind menu.
- InputUtils is not a dependency, but is recommended!<br><br>


## API Support (examples below)
+ Adds API features for developers to use to easily create their own Reserved Item Slot mods, or to add their items to existing Reserved Item Slots.
+ When creating a ReservedItemData for a specific item, developers can optionally specify a target bone to holster the item to on the player (and Masked Enemy), as well as set the position/rotation offsets.<br><br>


## My ReservedItemSlot Mods
+ [ReservedFlashlightSlot](https://thunderstore.io/c/lethal-company/p/FlipMods/ReservedFlashlightSlot/)
+ [ReservedWalkieSlot](https://thunderstore.io/c/lethal-company/p/FlipMods/ReservedWalkieSlot/)
+ [ReservedWeaponSlot](https://thunderstore.io/c/lethal-company/p/FlipMods/ReservedWeaponSlot/)
+ [ReservedUtilitySlot](https://thunderstore.io/c/lethal-company/p/FlipMods/ReservedUtilitySlot/)
+ [ReservedSprayPaintSlot](https://thunderstore.io/c/lethal-company/p/FlipMods/ReservedSprayPaintSlot/)
+ More Reserved Item Slot mods may exist from others on Thunderstore!
<br><br>

## Mod Compatibility
+ HotbarPlus is compatible!
+ LethalThings Utility Belt is (or should be) compatible! (hopefully stays that way)
+ <strong>This mod may not play well with Advanced Company. Use at your own risk!</strong>
+ Other mods that can add hotbar slots are not guaranteed to work.
+ Other mods that might re-arrange the hotbar slots (HUD) are not guaranteed to play nicely with these mods, but *might* technically work.
<br><br>

## If you read this far and are enjoying my mods

Please consider supporting me [here](https://ko-fi.com/flipf17)!<br>
Definitely not required, but it would be greatly appreciated! =)<br>

<br><br>
## API Examples
#### First off, make sure you add the latest ReservedItemSlotCore.dll to your VS project's references.

#### NOTE
+ Adding items that do not exist (either by mistake or items from a mod that is not loaded) to a ReservedItemSlotData will not break anything.<br>
+ Adding an item to an existing ReservedItemSlotData, that was created from a mod that is not loaded, will not break anything.
<br><br>

### Adding your mod's items to an existing Reserved Item Slot

This will be used to add items from your mod to existing Reserved Item Slots that were created by another mod, and if ReservedItemSlotCore is enabled.<br>

**Create a class similar to this in a separate file.**
```csharp
using ReservedItemSlotCore.Data;

public static class ReservedItemSlotsCompat
{
    public static void AddItemsToReservedItemSlots()
    {
        // Name of your item as it appears in-game
        ReservedItemData myReservedItemData = new ReservedItemData("ItemDisplayName");
        
        // It's okay if the mod that created this item slot isn't enabled on the client. Nothing will break
        ReservedItemSlotData.TryAddItemDataToReservedItemSlot(myReservedItemData, "nameOfItemSlot");
    }
}
```
<br>

**OR to allow your item to be seen while holstered:**

<br>

```csharp
using ReservedItemSlotCore.Data;

public static class ReservedItemSlotsCompat
{
    public static void AddItemsToReservedItemSlots()
    {
        // Arguments: ItemDisplayName, ParentBone(enum), PositionOffset, RotationOffset
        ReservedItemData myReservedItemData = new ReservedItemData("ItemDisplayName", PlayerBone.Spine3, new Vector3(0.2f, 0.25f, 0), new Vector3(90, 0, 0));
    
        // It's okay if the mod that created this item slot isn't enabled on the client. Nothing will break
        ReservedItemSlotData.TryAddItemDataToReservedItemSlot(myReservedItemData, "nameOfItemSlot");
    }   
}
```
<br>

**And in your Awake (or Start) method in your Plugin class, add this: (preferably after you bind your configs)**<br>
**If your mod does not depend on ReservedItemSlotCore, and only optionally adds your items to Reserved Item Slots if they exist, then checking if this mod is enabled is very important!**
```csharp
if (BepInEx.Bootstrap.Chainloader.PluginInfos.ContainsKey("FlipMods.ReservedItemSlotCore"))
    ReservedItemSlotsCompat.AddItemsToReservedItemSlots(); // This will be the call to your function
```
<br>

**Last but not least, add this SoftDependency header above your Plugin class definition**<br>
If your mod *does* depend on ReservedItemSlotCore, then you can change `BepInDependency.DependencyFlags.SoftDependency` to `BepInDependency.DependencyFlags.HardDependency`.
```csharp
[BepInDependency("FlipMods.ReservedItemSlotCore", BepInDependency.DependencyFlags.SoftDependency)] // Add this line
[BepInPlugin("EXAMPLE_MOD_GUID", "EXAMPLE_MOD_NAME", "1.0.0")] // YOUR SHOULD ALREADY HAVE THIS LINE ABOVE YOUR PLUGIN CLASS DEFINITION.
public class Plugin : BaseUnityPlugin
{
    ...
}
```
<br>

### Creating your own ReservedItemSlot
**Example for creating your own ReservedItemSlotData, and adding your mod's items (or existing items in the game) to your item slot.**<br>
Include this code in the Awake (or Start) method of your Plugin class. You don't *need* to create a separate file or class when adding this code.
```csharp
using ReservedItemSlotCore.Data;

// MAKE SURE YOU PUT THIS HEADER ABOVE YOUR PLUGIN CLASS
[BepInDependency("FlipMods.ReservedItemSlotCore", BepInDependency.DependencyFlags.HardDependency)]
[BepInPlugin("EXAMPLE_MOD_GUID", "EXAMPLE_MOD_NAME", "1.0.0")] // YOUR SHOULD ALREADY HAVE THIS LINE ABOVE YOUR PLUGIN CLASS DEFINITION.
public class Plugin : BaseUnityPlugin
{
    private void Awake()
    {
        // Your existing code...

        // This will register your ReservedItemSlotData and will be added to the game if the host is running the mod
        // Arguments: ItemSlotName (format is not too important), ItemSlotPriority, ItemSlotPrice
        ReservedItemSlotData myReservedItemSlot = ReservedItemSlotData.CreateReservedItemSlotData("my_item_slot_name", 20, 100);

        // Create your ReservedItemData for your item
        // You can also add the extra arguments to allow this item to be shown on players while holstered. (refer to the previous example)
        ReservedItemData myReservedItemData = new ReservedItemData("ItemDisplayName");

        // Add the ReservedItemData to your ReservedItemSlotData and you're done!
        myReservedItemSlot.AddItemToReservedItemSlot(myReservedItemData);
    }
}
```
<br>

### More API Functions
These are a few examples on how you can get and manage players' held reserved items.
```csharp
PlayerControllerB localPlayerController = StartOfRound.Instance.localPlayerController;
for (int i = 0; i < SessionManager.numReservedItemSlotsUnlocked; i++)
{
    ReservedItemSlotData itemSlotData = SessionManager.GetUnlockedReservedItemSlot(i);
    if (itemSlotData != null)
    {
        // Gets the index of this item slot in the player's inventory
        int indexInPlayerInventory = itemSlotData.GetIndexInInventory(localPlayerController); // can pass in any player controller


        // Get the currently held object in this slot by the specified player, or returns null
        GrabbableObject heldObjectInSlot = itemSlotData.GetHeldObjectInSlot(localPlayerController); 


        // Gets the item slot frame (Image component in the HUD) for this item slot. Only applies for the local player
        Image itemSlotFrameHUD = itemSlotData.GetItemSlotFrameHUD();


        // For checking if the reserved item slot will accepts a specific item (the name of the item as it appears in-game)
        // You can also pass in a GrabbableObject reference
        if (itemSlotData.ContainsItem("Flashlight"))
            Plugin.Log("This slot contains a flashlight");
    }
}
```
<br>

If creating your own ReservedItemSlotData, be sure to also include this line in the dependencies list in your manifest.json file.<br>
`"FlipMods-ReservedItemSlotCore-2.0.7"`<br><br>

If you would like to view more examples, feel free to look at my existing ReservedItemSlot mods on my [github](https://github.com/cmooref17/ReservedItemSlotMods)!<br>
If you feel that I missed anything, or run into any issues, please let me know! I'm fairly active in the Lethal Company Modding discord, so come find me!<br>
You can also post any issues on the github for this mod, as well!<br>