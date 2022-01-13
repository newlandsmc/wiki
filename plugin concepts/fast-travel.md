# Fast Travel

## Overview

Staff can set locations around the world as "waypoints" Players must visit a waypoint to unlock it, and then they can teleport there in the future. Uses a GUI for player interface.

## Behavior

Players can open a GUI with `/fasttravel` to see waypoints. All players can see all waypoints. Waypoints are "locked" by default and cannot be USED by players. The icon for the waypoint will be gray_dye if it is locked. Clicking a locked waypoint should do nothing (keep the GUI open)

A player must visit the location of the waypoint to unlock the waypoint. To reduce lag, you should only check if the player is in the right location to unlock a waypoint when they crouch. There should be a configurable radius around the waypoint in which they can crouch to unlock the waypoint (this way they don't need to be standing in the EXACT right location). After a player has visited a waypoint, the icon in the GUI will change, and then they can click it to teleport there. There should be a configurable delay before teleporting (default 5 seconds) and should cancel if they move or take damage (**looking around doesn't count as moving**).

The icon, title, and description of a waypoint should be configurable. The title should support color codes, minimessage is good. If a waypoint is locked, the plugin should make the title and description both gray and have `<red>Locked! - visit <x> <z> to unlock.` at the bottom of the description. The description should be white if the waypoint is unlocked.

A command in-game should be included for creating a waypoint, but I do NOT need or want a full in-game editor. The in-game command should let staff do "/fasttravel create <name>" and then a config entry will be created with a default icon and description, so we can go into the config later, find the new entry, and customize it to our liking. The default icon can be a grass_block and the default description can be "Coming Soon!".

## Commands

- \/fasttravel create <name> - fasttravel.create - create new waypoint
- \/fasttravel - fasttravel.use - open GUI
- \/fasttravel help - display help, no permission

Please make /warp and /waypoint aliases so we could do `/warp` to open the gui or even `/warp create <name>` for example.

## Messages

All messages should be configurable
  
- Message for teleport delay starting ("\<yellow\>Teleporting in 5 seconds, don't move...")
- Message for teleport commencing ("\<yellow\>Teleporting...")
- Message for teleport cancelled (on move) ("\<red\>Pending teleportation request cancelled.")
- Message for waypoint created ("\<green\>New waypoint <name> created. Open config to modify.")
- Message for waypoint already exists ("\<red\>A waypoint with that name already exists.")
- Message for access denied to command ("\<red\>You do not have permission to do that.")
- Message for unlocking a waypoint ("\<green\>You discovered %waypoint_name%! Now you can teleport to this waypoint!")
- Message for waypoint locked (don't close GUI) ("\<red\>You must visit this location to unlock this waypoint.")

## Config

main config:
- messages
- radius around warp to unlock
- GUI customization

in /data folder:
- config for all waypoints
- user data for what waypoints each user has unlocked

## Notes

**Squaremap Support:**
  
All waypoints should be marked on the map with an icon at their exact coordinates.

**References (existing plugins that appear to be what we want):**

https://git.lumine.io/mythiccraft/mmocore/-/wikis/Waypoints

https://www.spigotmc.org/resources/fasttravel.13231/

https://www.spigotmc.org/resources/cybertravel-%E2%9C%A8-discover-regions-%E2%9A%A1-teleport-back-%E2%9A%A1-fast-travel-%E2%9A%A1%E3%80%8C1-8-1-17%E3%80%8D.94603/
