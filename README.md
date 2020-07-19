# Unlimited Map Memory Mod
This is a very simple and small mod for [Cataclysm: Dark Days Ahead](https://github.com/CleverRaven/Cataclysm-DDA/).
It adds a zero-cost mutation to character creation screen, which disables the limit of your character's map memory, 
allowing you to retain information about terrain you've seen, no matter your character's intelligence stat.

Because this mutation only affects map memory and not skill rust, I opted not to add conflicts with the 'Forgetful'
or 'Good Memory' mutations. These mutations--or any others that modify the internal map_memory_capacity_multiplier 
variable--will not have an effect on your character's map memory as long as the unlimited map memory mutation is active.

Tested and made for version **0.E#10478**

This mod should work in all future versions of the game, as long as the way map memory works does not change.

NOTE: this mod may have a negative effect on your performance, although I have not noticed any during tests.

## Installation
1. Download or clone this repository
1. Copy the the `unlimited_map_memory` from this repository into `data/mods/` of your installation of cdda

The mod will now be available for selection when creating a new world.

If you'd like to use it with an **existing world/save**, after completing the above steps, do the following:
1. Locate the save folder of your world ('save/{name-of-your-world}/'
1. Open the `mods.json` file in a text editor
1. Add a comma to the end of the line of the last item between the square brackets
1. Create a new line after that item and paste `"no_map_capacity_limit"` there (no comma on the end of this line)
1. Save the file

Afterwards, simply load your save and add the mutation using the in-game [debug menu](http://cddawiki.chezzo.com/cdda_wiki/index.php?title=Debug_Menu).
