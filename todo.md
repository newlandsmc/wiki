# To Do:

## Configuring
- Configure rewards in Expeditions
- Configure MythicMobs _- started by Sarah_
    - Design mobs
    - Code mobs
- Learn and tweak Aurelium as needed
- Create Aurelium custom MOTD when CustomMOTD plugin is finished
- Configure buycraft items to run customMOTD commands

## Coding - improvements:

- Improve story messages
    - Mute chat during story messages
- Fix Expeditions
    - Cannot add reward items to existing stacks of that item in inventory
    - Duplicate rewards under certain conditions
    - Implement "instant expeditions" (voting and premium reward)
- Improve DisableAdvancement plugin _- started by Destro_
    - Add config for adding any Gamerule we want to set and the desired value
    - Rename to "GamruleManager"
- Improve CustomMOTD plugin _- started by Destro_
    - Update to 1.18.1
    - Fix commands
    - Improve counter system (multiple potential counter-based MOTDs somehow?)

## Coding - new:
- Write/find Commandspy plugin _- not needed for launch_
- Write CustomPVP plugin
- Write plugin for EnderDragon modifications
    - EnderDragon respawns on a random island
    - Configurable range to look for a new spawn location
    - Configurable cooldown between respawns
    - Compasses in the end point to the dragon
- Write player-tracker plugin _- not needed for launch_
    - Custom in-game item can be given to players (glowing Compass with custom name/description)
    - Custom item points to nearest player once activate (right click)
    - Custom time that the item lasts before it's used (60 seconds then it's removed from the player's inventory - maybe use item durability for this?)
    - Command to give players this item
- Find/write a plugin for warps _- low priority_
    - Allows players to warp to location AFTER they have "discovered" it
    - Some sort of cost so they can't spam it?
    - GUI - always show all warps and have an icon for ones not yet discovered
- Write plugin to discourage breaking spawners & loot chests _- started by Destro_
    - Slow down the action and print a message informing the player of why they should do that?
- Design and write custom placeholder plugin _- not needed for launch_
 
## Testing:

- Test Expeditions plugin for exploits
- Test buycraft subscription cancellation (ticket open with Buycraft)

--------------------


## Outdated To-Do List:

- Figre out how to handle staff wanting to play
    - Staff enable/disable command ? 
- Figure out claim limits and buffers
    - Staff will give you more claim blocks if you need them, not automated
    - Can we have a buffer around claims and notify players if they are building too close to someone else
- Do we need a worldborder? Do we need to pre-render the world? 
- Establish rules around limited resources
    - You can't restrict access to end portals
    - 30 second delay breaking spawners and chests with a message asking them not to? 
    - Regenerating chunks in end and nether?
