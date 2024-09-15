# FastSwitchPlayerViewInRadarMOD

## Overview
The FastSwitchPlayerCamInRadar mod let's you switch each player's cam,while using the radar built in the in-game Terminal, by pressing some predefined hotkeys, such as:LeftArrow, RightArrow keys.

Pressing one of those keys automatically switches the radar cam to the chosen player's one without needing to type in the terminal the keyword "switch playerName".

![](https://github.com/kRYstall9/FastSwitchPlayerViewInRadarMOD/blob/master/Switching%20Cam%20-%20Made%20with%20Clipchamp.gif)

## Change Log

* ### 1.3.2 (Latest)
    - Addressed an issue that was causing a conflict with the "ExtraDaysToDeadline" mod
      
* ### 1.3.1 
    - Addressed a case where misspelling "view monitor" or typing it backwards resulted in radar map successfully loaded but the user was not able to switch cams

* ### 1.3.0
    - Mod now fully supports the v45 of the game.
    - The user can now choose which hotkey to use through the settings -> keybinds menu

* ### 1.2.1
    - Addressed an issue where sometimes the cam wouldn't switch to the next or previous player
  
* ### 1.2.0
    - Removed Terminal Clock due to conflicts with other mods.
    - Handled client disconnection in order to correctly update the list of players that can be displayed in the terminal
    - Addressed an issue where placing the same radar booster more than one time resulted in storing the same radar booster that many times
 
*  ### 1.1.0
    - Added a clock on the top-right corner of the Terminal
    - Fixed a bug where being alone in a server resulted in some ArgumentOutOfRangeException while trying to switch radar map in the terminal
    - The clock text comes with 3 different colors:
      - Green (Default)
      - Orange (In the afternoon the clock turns orange)
      - Red (In the evening and night the clock turns red)
      -  Each color is swappable by changing the Hex Color Code inside the config file having the name of this mod.

* ### 1.0.3
  - Radar boosters, like players, are now visible in the terminal map
    
* ### 1.0.2

  - Bindable keys are now 2. The default binded keys are LeftArrow and RightArrow. LeftArrow let's you switch to the previous player's cam. RightArrow let's you switch to the next player's cam.
  - Cam is swappable without needing to type the keyword "view monitor" whenever the user leaves the terminal and then re-opens it.
 
## ~~Some ideas that might be "good to have" in game~~
- ~~[x] Clock displayed on the terminal~~
- ~~[ ] Doors keyword (Opens or Closes the ship's doors)~~
- ~~[ ] Ship loot value displayed on the terminal~~
- ~~[ ] Moon name's red if you can't afford to buy the route, otherwise green~~

## Suggestions | Bug Reports

If anything comes to your mind and want it to be added to this mod, or if there are some bugs popping out, feel free to join [this discord](https://discord.gg/Zhp4jB9u) and leave a comment [in this channel](https://discord.com/channels/1168655651455639582/1181265352911503430).