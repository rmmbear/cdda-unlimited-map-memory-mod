# Update: 2021/05/20
This mod has been made **obsolete** for experimental builds of CD:DA as per https://github.com/CleverRaven/Cataclysm-DDA/pull/47253 
(though it can still be used in previous stable releases).

Same goes for [C:BN](https://github.com/cataclysmbnteam/Cataclysm-BN), which has gotten
rid of the memory limit quite some time ago https://github.com/cataclysmbnteam/Cataclysm-BN/pull/247


## Unlimited Map Memory Mod
This is a very simple and small mod for [Cataclysm: Dark Days Ahead](https://github.com/CleverRaven/Cataclysm-DDA/) 
It adds a zero-cost mutation to character creation screen, which disables the limit of your character's map memory,
allowing you to retain information about terrain you've seen, no matter your character's intelligence stat. It works 
by setting the internal `map_memory_capacity_multiplier` variable to a negative value. 

Because this mutation only affects map memory and not skill rust, I opted not to add conflicts with the 'Forgetful'
or 'Good Memory' mutations. These mutations--or any others that modify the map_memory_capacity_multiplier--will not
have an effect on your character's map memory as long as the unlimited map memory mutation is active.

Tested on, and made for version Ellison-3 (**0.E#10478**)

This mod should work in all future versions of the game, as long as the way map memory works does not change.

NOTE: this mod may have a negative effect on your performance in the long run, especially in low-memory environments.

## Installation
1. Download or clone this repository
1. Copy the the directory named `unlimited_map_memory` from this repository into `data/mods/` of your installation of cdda (symbolic link also works)

The mod will now be available for selection when creating a new world.

If you'd like to use it with an **existing world/save**, after completing the above steps, do the following:
1. Locate the save folder of your world ('save/{name-of-your-world}/'
1. Open the `mods.json` file in a text editor
1. Add `"unlimited_map_memory"` to the list (ensure the file follows JSON syntax after your modification)
1. Save the file

Afterwards, simply load your save and add the mutation using the in-game [debug menu](http://cddawiki.chezzo.com/cdda_wiki/index.php?title=Debug_Menu).
