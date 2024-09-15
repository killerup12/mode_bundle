# 1.5.9
- Fixed maneater not playing hit sounds when the death animation occurs
- Fixed snare fleas screeching after death if they are killed right as they drop from the ceiling
- Fixed "Hey" voice when the ship is struck by lightning
- Reduced most logs from "Info" to "Debug" level
# v1.5.8
- Cruiser gets muted a little earlier when heading into orbit (when the outdoor ambience ends, not after the results screen)
# v1.5.7
- Fixed the snare flea sometimes still playing sounds after death (after a change made in v1.5.3)
# v1.5.6
- Fixed maneater still making noises after being killed
# v1.5.5
- Cruiser tire audio no longer plays when the car is airborne (like from turbo boosts), not just when attached to the magnet
# v1.5.4
- Fixed Cruiser tires still making certain noises (skidding, rolling over gravel) while attached to the magnet
- Cruiser alarm no longer plays while attached to the magnet (since the ship can't take damage)
- Fixed baboon hawks still playing their attack sound when walking over a corpse
- Added a config setting to mute the Cruiser in orbit
  - By default, this will mute everything except for the radio
# v1.5.3
- Cruiser sound fixes
  - Fixed the "engine stalling" sound still playing when releasing and twisting the key again
  - Fixed the engine rev sound effect playing multiple times when twisting the key too quickly
  - Fixed the engine rev sound effect continuing after the engine starts up
  - Fixed collision sounds restarting instead of stacking
- Fixed volume fade of flaming giant effects
- Fixed several enemies not playing hit sounds when their death animation occurs
  - Brackens
  - Hoarding bugs
  - Eyeless dogs
# v1.5.2
- Tulip snakes now play hit sound when killed
- Fixed kidnapper fox drooling after being killed
# v1.5.1
- Fixed hardlock when attacking the kidnapper fox
# v1.5.0
- Some fixes for kidnapper fox
- "BetterMimicSteps" config setting to make mimics' footsteps better match players'
# v1.4.0
- Some more fixes for dogs
  - Retooled the pitch fix from v1.3.0
  - Voice pitch should now synchronize for all players who install this mod
  - Fixed overlapping breathing sounds coming from the same dog
  - Fixed breathing sound stopping sometimes after killing players
  - Added hit sound (like with forest giants)
- Fixes for tulip snakes
  - Fixed "scurrying" sounds continuing after latching to a player's head
  - Fixed randomized pitch for scurry sounds
  - Fixed some edge cases where dead tulip snakes would still make noise
  - Added hit sound
- "Fixed" thumpers playing thunder sounds from their voice when de-aggroing
  - Made this a config setting, because I'm still not 100% sure this is unintended
- Enemies no longer play hit sounds if another enemy hits them after they are dead
- Fixed old "DontFixMasks" option still showing up in the config under certain circumstances
# v1.3.0
- Dogs no longer continue breathing after they die
- Fixed dogs using the wrong voice pitch after they finish eating a player
# v1.2.4
- Butler corpses no longer buzz
# v1.2.3
- Inverted "DontFixMasks" option to "FixMasks" option, which I think is more intuitive
  - Your config should be updated automatically to use the proper setting
- Snare flea death scream is no longer random pitch
# v1.2.2
- Fixed a potential nullref exception with animated particles.
# v1.2.1
- Fixed a bug that caused certain animated map objects to not play audio (in vanilla, that would be garage door on Experimentation)
# v1.2.0
- Fixed mask items and enemies not playing laugh/cry noises as often as they are supposed to.
# v1.1.2
- Fixed fall damage for players using the wrong SFX (unless you crash a jetpack)
# v1.1.1
- Forest keeper "eating fixes" now apply when you teleport a player out of their hand
# v1.1.0
- Polish pass on forest keepers
- Reworked some snare flea code (to fix a broken patch that I replaced last minute before release)
# v1.0.0
- Initial release