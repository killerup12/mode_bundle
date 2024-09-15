**0.5.2**
- Fixed visor rim positioning wrong while using TerminalDesktop.
- Fixed blood splatter not clearing immediately after dying.
- Blood splatter won't happen anymore when damage inflicted was zero.

**0.5.1**
- Fixed config not working correctly.

**0.5.0**
- Added an option to choose between post processing visor and physical visor.
- Added an option to stretch visor.
- Physical visor now gets affect by game's Depth Of Field effect.
- Config updated.

**0.4.8**
- Fixed post processing sorting problem.
- Fixed pixelate effect stretching.
- Added RaindropIntensity option.
- Minor shader changes.

**0.4.7**
- Fixed visor rim not showing with HDLethalCompany EnablePP set to false.
- Optimized visor rim.

**0.4.6**
- Fixed visor still being visible in 3rd camera.
- Fixed RimShow option not working.

**0.4.5**
- Change post processing visor rim to physical visor rim.
- Added options to pixelize Raindrop/BloodSplatter/Crack effects.

**0.4.4**
- Fixed raindrop dry time option not working;

**0.4.3**
- Fixed visor rim appearing wrong.

**0.4.2**
- Fixed cause of damage check for crack and blood splatter not working.

**0.4.1**
- Fixed blood splatter not scaling accurately.
- Added blood splatter self option.
- Added randomness to splatter position.

**0.4.0**
- Added blood splatter effect (Very primitive at the moment).
- Added an option to make raindrops last longer when fully disappearing.
- Fixed crack effect not showing with cetain mods.

**0.3.4**
- Optimized raindrop effect.
- Fixed post processing volume error when quitting.
- Fixed visor crack intrupting OpenBodyCams and other camera mods.
- Added an option to display raindrop only on player's view.
- Visor rim on ultrawide stretches more accurately.

**0.3.3**
- Views through OpenBodyCams now displays raindrops too.
- Fixed camera blacking out / shaders not working when going third person through other mods.
- Fixed main menu background not clearing when quitting to main menu.
- Fixed visor breaking no matter the health and playing breaking sound effect on every hit taken.
- Changed default visor condensation image to not appear when looking up in rainy weather.
- Changed visor rim to not stretch on ultra wide resolutions.

**0.3.2**
- Raindrop effect now works with OpenBodyCams by Zaggy1024.
- Fixed visor crack level going higher than max value.
- minor bug fixes.

**0.3.1**
- Fixed the deafult visor coming back after going third person.
- Fixed visor rim shader appearing wrong in ultra wide resolutions.
- Changed assetbundle name to avoid conflicts.

**0.3.0**
- Added raindrop effecf
- Added visor rim effect. This disables the mesh that surrounds the camera and replace it with post processing effect.
- Changed crack effect pattern.

**0.2.1**
- Fixed post-process effect not showing.

**v0.2.0**
- Version number naming reverted
- Fixed visor not checking if it was the local player was getting attacked.
- Fixed visor not repairing for non-host when quota was fulfilled.
- Adjusted glass shader to be less noisy.
- Circular crack pattern removed temporarily.

**v0.1.601**
- Changed version number naming format.
- Fixed compatibility issue with MirrorDecor by quackandcheese.
- Added a config option for visor breaking SFX volume.

**v0.1.6**
- Fixed version number and some typos.
- Using emote won't cycle through cracks anymore.

**v0.1.5**
- Added crack variant Vertical. Previous is Circular. You can change between them through config. This option is ON by default.
- Added configs for setting when the visor will get repaired ( New Day / Death / Quota Fulfilled ).
- Fixed the default LocalVolumetricFog on Rend/Dine not being visible through the visor.

**v0.1.2**
- Changed glass material to use simple custom shader. They won't obscure view too much under lights now.
- Added compatibility for FOV Adjust mod by Rozebud.

**v0.1.0**
- Added screen cracking effect depending on your health. Visor won't crack for taking damages caused by Abandoned/Drowning/Electrocution/Suffocation