# To Do:

## Configuring
- Configure rewards in Expeditions
- Configure MythicMobs _- started by Sarah_
    - Figure out mcMMO integration with MythicMobs
- Create premium ranks and add them to the store _- started by Braydon_
    - Need names, art, and prices
- Improve loot chests with datapack _- started by Sarah_

## Coding - improvements:

- Fix JoinHandler plugin _- started by Cookie_
    - player name variable doesn't work in leave messages
    - Schematic doesn't spawn on player join when using JakesRTP
- Improve story messages
    - Add blank lines between story messages
    - Mute chat during story messages
    - Add "use /skip to skip" message during story messages (where/how will this be added?)
- Improve DisableAdvancement plugin _- started by Destro_
    - Add config for adding any Gamerule we want to set and the desired value
    - Rename to "GamruleManager"
- Improve CustomMOTD plugin _- started by Destro_
    - Update to 1.18.1
    - Fix commands
    - Improve counter system (multiple potential counter-based MOTDs somehow?)
- Remove trailing colon from mentions in ChatCore
- Rename "SemiCore" to "CookieCore"


## Coding - new:
- Write CustomPVP plugin
- Write plugin for EnderDragon modifications
    - EnderDragon respawns on a random island
    - Configurable range to look for a new spawn location
    - Configurable cooldown between respawns
    - Compasses in the end point to the dragon
- Write new AFKDetector plugin
    - Updated AFK pool detection
    - Fix known exploits
    - Rename to "AdvancedAFK"
- Write player-tracker plugin
    - Custom in-game item can be given to players (glowing Compass with custom name/description)
    - Custom item points to nearest player once activate (right click)
    - Custom time that the item lasts before it's used (60 seconds then it's removed from the player's inventory - maybe use item durability for this?)
    - Command to give players this item
- Find/write a plugin for warps
    - Allows players to warp to location AFTER they have "discovered" it
    - Some sort of cost so they can't spam it?
    - GUI - always show all warps and have an icon for ones not yet discovered
- Write plugin to discourage breaking spawners & loot chests
    - Slow down the action and print a message informing the player of why they should do that?
 
## Testing:

- Test Expeditions plugin for exploits
- Test mcMMO leveling
- Test mcMMO exploit fixes


--------------------


## Outdated To-Do List:

- ~~Need plugin for custom join/leave messages~~
- ~~Need plugin for custom MOTD & changing MOTD real-time~~
    - Update CustomMOTD plugin
- ~~Need plugin to disable advancement announcements on every startup~~
    - Update DisableAdvancement plugin
- ~~Need plugin for advanced AFK detection ?~~
    - Update AFKDetector plugin
- ~~Need plugin for auto-respawn on death~~ --- Cancelled since players will respawn at their home it might not be safe.
- Define blocked words in ChatCore
- Customize chat formats in ChatCore (for staff chat and what not)
- How to make money - ranks, nicknames, what else?
    - 3 ranks - $10, $20, $30
    - Player trackers - $5 for 5
    - Pay to vote - $100 to get the daily reward forever
- ~~Find a land protection plugin~~
    - ~~Configure GriefPrevention~~
- ~~Fix respawning at player's home~~
- Need plugin for boss mobs
- Need plugin for custom pvp
- Need plugin for real sleep
- Need plugin for vote rewards (ADD TO REJOIN REWARDS - RENAME TO "EXPEDITIONS"?)
- ~~Need plugin for rpg levels~~
- Need plugin for player trackers (PTW item)
- ~~Change MOTD to be pastel colors~~
- ~~Discuss custom crafting recipes~~
- Figre out how to handle staff wanting to play
    - Staff enable/disable command ? 
- Figure out claim limits and buffers
    - Staff will give you more claim blocks if you need them, not automated
    - Can we have a buffer around claims and notify players if they are building too close to someone else
- Do we need a worldborder? Do we need to pre-render the world? 
- ~~Set up player permissions~~
- Establish rules around limited resources
    - You can't restrict access to end portals
    - 30 second delay breaking spawners and chests with a message asking them not to? 
    - Regenerating chunks in end and nether?
- Figure out how to prevent buff abusing (from pvp)
    - Make buff damage only apply to players
